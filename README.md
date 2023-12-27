# Alpine Linux Cloud Image Builder for Kubernetes

This repository is a specialized fork of the original [Alpine Linux Cloud Image Builder](https://gitlab.alpinelinux.org/alpine/cloud/alpine-cloud-images), designed to streamline the process of creating Alpine Linux cloud images that are optimized for Kubernetes deployments.

<!-- ## Pre-Built Kubernetes-Ready Images -->
<!---->
<!-- You can find pre-built Kubernetes-ready Alpine Linux images in the [GitHub releases section](https://github.com/michaelvanstraten/alpine-for-k8s/releases). -->

## Available Image Variants

This fork provides a diverse range of image variants, built on top of the [`existing offerings`](https://alpinelinux.org/cloud/), tailored for different Kubernetes environments, including:

**Kubernetes Versions**
- [x] Kubernetes 1.29
- [ ] Kubernetes 1.28
- [ ] Kubernetes 1.27

**Container Runtimes:**
- [x] containerd
- [ ] cri-o

**CNI Plugins:**
- [x] Cilium

**Kubernetes Node Variants**

Additionally, both Kubernetes master (kmaster) and worker (kworker) node images are available. Master images typically come with pre-installed tools for provisioning and managing clusters, such as `kubectl` and the `cilium-cli`.

### Building Images Locally

To build these images locally, follow these steps:

1. Install Packer.

   Get started by [installing Packer](https://developer.hashicorp.com/packer/tutorials/docker-get-started/get-started-install-cli#installing-packer).

2. Initialize the build configuration.

   ```shell
   packer init alpine.pkr.hcl
   ```

3. Build the images (this process may take some time).

   ```shell
   ./build local
   ```

For more detailed instructions, please refer to the [original repository's README](https://gitlab.alpinelinux.org/alpine/cloud/alpine-cloud-images#the-build-script).
