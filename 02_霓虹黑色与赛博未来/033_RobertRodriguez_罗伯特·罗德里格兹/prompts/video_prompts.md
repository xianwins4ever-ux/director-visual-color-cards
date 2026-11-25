# 视频提示词 — 罗德里格兹 Robert Rodriguez 风格

> **一个文件，四套规则。你用哪个模型，就用哪一段。**
> 编号 `033` ｜ 分类 02 霓虹黑色与赛博未来 ｜ 国籍 美国

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
纯黑底上血红泼洒与数码霓虹碰撞的漫画高反差世界中，罪城的暗影与阿丽塔的赛博大眼在墨黑与纯白的极端对比中燃烧着拉丁式的暴力美学。配色：主色 纯黑墨底 `#000000` 占 33%，辅色 罪城血红 `#CC0000` 占 18%、荒漠金褐 `#B8860B` 占 17%、高反差白 `#FFFFFF` 占 12%，点缀 数码霓虹粉 `#FF00FF` 占 10%、数码霓虹青 `#00FFFF` 占 10%。让主色占主导，其余按比例递减。光线：主光：极端硬光，高对比切割光，漫画式明暗分界，霓虹色光作为唯一光源；高光偏纯白/霓虹粉青（漫画高光/霓虹招牌/赛博光源）；阴影偏纯黑（几乎无细节的纯黑阴影，漫画墨色风格）；对比度：极端高对比（90-100%），黑白极致对比，选择性着色；整体：高反差漫画，70% 纯黑白 + 30% 选择性红/霓虹/金褐。运镜与构图：漫画分镜、高反差剪影、极端特写、低角度英雄、慢镜暴力、雨幕高对比、霓虹反光、黑白选色、速度线、墨西哥荒漠广角。色彩与光影：纯黑墨底、罪城血红、高反差白、数码霓虹粉、数码霓虹青、选择性着色、硬光切割、漫画光影、荒漠金褐、骨白惨色。氛围与情绪：漫画暴力、拉丁狂野、罪城黑暗、赛博朋克、B 级片趣味、反英雄、暴力美学、黑色幽默、墨西哥风情、数码酷感。
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
[总控] 30 秒 ｜ 竖版 9:16 ｜ 纯黑底上血红泼洒与数码霓虹碰撞的漫画高反差世界中，罪城的暗影与阿丽塔的赛博大眼在墨黑与纯白的极端对比中燃烧着拉丁式的暴力美学。 ｜ 单主角 ｜ 有对白 / 无对白
[参考素材职责] 见 2.2，只留这次真正用到的

[0–4 秒 镜头 S01]《罪恶之城》·雨中开篇：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[4–9 秒 镜头 S02]《阿丽塔：战斗天使》·钢铁城夜景：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[9–16 秒 镜头 S03]《阿丽塔》·机动铁球赛：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[16–30 秒 镜头 S04]《杀出个黎明》·沙漠公路：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。

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

#### 镜头 1：罪恶之城 · 雨中开篇

```text
【运镜】漫画分镜构图（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在雨中开篇里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《罪恶之城》的雨中开篇；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】纯黑底上血红泼洒与数码霓虹碰撞的漫画高反差世界中，罪城的暗影与阿丽塔的赛博大眼在墨黑与纯白的极端对比中燃烧着拉丁式的暴力美学。配色：主色 纯黑墨底 `#000000` 占 33%，辅色 罪城血红 `#CC0000` 占 18%、荒漠金褐 `#B8860B` 占 17%、高反差白 `#FFFFFF` 占 12%，点缀 数码霓虹粉 `#FF00FF` 占 10%、数码霓虹青 `#00FFFF` 占 10%。让主色占主导，其余按比例递减。光线：主光：极端硬光，高对比切割光，漫画式明暗分界，霓虹色光作为唯一光源；高光偏纯白/霓虹粉青（漫画高光/霓虹招牌/赛博光源）；阴影偏纯黑（几乎无细节的纯黑阴影，漫画墨色风格）；对比度：极端高对比（90-100%），黑白极致对比，选择性着色；整体：高反差漫画，70% 纯黑白 + 30% 选择性红/霓虹/金褐。运镜与构图：漫画分镜、高反差剪影、极端特写、低角度英雄、慢镜暴力、雨幕高对比、霓虹反光、黑白选色、速度线、墨西哥荒漠广角。色彩与光影：纯黑墨底、罪城血红、高反差白、数码霓虹粉、数码霓虹青、选择性着色、硬光切割、漫画光影、荒漠金褐、骨白惨色。氛围与情绪：漫画暴力、拉丁狂野、罪城黑暗、赛博朋克、B 级片趣味、反英雄、暴力美学、黑色幽默、墨西哥风情、数码酷感。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 2：阿丽塔：战斗天使 · 钢铁城夜景

