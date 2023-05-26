---
layout: default
title : Technical Overview
header : Technical Overview
group: navigation
subnavgroup: overview
order: 0
---
{% include JB/setup %}

HORUS will provide three distinct types of computational nodes, co-located with existing OSiRIS storage infrastructure and connected to an existing 100 Gbps research network. open source software makes the resource broadly available, including to researchers outside the region via the OSG/PATh sharing described below.

## Hardware

We have identified three types of computational servers that can allow us to support a broad range of use-cases: compute servers for high-throughput, compute servers for large memory, and compute servers for GPU tasks. The table below summarizes the characteristics of each.

### HORUS Computing System Details

<table class="styled-table">
    <thead>
        <tr>
            <th>Horus Systems</th>
            <th>Model</th>
            <th>Mem (G) / Host</th>
            <th>CPU</th>
            <th>CPU Cnt</th>
            <th>GPU</th>
            <th>GPU Mem</th>
            <th>GPU/Host</th>
            <th>NICs</th>
            <th>Host Cnt</th>
            <th>HT Job Slots (total)</th>
            <th>Mem (G) / Slot</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>GPU Node</td>
            <td>Dell R750xa</td>
            <td>512</td>
            <td>Xeon Gold 6334 8C/16T</td>
            <td>2</td>
            <td>A100</td>
            <td>80G</td>
            <td>4</td>
            <td>2x25G</td>
            <td>4</td>
            <td>128</td>
            <td>16.0</td>
        </tr>
        <tr>
            <td>Large Memory Node</td>
            <td>Dell R6525</td>
            <td>1024</td>
            <td>AMD Epyc 7F72 3.2GHz, 24C/48T</td>
            <td>2</td>
            <td>-</td>
            <td>-</td>
            <td>-</td>
            <td>2x25G</td>
            <td>10</td>
            <td>960</td>
            <td>10.7</td>
        </tr>
        <tr>
            <td>Compute Node</td>
            <td>Dell R6525</td>
            <td>512</td>
            <td>AMD Epyc 7H12 2.60GHz, 64C/128T</td>
            <td>2</td>
            <td>-</td>
            <td>-</td>
            <td>-</td>
            <td>2x25G</td>
            <td>10</td>
            <td>2560</td>
            <td>2.0</td>
        </tr>
    </tbody>
</table>

Dynamic partitioning of server resources is expected to be a main feature. For example, some of our GPU users simply need a single CPU and associated memory to match the total memory of a GPU. A server with four GPUs would only require assigning four hyper-threaded CPUs and about 320G of memory, leaving 28 CPUs and 192G of memory idle. We need to be able to dynamically make those CPUs and memory accessible for other jobs that just require one or more CPUs and a smaller amount of memory.

OSiRIS combined with HORUS makes a great enabler for many of the science domains in the project. Currently, OSiRIS has approximately 6 Petabytes of raw storage available for use, out of 13.5 Petabytes deployed. Using erasure-coding techniques (8+3), the 6 Petabytes translates into roughly 4.3 PB of usable space that did not need to be paid for by HORUS.

## High-Performance Network

A high-speed research network was created as part of the OSiRIS project (see Figure 1 below). This network, combined with Merit’s regional network, will support access to HORUS compute resources by educational institutions throughout Michigan and beyond. This network is highly resilient and features multiple 100 Gbps links internally and 100 Gbps connectivity to Merit and the wide-area network.

Merit’s core strength is enabling researchers, educators, and learners to transfer critical data across its high capacity optical network in a safe, secure environment. Merit’s network is designed with resiliency within its core network to our campuses and out to the national and global research communities. With Merit’s next-generation network, HORUS creates a high-capacity compute research platform across three campuses and makes it available to researchers throughout Michigan and the region.

<img src="{{IMAGE_PATH}}/horus-network.png" alt="Horus Network" width="100%" />
<p style="text-align: center; font-size: 0.875em;"><strong>Figure 1:</strong> The network that HORUS uses features multiple 100 Gbps resilient network links. It is well-connected to both the Merit network and broader global research and education networks. Note that HORUS equipment will be directly connected to the “gray” boxes at top and bottom of the diagram (MSU, UM or WSU, e.g., um-sw01 or wsu-sw02, etc).
</p>



## Software

The HORUS team has extensive experience operating cyberinfrastructure for researchers. Besides the work on OSiRIS, team members have designed and operated infrastructures such as the ATLAS Great Lakes Tier-2 for high-energy physics, the ICER infrastructure at Michigan State University, and Wayne State University's computing center.

The HORUS team made use of available open source software, typically deployed in grid sites and data centers. The system was developed with researchers in mind:

- Easy to submit work and track jobs
- Fair sharing of resources
- Dynamic partitioning of resources to suit varying job sets
- Resource accounting and system metrics

### Building Blocks / Open Source Components

HORUS uses software to adhere to its guiding principles of fairly sharing resources among users and maximizing the use of resources. The HORUS software architecture builds on a number of open source tools and applications, grouped by their particular role.

__Authentication and Authorization__

- __InCommon__, a set of community-designed identity and access management services
- __CoManage__, identity lifecycle management
- __Grouper__ for creating and managing roles, groups, and permissions
- __CILogon__, for logging on to cyberinfrastructure

__Resource allocation and management__

- __HTCondor__, used to manage fair-share access for computational tasks
- __HTCondor-CE__, a meta-scheduler used as a “door” to a set of resources
- __NVIDIA MIG__, used to subdivide a GPU (cores and memory) into up to seven smaller       instances, allowing more jobs to share a GPU
- __Ceph__, with quotas to manage storage use in OSiRIS

__Monitoring and Accounting__
- __Elasticsearch__, gathers data from syslogs and other sources for aggregation, visualization, analytics, and correlation
- __CheckMK__, intelligent server and host monitoring system capable of validating service states and tracking resource usage
- __perfSONAR__, used to test and monitor network behavior across infrastructure
- __RHEL8__, for accounting and auditing to augment usage and security information

Deployments of many of these tools (CoManage, Grouper, Elasticsearch, CheckMK, perfSONAR) already were in place for OSiRIS and have been reconfigured to accommodate HORUS. HTCondor is the HORUS batch scheduler, used with OSG/PATh to configure the appropriate connection to users' hosted Compute Element (CE) based upon HTCondor-CE. The HTCondor services, as well as all other required HORUS services, will rely on the virtualization platform already in place for OSiRIS. This virtualization platform includes four powerful virtualization hosts at each of our sites (UM, MSU, WSU) running libvirt. In addition, we have access to SLATE infrastructure, which provides the ability to orchestrate containers via Kubernetes if particular tools or jobs would benefit from that.
