# Module 02 — Resource Management & Declarative Workflows

This module focuses on **advanced resource management in Kubernetes**, deepening understanding of **YAML manifests**, **templating tools**, and **GitOps principles** used in production-grade clusters.

## 🎯 Learning Objectives

- Gain deeper insight into **YAML manifests** and resource lifecycles.

- Learn how **Helm** and **Kustomize** integrate into production pipelines.

- Apply **GitOps patterns** for version-controlled and auditable deployments.

## 🧩 Topics Covered

### Advanced YAML

- Anchors, aliases, and overlays for reusable manifest design.

### Helm

- Dynamic templating, hooks, and lifecycle event management.

### Kustomize

- Working with `patchesStrategicMerge` vs. `patchesJson6902`.

### GitOps

- Handling reconciliation drift, ensuring auditability, and implementing fallback logic.

### RBAC

- Designing granular access controls, managing impersonation, and preventing privilege escalation.

## 🧪 Lab Exercises

### Level 1 — Foundation

Based on experience from Module 01:

1. Generate 4 manifests for:
   - `etcd`
   - `kube-apiserver`
   - `kube-scheduler`
   - `kube-controller-manager`

2. Deploy the **control plane** using **kubelet static Pods**.
   
3. Create a **custom Deployment** (e.g., Nginx) with **3 replicas**.

**Question:** Why doesn’t it work initially? How can you fix it?

### Level 2 — Advanced

1. Deploy the **control plane**.

2. Create a **debug privileged container** using `verizondigital/kubectl-flame:v0.2.4-perf`.

3. Profile the **kube-apiserver**:
   ~~~bash
   perf record -F 99 -g -p <PID>
   ~~~

4. Build a **flame graph**:
   ~~~bash
   perf script -i /tmp/out | FlameGraph/stackcollapse-perf.pl | FlameGraph/flamegraph.pl > flame.svg
   ~~~

5. Copy `flame.svg` from the container and save it in your repo.

### Level 3 — Maximum

1. Deploy the **Cloud Controller Manager (CCM)** for your preferred cloud provider.

2. Configure `cloud-provider external` in your control plane configuration.

3. Set up `169.254.169.254/32` on localhost.

4. Create a **ServiceAccount** and configure `cloud.conf` and `sa.json`.

5. Deploy a **mock metadata server**.

6. Launch the **cloud-controller-manager**.

7. Register a node in the mock cloud environment.

8. Deploy any sample workload.

9. Create a **LoadBalancer** and obtain a real IP address.

> Notes:
> - Registering the node in the cluster is optional.
> - Remember to tear down cloud resources after finishing.

## 🔗 Useful References

- [amazon-ec2-metadata-mock](https://github.com/aws/amazon-ec2-metadata-mock)

- [gce_metadata_server](https://github.com/salrashid123/gce_metadata_server)
