# Learning-Linux

I use this repository to take notes about Linux and Tools

**Extract tar to a different Path**

```apache
tar -xzf cni-plugins-linux-amd64-v1.1.1.tgz -C /opt/cni/bin
```

**Load kernel Module**

```apache
modeprobe br_netfilter
```

**Check available Kernel Modules**

```apache
lsmod
```

**Load Kernel Parameters from directory runtime**

```apache
sysctl --system
```

**IP Tables**

IP Tables is a linux firewall program that allows to add rules for incoming and outgoing packets.[Click here to view more](IPTables.md)

**eBPF**
The eBPF allows to run programs in kernel space in runtime. 
