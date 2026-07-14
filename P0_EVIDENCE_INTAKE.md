# P0 Evidence Intake

填写这份表格后，我可以把 P0 的剩余事实核验完成，并直接推进 P1 的项目排序与信息架构。请只写你愿意公开、且能由代码、截图、报告、演示或个人确认支持的内容；不知道就填“未知”。

**填写方式：**保留每个问题，把 `TODO` 换成答案。中英文都可以。短句即可；我会把它整理成适合套磁/博士申请网站的英文文案。

## 1. Public profile decisions

- Public name: `Haojun Ma` / 是的，我的法定姓名是马好君 Haojun Ma，我有一个私下使用以及和在伯克利和回国后和外教沟通时使用，但不在任何法定文件的英文名June.
- Public site language: `English` / `Bilingual` / 我希望能提供中文和英文两个语言版本
- PhD target: `Fall 2027 entry` / 是的，其实我也考虑27fall的研究生申请
- A one-sentence research direction in your own words: 我其实还不是很明确，如果现在一定要提供会是“探索搭建更有效的、以人为中心的和AI的合作交互系统”
- Is this availability statement accurate? “Open to research collaborations and doctoral-application conversations in AI systems, HCI, and AI-assisted filmmaking.” / 我对AI systems不是那么确定，因为我对这方面的概念不是很清晰，我还在考虑要不要更技术一些，但我这方面的项目经历可能也不是那么充分；但是更偏设计的话，我的知识基础可能更薄弱
- CV file to link publicly: `Haojun_Ma_CV_new.pdf` / replacement file or status: CV之后很可能会进一步修改，目前用这个文件

## 2. Sign2Text — research and ownership

### Context

- Intended users and real use scenario: 针对聋哑人士在紧急场合比如公共交通上突发身体不适的场景，提供便捷的实时手语翻译
- Research question: 在实现低延迟的同时保证翻译的准确度，以及用户体验
- Status and date range: `Sep. 2025-present` 
- Team members and roles (including graduate collaborators/PI, without naming anyone who should stay private): 一个博士生负责进度和研究方向监督；一个研究生早期主要负责算法改进，但是他后来转向离线的手语视频算法改进，提高了离线模型的准确率；本科生一共3人，我是组长，另外两名组员主要参与了前期的调研和项目初期基线复现的部分工作，他们在项目中后期参与度很低，但这也有我的项目任务分配和领导能力的问题。
- What did you lead beyond coordination? 主要的软件实现、800词词表的设计、模型重新训练、可适应步长等部分都是我实现的

### My work

- Screens or workflows I personally built (camera, translation, history, dictionary, settings, vocabulary upload, etc.): 其实软件所有的功能都是我实现的，pipeline是有github仓库参考的，我重新训练过，并在online的算法增加了自适应步长
- Exact Swift files/components I primarily owned, if known: 所有的文件是我+codex AI coding的
- Literature review output: what did the 20+ paper review change in the design or model choice? 这部分其实有些tricky，我开始阅读的文献其实主要是离线的手语识别相关，但是当时我对这部分几乎没有了解，所以这部分其实主要是我进行基础的知识积累。在实现过程中，我们是直接找了近期的基本是实时手语识别的SOTA pipeline，然后在复现基础上，我结合了对离线手语分割时有论文通过速度变化分割词汇的思路，引入根据骨骼点速度变化的自适应步长思路；然后在项目实现过程中阅读了一些论文，对模型的进一步修改有了新的思路，比如模型除了骨骼点和RGB，也可以学习不同手语词汇的时长信息。
- “Continuous translation algorithm” contribution: name the method/model, your concrete change, and what code/experiment you touched. If you did not implement it, say so: 我实现的有从原本的词表提取了出现频率高的800词表进一步训练，还有实现了自适应步长，
- Did you build both the SwiftUI iOS app and the Expo/React Native prototype? Clarify which code should be linked: 我搭建了SwiftUI iOS app，连接了iphone手机进行了测试，但是实际的实时翻译效果其实不佳 

