# The Art of Thinking Clearly — 场景式认知偏误路由

> 来源: 《The Art of Thinking Clearly》— Rolf Dobelli (2013)
> 路由方式: **场景语义匹配** — 将用户的问题情景与 99 个偏误的 400+ 个具体场景进行匹配
> 偏误总数: 99 | 场景总数: 400+

---

## 路由算法 (MUST FOLLOW)

```
1. 阅读用户描述的问题/情景
2. 扫描所有偏误文件中的 scenarios 列表
3. 用语义理解找出与用户情景最匹配的 3 个偏误
   匹配依据: 偏误的 scenarios 描述的情景与用户描述的相似度
4. 输出 3 个偏误，必须列出匹配到的具体场景来说明为什么选它们

不依赖关键词 — 依赖情景的语义相似度。
```

**关键原则:**
- 每次选出恰好 3 个偏误
- 必须引用匹配到的具体场景（"你的情况与 X 偏误的第 2 个场景高度吻合：..."）
- 如果用户的情景和多个偏误都部分相关，选最核心的 3 个

---

## 情景域索引

以下按生活领域整理了最常见的思维偏误触发情景。当用户描述问题时，对照此表定位最可能的偏误。

### 投资与金钱

| 你的情景 | 最可能的偏误 |
|---|---|
| 股票跌了很多不舍得卖 | sunk-cost-fallacy, loss-aversion |
| 看到别人炒股/炒币赚了钱也想入场 | survivorship-bias, social-proof |
| 频繁查看行情、忍不住操作 | action-bias, information-bias |
| 赢了一笔钱后变得更大胆 | house-money-effect, overconfidence-effect |
| 觉得自己能预测市场走势 | forecast-illusion, illusion-of-control |
| 中了彩票/奖金后生活并没有更快乐 | hedonic-treadmill |
| 买了某个"专家推荐"的理财产品结果亏损 | authority-bias, outcome-bias |
| 用过去的价格作为买卖的参考点 | anchoring |
| 连续亏了几次后觉得"下次一定翻盘" | gamblers-fallacy |

### 工作与职业

| 你的情景 | 最可能的偏误 |
|---|---|
| 在一次会议上没人敢提反对意见 | groupthink, social-proof |
| 老板提了一个明显有问题的方案但没人说 | authority-bias, groupthink |
| 项目已经明显不行了但团队还在继续投入 | sunk-cost-fallacy, action-bias |
| 把成功归功于自己的能力，把失败归咎于外部因素 | self-serving-bias |
| 面试时因为候选人长得好看/名校毕业就给了高分 | halo-effect, swimmers-body-illusion |
| 团队里有人划水、出工不出力 | social-loafing |
| 觉得自己的方案最好，拒绝外部的建议 | not-invented-here, confirmation-bias |
| 给某个任务预估的时间总是不够用 | planning-fallacy, overconfidence-effect |
| 每天做太多决策到下午就判断力下降 | decision-fatigue |
| KPI考核后员工只做能考核的事 | incentive-super-response, motivation-crowding |
| 认为复杂的问题一定只有一个原因 | fallacy-of-single-cause |

### 消费与购物

| 你的情景 | 最可能的偏误 |
|---|---|
| 因为"限时优惠"买了不需要的东西 | scarcity-error, fear-of-regret |
| 看了一个贵的东西后再看便宜的觉得都很划算 | contrast-effect, anchoring |
| 办了健身卡后从来不去但也不取消 | sunk-cost-fallacy, default-effect |
| 买了某样东西后总觉得它特别好 | endowment-effect, cognitive-dissonance |
| "加 30 元升级大杯"让你多花了很多钱 | framing, contrast-effect |
| 朋友推荐的产品你更愿意买 | liking-bias, social-proof |
| 收到免费赠品后不好意思不买点什么 | reciprocity |
| 看到"仅剩 3 件"就赶紧下单 | scarcity-error |

### 人际关系

