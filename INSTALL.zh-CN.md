# The Poem 品牌搜集：安装与试用

## 1. 选择下载包

打开 https://github.com/gabrielle-xue/poem-brand-discovery-downloads/releases/tag/v0.1.0-beta.1 ，在 Assets 下载：
- Codex 或 Work 单技能上传：poem-brand-discovery.zip。
- Work 管理员插件上传：poem-brand-discovery-plugin.zip。

不需要原开发仓库访问权限。不要下载 Source code ZIP。两个包不必同时安装。

发布标记 v0.1.0-beta.1；技能/插件内部版本 0.3.0。公开下载版只修改安装说明，研究代码、规则与模板不变。

## 2. 在 ChatGPT Work 中试用

以下界面可能因工作区、套餐和权限不同而变化，以当前实际入口和扫描结果为准。

**有单技能上传入口：**
1. 在侧栏 Plugins 中进入 Skills，选择 Create / Upload from your computer。
2. 上传 poem-brand-discovery.zip，按扫描提示处理，以 Installed 或可选用状态为准。
3. 新建 Work 会话，输入 @，选择 The Poem 品牌搜集 / poem-brand-discovery。
4. 先运行下方安装验收提示，再在私密会话提交本次项目 brief。

**有管理员插件上传入口：**
1. 管理员进入 admin.openai.com，选择目标工作区，在 Plugins 中选择 Add / Upload plugin。
2. 上传 poem-brand-discovery-plugin.zip，等待扫描并依平台要求审阅。
3. 扫描通过后按工作区支持的分享/目录方式开放；同事在 Plugins 的工作区目录中找到插件并安装。
4. 新建 Work 会话，用 @ 选择插件或技能，再运行安装验收提示。

普通聊天附件不等于持久安装；上传成功也不等于扫描、安装和调用全部成功。找不到上述入口时，请联系工作区管理员，或使用 Codex。不要上传到 GPT 知识库来代替技能安装。

平台入口参考：[Skills in ChatGPT](https://help.openai.com/en/articles/20001066-skills-in-chatgpt)、[Plugins in ChatGPT](https://help.openai.com/en/articles/20001256-plugins-in-chatgpt)。本次未重新验证所有界面。

## 3. 在 Codex 中安装

要求 Python 3.10+，并带 venv/ensurepip。无需全局 pip 安装，包内含离线依赖。

1. 下载并解压 poem-brand-discovery.zip。
2. 在解压后的上级目录打开终端，执行：
   - macOS / Linux：`python3 poem-brand-discovery/install.py`
   - Windows：`py -3 poem-brand-discovery/install.py`
3. 安装器会在旁边创建 ThePoem-Workspace，并打印项目目录。已有项目可加 `--project "你的项目目录"`。已有不同版本时先备份，安装器不会直接覆盖。
4. 用 Codex 打开安装器打印的项目目录，新建会话，输入 /skills 或 $，选择 poem-brand-discovery。未出现时确认打开的是目标目录并重启 Codex。
5. 运行下面的验收提示。实际研究输出位于项目的 output/；brief 与证据位于 projects/。

参考：[Codex skills](https://developers.openai.com/codex/skills)。卸载时移走项目中的 .agents/skills/poem-brand-discovery；项目数据与 Excel 可保留。

## 4. 首次安装验收

复制到已选中技能的新会话：

> 请使用本技能做安装验收：不联网、不新增品牌、不发信。先报告技能实际路径，运行 doctor 及 setup，从空模板创建“安装验收”独立 brief，生成 plan 并明确只是计划；用空 research-data 导出 Excel 并重读，报告七个工作表与首页十列。不要把这个结果写成实时品牌研究或平台端到端验证。

验收通过后再提交实际项目需求。每次项目都独立配置，不继承粤海天地等历史案例条件。技能安装不授予联网、社媒登录或邮件权限。

## 5. 已验证范围与反馈

GPT Work 已完成一次粤海天地新店 10 品牌实际测试；本地 Linux Python 3.12 安装与导出已有验证。公开下载版重新检查压缩完整性、文件清单和逐文件校验。

同事安装、管理员插件上传、所有平台覆盖仍待验证；小红书与 Instagram 的全面访问未完成验证。受阻时记录实际范围与原因，并查官网、媒体或展会等替代来源。

公开包不包含内部原始资料、合作资源库、品牌数据库和项目样例输入。技能正文提到的仓库回放样例不随本公开包提供；无需获取样例即可处理自己的项目。不要将内部资料上传到本公开仓库或 Issues。

反馈请通过原分享者的私密渠道提供：平台、安装入口、失败步骤、错误原文及脱敏截图。不要附上内部 brief、联系人、研究数据、令牌或账号凭证。
