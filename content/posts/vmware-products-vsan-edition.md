+++
title = "vSAN Edition Comparison"
date = 2020-05-05T20:02:01+08:00
draft = true
description = ""
slug = ""
tags = ["vmware", "vsan"]
categories = ["VMware Product"]
externalLink = ""
series = ["VMware Product Edition"]
+++

## What is vSAN?

Have you heard of `HCI, Hyper Converged Infrastructure`? It's been a while since I joined VMware. I still feel that the term HCI is too fancy and not very intuitive. But it is not a fault of VMware because VMware is not the one who invented the term.

`Hyper Converged Infrastructure` usually means server computers with internal shared storages. What? When we use a laptop or a desktop, it usually comes with storage inside, isn't it?

But it is not necessarily like this in the server computer world. At the beginning of server computer era, it was like that. But imagine that hundreds or thousands of server computers. Each computer has its own storage but the usage of storage can vary depending on the service running on the server.

So what did IT administrators do to solve this issue? They moved internal storages into an external storage rack. Then they put a storage switch to connect the external storage rack and servers like storages are sitting in each server. But this approach also faced issues soon. The external storage racks grew very fast while external storages were more expensive than internal ones. And to maintain external storages, IT teams needed more manpower to configure storage racks and storage network devices.

vSAN, VMware HCI solution, was invented to put external storages back into servers, but still to keep them connected. vCenter manages vSAN clusters. It connects servers with internal storages so that end users can use them like there is only one shared storage.

## What editions does vSAN 7.0 include?

### what is All-Flash configuration?

Going through the edition comparision table and annotations below, you will see a term "All-Flash" for a couple of times. For your better understanding of vSAN editions, let me explain first what is it.

There are two types of storage, Solid State Drive(SSD) and Hard Disk Drive(HDD). SSD is much faster than HDD, but also much more expensive. All-Flash means all-SSD-storage setup.

vSAN has two tiers of storage, one is the capacity tier and the other is the cache tier. The cache tier stores read data temporarily to improve IOPS performance. Hybrid configuration means setting up HDD for the cache tier and SSD for the capacity tier. All-Flash means SSD for the cache and capacity tier.

### vSAN Standard vs Advanced vs Enterprise vs Enterprise Plus

*The summary of vSAN editions is based on [this VMware offical documentation](https://www.vmware.com/content/dam/digitalmarketing/vmware/en/pdf/products/vsan/vmware-vsan-licensing-guide.pdf). If you need more info, please click the link and find more.*

| vSAN Features | Standard | Advanced | Enterprise | Enterprise Plus |
| ---: | :---: | :---: | :---: | :---: |
| Storage Policy Based Mgmt | O | O | O | O |
| Virtual Distributed Switch | O | O | O | O |
| Rack Awareness | O | O | O | O |
| All-Flash Hardware | O | O | O | O |
| iSCS Target Service | O | O | O | O |
| Qos - IOPS Limit | O | O | O | O |
| Deduplication & Compression* | | O | O | O |
| RAID-5/6 Erasure Coding* | | O | O | O |
| vRealize Operations within vCenter | | O | O | O |
| Data-at-Rest Encryption | | | O | O |
| Stretched Cluster with Local Failure Protection | | | O | O |
| File Services | | | O | O |
| vROps 8 Advanced Features* | | | | O |

* Deduplication & Compression / RAID-5/6 Erasure Coding
  * require an all-flash vSAN configuration
* vROps 8 Advanced Features
  * vSAN-aware WLB
  * Customizable Dashboards
  * Auto Remediation
  * Troubleshooting Workflows
  * Automated Intent-Based Workload
  * Capacity Planning

---
Let me explain some key features here:

* **Storage Policy Based Mgmt**: You can set up a policy of storage. When launching a new VM, you can choose one policy so that all VMs under the policy follow the same storage setup.
* **Rack Awareness**: vSAN protects data by duplicating data and distributing duplicated data into different hosts. What if the power of server rack is down? If all duplicated data sits in servers of one rack, then you lose all data. So it is important vSAN awares of rack setup.
* **Stretched Cluster**: vSAN is used to connect servers with internal storages. Then can we connect servers in different two data centers? Yes, you can fulfill this requirement by vSAN Stretched Cluster.

In summary, `vSAN Advanced` has more effiency-related features like deduplication & compression, RAID-5/6 erasure coding. If you are planning to connect two data centers with storages connected, then you may want to consider `vSAN Enterprise`. `vSAN Enterprise Plus` has the same list of vSAN Enterprise features, but it comes with vROps 8 Advanced features. But you only can purchse this bundle per CPU.

## Pricing?

You may want to ask me how much these editions are. But the final price can be different depending on the volume of purchase and some factor. Please talk to your VMware sales or partner.
