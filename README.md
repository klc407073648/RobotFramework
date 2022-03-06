# RobotFramework
# 学习网站

1. 用户指导手册——[Robot Framework User Guide](http://robotframework.org/robotframework/latest/RobotFrameworkUserGuide.html)

2. 官网——[robotframework官网](https://robotframework.org/)

3. 自动化测试框架——[robotframework/RIDE](https://github.com/robotframework/RIDE)

4. web测试库 ——[SeleniumLibrary](http://robotframework.org/SeleniumLibrary/SeleniumLibrary.html)



https://github.com/MarketSquare/robotframework-requests



2.2.2   Using arguments

2.2.7  Test templates

pip install robotframework-sshlibrary

https://github.com/up1/course-robotframework

中文乱码解决：

找到Python路径下的testrunnerplugin.py文件，如我的文件路径：C:\Python\Python37\Lib\site-packages\robotide\contrib\testrunner\testrunnerplugin.py

将第565行的encoding['SYSTEM']改为encoding['OUTPUT']，如下图

```python
textctrl.SetReadOnly(False)
        try:
            if enc:
                textctrl.AppendText(string.encode(encoding['SYSTEM']))
            else:
                textctrl.AppendText(string)
            # print("DEBUG _AppendText Printed OK")
        except UnicodeDecodeError as e:
            # I'm not sure why I sometimes get this, and I don't know what I
            # can do other than to ignore it.
            if PY2:
                if is_unicode(string):
                    textctrl.AppendTextRaw(bytes(string.encode('utf-8')))
                else:
                    textctrl.AppendTextRaw(string)
            else:
                textctrl.AppendTextRaw(bytes(string, encoding['SYSTEM'])) #encoding['SYSTEM']改为encoding['OUTPUT']
```

