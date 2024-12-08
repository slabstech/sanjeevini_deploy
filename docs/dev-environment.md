Developer Environment Setup

- For New Installation
  - If windows is installed by default, create a dual boot with ubuntu  
    - Take a 8/16GB usb/pen-drive, create a ubuntu bootable disk with rufus

  - Create empty parition in windows,
    - Go to disks / parition
    - Shrink volume of largest drive. Keep atleast 80%GB for Ubuntu for ML/Gen AI 
    - You should see an empty partition

  - Disable BitLocker Encryption till Ubuntu is installed 

  - Restart laptop with bootable usb-drive plugged-in 
  - Go to boot menu, (Check Key to press for your laptop and manufacture)
  - Install Ubuntu 

- Disable SecureBoot

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
    - Complet MOK setup steps
    - Verify Secure boot is disabled,

    - Verfiy installation is complete , run nvidia-smi
    - Add cuda to path - check the cuda version installed,   
      - nano ~/.bashrc
      - export CUDA_HOME=/usr/local/cuda-12.6
      - export PATH=$PATH:$CUDA_HOME/bin

  - NVIDIA container toolkit
    - [Install](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html#installing-with-apt)
  - docker engine
    - [Install](https://docs.docker.com/engine/install/ubuntu/) & [Post-install](https://docs.docker.com/engine/install/linux-postinstall/#manage-docker-as-a-non-root-user) 
  - container + docker
    - [Configuration](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html#configuring-docker)

    - for NVML error,  change no-cgroups setting [link](https://bobcares.com/blog/docker-failed-to-initialize-nvml-unknown-error/)
        - sudo nano /etc/nvidia-container-runtime/config.toml
        - set the parameter   
          - no-cgroups = false
  - Mistral Inference API
    - [api setup](https://mistral.ai)
  
- Project Setup
  - To setup project follow [deployment](../docs/deployment.md)
  - UX / Frontend
    - https://github.com/slabstech/sanjeevini_frontend
      - Follow install setup []
  - Server / Backend
    - https://github.com/slabstech/sanjeevini_backend
  - Deployment
    - https://github.com/slabstech/sanjeevini_deploy