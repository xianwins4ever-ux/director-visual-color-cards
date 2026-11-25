# 视频提示词 — 麦克蒂尔南 John McTiernan 风格

> **一个文件，四套规则。你用哪个模型，就用哪一段。**
> 编号 `040` ｜ 分类 02 霓虹黑色与赛博未来 ｜ 国籍 美国

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
暗调动作中烟雾弥漫的硬汉剪影，潜艇钢蓝与丛林暗绿交织的硬核战场，爆炸暖橙撕裂烟雾阴影的 80 年代动作巅峰。配色：主色 潜艇钢蓝 `#1E3040` 占 25%，辅色 丛林暗绿 `#1E2E1A` 占 20%、烟雾影黑 `#2A2A2E` 占 20%、爆炸暖橙 `#C45020` 占 15%，点缀 硬汉汗肤 `#9C7860` 占 12%、军事卡其 `#6B6448` 占 8%。让主色占主导，其余按比例递减。光线：主光：硬侧光+烟雾散射光，明暗分明的硬汉布光，实战质感；高光偏暖橙/火光（爆炸、火焰、枪口焰）；阴影偏钢蓝/暗绿（夜战冷蓝+丛林绿暗，烟雾弥漫处呈烟灰）；对比度：高对比（70-88%），烟雾柔化边缘但核心明暗分明；整体：暗调硬核动作，70% 冷钢蓝暗绿烟灰 + 30% 暖橙火光点缀。运镜与构图：经典三幕式构景、低角度硬汉、烟雾弥漫纵深、热成像视角、手持战场感、轨道侧移跟拍、爆炸逆光剪影、封闭式空间压迫、军事地图俯拍、第一人称瞄准。色彩与光影：暗调钢蓝、丛林暗绿、烟雾烟灰、爆炸暖橙、硬汉汗光、军事卡其、热成像红、警灯红蓝、枪口焰、油汗质感。氛围与情绪：硬核硬汉、孤立无援、猫鼠猎杀、军事紧张、黑色幽默、蓝领英雄、80 年代动作、烟雾迷漫、一触即发、原始暴力。
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
[总控] 30 秒 ｜ 竖版 9:16 ｜ 暗调动作中烟雾弥漫的硬汉剪影，潜艇钢蓝与丛林暗绿交织的硬核战场，爆炸暖橙撕裂烟雾阴影的 80 年代动作巅峰。 ｜ 单主角 ｜ 有对白 / 无对白
[参考素材职责] 见 2.2，只留这次真正用到的

[0–4 秒 镜头 S01]《虎胆龙威》·Nakatomi大厦之夜：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[4–9 秒 镜头 S02]《铁血战士》·丛林热成像：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[9–16 秒 镜头 S03]《猎杀红色十月》·潜艇舱内：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[16–30 秒 镜头 S04]《虎胆龙威3》·纽约街头：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。

[声音] 环境声：（照场景补）／对白：<写准确台词，不要写「说点什么」>／配乐：（不想要就写「无配乐」）

[场景特定限制] 避免平光照明，避免色彩杂乱，避免构图失衡。
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

#### 镜头 1：虎胆龙威 · Nakatomi大厦之夜

```text
【运镜】低角度硬汉布光（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在Nakatomi大厦之夜里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《虎胆龙威》的Nakatomi大厦之夜；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】暗调动作中烟雾弥漫的硬汉剪影，潜艇钢蓝与丛林暗绿交织的硬核战场，爆炸暖橙撕裂烟雾阴影的 80 年代动作巅峰。配色：主色 潜艇钢蓝 `#1E3040` 占 25%，辅色 丛林暗绿 `#1E2E1A` 占 20%、烟雾影黑 `#2A2A2E` 占 20%、爆炸暖橙 `#C45020` 占 15%，点缀 硬汉汗肤 `#9C7860` 占 12%、军事卡其 `#6B6448` 占 8%。让主色占主导，其余按比例递减。光线：主光：硬侧光+烟雾散射光，明暗分明的硬汉布光，实战质感；高光偏暖橙/火光（爆炸、火焰、枪口焰）；阴影偏钢蓝/暗绿（夜战冷蓝+丛林绿暗，烟雾弥漫处呈烟灰）；对比度：高对比（70-88%），烟雾柔化边缘但核心明暗分明；整体：暗调硬核动作，70% 冷钢蓝暗绿烟灰 + 30% 暖橙火光点缀。运镜与构图：经典三幕式构景、低角度硬汉、烟雾弥漫纵深、热成像视角、手持战场感、轨道侧移跟拍、爆炸逆光剪影、封闭式空间压迫、军事地图俯拍、第一人称瞄准。色彩与光影：暗调钢蓝、丛林暗绿、烟雾烟灰、爆炸暖橙、硬汉汗光、军事卡其、热成像红、警灯红蓝、枪口焰、油汗质感。氛围与情绪：硬核硬汉、孤立无援、猫鼠猎杀、军事紧张、黑色幽默、蓝领英雄、80 年代动作、烟雾迷漫、一触即发、原始暴力。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 2：铁血战士 · 丛林热成像