### Evidence and limits

- Can these be published? (screenshots, demo video, code, design diagram, model details, data details): 目前所有代码数据都在远程服务器，目前还没有同步到github，数据采用的是CSL-daily的数据，需要申请使用不能公开，其他都可以公开。
- Any measured latency, accuracy, vocabulary size, user feedback, or test result? Include setup and whether it can be public: TODO
- Known limitations: 我个人认为现在项目还在中期，后续在模型算法还有现实识别准确性上都需要提高。而且目前虽然在计算量上降低了，但是没有一个前后对照的数据，也没有对这个实时性提高的幅度的量化评估。
- Is `sign2text.app` safe to link publicly now? `No`, because 我还没有整理好后端代码，demo现实运行时识别准确率还有比较大的问题，经常输出同一个词汇。
- Is the ML repository meant to become public evidence after its README is cleaned, or should it stay unlinked? 之后会尽量做到公开。

## 3. CHI Social Media Research Dashboard — case-study facts

- Is the dataset statement accurate and public? “197 published records, mostly 2020-2025, tagged by content, method, and platform taxonomy.” Yes
- Did you create, validate, or only consume the dataset/labels? Describe exactly: 数据集是我们三人小组构建的，每人负责两个年份，从sigchi上下载所有social media相关论文，然后利用论文概要、tag、大语言模型分析论文得到ontent, method, and platform tags，然后核对一下。对于tag，我们集中管理，延续使用其他成员已经有同样含义的tag，最后对所有tag进行整理，合并含义过于近似的，并对所有tag分级。
- My exact code ownership beyond the Overview Panel and bar/pie-to-Sankey filtering: 我的代码贡献主要就是这两部分。
- The hardest interaction/state problem I solved: pie-to-Sankey filtering这部分是开发中最困难的，首先是tag的层级其实比较复杂且有三个类别，所以本地帮助数据筛选的json文件设计就有些困难，
- Chosen approach and trade-off (for example, shared store versus local component state; recomputation versus caching): TODO
- Team workflow and how integration/code review worked: 我们先进行一个讨论，确定一些基本的UI设计，然后实验室的研究生学姐进行UI设计，我们本科生三人小组进行代码实现。我们三人小组基本每周开2-3次线上会议，同步开发进度，并明确下一步开发任务。因为我们每个人负责的板块交叉比较少，所以可以同步进行开发，用github仓库进行代码管理，每个人在自己的分支进行开发，有阶段性成果会push并在审查后merge到主分支。
- Is the project complete? `Archived`
- Known limitations (dataset coverage, screen size, interaction complexity, mobile support, incomplete features): 数据比较少，只包含197篇论文，只有网页端；我们当时处理论文时都是手动打tag的，后续如果要拓展到大量的论文，需要开发自动化的打tag方法
- Screenshots I can publish: `overview` ， `filtered Sankey` ，`details` 都可以

## 4. Movie Agent — individual AI-systems work

- Is this entirely your own project? If there are collaborators, copied starters, or code-generation components that require attribution, describe them: 只有我，但是是偏向vibe coding，使用了codex AI 
- Current status and public date range: 目前没有公开的时间规划，还是本地项目
- Which of these did you personally build or substantially modify? `crewAI agents`, `MCP server`, `Letterboxd tool wrappers`, `FastAPI`, `Vue UI`, `SQLite persistence`, `settings/security`, `tests`, `other`: 整个项目基本都是我vibe coding实现的，crew AI 是一个已有的multi-agent系统，我只需要部署后设计好各个agent的职责和skill，
- One agent-orchestration/MCP lifecycle decision: what problem did it solve, what alternatives did you reject, and how does failure recovery work? TODO
- Can the public site say “working local prototype”? If yes, what was actually tested? 可以，是的测试过，可以得到个人的电影品味和电影推荐
- Known limitations (single-user, login/security challenges, provider/model quality, API reliability, no user study, etc.): 目前我只测试了cookie登录letterboxd，所以如果要使用包含电影品味功能的话，需要letterboxd账号并且需要用户自己提供cookie；目前也没有进行user study，调用get_film等API时确实有一定不稳定性
- Screenshots/video permitted for: `Home`, `History`, `Taste Profile`, `Settings`, `architecture`, `demo`: 都可以提供
- Preferred public project name: 目前还没确定，可以用movie chef(based on letterboxd)? 我还没想好

