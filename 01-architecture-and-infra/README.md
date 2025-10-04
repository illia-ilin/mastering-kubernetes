# Module 01 — Kubernetes Architecture & Low-Level Infrastructure

This module explores the **internal architecture of Kubernetes** and its **core control plane components**.  

---

## 🎯 Learning Objectives

- Understand the internal structure of the **Kubernetes control plane**: `kube-apiserver`, `etcd`, `kubelet`, and the **Container Runtime Interface (CRI)**.
- Learn how the **API Server**, **admission chain**, and **webhooks** process and validate requests.
- Dive into **Linux primitives** that underpin container isolation and security: `cgroups`, `namespaces`, `seccomp`, and `AppArmor`.

---

## 🧩 Topics Covered

### Control Plane Internals
- **kube-apiserver** — request lifecycle, throttling, and audit logging  
- **etcd** — data model, snapshotting, and disaster recovery  
- **kubelet** — Pod lifecycle, probes, and eviction management  
- **containerd vs CRI-O** — runtime comparison and performance trade-offs  

### Linux Foundations
- **cgroups v2** — resource control and isolation  
- **PID namespaces** — process isolation  
- **Syscall filtering** — `seccomp` and `AppArmor` for workload hardening  

---

## 🧠 Practical Task

> Goal: Bring up a functional **Kubernetes control plane** manually (without automation scripts).

Tasks:
1. Review the reference repository [den-vasyliev/mastering-k8s](https://github.com/den-vasyliev/mastering-k8s).  
2. Deploy the control plane components manually in Codespaces or a local environment.  
3. Explore the component configurations and verify cluster health.  
4. Identify and fix issues in the deployment.

---

## 💡 Notes

- The setup is expected to work in **GitHub Codespaces**, with minimal adjustments.