```text
【运镜】烟雾纵深构图（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在丛林热成像里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《铁血战士》的丛林热成像；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】暗调动作中烟雾弥漫的硬汉剪影，潜艇钢蓝与丛林暗绿交织的硬核战场，爆炸暖橙撕裂烟雾阴影的 80 年代动作巅峰。配色：主色 潜艇钢蓝 `#1E3040` 占 25%，辅色 丛林暗绿 `#1E2E1A` 占 20%、烟雾影黑 `#2A2A2E` 占 20%、爆炸暖橙 `#C45020` 占 15%，点缀 硬汉汗肤 `#9C7860` 占 12%、军事卡其 `#6B6448` 占 8%。让主色占主导，其余按比例递减。光线：主光：硬侧光+烟雾散射光，明暗分明的硬汉布光，实战质感；高光偏暖橙/火光（爆炸、火焰、枪口焰）；阴影偏钢蓝/暗绿（夜战冷蓝+丛林绿暗，烟雾弥漫处呈烟灰）；对比度：高对比（70-88%），烟雾柔化边缘但核心明暗分明；整体：暗调硬核动作，70% 冷钢蓝暗绿烟灰 + 30% 暖橙火光点缀。运镜与构图：经典三幕式构景、低角度硬汉、烟雾弥漫纵深、热成像视角、手持战场感、轨道侧移跟拍、爆炸逆光剪影、封闭式空间压迫、军事地图俯拍、第一人称瞄准。色彩与光影：暗调钢蓝、丛林暗绿、烟雾烟灰、爆炸暖橙、硬汉汗光、军事卡其、热成像红、警灯红蓝、枪口焰、油汗质感。氛围与情绪：硬核硬汉、孤立无援、猫鼠猎杀、军事紧张、黑色幽默、蓝领英雄、80 年代动作、烟雾迷漫、一触即发、原始暴力。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 3：猎杀红色十月 · 潜艇舱内

```text
【运镜】热成像视角POV（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在潜艇舱内里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《猎杀红色十月》的潜艇舱内；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】暗调动作中烟雾弥漫的硬汉剪影，潜艇钢蓝与丛林暗绿交织的硬核战场，爆炸暖橙撕裂烟雾阴影的 80 年代动作巅峰。配色：主色 潜艇钢蓝 `#1E3040` 占 25%，辅色 丛林暗绿 `#1E2E1A` 占 20%、烟雾影黑 `#2A2A2E` 占 20%、爆炸暖橙 `#C45020` 占 15%，点缀 硬汉汗肤 `#9C7860` 占 12%、军事卡其 `#6B6448` 占 8%。让主色占主导，其余按比例递减。光线：主光：硬侧光+烟雾散射光，明暗分明的硬汉布光，实战质感；高光偏暖橙/火光（爆炸、火焰、枪口焰）；阴影偏钢蓝/暗绿（夜战冷蓝+丛林绿暗，烟雾弥漫处呈烟灰）；对比度：高对比（70-88%），烟雾柔化边缘但核心明暗分明；整体：暗调硬核动作，70% 冷钢蓝暗绿烟灰 + 30% 暖橙火光点缀。运镜与构图：经典三幕式构景、低角度硬汉、烟雾弥漫纵深、热成像视角、手持战场感、轨道侧移跟拍、爆炸逆光剪影、封闭式空间压迫、军事地图俯拍、第一人称瞄准。色彩与光影：暗调钢蓝、丛林暗绿、烟雾烟灰、爆炸暖橙、硬汉汗光、军事卡其、热成像红、警灯红蓝、枪口焰、油汗质感。氛围与情绪：硬核硬汉、孤立无援、猫鼠猎杀、军事紧张、黑色幽默、蓝领英雄、80 年代动作、烟雾迷漫、一触即发、原始暴力。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```


### 3.2 本导演可用的运镜（挑一个，别叠加）

