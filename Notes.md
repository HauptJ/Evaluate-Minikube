# Evaluate Minikube

### Pros
1. Easy to setup (if not using Fedora 29 with Secure Boot enabled)
    - VirtualBox will not work with Secure Boot enabled <-- **production concern**
2. Large userbase and is well maintained
3. Supportes Windows, Linux and MacOS
4. Supports [Helm](https://helm.sh/)

### Cons
1. Nat and host only networking and it does not support bridged networking.
    - [However, port forwarding may be possible.](https://cwienczek.com/2017/09/reaching-minikube-from-other-devices/)
    - ![VM NAT](imgs/minikube_vm_nat.png "Minikube VM NAT")
    - ![VM HOST](imgs/minikube_vm_host.png "Minikube VM Host Net")
2. Requires access to public internet to download dependencies
3. Conflicts with out Mac Watcher dev environment
    - breakes kubectl
4. Not considered production ready by most
5. Can't port forward reserved ports 0 - 1024 even with sudo
    - Must use non reserved ports > 1024
    - ![Port 88](imgs/MinikubePort88.png "Minikube Port 88")

### Upgradeability
- Persistant volumes are mapped to directories inside the Minikube VM.
    - It appears that is possible to mount a directory on the host machine to the
        - However, this may be a problem.
        - ![Host Sharing Daemon](imgs/minikube_vm_host_dir.png "host to VM dir sharing")
        - However, it could be mitigated using `&`
        - **Command:** `minikube mount ~/temp/minikube/:/host`

### Overall
- It just feels like a dev tool instead of something you would use in production.