```text
【运镜】高反差剪影（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在钢铁城夜景里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《阿丽塔：战斗天使》的钢铁城夜景；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】纯黑底上血红泼洒与数码霓虹碰撞的漫画高反差世界中，罪城的暗影与阿丽塔的赛博大眼在墨黑与纯白的极端对比中燃烧着拉丁式的暴力美学。配色：主色 纯黑墨底 `#000000` 占 33%，辅色 罪城血红 `#CC0000` 占 18%、荒漠金褐 `#B8860B` 占 17%、高反差白 `#FFFFFF` 占 12%，点缀 数码霓虹粉 `#FF00FF` 占 10%、数码霓虹青 `#00FFFF` 占 10%。让主色占主导，其余按比例递减。光线：主光：极端硬光，高对比切割光，漫画式明暗分界，霓虹色光作为唯一光源；高光偏纯白/霓虹粉青（漫画高光/霓虹招牌/赛博光源）；阴影偏纯黑（几乎无细节的纯黑阴影，漫画墨色风格）；对比度：极端高对比（90-100%），黑白极致对比，选择性着色；整体：高反差漫画，70% 纯黑白 + 30% 选择性红/霓虹/金褐。运镜与构图：漫画分镜、高反差剪影、极端特写、低角度英雄、慢镜暴力、雨幕高对比、霓虹反光、黑白选色、速度线、墨西哥荒漠广角。色彩与光影：纯黑墨底、罪城血红、高反差白、数码霓虹粉、数码霓虹青、选择性着色、硬光切割、漫画光影、荒漠金褐、骨白惨色。氛围与情绪：漫画暴力、拉丁狂野、罪城黑暗、赛博朋克、B 级片趣味、反英雄、暴力美学、黑色幽默、墨西哥风情、数码酷感。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 3：阿丽塔 · 机动铁球赛

```text
【运镜】极端暴力特写（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在机动铁球赛里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《阿丽塔》的机动铁球赛；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】纯黑底上血红泼洒与数码霓虹碰撞的漫画高反差世界中，罪城的暗影与阿丽塔的赛博大眼在墨黑与纯白的极端对比中燃烧着拉丁式的暴力美学。配色：主色 纯黑墨底 `#000000` 占 33%，辅色 罪城血红 `#CC0000` 占 18%、荒漠金褐 `#B8860B` 占 17%、高反差白 `#FFFFFF` 占 12%，点缀 数码霓虹粉 `#FF00FF` 占 10%、数码霓虹青 `#00FFFF` 占 10%。让主色占主导，其余按比例递减。光线：主光：极端硬光，高对比切割光，漫画式明暗分界，霓虹色光作为唯一光源；高光偏纯白/霓虹粉青（漫画高光/霓虹招牌/赛博光源）；阴影偏纯黑（几乎无细节的纯黑阴影，漫画墨色风格）；对比度：极端高对比（90-100%），黑白极致对比，选择性着色；整体：高反差漫画，70% 纯黑白 + 30% 选择性红/霓虹/金褐。运镜与构图：漫画分镜、高反差剪影、极端特写、低角度英雄、慢镜暴力、雨幕高对比、霓虹反光、黑白选色、速度线、墨西哥荒漠广角。色彩与光影：纯黑墨底、罪城血红、高反差白、数码霓虹粉、数码霓虹青、选择性着色、硬光切割、漫画光影、荒漠金褐、骨白惨色。氛围与情绪：漫画暴力、拉丁狂野、罪城黑暗、赛博朋克、B 级片趣味、反英雄、暴力美学、黑色幽默、墨西哥风情、数码酷感。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```


### 3.2 本导演可用的运镜（挑一个，别叠加）

