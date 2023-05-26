---
layout: default
title : Use Cases
tagline: Horus
header : Use Cases
group: navigation
order: 1
---
{% include JB/setup %}

The following projects have driven the development of HORUS and point to the types of use cases others may apply. A summary table also defines the computing details and requirements for each of these projects.

__Material Simulation — University of Michigan__: Explores material properties by running material simulation applications using so-called integral files (typically 1-2 TB each) to do computation. With recent GPU optimization, the bottleneck for certain calculations is now completely related to the I/O efficiency, especially when one considers disorder (where hundreds of 1-2 TB files are used in each simulation). For HORUS, it will be interesting to see how these codes perform with quick read access to multiple such files in OSiRIS storage. This discipline is well matched to HORUS GPU use in parallel with the OSiRIS storage.

__Pritzker Neuropsychiatric Disorders Research Consortium__: The Pritzker Consortium aims to 1) discover neurobiological and genetic causes of major depression, bipolar disorder, and schizophrenia 2) identify biomarkers for better diagnosis and novel targets for their treatment. The Consortium involves researchers from several institutions including Cornell, Stanford, UC Irvine, HudsonAlpha Institute for Biotechnology, and the University of Michigan. This area of work has significant computational and data challenges.

__Van Andel Institute__: Van Andel Institute hosts a busy genomics facility that is used heavily both internally and by neighboring regional collaborators in West Michigan (such as Michigan State University). Last year nearly $1 million of mainly genomics services was provided to external partners (mainly MSU). This effort represents dozens to hundreds of TBs of unique data to be analyzed and transformed, which is a challenge to move and even harder to analyze. The analyses required are each a special challenge, requiring a mix of central VAI computation mixed with those of the individual customers (researchers).

__Cryo-EM__ — University of Michigan: Single particle cryo-electron microscopy allows scientists to determine the atomic structure of biological macromolecules. Given that the 3D structure of a protein determines its function, understanding the structure of proteins allows structural biologists to understand basic biology, evolution, human health, and disease. At UM, computing and storage is a huge bottleneck for cryo-EM researchers on campus. Currently, each lab that uses cryo-EM instruments needs to accommodate their own storage and computing, which means each lab has local workstations. A centralized compute-resource and data storage would be a boon for the campus. Existing solutions are not optimal for a large number of users. On campus, more than 30 laboratories are using the UM Cryo-EM resource.

__Evolutionary Genomics__ — Oakland University: This discipline explores deep evolutionary histories (e.g., early life evolution) which require large-scale simulations and analyses of empirical data. These kinds of analyses use Maximum Likelihood and Bayesian approaches that require extensive computational time, even in a parallelized environment. Additionally, the reconstruction of ancient phylogenetic events are highly dependent on assumptions and priors given at the start of the analyses. Extensive hypothesis-testing to determine the robustness of results to these assumptions is required. Additional centralized computational resources and data storage are key to continue this line of research at Oakland University and to grow its reach over time (e.g., ancestral state reconstructions).

__Network Telescope — Merit__: Network telescopes, or darknets, consist of networking instrumentation that receive and record unsolicited internet traffic destined to large swaths of unused IP space. Internet traffic destined to this "dark IP space" is inherently suspicious since no real user services are hosted in the IP space monitored by the darknet. Thus, darknets provide a unique vantage point to computer networking and cybersecurity researchers for studying internet-wide scanning activities, distributed denial of service attacks, misconfigurations, and even network outages. Merit operates one of only two large network telescopes in the country and maintains an archive of darknet data dating back to 2005. Currently, Merit's darknet collects more than 100 GB of compressed PCAP data daily, and the archive exceeds 500 TB. Processing the telescope data is challenging because of the large amounts of CPU, memory, and storage required. Tasks include: 1) longitudinal studies, 2) performing annotations with external, third-party data sources (e.g., Censys.io, historical DNS data, etc.), and 3) employing ML/AI/statistical techniques for data clustering, predictive analytics, inference, anomaly detection, and other applications.

