# frigate-lxc-with-gpu-passthrough
Frigate docker container running in an LXC with GPU passthrough, to share with Ollama

1. Create Debian 13 LXC in Proxmox
2. Set bash as default shell
   ```
   sudo chsh -s /usr/bin/bash $(whoami) # or sudo chsh -s /bin/bash $(whoami)
   ```
4. Install frigate as per https://www.mostlychris.com/installing-frigate-nvr-on-proxmox-in-an-lxc-container/
5. Configure GPU passthrough as per https://digitalspaceport.com/how-to-setup-an-ai-server-homelab-beginners-guides-ollama-and-openwebui-on-proxmox-lxc/
6. Install NVIDIA Container Toolkit
7. Set "no-cgroups = true" in /etc/nvidia-container-runtime/config.toml
8. Build Docker Compose file as per attached
9. Set Frigate ~/config/config.yaml as per attached
10. Download YOLOv9 as per: https://docs.frigate.video/configuration/object_detectors/#downloading-yolo-models and store in /config/model_cache ensuring frigate config is updated with the right path to point to the model

<img width="1916" height="905" alt="image" src="https://github.com/user-attachments/assets/1bc20c0a-9086-4084-9757-ec08a00c7e62" />

