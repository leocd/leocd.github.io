---
title: "如何在国内安装Kubernetes"
date: 2019-07-08T11:36:23+08:00
tags: ["k8s","kubernetes","国内安装k8s"]
categories: ["学习笔记"]
---

## 前言  

&emsp;&emsp;Kubernetes是Google开源的一套容器集群管理系统，目前已经成为事实上的容器编排标准。  
&emsp;&emsp;但Kubernetes集群的组件众多，要在本地部署一套符合生产环境的集群并不是一件容易的事。  
&emsp;&emsp;还好除了手动部署方式之外，社区提供了诸如Kubeadm、Kubespray、kops、Rancher等多种自动化方式。rancher和kubeadm均使用docker部署组件，对于生产环境而言，这样的做法略欠妥当，而kops更偏向于在AWS或者GCE之类的公有云平台部署。所以最终我们选择了Kubespary。  
&emsp;&emsp;Kubespray是Google开源的一个部署生产级别的Kubernetes HA集群的开源项目，它整合了Ansible作为部署的工具。  
&emsp;&emsp;由于国内的特殊情况，直接使用kubespary提供的部署步骤是无法正确部署Kubernetes的，本文将提供在国内网络环境下，快速自动化部署K8s集群的方法。那么，开始吧！  
