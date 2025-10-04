# Module 03 — Built-In Controllers

This module provides a deep understanding of **native Kubernetes controllers** — their reconciliation behavior, roles in maintaining desired state, and best practices for production usage.  
It’s part of my hands-on work from the [Fwdays *Kubernetes Mastering Course*](https://fwdays.com/en/event/kubernetes-mastering-course).

## 🎯 Learning Objectives

- Develop a solid grasp of how built-in controllers reconcile cluster state.

- Explore how different controllers manage workloads, rollouts, and system daemons.

- Gain experience building workload scenarios using multiple controller types.

## 🧩 Topics Covered

### ReplicaSet vs Deployment

- Replica count control, rollout strategies, and revision history management.

### DaemonSet

- Node-level workloads for logging, monitoring, and storage sidecars.

### StatefulSet

- Stable pod identities, headless services, and ordered scaling behavior.

### Job & CronJob

- Batch and scheduled jobs, `backoffLimit`, and `concurrencyPolicy`.

## 🧪 Lab Exercises

### Level 1 — Foundation
- Check Den's command history in the repository and practice various controller operations.

### Level 2 — Advanced
- Register a **node** with your control plane using a valid **kubeconfig**.

### Level 3 — Maximum
- Register a **node** with the control plane using a **Certificate Signing Request (CSR)** workflow.

---

## 🔗 Useful References

- [How the Kubernetes Resource Model Enables Configuration as Data](https://blog.upbound.io/how-the-kubernetes-resource-model-enables-configuration-as-data)  

- [Medium — Brendan Burns (Kubernetes co-founder)](https://medium.com/@bgrant0607)  

- [Controlling Process Resources with cgroups](https://labs.iximiuz.com/tutorials/controlling-process-resources-with-cgroups)  

- [Cluster API](https://cluster-api.sigs.k8s.io/)  

- [Kubernetes Resource Quotas Documentation](https://kubernetes.io/docs/concepts/policy/resource-quotas/)
