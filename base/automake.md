自动生成项目目录
===

Mushroom自带应用目录生成工具，能快速构建应用目录，使用方法如下

>注意：使用此功能时请先“删除或注释”入口文件中 MR_CONF_FILE 常量的赋值

1.windows系统中

    1)将php.exe所在目录加入PATH环境变量中

    2)在cmd中切换到项目入口文件所在目录

    3)执行命令 "php.exe index.php --develop automake"

2.Linux系统中

    1)cd {项目入口文件目录}

    2)执行命令 "php -f index.php --develop automake"


