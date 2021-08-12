# My own kernel. Use at your own risk.
- [**Zen Kernel**](https://github.com/zen-kernel/zen-kernel) — Result of a collaborative effort of kernel  hackers to provide the best Linux kernel possible for everyday systems.  Some more details can be found on https://liquorix.net (which provides kernel binaries based on Zen for Debian). [linux-zen](https://archlinux.org/packages/?name=linux-zen) default use CFS CPU scheduler.
- MuQSS —See the [LKML announcement](https://lkml.org/lkml/2016/10/29/4) posted by CK.

# Check if MuQSS is enabled

This start-up message should appear in the kernel ring buffer when MuQSS in enabled, use:

```
# dmesg | grep -i 'muqss cpu'
```

You can see: `MuQSS CPU scheduler v0.xxx by Con Kolivas.`

# MuQSS patched kernels and systemd

It is a common mistake to think that MuQSS does not support *cgroups*. It does but not all the cgroup features (e.g. CPU limiting will not work).

# You've been warned.
