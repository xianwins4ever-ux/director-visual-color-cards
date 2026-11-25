# 视频提示词 — 大友克洋 Katsuhiro Otomo 风格

> **一个文件，四套规则。你用哪个模型，就用哪一段。**
> 编号 `029` ｜ 分类 02 霓虹黑色与赛博未来 ｜ 国籍 日本

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
爆炸橙红撕裂末日都市的废墟灰棕，赛博朋克的能量洪流与毁灭美学在高饱和色块碰撞中迸发新东京的末世预言。配色：主色 末日深黑 `#0D0D0D` 占 28%，辅色 爆炸橙红 `#FF3D00` 占 20%、废墟灰棕 `#5D4037` 占 15%、烟尘金 `#BF8F3C` 占 13%，点缀 新东京红 `#D32F2F` 占 12%、能量蓝 `#1565C0` 占 12%。让主色占主导，其余按比例递减。光线：主光：强烈的顶光/爆炸光源，硬光为主，能量自发光体（爆炸/超能力）作为核心光源；高光偏爆炸橙红/核爆白黄（爆炸核心/能量释放/火光）；阴影偏冷蓝偏黑（建筑阴影/军事科技暗部/夜晚）；对比度：极高对比（80-95%），饱和色块碰撞，黑与亮橙红极端对比；整体：高饱和末日，60% 暖橙红棕 + 40% 冷蓝黑。运镜与构图：爆炸中心扩散、废墟纵深透视、大规模破坏全景、速度线爆发、建筑崩塌碎片、少年暴走正面、军事机械对峙、烟尘弥漫远景、赛博街道纵深、能量光流扭曲。色彩与光影：爆炸橙红、末日深黑、废墟棕灰、新东京血红、能量蓝光、烟尘金、核爆白黄、高饱和碰撞、硬光切割、自发光体。氛围与情绪：末日预言、少年暴走、毁灭美学、赛博废墟、社会崩溃、能量觉醒、暴力史诗、反乌托邦、科技恐惧、新东京狂热。
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
[总控] 30 秒 ｜ 竖版 9:16 ｜ 爆炸橙红撕裂末日都市的废墟灰棕，赛博朋克的能量洪流与毁灭美学在高饱和色块碰撞中迸发新东京的末世预言。 ｜ 单主角 ｜ 有对白 / 无对白
[参考素材职责] 见 2.2，只留这次真正用到的

[0–4 秒 镜头 S01]《阿基拉》·东京毁灭爆炸：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[4–9 秒 镜头 S02]《回忆三部曲·她的回忆》·宇宙废弃空间站：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[9–16 秒 镜头 S03]《回忆三部曲·最臭兵器》·日本乡村灾难：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[16–30 秒 镜头 S04]《蒸汽男孩》·工业伦敦博览会：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。

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

#### 镜头 1：阿基拉 · 东京毁灭爆炸

```text
【运镜】爆炸中心扩散（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在东京毁灭爆炸里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《阿基拉》的东京毁灭爆炸；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】爆炸橙红撕裂末日都市的废墟灰棕，赛博朋克的能量洪流与毁灭美学在高饱和色块碰撞中迸发新东京的末世预言。配色：主色 末日深黑 `#0D0D0D` 占 28%，辅色 爆炸橙红 `#FF3D00` 占 20%、废墟灰棕 `#5D4037` 占 15%、烟尘金 `#BF8F3C` 占 13%，点缀 新东京红 `#D32F2F` 占 12%、能量蓝 `#1565C0` 占 12%。让主色占主导，其余按比例递减。光线：主光：强烈的顶光/爆炸光源，硬光为主，能量自发光体（爆炸/超能力）作为核心光源；高光偏爆炸橙红/核爆白黄（爆炸核心/能量释放/火光）；阴影偏冷蓝偏黑（建筑阴影/军事科技暗部/夜晚）；对比度：极高对比（80-95%），饱和色块碰撞，黑与亮橙红极端对比；整体：高饱和末日，60% 暖橙红棕 + 40% 冷蓝黑。运镜与构图：爆炸中心扩散、废墟纵深透视、大规模破坏全景、速度线爆发、建筑崩塌碎片、少年暴走正面、军事机械对峙、烟尘弥漫远景、赛博街道纵深、能量光流扭曲。色彩与光影：爆炸橙红、末日深黑、废墟棕灰、新东京血红、能量蓝光、烟尘金、核爆白黄、高饱和碰撞、硬光切割、自发光体。氛围与情绪：末日预言、少年暴走、毁灭美学、赛博废墟、社会崩溃、能量觉醒、暴力史诗、反乌托邦、科技恐惧、新东京狂热。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 2：回忆三部曲·她的回忆 · 宇宙废弃空间站

