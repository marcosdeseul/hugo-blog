+++
title = "What Do You Need for Your Own Homelab?"
date = 2020-05-01T18:55:05+08:00
draft = false
description = ""
slug = ""
tags = ["vmware", "homelab"]
categories = ["Homelab"]
externalLink = ""
series = ["Set Up Your Own VMware Homelab"]
+++

## What is Homelab?

I have used many public cloud services for a while. Since I started my career as a software engineer, AWS was already quite popular. Some old developer folks might not have chance to use public cloud services when landing on their first job, but I was lucky. So I used AWS in my first company. I have used AWS, GCP, Firebase for most of my careers.

But I always wanted to have my own home data center, which is a `homelab`. Why? Because instances on public cloud services are already virtualized. I can easily rent some computing resources from cloud vendors, but you have no idea of what is happening behind the scene.

I recently joined VMware. What is VMware? VMware is the biggest data center virtualization solution vendor. Before joining VMware, I didn't know what products VMware was selling precisely. But I knew the company had a promising vision of hybrid cloud. So I applied for a SE position in VMware and got an offer.

In VMware, it is a paradise to set up a home lab. Many engineers already have experience of building up server clusters and there are good internal resources. Moreover, these knowledges are relevant to my work to support customers. Then why not?

## How is a home server different from an enterprise one?

A server computer is technically a computer. It also has CPU, memory, storage, and etc. But a server computer has more stuffs compared to a home desktop or a laptop. Server computers usually have multiple CPU sockets and more slots for memory and storage. And power suply is also redundant to prevent power failure. It is also very common that server computers have interactions with each other, so also they usually have multiple ethernet ports.

But do you really need server computers for your own homelab? My answer is NO. If you really want to experience something like ones in a data center, then you should buy server computers for sure. But if you just want to try a similiar set-up at home and to understand the functionality, then you just can go with mini computers. Even with mini computers, you can try most of features of server computers, including setting up a cluster.

## What do you have to consider before buying mini computers for homelab?

First of all, why do you want to have your own homelab setup? Is it to deploy your applications? Or do you want to have a hands-on experience with VMware products such as vSphere, vSAN, NSX? Do you want to set up a cluster of computers like ones in data centers? Do you want to improve your Linux operation skills?

* If you just want to know how VMware products work or to experience a server computer setup, then buying a mini computer might be an overkill. There are great virtualization solutions for desktop such as VMware Workstation and Fusion or Oracle Virtualbox. Even though your laptop or desktop should have enough computing resource to have a big enough cluster setup, it should be good enough using this solutions in most of cases.
* If you want to deploy several applications on your own server like on AWS, then purchase one and try first. If you just assume that operating your own server will be similar like running an EC2 on AWS, you will get disappointed. Once you get familiar with local servers, then you can buy more machines and set up a cluster.

Secondly, CPU, memory, storage do not come with server computers. When you buy a laptop or a desktop, it usually comes with a full setup including OS installed. But when you buy a server, you usually have to buy memory, storage on top of your servers. If you haven’t check the price of memory and storage before purchasing a server computer, then the final cost can be a snowball. Moreover, if you want to virtualize your servers with VMware products, then you also should check the hardware compatibility. One of popular products from VMware, vSphere has a wide range of compatible hardware list but there are also many models without compatibility from local server vendors.

Lastly, noise and power consumption are also factors to consider. Normal server computers are very noisy due to fan and consuming a lot of energy to run heavy computing resources. Server computers are meant to run 24/7 without pausing or turning off, not like your laptop. If your server computers are not electricity efficient, then you will receive a surprising utility bill. In terms of noise, there are even fan-less computers these days. If you are planning to put server computers at home, you won’t want them to bother your sleep at night.

## What mini computers do I recommend for your own homelab?

I would like to recommend these two models below for those who want to set up their own lab for the first time. These two platforms are already very popular amongh the VMware community, so it is easy to get some help.

* Intel NUC - [link](https://www.intel.sg/content/www/xa/en/products/boards-kits/nuc/kits/nuc10i7fnhc.html)
* Supermicro - [link](https://www.supermicro.com/en/products/system/Mini-ITX/SYS-E300-9D-8CN8TP.cfm)

### Intel NUC

If you are planning to buy only one mini computer for homelab, then I highly recommend Intel NUC. It is compact and very quiet. Intel NUC 10 generation i7 model has a 6-core CPU, so more powerful. And Intel is one of the most well-know hardware vendor, so it is quite easy to find one Intel NUC box in most of countries.

### Supermicro

If you want to set up a cluster of more than 3 servers, then Supermicro will be a better option. It is because Supermicro has 2 x 1 Gbps ethernet ports and 2 x 10 Gbps ethernet ports. It is quite essential to have a good network connectivity in a cluster to test vMotion, vSAN, NSX, etc. But Intel NUC only has one 1 Gbps ethernet port, even though you can use a "usb-c to ethernet adapter", but it's quite limited natively. But Supermicro servers are noisier because it was designed as a mini server, so you may want to consider a seperate place or a server rack to put Supermicro machines in.
