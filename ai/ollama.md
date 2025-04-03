# Ollama

## Set Server
```
sudo vi /etc/systemd/system/default.target.wants/ollama.service
```
```
Environment="OLLAMA_DEBUG=1"
Environment="https_proxy=http://xxx.com:yyy" 
```
## Restart Server
```
sudo systemctl daemon-reload
sudo systemctl restart ollama
```

## Run Client
```
ollama  run smollm:135m
```

## Monitor Log

```
tail -rf  /var/log/syslog
```
