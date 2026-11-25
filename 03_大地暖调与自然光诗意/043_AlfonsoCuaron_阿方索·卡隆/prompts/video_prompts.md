# 视频提示词 — 阿方索·卡隆 Alfonso Cuarón 风格

> **一个文件，四套规则。你用哪个模型，就用哪一段。**
> 编号 `043` ｜ 分类 03 大地暖调与自然光诗意 ｜ 国籍 墨西哥

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
长镜头沉浸于记忆与宇宙之间，暖金色的回忆柔光与黑白纪实的冷峻诗意在银幕上彼此呼应。配色：主色 暖金回忆 `#D4A574` 占 22%，辅色 土黄街景 `#B89968` 占 18%、深空黑 `#2C2C2C` 占 15%、冷钢蓝灰 `#6B8E9A` 占 15%，点缀 橄榄棕 `#8B7355` 占 15%、柔光米白 `#E8D5B7` 占 15%。让主色占主导，其余按比例递减。光线：主光：natural available light, long take continuous lighting, soft window bounce；高光偏 warm gold / amber memory；阴影偏 cool steel blue / warm umber；对比度：medium 50-65%，依场景跨度极大；整体：warm memory + cold reality, 60% warm + 40% cool。运镜与构图：long take immersion、zero-gravity fluid camera、wide-angle depth、handheld documentary、child's eye low angle、360-degree spatial camera、natural framing、silent long shot。色彩与光影：warm golden memory tones、black and white stark realism、cool steel blue space、earth brown post-apocalypse、soft morning light、dust motes in sunbeam、rain-washed street、fire in darkness。氛围与情绪：memory and longing、isolation in vastness、childhood innocence lost、human connection、gravity and weightlessness、political urgency、poetic realism、quiet resilience。
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
[总控] 30 秒 ｜ 竖版 9:16 ｜ 长镜头沉浸于记忆与宇宙之间，暖金色的回忆柔光与黑白纪实的冷峻诗意在银幕上彼此呼应。 ｜ 单主角 ｜ 有对白 / 无对白
[参考素材职责] 见 2.2，只留这次真正用到的

[0–4 秒 镜头 S01]《罗马》·街区日常：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[4–9 秒 镜头 S02]《地心引力》·太空漂流：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[9–16 秒 镜头 S03]《人类之子》·末世街道：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[16–30 秒 镜头 S04]《阿兹卡班》·魔法校园：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。

[声音] 环境声：（照场景补）／对白：<写准确台词，不要写「说点什么」>／配乐：（不想要就写「无配乐」）

[场景特定限制] 炫彩 LUT，切碎长动作，不连续曝光，无动机环绕和随机变焦，用统一滤镜替代色彩比例，光源和材质。
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

#### 镜头 1：罗马 · 街区日常

```text
【运镜】长镜头沉浸（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在街区日常里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《罗马》的街区日常；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】长镜头沉浸于记忆与宇宙之间，暖金色的回忆柔光与黑白纪实的冷峻诗意在银幕上彼此呼应。配色：主色 暖金回忆 `#D4A574` 占 22%，辅色 土黄街景 `#B89968` 占 18%、深空黑 `#2C2C2C` 占 15%、冷钢蓝灰 `#6B8E9A` 占 15%，点缀 橄榄棕 `#8B7355` 占 15%、柔光米白 `#E8D5B7` 占 15%。让主色占主导，其余按比例递减。光线：主光：natural available light, long take continuous lighting, soft window bounce；高光偏 warm gold / amber memory；阴影偏 cool steel blue / warm umber；对比度：medium 50-65%，依场景跨度极大；整体：warm memory + cold reality, 60% warm + 40% cool。运镜与构图：long take immersion、zero-gravity fluid camera、wide-angle depth、handheld documentary、child's eye low angle、360-degree spatial camera、natural framing、silent long shot。色彩与光影：warm golden memory tones、black and white stark realism、cool steel blue space、earth brown post-apocalypse、soft morning light、dust motes in sunbeam、rain-washed street、fire in darkness。氛围与情绪：memory and longing、isolation in vastness、childhood innocence lost、human connection、gravity and weightlessness、political urgency、poetic realism、quiet resilience。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 2：地心引力 · 太空漂流

```text
【运镜】零重力摄影（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在太空漂流里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《地心引力》的太空漂流；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】长镜头沉浸于记忆与宇宙之间，暖金色的回忆柔光与黑白纪实的冷峻诗意在银幕上彼此呼应。配色：主色 暖金回忆 `#D4A574` 占 22%，辅色 土黄街景 `#B89968` 占 18%、深空黑 `#2C2C2C` 占 15%、冷钢蓝灰 `#6B8E9A` 占 15%，点缀 橄榄棕 `#8B7355` 占 15%、柔光米白 `#E8D5B7` 占 15%。让主色占主导，其余按比例递减。光线：主光：natural available light, long take continuous lighting, soft window bounce；高光偏 warm gold / amber memory；阴影偏 cool steel blue / warm umber；对比度：medium 50-65%，依场景跨度极大；整体：warm memory + cold reality, 60% warm + 40% cool。运镜与构图：long take immersion、zero-gravity fluid camera、wide-angle depth、handheld documentary、child's eye low angle、360-degree spatial camera、natural framing、silent long shot。色彩与光影：warm golden memory tones、black and white stark realism、cool steel blue space、earth brown post-apocalypse、soft morning light、dust motes in sunbeam、rain-washed street、fire in darkness。氛围与情绪：memory and longing、isolation in vastness、childhood innocence lost、human connection、gravity and weightlessness、political urgency、poetic realism、quiet resilience。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 3：人类之子 · 末世街道

