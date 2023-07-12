## Record memory usage

watch -t -n 1 "xpumcli stats -d 0 | grep \"GPU Memory Used\" |  tee -a a.log"

watch -t -n 1 "xpu-smi stats -d 0 | grep \"GPU Memory Used\" |  tee -a a.log"

watch -t -n 1 "nvidia-smi | grep 15360MiB |  tee -a a.log"
