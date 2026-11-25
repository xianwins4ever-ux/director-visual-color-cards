# 视频提示词 — 巴里·詹金斯 Barry Jenkins 风格

> **一个文件，四套规则。你用哪个模型，就用哪一段。**
> 编号 `046` ｜ 分类 03 大地暖调与自然光诗意 ｜ 国籍 美国

---

## 〇、你用哪个模型，就用哪一段

| 你用什么 | 用哪段 |
|---|---|
| **Seedance 2.5**（火山方舟 / 即梦） | **§二** ← 现在最主流，优先用它 |
| **Seedance 2.0**（火山方舟 / 即梦） | **§三** |
| **MiniMax H3**（海螺 Hailuo 3） | **§四** |
| **Runway / Pika** | **§五** |

### 四套规则差在哪

| | **Seedance 2.5** | **Seedance 2.0** | **MiniMax H3** |
|---|---|---|---|
| 组织方式 | **总控 → 参考素材职责 → 首帧完整状态 → 连续时间轴 → 场景限定** | 一个镜头一件事，按四段写 | **参考素材说明 ＋ 核心创意 ＋ 分段过程描述** |
| 时间写法 | **时间戳连续段落**，可多镜头长叙事 | 精确时间戳支持不稳定，别硬写 | **按时间戳分段** |
| 运镜 | 每镜一种主导运镜 | **一个镜头只写 1 种** | 同，一种主导运镜 |
| 动作 | 抽象情绪要转成可观察的面部/呼吸/重心/肢体 | **肢体细化 ＋ 程度量化** | 拆 2–3 个节拍，写清因果 |
| 参考图 | **最多 30 图 / 10 视频 / 10 音频，共 50 个素材，每个写唯一职责** | 可垫图 | 参考素材就地声明角色 |
| 时长 | **单次最长 30 秒**，可续写延长 | 不支持长叙事 | 4–15 秒（整数秒） |
| 声音 | 总控里声明方式 | 可写音频信息 | **原生立体声同生**，必须写 `overall_soundscape` |
| 负面词 | **只写场景特定限制**，不堆通用负面词 | **不是可选项**，一定要给 | 尽量正向表达 |

---

## 一、风格锚（四套都要先贴这段）

```text
饱和温暖的肤色在蓝紫暮光中呼吸，城市诗意里黑人的生命与爱情被光温柔地捧起。配色：主色 暖金褐肤 `#C68642` 占 22%，辅色 暮光紫蓝 `#3A2E5F` 占 20%、深棕暖肤 `#8B5A2B` 占 15%、阳光金棕 `#D4A574` 占 15%，点缀 墨绿青蓝 `#2E5E4E` 占 14%、暖沙金 `#E8C99B` 占 14%。让主色占主导，其余按比例递减。光线：主光：soft warm key with color fill, practical neon/tungsten, natural window light；高光偏 warm gold / orange sunset；阴影偏 deep purple-blue / teal green；对比度：medium-high 60-75%，肤色始终暖调；整体：warm skin + cool purple/teal environment, 55% warm + 45% cool。运镜与构图：slow push-in intimacy、centered portrait、circular camera movement、soft shallow focus、negative space loneliness、streetlamp silhouette、tender close-up、mirror/glass reflection。色彩与光影：saturated warm brown skin、twilight purple-blue、teal pool water、golden hour beach、warm tungsten streetlight、deep blue night、orange sunset haze、yellow memory glow。氛围与情绪：tender black masculinity、queer love and longing、urban poetry、childhood memory、racial injustice、gentle intimacy、dreamlike memory、resilience and hope。
```

---

## 二、Seedance 2.5

> 单次最长 **30 秒**，可续写延长。单次最多 **30 张图 + 10 段视频 + 10 段音频**（合计 50 个素材）。
> 支持多镜头长叙事、参考视频、白模控制、绿幕、时间戳控制、局部编辑。

### 2.1 官方五段结构（缺一段就不完整）

```text
[总控]         时长、画幅、风格、角色数、声音方式
[参考素材职责]  只列这次真正用到的素材
[首帧完整状态]  人物／位置／朝向／姿势／道具／场景／光源／轴线
[连续时间轴]    每段：动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机 ＋ 结束状态
[场景特定限制]  只写这一场要注意的，不堆通用负面词
```

### 2.2 先传「影调色卡」

本导演的影调色卡就在本包：

```text
assets/color_palettes/影调色卡.jpg
```

把它当参考图传上去，职责**只写「影调与光色」**——不要让它决定构图、机位和人物。

参考素材职责表照这个格式填，**没用到的不写**：

```text
素材 | 类型 | 唯一职责 | 必须保留 | 禁止影响
@Image1 | 图片 | 影调与光色 | 主色比例、高光/阴影色偏、对比度 | 构图、机位、人物身份
@Image2 | 图片 | 主角身份与服装 | 脸、发型、服装版本 | 场景构图、运镜
@Image3 | 图片 | 场景空间与材质 | 门窗、桌椅、主光方向 | 人物身份
@Video1 | 视频 | 动作节奏 | 起势、速度、落点 | 角色外貌、故事结果
```

> 一个素材职责冲突时：**要么拆职责，要么改文字写死**，不要指望模型自己分。

### 2.3 30 秒连续段落模板

```text
[总控] 30 秒 ｜ 竖版 9:16 ｜ 饱和温暖的肤色在蓝紫暮光中呼吸，城市诗意里黑人的生命与爱情被光温柔地捧起。 ｜ 单主角 ｜ 有对白 / 无对白
[参考素材职责] 见 2.2，只留这次真正用到的