```text
【运镜】儿童视角（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在末世街道里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《人类之子》的末世街道；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】长镜头沉浸于记忆与宇宙之间，暖金色的回忆柔光与黑白纪实的冷峻诗意在银幕上彼此呼应。配色：主色 暖金回忆 `#D4A574` 占 22%，辅色 土黄街景 `#B89968` 占 18%、深空黑 `#2C2C2C` 占 15%、冷钢蓝灰 `#6B8E9A` 占 15%，点缀 橄榄棕 `#8B7355` 占 15%、柔光米白 `#E8D5B7` 占 15%。让主色占主导，其余按比例递减。光线：主光：natural available light, long take continuous lighting, soft window bounce；高光偏 warm gold / amber memory；阴影偏 cool steel blue / warm umber；对比度：medium 50-65%，依场景跨度极大；整体：warm memory + cold reality, 60% warm + 40% cool。运镜与构图：long take immersion、zero-gravity fluid camera、wide-angle depth、handheld documentary、child's eye low angle、360-degree spatial camera、natural framing、silent long shot。色彩与光影：warm golden memory tones、black and white stark realism、cool steel blue space、earth brown post-apocalypse、soft morning light、dust motes in sunbeam、rain-washed street、fire in darkness。氛围与情绪：memory and longing、isolation in vastness、childhood innocence lost、human connection、gravity and weightlessness、political urgency、poetic realism、quiet resilience。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```


### 3.2 本导演可用的运镜（挑一个，别叠加）

- **长镜头沉浸** —— 超长镜头制造沉浸式体验（例：《人类之子》车内长镜头）
- **零重力摄影** —— 模拟失重状态的流畅运动（例：《地心引力》太空漫游）
- **儿童视角** —— 低角度从儿童高度看世界（例：《罗马》童年视角）
- **手持纪实** —— 手持带来纪录片质感（例：《罗马》黑白街景）
- **空间调度** —— 360 度探索画面空间（例：《地心引力》空间站）
- **自然画框** —— 门窗、车厢、头盔画框（例：《人类之子》车窗）

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
画面抖动，多余肢体，手指畸形，面部漂移，文字水印，物体变形，闪烁跳帧，重复物体，光线杂乱，炫彩 LUT，切碎长动作，不连续曝光，无动机环绕和随机变焦，用统一滤镜替代色彩比例，光源和材质。
```

---

## 四、MiniMax H3（海螺）

H3 按时间戳写，不分镜头。**声音要单独成段**。

```text
【核心创意】长镜头沉浸于记忆与宇宙之间，暖金色的回忆柔光与黑白纪实的冷峻诗意在银幕上彼此呼应。
［主体］在街区日常。

【分段过程描述】
[0–4s] 开场：罗马 式空间。［主体动作：缓慢抬手 / 微微低头 / 顺势坐下，写清幅度和速度］。
[4–8s] 中段：［主体动作承接上一拍，写惯性衔接］。
[8–12s] 收尾：［主体停住，画面定格在 暖金回忆+土黄街景 的调子上］。

【声音】
overall_soundscape：（环境声 + 物理声 + 有无对白）
non_diegetic_music：（配乐；不想要就写「无配乐」）

【结束状态】画面收在［想要的那一帧］。
```

> 提示词上限约 **7000 字符**，写长不是问题，**糊成一段不分层才是**。

---

## 五、Runway / Pika

# 视频提示词模板 — 阿方索·卡隆 Alfonso Cuarón 风格

---

## 镜头脚本
| 镜头 | 运镜 |
|------|------|
| 镜头1 | 长镜头跟随人物穿过街道，手持微晃，自然光变化 |
| 镜头2 | 零重力漂浮摄影，360度环绕人物，空间纵深 |
| 镜头3 | 儿童视角低角度跟拍，世界显得高大而神秘 |
| 镜头4 | 车内长镜头，摄影机在车内自由移动，空间被打破 |
| 镜头5 | 缓慢推进的静默长镜，从环境细节到人物情绪 |
| 镜头6 | 雨天街道跟拍，雨丝和水珠在镜头前掠过 |

## 运镜关键词
long take immersion, zero-gravity fluid camera, wide-angle depth, handheld documentary, child's eye low angle, 360-degree spatial camera, natural framing, silent long shot

## 色彩关键词
warm golden memory tones, black and white stark realism, cool steel blue space, earth brown post-apocalypse, soft morning light, dust motes in sunbeam, rain-washed street, fire in darkness

## 视频公式
```
An Alfonso Cuarón inspired cinematic scene,
long take immersive continuous camera movement,
warm golden memory color palette with cool steel blue accents,
natural available light, fluid spatial camera work,
poetic realism and human connection,
35mm film grain, anamorphic lens, 16:9 cinematic
```

## 负面描述
fast editing cuts, static tripod shots, neon saturated lighting,
cartoon or anime style, flat shallow composition

---

> 本文件由 `色卡主文档.md` 派生（运镜特征表 / 经典场景表 / 色板 / 光影），未新增事实。
> Seedance 2.5 段的结构规则来自本机技能库 `film-cinedance/references/seedance-25-prompt-format.md`。
> 图像提示词见 `midjourney_prompts.md` · `conversational_prompts.md`。