__Population Health Informatics — Oakland University__: This discipline involves multiple research projects using natural language processing and machine learning for biomedical and healthcare analytics. Heterogeneous datasets include massive amounts of unstructured textual data as well as alphanumeric tabular data and image data. Natural language processing is GPU-intensive; currently, the relatively few number of GPU nodes result in extended wait times for jobs in the queue to start running.

__Oakland Genomics Oleksyk Lab — Oakland University__: Genomic analysis on a population scale often operates with extensive volumes of data and requires multi-step heterogenous (cpu/IO intensive) analysis. For example, a basic population genomics dataset of 100 samples amounts to an estimated 9 TB of data and 60 billions of short unassembled reads. During the initial steps of this analysis (sequence alignment and variant calling) the total dataset temporarily triples in volume. In addition to the approaches to optimize the later downstream analysis, some of the approaches in the field (i.e. population structure using dense sequencing data analysis) involve model-based Bayesian clustering and similar computationally intensive data. The requirements for storage, IO, and CPU increases and expands with every additional step used for comparative analyses of multiple populations that involve thousands of samples. Additional data storage and storage-lenient computational resources would allow Oakland University and our laboratory to stay current with the demands of big data analysis, enable use of the latest computational instruments, and further promote research and collaboration with other groups in the field.

__Autophagic Body Modeling — Eastern Michigan University__: Autophagic body modeling is an important tool for improving our basic understanding of the process of autophagy, a conserved intracellular recycling pathway important for human health. We measure the size and number of autophagic bodies formed in yeast with altered levels of key autophagy proteins. Accurate estimation of the original size and number of autophagic bodies from random TEM sections requires the use of a simulation to compare with the actual data. We are developing improved versions of this simulation that use CompuCell3D (CC3D) to model the bodies as more realistic non-spherical shapes. Currently, a single CC3D run takes ~1 hour on a laptop, but our automated workflow will require thousands of runs to generate enough simulated data for statistical accuracy.

__JETSCAPE — Wayne State University__: The JETSCAPE collaboration (jetscape.org) is a consortium of about 50 researchers from 14 institutions in the US, Canada, Japan, and Germany, including physicists, computer scientists, and statisticians. The collaboration develops simulation frameworks for the simulation of very high energy nuclear collisions. These collisions carried out at the Brookhaven National Lab. and at CERN produce nuclear-sized exploding droplets of matter that reach temperatures over 3 trillion degrees Celsius. The software is made available to the worldwide community via Github. However, these simulations are extremely compute-intensive. From time to time, the collaboration will compete for and receive computing allocations to carry out large-scale simulations and compare with experimental data. However, the typical allocations fall far short of the required time; hence, the collaboration has divided the simulation into several stages which can be simulated separately. The results of the earlier stages are then stored in large storage facilities such as OSiRIS where they can be retrieved to carry out the later stages of the simulations. HORUS will provide needed resources for the collaboration as well as a mechanism for broader access to the models and datasets.

__Heavy-Element Quantum Chemistry — Oakland University__: Successful heavy-element chemistry depends on the availability of powerful tools of theoretical chemistry to predict the non-trivial behavior of the elements at the bottom of the periodic table. The development of reliable infrastructure (basis sets, force fields, density functionals) for predictive relativistic quantum-chemical modeling of complex chemical systems — involving actinides, heavy main-group, and superheavy elements — relies on a readily accessible computing facility with hundreds of CPUs, including large-memory nodes, and massive and fast scratch space. The continuation of this line of research at Oakland University is predicated on sustainable maintenance and growth beyond the current high-performance computing cluster in the wake of an influx of new STEM faculty with growing demands for expansive parallel computing.

__Certificate Program in Data Science — Oakland Community College__: The Data Science Certificate is designed to provide a strong foundation for data investigation, including data wrangling, cleaning, security, regression and classification, prediction, and data communication. It will be a 35-hour program including Python, R programming for data science, machine learning, big data, and NoSQL. OCC needs easy-to-use compute, storage, and software resources to provide a broad introduction to the exploding field of data science.

## HORUS Science Driver Summary


