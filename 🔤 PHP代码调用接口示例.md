# PHP 代码调用接口示例 📄

> **📢 哼哼猫最近新增了一些 API，请前往 👉 [docs.henghengmao.com](https://docs.henghengmao.com/zh/developer/code-example/php) 查看最新版本接口文档。**

以下为 PHP 语言调用提取接口的示例。示例代码中用到的 userId 和 secretKey 请前往[开发者接口管理中心](https://www.henghengmao.com/user/developer)获取。

```php
$api = "https://h.aaaapp.cn/single_post";   # 单个帖子提取接口 (如果主页批量提取使用：https://h.aaaapp.cn/posts)
$userId = "C81E728D9DC2F636F06CC14862C";   //这里改成你自己的 userId
$secretKey = "eac9587cb785c2dd70cd07e116c";  //这里改成你自己的 secretKey

//参数
$url = "https://www.tiktok.com/@nike/video/7198345395863309611";

$params = array("url" => $url, "userId" => $userId, "secretKey" => $secretKey);
$options = array(
    "http" => array(
        "header"  => "Content-type: application/json",
        "method"  => "POST",
        "content" => json_encode($params),
    ),
    "ssl" => array(
        "verify_peer" => false,
        "verify_peer_name" => false,
    ),
);

$result = file_get_contents($api,false, stream_context_create($options));
var_dump($result);
```