| 你的情景 | 最可能的偏误 |
|---|---|
| 讨厌一个人就觉得他做什么都是错的 | halo-effect, confirmation-bias |
| 朋友帮了你一个忙后总想找机会还回去 | reciprocity |
| 觉得自己的朋友/圈子就是大多数人的样子 | false-consensus-effect |
| 对不同圈子的人态度完全不同 | in-group-out-group |
| 新认识的人给你的第一印象影响了你对他的所有判断 | primacy-recency, halo-effect |
| 总觉得别人过得比自己好 | social-comparison-bias, envy |
| 别人犯了错你就觉得是他这个人有问题，自己犯错就是环境所迫 | fundamental-attribution-error, self-serving-bias |

### 学习与自我提升

| 你的情景 | 最可能的偏误 |
|---|---|
| 学了很多"干货"但实际什么都没改变 | information-bias, action-bias |
| 花了很多钱和时间读了一个不值当的学位/课程 | sunk-cost-fallacy, effort-justification |
| 总觉得自己不如别人、配不上当前的成就 | impostor-syndrome（冒名顶替综合征，未直接收录,但 related） |
| 看到某个技能很火就想学，学了一半又换别的 | neomania, inability-to-close-doors |
| 做了个性格测试觉得"说得好准" | forer-effect |
| 觉得自己已经懂了，实际只是皮毛 | chauffeur-knowledge, overconfidence-effect |
| 总想等到"准备好了"再开始，一拖再拖 | procrastination, overthinking |
| 过了很久还没完成的待办事项总是萦绕心头 | zeigarnik-effect |

### 决策与判断

| 你的情景 | 最可能的偏误 |
|---|---|
| 在两个选项间反复横跳、做不了决定 | paradox-of-choice, overthinking |
| 做了一个决定后不断给自己找理由证明是对的 | cognitive-dissonance, confirmation-bias |
| 用结果的好坏来评判当时的决策质量 | outcome-bias, hindsight-bias |
| 听到一个好故事就被说服了，忽略了统计数据 | story-bias, personification |
| 同样的信息，换一种说法就让你做出完全不同决定 | framing |
| 宁可什么都不做，也不愿做一个可能有坏结果的决定 | omission-bias, ambiguity-aversion |
| 相信"先苦后甜"而忍受了一个持续恶化的局面 | itll-get-worse-before-it-gets-better |
| 对一个复杂问题只找一个简单原因 | fallacy-of-single-cause |
| "因为"有了一个理由（哪怕很牵强）就觉得合理了 | because-justification |

### 信息与新闻

| 你的情景 | 最可能的偏误 |
|---|---|
| 每天刷大量新闻但回头想想什么都没记住 | news-illusion, information-bias |
| 因为最近的新闻/事件改变了长期决策 | availability-bias, recency-effect |
| 只关注符合自己已有观点的信息来源 | confirmation-bias-2 |
| 看到关于人工智能的报道就觉得自己要被淘汰了 | availability-bias, salience-effect |
| 被一个煽情的故事打动后忽略了理性分析 | affect-heuristic, story-bias |
| 看到数据图表就深信不疑，不去想数据来源 | information-bias, cherry-picking |
| 忽略"什么事情没发生"（只看发生的） | feature-positive-effect, survivorship-bias |

---

## 完整偏误列表（附示例场景）

以下列出所有 99 个偏误，各附一个典型场景，帮助快速匹配。

