# 系统配置
tp5.0	php7.3.4		Apache2.4.39	Mysql5.7.26

tp5.0改动

App->
 Config.php
// 应用调试模式
'app_debug'              => false,
// 是否开启路由
    'url_route_on'           => true,
// 默认输出类型
    'default_return_type'    => 'json',
// 显示错误信息
    'show_error_msg'         => false,
// 异常处理handle类 留空使用 \think\exception\Handle
'exception_handle'       => '\app\lib\exception\ExceptionHandler',

Route.php
建立group路由分组	用于拒绝没登录直接进入界面

Contorller->
控制器 只负责调用返回数据	不处理逻辑

Service->
负责处理各种事务逻辑 成功调用model处理数据	失败调用exception返回错误信息

Model->
调用db数据库	处理数据 

Validate->
验证器 基本的校验方法	自己定义的isPositiveInteger规则

Lib->
Exception	自定义异常的基类	重写Handle	记录日志

Vendor->	引入文件
PHPExcel.php	引入phpexcel处理xls xlsx文件
