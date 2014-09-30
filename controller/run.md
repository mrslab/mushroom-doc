控制器文件执行流程
===

执行流程

    1.执行mr_before_controller 绑定的hook类方法

    2.执行控制器init方法(若存在)

    3.执行经过路由获取的控制方法，若控制方法不存在则执行empty方法，若都不存在则抛出异常

    4.执行mr_after_controller 绑定的hook类方法