| # | 偏误 | 典型场景 |
|---|---|---|
| 1 | survivorship-bias | 看到成功故事就想复制，忽略了失败的大多数 |
| 2 | swimmers-body-illusion | 以为上了名校就能变优秀，其实是名校选了优秀的人 |
| 3 | clustering-illusion | 在股票的随机波动中看到了"规律" |
| 4 | social-proof | 看到大家都在抢购，自己也跟着下单 |
| 5 | sunk-cost-fallacy | 烂片看到一半，不舍得票钱硬撑到最后 |
| 6 | reciprocity | 收到免费赠品后不好意思不掏钱 |
| 7 | confirmation-bias-1 | 认定某观点后只找支持证据，无视反面 |
| 8 | confirmation-bias-2 | 只关注符合自己立场的媒体和公众号 |
| 9 | authority-bias | 专家说什么就信什么，不自己思考 |
| 10 | contrast-effect | 先看贵的再看不贵的，就觉得便宜很划算 |
| 11 | availability-bias | 最近飞机失事的新闻让你不敢坐飞机 |
| 12 | itll-get-worse... | 相信"黎明前的黑暗"而忍受持续恶化的项目 |
| 13 | story-bias | 被一个好故事打动，忽略了统计数据 |
| 14 | hindsight-bias | 事后觉得"我早知道会这样" |
| 15 | overconfidence-effect | 对自己预测的准确性过于自信 |
| 16 | chauffeur-knowledge | 能复述专家的观点但实际并不真正理解 |
| 17 | illusion-of-control | 觉得自己掷骰子的方式能影响结果 |
| 18 | incentive-super-response | 按小时计费的律师倾向于把案子拖得更久 |
| 19 | regression-to-mean | 极端表现后必然回归正常，却以为是你的干预起了作用 |
| 20 | outcome-bias | 根据结果好坏批评决策，不看去时的信息 |
| 21 | paradox-of-choice | 选项越多越焦虑，最后什么都不选 |
| 22 | liking-bias | 销售人员长得好看/亲切，你更容易下单 |
| 23 | endowment-effect | 自己的东西总觉得比别人的值钱 |
| 24 | coincidence | 把随机事件当成了不起的巧合 |
| 25 | groupthink | 会上没人反对，不代表大家都同意 |
| 26 | neglect-of-probability | 买彩票时只想着中奖，不去看中奖概率 |
| 27 | scarcity-error | "仅剩 3 件"让你赶紧下单 |
| 28 | base-rate-neglect | 听到马蹄声就觉得是斑马，忘了常见的是马 |
| 29 | gamblers-fallacy | 连开了 5 次"大"，觉得下次一定开"小" |
| 30 | anchoring | 商家标一个高价"原价"，让你觉得折后很值 |
| 31 | induction | 因为过去 10 年房价都在涨，认为明年也会涨 |
| 32 | loss-aversion | 亏 100 元的痛苦远大于赚 100 元的快乐 |
| 33 | social-loafing | 团队任务中有人躲在后排不出力 |
| 34 | exponential-growth | 低估了复利或者指数增长的威力 |
| 35 | winners-curse | 拍卖中出价最高的人往往付了最多的冤枉钱 |
| 36 | fundamental-attribution-error | 别人迟到是他懒，自己迟到是路上堵车 |
| 37 | false-causality | 发现冰激凌销量和溺水率正相关 |
| 38 | halo-effect | 长得好看的人面试更容易拿高分 |
| 39 | alternative-paths | 侥幸成功后，不去想万一当时走岔了会怎样 |
| 40 | forecast-illusion | 相信"专家"对明年经济的预测 |
| 41 | conjunction-fallacy | 觉得"银行出纳+女权主义者"比"银行出纳"更可能 |
| 42 | framing | "成功率 90%"和"失败率 10%"让人做出不同选择 |
| 43 | action-bias | 股票跌了就忍不住操作，哪怕不动更好 |
| 44 | omission-bias | 宁愿不作为也不愿做可能有风险的决定 |
| 45 | self-serving-bias | 成功是自己的功劳，失败是环境的错 |
| 46 | hedonic-treadmill | 加薪后的幸福感几周后就回到了原点 |
| 47 | self-selection-bias | 网上调查"你幸福吗"的回应者大多是极端的人 |
| 48 | association-bias | 广告把产品和美好的画面联系在一起让你产生好感 |
| 49 | beginners-luck | 第一次打牌赢了，以为自己是天才 |
| 50 | cognitive-dissonance | 买了一件贵但不好用的东西后找理由说服自己买得值 |
| 51 | hyperbolic-discounting | 今天给你 100 和明天给你 110，你选了今天的 100 |
| 52 | because-justification | 插队时说"因为我要复印"就更容易被允许 |
| 53 | decision-fatigue | 做了太多决定后变得暴躁、判断力下降 |
| 54 | contagion-bias | 不愿意穿"希特勒穿过的毛衣" |
| 55 | problem-with-averages | "平均水深一米"的河也能淹死人 |
| 56 | motivation-crowding | 用奖金奖励志愿行为反而让人失去内在动力 |
| 57 | twaddle-tendency | 会议中有人滔滔不绝但什么都没说 |
| 58 | will-rogers-phenomenon | 把一个人移出A组后两组平均都提高了 |
| 59 | information-bias | 以为掌握更多信息就能做更好的决策 |
| 60 | effort-justification | 一个很难加入的社团你觉得特别有价值 |
| 61 | law-of-small-numbers | 两个朋友都说某个餐厅好，你就认定它真的很好 |
| 62 | expectations | 你相信这药有效，吃完真的感觉好多了 |
| 63 | simple-logic | 直觉上对的答案被仔细推理推翻 |
| 64 | forer-effect | 星座描述中看到了"自己" |
| 65 | volunteers-folly | 做义工的实际价值可能不如直接捐钱 |
| 66 | affect-heuristic | 因为喜欢某明星所以觉得他代言的产品也好 |
| 67 | introspection-illusion | 以为自己很了解自己，其实并不 |
| 68 | inability-to-close-doors | 舍不得放弃任何一个选项，结果每个都做不好 |
| 69 | neomania | 每次手机出新款就觉得自己的旧手机"变慢了" |
| 70 | sleeper-effect | 忘了信息来源后，虚假信息反而被当成真的 |
| 71 | alternative-blindness | 在两个都不好的选项中纠结，没看到第三条路 |
| 72 | social-comparison-bias | 总是跟比自己强的人比，觉得自己一事无成 |
| 73 | primacy-recency | 面试第一个和最后一个候选人的印象最深刻 |
| 74 | not-invented-here | 拒绝用别人开发的方案，非要自己重新做 |
| 75 | black-swan | 911 之前谁也想不到飞机能撞大楼 |
| 76 | domain-dependence | 你在工作中学到的谈判技巧，回家跟伴侣却用不上 |
| 77 | false-consensus-effect | 以为大多数人都同意你的政治观点 |
| 78 | falsification-of-history | 回忆过去时自动美化了自己的选择和表现 |
| 79 | in-group-out-group | 对"自己人"宽容，对"外人"苛刻 |
| 80 | ambiguity-aversion | 在两个选项中选了风险"已知"的那个，尽管另一可能更好 |
| 81 | default-effect | 从不改手机的默认设置，包括默认铃声 |
| 82 | fear-of-regret | "最后三天"的促销让你不敢不买 |
| 83 | salience-effect | 一个醒目的特征让你忽略了其他更重要的问题 |
| 84 | house-money-effect | 赢了 500 块后下注变得更随意 |
| 85 | procrastination | 新年计划坚持不了一周 |
| 86 | envy | 看到同学买了新房，心里不是滋味 |
| 87 | personification | 一个具体孩子的故事比"百万儿童饿死"更能打动你 |
| 88 | illusion-of-attention | 专注数传球次数时完全没看到穿大猩猩服的人走过 |
| 89 | strategic-misrepresentation | 投标时故意低估成本和时间以中标 |
| 90 | overthinking | 为午餐吃什么纠结了半小时 |
| 91 | planning-fallacy | 想着"这次装修两个月搞定"，结果拖了一年 |
| 92 | deformation-professionnelle | 外科医生觉得所有病都可以用手术解决 |
| 93 | zeigarnik-effect | 没完成的任务总是占据你的大脑后台 |
| 94 | illusion-of-skill | 基金经理的成功大部分靠运气而非能力 |
| 95 | feature-positive-effect | 检查清单只关注"做了什么"，不关注"没做什么" |
| 96 | cherry-picking | 只展示支持自己结论的数据，隐藏不利数据 |
| 97 | fallacy-of-single-cause | "公司业绩不好，都怪 CEO" |
| 98 | intention-to-treat-error | 忽略中途退出实验的受试者，得出错误的结论 |
| 99 | news-illusion | 刷了一小时新闻后感觉自己"掌握了世界"，实际什么都没留下 |
