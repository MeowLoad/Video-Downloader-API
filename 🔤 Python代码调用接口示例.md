# Python 代码调用接口示例 📄

> [!IMPORTANT]
> ## 📢 哼哼猫最近新增了一些 API
> 请前往 👉 **[哼哼猫文档中心](https://docs.henghengmao.com/zh/developer/code-example/python)** 查看最新版本接口文档。

以下为 Python 语言调用提取接口的示例。示例代码中用到的 userId 和 secretKey 请前往[开发者接口管理中心](https://www.henghengmao.com/user/developer)获取。

```python
import requests
hhm_api = 'https://h.aaaapp.cn/single_post'     # 单个帖子提取接口 (如果主页批量提取使用：https://h.aaaapp.cn/posts)
user_id = 'C81E028D9DC2F636F06CA19862C'         # 这里改成你自己的 userId
secret_key = 'eac9387cb705c2dd70cd07e216c'      # 这里改成你自己的 secretKey

# 参数
url = 'https://www.bilibili.com/video/BV1sG4y1p7TA/'

params = {
    'userId': user_id,
    'secretKey': secret_key,
    'url': url
}
r = requests.post(hhm_api, json=params, verify=False)
print(r.json())
```