[0–4 秒 镜头 S01]《月光男孩》·海滩初夜：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[4–9 秒 镜头 S02]《假若比尔街能说话》·哈莱姆街道：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[9–16 秒 镜头 S03]《月光下的布鲁斯男孩》·街角夜晚：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[16–30 秒 镜头 S04]《药剂师》·旧金山漫步：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。

[声音] 环境声：（照场景补）／对白：<写准确台词，不要写「说点什么」>／配乐：（不想要就写「无配乐」）

[场景特定限制] 肤色发灰，全屏紫蓝，商业美颜，无动机环绕和随机变焦，用统一滤镜替代色彩比例，光源和材质。
```

**四条硬规则**

1. 总时长 **≤ 30 秒**
2. 时间段必须**连续、不重叠**，不留无意义空白
3. **切镜时把新机位整段重写**——不能写「同上」「继续」「保持上一镜头」
4. 每个镜头都要有你自己那版的分镜图 / 首帧图，且**文字仍要独立写全物理状态**

### 2.4 写对白之前先算字数

| 情况 | 可用字数（30 秒） |
|---|---|
| 几乎全在说话 | 约 **72–84 个有效汉字** |
| 有动作、呼吸、停顿、听者反应、走位或收尾 | **先扣掉这些时间，再按剩下可说话时间算** |

**装不下就按语义拆段 / 延长 / 删改，禁止加快语速硬塞。**

---

## 三、Seedance 2.0

### 3.1 镜头模板

**每镜头只挑一种运镜**，按官方四段写。下面 3 个镜头都是从本导演的经典场景来的，直接改「［主体动作］」。

#### 镜头 1：月光男孩 · 海滩初夜

```text
【运镜】缓慢推近（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在海滩初夜里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《月光男孩》的海滩初夜；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】饱和温暖的肤色在蓝紫暮光中呼吸，城市诗意里黑人的生命与爱情被光温柔地捧起。配色：主色 暖金褐肤 `#C68642` 占 22%，辅色 暮光紫蓝 `#3A2E5F` 占 20%、深棕暖肤 `#8B5A2B` 占 15%、阳光金棕 `#D4A574` 占 15%，点缀 墨绿青蓝 `#2E5E4E` 占 14%、暖沙金 `#E8C99B` 占 14%。让主色占主导，其余按比例递减。光线：主光：soft warm key with color fill, practical neon/tungsten, natural window light；高光偏 warm gold / orange sunset；阴影偏 deep purple-blue / teal green；对比度：medium-high 60-75%，肤色始终暖调；整体：warm skin + cool purple/teal environment, 55% warm + 45% cool。运镜与构图：slow push-in intimacy、centered portrait、circular camera movement、soft shallow focus、negative space loneliness、streetlamp silhouette、tender close-up、mirror/glass reflection。色彩与光影：saturated warm brown skin、twilight purple-blue、teal pool water、golden hour beach、warm tungsten streetlight、deep blue night、orange sunset haze、yellow memory glow。氛围与情绪：tender black masculinity、queer love and longing、urban poetry、childhood memory、racial injustice、gentle intimacy、dreamlike memory、resilience and hope。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 2：假若比尔街能说话 · 哈莱姆街道

