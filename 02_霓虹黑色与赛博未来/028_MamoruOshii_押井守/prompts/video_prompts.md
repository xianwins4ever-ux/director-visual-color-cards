# 视频提示词 — 押井守 Mamoru Oshii 风格

> **一个文件，四套规则。你用哪个模型，就用哪一段。**
> 编号 `028` ｜ 分类 02 霓虹黑色与赛博未来 ｜ 国籍 日本

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
雨幕笼罩的赛博都市中数据绿流淌，存在主义哲思与冷硬机械美学交织成冷蓝灰调的未来寓言。配色：主色 赛博深黑 `#0D1117` 占 32%，辅色 雨城灰蓝 `#37474F` 占 22%、数据绿 `#00C853` 占 14%、霓虹青 `#00E5FF` 占 12%，点缀 暖肤黄 `#F0D9B5` 占 10%、机械灰 `#607D8B` 占 10%。让主色占主导，其余按比例递减。光线：主光：顶光+侧光为主，雨幕散射光营造湿冷氛围，霓虹招牌作为色彩光源；高光偏数据绿/霓虹青（终端界面/全息投影/霓虹反射）；阴影偏冷蓝灰偏黑（雨城暗部/机械缝隙/建筑阴影）；对比度：中高对比（65-80%），暗部偏冷蓝，高光处有霓虹色溢出；整体：冷调赛博，75% 冷蓝绿灰 + 25% 暖黄肤色/夕照。运镜与构图：雨幕远景、水面倒影、义体镜面反射、城市俯瞰长镜、人偶静止构图、走廊纵深透视、数据雨叠层、鸟类/狗意象空镜、玻璃反射叠影、城市天际线。色彩与光影：数据绿流、雨城冷蓝、霓虹青溢光、湿面反射、机械灰冷调、暖肤对比、夕照金边、全息投影半透、暗色深黑、水面碎光。氛围与情绪：赛博哲学、存在主义、记忆与身份、灵肉二元、冷疏离感、都市孤独、政治隐喻、神学暗喻、静止与等待、人偶凝视。
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
[总控] 30 秒 ｜ 竖版 9:16 ｜ 雨幕笼罩的赛博都市中数据绿流淌，存在主义哲思与冷硬机械美学交织成冷蓝灰调的未来寓言。 ｜ 单主角 ｜ 有对白 / 无对白
[参考素材职责] 见 2.2，只留这次真正用到的

[0–4 秒 镜头 S01]《攻壳机动队》·开篇城市雨景：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[4–9 秒 镜头 S02]《空中杀手》·基地永恒天空：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[9–16 秒 镜头 S03]《人狼》·下水道反乌托邦：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[16–30 秒 镜头 S04]《攻壳机动队2：无罪》·祭典人偶游行：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。

[声音] 环境声：（照场景补）／对白：<写准确台词，不要写「说点什么」>／配乐：（不想要就写「无配乐」）

[场景特定限制] 统一滤镜替代真实材质，无动机环绕和随机变焦，人物身份与空间轴漂移，肤色污染，死黑和爆白，只模仿颜色不执行镜头语言。
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

#### 镜头 1：攻壳机动队 · 开篇城市雨景

```text
【运镜】雨幕长镜（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在开篇城市雨景里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《攻壳机动队》的开篇城市雨景；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】雨幕笼罩的赛博都市中数据绿流淌，存在主义哲思与冷硬机械美学交织成冷蓝灰调的未来寓言。配色：主色 赛博深黑 `#0D1117` 占 32%，辅色 雨城灰蓝 `#37474F` 占 22%、数据绿 `#00C853` 占 14%、霓虹青 `#00E5FF` 占 12%，点缀 暖肤黄 `#F0D9B5` 占 10%、机械灰 `#607D8B` 占 10%。让主色占主导，其余按比例递减。光线：主光：顶光+侧光为主，雨幕散射光营造湿冷氛围，霓虹招牌作为色彩光源；高光偏数据绿/霓虹青（终端界面/全息投影/霓虹反射）；阴影偏冷蓝灰偏黑（雨城暗部/机械缝隙/建筑阴影）；对比度：中高对比（65-80%），暗部偏冷蓝，高光处有霓虹色溢出；整体：冷调赛博，75% 冷蓝绿灰 + 25% 暖黄肤色/夕照。运镜与构图：雨幕远景、水面倒影、义体镜面反射、城市俯瞰长镜、人偶静止构图、走廊纵深透视、数据雨叠层、鸟类/狗意象空镜、玻璃反射叠影、城市天际线。色彩与光影：数据绿流、雨城冷蓝、霓虹青溢光、湿面反射、机械灰冷调、暖肤对比、夕照金边、全息投影半透、暗色深黑、水面碎光。氛围与情绪：赛博哲学、存在主义、记忆与身份、灵肉二元、冷疏离感、都市孤独、政治隐喻、神学暗喻、静止与等待、人偶凝视。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 2：空中杀手 · 基地永恒天空

