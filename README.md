# frigate-lxc-with-gpu-passthrough
Frigate docker container running in an LXC with GPU passthrough, to share with Ollama

1. Create Debian LXC
2. Set bash as default shell
3. Install frigate as per https://www.mostlychris.com/installing-frigate-nvr-on-proxmox-in-an-lxc-container/
4. Configure GPU passthrough as per https://digitalspaceport.com/how-to-setup-an-ai-server-homelab-beginners-guides-ollama-and-openwebui-on-proxmox-lxc/
5. Install NVIDIA Container Toolkit
6. Set "no-cgroups = true" in /etc/nvidia-container-runtime/config.toml

<img width="1916" height="905" alt="image" src="https://github.com/user-attachments/assets/1bc20c0a-9086-4084-9757-ec08a00c7e62" />