```text
【运镜】废墟纵深透视（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在宇宙废弃空间站里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《回忆三部曲·她的回忆》的宇宙废弃空间站；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】爆炸橙红撕裂末日都市的废墟灰棕，赛博朋克的能量洪流与毁灭美学在高饱和色块碰撞中迸发新东京的末世预言。配色：主色 末日深黑 `#0D0D0D` 占 28%，辅色 爆炸橙红 `#FF3D00` 占 20%、废墟灰棕 `#5D4037` 占 15%、烟尘金 `#BF8F3C` 占 13%，点缀 新东京红 `#D32F2F` 占 12%、能量蓝 `#1565C0` 占 12%。让主色占主导，其余按比例递减。光线：主光：强烈的顶光/爆炸光源，硬光为主，能量自发光体（爆炸/超能力）作为核心光源；高光偏爆炸橙红/核爆白黄（爆炸核心/能量释放/火光）；阴影偏冷蓝偏黑（建筑阴影/军事科技暗部/夜晚）；对比度：极高对比（80-95%），饱和色块碰撞，黑与亮橙红极端对比；整体：高饱和末日，60% 暖橙红棕 + 40% 冷蓝黑。运镜与构图：爆炸中心扩散、废墟纵深透视、大规模破坏全景、速度线爆发、建筑崩塌碎片、少年暴走正面、军事机械对峙、烟尘弥漫远景、赛博街道纵深、能量光流扭曲。色彩与光影：爆炸橙红、末日深黑、废墟棕灰、新东京血红、能量蓝光、烟尘金、核爆白黄、高饱和碰撞、硬光切割、自发光体。氛围与情绪：末日预言、少年暴走、毁灭美学、赛博废墟、社会崩溃、能量觉醒、暴力史诗、反乌托邦、科技恐惧、新东京狂热。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 3：回忆三部曲·最臭兵器 · 日本乡村灾难

```text
【运镜】大规模破坏全景（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在日本乡村灾难里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《回忆三部曲·最臭兵器》的日本乡村灾难；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】爆炸橙红撕裂末日都市的废墟灰棕，赛博朋克的能量洪流与毁灭美学在高饱和色块碰撞中迸发新东京的末世预言。配色：主色 末日深黑 `#0D0D0D` 占 28%，辅色 爆炸橙红 `#FF3D00` 占 20%、废墟灰棕 `#5D4037` 占 15%、烟尘金 `#BF8F3C` 占 13%，点缀 新东京红 `#D32F2F` 占 12%、能量蓝 `#1565C0` 占 12%。让主色占主导，其余按比例递减。光线：主光：强烈的顶光/爆炸光源，硬光为主，能量自发光体（爆炸/超能力）作为核心光源；高光偏爆炸橙红/核爆白黄（爆炸核心/能量释放/火光）；阴影偏冷蓝偏黑（建筑阴影/军事科技暗部/夜晚）；对比度：极高对比（80-95%），饱和色块碰撞，黑与亮橙红极端对比；整体：高饱和末日，60% 暖橙红棕 + 40% 冷蓝黑。运镜与构图：爆炸中心扩散、废墟纵深透视、大规模破坏全景、速度线爆发、建筑崩塌碎片、少年暴走正面、军事机械对峙、烟尘弥漫远景、赛博街道纵深、能量光流扭曲。色彩与光影：爆炸橙红、末日深黑、废墟棕灰、新东京血红、能量蓝光、烟尘金、核爆白黄、高饱和碰撞、硬光切割、自发光体。氛围与情绪：末日预言、少年暴走、毁灭美学、赛博废墟、社会崩溃、能量觉醒、暴力史诗、反乌托邦、科技恐惧、新东京狂热。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```


### 3.2 本导演可用的运镜（挑一个，别叠加）

