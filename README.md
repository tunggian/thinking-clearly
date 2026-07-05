# Thinking Clearly — 认知偏误避坑工具箱 🚫🧠

> **99 个认知偏误，让你的 AI 帮你识别思维陷阱。**
>
> 基于 Rolf Dobelli 的《The Art of Thinking Clearly》（清醒思考的艺术，2013）。

## 📖 背景

人脑不是理性的。我们在进化过程中积累了大量的认知捷径（heuristics），这些捷径在原始社会帮助我们存活，但在现代社会却让我们反复掉坑。

读了《清醒思考的艺术》后，我意识到：**如果能把这 99 个偏误变成 AI 可理解的技能文件，当用户描述一个决策困境时，AI 就能立刻识别出——"你正在掉入 XX 偏误的坑"。**

这套 skill 与姊妹项目 **[Super Thinking](https://github.com/tunggian/super-thinking)**（思维模型工具箱）形成了完美互补：

| | Super Thinking | Thinking Clearly |
|---|---|---|
| 侧重 | **给工具** — 遇到问题用什么思维模型分析 | **避坑** — 识别自己是否掉入了认知偏误 |
| 来源 | 《Super Thinking》Gabriel Weinberg | 《The Art of Thinking Clearly》Rolf Dobelli |
| 数量 | 97 个思维模型 | 99 个认知偏误 |
| 回答 | "你应该这样思考" | "你正在犯这个错，这样避免" |

> 💡 **最佳实践**：先用 `/thinking-clearly` 排除认知偏误的干扰，再用 `/super-thinking` 找合适的思维模型来解决问题。

## ✨ 功能

当你在 Claude Code 或其他兼容 AI Agent 中描述一个决策困境、行为困惑、或判断失误时，调用 `/thinking-clearly`，AI 将：

1. 理解你描述的情景
2. 从 **99 个偏误 × 400+ 场景** 中找到最匹配的 **3 个认知偏误**
3. 用 E（如何避免）步骤帮你识别和规避思维陷阱

覆盖的偏误类型：

| 类型 | 数量 | 示例 |
|---|---|---|
| 🎲 概率与统计盲区 | 12 | 幸存者偏差、忽视概率、赌徒谬误 |
| 👥 社会影响偏误 | 10 | 社会认同、权威偏误、内群体偏误 |
| 🪞 自我认知扭曲 | 12 | 过度自信、自利偏误、控制错觉 |
| 🎯 决策陷阱 | 14 | 沉没成本、选择悖论、决策疲劳 |
| 💢 情感驱动偏误 | 8 | 损失厌恶、嫉妒、情感启发式 |
| 📡 信息处理偏误 | 12 | 确认偏误、可得性偏误、框架效应 |
| ⏰ 时间相关偏误 | 8 | 双曲贴现、拖延症、计划谬误 |
| 🔍 归因与解释偏误 | 10 | 基本归因错误、虚假因果 |
| 🌀 其他偏误 | 13 | 光环效应、对比效应、禀赋效应 |

## 🚀 安装

### 前提

- 安装 Claude Code 或其他兼容的 AI Agent 工具
- 确保你的 skills 目录已配置（如 `.agents/skills`、`~/.claude/skills` 或对应工具的 skills 文件夹）

### 方法一：直接安装

```bash
git clone https://github.com/tunggian/thinking-clearly.git
cp -r thinking-clearly ~/.agents/skills/
```

### 方法二：符号链接（便于更新）

```bash
git clone https://github.com/tunggian/thinking-clearly.git ~/thinking-clearly
ln -s ~/thinking-clearly ~/.agents/skills/thinking-clearly
```

### 方法三：直接从 GitHub 安装

```bash
cd ~/.agents/skills
git clone https://github.com/tunggian/thinking-clearly.git
```

### 验证安装

重启 Claude Code，输入 `/thinking-clearly`，应该看到 skill 被加载的提示。

## 💡 使用方法

### 快速启动

```
/thinking-clearly
```

### 提问范例

直接描述你的决策困境或行为困惑：

| 你的情景 | 匹配的偏误 |
|---|---|
| "股票跌了，但我就是不想卖，等回本再说" | sunk-cost-fallacy, loss-aversion, endowment-effect |
| "大家都说这个理财产品好，我就买了" | social-proof, authority-bias, herd-mentality |
| "我觉得我比平均水平开得好" | overconfidence-effect, illusion-of-control, self-serving-bias |
| "买之前觉得这个包超级好看，买回来就没那么喜欢了" | rosy-projection, affect-heuristic, endowment-effect |
| "我做了一个项目成功了，都是我的功劳；失败了，是市场不好" | self-serving-bias, fundamental-attribution-error |

### 回答格式示例

```
根据你描述的情景，我找到 3 个最相关的认知偏误：

**偏误 1: [名称]** — 匹配场景: "[引用具体场景]"
- 为什么你会犯这个错: ...
- 如何避免: ...

**偏误 2: [名称]** — 匹配场景: "[引用具体场景]"
...

**偏误 3: [名称]** — 匹配场景: "[引用具体场景]"
...

**综合建议**: ...
```

### 与 Super Thinking 结合使用

建议工作流：

1. **先 `thinking-clearly`** → 识别自己是否陷入了认知偏误（避免踩坑）
2. **再 `super-thinking`** → 找到合适的思维模型分析问题（找到出路）

## 📁 目录结构

```
thinking-clearly/
├── README.md              # 本文件
├── SKILL.md               # 技能定义（核心工作流 + 触发规则）
├── INDEX.md               # 情景域索引（400+ 场景 → 偏误映射）
├── models/                # 99 个认知偏误文件
│   ├── action-bias.md
│   ├── affect-heuristic.md
│   ├── anchoring.md
│   ├── confirmation-bias-1.md
│   ├── ... (共 99 个)
└── LICENSE                # MIT
```

## 🗺 完整偏误清单

### 🎲 概率与统计盲区（12）

| # | 偏误 | 一句话 |
|---|---|---|
| 1 | Survivorship Bias（幸存者偏差） | 你只看到活下来的，没看到死掉的 |
| 2 | Swimmer's Body Illusion（游泳运动员身材错觉） | 把结果当成了原因 |
| 3 | Clustering Illusion（聚类错觉） | 随机数据中看出了"模式" |
| 4 | Neglect of Probability（忽视概率） | 被"可能"吓到，却不问"多可能" |
| 5 | Gambler's Fallacy（赌徒谬误） | 连续 5 次正面，下一次肯定是反面（其实并不是） |
| 6 | Base Rate Neglect（忽略基础概率） | 这测试准确率 99%，你肯定有病——等等，先看看患病率 |
| 7 | Regression to Mean（均值回归） | 踢得特别好下次肯定差一点，不是退步，是回归 |
| 8 | Coincidence（巧合） | 全世界每天发生几十亿件事，总会有几件"不可思议" |
| 9 | Alternative Paths（替代路径） | 你看结果，没看如果当时选了另一条路会怎样 |
| 10 | Beginner's Luck（新手运气） | 第一次就成功，不是因为天赋 |
| 11 | Black Swan（黑天鹅） | 没人预测到的巨大事件 |
| 12 | Cherry Picking（摘樱桃） | 只选对自己有利的证据 |

### 👥 社会影响偏误（10）

| # | 偏误 | 一句话 |
|---|---|---|
| 13 | Social Proof（社会认同） | 别人都这么做，所以我也这么做 |
| 14 | Authority Bias（权威偏误） | 专家说的就是对的（其实不一定） |
| 15 | Groupthink（群体迷思） | 为了和谐，没人说真话 |
| 16 | In-Group Bias（内群体偏误） | 我们的人总是对的，他们的人总是错的 |
| 17 | Association Bias（关联偏误） | 这个人毕业于名校，所以他一定很厉害 |
| 18 | Halo Effect（光环效应） | 一个人长得好看，你以为他什么都好 |
| 19 | Herd Mentality（羊群效应） | 大家都在跑，你也跟着跑 |
| 20 | Reciprocity（互惠） | 收了礼物就觉得欠他人的 |
| 21 | Contrast Effect（对比效应） | 先看贵的，再看便宜的，就觉得便宜很值 |
| 22 | Spotlight Effect（聚光灯效应） | 你以为全世界都在看你 |

### 🪞 自我认知扭曲（12）

| # | 偏误 | 一句话 |
|---|---|---|
| 23 | Overconfidence Effect（过度自信） | 90% 的司机认为自己的水平高于平均 |
| 24 | Self-Serving Bias（自利偏误） | 成功是我的功劳，失败是别人的问题 |
| 25 | Illusion of Control（控制错觉） | 你觉得自己能控制其实控制不了的事 |
| 26 | Dunning-Kruger Effect（邓宁-克鲁格效应） | 越不懂的人越觉得自己很懂 |
| 27 | Impostor Syndrome（冒名顶替综合征） | 明明很厉害，却觉得自己不配 |
| 28 | Introspection Illusion（内省错觉） | 你以为你很了解自己的动机 |
| 29 | Illusion of Understanding（理解错觉） | 听过就以为自己懂了 |
| 30 | Outcome Bias（结果偏误） | 结果好 = 决策好（其实不一定） |
| 31 | Luck Surface（运气的表面） | 低估了运气在成功中的作用 |
| 32 | It'll Get Worse Before It Gets Better（先坏后好谬误） | 事情还没好转，不是我错了，是还没到时间 |
| 33 | Self-Fulfilling Prophecy（自我实现预言） | 你相信什么，什么就成真 |
| 34 | Winner's Curse（赢家诅咒） | 你赢了竞标，但是你出价过高了 |

### 🎯 决策陷阱（14）

| # | 偏误 | 一句话 |
|---|---|---|
| 35 | Sunk Cost Fallacy（沉没成本谬误） | 已经花了这么多，不能放弃（其实应该放弃） |
| 36 | Paradox of Choice（选择悖论） | 选项越多越不幸福 |
| 37 | Decision Fatigue（决策疲劳） | 做了一天决定后，晚上做的决定都是错的 |
| 38 | Action Bias（行动偏误） | 做点什么总比什么都不做要好（不一定） |
| 39 | Omission Bias（不作为偏误） | 没做导致的坏结果比做了导致的坏结果更容易接受 |
| 40 | Status Quo Bias（现状偏误） | 不想改变，哪怕现状很差 |
| 41 | Default Effect（默认效应） | 默认选项就是最好的选择（被设计的） |
| 42 | Endowment Effect（禀赋效应） | 已经拥有的东西价值更高 |
| 43 | Loss Aversion（损失厌恶） | 丢 100 块的痛苦 > 赚 100 块的快乐 |
| 44 | Zero Risk Bias（零风险偏误） | 愿意花大代价消除最后一丁点风险 |
| 45 | Will Rogers Phenomenon（威尔·罗杰斯现象） | 把 B 组最差的移到 A 组，两组平均都变好了——但整体没变 |
| 46 | Planning Fallacy（计划谬误） | 所有项目都会超出预算和时间 |
| 47 | Procrastination（拖延症） | 今天的痛苦 > 未来的收益 |
| 48 | Hyperbolic Discounting（双曲贴现） | 现在的 100 块 > 一年后的 150 块 |

### 💢 情感驱动偏误（8）

| # | 偏误 | 一句话 |
|---|---|---|
| 49 | Affect Heuristic（情感启发式） | 喜欢就高估优点、低估风险 |
| 50 | Envy（嫉妒） | 关注别人的拥有，忽略自己的满足 |
| 51 | Rosy Projection（玫瑰色投影） | 买之前觉得什么都好，买之后其实没那么好 |
| 52 | Scarcity Error（稀缺谬误） | 最后一件了，快买（管它需不需要） |
| 53 | Zeigarnik Effect（蔡格尼克效应） | 未完成的事一直挂在脑子里 |
| 54 | Need for Closure（需要闭合） | 没有答案比错误的答案更让人难受 |
| 55 | Othello Error（奥赛罗错误） | 觉得对方在撒谎，其实只是紧张 |
| 56 | Liking/Loving（喜欢/爱偏误） | 喜欢一个人，就看不见他的缺点 |

### 📡 信息处理偏误（12）

| # | 偏误 | 一句话 |
|---|---|---|
| 57 | Confirmation Bias（确认偏误） | 只看支持自己观点的信息 |
| 58 | Availability Bias（可得性偏误） | 容易想到的就是最常见的（其实不一定） |
| 59 | Story Bias（故事偏误） | 一个好听的故事胜过一堆枯燥的数据 |
| 60 | Framing（框架效应） | 90% 有效 vs 10% 无效，说法不同效果完全不同 |
| 61 | Anchoring（锚定效应） | 第一个数字锚定了你的判断 |
| 62 | Primacy/Recency Effect（首因/近因效应） | 第一印象和最近印象最重要 |
| 63 | Hindsight Bias（后见之明） | 事后看一切都是"早就知道" |
| 64 | Observer-Expectancy Effect（观察者期望效应） | 你希望看到什么，就看到什么 |
| 65 | False Consensus（虚假共识） | 你以为大多数人跟你想的一样 |
| 66 | Projection Bias（投射偏误） | 用自己的想法去揣测别人 |
| 67 | Curse of Knowledge（知识的诅咒） | 你知道后就很难理解不知道别人的感受 |
| 68 | Blind Spot Bias（盲点偏误） | 我能看出别人的偏误，但看不出自己的 |

### ⏰ 时间相关偏误（8）

| # | 偏误 | 一句话 |
|---|---|---|
| 69 | Discounting the Future（未来贴现） | 未来的收益不如今天的收益值钱 |
| 70 | Present Bias（现时偏误） | 今天的快乐 > 明天的快乐 |
| 71 | Exponential Growth Bias（指数增长盲区） | 低估了复利的力量 |
| 72 | Time Horizon Bias（时间视野偏误） | 短期思维 vs 长期思维 |
| 73 | Peak-End Rule（峰终定律） | 你记住的不是整个过程，是最高潮和结尾 |
| 74 | Duration Neglect（时长忽略） | 经历多长不重要，感受多强才重要 |
| 75 | Memory Bias（记忆偏误） | 记忆不是录像，每次回忆都在改写 |
| 76 | Rosy Retrospection（怀旧偏误） | 过去总是比现在好 |

### 🔍 归因与解释偏误（10）

| # | 偏误 | 一句话 |
|---|---|---|
| 77 | Fundamental Attribution Error（基本归因错误） | 别人迟到是懒，自己迟到是堵车 |
| 78 | Single Cause Fallacy（单一因果谬误） | 一个结果只有一个原因（其实不止） |
| 79 | Causal Fallacy（虚假因果） | 公鸡打鸣后太阳升起，但公鸡没有导致日出 |
| 80 | Conjunction Fallacy（合取谬误） | 琳达是银行出纳 + 女权主义者的概率比是银行出纳高？不合逻辑 |
| 81 | "Because" Justification（"因为"正当化） | 只要说"因为"，别人就更容易答应 |
| 82 | Just-World Hypothesis（公正世界假设） | 世界是公平的，好人好报恶人恶报 |
| 83 | Slippery Slope（滑坡谬误） | 开了一个口子就会滑向深渊（不一定） |
| 84 | Straw Man（稻草人谬误） | 扭曲对方的论点再攻击 |
| 85 | Tautology（同义反复） | 这家公司会成功，因为它的产品好（说了等于没说） |
| 86 | Double Standard（双重标准） | 同样的事，自己做可以，别人做不行 |

### 🌀 其他偏误（13）

| # | 偏误 | 一句话 |
|---|---|---|
| 87 | Chauffeur Knowledge（司机知识） | 听起来很专业，其实只是背台词 |
| 88 | Cognitive Dissonance（认知失调） | 做了一件事后，开始说服自己这件事是对的 |
| 89 | Commitment & Consistency（承诺与一致） | 一旦说了就会做到底（哪怕错了） |
| 90 | Foot-in-the-Door（登门坎效应） | 先让你答应一个小请求，再提大请求 |
| 91 | Backfire Effect（逆火效应） | 给你反面证据，你反而更坚信原来的观点 |
| 92 | Third Person Effect（第三人效应） | 媒体影响你，不影响我 |
| 93 | Feature-Positive Effect（特征正效应） | 你能看到的比看不到的更能影响你 |
| 94 | Less-is-Better Effect（少即是好） | 小而精比大而全更好（但不总是） |
| 95 | Peak Shift（峰值位移） | 过度追求某个特征忘了整体 |
| 96 | Google Effect（谷歌效应） | 知道能查到，就不去记了 |
| 97 | Ambiguity Aversion（模糊厌恶） | 确定的损失比不确定的收益更容易接受 |
| 98 | Not-Invented-Here Syndrome（非我发明综合征） | 外部的方案再好也不用 |
| 99 | Alternative Blindness（替代盲区） | 聚焦一个方案，忽略了其他更好的选择 |

## 🧩 技术细节

- 每个偏误文件使用标准化的 **R-I-A1-A2-E-B** 结构
- 通过 **情景语义匹配** 路由：用户描述情景 → 在 400+ 具体场景中匹配最相似的 3 个偏误
- `INDEX.md` 包含 400+ 具体生活场景的语义映射，覆盖投资、工作、消费、人际等 9 大领域
- **深层结构匹配**：不仅看表面关键词，更理解情景的深层逻辑

## 🧠 姊妹项目：Super Thinking

**[Super Thinking](https://github.com/tunggian/super-thinking)** — 97 个核心思维模型工具箱。

| | Thinking Clearly | Super Thinking |
|---|---|---|
| 来源 | 《清醒思考的艺术》Rolf Dobelli | 《Super Thinking》Gabriel Weinberg |
| 数量 | 99 个认知偏误 | 97 个思维模型 |
| 解决的问题 | "我是不是掉进了思维陷阱？" | "我该用什么方法来分析这个问题？" |
| 安装 | `git clone https://github.com/tunggian/thinking-clearly.git` | `git clone https://github.com/tunggian/super-thinking.git` |

**建议工作流**：
1. `/thinking-clearly` — 先检查自己有没有陷入认知偏误
2. `/super-thinking` — 再找合适的思维模型分析问题

## 📜 许可

MIT License

## 🙏 致谢

- **Charlie Munger** — 多元思维模型的倡导者
- **Gabriel Weinberg & Lauren McCann** —《Super Thinking》的作者，系统地整理了 97 个思维模型
- **Rolf Dobelli** —《The Art of Thinking Clearly》作者，翻译为中文《清醒思考的艺术》
- **[book-to-skill](https://github.com/apple-ouyang/book-to-skill)** — 将书籍转化为 AI Agent 可执行 Skill 的开源项目