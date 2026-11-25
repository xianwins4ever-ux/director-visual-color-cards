# 视频提示词 — 詹姆斯·卡梅隆 James Cameron 风格

> **一个文件，四套规则。你用哪个模型，就用哪一段。**
> 编号 `031` ｜ 分类 02 霓虹黑色与赛博未来 ｜ 国籍 加拿大

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
蓝钢机械与水下幽光交织的高科技冷色世界中，镀铬银反射火焰橙的爆裂冲击，生物荧光青在深海与外星丛林中点亮史诗奇观。配色：主色 深海蓝黑 `#0A1929` 占 28%，辅色 机械钢蓝 `#37474F` 占 18%、暖金内光 `#FFB74D` 占 17%、生物荧光青 `#00E676` 占 15%，点缀 火焰橙 `#FF6D00` 占 12%、镀铬银 `#B0BEC5` 占 10%。让主色占主导，其余按比例递减。光线：主光：强侧光/底光为主，机械硬光与生物柔光交替，爆炸光源和生物自发光；高光偏镀铬银/火焰橙（金属反射/爆炸火光/枪火闪光）；阴影偏深海蓝黑（暗部偏蓝、水底/太空/夜景阴影）；对比度：高对比（70-90%），冷暖极端对比，蓝冷 vs 橙暖经典互补；整体：冷调科技，65% 蓝冷钢色 + 35% 橙暖火焰/金内光。运镜与构图：史诗远景、机械细节特写、追逐运动长镜、水下光影、机甲对峙正面、外星奇观全景、沉船纵深、爆炸冲击帧、终结者行走、飞船/潜艇航行。色彩与光影：蓝钢机械、镀铬银反射、火焰橙爆裂、生物荧光青、深海幽蓝、暖金内光、激光红眼、水下光柱、全息电蓝、冷暖强对比。氛围与情绪：高科技史诗、机械无情、生存搏斗、深海幽闭、外星奇观、人机对抗、末日审判、浪漫悲剧、技术敬畏、英雄主义。
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
[总控] 30 秒 ｜ 竖版 9:16 ｜ 蓝钢机械与水下幽光交织的高科技冷色世界中，镀铬银反射火焰橙的爆裂冲击，生物荧光青在深海与外星丛林中点亮史诗奇观。 ｜ 单主角 ｜ 有对白 / 无对白
[参考素材职责] 见 2.2，只留这次真正用到的

[0–4 秒 镜头 S01]《终结者2》·T-800酒吧出场：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[4–9 秒 镜头 S02]《阿凡达》·潘多拉夜光森林：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[9–16 秒 镜头 S03]《泰坦尼克号》·沉船/深海：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[16–30 秒 镜头 S04]《深渊》·深海外星生命体：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。

[声音] 环境声：（照场景补）／对白：<写准确台词，不要写「说点什么」>／配乐：（不想要就写「无配乐」）

[场景特定限制] 颜色脏混，看不清动作，廉价霓虹，无动机环绕和随机变焦，用统一滤镜替代色彩比例，光源和材质。
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

#### 镜头 1：终结者2 · T-800酒吧出场

```text
【运镜】史诗远景建立（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在T-800酒吧出场里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《终结者2》的T-800酒吧出场；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】蓝钢机械与水下幽光交织的高科技冷色世界中，镀铬银反射火焰橙的爆裂冲击，生物荧光青在深海与外星丛林中点亮史诗奇观。配色：主色 深海蓝黑 `#0A1929` 占 28%，辅色 机械钢蓝 `#37474F` 占 18%、暖金内光 `#FFB74D` 占 17%、生物荧光青 `#00E676` 占 15%，点缀 火焰橙 `#FF6D00` 占 12%、镀铬银 `#B0BEC5` 占 10%。让主色占主导，其余按比例递减。光线：主光：强侧光/底光为主，机械硬光与生物柔光交替，爆炸光源和生物自发光；高光偏镀铬银/火焰橙（金属反射/爆炸火光/枪火闪光）；阴影偏深海蓝黑（暗部偏蓝、水底/太空/夜景阴影）；对比度：高对比（70-90%），冷暖极端对比，蓝冷 vs 橙暖经典互补；整体：冷调科技，65% 蓝冷钢色 + 35% 橙暖火焰/金内光。运镜与构图：史诗远景、机械细节特写、追逐运动长镜、水下光影、机甲对峙正面、外星奇观全景、沉船纵深、爆炸冲击帧、终结者行走、飞船/潜艇航行。色彩与光影：蓝钢机械、镀铬银反射、火焰橙爆裂、生物荧光青、深海幽蓝、暖金内光、激光红眼、水下光柱、全息电蓝、冷暖强对比。氛围与情绪：高科技史诗、机械无情、生存搏斗、深海幽闭、外星奇观、人机对抗、末日审判、浪漫悲剧、技术敬畏、英雄主义。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 2：阿凡达 · 潘多拉夜光森林

