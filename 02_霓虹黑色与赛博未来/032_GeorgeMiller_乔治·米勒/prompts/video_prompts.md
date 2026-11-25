# 视频提示词 — 乔治·米勒 George Miller 风格

> **一个文件，四套规则。你用哪个模型，就用哪一段。**
> 编号 `032` ｜ 分类 02 霓虹黑色与赛博未来 ｜ 国籍 澳大利亚

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
高饱和橙黄沙漠中烈焰红与天空深蓝极端碰撞，废土美学在铬银战车与战妆白的狂乱追逐中燃烧成末日公路的视觉烈火。配色：主色 沙漠橙 `#E65100` 占 26%，辅色 废土深棕 `#3E2723` 占 18%、烈焰红 `#C62828` 占 15%、尘暴赭 `#8D6E2F` 占 15%，点缀 天空深蓝 `#0D47A1` 占 14%、铬银战妆 `#CFD8DC` 占 12%。让主色占主导，其余按比例递减。光线：主光：烈日顶光为主，硬光切割，火焰/爆炸作为动态光源，沙漠烈日形成极端明暗；高光偏火焰橙黄/铬银白（爆炸火光/金属反光/烈日高光）；阴影偏废土深棕/天空深蓝（暗部偏冷蓝/深棕，沙漠阴影极深）；对比度：极高对比（85-95%），橙黄与深蓝极端互补碰撞，饱和度极高；整体：高饱和暖废土，70% 暖橙红赭 + 30% 冷蓝铬白。运镜与构图：极速追车、低角度战车正面、爆炸中心帧、尘暴远景、人物群像正面、战车对冲、慢镜飞溅、广角畸变、手持颠簸、中心对称冲击。色彩与光影：沙漠橙黄、烈焰红、天空深蓝、铬银反光、尘暴赭、战妆白、火焰橙黄、硬光切割、极端互补、高饱和碰撞。氛围与情绪：废土狂热、速度暴力、末日公路、生存本能、战车崇拜、汽油文化、沙漠神话、狂暴美学、女性反抗、希望绿洲。
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
[总控] 30 秒 ｜ 竖版 9:16 ｜ 高饱和橙黄沙漠中烈焰红与天空深蓝极端碰撞，废土美学在铬银战车与战妆白的狂乱追逐中燃烧成末日公路的视觉烈火。 ｜ 单主角 ｜ 有对白 / 无对白
[参考素材职责] 见 2.2，只留这次真正用到的

[0–4 秒 镜头 S01]《疯狂的麦克斯4》·公路追逐开篇：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[4–9 秒 镜头 S02]《疯狂的麦克斯2》·公路战士追车：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[9–16 秒 镜头 S03]《疯狂的麦克斯1》·公路复仇：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[16–30 秒 镜头 S04]《快乐的大脚》·南极冰原：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。

[声音] 环境声：（照场景补）／对白：<写准确台词，不要写「说点什么」>／配乐：（不想要就写「无配乐」）

[场景特定限制] 动作模糊成团，糖果霓虹，无沙尘层次，无动机环绕和随机变焦，用统一滤镜替代色彩比例，光源和材质。
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

#### 镜头 1：疯狂的麦克斯4 · 公路追逐开篇

```text
【运镜】极速追车剪辑（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在公路追逐开篇里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《疯狂的麦克斯4》的公路追逐开篇；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】高饱和橙黄沙漠中烈焰红与天空深蓝极端碰撞，废土美学在铬银战车与战妆白的狂乱追逐中燃烧成末日公路的视觉烈火。配色：主色 沙漠橙 `#E65100` 占 26%，辅色 废土深棕 `#3E2723` 占 18%、烈焰红 `#C62828` 占 15%、尘暴赭 `#8D6E2F` 占 15%，点缀 天空深蓝 `#0D47A1` 占 14%、铬银战妆 `#CFD8DC` 占 12%。让主色占主导，其余按比例递减。光线：主光：烈日顶光为主，硬光切割，火焰/爆炸作为动态光源，沙漠烈日形成极端明暗；高光偏火焰橙黄/铬银白（爆炸火光/金属反光/烈日高光）；阴影偏废土深棕/天空深蓝（暗部偏冷蓝/深棕，沙漠阴影极深）；对比度：极高对比（85-95%），橙黄与深蓝极端互补碰撞，饱和度极高；整体：高饱和暖废土，70% 暖橙红赭 + 30% 冷蓝铬白。运镜与构图：极速追车、低角度战车正面、爆炸中心帧、尘暴远景、人物群像正面、战车对冲、慢镜飞溅、广角畸变、手持颠簸、中心对称冲击。色彩与光影：沙漠橙黄、烈焰红、天空深蓝、铬银反光、尘暴赭、战妆白、火焰橙黄、硬光切割、极端互补、高饱和碰撞。氛围与情绪：废土狂热、速度暴力、末日公路、生存本能、战车崇拜、汽油文化、沙漠神话、狂暴美学、女性反抗、希望绿洲。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 2：疯狂的麦克斯2 · 公路战士追车

