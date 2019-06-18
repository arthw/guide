### Set local source of PIP/PIP3
`mkdir ~/.pip`

CMD

`vi ~/.pip/pip.conf`

Then copy and paste below texts

```
[global]
trusted-host=mirrors.douban.com
index-url=https://pypi.douban.com/simple/
```

### Set Local Mirror

```
pip install pygame -i https://pypi.tuna.tsinghua.edu.cn/simple 
```
