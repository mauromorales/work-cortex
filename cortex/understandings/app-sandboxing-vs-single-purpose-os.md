---
created: 2026-01-18
updated: 2026-01-18
title: App Sandboxing vs Single-Purpose OS
tags: [security, linux, kubernetes, sandboxing, spos]
actions: []
---

## Current understanding

I currently think about strict confinement and single-purpose operating systems as solving problems at different layers, rather than being alternatives to each other.

Strict confinement belongs to the world of general-purpose systems. In those systems, installing new applications is a normal and expected action performed locally on the machine. Because of that, each application is treated as potentially hostile, and sandboxing mechanisms like Snap strict confinement or Flatpak exist to control what an app can access: filesystem paths, network, devices, and IPC. This model makes sense when the system is meant to continuously change and when many unrelated apps coexist.

An immutable system can still be general-purpose. Systems like Fedora Silverblue are immutable at the OS layer but are still designed to be changed easily by the user through application installation. The need for a reboot doesn't really change that — the intent of the system is still to allow users to add, remove, and experiment with software locally. In that context, strict confinement still has value because apps remain a primary source of risk.

A single-purpose operating system (SPOS) feels fundamentally different. In that model, installing new applications on the device itself should not be a supported action. The system exists to perform one mission, and any change to what runs on it is expected to come from a higher layer — an orchestrator or platform — rather than from inside the node. The responsibility for composition, deployment, and policy is intentionally moved upward.

In that setup, strict confinement is less relevant, not because it is weak, but because the assumption it is built on no longer applies. The system is not defending itself from arbitrary local applications; it is running a predefined stack.

Kubernetes fits into this model as the environment where application-level security is expressed. Workloads are the potentially risky entities, and the controls around them — privileges, mounts, seccomp, SELinux, and runtime isolation — are enforced there. This is similar to the browser model: the browser is trusted, and the tabs are not. The sandbox lives around the tabs, not around the browser itself.

From this perspective, strict confinement protects a general-purpose system from untrusted applications, while a single-purpose OS focuses on protecting the system from a hostile environment and from long-term drift. These approaches don't overlap much because they assume very different ways of operating the machine.

I don't see this as a gap in the single-purpose model. Its limitations are known, and over time we'll learn where it needs to evolve. But lacking application-level confinement doesn't feel like one of those gaps unless the system is expected to locally install software that bypasses Kubernetes' security mechanisms or allows arbitrary workloads to run without those layers.

## Historical record

### 2026-01-18 — Initial understanding

I was reasoning about how strict confinement, immutable systems, and single-purpose operating systems relate to each other, especially in environments where Kubernetes is responsible for running workloads and enforcing runtime isolation.

## Notes

- The distinction between immutable general-purpose systems and single-purpose systems feels more important than immutability alone.
- The browser analogy helps clarify where sandboxing naturally belongs.
- This framing may be useful when explaining why certain security mechanisms feel unnecessary rather than missing.
- I need to learn more about Kubernetes security to be sure that my statements are correct.
