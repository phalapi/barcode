# barcode
PhalApi 条形码扩展，基于[barcodegen](http://www.barcodebakery.com/)实现。


## 安装和配置
修改项目下的composer.json文件，并添加：  
```
    "phalapi/barcode":"dev-master"
```
然后执行```composer update```。  

## 注册
在/path/to/phalapi/config/di.php文件中，注册：  
```php
$di->barcode = function() {
    return new \PhalApi\BarCode\Lite();
};
```

## 使用
使用方式：直接输出条形码图片：
```php
\PhalApi\DI()->barcode->gen('PhalApi 2.x');
```

效果类似如下：  
![](http://7xiz2f.com1.z0.glb.clouddn.com/20171121234645_f8e021b5c98a7e4c75e4fa95bb4fb86e)

或者直接浏览器访问：[http://api.phalapi.net/?service=App.BarCode.Gen&check_sum=PhalApi%202.x](http://api.phalapi.net/?service=App.BarCode.Gen&check_sum=PhalApi%202.x)  