- **爆炸中心扩散** —— 从爆炸核心向外辐射的冲击波镜头（例：《阿基拉》铁雄能量爆炸）
- **废墟纵深透视** —— 沿崩坏街道的极强透视，建筑碎片飞溅（例：《阿基拉》新东京废墟追逐）
- **大规模破坏全景** —— 极远景展现城市级别的毁灭（例：《阿基拉》东京毁灭/新东京崩坏）
- **速度线爆发** —— 漫画式速度线与光流表现极速运动（例：《阿基拉》金田摩托车飙车）
- **建筑崩塌碎片** —— 慢镜展现建筑碎裂崩塌的壮观（例：《阿基拉》奥林匹克体育场崩塌）
- **少年正面暴走** —— 正面/低角度拍摄少年暴走的压迫感（例：《阿基拉》铁雄超能力失控）

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
【核心创意】爆炸橙红撕裂末日都市的废墟灰棕，赛博朋克的能量洪流与毁灭美学在高饱和色块碰撞中迸发新东京的末世预言。
［主体］在东京毁灭爆炸。

【分段过程描述】
[0–4s] 开场：阿基拉 式空间。［主体动作：缓慢抬手 / 微微低头 / 顺势坐下，写清幅度和速度］。
[4–8s] 中段：［主体动作承接上一拍，写惯性衔接］。
[8–12s] 收尾：［主体停住，画面定格在 爆炸橙红+核爆白黄+末日深黑 的调子上］。

【声音】
overall_soundscape：（环境声 + 物理声 + 有无对白）
non_diegetic_music：（配乐；不想要就写「无配乐」）

