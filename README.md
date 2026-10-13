# -ctf-agent
可本地运行的ctf比赛agent

这是第一版：
它现在能做什么？
一：源码分析：扫描 Python、PHP、JavaScript、HTML 等文件，提取相关代码片段。
Web 信息收集：检查本地靶场的 HTTP 响应头、表单、同源链接及常见公开路径。
AI 辅助分析：可选接入云端大模型，分析证据并提出下一步建议。
报告生成：保存为 JSON，方便复查和后续迭代。
二： 三步启动
解压项目后，在项目目录执行：
python -m venv .venv
激活环境并安装依赖：
# Linux / macOS
source .venv/bin/activate

# Windows PowerShell
.venv\Scripts\Activate.ps1

python -m pip install -r requirements.txt

先测试源码分析：
python ctf_web_agent.py --source ./你的题目源码目录 --no-llm

如果题目服务已经运行在本机的 8080 端口：
python ctf_web_agent.py --url 
http://127.0.0.1:8080/
 --no-llm


运行后会生成 ctf-web-report.json。


作者会看评论，有相关改进意见请评论
已更新至v2版本，详情见v2