```text
【运镜】居中肖像（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在哈莱姆街道里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《假若比尔街能说话》的哈莱姆街道；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】饱和温暖的肤色在蓝紫暮光中呼吸，城市诗意里黑人的生命与爱情被光温柔地捧起。配色：主色 暖金褐肤 `#C68642` 占 22%，辅色 暮光紫蓝 `#3A2E5F` 占 20%、深棕暖肤 `#8B5A2B` 占 15%、阳光金棕 `#D4A574` 占 15%，点缀 墨绿青蓝 `#2E5E4E` 占 14%、暖沙金 `#E8C99B` 占 14%。让主色占主导，其余按比例递减。光线：主光：soft warm key with color fill, practical neon/tungsten, natural window light；高光偏 warm gold / orange sunset；阴影偏 deep purple-blue / teal green；对比度：medium-high 60-75%，肤色始终暖调；整体：warm skin + cool purple/teal environment, 55% warm + 45% cool。运镜与构图：slow push-in intimacy、centered portrait、circular camera movement、soft shallow focus、negative space loneliness、streetlamp silhouette、tender close-up、mirror/glass reflection。色彩与光影：saturated warm brown skin、twilight purple-blue、teal pool water、golden hour beach、warm tungsten streetlight、deep blue night、orange sunset haze、yellow memory glow。氛围与情绪：tender black masculinity、queer love and longing、urban poetry、childhood memory、racial injustice、gentle intimacy、dreamlike memory、resilience and hope。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 3：月光下的布鲁斯男孩 · 街角夜晚

```text
【运镜】环绕运动（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在街角夜晚里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《月光下的布鲁斯男孩》的街角夜晚；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】饱和温暖的肤色在蓝紫暮光中呼吸，城市诗意里黑人的生命与爱情被光温柔地捧起。配色：主色 暖金褐肤 `#C68642` 占 22%，辅色 暮光紫蓝 `#3A2E5F` 占 20%、深棕暖肤 `#8B5A2B` 占 15%、阳光金棕 `#D4A574` 占 15%，点缀 墨绿青蓝 `#2E5E4E` 占 14%、暖沙金 `#E8C99B` 占 14%。让主色占主导，其余按比例递减。光线：主光：soft warm key with color fill, practical neon/tungsten, natural window light；高光偏 warm gold / orange sunset；阴影偏 deep purple-blue / teal green；对比度：medium-high 60-75%，肤色始终暖调；整体：warm skin + cool purple/teal environment, 55% warm + 45% cool。运镜与构图：slow push-in intimacy、centered portrait、circular camera movement、soft shallow focus、negative space loneliness、streetlamp silhouette、tender close-up、mirror/glass reflection。色彩与光影：saturated warm brown skin、twilight purple-blue、teal pool water、golden hour beach、warm tungsten streetlight、deep blue night、orange sunset haze、yellow memory glow。氛围与情绪：tender black masculinity、queer love and longing、urban poetry、childhood memory、racial injustice、gentle intimacy、dreamlike memory、resilience and hope。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```


### 3.2 本导演可用的运镜（挑一个，别叠加）

- **缓慢推近** —— 温柔推近进入人物内心（例：《月光男孩》奇伦凝视）
- **居中肖像** —— 人物居中直视镜头（例：《月光男孩》三段肖像）
- **环绕运动** —— 摄影机环绕双人舞蹈（例：《假若比尔街能说话》跳舞）
- **浅景深柔焦** —— 柔和散景突出主体（例：《月光男孩》海滩约会）
- **街灯剪影** —— 路灯下人物剪影（例：《月光男孩》街角相遇）
- **镜面倒影** —— 水面/镜面对称构图（例：《月光男孩》泳池水面）

