---
layout: default
title : Security
group: navigation
order: 1
group: overview
subnavgroup: overview
---
{% include JB/setup %}

HORUS follows best practice recommendations from the NSF-funded Center for Trustworthy Scientific Cyberinfrastructure (CTSC), while building on tools already secured and implemented for the previous OSiRIS project.

For user authentication, authorization, and organization, HORUS uses the InCommon framework and tools such as CoManage and Grouper. Users are authorized using their institutional credentials. HORUS is involved in creating user accounts or storing passwords.

Monitoring tools (Elasticsearch central logging, CheckMK) and auditing tools available within our RHEL8 operating system help to identify security-related issues. HORUS also uses the ongoing institutional vulnerability scanning already in place for OSiRIS systems, extended to include the HORUS systems.

HORUS package management is configured to auto-update security-related packages as soon as updates become available.