```text
【运镜】机械细节特写（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在潘多拉夜光森林里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《阿凡达》的潘多拉夜光森林；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】蓝钢机械与水下幽光交织的高科技冷色世界中，镀铬银反射火焰橙的爆裂冲击，生物荧光青在深海与外星丛林中点亮史诗奇观。配色：主色 深海蓝黑 `#0A1929` 占 28%，辅色 机械钢蓝 `#37474F` 占 18%、暖金内光 `#FFB74D` 占 17%、生物荧光青 `#00E676` 占 15%，点缀 火焰橙 `#FF6D00` 占 12%、镀铬银 `#B0BEC5` 占 10%。让主色占主导，其余按比例递减。光线：主光：强侧光/底光为主，机械硬光与生物柔光交替，爆炸光源和生物自发光；高光偏镀铬银/火焰橙（金属反射/爆炸火光/枪火闪光）；阴影偏深海蓝黑（暗部偏蓝、水底/太空/夜景阴影）；对比度：高对比（70-90%），冷暖极端对比，蓝冷 vs 橙暖经典互补；整体：冷调科技，65% 蓝冷钢色 + 35% 橙暖火焰/金内光。运镜与构图：史诗远景、机械细节特写、追逐运动长镜、水下光影、机甲对峙正面、外星奇观全景、沉船纵深、爆炸冲击帧、终结者行走、飞船/潜艇航行。色彩与光影：蓝钢机械、镀铬银反射、火焰橙爆裂、生物荧光青、深海幽蓝、暖金内光、激光红眼、水下光柱、全息电蓝、冷暖强对比。氛围与情绪：高科技史诗、机械无情、生存搏斗、深海幽闭、外星奇观、人机对抗、末日审判、浪漫悲剧、技术敬畏、英雄主义。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 3：泰坦尼克号 · 沉船/深海

```text
【运镜】追逐运动长镜（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在沉船/深海里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《泰坦尼克号》的沉船/深海；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】蓝钢机械与水下幽光交织的高科技冷色世界中，镀铬银反射火焰橙的爆裂冲击，生物荧光青在深海与外星丛林中点亮史诗奇观。配色：主色 深海蓝黑 `#0A1929` 占 28%，辅色 机械钢蓝 `#37474F` 占 18%、暖金内光 `#FFB74D` 占 17%、生物荧光青 `#00E676` 占 15%，点缀 火焰橙 `#FF6D00` 占 12%、镀铬银 `#B0BEC5` 占 10%。让主色占主导，其余按比例递减。光线：主光：强侧光/底光为主，机械硬光与生物柔光交替，爆炸光源和生物自发光；高光偏镀铬银/火焰橙（金属反射/爆炸火光/枪火闪光）；阴影偏深海蓝黑（暗部偏蓝、水底/太空/夜景阴影）；对比度：高对比（70-90%），冷暖极端对比，蓝冷 vs 橙暖经典互补；整体：冷调科技，65% 蓝冷钢色 + 35% 橙暖火焰/金内光。运镜与构图：史诗远景、机械细节特写、追逐运动长镜、水下光影、机甲对峙正面、外星奇观全景、沉船纵深、爆炸冲击帧、终结者行走、飞船/潜艇航行。色彩与光影：蓝钢机械、镀铬银反射、火焰橙爆裂、生物荧光青、深海幽蓝、暖金内光、激光红眼、水下光柱、全息电蓝、冷暖强对比。氛围与情绪：高科技史诗、机械无情、生存搏斗、深海幽闭、外星奇观、人机对抗、末日审判、浪漫悲剧、技术敬畏、英雄主义。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```


### 3.2 本导演可用的运镜（挑一个，别叠加）