- **低角度硬汉布光** —— 经典好莱坞硬汉打光，侧光勾勒轮廓（例：《虎胆龙威》麦克莱恩登场、《铁血战士》达奇）
- **烟雾纵深构图** —— 硝烟/雾气/蒸汽制造纵深层次（例：《虎胆龙威》通风管道、《铁血战士》丛林晨雾）
- **热成像视角POV** —— 铁血战士视角的热成像视觉（例：《铁血战士》经典热成像猎杀视角）
- **爆炸逆光剪影** —— 爆炸在身后人物成剪影（例：《虎胆龙威》屋顶爆炸、多场动作戏）
- **封闭空间压迫** —— 建筑/潜艇/丛林的封闭感构图（例：《虎胆龙威》Nakatomi 大厦、《猎杀红色十月》潜艇舱）
- **手持战场晃动** —— 动作场景中手持增加实战感（例：《铁血战士》丛林交火、《虎胆龙威》枪战场面）

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
画面抖动，多余肢体，手指畸形，面部漂移，文字水印，物体变形，闪烁跳帧，重复物体，光线杂乱，避免平光照明，避免色彩杂乱，避免构图失衡。
```

---

## 四、MiniMax H3（海螺）

H3 按时间戳写，不分镜头。**声音要单独成段**。

```text
【核心创意】暗调动作中烟雾弥漫的硬汉剪影，潜艇钢蓝与丛林暗绿交织的硬核战场，爆炸暖橙撕裂烟雾阴影的 80 年代动作巅峰。
［主体］在Nakatomi大厦之夜。

【分段过程描述】
[0–4s] 开场：虎胆龙威 式空间。［主体动作：缓慢抬手 / 微微低头 / 顺势坐下，写清幅度和速度］。
[4–8s] 中段：［主体动作承接上一拍，写惯性衔接］。
[8–12s] 收尾：［主体停住，画面定格在 潜艇钢蓝+烟雾影黑+爆炸暖橙 的调子上］。

【声音】
overall_soundscape：（环境声 + 物理声 + 有无对白）
non_diegetic_music：（配乐；不想要就写「无配乐」）

