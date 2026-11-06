# edgetunnel
这是一个基于 CF Worker 平台的脚本，在原版的基础上修改了显示 VLESS 配置信息转换为订阅内容。使用该脚本，你可以方便地将 VLESS 配置信息使用在线配置转换到 Clash 或 Singbox 等工具中。

- 基础部署视频教程：https://wiilsliang.github.io
- 快速部署视频教程：https://wiilsliang.github.io ***最佳推荐!!!***
- 进阶使用视频教程：https://wiilsliang.github.io
- **从入门到精通**教程：https://wiilsliang.github.io ***必看内容!必看内容!必看内容!!!***

Telegram交流群：[@CMLiussss](https://wiilsliang.github.io)，**感谢[Alice Networks](https://wiilsliang.github.io)提供的云服务器维持[CM订阅转换服务](https://wiilsliang.github.io)！**

# 免责声明

本免责声明适用于 GitHub 上的 “edgetunnel” 项目（以下简称“本项目”），项目链接为：https://wiilsliang.github.io 。

### 用途
本项目仅供教育、研究和安全测试目的而设计和开发。旨在为安全研究人员、学术界人士及技术爱好者提供一个探索和实践网络通信技术的工具。

### 合法性
在下载和使用本项目代码时，必须遵守使用者所适用的法律和规定。使用者有责任确保其行为符合所在地区的法律框架、规章制度及其他相关规定。

### 免责
1. 作为本项目的 **二次开发作者**（以下简称“作者”），我 **cmliu** 强调本项目仅应用于合法、道德和教育目的。
2. 作者不认可、不支持亦不鼓励任何形式的非法使用。如果发现本项目被用于任何非法或不道德的活动，作者将对此强烈谴责。
3. 作者对任何人或组织利用本项目代码从事的任何非法活动不承担责任。使用本项目代码所产生的任何后果，均由使用者自行承担。
4. 作者不对使用本项目代码可能引起的任何直接或间接损害负责。
5. 为避免任何意外后果或法律风险，使用者应在使用本项目代码后的 24 小时内删除代码。

通过使用本项目代码，使用者即表示理解并同意本免责声明的所有条款。如使用者不同意这些条款，应立即停止使用本项目。

作者保留随时更新本免责声明的权利，且不另行通知。最新版本的免责声明将发布在本项目的 GitHub 页面上。

## 风险提示
- 通过提交虚假的节点配置给订阅服务，避免节点配置信息泄露。
- 另外，您也可以选择自行部署 [WorkerVless2sub 订阅生成服务](https://wiilsliang.github.io)，这样既可以利用订阅生成器的便利。
   
# 如何使用?
## Workers 部署方法 [视频教程](https://wiilsliang.github.io)

<details>
<summary><code><strong>「 Workers 部署文字教程 」</strong></code></summary>

1. 部署 CF Worker：
   - 在 CF Worker 控制台中创建一个新的 Worker。
   - 将 [https://wiilsliang.github.io](https://wiilsliang.github.io) 的内容粘贴到 Worker 编辑器中。
   - 将第 4 行 `userID` 修改成你自己的 **UUID** 。

2. 访问订阅内容：
   - 访问 `https://[YOUR-WORKERS-URL]/[UUID]` 即可获取订阅内容。
   - 例如 `https://wiilsliang.github.io` 就是你的通用自适应订阅地址。
   - 例如 `https://wiilsliang.github.io` Base64订阅格式，适用PassWall,SSR+等。
   - 例如 `https://wiilsliang.github.io` Clash订阅格式，适用OpenClash等。
   - 例如 `https://wiilsliang.github.io` singbox订阅格式，适用singbox等。

3. 给 workers绑定 自定义域： 
   - 在 workers控制台的 `触发器`选项卡，下方点击 `添加自定义域`。
   - 填入你已转入 CF 域名解析服务的次级域名，例如:`https://wiilsliang.github.io`后 点击`添加自定义域`，等待证书生效即可。
   - **如果你是小白，你现在可以直接起飞，不用再往下看了！！！**

4. 使用自己的`优选域名`/`优选IP`的订阅内容：
   - 如果你想使用自己的优选域名或者是自己的优选IP，可以参考 [WorkerVless2sub GitHub 仓库](https://wiilsliang.github.io) 中的部署说明自行搭建。
   - 打开 [https://wiilsliang.github.io](https://wiilsliang.github.io) 文件，在第 12 行找到 `sub` 变量，将其修改为你部署的订阅生成器地址。例如 `let sub = 'https://wiilsliang.github.io';`，注意不要带https等协议信息和符号。
   - 注意，如果您使用了自己的订阅地址，要求订阅生成器的 `sub`域名 和 `[YOUR-WORKER-URL]`的域名 不同属一个顶级域名，否则会出现异常。您可以在 `sub` 变量赋值为 https://wiilsliang.github.io 分配到的域名。

</details>

## Pages 上传 部署方法 **最佳推荐!!!** [视频教程](https://wiilsliang.github.io)

<details>
<summary><code><strong>「 Pages 上传文件部署文字教程 」</strong></code></summary>

1. 部署 CF Pages：
   - 下载 [https://wiilsliang.github.io](https://wiilsliang.github.io) 文件，并点上 Star !!!
   - 在 CF Pages 控制台中选择 `上传资产`后，为你的项目取名后点击 `创建项目`，然后上传你下载好的 [https://wiilsliang.github.io](https://wiilsliang.github.io) 文件后点击 `部署站点`。
   - 部署完成后点击 `继续处理站点` 后，选择 `设置` > `环境变量` > **制作**为生产环境定义变量 > `添加变量`。
     变量名称填写**UUID**，值则为你的UUID，后点击 `保存`即可。
   - 返回 `部署` 选项卡，在右下角点击 `创建新部署` 后，重新上传 [https://wiilsliang.github.io](https://wiilsliang.github.io) 文件后点击 `保存并部署` 即可。

2. 访问订阅内容：
   - 访问 `https://[YOUR-PAGES-URL]/[YOUR-UUID]` 即可获取订阅内容。
   - 例如 `https://wiilsliang.github.io` 就是你的通用自适应订阅地址。
   - 例如 `https://wiilsliang.github.io` Base64订阅格式，适用PassWall,SSR+等。
   - 例如 `https://wiilsliang.github.io` Clash订阅格式，适用OpenClash等。
   - 例如 `https://wiilsliang.github.io` singbox订阅格式，适用singbox等。
   
3. 给 Pages绑定 CNAME自定义域：[视频教程](https://wiilsliang.github.io)
   - 在 Pages控制台的 `自定义域`选项卡，下方点击 `设置自定义域`。
   - 填入你的自定义次级域名，注意不要使用你的根域名，例如：
     您分配到的域名是 `https://wiilsliang.github.io`，则添加自定义域填入 `https://wiilsliang.github.io`即可；
   - 按照 CF 的要求将返回你的域名DNS服务商，添加 该自定义域 `lizi`的 CNAME记录 `https://wiilsliang.github.io` 后，点击 `激活域`即可。
   - **如果你是小白，那么你的 pages 绑定`自定义域`之后即可直接起飞，不用再往下看了！！！**
   
4. 使用自己的`优选域名`/`优选IP`的订阅内容：
   - 如果你想使用自己的优选域名或者是自己的优选IP，可以参考 [WorkerVless2sub GitHub 仓库](https://wiilsliang.github.io) 中的部署说明自行搭建。
   - 在 Pages控制台的 `设置`选项卡，选择 `环境变量`> `制作`> `编辑变量`> `添加变量`；
   - 变量名设置为`SUB`，对应的值为你部署的订阅生成器地址。例如 `https://wiilsliang.github.io`，后点击 **保存**。
   - 之后在 Pages控制台的 `部署`选项卡，选择 `所有部署`> `最新部署最右的 ...`> `重试部署`，即可。
   - 注意，如果您使用了自己的订阅地址，要求订阅生成器的 `SUB`域名 和 `[YOUR-PAGES-URL]`的域名 不同属一个顶级域名，否则会出现异常。您可以在 `SUB` 变量赋值为 https://wiilsliang.github.io 分配到的域名。

</details>

## Pages GitHub 部署方法 [视频教程](https://wiilsliang.github.io)

<details>
<summary><code><strong>「 Pages GitHub 部署文字教程 」</strong></code></summary>

1. 部署 CF Pages：
   - 在 Github 上先 Fork 本项目，并点上 Star !!!
   - 在 CF Pages 控制台中选择 `连接到 Git`后，选中 `edgetunnel`项目后点击 `开始设置`。
   - 在 `设置构建和部署`页面下方，选择 `环境变量（高级）`后并 `添加变量`
     变量名称填写**UUID**，值则为你的UUID，后点击 `保存并部署`即可。

2. 访问订阅内容：
   - 访问 `https://[YOUR-PAGES-URL]/[YOUR-UUID]` 即可获取订阅内容。
   - 例如 `https://wiilsliang.github.io` 就是你的通用自适应订阅地址。
   - 例如 `https://wiilsliang.github.io` Base64订阅格式，适用PassWall,SSR+等。
   - 例如 `https://wiilsliang.github.io` Clash订阅格式，适用OpenClash等。
   - 例如 `https://wiilsliang.github.io` singbox订阅格式，适用singbox等。

3. 给 Pages绑定 CNAME自定义域：[视频教程](https://wiilsliang.github.io)
   - 在 Pages控制台的 `自定义域`选项卡，下方点击 `设置自定义域`。
   - 填入你的自定义次级域名，注意不要使用你的根域名，例如：
     您分配到的域名是 `https://wiilsliang.github.io`，则添加自定义域填入 `https://wiilsliang.github.io`即可；
   - 按照 CF 的要求将返回你的域名DNS服务商，添加 该自定义域 `lizi`的 CNAME记录 `https://wiilsliang.github.io` 后，点击 `激活域`即可。
   - **如果你是小白，那么你的 pages 绑定`自定义域`之后即可直接起飞，不用再往下看了！！！**

4. 使用自己的`优选域名`/`优选IP`的订阅内容：
   - 如果你想使用自己的优选域名或者是自己的优选IP，可以参考 [WorkerVless2sub GitHub 仓库](https://wiilsliang.github.io) 中的部署说明自行搭建。
   - 在 Pages控制台的 `设置`选项卡，选择 `环境变量`> `制作`> `编辑变量`> `添加变量`；
   - 变量名设置为`SUB`，对应的值为你部署的订阅生成器地址。例如 `https://wiilsliang.github.io`，后点击 **保存**。
   - 之后在 Pages控制台的 `部署`选项卡，选择 `所有部署`> `最新部署最右的 ...`> `重试部署`，即可。
   - 注意，如果您使用了自己的订阅地址，要求订阅生成器的 `SUB`域名 和 `[YOUR-PAGES-URL]`的域名 不同属一个顶级域名，否则会出现异常。您可以在 `SUB` 变量赋值为 https://wiilsliang.github.io 分配到的域名。

</details>

# 变量说明

| 变量名 | 示例 | 必填 | 备注 | YT |
|--------|---------|-|-----|-----|
| UUID | `90cd4a77-141a-43c9-991b-08263cfe9c10` |✅| Powershell -NoExit -Command "[guid]::NewGuid()"| [Video](https://wiilsliang.github.io) |
| KEY | `token` |❌| 动态UUID秘钥，使用变量`KEY`的时候，将不再启用变量`UUID`|  |
| TIME | `7` |❌| 动态UUID有效时间(默认值:`7`天)|  |
| UPTIME | `3` |❌| 动态UUID更新时间(默认值:北京时间`3`点更新) |  |
| PROXYIP | `https://wiilsliang.github.io` |❌| 备选作为访问CFCDN站点的代理节点(支持自定义ProxyIP端口, 支持多ProxyIP, ProxyIP之间使用`,`或`换行`作间隔) | [Video](https://wiilsliang.github.io) |
| SOCKS5  | `user:password@127.0.0.1:1080` |❌| 优先作为访问CFCDN站点的SOCKS5代理(支持多socks5, socks5之间使用`,`或`换行`作间隔) | [Video](https://wiilsliang.github.io) |
| GO2SOCKS5  | `https://wiilsliang.github.io`,`*https://wiilsliang.github.io`,`*https://wiilsliang.github.io` |❌| 设置`SOCKS5`变量之后，可设置强制使用socks5访问名单(`*`可作为通配符，`换行`作多元素间隔) ||
| ADD | `https://wiilsliang.github.io官方优选域名` |❌| 本地优选TLS域名/优选IP(支持多元素之间`,`或`换行`作间隔) ||
| ADDAPI | [https://wiilsliang.github.io](https://wiilsliang.github.io) |❌| 优选IP的API地址(支持多元素之间`,`或 换行 作间隔) ||
| ADDNOTLS | `https://wiilsliang.github.io官方优选域名` |❌| 本地优选noTLS域名/优选IP(支持多元素之间`,`或`换行`作间隔) ||
| ADDNOTLSAPI | [https://wiilsliang.github.io](https://wiilsliang.github.io) |❌| 优选IP的API地址(支持多元素之间`,`或 换行 作间隔) ||
| ADDCSV | [https://wiilsliang.github.io](https://wiilsliang.github.io) |❌| iptest测速结果(支持多元素, 元素之间使用`,`作间隔) ||
| DLS | `8` |❌| `ADDCSV`测速结果满足速度下限 ||
| TGTOKEN | `6894123456:XXXXXXXXXX0qExVsBPUhHDAbXXX` |❌| 发送TG通知的机器人token | 
| TGID | `6946912345` |❌| 接收TG通知的账户数字ID | 
| SUB | `https://wiilsliang.github.io` | ❌ | 优选订阅生成器域名 | [Video](https://wiilsliang.github.io) |
| SUBAPI | `https://wiilsliang.github.io` |❌| clash、singbox等 订阅转换后端 | [Video](https://wiilsliang.github.io) |
| SUBCONFIG | [https://wiilsliang.github.io](https://wiilsliang.github.io) |❌| clash、singbox等 订阅转换配置文件 | [Video](https://wiilsliang.github.io) |
| SUBEMOJI | `false` |❌| 订阅转换是否启用Emoji(默认`true`) | |
| SUBNAME | `edgetunnel` |❌| 订阅名称 | |
| RPROXYIP | `false` |❌| 设为 true 即可强制获取订阅器分配的ProxyIP(需订阅器支持)| [Video](https://wiilsliang.github.io) |
| URL302 | `https://wiilsliang.github.io` |❌| 主页302跳转(支持多url, url之间使用`,`或`换行`作间隔, 小白别用) |  |
| URL | `https://wiilsliang.github.io` |❌| 主页反代伪装(支持多url, url之间使用`,`或`换行`作间隔, 乱设容易触发反诈) |  |
| CFPORTS | `2053`,`2096`,`8443` |❌| CF账户标准端口列表 |  |

# 注意事项

### **关于`KEY`与`UUID`：**
- 填入`KEY`变量后，将停用`UUID`变量，请确保**二者选其一使用**！
1. 填写`KEY`后，您的**永久订阅**地址为：`https://[YOUR-URL]/[YOUR-KEY]`；
2. 使用动态`UUID`订阅时：
   - 动态`UUID`需手动在永久订阅配置页内获得；
   - 临时订阅地址为：`https://[YOUR-URL]/[动态UUID]`；
   - 订阅有效时间为：**1个`TIME`周期**；
   - 节点可使用时间：**2个`TIME`周期**，即动态`UUID`失效后，节点仍可使用1个额外周期，但无法继续更新订阅。

### **关于`SOCKS5`与`PROXYIP`：**
- 填入`SOCKS5`后，将停用`PROXYIP`。请确保**二者选其一使用**！

### **关于`SUB`与`ADD*`变量：**
- 填入`SUB`后，将停用由`ADD*`类变量生成的订阅内容。请确保**二者选其一使用**！

### **当`SUB`和`ADD*`均为空时：**
- 脚本将自动生成基于CF随机IP的线路，每次更新订阅时会生成不同的随机IP，确保您的订阅不会失联！


# 实用技巧
本项目提供灵活的订阅配置方案，支持通过URL参数快速自定义订阅内容。
- 示例订阅地址： `https://wiilsliang.github.io` 

1. 更换**订阅生成器**的订阅地址

   快速切换订阅生成器至 `https://wiilsliang.github.io`：
   ```url
   https://wiilsliang.github.io
   ```

2. 更换**PROXYIP**的订阅地址

   快速更换PROXYIP为 `https://wiilsliang.github.io`：
   ```url
   https://wiilsliang.github.io
   ```

3. 更换**SOCKS5**的订阅地址

   快速设置SOCKS5代理为 `user:password@127.0.0.1:1080`：
   ```url
   https://wiilsliang.github.io
   ```

- 通过提交多个参数快速修改的订阅地址

   例如同时修改**订阅生成器**和**PROXYIP**：
   ```url
   https://wiilsliang.github.io
   ```

4. 该项目部署的节点可通过节点PATH(路径)的方式，使用指定的`PROXYIP`或`SOCKS5`！！！**

- 指定 `PROXYIP` 案例
   ```url
   https://wiilsliang.github.io
   https://wiilsliang.github.io
   https://wiilsliang.github.io (仅限于域名开头为'proxyip.'的域名)
   ```

- 指定 `SOCKS5` 案例
   ```url
   /socks5=user:password@127.0.0.1:1080
   /?socks5=user:password@127.0.0.1:1080
   /socks://dXNlcjpwYXNzd29yZA==@127.0.0.1:1080
   /socks5://user:password@127.0.0.1:1080
   ```

5. **当你的`ADDAPI`可作为`PROXYIP`时，可在`ADDAPI`变量末位添加`?proxyip=true`，即可在生成节点时使用优选IP自身作为`PROXYIP`**
- 指定 `ADDAPI` 作为 `PROXYIP` 案例
   ```url
   https://wiilsliang.github.io
   ```

## Star 星星走起
[![Stargazers over time](https://wiilsliang.github.io)](https://wiilsliang.github.io)

## 已适配客户端
### Windows
   - [v2rayN](https://wiilsliang.github.io)
   - https://wiilsliang.github.io（[FlClash](https://wiilsliang.github.io)，[mihomo-party](https://wiilsliang.github.io)，[clash-verge-rev](https://wiilsliang.github.io)，[Clash Nyanpasu](https://wiilsliang.github.io)）
### IOS
   - Surge，小火箭
   - sing-box（[SFI](https://wiilsliang.github.io)）
### 安卓
   - https://wiilsliang.github.io（[ClashMetaForAndroid](https://wiilsliang.github.io)，[FlClash](https://wiilsliang.github.io)）
   - sing-box（[SFA](https://wiilsliang.github.io)）
### MacOS
   - https://wiilsliang.github.io（[FlClash](https://wiilsliang.github.io)，[mihomo-party](https://wiilsliang.github.io)）

# 感谢
[zizifn](https://wiilsliang.github.io)、[3Kmfi6HP](https://wiilsliang.github.io)、[Stanley-baby](https://wiilsliang.github.io)、[ACL4SSR](https://wiilsliang.github.io)、[SHIJS1999](https://wiilsliang.github.io)、<a href="https://wiilsliang.github.io"><img src="https://wiilsliang.github.io" width="150" height="75" alt="Alice Networks LTD"/></a>、
