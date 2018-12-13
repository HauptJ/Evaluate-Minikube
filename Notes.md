# Evaluate Minikube

### Pros
1. Easy to setup (if not using Fedora 29 with Secure Boot enabled)
    - VirtualBox will not work with Secure Boot enabled <-- **production concern**
2. Large userbase and is well maintained
3. Supportes Windows, Linux and MacOS

### Cons
1. Nat and host only networking and it does not support bridged networking.
    - [However, port forwarding may be possible.](https://cwienczek.com/2017/09/reaching-minikube-from-other-devices/)
2. Requires access to public internet to download dependencies
3. Conflicts with out Mac Watcher dev environment
    - breakes kubectl
4. Not considered production ready by most

### Upgradeability
- Persistant volumes are mapped to directories inside the Minikube VM. <-- TODO: Test if data persists after restarting and upgrading Minikube
    - It appears that is possible to mount a directory on the host machine to the 
        - However, this may be a problem.