```text
【运镜】水面倒影构图（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在基地永恒天空里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《空中杀手》的基地永恒天空；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】雨幕笼罩的赛博都市中数据绿流淌，存在主义哲思与冷硬机械美学交织成冷蓝灰调的未来寓言。配色：主色 赛博深黑 `#0D1117` 占 32%，辅色 雨城灰蓝 `#37474F` 占 22%、数据绿 `#00C853` 占 14%、霓虹青 `#00E5FF` 占 12%，点缀 暖肤黄 `#F0D9B5` 占 10%、机械灰 `#607D8B` 占 10%。让主色占主导，其余按比例递减。光线：主光：顶光+侧光为主，雨幕散射光营造湿冷氛围，霓虹招牌作为色彩光源；高光偏数据绿/霓虹青（终端界面/全息投影/霓虹反射）；阴影偏冷蓝灰偏黑（雨城暗部/机械缝隙/建筑阴影）；对比度：中高对比（65-80%），暗部偏冷蓝，高光处有霓虹色溢出；整体：冷调赛博，75% 冷蓝绿灰 + 25% 暖黄肤色/夕照。运镜与构图：雨幕远景、水面倒影、义体镜面反射、城市俯瞰长镜、人偶静止构图、走廊纵深透视、数据雨叠层、鸟类/狗意象空镜、玻璃反射叠影、城市天际线。色彩与光影：数据绿流、雨城冷蓝、霓虹青溢光、湿面反射、机械灰冷调、暖肤对比、夕照金边、全息投影半透、暗色深黑、水面碎光。氛围与情绪：赛博哲学、存在主义、记忆与身份、灵肉二元、冷疏离感、都市孤独、政治隐喻、神学暗喻、静止与等待、人偶凝视。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 3：人狼 · 下水道反乌托邦

```text
【运镜】俯瞰城市远景（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在下水道反乌托邦里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《人狼》的下水道反乌托邦；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】雨幕笼罩的赛博都市中数据绿流淌，存在主义哲思与冷硬机械美学交织成冷蓝灰调的未来寓言。配色：主色 赛博深黑 `#0D1117` 占 32%，辅色 雨城灰蓝 `#37474F` 占 22%、数据绿 `#00C853` 占 14%、霓虹青 `#00E5FF` 占 12%，点缀 暖肤黄 `#F0D9B5` 占 10%、机械灰 `#607D8B` 占 10%。让主色占主导，其余按比例递减。光线：主光：顶光+侧光为主，雨幕散射光营造湿冷氛围，霓虹招牌作为色彩光源；高光偏数据绿/霓虹青（终端界面/全息投影/霓虹反射）；阴影偏冷蓝灰偏黑（雨城暗部/机械缝隙/建筑阴影）；对比度：中高对比（65-80%），暗部偏冷蓝，高光处有霓虹色溢出；整体：冷调赛博，75% 冷蓝绿灰 + 25% 暖黄肤色/夕照。运镜与构图：雨幕远景、水面倒影、义体镜面反射、城市俯瞰长镜、人偶静止构图、走廊纵深透视、数据雨叠层、鸟类/狗意象空镜、玻璃反射叠影、城市天际线。色彩与光影：数据绿流、雨城冷蓝、霓虹青溢光、湿面反射、机械灰冷调、暖肤对比、夕照金边、全息投影半透、暗色深黑、水面碎光。氛围与情绪：赛博哲学、存在主义、记忆与身份、灵肉二元、冷疏离感、都市孤独、政治隐喻、神学暗喻、静止与等待、人偶凝视。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```


### 3.2 本导演可用的运镜（挑一个，别叠加）

