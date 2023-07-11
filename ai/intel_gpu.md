## Record memory usage

watch -t -n 1 "xpumcli stats -d 0 | grep \"GPU Memory Used\" |  tee -a a.log"
