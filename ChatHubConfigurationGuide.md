# AI ChatHub 配置指南

目前支持 & 计划支持的服务

名称 | 状态 | 实现方式 | 备注
:-:|:-:|:-:|:-:
New Bing | 🟢 | 逆向工程 | 暂时不支持 GenerateContentQuery
ChatGPT | 🟡 | API | 暂时不支持

## New Bing
> ⚠ 词典笔版New Bing通过分析网页版ChatHub聊天接口实现，可能导致您的账号被封禁、被退出候补名单等后果，项目作者不对产生的任何后果负责，若有顾虑请勿使用。

### 1. 确保您已加入候补名单
> ⚠ 如果您在中国大陆，请在接下来的步骤**使用全局代理**

打开 [https://www.bing.com/new](https://www.bing.com/new) 若您看到的内容类似于下图，则说明您有 New Bing 的访问权限。  
否则，请先申请，确保您处于 New Bing 候补名单中。

![image](https://user-images.githubusercontent.com/29711228/232077698-ec01249a-79cd-4055-8285-de8a0eca19c5.png)

点击 [立即聊天](https://www.bing.com/chat)，然后随意询问一个问题，观察 New Bing 是否能够正常回答。

![image](https://user-images.githubusercontent.com/29711228/232079326-a4f7d8e3-807a-4109-bc7d-0ae157e81647.png)

如果能正常回答，则可以进入下一步。如果出现 `Sorry, looks like your network settings are preventing access to this feature.` 请参阅文末 **使用代理** 章节，并确保您确实已加入候补名单。

### 2. 安装浏览器插件
安装 [Cookie Editor](https://microsoftedge.microsoft.com/addons/detail/cookieeditor/neaplmfkghagebokkhpjpoebhdledlfi)，只需点击 **获取** 即可安装。  

![image](https://user-images.githubusercontent.com/29711228/232080829-4958f46d-a85d-4af1-95a0-793f2654a356.png)

`Cookies` 是网页留存在用户浏览器上的一些内容，主要用于储存用户名、密码等信息，这些信息和您的密码同样重要，请务必妥善保管。

### 3. 导出 Cookies 为 Json 格式
您不需要知道何为 `Json`，只需**在刚刚的聊天网页**找到 Cookies Editor 图标（🍪）并按图操作。
点击 “Export as JSON”，点完后什么似乎也不会发生，这是正常现象。

![image](https://user-images.githubusercontent.com/29711228/232083396-86ca5fda-73e9-4319-aff5-b564843e6ca4.png)

顺便一提，如果你找不到饼干图标，那么它可能藏在![image](https://user-images.githubusercontent.com/29711228/232083989-7e6bd0f3-81ca-4aad-97a2-5bfb6fcf125a.png)里。

### 4. 保存文件为 `bing-cookies.json`
还是那句话，`Json` 是什么并不重要，现在你需要新建一个文本文件。

![image](https://user-images.githubusercontent.com/29711228/232085169-d7d365ee-42d9-4b1a-ab17-c5ba9e19d3f0.png)

然后，右键粘贴或 `Ctrl+V` 粘贴 Cookies 信息。最后不要忘记保存。

把刚刚新建的文本文件重命名为 `bing-cookies.json`
出现下面的提示选择 **是**

![image](https://user-images.githubusercontent.com/29711228/232086316-15c0c7d3-17fb-4d62-8926-eb7b07bc276c.png)

正常情况下，一定会出现上面的提示。否则你的电脑可能没有打开显示文件拓展名（自然无法修改文件拓展名），这样打开：

![image](https://user-images.githubusercontent.com/29711228/232086908-bfa1d1c9-6797-47dd-9513-f58721f1ff32.png)

### 5. 转移文件到词典笔
连接词典笔，将 `bing-cookies.json` 拖动到 `Music` 文件夹内。

![image](https://user-images.githubusercontent.com/29711228/232087848-d268091d-aacf-4433-b87d-d03e78800c71.png)

重启即可使用 New Bing，enjoy it~

### 6. （可选）使用代理
> ⚠ New Bing 代理服务的提供者理论上可以获得您的 Cookies 数据，因此在你选择使用某个代理服务时请务必确保信任服务提供者。

如果您现在在中国大陆地区，或者您单位的网络（如部分校园网）阻止了 New Bing 的链接，那么您需要配置代理才能使用 New Bing。  
词典笔版 New Bing 提供了一种修改与 New Bing API 通信链接的选项以允许反向代理，PenMods 社群友情提供了一个代理站点，请加群获取。  
下面是代理的配置方法：

 - 在设置中找到 Bing ChatBot，点击进入
 - 点击标题修改该项内容
 - *Signature 申请地址* 必须以 `https://` 或 `http://` 开头
 - *Bing ChatHub 地址* 必须以 `ws://` 或 `wss://` 开头

![wayland-screenshot-2023-04-15_00-01-05](https://user-images.githubusercontent.com/29711228/232096534-881fbe72-93e6-4138-8738-f0e1188976e9.png)

网上关于中国大陆地区使用 New Bing 的教程经常会提到设置 `x-forwarded-for` 请求头，这通常是有效的，并且我已将这个请求头内置在，因此无需手动设置。  
得益于内置请求头与代理，即使你的浏览器无法访问 New Bing，PenMods 提供的 New Bing 往往也可以正常使用。
