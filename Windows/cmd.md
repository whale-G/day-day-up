# cmd使用

[TOC]

## 查看端口占用

1. 以管理员身份运行

2. `netstat -ano`列出所有端口的使用情况

3. 查看被占用端口对应的 PID（例如端口8081）：

   ```shell
   netstat -aon|findstr "8081"
   ```

4. 查看指定 PID 的进程：

   ```
   tasklist|findstr "PID"
   ```

5. 结束进程：

   ```shell
   # /F 强制 /T删除包括子进程
   taskkill /T /F /PID PID 
   ```

## window启用telnet客户端

### 通过控制面板

按下 **Win + R**，输入 *control* 打开控制面板。选择 **程序** > **程序和功能** > **启用或关闭 Windows 功能**。勾选 **Telnet 客户端**，点击 **确定**，等待安装完成。

### 使用telnet命令

1. 基本连接

   打开命令提示符或 PowerShell。输入以下命令连接到远程主机：

   ```shell
   telnet <IP地址> <端口号>
   ```

2. 测试特定端口

   用于检查服务是否正常运行。例如：

   ```shell
   telnet 192.168.1.100 80
   ```

3. 常用命令（连接成功后光标闪动且黑屏，输入`ctrl+]`进入telnet命令输入）

   *open <主机名>*：连接到指定主机。*close*：关闭当前连接。*quit*：退出 Telnet 模式。
