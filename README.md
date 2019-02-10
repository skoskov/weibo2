=================

PHP SDK for Sina Weibo open platform. 

SAE (Sina App Engine, http://sae.sina.com.cn ) has built-in SDK, no need to download, you need to manually call require_once('saetv2.ex.class.php') before use;

Composer
Composer.phar 

Microblog write interface description
Due to the Weibo open platform adjustment, the write interface needs to be switched to the share sharing interface, which is indicated at http://open.weibo.com/blog/%E3%80%90%E5%B9%B3%E5%8F%B0 %E5%85%AC%E5%91%8A%E3%80%91%E5%BE%AE%E5%8D%9A%E5%BC%80%E6%94%BE%E5%B9%B3%E5 %8F%B0%E5%88%86%E4%BA%AB%E5%88%B0%E5%BE%AE%E5%8D%9A%E6%8E%A5%E5%8F%A3%E5%8D %87%E7%BA%A7%E5%85%AC here. You need to use the $instance->share($status, $pic); method when calling, for example:

$c = new SaeTClientV2( WB_AKEY , WB_SKEY , WB_ACCESSTOKEN );
// 待发送的文字内容
$status = '发送的文字内容';
// 本地一张图片，也可以不带图片
$file_local = '5486087cly1fhh2yaksr1j20j60srtd0.jpg';
// 拼接'http://weibosdk.sinaapp.com/'是因为这个share接口至少要带上一个【安全域名】下的链接。
$ret = $c->share($status.'http://weibosdk.sinaapp.com/', $file_local);
var_dump($ret);
Update
Increase sharing interface on July 14, 2017
Revised V2 version of a notice on February 20, 2013
Revised V2 version of two hand errors on December 16, 2011
The V2 version of the PHP SDK was released on October 21, 2011, based on the latest interface package in http://open.weibo.com/wiki/API%E6%96%87%E6%A1%A3_V2 .
On June 16, 2011, the OAuth2 version of the PHP SDK was released, and the Basic authentication SDK was deleted (the microblog open platform does not support Basic authentication).
On November 17, 2010, the default callback url of the demo program was modified incorrectly in some access modes.
On June 29, 2010, the Basic authentication version & OAuth version added the verify_credentials function to get the current user information. OAuth added update_avatar to update the avatar.
Added support for image release on May 5, 2010 Basic certified version
Added image support for OAuth certified version on May 12, 2010
Description
Demo demo address

Demo version V2: http://weibosdk.sinaapp.com/
Application Demo on the site: http://apps.weibo.com/weibosdk
OAuth version of Demo: http://saettest.sinaapp.com/
How to apply for an API Key

You need to have an API Key for Sina Weibo Open Platform. Apply here: http://open.weibo.com

About the function of the Class

Based on OAuth authentication.
Completed until October 21, 2011, all interface packages
Sina Weibo V2 version PHPSDK Demo tutorial

1. Create an application at open.weibo.com and get the API KEY. Set the "Apply Callback Page" address in "Authorization Settings" to " http://host/callback.php", where host is the website domain name.
2. Download Demo, then extract, modify WB_AKEY in config.php as App Key, WB_SKEY as App Secret, and WB_CALLBACK_URL as the callback page address just filled in.
3. Upload to PHP space
Sina Weibo station application Demo tutorial

1. Create an in-site application at open.weibo.com and get the API KEY
2. Edit the application properties and set the "Site Application Address" in the "Application Page"
3. Download, unzip, modify WB_AKEY in config.php as App Key, WB_SKEY as App Secret, and CANVAS_PAGE as "In-Site Application Address" set in "Application Page"
4. Upload code to PHP space
5. Edit the application properties, set the "Application Actual Address" in the "Application Page" to the address of the apps.php that just uploaded the code, for example: " http://xxxxx.sinaapp.com/apps.php", set "Iframe" The height is "2000px.
6. Access the “In-Site Application Address” you just set.
OAuth version of the demo tutorial

1. Create an application at open.weibo.com and get the API KEY
2. Download, then extract, modify WB_AKEY in config.php as App Key, WB_SKEY as App Secret.
3. Upload to PHP space
Bug tracker
Have a bug? Please create an issue here on GitHub!

Https://github.com/xiaosier/libweibo/issues

Authors
Http://weibo.com/lazypeople
Http://lazy.changes.com.cn
License
Copyright 2011 SINA, Inc. Copyright 2011 SAE

Licensed under the Apache License, Version 2.0: http://www.apache.org/licenses/LICENSE-2.0