- **史诗远景建立** —— 极广阔的全景建立世界观（例：《阿凡达》潘多拉星球全景）
- **机械细节特写** —— 金属/武器/机甲的极致细节特写（例：《终结者 2》T-800/T-1000 金属特写）
- **追逐运动长镜** —— 高速运动的长镜头追逐（例：《终结者 2》卡车/摩托车追逐）
- **水下光影漫游** —— 水下光束与粒子的缓慢运动（例：《深渊》《泰坦尼克号》深海场景）
- **机甲正面行走** —— 低角度正面拍摄机械/战士逼近（例：《终结者 2》T-800 走来）
- **外星奇观全景** —— 360 度展现外星生态奇观（例：《阿凡达》潘多拉夜光森林）

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
画面抖动，多余肢体，手指畸形，面部漂移，文字水印，物体变形，闪烁跳帧，重复物体，光线杂乱，颜色脏混，看不清动作，廉价霓虹，无动机环绕和随机变焦，用统一滤镜替代色彩比例，光源和材质。
```

---

## 四、MiniMax H3（海螺）

H3 按时间戳写，不分镜头。**声音要单独成段**。

```text
【核心创意】蓝钢机械与水下幽光交织的高科技冷色世界中，镀铬银反射火焰橙的爆裂冲击，生物荧光青在深海与外星丛林中点亮史诗奇观。
［主体］在T-800酒吧出场。

【分段过程描述】
[0–4s] 开场：终结者2 式空间。［主体动作：缓慢抬手 / 微微低头 / 顺势坐下，写清幅度和速度］。
[4–8s] 中段：［主体动作承接上一拍，写惯性衔接］。
[8–12s] 收尾：［主体停住，画面定格在 机械钢蓝+镀铬银+激光红眼 的调子上］。

【声音】
overall_soundscape：（环境声 + 物理声 + 有无对白）
non_diegetic_music：（配乐；不想要就写「无配乐」）

