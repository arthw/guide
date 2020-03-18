## Set ptrace_scope without reboot
```
echo 0|sudo tee /proc/sys/kernel/yama/ptrace_scope
```
