# Evaluate Minikube

### Pros
1. Easy to setup (if not using Fedora 29 with Secure Boot enabled)
    - VirtualBox will not work with Secure Boot enabled <-- **production concern**
2. Large userbase and is well maintained
3. Supportes Windows, Linux and MacOS

### Cons
1. Nat and host only networking and it does not support bridged networking.
    - However, port forwarding is possible. 
2. Requires access to public internet to download dependencies
3. Conflicts with out Mac Watcher dev environment
4. Officially not production ready

### Upgradeability
- Persistant volumes are mapped to directories inside the Minikube VM. <-- TODO: Test if data persists after restarting and upgrading Minikube
