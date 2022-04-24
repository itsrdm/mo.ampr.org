---
layout: default
title: Onboarding
nav_order: 2
---

# Customization
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

* Missouri Amateur Radio Operator Subitting Allocation Request
* Allocation Request is reviewed by me, the Coordinator
  * Block Size Reviewed against my [IP Addressing Methodology](guideline.MD)
* Approved or Denied
  * Approval Email Sent to Requestor
  * Rejection Email Sent, explination will be sent. The only time this happens is if I'm unable to validate information given or I need clarification.
* CIDR Blocks smaller than a `/24` are generally available to the requestor after I mark my approval.
* `/24` BGP routed blocks follow a different workflow.  
  * After my approval, the request is routed to the BGP Coordinator for additional processing.  Until the BGP Coordinator has granted approval and issued the LOR for your BGP setup, this process requires more processing time compared to non-BGP routed CIDR blocks.
  * The BGP Coordinator must issue the LOR before you will be able to move forward with your BGP routing setup.
  * BGP Routing is more complex than the IPIP tunnel.
* IPIP Tunnel allocations **will not work** until DNS Records have been added by me.
  * My Approval email will instruct you to reply with your DNS records. [Please read bullet #4 & #4a](guideline.MD)
* DNS Records are added.
  * I will email you confirmation of the record being added.
  * IPIP mesh gateways update in 24-hour batch cycles. Thus, your newly minted DNS entry will not grant real-time acceptance. So, roughly 24-48 hours after the newly minted DNS entries are accepted, your IPIP tunnel should be routable over the mesh.