```text
【运镜】低角度战车正面（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在公路战士追车里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《疯狂的麦克斯2》的公路战士追车；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】高饱和橙黄沙漠中烈焰红与天空深蓝极端碰撞，废土美学在铬银战车与战妆白的狂乱追逐中燃烧成末日公路的视觉烈火。配色：主色 沙漠橙 `#E65100` 占 26%，辅色 废土深棕 `#3E2723` 占 18%、烈焰红 `#C62828` 占 15%、尘暴赭 `#8D6E2F` 占 15%，点缀 天空深蓝 `#0D47A1` 占 14%、铬银战妆 `#CFD8DC` 占 12%。让主色占主导，其余按比例递减。光线：主光：烈日顶光为主，硬光切割，火焰/爆炸作为动态光源，沙漠烈日形成极端明暗；高光偏火焰橙黄/铬银白（爆炸火光/金属反光/烈日高光）；阴影偏废土深棕/天空深蓝（暗部偏冷蓝/深棕，沙漠阴影极深）；对比度：极高对比（85-95%），橙黄与深蓝极端互补碰撞，饱和度极高；整体：高饱和暖废土，70% 暖橙红赭 + 30% 冷蓝铬白。运镜与构图：极速追车、低角度战车正面、爆炸中心帧、尘暴远景、人物群像正面、战车对冲、慢镜飞溅、广角畸变、手持颠簸、中心对称冲击。色彩与光影：沙漠橙黄、烈焰红、天空深蓝、铬银反光、尘暴赭、战妆白、火焰橙黄、硬光切割、极端互补、高饱和碰撞。氛围与情绪：废土狂热、速度暴力、末日公路、生存本能、战车崇拜、汽油文化、沙漠神话、狂暴美学、女性反抗、希望绿洲。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 3：疯狂的麦克斯1 · 公路复仇

```text
【运镜】爆炸慢镜飞溅（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在公路复仇里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《疯狂的麦克斯1》的公路复仇；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】高饱和橙黄沙漠中烈焰红与天空深蓝极端碰撞，废土美学在铬银战车与战妆白的狂乱追逐中燃烧成末日公路的视觉烈火。配色：主色 沙漠橙 `#E65100` 占 26%，辅色 废土深棕 `#3E2723` 占 18%、烈焰红 `#C62828` 占 15%、尘暴赭 `#8D6E2F` 占 15%，点缀 天空深蓝 `#0D47A1` 占 14%、铬银战妆 `#CFD8DC` 占 12%。让主色占主导，其余按比例递减。光线：主光：烈日顶光为主，硬光切割，火焰/爆炸作为动态光源，沙漠烈日形成极端明暗；高光偏火焰橙黄/铬银白（爆炸火光/金属反光/烈日高光）；阴影偏废土深棕/天空深蓝（暗部偏冷蓝/深棕，沙漠阴影极深）；对比度：极高对比（85-95%），橙黄与深蓝极端互补碰撞，饱和度极高；整体：高饱和暖废土，70% 暖橙红赭 + 30% 冷蓝铬白。运镜与构图：极速追车、低角度战车正面、爆炸中心帧、尘暴远景、人物群像正面、战车对冲、慢镜飞溅、广角畸变、手持颠簸、中心对称冲击。色彩与光影：沙漠橙黄、烈焰红、天空深蓝、铬银反光、尘暴赭、战妆白、火焰橙黄、硬光切割、极端互补、高饱和碰撞。氛围与情绪：废土狂热、速度暴力、末日公路、生存本能、战车崇拜、汽油文化、沙漠神话、狂暴美学、女性反抗、希望绿洲。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```


### 3.2 本导演可用的运镜（挑一个，别叠加）

