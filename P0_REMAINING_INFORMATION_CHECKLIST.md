# P0 Remaining Information Checklist

这份清单只收录当前仍需明确或补充的信息。回答不知道的项目时，可以直接写“未知”；没有量化结果时，可以写“暂无可靠测量”，不需要为了完整而推测。

## A. 进入 P1 前需要明确

以下内容会影响主页定位、项目是否入选或公开陈述是否准确。完成后即可把 P0 视为正式结束。

### 1. 主页定位与申请目标

- [ ] 确认是否接受以下临时研究定位，或提供修改版本：
  - English: `I build and study human-centered AI systems that turn model capabilities into usable interactive tools.`
  - 中文：`探索并构建以人为中心的 AI 交互系统，将模型能力转化为可用的交互工具。`
  - 回答：`接受`
- [ ] 确认主页当前是否公开写 `Fall 2027 graduate/PhD applicant`；如果暂时不希望公开，写明何时再加入。
  - 回答：`如果这不会影响我申请科研机会或者跟老师联系，可以公开`
- [ ] 确认公开 availability statement。可以直接修改下面这句：
  - `Open to research collaborations and conversations about human-centered AI, interactive systems, and future graduate study.`
  - 回答：`好的，但其实我也在考虑用这个网站进行实习投递，后续可以考虑添加open to internship`

### 2. Sign2Text 的公开边界

- [ ] 确认当前主页是否完全不链接 `sign2text.app` 和 ML 仓库。
  - 建议答案：`暂不链接；只展示允许公开的截图、架构图和文字说明。`
  - 回答：`目前不链接，但是后续整理后还是有比较大可能可以提供的`
- [ ] 如果没有可靠的 accuracy、latency 或用户测试数据，确认可以公开写“暂无可靠量化结果”。
  - 回答：`具体情况可以参考 项目成果.docx，浙江大学大学生创新创业训练计划项目结题报告.docx，srtp结项答辩.pptx文件`
- [ ] 补充所参考的实时手语识别 pipeline：论文或仓库名称、链接，以及自己复现和修改的代码边界。
  - 回答：`TODO`
- [ ] 用 2–4 句话说明“自适应步长”：输入信号是什么、如何调整步长、希望解决什么问题、目前是否验证有效。
  - 回答：`TODO`
- [ ] 说明 800 词词表如何选出，例如词频来源、筛选规则，以及重新训练了哪个模型。
  - 回答：`TODO`

### 3. NLP 项目的事实纠正

- [ ] 确认实际比较的是 `Logistic Regression` 和 `Random Forest`，而不是单棵 Decision Tree。
  - 回答：`是的`
- [ ] 确认数据集描述：`4,000 IMDb movie reviews`；补充原始数据集名称或下载页面，而不只是参考 notebook 链接。
  - 回答：`下砸界面：https://www.kaggle.com/code/ashwinshetgaonkar/movie-rating-sentiment-analysis/input`
- [ ] 确认 BOW/TF-IDF vectorizer 是否只在训练集上 `fit`，再用于 validation/test。
  - 回答：`是的。但是对超参的确定是根据validation数据集的结果`
- [ ] 说明预处理中的 `tag` 是否指删除 HTML tags；“删除连接词”是否实际指删除 stop words。
  - 回答：`这里主要是通过调用函数：        text_value = gensim.parsing.preprocessing.strip_tags(text_value)
        text_value = gensim.parsing.preprocessing.strip_punctuation(text_value)
        text_value = gensim.parsing.preprocessing.strip_multiple_whitespaces(text_value)
        text_value = gensim.parsing.preprocessing.strip_numeric(text_value)
        text_value = gensim.parsing.preprocessing.remove_stopwords(text_value)`
- [ ] 说明导师提供的示例代码与自己的实现边界：哪些结构被参考，哪些数据处理、训练、调参和可视化由自己完成。
  - 回答：`首先，我们不是针对同一个数据集进行的。老师当时也没有调参过程；可视化部分我主要添加了词云的效果，老师当时的数据集用t-sne降维效果比较好，我的数据降维效果不佳，所以没有使用这个降维的可视化；其实数据处理还有前5个影响最大的词汇的代码结构，我很大程度上参考的老师的代码思路`

### 4. MiniSQL 的日期与公开许可

- [ ] 解决日期冲突：intake 写 `2024 春夏`，个人报告日期为 `2025-06-12`。确认正确的课程学期和项目完成时间。
  - 回答：`实际时间是25年春夏学期`
