# PenMods
> 一般来说，你不需要手动下载PenMods  
> **全新安装** 👉[Installer](https://github.com/PenUniverse/Installer)  
> **从旧版更新** 👉系统自带的OTA

这里是 PenMods 的发布仓库。

### Supported
 - 设备支持情况
 - 对于同代（按屏幕大小区分代）但不同发行版本较多的笔，不一一适配，仅适配功能最多的型号

型号 | 是否支持 | 系统版本 | Mod 版本 | 备注
-|-|-|-|-
YDP021 | ✔ | 2.0.4 | 1.0.0 | 老系统请先自行刷到新系统，请保证`userdisk`分区可以正常读写
YDP022 | ❓ | - | - | 缺少测试数据，理论与YDP021同样支持
YDP032 | ❌ | - | - | 适配工作正在抽空进行
P5/X5 | ❌ | - | - | 没有适配计划

### Notice
 - **PenMods 会拦截原系统更新**，若原系统有更新，需要先卸载PenMods才能更新（因为版本更新可能导致Mod不兼容或其他不可预料的情况）
 - 原本是想着开源的，由于在PenMods在开发周期内，**发给群友看的demo竟被恶意转载**，令人心寒(具体就不说了)，不得已暂不开源 [Mod的查毒报告](https://s.threatbook.com/report/file/119163811bf90da15dd6d5145df44eb74d40fb8e2de74c22c609fb4cbc80054d)
 - **安装 PenMods 可能导致您失去有道官方保修**
 - 使用 PenMods 造成的一切后果均由您本人承担，与项目作者没有任何关系

### Features (1.0.0)
 - 增强单词本
   - 支持区分词组和单词（可开关）
   - 修复“选择语言”不会记住的Bug
   - 单词间相互大小写不敏感（可开关）
   - 导出更详细的内容
 - 增强“我的导入”
   - 重新实现文件管理：完全重写实现逻辑，不再依赖SQLite，性能提升
   - 文件管理支持无限级子目录
   - 修复原版播放器播放无效音频会一直重播导致高占用的问题（添加文件实际类型检查）
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
   - 可自设密码，目前只有：重置选项页面输入密码
   - 防止尴尬系列：蓝牙断连自动静音，强制禁用自动发音/朗读，降低最低音量
 - 防止未经许可的日志上传
   - 清除系统日志
   - 防止未经许可的日志上传（行为记录，扫描图像等）
 - 开发者选项
   - 支持管理ADB/SSH服务（目前这个的功能比较简单）
   - 在WiFi连接页面显示当前词典笔的局域网IP地址
 - 录音机
   - 录音自动保存到 /userdisk/Music/录音文件
 - 其他
   - 支持控制列式数据库单次查询限制（比如单词本原版一次只加载10个...）
   - OTA更新Mod
   
### Installation
 - 请移步 [Installer](https://github.com/PenUniverse/Installer)

### Credits
 - [Dobby](https://github.com/jmpews/Dobby)
 - [Qt Project](https://www.qt.io/)
 - [injector](https://github.com/kubo/injector)

### Donation
 - 如果你觉得 PenMods 做的不错，请考虑捐赠 👉[爱发电](https://afdian.net/a/kbs007)