- **漫画分镜构图** —— 直接引用漫画分格的构图方式（例：《罪恶之城》全片漫画式构图）
- **高反差剪影** —— 人物以纯黑剪影出现在亮背景前（例：《罪恶之城》雨中剪影）
- **极端暴力特写** —— 暴力瞬间的极端特写慢镜（例：《罪恶之城》马弗暴力场景）
- **低角度英雄** —— 低角度仰拍反英雄人物（例：《罪恶之城》哈提根/马弗出场）
- **慢镜暴力美学** —— 暴力动作的慢镜头美学化（例：《300 勇士》风格（罗德里格兹参与）/《罪恶之城》）
- **黑白选色** —— 黑白画面中仅保留某一色彩（通常红色）（例：《罪恶之城》红裙/红唇/血）

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
【核心创意】纯黑底上血红泼洒与数码霓虹碰撞的漫画高反差世界中，罪城的暗影与阿丽塔的赛博大眼在墨黑与纯白的极端对比中燃烧着拉丁式的暴力美学。
［主体］在雨中开篇。

【分段过程描述】
[0–4s] 开场：罪恶之城 式空间。［主体动作：缓慢抬手 / 微微低头 / 顺势坐下，写清幅度和速度］。
[4–8s] 中段：［主体动作承接上一拍，写惯性衔接］。
[8–12s] 收尾：［主体停住，画面定格在 纯黑墨底+高反差白+罪城血红 的调子上］。

【声音】
overall_soundscape：（环境声 + 物理声 + 有无对白）
non_diegetic_music：（配乐；不想要就写「无配乐」）