【结束状态】画面收在［想要的那一帧］。
```

> 提示词上限约 **7000 字符**，写长不是问题，**糊成一段不分层才是**。

---

## 五、Runway / Pika

## 二、场景镜头模板

### 镜头 1：新东京开篇全景（Establishing Shot）

**提示词：**
```
Extreme wide aerial shot of neo-Tokyo at night,
Katsuhiro Otomo Akira style,
massive sprawling cyberpunk city stretching to the horizon,
neon signs in orange-red and energy blue,
the Olympic stadium crater visible in the distance with faint glow,
helicopters with searchlights cross the sky,
the camera slowly pans across the vast cityscape,
dark sky with smog and city glow,
ruined sections contrast with neon-lit areas,
post-apocalyptic cyberpunk atmosphere,
80s anime cinematic, film grain, high saturation,
16:9 aspect ratio, slow panoramic aerial movement
```

**镜头参数：**
- 时长：7-9秒
- 运镜：航拍横摇（aerial pan）
- 节奏：缓慢，末日都市压迫感

---

### 镜头 2：摩托车飙车追逐（Bike Chase）

**提示词：**
```
Red futuristic motorcycles speeding through neo-Tokyo streets at high speed,
Katsuhiro Otomo Akira style,
the bikes race past neon signs and towering buildings,
speed lines streak behind them, motion blur on the background,
orange-red taillights leave glowing trails,
wet asphalt reflects the neon cyan and red lights,
the camera follows alongside the bikes at high speed,
buildings rush past in a blur of perspective,
smoke and exhaust trail behind,
intense velocity and teenage rebellion,
80s anime cyberpunk chase, high energy,
16:9 aspect ratio, fast lateral tracking shot
```

**镜头参数：**
- 时长：5-7秒
- 运镜：高速侧跟（high-speed lateral tracking）
- 节奏：快速，速度感与叛逆感

---

### 镜头 3：铁雄能量爆发（Energy Explosion）

**提示词：**
```
A teenage boy standing in a destroyed street, energy erupting from his body,
Katsuhiro Otomo Akira style,
his body begins to glow with intense white-yellow nuclear light,
orange-red energy shockwave expands outward in slow motion,
the ground cracks and debris rises into the air,
buildings around him begin to crumble inward,
glass shatters and metal bends from the psychic force,
his hair blows wildly in the energy wind,
self-illuminated by the power within him,
the camera pulls back rapidly as the explosion grows,
apocalyptic power, transcendence through destruction,
anime cinematic, high contrast, high saturation,
2.35:1 aspect ratio, rapid pull-back with slow-motion energy
```

**镜头参数：**
- 时长：5-7秒
- 运镜：快速拉远+慢镜爆炸（rapid pull-back + slow-mo）
- 节奏：渐强爆发，毁灭与升华

---

### 镜头 4：建筑崩塌（Building Collapse）

**提示词：**
```
Massive concrete buildings crumbling and collapsing in neo-Tokyo,
Katsuhiro Otomo Akira style,
the structures crack and break apart in slow motion,
huge chunks of concrete and steel rebar fall through dusty air,
orange fire and smoke billow from within,
grey-brown dust cloud expands outward,
debris rains down on the street below,
people running from the destruction,
military tanks retreating,
the camera is at street level looking up at the falling buildings,
overwhelming scale of destruction,
anime epic cinematic, film grain, detailed rubble,
16:9 aspect ratio, slow-motion collapse
```

**镜头参数：**
- 时长：6-8秒
- 运镜：低角度仰拍慢镜（low angle slow-motion）
- 节奏：慢镜，毁灭的壮观

---

### 镜头 5：废墟行走（Ruins Walk）

**提示词：**
```
Three figures walking through the vast ruins of neo-Tokyo after destruction,
Katsuhiro Otomo Akira style,
grey-brown rubble and twisted metal stretches in every direction,
a massive crater glows with faint energy blue light in the distance,
orange-tinted dusty sky, smoke columns rising,
they walk slowly through debris, small figures against the vast ruin,
a destroyed motorcycle lies half-buried in rubble,
the camera tracks alongside them at a distance,
dust motes float in the orange-tinted air,
post-apocalyptic desolation, the world after,
80s anime cinematic, film grain, melancholic beauty,
21:9 aspect ratio, slow distant tracking shot
```

**镜头参数：**
- 时长：6-8秒
- 运镜：远景侧跟（distant lateral tracking）
- 节奏：缓慢，废墟中的渺小感

---

### 镜头 6：东京核爆（Tokyo Destruction）

**提示词：**
```
The massive explosion that destroys Tokyo, seen from above,
Katsuhiro Otomo Akira style,
a blinding white-yellow light expands from a single point,
the orange-red fireball grows to consume the entire city,
a shockwave ring of dust and debris races outward,
buildings are flattened in an expanding circle,
the sky turns from dark to bright orange,
everything is consumed by the nuclear-like detonation,
the camera pulls back rapidly showing the scale of destruction,
genesis-level event, the end and beginning,
anime cinematic epic, extreme high contrast,
white-yellow center to orange-red edges,
16:9 or 2.35:1 aspect ratio, rapid pull-back
```

**镜头参数：**
- 时长：5-7秒
- 运镜：高速拉远（rapid pull-back/reverse zoom）
- 节奏：极快，创世纪级别的毁灭

---

## 三、运镜关键词速查

| 运镜效果 | 英文关键词 |
|---------|-----------|
| 爆炸扩散 | explosion expanding outward, shockwave spreading, energy blast radius |
| 高速追逐 | high speed tracking, speed chase, lateral motion blur, velocity streaks |
| 建筑崩塌慢镜 | slow-motion building collapse, debris falling, concrete crumbling |
| 废墟远景 | extreme wide ruin shot, vast destruction panorama, apocalyptic landscape |
| 能量爆发 | energy erupting, self-illuminated power, glow intensifying, psychic power |
| 军事对峙 | military standoff, tanks facing, helicopters overhead, standoff tension |
| 城市航拍 | aerial cityscape, neo-Tokyo panorama, establishing shot from above |
| 透视纵深 | deep perspective street, vanishing point, buildings towering overhead |

---

## 四、颜色与光影关键词

| 效果 | 英文关键词 |
|------|-----------|
| 爆炸橙红 | explosive orange-red, fireball orange, nuclear orange glow |
| 核爆白黄 | nuclear white-yellow, blinding white core, pure energy white |
| 新东京红 | neo-Tokyo red, biker jacket red, red taillight streaks |
| 能量蓝 | energy blue, psychic blue glow, power line blue, military tech blue |
| 废墟灰棕 | grey-brown ruins, concrete dust, rubble tones, post-apocalyptic muted |
| 烟尘金 | dust gold, smoke haze, orange-tinted air, explosion dust cloud |
| 超能紫 | psychic purple, supernatural energy purple, power aura purple |
| 硬光切割 | hard edge lighting, harsh shadows, high contrast, sharp light |

---

## 五、负面描述（避免的效果）

```
slow contemplative mood, soft lighting, gentle atmosphere,
pastel colors, watercolor, muted desaturated tones,
cute characters, chibi, moe style,
peaceful scenery, nature landscape, flowers,
3d cgi, photorealistic rendering,
romance, comedy, slice of life,
shaky cam found footage,
steampunk (unless specifically Steamboy)
```

---

> 本文件由 `色卡主文档.md` 派生（运镜特征表 / 经典场景表 / 色板 / 光影），未新增事实。
> Seedance 2.5 段的结构规则来自本机技能库 `film-cinedance/references/seedance-25-prompt-format.md`。
> 图像提示词见 `midjourney_prompts.md` · `conversational_prompts.md`。
