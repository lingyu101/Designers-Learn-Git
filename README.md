二、开启php的openssl扩展，下载ca证书


具体操作如下：



1、开启php扩展，左键wamp-php-php扩展-php_openssl前面打勾。

2、在D:\wamp\wamp\bin\php\php5.4.12（看个人安装路径确定）下找到php.ini文件，用sublime打开。

查找 extension=php_openssl.dll ，删除extension=php_openssl.dll前面的分号，取消注释，从而启用OpenSSL插件。

注意：因为SSL连接需要认证，所以继续下面的步骤之前，需要准备好CA证书（建议把证书保存到D:\wamp\wamp\bin\php\php5.4.12\verify目录中），可以从https://curl.haxx.se/docs/caextract.html处下载。（如果直接打开文件的话，另存为修改文件名即可）

3、如果php.ini文件中能够找到

;openssl.cafile=

和上面一样，去掉分号注释，设置CA证书为D:\wamp\wamp\bin\php\php5.4.12\verify，即

openssl.cafile= "D:\wamp\wamp\bin\php\php5.4.12\verify\cacert.pem"如果无法找到直接添加

openssl.cafile= "D:\wamp\wamp\bin\php\php5.4.12\verify\cacert.pem"
--------------------- 
作者：fjnjxr 
来源：CSDN 
原文：https://blog.csdn.net/fjnjxr/article/details/54968072 
版权声明：本文为博主原创文章，转载请附上博文链接！
