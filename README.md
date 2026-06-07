CPA 小白无脚本版使用说明

这版不需要运行任何脚本。
只需要手动下载、解压、复制配置、改几行内容、双击 exe。

第 1 步：
下载 CLIProxyAPI_xxx_windows_amd64.zip。

第 2 步：
解压后，把里面的文件放到：
D:\CLIProxyAPI

至少要看到：
D:\CLIProxyAPI\cli-proxy-api.exe
D:\CLIProxyAPI\config.example.yaml

第 3 步：
复制：
D:\CLIProxyAPI\config.example.yaml

重命名为：
D:\CLIProxyAPI\config.yaml

第 4 步：
用记事本打开 config.yaml，改 4 个地方：

1. 确认端口：
port: 8317

2. 设置后台登录密码：
remote-management:
  secret-key: "admin123"

3. 设置 NewAPI 调用 CPA 的 API Key：
api-keys:
  - "sk-cpa-test-123"

4. 设置代理：
proxy-url: "http://127.0.0.1:7890"

第 5 步：
双击：
D:\CLIProxyAPI\cli-proxy-api.exe

看到：
API server started successfully on :8317
就说明启动成功。

第 6 步：
浏览器打开：
http://localhost:8317/management.html

上传你的 Codex / OpenAI JSON，然后刷新配额。

第 7 步：
NewAPI 添加 OpenAI 渠道：

Base URL:
http://127.0.0.1:8317/v1

API Key:
sk-cpa-test-123

交流：
CPA 使用教程、AI 交流分享可以加 Q 群：753488355