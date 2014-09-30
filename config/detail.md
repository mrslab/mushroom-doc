配置说明
===

以下将对config.php中配置信息进行详细说明

1.基本设置(base)中共包含六项基本设置

    'base'  => array(

        //charset 设置页面输出的字符编码
        'charset'    => 'utf-8',

        //timezone 设置系统时区
        'timezone'   => 8,

        //controller 设置默认控制器名称
        'controller' => 'index',

        //method 设置默认控制方法名称
        'method'     => 'index',

        //gzip 设置是否开启gzip压缩 
        'gzip'      => true,
        
        //mode 设置Url解析模式
        //支持一下几种模式 
        //  1.MR_MODE_QUERY-基于查询字符串 如: index.php?m=index&a=index
        //  2.MR_MODE_REGEXP-基于段 如:index.php/index/index
        //  3.MR_MODE_SEGMENT-基于正则匹配 如 /index/ => IndexController::indexMethod()
        'mode'       => MR_MODE_QUERY, //MR_MODE_REGEXP || MR_MODE_SEGMENT
    )

2.Cookie设置

    'cookie' => array(
        'path'     => '/',
        'domain'   => null,
        'secure'   => null,
        'httponly' => false,
    )

3.Session设置

    'session' => array(
        'driver'       => 'File',
    )

4.comp组件配置信息

    'comp' => array(
    )

5.hook配置信息

    'hook' => array(
    )

6.param用户自定义配置信息

    'param' => array(
    )

7.route配置信息，当 base中mode为MR_MODE_REGEXP时，须配置此选项
    
    'route' => array(
    )

8.模板配置

    'template' => array(
        'driver' => 'mrtpl' // or smarty
    )

#####具体使用方法将在后续文档中详细描述
