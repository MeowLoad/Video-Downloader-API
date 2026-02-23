# JavaScript 代码调用接口示例 📄

> **📢 哼哼猫最近新增了一些 API，请前往 👉 [docs.henghengmao.com](https://docs.henghengmao.com/zh/developer) 查看最新版本接口文档。**

以下为 JavaScript 语言调用提取接口的示例。示例代码中用到的 userId 和 secretKey 请前往[开发者接口管理中心](https://www.henghengmao.com/user/developer)获取。

```javascript
const api = "https://h.aaaapp.cn/single_post"; // 单个帖子提取接口 (如果主页批量提取使用：https://h.aaaapp.cn/posts)
const userId = "C81E728D9DC2F636F06CC14862C"; //这里改成你自己的 userId
const secretKey = "eac9587cb785c2dd70cd07e116c"; //这里改成你自己的 secretKey

let url = "https://v.douyin.com/MGkSpJS/";

const params = {
  userId: userId,
  secretKey: secretKey,
  url: url,
};

const xhr = new XMLHttpRequest();
xhr.open("POST", api, true);
xhr.setRequestHeader("content-type", "application/json;charset=UTF-8");
xhr.onreadystatechange = function () {
  if (xhr.readyState === 4) {
    console.log(xhr.responseText);
  }
};
xhr.send(JSON.stringify(params));
```
