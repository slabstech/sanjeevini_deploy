Developer Environment Setup

- After Ubuntu is installed, update all required libraries
    - sudo apt-get update
    - sudo apt-get upgrade
    - sudo apt upgrade
    - sudo apt install git

- Tools
  - VS Code
    - download from [link](https://code.visualstudio.com/docs/?dv=linux64_deb)
    - cd Downloads && sudo dpkg -i code_*.deb
  - CUDA toolkit for ubuntu
    - [Install](https://developer.nvidia.com/cuda-downloads)
  - NVIDIA container toolkit
    - [Install](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html#installing-with-apt)
  - docker engine
    - [Install](https://docs.docker.com/engine/install/ubuntu/) & [Post-install](https://docs.docker.com/engine/install/linux-postinstall/#manage-docker-as-a-non-root-user) 
  - container + docker
    - [Configuration](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html#configuring-docker)
  - Mistral Inference API
    - [api setup](https://auth.mistral.ai/ui/login?flow=82a0829e-2262-4a2f-a588-8a4c2b38573b)
  
- Project Setup
  - UX / Frontend
    - https://github.com/slabstech/sanjeevini_frontend
  - Server / Backend
    - https://github.com/slabstech/sanjeevini_backend
  - Deployment
    - https://github.com/slabstech/sanjeevini_deploy