【结束状态】画面收在［想要的那一帧］。
```

> 提示词上限约 **7000 字符**，写长不是问题，**糊成一段不分层才是**。

---

## 五、Runway / Pika

## 二、场景镜头模板

### 镜头 1：罪城雨中行走（Rain Walk）

**提示词：**
```
A man in a trench coat walks through heavy rain on a dark city street,
Robert Rodriguez Sin City style,
extreme high contrast black and white,
pure black background with stark white street lights,
rain creates white vertical streaks against darkness,
his shoes splash in white puddles reflecting neon,
selective red color on a distant neon sign,
he walks with deliberate hard-boiled steps,
the camera follows him from behind at a distance,
comic book noir atmosphere, hard shadows,
graphic novel aesthetic, film grain,
16:9 aspect ratio, slow rear tracking shot
```

**镜头参数：**
- 时长：6-8秒
- 运镜：背面跟随（rear tracking follow）
- 节奏：缓慢，硬汉漫步

---

### 镜头 2：红裙女郎下楼梯（Femme Fatale）

**提示词：**
```
A beautiful woman in a flowing red dress descends a dark staircase,
Robert Rodriguez Sin City style,
everything is extreme black and white except her vivid red dress and red lips,
she is silhouetted against white light from above,
her dress flows and sways as she walks down,
pure black shadows surround her,
stark white rim light outlines her figure,
the camera looks up at her from below,
she pauses and looks directly at camera with a mysterious smile,
femme fatale, noir seduction,
comic book glamour, selective red color,
2.35:1 aspect ratio, low angle slow dolly
```

**镜头参数：**
- 时长：5-7秒
- 运镜：低角度仰拍慢推（low angle slow dolly up）
- 节奏：缓慢，致命诱惑

---

### 镜头 3：暴力出拳瞬间（Punch Impact）

**提示词：**
```
A fist connects with a jaw in slow motion,
Robert Rodriguez Sin City style,
extreme high contrast black and white,
selective bright red blood splatters outward in droplets,
the impact distorts the face in graphic detail,
white motion speed lines radiate from the impact point,
pure black background, stark white highlights on knuckles,
comic book impact frame, violent aesthetic,
blood droplets hang suspended in air,
the head snaps back from the force,
graphic novel violence, hard edge style,
16:9 aspect ratio, extreme slow motion impact
```

**镜头参数：**
- 时长：4-6秒
- 运镜：固定机位极慢镜（static extreme slow-motion）
- 节奏：极慢镜，暴力美学化

---

### 镜头 4：霓虹赛博街道（Neon Cyber Street）

**提示词：**
```
A crowded cyberpunk street at night with neon signs,
Robert Rodriguez Alita Battle Angel style,
neon magenta and cyan signs glow intensely,
holographic advertisements float in the dark air,
cyborgs and humans walk through the rain-slicked street,
neon reflects on wet pavement in magenta and cyan pools,
orange flame from street food stalls,
dark black sky above, no stars,
the camera moves slowly down the street at eye level,
mechanical limbs and cybernetic eyes visible on passersby,
digital cyberpunk aesthetic, high contrast neon,
16:9 aspect ratio, slow forward dolly through crowd
```

**镜头参数：**
- 时长：6-8秒
- 运镜：街道视线高度推进（eye-level dolly forward）
- 节奏：缓慢，赛博街道沉浸

---

### 镜头 5：机动铁球竞速（Motorball Race）

**提示词：**
```
Cyborgs racing on a circular track at high speed,
Robert Rodriguez Alita style,
cyborg warriors on roller blades fighting for a metal ball,
sparks fly from metal clashes,
orange fire and explosions,
neon magenta and cyan track lights,
the camera follows the racers at high speed,
mechanical limbs and weapons clash,
audience shadows in dark stands,
fast-paced cyberpunk sports action,
high contrast, digital neon glow,
intense kinetic energy,
2.35:1 cinemascope aspect ratio, high speed tracking
```

**镜头参数：**
- 时长：5-7秒
- 运镜：高速跟随（high-speed tracking）
- 节奏：极速，机械战斗

---

### 镜头 6：吸血鬼酒吧（Vampire Bar）

**提示词：**
```
Inside a Mexican bar at night, dark and smoky,
Robert Rodriguez From Dusk Till Dawn style,
red neon sign casts red light on everything,
amber warm light from the bar,
dusty floor, tequila bottles, mariachi music implied,
suddenly vampires reveal themselves in monstrous form,
green and red light flashes,
chaos erupts as attacks begin,
the camera is inside the chaos, slightly handheld,
dark shadows with pools of red and neon light,
B-movie horror action, latin grindhouse,
16:9 aspect ratio, chaotic handheld movement
```

**镜头参数：**
- 时长：5-7秒
- 运镜：手持混乱（chaotic handheld）
- 节奏：从静到爆，B级片狂欢

---

## 三、运镜关键词速查

| 运镜效果 | 英文关键词 |
|---------|-----------|
| 漫画分镜 | comic book panel composition, frame within frame, graphic novel layout |
| 高反差剪影 | silhouette against white, stark black outline, high contrast figure |
| 极端特写 | extreme close-up on impact, macro on fist/gun/eye, tight detail |
| 低角度英雄 | low angle heroic shot, looking up at tough character, imposing angle |
| 慢镜暴力 | slow-motion violence, blood droplets in air, impact frame, suspended motion |
| 雨幕高对比 | rain streaks against black, white rain on dark background, wet reflections |
| 霓虹穿行 | moving through neon-lit street, eye-level dolly, passing neon signs |
| 黑白选色 | selective color, only red in black and white, desaturated except accent |

---

## 四、颜色与光影关键词

| 效果 | 英文关键词 |
|------|-----------|
| 纯黑墨底 | pure ink black, absolute black shadows, deep black void, no detail in shadow |
| 罪城血红 | sin city red, blood red accent, selective red color, vivid red dress |
| 高反差白 | stark white highlight, pure white rim light, blown out white, hard white edge |
| 数码霓虹粉 | neon magenta, hot pink neon, electric magenta glow, fuchsia sign |
| 数码霓虹青 | neon cyan, electric cyan glow, cyan hologram, aqua neon reflection |
| 硬光切割 | hard edge shadow, sharp shadow line, cut-off lighting, noir hard light |
| 荒漠金褐 | desert golden brown, amber warm light, dusty ochre, sepia Mexico |
| 罪城黄 | sickly yellow, jaundiced yellow, unnatural yellow skin, yellow bastard |

---

## 五、负面描述（避免的效果）

```
soft lighting, diffused gentle light, romantic mood,
pastel colors, muted grey tones, low contrast,
natural daylight, bright sunny, cheerful,
CGI cartoon, 3d animation, pixar style,
slow contemplative art film, quiet subtle,
shaky cam overload, found footage,
superhero movie, big budget clean CGI,
historical period drama, costume drama
```

---

> 本文件由 `色卡主文档.md` 派生（运镜特征表 / 经典场景表 / 色板 / 光影），未新增事实。
> Seedance 2.5 段的结构规则来自本机技能库 `film-cinedance/references/seedance-25-prompt-format.md`。
> 图像提示词见 `midjourney_prompts.md` · `conversational_prompts.md`。
