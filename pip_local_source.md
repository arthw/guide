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
pip install pygame -i https://pypi.tuna.tsinghua.edu.cn/simple  --default-timeout=100 
```

### Set local mirror in Windows

(1):在windows文件管理器中,输入 %APPDATA%

(2):会定位到一个新的目录下，在该目录下新建pip文件夹，然后到pip文件夹里面去新建个pip.ini文件

(3):在新建的pip.ini文件中输入以下内容，搞定文件路径："C:\Users\Administrator\AppData\Roaming\pip\pip.ini"


"C:\Users\Administrator\AppData\Roaming\pip\pip.ini"
or
"C:\Users\xxx\pip\pip.ini"

    [global]
    timeout = 6000
    index-url = http://pypi.douban.com/simple
    trusted-host = pypi.douban.com
    