- **极速追车剪辑** —— 极快节奏的追车剪辑，速度线与尘土（例：《疯狂的麦克斯 4》全程公路追逐）
- **低角度战车正面** —— 极低角度正面拍摄战车冲来（例：《疯狂的麦克斯 4》战车对冲）
- **爆炸慢镜飞溅** —— 爆炸瞬间火焰/碎片/人体慢镜飞溅（例：《疯狂的麦克斯 4》油罐车爆炸）
- **尘暴远景** —— 巨大沙尘暴墙的末日远景（例：《疯狂的麦克斯 4》沙尘暴场景）
- **战妆正面群像** —— 战争男孩白妆正面冲锋（例：《疯狂的麦克斯 4》战争男孩冲锋）
- **车顶上动作** —— 战车上的人物动作与战斗（例：《疯狂的麦克斯 4》车顶上的弗瑞奥萨）

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
画面抖动，多余肢体，手指畸形，面部漂移，文字水印，物体变形，闪烁跳帧，重复物体，光线杂乱，动作模糊成团，糖果霓虹，无沙尘层次，无动机环绕和随机变焦，用统一滤镜替代色彩比例，光源和材质。
```

---

## 四、MiniMax H3（海螺）

H3 按时间戳写，不分镜头。**声音要单独成段**。

```text
【核心创意】高饱和橙黄沙漠中烈焰红与天空深蓝极端碰撞，废土美学在铬银战车与战妆白的狂乱追逐中燃烧成末日公路的视觉烈火。
［主体］在公路追逐开篇。

【分段过程描述】
[0–4s] 开场：疯狂的麦克斯4 式空间。［主体动作：缓慢抬手 / 微微低头 / 顺势坐下，写清幅度和速度］。
[4–8s] 中段：［主体动作承接上一拍，写惯性衔接］。
[8–12s] 收尾：［主体停住，画面定格在 沙漠橙+烈焰红+天空深蓝 的调子上］。

【声音】
overall_soundscape：（环境声 + 物理声 + 有无对白）
non_diegetic_music：（配乐；不想要就写「无配乐」）