【结束状态】画面收在［想要的那一帧］。
```

> 提示词上限约 **7000 字符**，写长不是问题，**糊成一段不分层才是**。

---

## 五、Runway / Pika

## 二、场景镜头模板

### 镜头 1：大厦走廊枪战（Corridor Shootout）

**提示词：**
```
A man in a dirty white tank top moves cautiously down a dark office corridor,
John McTiernan Die Hard style,
steel blue fluorescent lights flicker overhead,
smoke billows from a doorway ahead,
he holds a pistol in both hands, barefoot on broken glass,
warm orange fire glow pulses from a room further down,
bullet holes in walls, spent casings on carpet,
he presses against the wall, peeks around corner,
classic 80s action tension,
hard side lighting, deep shadows,
tracking shot following him from behind,
smoke creating depth layers,
16:9 aspect ratio, steady but tense camera movement
```

**镜头参数：**
- 时长：6-8秒
- 运镜：跟踪跟拍（tracking from behind）
- 节奏：紧张、屏息、一触即发

---

### 镜头 2：屋顶爆炸跳跃（Roof Explosion Jump）

**提示词：**
```
A massive orange fireball erupts on a skyscraper rooftop at night,
John McTiernan Die Hard style,
a man tied to a fire hose leaps off the roof edge as the explosion hits,
debris and glass fly outward in slow motion,
he falls silhouetted against the brilliant orange fireball,
smoke billows up into the steel blue night sky,
the fire hose unspools behind him,
warm orange backlight contrasts with cold blue night,
classic action movie hero moment,
slow motion shot, high contrast,
practical explosion effects,
2.35:1 widescreen aspect ratio
```

**镜头参数：**
- 时长：5-7秒
- 运镜：慢动作固定/微跟（slow motion wide shot）
- 节奏：爆发、慢动作、经典动作时刻

---

### 镜头 3：丛林热成像POV（Thermal Vision POV）

**提示词：**
```
First person perspective through thermal imaging goggles in a dark jungle,
John McTiernan Predator style,
the world is dark green and black with bright red-orange heat signatures,
soldiers move through foliage below glowing with body heat,
their weapons and recently fired guns glow brighter red,
a crosshair tracks across the scene,
the camera slowly pans scanning for targets,
one soldier looks up directly at the camera sensing something,
his heat signature glows intensely,
unseen hunter perspective, terrifying,
dense dark green jungle with red heat blobs,
POV shot, slow deliberate panning,
16:9 aspect ratio, eerie tension
```

**镜头参数：**
- 时长：6-8秒
- 运镜：POV缓慢扫描（first person slow pan/scan）
- 节奏：恐怖、猎杀、未知威胁

---

### 镜头 4：潜艇紧急下潜（Submarine Crash Dive）

**提示词：**
```
Inside a Soviet nuclear submarine control room during an emergency,
John McTiernan Hunt for Red October style,
red alarm lights flash rhythmically casting crimson light across steel faces,
sailors in dark uniforms rush to stations, shouting commands,
depth needles spin, sonar screens glow green with blips,
steam or smoke leaks from a pipe overhead,
steel blue bulkheads with condensation dripping,
the submarine tilts sharply throwing men off balance,
cold war tension, claustrophobic metallic room,
handheld camera with the tilt of the sub,
hard shadows, red emergency lighting,
naval thriller intensity, 16:9 aspect ratio
```

**镜头参数：**
- 时长：6-8秒
- 运镜：手持晃动+潜艇倾斜（handheld with sub tilt）
- 节奏：紧急、军事、危机

---

### 镜头 5：硬汉现身（Tough Guy Reveal）

**提示词：**
```
A man in a dirty tank top emerges from smoke and shadow in a dark office,
John McTiernan Die Hard style,
he steps forward out of the smoke into a shaft of warm orange firelight,
sweat and blood on his face, barefoot, gun in hand,
catchphrase one-liner expression, cool and determined,
steel blue darkness behind him, smoke swirling around,
classic action hero reveal shot,
low angle looking up slightly,
he catches his breath, smirks slightly,
hard side lighting from the fire carving his features,
smoke parts revealing him,
iconic tough guy moment,
medium shot, slow dolly in, 16:9 aspect ratio
```

**镜头参数：**
- 时长：5-6秒
- 运镜：低角度慢推（low angle slow dolly in）
- 节奏：英雄现身、经典、酷

---

### 镜头 6：丛林小队伏击中（Jungle Ambush）

**提示词：**
```
A squad of soldiers moves through dense dark green jungle,
John McTiernan Predator style,
military khaki uniforms, faces streaked with mud and sweat,
they move in formation, weapons raised, eyes scanning the trees,
dappled green sunlight through thick canopy,
humidity visible in the air, insects swarming,
the jungle is too quiet, no birds,
one soldier freezes and points at something unseen in trees,
the others take cover positions,
tension builds before the ambush,
slow tracking shot following the point man,
dark green palette with khaki accents,
natural hard lighting, 16:9 aspect ratio
```

**镜头参数：**
- 时长：7-9秒
- 运镜：缓慢推进（slow advance tracking）
- 节奏：寂静→紧张→伏击前

---

## 三、运镜关键词速查

| 运镜效果 | 英文关键词 |
|---------|-----------|
| 硬汉低角度 | low angle tough guy shot, heroic angle, looking up at hero |
| 跟踪跟拍 | tracking shot from behind, following through corridors |
| 爆炸慢动作 | slow motion explosion, fireball backlight, debris flying |
| 手持战场 | handheld combat camera, shaky action, battle cam |
| 热成像POV | thermal vision POV, heat signature scan, first person hunter |
| 轨道侧移 | lateral dolly track, side tracking hero walk |
| 封闭空间 | claustrophobic interior, narrow corridor, enclosed space |
| 烟雾纵深 | smoke-filled depth, atmospheric haze, layered fog |

---

## 四、颜色与光影关键词

| 效果 | 英文关键词 |
|------|-----------|
| 钢蓝冷调 | steel blue, cold fluorescent, blue night interior, metallic blue |
| 丛林暗绿 | dark jungle green, military olive, foliage darkness, camo green |
| 烟雾影黑 | smoke shadow, thick smoke haze, dark silhouette, black shadows |
| 爆炸暖橙 | warm orange explosion, fire backlight, muzzle flash orange, fire glow |
| 硬汉汗光 | sweat glistening, hard side lighting, tough guy key light |
| 军事卡其 | military khaki, olive drab, army green, camo pattern |
| 热成像红 | thermal red, heat signature glow, red-orange body heat |
| 警灯红蓝 | red and blue police lights, siren flash, emergency lighting |

---

## 五、负面描述（避免的效果）

```
superhero movies, marvel CGI, john wick neon style,
wire fu martial arts, fast cgi cuts,
bright saturated colors, daylight action scenes,
sleek modern guns, polished clean aesthetic,
anime style, cartoon violence, video game graphics,
shaky cam overload, bourne identity quick cuts,
romantic subplot, comedy relief,
slow cinema, meditative shots, art house style,
lush green paradise, bright sunny jungle
```

---

> 本文件由 `色卡主文档.md` 派生（运镜特征表 / 经典场景表 / 色板 / 光影），未新增事实。
> Seedance 2.5 段的结构规则来自本机技能库 `film-cinedance/references/seedance-25-prompt-format.md`。
> 图像提示词见 `midjourney_prompts.md` · `conversational_prompts.md`。