- **雨幕长镜** —— 固定或缓慢移动的长镜，雨丝成为视觉肌理（例：《攻壳机动队》开篇城市雨景）
- **水面倒影构图** —— 城市与人物在积水中的倒影，虚实交错（例：《攻壳机动队》运河追逐戏）
- **俯瞰城市远景** —— 极高角度俯瞰赛博都市，人物渺小（例：《攻壳机动队》新港市全景）
- **人偶静止特写** —— 极度静止的人物特写，义体的非人凝视（例：《攻壳机动队》素子凝视橱窗人偶）
- **走廊纵深推镜** —— 沿走廊/通道缓慢推进，压迫感与仪式感（例：《人狼》反乌托邦巷道）
- **数据叠层画面** —— 数据流/代码/界面叠加在实景上（例：《攻壳机动队》黑客入侵场景）

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
画面抖动，多余肢体，手指畸形，面部漂移，文字水印，物体变形，闪烁跳帧，重复物体，光线杂乱，统一滤镜替代真实材质，无动机环绕和随机变焦，人物身份与空间轴漂移，肤色污染，死黑和爆白，只模仿颜色不执行镜头语言。
```

---

## 四、MiniMax H3（海螺）

H3 按时间戳写，不分镜头。**声音要单独成段**。

```text
【核心创意】雨幕笼罩的赛博都市中数据绿流淌，存在主义哲思与冷硬机械美学交织成冷蓝灰调的未来寓言。
［主体］在开篇城市雨景。

【分段过程描述】
[0–4s] 开场：攻壳机动队 式空间。［主体动作：缓慢抬手 / 微微低头 / 顺势坐下，写清幅度和速度］。
[4–8s] 中段：［主体动作承接上一拍，写惯性衔接］。
[8–12s] 收尾：［主体停住，画面定格在 赛博深黑+数据绿+霓虹青 的调子上］。

【声音】
overall_soundscape：（环境声 + 物理声 + 有无对白）
non_diegetic_music：（配乐；不想要就写「无配乐」）

