+++
draft = false
date = 2020-06-05T19:28:45+08:00
title = "How to Prepare CKA and CKAD"
description = ""
slug = ""
tags = ["devops", "cka", "ckad", "certificate", "exam", "k8s", "kubernetes"]
categories = ["DevOps"]
externalLink = ""
series = []
+++

## What is Kubernetes?

When I first learned programming, it was not very difficult to build an application. There were a lot of useful resources to use for application development. (Developers like sharing.) If you have chosen right courses, then it took a couple of weeks to build what you wanted. But a real problem was deployment. You can learn programming on your laptop, but it was not easy learn application deployment and maintanance on your machine. Back then, `AWS` was already running their business, so I could start an EC2 instance (a Virtual Machiine) and run applications. But what if issues happen? Then if you do not have enough knowledge of Linux, it becomes a very difficult issue to solve. To solve this issue, I used many solutions like AWS Elastic Beanstalk, GCP Firebase, etc. They were very convinient, but they were not flexible enough.

Later, I learned `Docker`. Container was a truly new and fascinating technology which got rid of inefficient processes which I was suffering a lot from. After dockerizing your applications, then they always work same anywhere a docker engine is installed. But even, it was not enough to solve all issues. I had to handle all auto-scaling, load balancing issues even with Docker. `Serverless` technology was invented to remove developers' stress to handle applications, but the functionalities of serverless technologies were quite limited compared to the previous way of deployment and You had to modify existing applications. `Microservices` architecture became popular, so managing containers were getting complex. Kubernetes was invented to solve these issues in Google and Google opensourced the project later.

`Kubernetes`, also called `k8s`, is a portable, extensible, open-source platform for managing containerized workloads and services, that facilitates both declarative configuration and automation. (from [kubernetes.io](https://kubernetes.io/docs/concepts/overview/what-is-kubernetes/)) It solved most of my previous concerns. It supported native load-balancing, auto-scaling, liveness check, etc. I didn't have to worry about the availability of my applications anymore.

In my previous company, I used k8s on a daily basis. We didn't have a big DevOps team or a system engineering team. Most of engineers were software engineeres and we had to find our own solutions to maximize our experience, which was k8s. All of us were senior engineers with a least 5+ years and some of us were with 10-15+ years of experience. We truly wanted to use our existing skill set, not compromising the scability and the availability of products.

## What are CKA / CKAD?

The `Certified Kubernetes Administrator (CKA)` and `Certified Kubernetes Application Developer (CKAD)` were created by the `Cloud Native Computing Foundation (CNCF)`, in collaboration with The Linux Foundation, to help develop the Kubernetes ecosystem. (from [Cloud Native Computing Foundation](https://www.cncf.io/certification/cka/))

In other words, it is the most popular k8s certifiaction exam for now. And the exams are all hands-on and command-line environment, not like old-fashioned multiple-choice question(MCQ) exames, which means You will become quite knowledgeable enough to manage your own k8s cluster once you pass CKA and/or CKAD.

## Do I need CKA and/or CKAD?

If you are planning to manage k8s cluster or if you are a software engineer who is already heavily using k8s, then the time to prepare for CKA and/or CKA will be a good inventment. It is a hands-on environment, so there is no dump. It makes you keep practicing, so that you are becoming truly capable of k8s.

But if you just want to know what k8s is, then taking CKA and/or CKAD can be an overkill. To pass the exam, you should understand the basic concepts of k8s, but CKA and CKAD are more focused on hands-on experience. You may have to spend more time on practice, not on technical concepts.

### The difference between CKA and CKAD

So which one do you have to take between CKA and CKAD, or both? `CKA` is an exam for system administrators like system engineers who want to set up k8s clusters on Linux. So it includes how to install k8s clusters by using `kubeadm` tool, how to troubleshoot when one of your server node is down, security concepts like TLS certificate, etc. `CKAD` has more parts for developers who work on k8s. It includes Stafeful Pods, Multi Container Pods like Sidecar, which are more important when you are building applications.

But to be very honest with you, two of them have a lot of overlap. Let's assume that CKA and CKAD have 10 common parts, for example. Then CKA has 25~30% more to study including cluster setup, and CKAD has 10% more including multi-container pod. That is also why **CKA is 3-hour long** and **CKAD is 2-hour long**. CKA can be slightly more difficult if you don't have security, networking and Linux administration background. So if you are targeting both, then I highly recommend you to take CKA first and CKAD later.

## How to prepare CKA and/or CKAD?

The best courses for CKA and/or CKAD are Mumshad Mannambeth's courses from Udemy. He has two courses for [CKA](https://www.udemy.com/course/certified-kubernetes-application-developer/learn/lecture/16488118?start=1#overview) and [CKAD](https://www.udemy.com/course/certified-kubernetes-application-developer/learn/lecture/16488118?start=1#overview). The CKA course has 15-hour-long videos and CKAD one has 7-hour-long videos. They also have free hands-on-labs which aren't counted. So if you are planning to take CKA, I highly recommend you to have 40 hours for videos and practices. If you want to take CKAD after CKA, then it will be good enough to have 10 more hours at most for non-overlapping videos and practices. Otherwise, it may take you to prepare CKAD for around 20 hours.

In comparison, I also took Linux Academy's CKA prep course. The one had good terminal environment like a real CKA exam, but the depth of contents was not deep enough and practices were much less. Mumshad's hands-on-lab terminal environment, to be honest, was not very nice. It was quite slow, sometimes hanging, even exited serveral times unexpectedly, but still acceptable. Most of all, the quaility of hands-on-lab contents of Mumshad's was really good, which really matters. So just go with Mumshad's one not to waste your time.

If you are very new to k8s, it is highly recommended to finish hands-on-labs in each section at least twice, and mock exams three times.

## What will happen on the day you take one of the exams?

Before taking CKA, what I really wanted to know was how the exam interface was. Some were answered by googling, but others were not. My questions with answers were like below:

* What materials can I use?
  * https://kubernetes.io/docs and its subdomains
  * https://github.com/kubernetes/ and its subdomains
  * https://kubernetes.io/blog/
* Can I use my own terminal?
  * No, You can't. It is a full **hands-on-lab environment** where a terminal and exam questions are provided. Since you are allowed to use only one terminal tab, there are guides to recommend to use tmux to have multiple terminal sessions. But I am a tmux user, but I couldn't find any reason why I had to use tmux for CKA/CKAD.
* How can exam proctors validate my ID card?
  * You just show your ID via the webcam of your computer. But I really suffered from connecting my webcam with Chrome since webcam was not allowed on Chrome back then. It took me 30 minutes to connect webcam, so I highly recommend you to join your exam 15 minutes earlier.
* Can I request a break during exam?
  * There is a pause button. You click the pause button, then your proctor hide your screen. Once you come back, then you click a resume button, your proctor show your screen again. But they count against your time.
