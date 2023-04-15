# PenMods
> 一般来说，你不需要手动下载PenMods  
> **全新安装** 👉[Installer](https://github.com/PenUniverse/Installer)  
> **从旧版更新** 👉系统自带的OTA

这里是 PenMods[^1] 的发布仓库。

### Supported
 - 设备支持情况
 - 对于同代（按屏幕大小区分代）但不同发行版本较多的笔，不一一适配，仅适配功能最多的型号
 - 词典笔OS[^2]与目前的经典系统相差太大，目前的Mod不可能适配
 - 根据有道官方消息，YDP03x（三代）有计划全面升级到词典笔OS

🟢 | 测试通过 | 🟡 | 适配工作正在进行 | 🔴 | 暂无计划
-|-|-|-|-|-

型号 | 是否支持 | 系统版本 | Mod 版本 | 备注
-|-|-|-|-
YDP02x | 🟢 | 2.0.7 | Latest | 老系统请先自行刷到新系统，请保证`userdisk`分区可以正常读写
YDPG3 | 🟢 | 1.0.2, 1.0.3 | 1.1.8 | -
YDP03x | 🟡 | 2.7.2 | - | -
P5/X5 | 🔴 | N/A | N/A | -

### Notice
 - **PenMods 会拦截原系统更新**，若原系统有更新，需要先卸载PenMods才能更新（因为版本更新可能导致Mod不兼容或其他不可预料的情况）
 - 原本是想着开源的，由于在PenMods在开发周期内，**发给群友看的demo竟被恶意转载**，令人心寒(具体就不说了)，不得已暂不开源
 - **安装 PenMods 可能导致您失去有道官方保修**
 - 使用 PenMods 造成的一切后果均由您本人承担，与项目作者没有任何关系

### Attention
```diff
- 这是免费项目，未经许可任何人不得使用本仓库的任何内容进行商业活动。
- 若您发现有人非法盗卖 PenMods，请立即向相关交易平台举报并申请退款，盗卖者的每一笔订单都使项目向死亡方向更进一步！
```

### Features (1.2.0)
 - 🔥 增强AI助手
   - New Bing [配置指南](https://github.com/PenUniverse/PenMods-release/blob/main/ChatHubConfigurationGuide.md)
 - 增强单词本
   - 支持区分词组和单词（可开关）
   - 修复“选择语言”不会记住的Bug
   - 单词间相互大小写不敏感（可开关）
   - 导出更详细的内容
 - 增强“我的导入”
   - 重新实现文件管理：完全重写实现逻辑，不再依赖SQLite，性能提升
   - 重新实现自动播放：完全重写随机播放等逻辑
   - 增强系统播放器，增加有效音频检查，并在任何场景下都可用倍速和复读
   - 文件管理支持无限级子目录
   - 文件管理器现支持删除/改名/排序
   - 文件管理器可以打开 `txt`、`md`（markdown）文件
 - 增强查词功能
   - 查词支持手动输入（英文，可开关）
   - 扫描查询支持将扫描结果转到小写（可开关）
 - 息屏控制
   - 添加自动息屏时间控制：30秒，1,2,3,4,5分钟，永不
   - 添加场景智能息屏（音频播放器和单词本卡片模式不会自动息屏，可开关）
 - 电池信息查看/休眠控制
   - 添加电池信息：电池状态、电压、温度、健康状况、实时电流
   - 支持控制自动休眠时间：5,10,20,40分钟，永不
 - 安全选项
   - 可自设密码，目前有：重置选项页、开发者选项页
   - 防止尴尬系列：蓝牙断连自动静音，强制禁用自动发音/朗读，降低最低音量
   - 默认密码 `abcd`
 - 防止未经许可的日志上传
   - 清除系统日志
   - 防止未经许可的日志上传（行为记录，扫描图像等）
 - 开发者选项
   - 支持管理ADB/SSH服务（目前这个的功能比较简单）
   - 在WiFi连接页面显示当前词典笔的局域网IP地址
 - 录音机
   - 录音自动保存到 /userdisk/Music/录音文件
 - 手电筒
   - 可在设置内自行开关笔头灯
 - 键盘
   - 键盘已支持多行输入
   - 在键盘页面扫描，扫描结果将附加到光标处
 - 其他
   - 支持控制列式数据库单次查询限制（比如单词本原版一次只加载10个...）
   - 切换系统 A/B 槽位
   - 快速静音
   - 开机自动挂载根目录为可读写
   - 内置自动 vendor_storage 修复
   - OTA更新Mod
   
### Installation
 - 请移步 [Installer](https://github.com/PenUniverse/Installer)

### Contact Us
 - Telegram 群组 [PenUniverse](https://t.me/PenUniverse)
 - QQ交流群: [641664873](https://jq.qq.com/?_wv=1027&k=e0dvMZQU)

### Credits
 - [Dobby](https://github.com/jmpews/Dobby)
 - [Qt Project](https://www.qt.io/)
 - [injector](https://github.com/kubo/injector)

### Donation
 - 如果你觉得 PenMods 做的不错，请考虑捐赠 👉[爱发电](https://afdian.net/a/kbs007)

[^1]: PenMods by [RedbeanW](https://github.com/Redbeanw44602)
[^2]: [DictPen OS](https://smart.youdao.com/dictPenOS)
