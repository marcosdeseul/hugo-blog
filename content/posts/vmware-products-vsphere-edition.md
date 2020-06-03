+++
title = "vSphere Edition Comparison"
date = 2020-05-02T19:15:05+08:00
draft = false
description = ""
slug = ""
tags = ["vmware", "vsphere", "esxi"]
categories = ["VMware Product"]
externalLink = ""
series = ["VMware Product Edition"]
+++

## What is vSphere?

I believe that you already know what vSphere is if you visit this post. Since `VMware vSphere` is **the most popular server virtualization product**, so if you are in the IT infrastructure industry, you must have heard of vSphere once at leat. But just in case someone visits this blog to learn about VMware and its products, I would like to describe what vSphere is.

Before talking about what vSphere is, we need to know what a hypervisor is. A `hypervisor` is a software that helps to run virtual machines. What is a virtual machine? A `virtual machine` is a virtual computer in a physical computer like your laptop or desktop. Virtual machines are used to fully utilize computing resources such as CPU, memory.

A server is technically a computer. Corporates have many server computers at their data center. But when they use them, most of computing resources are usually not utilized. But servers are super expensive. People wanted to find better ways to maximize the utilization and the outcome was the advent of hypervisor.

vSphere is a package of products like Office 365, which includes ESXi the VMware Hypervisor. But when many people speak of vSphere, it usually refers to ESXi, so it can be quite confusing. Technically speaking, vSphere includes ESXi, vCenter, vSphere Client, etc.

## What editions does vSphere include?

### vSphere Standard vs vSphere Enterprise Plus

*The summary of vSphere editions is based on [this VMware offical documentation](https://www.vmware.com/content/dam/digitalmarketing/vmware/en/pdf/products/vsphere/vmware-vsphere-pricing-whitepaper.pdf). If you need more info, please click the link and find more.*

There are two main editions of vSphere: `vSphere Standard` and `vSphere Enterprise Plus`. Let me list up features before explaining what they are.

| Features | vSphere Standard | vSphere Enterprise |
| ---: | :---: | :---: |
| vMotion | O | O |
| vCenter Hybrid Linked Mode | O | O |
| High Availability (HA) | O | O |
| Fault Tolerance* (FT) | O | O |
| Per-VM Enhanced vMotion Compatibility | O | O |
| Content Library | O | O |
| vSphere Virtual Volumes | O | O |
| VM encryption | | O |
| vSphere Distributed Switch | | O |
| Host Profile and vSphere Auto Deploy | | O |
| vSphere Distributed Resource Scheduler (DRS) | | O |
| vSphere Storage DRS | | O |
| NVIDIA GRID vGPU | | O |
| Single root I/O virtualization (SR-IOV) | | O |
| vSphere Network I/O Control and vSphere Storage I/O Control | | O |

* Fault Tolerance
  * vSphere Standard allows 2-vCPU VMs FT
  * vSphere Enterprise allows 8-vCPU VMs FT

---
Let me briefly introduce main features here:

* **vMotion**: It is a technology to migrate VMs from one host to another host.
* **High Availability**: When there is a host failure, VMs are restarted on another host.
* **Fault Toelerance**: When there is a host failure, VMs on the hosts are switched to secondary VMs on live hosts without downtime.
* **Distributed Resource Scheduler**: When a host experiences shortage of computing resources, this feature migrate VMs to other hosts with enough resources.

After comparing two editions, you can say that `vSphere Standard` is more focusing on consolidating computing resources and `vSphere Enterprise Plus` is more for a bigger cluster management. vSphere Distributed Switch, Host Profile, vSphere Auto Deploy and DRS are all great features for cluster management.

### vSphere Essentials Kit

What if you have only a few nodes, but you still want to try vSphere with a minimum investment? Then you may want to consider `vSphere Essentials Kit`. It comes with a license supporting up to three hosts with up to two CPUs each and a vCenter server.

It is a minimal setup for small environments, so it does not include many features. But `vSphere Essentials Plus` (not `vSphere Essentials`) includes vMotion and HA.

### vSphere Desktop

Are you looking for a VDI solution to allow your employees to work remotely efficiently by? VMware has Horizon to address your need. But if you have to set up a data center from scratch for VDI, then from hardwares, softwares to guest OSs, it may cost a lot.

VMware provides `vSphere Desktop` License which is included in Horizon licenses. So if you are using your infrastructure only for VDI, then you do not need to buy extra vSphere licenses. By default, it has `vSphere Enterprise Plus`.

But if you still want to run some VMs with virtual desktops, then you may want to know Horizon add-ons licenses which help you to run virtual desktops on your existing vSphere environment.

## Pricing?

You may want to ask me how much these editions are. But the final price can be different depending on the volume of purchase and some factor. Please talk to your VMware sales or partner.