【结束状态】画面收在［想要的那一帧］。
```

> 提示词上限约 **7000 字符**，写长不是问题，**糊成一段不分层才是**。

---

## 五、Runway / Pika

## 二、场景镜头模板

### 镜头 1：终结者走来（Terminator Approach）

**提示词：**
```
A tall muscular figure in black leather walks through a fiery corridor,
James Cameron Terminator style,
orange fire and explosions on both sides,
chrome metal glinting in the firelight,
sparks and debris falling around him,
he walks steadily, unstoppable, sunglasses reflecting flames,
cold blue-steel night visible through broken walls behind,
the camera tracks backward as he walks forward,
his leather jacket blows from the shockwave,
high contrast between hot orange fire and cold blue night,
unstoppable machine menace,
cinematic action, film grain, 80s sci-fi,
16:9 aspect ratio, reverse tracking shot
```

**镜头参数：**
- 时长：6-8秒
- 运镜：反向拉跟（reverse tracking）
- 节奏：稳定逼近，不可阻挡

---

### 镜头 2：卡车爆炸追逐（Truck Chase）

**提示词：**
```
High speed chase on a highway at night,
James Cameron Terminator 2 style,
a massive tanker truck engulfed in orange flames,
motorcycle weaving through traffic ahead,
sparks flying from collisions,
the truck smashes through cars creating explosions,
cold blue night sky contrasts with hot orange fire,
chrome and metal reflecting the flames intensely,
debris scattering across the wet road,
the camera follows the chase at high speed from the side,
intense action, practical effects style explosions,
cinematic blockbuster, film grain, high contrast,
2.35:1 aspect ratio, high speed lateral tracking
```

**镜头参数：**
- 时长：5-7秒
- 运镜：高速侧跟（high-speed lateral tracking）
- 节奏：极速，生死追逐

---

### 镜头 3：潘多拉森林夜（Pandora Night Forest）

**提示词：**
```
Flying through a bioluminescent alien forest at night,
James Cameron Avatar style,
trees and plants glowing with cyan-green bioluminescence,
purple and magenta foliage, floating glowing seeds,
the camera flies between giant glowing trees,
waterfalls cascade with glowing water,
alien creatures with glowing markings move through the underbrush,
multiple moons visible through the canopy above,
every surface pulses with gentle bioluminescent light,
the air shimmers with glowing spores,
magical epic alien nature wonder,
cinematic 3D depth, vivid saturated colors,
16:9 aspect ratio, smooth flying camera movement
```

**镜头参数：**
- 时长：7-9秒
- 运镜：林间飞行（flying through forest）
- 节奏：缓慢壮美，外星奇观

---

### 镜头 4：深海下潜（Deep Dive）

**提示词：**
```
Descending into the deep ocean abyss,
James Cameron The Abyss style,
light beams from submersible headlights cutting through dark blue-black water,
bioluminescent cyan and blue creatures swim past,
bubbles rise as we descend deeper,
particles and marine snow float in the water,
a massive mysterious alien structure glows far below,
the water grows darker and bluer with depth,
pressure seems to build, ethereal and awe-inspiring,
the camera slowly descends downward,
sense of immense depth and unknown wonder,
cinematic underwater shot, blue-dominated,
16:9 or 2.35:1 aspect ratio, slow descending
```

**镜头参数：**
- 时长：6-8秒
- 运镜：垂直下潜（slow vertical descent）
- 节奏：缓慢下潜，幽闭敬畏

---

### 镜头 5：机甲大战（Mech Battle）

**提示词：**
```
Giant mechanical robot suit fighting in a war zone,
James Cameron sci-fi epic style,
blue-steel mech suit with pilot visible in cockpit,
massive orange explosions erupting around it,
enemy mechs firing blue energy weapons,
buildings collapsing from the battle,
sparks and shrapnel flying,
the mech raises its arm and fires a weapon,
muzzle flash illuminates the metal armor,
chrome and steel reflecting fire and energy blasts,
epic scale warfare, high contrast action,
cinematic blockbuster, film grain,
2.35:1 cinemascope aspect ratio, dynamic action camera
```

**镜头参数：**
- 时长：5-7秒
- 运镜：动态环绕/手持（dynamic circling/handheld action）
- 节奏：快速，史诗战斗

---

### 镜头 6：泰坦尼克号沉船（Titanic Wreck）

**提示词：**
```
Submersible lights illuminate the sunken Titanic wreck on the ocean floor,
James Cameron style,
deep blue-black ocean, dark and cold,
the sub's headlights reveal the massive ship covered in rust and sediment,
fish swim through the broken windows,
the ship's grand staircase visible through a collapsed section,
particles of rust float in the water like snow,
warm golden light from the sub contrasts with cold blue deep sea,
the camera slowly moves along the ship's deck,
ghostly, tragic, hauntingly beautiful,
cinematic underwater shot, film grain,
16:9 aspect ratio, slow forward movement along wreck
```

**镜头参数：**
- 时长：7-9秒
- 运镜：慢速沿沉船推进（slow forward along wreck）
- 节奏：缓慢，悲剧浪漫

---

## 三、运镜关键词速查

| 运镜效果 | 英文关键词 |
|---------|-----------|
| 史诗远景建立 | epic establishing wide shot, sweeping aerial, vast panorama |
| 机械细节特写 | extreme close-up on metal, chrome detail, mechanical piston |
| 高速追逐 | high speed tracking, chase shot, vehicle pursuit, lateral motion |
| 水下摄影 | underwater shot, submersible POV, deep ocean camera, bubbles |
| 正面行走逼近 | low angle approaching shot, walking toward camera, reverse tracking |
| 爆炸慢镜 | slow-motion explosion, fireball expanding, shockwave debris |
| 外星飞行 | flying through alien landscape, soaring over terrain, aerial glide |
| 沉船深潜 | slow descent, deep submersible POV, underwater exploration |

---

## 四、颜色与光影关键词

| 效果 | 英文关键词 |
|------|-----------|
| 蓝钢机械 | blue-steel metallic, cold blue metal, steel blue tones |
| 镀铬银反射 | chrome silver reflection, polished metal, specular highlight on steel |
| 火焰橙 | orange fireball, fire glow, explosion orange, molten orange light |
| 生物荧光青 | bioluminescent cyan-green, glowing plants, underwater glow, neon cyan life |
| 深海幽蓝 | deep ocean blue-black, abyss blue, underwater darkness |
| 暖金内光 | warm golden interior light, ship cabin glow, warm tungsten |
| 激光红眼 | red laser eye, glowing red optic, red sensor light |
| 电蓝全息 | electric blue hologram, HUD blue light, futuristic blue interface |

---

## 五、负面描述（避免的效果）

```
soft focus dreamy, pastel colors, romantic soft lighting,
low budget look, cheap CGI video game graphics,
shaky cam found footage, phone camera,
slow contemplative art film, minimal action,
bright comedy tone, cheerful sunny day,
anime cartoon style, superhero costumes,
fantasy magic, medieval castles, dragon,
flat lighting, low contrast, desaturated
```

---

> 本文件由 `色卡主文档.md` 派生（运镜特征表 / 经典场景表 / 色板 / 光影），未新增事实。
> Seedance 2.5 段的结构规则来自本机技能库 `film-cinedance/references/seedance-25-prompt-format.md`。
> 图像提示词见 `midjourney_prompts.md` · `conversational_prompts.md`。
