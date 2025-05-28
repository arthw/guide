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

## Windows building

install gcc by: https://github.com/skeeto/w64devkit/releases/download/v1.22.0/w64devkit-1.22.0.zip
add the **bin** in $PATH.

