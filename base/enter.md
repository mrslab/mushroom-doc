入口文件
===

1.Mushroom采用单一入口的模式进行部署，入口文件引入框架文件;

2.入口文件名可以是任意PHP文件名，如 index.php

3.在入口文件中可定义全局常量

    <?php
        
    define("MR_APP_PATH", dirname(__FILE__) . '/application'); //应用目录(可选) 默认与入口文件所在目录相同

    define('MR_CONF_PATH',       MR_APP_PATH . '/config');     //配置文件所在目录(可选) 默认为 "应用目录/config"
    define('MR_RUNTIME_PATH',    MR_APP_PATH . '/runtime');    //运行临时目录(可选) 默认为 "应用目录/runtime"
    define('MR_CONTROLLER_PATH', MR_APP_PATH . '/controller'); //控制器目录(可选) 默认为 "应用目录/controller"
    define('MR_COMMAND_PATH',    MR_APP_PATH . '/command');    //Cli控制器目录(可选) 默认为 "应用目录/command"
    define('MR_MODEL_PATH',      MR_APP_PATH . '/model');      //模型目录(可选) 默认为 "应用目录/model"
    define('MR_VIEW_PATH',       MR_APP_PATH . '/view');       //视图目录(可选) 默认为 "应用目录/view"

    //define('MR_CONF_FILE',       MR_CONF_PATH. '/config.php'); //配置文件(可选) 默认为 "应用目录/config/config.php" 若不存在则使用默认配置信息

    define('MR_DEV_DEBUG', true); //是否开启Debug模式(可选) 默认为true

    require '{框架目录}/mushroom/Mushroom.php';

    ?>