【结束状态】画面收在［想要的那一帧］。
```

> 提示词上限约 **7000 字符**，写长不是问题，**糊成一段不分层才是**。

---

## 五、Runway / Pika

## 二、场景镜头模板

### 镜头 1：追车开篇（Chase Opening）

**提示词：**
```
Multiple customized war vehicles speeding across orange desert at high speed,
George Miller Mad Max Fury Road style,
the lead war rig charges forward, pursued by war parties,
flames shoot from vehicle exhausts,
orange dust trails behind each vehicle,
deep vivid blue sky contrasts with saturated orange desert,
warriors with white paint lean from vehicles,
the camera races alongside the chase at vehicle level,
sand and debris fly past the lens,
intense kinetic energy, non-stop action,
extreme high contrast orange vs blue,
cinematic 2.35:1 aspect ratio, high speed lateral tracking
```

**镜头参数：**
- 时长：5-7秒
- 运镜：高速侧跟（high-speed vehicle-level tracking）
- 节奏：极速，狂暴能量

---

### 镜头 2：战争男孩冲锋（War Boys Charge）

**提示词：**
```
War boys with white chalk paint screaming and leaping between speeding vehicles,
George Miller Mad Max style,
they swing on poles between trucks,
orange desert blurring past at high speed,
fire and explosions around them,
chrome spray paint in their mouths before battle,
deep blue sky overhead,
the camera follows a war boy as he leaps in slow motion,
dust and orange sand in the air,
frenzied religious ecstasy of combat,
kinetic chaotic action,
cinematic, high saturation, film grain,
2.35:1 aspect ratio, slow-motion leap with fast background
```

**镜头参数：**
- 时长：4-6秒
- 运镜：慢镜跟随跳跃（slow-motion follow leap）
- 节奏：慢镜人物+极速背景，狂热冲击

---

### 镜头 3：沙尘暴来袭（Sandstorm Approach）

**提示词：**
```
A massive wall of orange ochre dust storm towers across the desert,
George Miller Mad Max Fury Road style,
vehicles race toward the storm as it grows larger,
swirling orange and brown sand clouds,
dark indigo-blue sky above the storm,
lightning flickers within the dust wall,
tornado-like vortices of sand twist in the storm,
the camera pulls back to reveal the immense scale,
vehicles look tiny against the wall of dust,
apocalyptic natural fury,
cinematic wide shot, dramatic contrast, film grain,
2.35:1 aspect ratio, rapid pull-back to reveal scale
```

**镜头参数：**
- 时长：6-8秒
- 运镜：快速拉远揭示规模（rapid pull-back reveal）
- 节奏：渐强，自然之怒压迫

---

### 镜头 4：油罐爆炸（Tanker Explosion）

**提示词：**
```
A massive tanker truck explodes in the desert in slow motion,
George Miller Fury Road style,
a giant orange-yellow fireball expands outward,
metal debris and shrapnel fly in all directions,
the shockwave kicks up a wall of orange sand,
deep blue sky behind the fire creates extreme contrast,
silhouettes of other vehicles against the fireball,
a flaming figure is thrown through the air,
the explosion's light bathes everything in orange,
practical effects style explosion,
cinematic slow-motion, high speed photography look,
2.35:1 cinemascope aspect ratio
```

**镜头参数：**
- 时长：5-7秒
- 运镜：慢镜爆炸（slow-motion explosion）
- 节奏：慢镜，火焰冲击

---

### 镜头 5：弗瑞奥萨驾驶（Furiosa Driving）

**提示词：**
```
A fierce woman with short hair and mechanical arm drives a massive war rig,
George Miller Fury Road style,
her face is streaked with black war paint and dust,
intense determined eyes focused ahead,
she grips the massive chrome steering wheel,
orange desert rushes past the windshield,
fire glows in the side mirrors,
dust blows through the cab,
the camera is inside the cab looking at her,
shallow depth of field with action visible behind,
one determined driver against the wasteland,
cinematic medium close-up, film grain, high contrast,
16:9 aspect ratio, steady with vehicle vibration
```

**镜头参数：**
- 时长：5-7秒
- 运镜：车内固定+震动（in-vehicle static with vibration）
- 节奏：紧张专注，一人对抗荒原

---

### 镜头 6：战车集结（War Rig Gathering）

**提示词：**
```
Dozens of customized post-apocalyptic vehicles gathered in a desert canyon at dawn,
George Miller Mad Max style,
massive war rigs, spike-covered cars, flame-spewing hot rods,
warriors with white paint stand on vehicles,
orange canyon walls, golden dawn light,
deep blue sky above, dust in the air,
engines rev, flames spurt from exhaust pipes,
the camera slowly cranes up to reveal the full fleet,
a war party about to charge,
epic scale, dozens of machines ready for battle,
cinematic crane shot, film grain,
2.35:1 aspect ratio, slow crane up reveal
```

**镜头参数：**
- 时长：6-8秒
- 运镜：缓慢摇臂上升（slow crane up reveal）
- 节奏：缓慢蓄势，战前集结

---

## 三、运镜关键词速查

| 运镜效果 | 英文关键词 |
|---------|-----------|
| 高速追车 | high speed chase, vehicle-level tracking, racing alongside, pursuit |
| 慢镜爆炸 | slow-motion explosion, fireball expanding, debris flying, high speed photography |
| 低角度战车 | low angle vehicle shot, looking up at massive machine, imposing war rig |
| 广角畸变 | wide angle lens distortion, fisheye effect, edge distortion, extreme wide |
| 手持颠簸 | handheld camera, kinetic shaky cam, in-vehicle vibration, rough ride |
| 尘暴远景 | extreme wide storm shot, vast dust wall, apocalyptic scale panorama |
| 车内驾驶 | in-vehicle POV, driver close-up, through windshield, cab interior shot |
| 慢镜跳跃 | slow-motion leap, flying through air, suspended mid-action |

---

## 四、颜色与光影关键词

| 效果 | 英文关键词 |
|------|-----------|
| 沙漠橙黄 | saturated orange desert, blazing orange sand, ochre wasteland, orange-tinted air |
| 烈焰红 | blazing red fire, explosion orange-red, flame thrower, fire and blood red |
| 天空深蓝 | deep vivid blue sky, cobalt blue contrast, saturated blue, ultra blue sky |
| 铬银反光 | chrome reflection, polished metal gleam, silver specular highlight, shiny steel |
| 战妆白 | white war paint, chalk white skin, bone white, albino white warrior |
| 尘暴赭 | ochre dust storm, brown sand cloud, rust-colored haze, sepia dust |
| 火焰橙黄 | orange-yellow fireball, bright flame, explosion core, gasoline fire |
| 废土深棕 | dark brown shadows, oil-stained leather, rust brown, burnt umber |

---

## 五、负面描述（避免的效果）

```
green forests, lush nature, clean water, lakes,
futuristic clean sci-fi, sterile white spaceships,
soft focus, dreamy romantic, pastel colors,
slow contemplative art film, quiet stillness,
CGI cartoon, anime, video game graphics,
snow and ice, cold arctic, winter landscape,
shaky cam overload, found footage,
calm peaceful atmosphere, comedy tone
```

---

> 本文件由 `色卡主文档.md` 派生（运镜特征表 / 经典场景表 / 色板 / 光影），未新增事实。
> Seedance 2.5 段的结构规则来自本机技能库 `film-cinedance/references/seedance-25-prompt-format.md`。
> 图像提示词见 `midjourney_prompts.md` · `conversational_prompts.md`。