- [ ] 确认这是个人实现、团队项目中的个人模块，还是基于课程框架完成的个人作业。
  - 回答：`完整的miniSQL是基于课程框架完成的小组作业。3230103576_马好君_minisql个人报告.pdf文件中的是我在团队中的个人模块部分`
- [ ] 确认哪些材料允许公开：个人报告、代码片段、测试结果、B+ Tree 可视化图。
  - 回答：`这些材料都可以公开`
- [ ] 如果代码不能公开，确认是否允许在详情页展示经过删减的伪代码、结构图和测试说明。
  - 回答：`TODO`

## B. P1 项目筛选时需要决定

这些是项目阵容决策，不要求先补齐完整详情页内容。

- [ ] 确认首批主项目是否采用：`Sign2Text`、`Movie Agent`、`CHI Dashboard`。
  - 回答：`我觉得这里可以再讨论一下，还有movie agent项目是我个人兴趣项目，我觉得可能在难度和深度上不够？`
- [ ] 确认 MiniSQL 是否作为第四个 supporting project；如果公开许可不明确，则暂不进入主页。
  - 回答：`可以添加，但这只是课程项目中的一个，如果这个可以添加，那么其他课程项目是不是也可以添加？我认为需要讨论一下`
- [ ] 确认 NLP 是否先作为次级项目，待 notebook 审查和归属说明完成后再决定是否进入 Selected Work。
  - 回答：`次级项目和主项目主要的分别是什么？我对这个项目的考虑主要是它的复现性质比较强，但这其实也算是我的第一个科研项目，也和电影相关，所以我比较想放在项目里`
- [ ] 确认 Pintos 暂不进入主页主项目区。
  - 回答：`可以`
- [ ] 确认未来影视/剪辑工具仍是概念，不建立项目卡片或 `coming soon` 页面。
  - 回答：`这个SceneZero项目已经有一版demo app实现了，我认为可以建立项目卡片`

## C. 可在 P2–P3 补充，不阻塞 P1

### CHI Dashboard

- [ ] 说明 pie-to-Sankey 筛选的数据结构和状态流。
- [ ] 说明为何选择该方案、考虑过什么替代方案，以及主要代价。
- [ ] 准备 overview、filtered Sankey、details 三类截图。
- [ ] 确认公开仓库、在线 demo 和 197 条记录的描述可继续使用。

### Movie Agent

- [ ] 确认项目开始日期和状态，例如 `Mar. 2026–present · working local prototype`。
- [ ] 确认临时公开名称；未决定前可继续使用 `Movie Agent`。
- [ ] 记录一个 agent orchestration 或 MCP lifecycle 决策。
- [ ] 说明 API 调用失败、cookie 失效或工具无结果时的恢复方式。
- [ ] 明确 Codex 辅助开发、CrewAI 框架使用与个人系统设计之间的边界。
- [ ] 准备 Home、History、Taste Profile、Settings 和 architecture 截图。

### Sign2Text

- [ ] 准备不会暴露受限数据的应用截图、流程图或短视频。
- [ ] 记录测试设备、运行条件和典型失败现象。
- [ ] 后续有测量时，记录数据集、实验设置、指标定义和前后对照；没有数据时继续保持“未量化”。

### NLP

- [ ] 整理 notebook、依赖版本、结果图和完整结果表。
- [ ] 补充 confusion matrix 或代表性错误样例；若没有，明确写“未进行错误分析”。
- [ ] 决定 notebook/PPT 是否公开，并移除不应公开的信息。

### Systems

- [ ] Pintos：补全个人实现的 feature/system call 列表。
- [ ] Pintos：记录一个确实由自己诊断的 concurrency/race-condition 问题；无法准确归属时不展示。
- [ ] Pintos：确认课程代码和报告的公开政策。
- [ ] MiniSQL：整理测试、调试过程和 B+ Tree 结构证据。

## D. 素材公开记录

为每个准备上站的素材填写一行：

| 素材或链接 | 项目 | 能证明什么 | 可以公开？ | 限制或处理方式 |
|---|---|---|---|---|
| `TODO` | `TODO` | `TODO` | Yes / No | `TODO` |

## P0 完成判定

满足以下条件即可正式关闭 P0：

- [ ] A 区问题均已回答，或明确记录为未知/暂无数据。
- [ ] B 区已经确定首批主项目与暂不展示的项目。
- [ ] 所有拟公开的关键表述均有个人确认或现有材料支持。
- [ ] 团队成果与个人贡献可以清楚区分。
- [ ] 没有把未测量结果、未完成原型或受限材料写成公开成果。

C、D 区不阻塞进入 P1，可在项目文案和素材准备阶段逐步完成。