<table class="styled-table">
    <thead>
        <tr>
            <th>Science Description & Challenges</th>
            <th>Resource Types</th>
            <th>Codes</th>
            <th>Core Range</th>
            <th>Runtime Range</th>
            <th>Memory</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>
                <strong>Materials Simulation — University of Michigan</strong> : Explores materials and their behaviors by running detailed simulations requiring large input datasets and optimized use of GPU and CPU resources
            </td>
            <td>
                GPU, CPU, I/O streaming, large inputs
            </td>
            <td>
                Green's function codes (green.physics.lsa.umich.edu)
            </td>
            <td>
                One iteration uses a full GPU and associated CPU core
            </td>
            <td>
                One iteration is one hour; need 10-100 iterations to complete the work
            </td>
            <td>
                Memory: 20-40 GB on GPU & replicated on CPU
            </td>
        </tr>
        <tr>
            <td>
                <strong>Pritzker Neuropsychiatric Disorders Research Consortium</strong>: Works to discover neurobiological and genetic causes of major depression, bipolar disorder, and schizophrenia, and to identify biomarkers for better diagnosis
            </td>
            <td>
                GPU, CPU, large inputs
            </td>
            <td>
                Neuroinfo, Imaris, Amira, Metamorph, Huygens image analysis, Halo, Volocity, Zen and Arivis, Image Pro Plus, ImageJ, Ilastik,Tarastitcher, STAR aligner, Portcullis, Matlab, Python, R
            </td>
            <td>
                Four cores using 32G
            </td>
            <td>
                Varies from several minutes to several weeks; majority of jobs are in range of several hours to a couple of days
            </td>
            <td>
                GPU: 16G/GPU CPU 8G/core
            </td>
        </tr>
        <tr>
            <td>
                <strong>Van Andel Research Center</strong>: Conducts diverse set of genomics research between the center and external collaborators; challenges include multi-TB size data and complex joint computation required to analyze the data
            </td>
            <td>
                CPU, large inputs, large outputs
            </td>
            <td>
                Illumina tools, Aligners, tertiary analysis tools, bio-statistical tools
            </td>
            <td>
                40 to 400 based upon sample sizes
            </td>
            <td>
                Hours to days
            </td>
            <td>
                Maximum of 256GB / server (4GB/core)
            </td>
        </tr>
        <tr>
            <td>
                <strong>Cryo-EM — University of Michigan</strong>: Single particle cryo-electron microscopy allows scientists to determine atomic structure of biological macromolecules; currently, computing and storage is a bottleneck for cryo-EM researchers on campus. Over 30 labs that use our cryo-EM instruments need to accommodate their own storage and computing
            </td>
            <td>
                Each project needs CPU, GPU and large input data
            </td>
            <td>
                RELION, cisTEM
            </td>
            <td>
                RELION: GPU jobs will use four GPUs plus any associated CPUs on the GPU node (typically 12-24 CPUs); cisTEM: 100 CPUs
            </td>
            <td>
                RELION: 0-24 hours; cisTEM: 0-3 hours
            </td>
            <td>
                CPU: 2-5 GB CPU RAM / core GPU: 12-24 GB / GPU
            </td>
        </tr>
        <tr>
            <td>
                <strong>Evolutionary Genomics — Oakland University</strong>: Explores deep evolutionary histories (e.g., early life evolution) which require large-scale simulations and analyses of empirical data using Bayesian and Maximum Likelihood techniques; additional centralized computational resources and data storage are key to growing this line of research at Oakland University
            </td>
            <td>
                CPU, large input data
            </td>
            <td>
                RAxML, BEAST, MrBayes, IQ-Tree, MCMCTree
            </td>
            <td>
                Single CPU per job
            </td>
            <td>
                Runtimes of 1-30 days
            </td>
            <td>
                2GB / core
            </td>
        </tr>
        <tr>
            <td>
                <strong>Network Telescope — Merit Network</strong>: Cybersecurity research using "darknets" record unsolicited internet traffic destined to large swaths of unused IP space, generating large amounts of data and the need for continual analysis
            </td>
            <td>
                GPU/CPUs, storage, memory, I/O streaming data
            </td>
            <td>
                Custom-built Go software, PyTorch, R/Python
            </td>
            <td>
                One core per hour of data gathered
            </td>
            <td>
                20-30 minutes per PCAP for Darknet event extraction
            </td>
            <td>
                128 GB / server
            </td>
        </tr>
        <tr>
            <td>
                <strong>Population Health Informatics — Oakland University</strong>: Multiple research projects using natural language processing and machine learning for biomedical and healthcare analytics; GPU-intensive and requiring large inputs
            </td>
            <td>
                CPU, GPU, high IOPs, large input datasets
            </td>
            <td>
                Python, MATLAB, R
            </td>
            <td>
                Typical job requires a CUDA supported GPU with >= 16G RAM
            </td>
            <td>
                Job runtimes may vary from several minutes to a few (1-2) days
            </td>
            <td>
                >=16G RAM per GPU and 16-64G CPU RAM per node
            </td>
        </tr>
        <tr>
            <td>
                <strong>Oakland Genomics Oleksyk Lab — Oakland University</strong>: Conducts genomic analysis on a population scale requiring extensive volumes of data and multi-step heterogenous (cpu/IO intensive) analysis
            </td>
            <td>
                High IOPs, CPU, GPU
            </td>
            <td>
                BWA, GATK, BEAGLE, fastPHASE, IMPUTEv2,bcftools, MACH, ShapeIT, CHROMOPAITER, fineSTRUCTURE and others
            </td>
            <td>
                Single CPU per job but typical work needs 200 jobs
            </td>
            <td>
                Varies: tasks from tens of minutes to 200-300 hours@128 cores for alignment and variant calling pipeline for 100 samples
            </td>
            <td>
                Majority of the tasks 2GB/core, some tasks 4GB/core
            </td>
        </tr>
        <tr>
            <td>
                <strong>Autophagic Body Modeling — Eastern Michigan University</strong>: Important tool for improving basic understanding of the process of autophagy; individual runs on a laptop take about one hour, but statistical accuracy requires thousands of runs
            </td>
            <td>
                CPU
            </td>
            <td>
                CompuCell3D, python
            </td>
            <td>
                Single CPU per job but requires thousands of jobs for a study
            </td>
            <td>
                Minimum runtime for a single simulation ~1 hour
            </td>
            <td>
                2-4 GB / core
            </td>
        </tr>
        <tr>
            <td>
                <strong>JETSCAPE — Wayne State University</strong>: Develops frameworks for the simulation of very high energy nuclear collisions; extremely compute-intensive and generating large datasets, making it challenging to acquire access to enough CPU and storage for collaboration
            </td>
            <td>
                CPU, large output datasets
            </td>
            <td>
                Physics codes in C++, statistical analysis codes in Python; general scripting for large-scale runs in Parsl (Python)
            </td>
            <td>
                Using a single thread on a single core, a single event would take 30 hours
            </td>
            <td>
                100-200M thread hours to calibrate the model; 17 unknown parameters to set
            </td>
            <td>
                Single event on a single thread will use a little over 2GB of memory
            </td>
        </tr>
        <tr>
            <td>
                <strong>Heavy-Element Quantum Chemistry — Oakland University</strong>: Develops reliable infrastructure (basis sets, force fields, density functionals) for predictive relativistic quantum-chemical modeling of complex chemical systems involving actinides, heavy main-group, and superheavy elements requiring hundreds of CPUs, large-memory nodes, and large, fast scratch space
            </td>
            <td>
                CPU, high streaming, large memory
            </td>
            <td>
                Gaussian, NWChem, TURBOMOLE, Dirac, Columbus, EXP-T, in-house codes
            </td>
            <td>
                80-400 cores
            </td>
            <td>
                Hours to weeks per job.
            </td>
            <td>
                192G / server but some tasks would benefit from 1TB servers
            </td>
        </tr>
        <tr>
            <td>
                <strong>Certificate Program in Data Science — Oakland Community College</strong>: Introduction of HPC, machine learning, data management, working with large datasets
            </td>
            <td>
                GPU/CPUstorage, memory
            </td>
            <td>
                Stata, R/Python, MATLAB
            </td>
            <td>
                One to four cores, but requires hundreds of jobs for each class
            </td>
            <td>
                Expect short runtimes for class projects
            </td>
            <td>
                128 GB / server
            </td>
        </tr>
    </tbody>
</table>
