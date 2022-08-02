# localplane

This script will start a `k3d` cluster and `localstack` instance, and will setup Crossplane with the two.

```
-> % localplane start
[INFO] Creating kubernetes cluster 'mycluster'...
[INFO] Starting localstack...
[INFO] localstack_main container network IP: 172.19.0.4
[INFO] Preparing Crossplane Helm repositories
[INFO] Installing Crossplane. This could take a while...
[INFO] Crossplane installed!
[INFO] Provisioning AWS provider. Also this could take a while...
[INFO] AWS provider not ready yet..................
[INFO] Setting up provider configuration
[INFO] Done!
```

## Installation

Just download the script and make it executable.

## Usage

It has a `start` and `stop` command. You can provide the cluster name as an additional argument, otherwise the `mycluster` default will be used.

```
-> % localplane start
[INFO] Creating kubernetes cluster 'mycluster'...

-> % localplane start anothercluster
[INFO] Creating kubernetes cluster 'anothercluster'...
```

```
-> % localplane stop                
[INFO] Stopping localstack
[INFO] Deleting cluster 'mycluster'
[INFO] Done!
```