### 3.3 动作怎么写（Seedance 硬要求）

**要写到肢体部位 + 幅度 + 速度 + 力度：**

| ❌ 不合格 | ✅ 合格 |
|---|---|
| 他很悲伤 | 低头，肩膀微微颤抖，手指无意识地攥紧衣角 |
| 她转身 | 缓慢侧身，肩膀先动，视线跟着转过去 |
| 走过去 | 一步一步向前，步伐放慢，重心压低 |

**优先低缓连续的小动作**，规避狂奔、大跳、剧烈翻滚这类高爆发动作。
**补一句动作过渡**（「借着转身的惯性顺势抬手」），画面才连得上。

### 3.4 负面提示词（Seedance 必填）

```text
画面抖动，多余肢体，手指畸形，面部漂移，文字水印，物体变形，闪烁跳帧，重复物体，光线杂乱，肤色发灰，全屏紫蓝，商业美颜，无动机环绕和随机变焦，用统一滤镜替代色彩比例，光源和材质。
```

---

## 四、MiniMax H3（海螺）

H3 按时间戳写，不分镜头。**声音要单独成段**。

```text
【核心创意】饱和温暖的肤色在蓝紫暮光中呼吸，城市诗意里黑人的生命与爱情被光温柔地捧起。
［主体］在海滩初夜。

【分段过程描述】
[0–4s] 开场：月光男孩 式空间。［主体动作：缓慢抬手 / 微微低头 / 顺势坐下，写清幅度和速度］。
[4–8s] 中段：［主体动作承接上一拍，写惯性衔接］。
[8–12s] 收尾：［主体停住，画面定格在 暖金褐肤+暮光紫蓝 的调子上］。

【声音】
overall_soundscape：（环境声 + 物理声 + 有无对白）
non_diegetic_music：（配乐；不想要就写「无配乐」）

【结束状态】画面收在［想要的那一帧］。
```

> 提示词上限约 **7000 字符**，写长不是问题，**糊成一段不分层才是**。

---

## 五、Runway / Pika

# 视频提示词模板 — 巴里·詹金斯 Barry Jenkins 风格

---

## 镜头脚本
| 镜头 | 运镜 |
|------|------|
| 镜头1 | 缓慢推近的居中肖像，暮光紫蓝背景，暖光打在脸上 |
| 镜头2 | 环绕双人运动，街灯暖光晕染，亲密舞蹈 |
| 镜头3 | 海滩黄金时刻，人物逆光剪影，海浪轻拍 |
| 镜头4 | 手持轻晃跟拍，人物穿过夜晚城市街道 |
| 镜头5 | 水面/镜面倒影，叠化梦境般的回忆片段 |
| 镜头6 | 景深很浅的近景，背景虚化成光斑，前景人物低语 |

## 运镜关键词
slow push-in intimacy, centered portrait, circular camera movement, soft shallow focus, negative space loneliness, streetlamp silhouette, tender close-up, mirror/glass reflection

## 色彩关键词
saturated warm brown skin, twilight purple-blue, teal pool water, golden hour beach, warm tungsten streetlight, deep blue night, orange sunset haze, yellow memory glow

## 视频公式
```
A Barry Jenkins inspired cinematic scene,
saturated warm brown skin tones against twilight purple-blue night,
tender intimacy with slow push-in camera movement,
soft shallow depth of field, centered portrait composition,
urban poetry and gentle emotion,
warm golden hour and cool purple night contrast,
35mm film grain, anamorphic lens, 16:9 cinematic
```

## 负面描述
cold flat lighting, desaturated skin tones,
fast MTV editing, harsh action camera,
stereotypical imagery, cartoon or anime style

---

> 本文件由 `色卡主文档.md` 派生（运镜特征表 / 经典场景表 / 色板 / 光影），未新增事实。
> Seedance 2.5 段的结构规则来自本机技能库 `film-cinedance/references/seedance-25-prompt-format.md`。
> 图像提示词见 `midjourney_prompts.md` · `conversational_prompts.md`。
