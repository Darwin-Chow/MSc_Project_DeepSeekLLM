## 配置说明

OpenManus 需要配置使用的 LLM API，请按以下步骤设置：

1. 在 `config` 目录创建 `config.toml` 文件（可从示例复制）：

```bash
cp config/config.example.toml config/config.toml
```

2. 编辑 `config/config.toml` 添加 API 密钥和自定义设置：

```toml
# 全局 LLM 配置
[llm]
model = "gpt-4o"
base_url = "https://api.openai.com/v1"
api_key = "sk-..."  # 替换为真实 API 密钥
max_tokens = 4096
temperature = 0.0

# 可选特定 LLM 模型配置
[llm.vision]
model = "gpt-4o"
base_url = "https://api.openai.com/v1"
api_key = "sk-..."  # 替换为真实 API 密钥
```

## 快速启动

一行命令运行 OpenManus：

```bash
python main.py
```

然后通过终端输入你的创意！

### Web界面

您也可以通过用户友好的Web界面使用OpenManus：

```bash
uvicorn app.web.app:app --reload
```
或者
```bash
python web_run.py
```

然后打开浏览器，访问`http://localhost:8000`即可使用Web界面。Web界面提供以下功能：

- 通过类聊天界面与OpenManus交互
- 实时监控AI思考过程
- 查看和访问工作区文件
- 直观地查看执行进度

如需体验开发中版本，可运行：

```bash
python run_flow.py
```
