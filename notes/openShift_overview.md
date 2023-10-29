# Managing Application with Kubernetes

# Table of Contents
1. [Introduction to Red Hat OpenShift](#openShift_overview)
2. [OpenShift Builds Overview](#builds)


<a id="openShift_overview"></a>
# Introduction to Red Hat OpenShift
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

## Overview

OpenShift is an **enterprise-grade Kubernetes container platform** designed for hybrid cloud strategies, providing automated operations and a consistent application platform. It extends Kubernetes functionalities with additional features and services, enhancing the application lifecycle, CI/CD, monitoring, and more.

### Key Features

- **Scalable:** Can scale applications across hundreds of nodes instantly.
- **Hybrid Infrastructure:** Simplifies deployment and management in various environments.
- **Open Standards:** Uses Kubernetes and OCI containers for familiarity and portability.
- **Developer Tools:** Offers a comprehensive set of tools, multilanguage support, and integrations.
- **Automated Operations:** Streamlines processes like builds, deployments, scaling, and health management.
- **Enhanced Security:** Provides advanced controls, threat detection, and risk profiling.
- **Persistent Storage:** Supports stateful and stateless apps through enterprise storage solutions.
- **Extensive Ecosystem:** Includes additional services and integrations through partners.

### OpenShift vs. Kubernetes

- **Nature:** OpenShift is a comprehensive product, while Kubernetes is an open-source project.
- **Installation:** OpenShift has more constrained installation options compared to Kubernetes.
- **Flexibility:** Kubernetes offers more flexibility in configuration and extensions.
- **Security:** OpenShift enforces stricter security policies out-of-the-box.
- **User Experience:** OpenShift offers a more user-friendly interface and in-built functionalities.
- **CI/CD Integration:** OpenShift integrates with Jenkins, providing streamlined CI/CD processes.
- **Networking:** OpenShift includes out-of-the-box networking solutions, whereas Kubernetes relies on third-party plugins.

### OpenShift Architecture

- Based on **microservices** architecture.
- Core components include **REST APIs** and **controllers**.
- Utilizes **Docker** for container images and **Kubernetes** for orchestration.
- Enhancements for source code management, image management, application management, and user tracking.

### OpenShift Command Line Interface (CLI)

- **`oc`** is the primary CLI tool, extended to support OpenShift's unique features.
- Compatible with **Windows, Linux, and Mac**.
- Allows for direct interaction with project source, scripting operations, and managing projects during limited web console access.
- Incorporates a version of **`kubectl`** for Kubernetes compatibility.

### Conclusion

OpenShift enhances Kubernetes by offering a robust, enterprise-ready platform with comprehensive features for the complete application lifecycle. It simplifies many operational aspects, providing a user-friendly, secure, and scalable environment for deploying containerized applications in various infrastructures.

<!-- /MarkdownTOC -->
</details>

---

<a id="builds"></a>
# OpenShift Builds Overview
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

## Builds

- **Definition**: A build is a process of transforming input sources (like source code) into a new, runnable object - usually a container image.
- **BuildConfig**: A crucial component that defines the build strategy and the source of the build.

## Build Strategies

- **Source-to-Image (S2I)**:
  - Combines source code with a base image to produce a new image.
  - Avoids the need for a Dockerfile.
- **Docker**:
  - Requires a Dockerfile and related artifacts.
  - Uses the `docker build` command internally.
- **Custom**:
  - User-defined build process where you create your own builder image.
  - Used for advanced use-cases beyond the standard build strategies.

## Build Inputs

- Sources for build content can include:
  - Inline Dockerfile definitions.
  - Content from existing images.
  - Git repositories.
  - Binary or Local inputs.
  - Input secrets.
  - External artifacts.

*Note*: Multiple inputs can merge in a single build, and precedence rules apply (e.g., an inline Dockerfile overrides an external one).

## ImageStreams

- Abstracts the referencing of container images within OpenShift.
- Does not store the image data itself but references to images in registries.
- Supports tagging (e.g., latest, dev, test) and automated updates/rollbacks.
- Simplifies deployment processes by referencing an image stream tag instead of specific image URLs.

## Automating Builds with Triggers

- **Webhook triggers**:
  - Automated way to invoke new builds upon events, like code updates in a Git repository.
- **Image change triggers**:
  - Monitors for updates in the base image and triggers a new build when changes are detected.
- **Configuration change triggers**:
  - Initiates builds when there are updates in the BuildConfig itself.

## BuildConfig Specification

- Defines details about the build, including source, strategy, output, and triggers.
- The strategy section specifies the build strategy (e.g., S2I, Docker, Custom).
- The output section defines where the resultant image will be pushed.

## Source-to-Image (S2I) Process

- Designed for simplicity and maintaining reproducibility.
- Integrates source code with a builder image without the need for Dockerfiles.

## Docker Build Strategy

- Involves the use of a Dockerfile to dictate how the build process should occur.
- Four implementation methods are outlined in the video.

## Custom Build Strategy

- Offers the most flexibility but requires a custom builder image with embedded build logic.
- Suitable for complex build scenarios not covered by S2I or Docker builds.

## Continuous Integration/Continuous Deployment (CI/CD)

- Emphasizes the need for automation in the build and deployment phases.
- Facilitates consistent and rapid application updates.

## Conclusion

- Builds are foundational to working with containerized applications in OpenShift.
- Different strategies (S2I, Docker, Custom) cater to various use-cases and complexity levels.
- ImageStreams offer a level of abstraction and convenience, working in tandem with builds for a streamlined application update process.
- Automation and CI/CD integration are vital for efficient and reliable application delivery.

<!-- /MarkdownTOC -->
</details>

---

<a id="binary"></a>
# 
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->



<!-- /MarkdownTOC -->
</details>

---
