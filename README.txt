
git clone https://github.com/Fanli2012/lqycms.git

cmd下创建.env文件
echo hello > .env


说明

1、基于Laravel 5.4
2、PHP+Mysql
3、后台登录：/fladmin/login
账号：admin888
密码：admin
4、恢复后台默认账号密码：/fladmin/recoverpwd


安装

1、 导入数据库
1) 打开根目录下的lqycms.sql文件，将 http://www.lqycms.com 改成自己的站点根网址，格式：http://+域名
2) 导入数据库

2、复制.env.example重命名成.env，修改相应配置APP_DOMAIN、APP_SUBDOMAIN及数据库配置

3、
php composer.phar install
php artisan key:generate

4、 登录后台->顶部按钮，更新缓存：/fladmin/login.php，账号：admin888，密码：123456


注意

只能放在根目录
如果要开启调试模式，请修改 .env 文件， APP_ENV=local 和 APP_DEBUG=true 。



Simple QrCode文档：https://www.simplesoftware.io/docs/simple-qrcode/zh
$qrcode = new \SimpleSoftwareIO\QrCode\BaconQrCodeGenerator;
return $qrcode->size(500)->generate('Make a qrcode without Laravel!');

二进制数据直接显示成二维码图片return '<img src="data:image/png;base64,'.base64_encode(\QrCode::format('png')->encoding('UTF-8')->size(200)->generate('http://www.baidu.com/')).'">';


composer.phar install安装出现proc_open错误，解决办法
修改composer.json中scripts下的"php artisan optimize"为"php artisan clear-compiled"


composer中国全量镜像修改
进入项目的根目录（也就是 composer.json 文件所在目录），执行如下命令：
composer config repo.packagist composer https://packagist.phpcomposer.com


微信开发，支付
https://easywechat.org/











