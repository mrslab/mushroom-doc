配置格式
===

config.php 为项目配置信息入口文件，框架会读取此文件作为项目的配置信息，在开发中我们可以将此文件分解成若干小文件，这样方便对配置信息进行管理

格式：

    return array(

        'base'  => array(
        ),

        'cookie' => array(
        ),

        'session' => array(
        ),

        'comp' => array(
        ),

        'hook' => array(
        ),

        'param' => array(
        ),

        'route' => array(
        ),

        'template' => array(
        )

    );

分拆成若干配置文件后：
    
    define('_THIS_', dirname(__FILE__));

    return array(
        'base'       => include _THIS_.'/base.php',
        'cookie'     => include _THIS_.'/cookie.php',
        'session'    => include _THIS_.'/session.php',
        'comp'       => include _THIS_.'/component.php',
        'hook'       => include _THIS_.'/hook.php',
        'param'      => include _THIS_.'/param.php',
        'route'      => include _THIS_.'/route.php',
        'template'   => include _THIS_.'/template.php',
    );


