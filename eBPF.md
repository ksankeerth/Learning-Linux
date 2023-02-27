# eBPF - extended Berkly Packet Filter

The `ebpf` was introduced in Linux 3.18 with limited capablities. The Linux Kernel version 4.4 introduced more features to `ebpf`.

In usual, We run programs in `userspace`. For example, when a program want to open an `TCP` connection, the request/call will be made to `kernel` via the `syscalls`. The userspace programs can interact with resources(`devices and data`) only by using supported `syscalls`. So in some cases, it's not possible to go beyond the `userspace` and do something closely with `devices, resources and data in raw format`. 

The `eBPF` new technology solves the mentioned problem in safe way. Before `eBPF`, We can use `Linux Kernel Modules` known as `LKMS` to load in runtime and add new functionalties to the `kernel` without compiling the source code of  `kernel`. For example, We can load modules using the command `modprobe`. The problem with `LKMS` is that they introduce problems to `OS` and may yield to crash the system if there were any bugs. So the safety is the problem. 

The `eBPF` solve the above mentioned security/safety concern as well. If I descripe the `eBPF` program, first We need to write `eBPF bytecode` and then We have to make a request to load it in the kernel. Before the kernel load into runtime, it'll do a few checks to ensure the safety. Once all the checkes are passed, the `eBPF bytecode` will be compiled using `JIT` compiler into native machine code and will placed in the runtime. If the program failed to pass checks, then they'll be rejected by the kernel.


## How an eBPF program works

In my undestanding, We can think `eBPF` programs as `interceptors`. For example, We can intercept all the `syscalls` made to the kernel using an `eBPF` program. There are many hook points available for `eBPF` program.

## How to start with eBPF program



## Instaling bpftool for Ubuntu 22.04

```apache
sudo apt install linux-tools-5.15.0-48-generic
```

To execute `bpftool`, you mostly need to provide root privileges. 

### Playing with `bpftool`

- Version
   
   ```apache 
        bpftool version
   ```
- Maps 

    ```apache
        sudo bpftool map show
        sudo bpftool map list

    ```

- Programs 
    ```apache
        sudo bpftool
    ```


References 

1. https://www.slideshare.net/suselab/ebpf-maps-101
2. https://www.sartura.hr/blog/simple-ebpf-core-application/
3. https://qmonnet.github.io/whirl-offload/2021/09/23/bpftool-features-thread/