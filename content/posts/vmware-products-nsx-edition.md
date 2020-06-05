+++
title = "NSX Data Center Edition Comparison"
date = 2020-05-18T20:17:44+08:00
draft = false
description = ""
slug = ""
tags = ["vmware", "nsx", "nsx-v", "nsx-t", "nsx-dc"]
categories = ["VMware Product"]
externalLink = ""
series = ["VMware Product Edition"]
+++

## What is NSX Data Center?

You always use Network to access to the Internet. If you didn't go to a place without Internet connection like an island, you are technically living with Networks; Wifi, mobile cellular data, routers to provide wifi at home, etc.

But I had not thought of Network as a computing resource before joining VMware. Even my previous company was one of wireless network hardware vendor, Ruckus Network, but my exposure to Networking was limited. But after joining VMware, I can truely understand why Networking is very important and how they work.

Networking is important for individuals' life but more important for data centers and cloud services. So networking experts are in high demands in the cloud industry. It is because server computers are connected, so that applications running on different servers can interact with each other.

But fulfilling all networking requirements is never easy. You have to understand how to set up physical networking devices and how networking features work such as **routing, switching, firewall, VPN, load balancing, etc**. And you also need to understand all Networking concepts and commands on the OS level and how to manage them in multiple networking layers. The complexity is not comparable to fixing your home wifi router.

That's why `NSX` was invented. Setting up networking across servers is extremely complex, so NSX, network virtualization solution, helps engineers to configure their data centers' network in a proper and efficent way.

## NSX-V? NSX-T? NSX Data Center?

If you have heard of NSX, then you may have heard of `NSX-V` and `NSX-T`. And we have `NSX Data Center` here. `NSX-V` is **NSX for vSphere**, so the architecture of NSX-V is only focused on vSphere. But `NSX-T` covers a wider range of OS. It covers not only vSphere, but KVM and bare-metal. `NSX Data Center (NSX-DC)` include both of NSX-V and NSX-T. `VMware Cloud Foundation (VCF)` allows customers to deploy both NSX-V and NSX-T. I think this is why the new name `NSX-DC` was made.

## What editions does NSX Data Center include?

### NSX Data Center Standard vs Professional vs Advanced vs Enterprise Plus

*The summary of NSX-T Data Center editions is based on [this VMware offical documentation](https://www.vmware.com/content/dam/digitalmarketing/vmware/en/pdf/products/nsx/vmware-nsx-datasheet.pdf). If you need more info, please click the link and find more.*

| NSX Features | Standard | Professional | Advanced | Enterprise Plus |
| ---: | :---: | :---: | :---: | :---: |
| Distributed Switching and Routing | O | O | O | O |
| NSX Gateway Firewall (Stateful) | O | O | O | O |
| NSX Gateway NAT | O | O | O | O |
| Software L2 Bridging to Physical Environments | O | O | O | O |
| Distributed Firewalling for VMs and Workloads Running on Bare Metal | | O | O | O |
| VPN (L2 and L3) | | O | O | O |
| Integration with NSX Cloud* for AWS and Azure Support | | O | O | O |
| Load Balancing | | | O | O |
| Container Networking and Security | | | O | O |
| Multi-vCenter® Networking and Security | | | O | O |
| IPv6 with Dynamic Routing, Dynamic IPv6 Allocation and Services | | | O | O |
| Context-Aware Micro-Segmentation (L7 Application Identification, RDSH, Protocol Analyzer) | | | O | O |
| NSX Distributed IDS/IPS1 | | | O | O |
| Federation | | | | O |
| VM-to-VM Traffic Flow Analysis | | | | O |
| Firewall Visibility | | | | O |
| Automated Security Policy | | | | O |
| vRealize Network Insight Advanced | | | | O |
| VMware HCX Advanced | | | | O |

*For detailed feature capabilities, please refer to the knowledge base articles on NSX Data Center features including the [Product Offerings for NSX-T Data Center 3.0](https://kb.vmware.com/s/article/78223).*

---
Let me explain some key features here:

* **Load Balancing**: Distribute network traffic into multiple VMs so that applications only receives bearable amount of traffic.
* **Federation**: Centralized policy configuration and enforcement across multiple locations from a single pane of glass.

In summary, `NSX Standard` includes basic networking features; switching, routing, gateway firewall, gateway NAT. `NSX Professional` includes micro-segmentation and VPN on top of NSX Standard. `NSX Advanced` has more features for bigger and/or multiple sites; load balancing, multi-vCenter networking and security, context-aware micro-segmentation. It also supports container networking and security. `NSX Enterprise Plus`, the big boss, supports Federation and has VM-to-VM traffic analysis. It also comes with vRealize Network Insight Advanced and VMware HCX Advanced.

## Pricing?

You may want to ask me how much these editions are. But the final price can be different depending on the volume of purchase and some factor. Please talk to your VMware sales or partner.
