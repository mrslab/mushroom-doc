定义控制器
===

控制器是存放在 MR_CONTROLLER_PATH目录中的一个PHP类文件，控制器方法是控制器类中的一个以Method结尾的类方法。

以下是一个控制器类的定义：

    MR_CONTROLLER_PATH/IndexController.php

    <?php

        namespace controller;

        class IndexController extends \mr\Controller {

            public function helloMethod() {
                echo "Hello Mushroom!";               
            }
        }

    ?>

定义控制器时以下几点需要注意：

    控制器类的命名空间均为 "controller" 

    控制器类名以"Controller"结尾，必须继承"\mr\Controller"基类

    方法须以"Method"结尾，非"Method"结尾的方法无法成为入口方法被执行

控制器独有的API：

    $this->assign($key, $value);

    $this->display($tpl, $output = false);

控制器Url访问方式：

    http://yourdomain/app/index.php?m=index&a=hello
    或者
    http://yourdomain/app/index.php/index/hello
    或者
    http://yourdomain/hello/ (/^\/hello\/$/ => index::hello)

可定义多层控制器

    MR_CONTROLLER_PATH/hello/IndexController.php

    <?php

        namespace hello\controller;

        class IndexController extends \mr\Controller {

            public function helloMethod() {
                echo "Hello Mushroom!";               
            }
        }

    ?>

    访问方法与单层控制器相类似：
    http://yourdomain/app/index.php?m=hello/index&a=hello