【结束状态】画面收在［想要的那一帧］。
```

> 提示词上限约 **7000 字符**，写长不是问题，**糊成一段不分层才是**。

---

## 五、Runway / Pika

## 二、场景镜头模板

### 镜头 1：雨城开篇（Establishing Shot）

**提示词：**
```
Slow aerial tracking shot over a vast cyberpunk city at night,
Mamoru Oshii Ghost in the Shell style,
endless dark buildings stretching to the horizon in heavy rain,
neon cyan and data green signs glowing through fog,
raindrops visible in the light beams,
wet rooftops reflecting the neon below,
a single helicopter flies across the distant skyline,
the camera slowly descends toward the street level,
cold blue-grey dominant palette,
contemplative philosophical atmosphere,
90s anime cinematic, film grain,
16:9 aspect ratio, slow and meditative camera movement
```

**镜头参数：**
- 时长：7-9秒
- 运镜：缓慢航拍下降（aerial descend）
- 节奏：极慢，哲思凝视感

---

### 镜头 2：街道行走（Street Walk）

**提示词：**
```
A female cyborg with short purple hair walks alone down a rain-soaked cyberpunk street,
Mamoru Oshii anime style,
heavy rain falls around her, neon cyan signs reflect in deep puddles,
her red jacket is the only warm color in the cold blue-grey scene,
she walks with deliberate slow steps, hands in pockets,
water splashes softly with each step,
the camera follows her from behind at a distance,
data green terminal glow from a nearby window illuminates her face briefly,
wet surfaces mirror the neon above,
philosophical lonely mood, anime film aesthetic,
16:9 aspect ratio, slow following tracking shot
```

**镜头参数：**
- 时长：6-8秒
- 运镜：背面跟随（rear tracking follow）
- 节奏：缓慢，孤独行走感

---

### 镜头 3：水面倒影（Water Reflection）

**提示词：**
```
Dark canal water in a cyberpunk city, perfectly still,
Mamoru Oshii style,
neon-lit buildings reflected on the water surface like a mirror,
data green and neon cyan lights shimmering in the reflection,
raindrops begin to fall creating expanding ripples that distort the reflections,
a small boat with a motionless figure drifts slowly across frame,
the camera is at water level, half-submerged perspective,
distorted neon lights fragment and merge in the ripples,
cold blue-grey night, deeply contemplative,
anime cinematic, film grain, meditative pace,
16:9 or 21:9 aspect ratio, static camera with subtle movement
```

**镜头参数：**
- 时长：6-8秒
- 运镜：水面半潜固定机位（water-level static）
- 节奏：极慢，冥想般的静止

---

### 镜头 4：数据流入侵（Data Stream Hack）

**提示词：**
```
Close-up of a person's face in profile, eyes open staring forward,
Mamoru Oshii cyberpunk style,
data green code streams cascade across the screen and reflect in their eyes,
neon cyan holographic projections float in the foreground,
the green light pulses and intensifies as data flows faster,
mechanical cables and equipment surround them in dark silhouette,
cold blue-grey background,
the camera slowly pushes in toward their face,
their expression remains completely still and emotionless,
digital consciousness awakening,
anime film still, cinematic, green glow intensifying,
16:9 aspect ratio, slow push-in
```

**镜头参数：**
- 时长：5-7秒
- 运镜：缓慢推进（slow push-in）
- 节奏：绿光渐强，数字意识觉醒

---

### 镜头 5：义体战斗（Cyborg Combat）

**提示词：**
```
A female cyborg in combat using thermoptic camouflage in shallow water,
Mamoru Oshii Ghost in the Shell style,
her body becomes semi-transparent with neon cyan outline,
water splashes around her in slow motion,
mechanical grey and cold blue-grey environment,
red alert lights pulse in the background,
rain falls heavily through the scene,
she moves with inhuman speed and precision,
the camera tracks her lateral movement in slow motion,
glass and water surfaces create multiple reflections,
action mixed with philosophical stillness,
anime cinematic, film grain, high contrast,
2.35:1 cinemascope aspect ratio
```

**镜头参数：**
- 时长：5-7秒
- 运镜：慢镜横移（slow-motion lateral track）
- 节奏：慢动作，暴力与静止并存

---

### 镜头 6：城市天际线日落（Sunset Cityscape）

**提示词：**
```
Wide shot of cyberpunk city skyline at sunset,
Mamoru Oshii style,
warm golden sunset light on the far horizon,
contrasting sharply with the cold blue-grey city below,
neon signs are just beginning to flicker on in cyan and green,
birds fly across the frame in formation,
the camera slowly pans across the vast urban landscape,
buildings of incredible height with countless windows,
a single aircraft leaves a contrail across the golden sky,
momentary peace between human warmth and technological cold,
deeply melancholic and philosophical,
anime cinematic beauty, film grain,
16:9 aspect ratio, slow panoramic pan
```

**镜头参数：**
- 时长：6-8秒
- 运镜：缓慢横摇（slow panoramic pan）
- 节奏：极慢，夕照中短暂宁静

---

## 三、运镜关键词速查

| 运镜效果 | 英文关键词 |
|---------|-----------|
| 雨幕长镜头 | long take in rain, static camera with rain, contemplative shot |
| 水面镜像 | water reflection shot, mirror surface, symmetrical reflection |
| 城市俯瞰 | aerial establishing shot, bird's eye view cityscape, top-down |
| 缓慢跟随 | slow tracking follow shot, following from behind, distant follow |
| 人偶凝视推镜 | slow push-in on face, doll-like stillness, static subject |
| 走廊纵深 | dolly down corridor, perspective push-in, depth corridor |
| 数据叠层 | data overlay, holographic UI, digital code streams |
| 空镜静止 | static empty shot, architectural stillness, contemplative insert |

---

## 四、颜色与光影关键词

| 效果 | 英文关键词 |
|------|-----------|
| 数据绿 | data green glow, green terminal light, matrix green code, phosphorescent green |
| 霓虹青 | neon cyan, cyan holographic glow, electric cyan reflection |
| 雨城冷蓝 | cold blue-grey rain, blue-grey overcast, rain-soaked cool tones |
| 湿面反射 | wet asphalt reflection, puddle mirror, rain-slicked surfaces |
| 暖肤对比 | warm skin tone contrast, single warm element in cold scene |
| 夕照金 | sunset gold rim light, warm horizon glow, golden dusk |
| 机械冷调 | mechanical grey, cold metallic surfaces, sterile tech |
| 警报红 | red alert pulsing light, warning beacon, danger indicator |

---

## 五、负面描述（避免的效果）

```
fast-paced action, michael bay explosions,
bright cheerful colors, sunny day, warm lighting,
chibi style, cartoonish, super deformed,
3d cgi look, photorealistic, live action,
comedy tone, slapstick, happy ending feeling,
shaky cam, quick cuts, mtv editing,
fantasy magic, medieval, steampunk elements
```

---

> 本文件由 `色卡主文档.md` 派生（运镜特征表 / 经典场景表 / 色板 / 光影），未新增事实。
> Seedance 2.5 段的结构规则来自本机技能库 `film-cinedance/references/seedance-25-prompt-format.md`。
> 图像提示词见 `midjourney_prompts.md` · `conversational_prompts.md`。