## 5. NLP Model Comparison — experimental integrity

- Was this solo, mentored, or collaborative? State the mentor’s role only if you want it public: mentored. 我的mentor当时教了我一些machine learning的基础知识，并展示且提供了他的一个类似的NLP项目代码。 
- Exact dataset name/version, record count, and source: 我的数据来自https://www.kaggle.com/code/ashwinshetgaonkar/movie-rating-sentiment-analysis/notebook
- Train/validation/test split: 70/15/15
- Preprocessing in order (including any fit-on-train-only controls): 词根化、小写、去除标点、tag、删除连接词
- Models actually evaluated and each baseline’s result: 逻辑回归、决策树，这两种分别使用了BOW和TF-IDF两种模型。好像没做baseline
- Which model achieved 89.3%, on which split, and under what metric definition?  LR+TF-IDF accuracy达到89.3%，在测试集上
- Hyperparameters selected on which split? Was the test set touched before final reporting? 超参是根据验证集的结果选的，具体数据可以看'项目展示.pptx'中的第7页部分图像。测试集之前没有被模型使用过
- Additional metrics (F1, AUROC, AUPRC), result table, confusion matrix, and error examples available: auroc, accuracy, auprc, f1_score; result table 也可以看'项目展示.pptx'中的第9页部分图像
- Public artifacts: repository / notebook / report / environment file / figures / none: 我还没公开，但目前有notebook, figures, 展示ppt可以整理后公开
- Known limitations: 我没探究LR+TF-IDF准确率最高的原因，缺少baseline，缺少进一步的深入分析

## 6. Systems evidence

### Pintos

- Course, dates, individual or team work: CS162 2025fall team work(4 people)
- System calls/features personally implemented: extensible files 里的inode部分，还有
- One concurrency/race-condition bug you diagnosed and how: TODO
- Public proof available (repository, test log, report, diagram, sanitized code): 我们原本的github仓库在课程结束后自动被删除了，但是我保留了代码压缩包，原本的报告应该也还能找到
- Publication permission and limitations: 不确定能不能公开，我们当时其实还有bug没有解决

### MiniSQL

- Course, dates, individual or team work: 数据库系统，浙江大学，2024 春夏学期
- Exact B+ tree ownership (insert/search/delete/split/merge/recovery/index integration/etc.): insert/search/delete/split/merge/ 
- Architecture or correctness/performance evidence: TODO
- Public proof available (repository, test log, report, diagram, sanitized code): TODO
- Publication permission and limitations: TODO

## 7. Future filmmaking / editing tool (optional candidate)

Do not treat a concept as a portfolio project yet. This section helps decide whether it can become one.

- Working title: TODO
- Who would use it, at which filmmaking step (writing, previsualization, production, VFX, editing, post, etc.)? TODO
- Concrete workflow problem: TODO
- What is already built today (not planned): TODO
- Your technical hypothesis or system idea: TODO
- Current repository/demo/screenshots/design evidence: TODO
- What will make it portfolio-ready, and by when? TODO
- May it be shown as `ongoing` before the first prototype is finished? TODO

## 8. Asset and publication log

| Asset / link | Project | What it proves | May publish? | Any privacy/copyright limitation? |
|---|---|---|---|---|
| TODO | TODO | TODO | Yes / No | TODO |
