# win10安装ubuntu18.04双系统黑屏怎么解救？
进去了ubuntu的启动界面，结果一闪就成了黑屏。

题主是有用独立显卡吗？
尝试让光标停留在“Try”项目按e，在代码中找到quiet slash ，在这之后添加acpi_osi=linux nomodeset，保存文本进入即可（Ctrl+X）。 
