# Learning-Linux

I use this repository to take notes about Linux and Tools

**Extract tar to a different Path**

```apache
tar -xzf cni-plugins-linux-amd64-v1.1.1.tgz -C /opt/cni/bin
```

**Load kernel Module**

```
modeprobe br_netfilter
```

**Check available Kernel Modules**

```
lsmod
```

**Load Kernel Parameters from directory runtime**

```apache
sysctl --system
```
