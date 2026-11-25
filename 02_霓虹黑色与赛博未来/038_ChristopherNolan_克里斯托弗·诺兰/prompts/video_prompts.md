# 视频提示词 — 诺兰 Christopher Nolan 风格

> **一个文件，四套规则。你用哪个模型，就用哪一段。**
> 编号 `038` ｜ 分类 02 霓虹黑色与赛博未来 ｜ 国籍 英/美

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
IMAX 巨幕下冷钢蓝与建筑灰构筑的暗色史诗，时间折叠的建筑感构图中，黑洞暖橙与记忆金是理性迷宫里唯一的情感坐标。配色：主色 `#0C1420` 占 30%，辅色 冷钢蓝 `#2A4060` 占 22%、建筑灰 `#6E7580` 占 16%、玉米金 `#C9A44C` 占 12%，点缀 暖棕木色 `#7A5C3E` 占 11%、虚空墨黑 `#060A10` 占 9%。让主色占主导，其余按比例递减。光线：主光：IMAX 大画幅硬光，自然光为主，建筑感定向光，极少散射；高光偏冷钢蓝/金（现实冷蓝 vs 梦境/记忆暖金，诺兰标志性冷暖二元）；阴影偏深蓝黑偏墨色（IMAX 暗部浓郁，纯黑死黑区域）；对比度：极高对比（75-90%），IMAX 画幅特有的大光比；整体：暗色史诗，65% 冷蓝灰 + 35% 暖金棕橙，现实冷 vs 梦境暖。运镜与构图：IMAX 巨幅构图、建筑感对称、透视纵深走廊、折叠城市、低角度仰拍、大远景人物渺小、实用特效实拍、旋转走廊、时间逆向运动、交叉蒙太奇。色彩与光影：IMAX 冷钢蓝、建筑混凝土灰、玉米金暖光、黑洞暖橙、梦境琥珀暖调、蝙蝠侠黑、时间灰白、实拍质感、大光比、冷暖二元对立。氛围与情绪：时间迷宫、存在主义、记忆执念、暗色史诗、理性与情感、道德困境、宏大叙事、智识悬疑、父爱/执念、诺兰式精密。
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
[总控] 30 秒 ｜ 竖版 9:16 ｜ IMAX 巨幕下冷钢蓝与建筑灰构筑的暗色史诗，时间折叠的建筑感构图中，黑洞暖橙与记忆金是理性迷宫里唯一的情感坐标。 ｜ 单主角 ｜ 有对白 / 无对白
[参考素材职责] 见 2.2，只留这次真正用到的

[0–4 秒 镜头 S01]《星际穿越》·玉米地追逐：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[4–9 秒 镜头 S02]《盗梦空间》·折叠巴黎：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[9–16 秒 镜头 S03]《黑暗骑士》·哥谭夜景：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[16–30 秒 镜头 S04]《敦刻尔克》·喷火式空战：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。

[声音] 环境声：（照场景补）／对白：<写准确台词，不要写「说点什么」>／配乐：（不想要就写「无配乐」）

[场景特定限制] 全局青橙，晃动动作，科幻霓虹泛滥，无动机环绕和随机变焦，用统一滤镜替代色彩比例，光源和材质。
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

#### 镜头 1：星际穿越 · 玉米地追逐

```text
【运镜】IMAX巨幅大远景（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在玉米地追逐里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《星际穿越》的玉米地追逐；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】IMAX 巨幕下冷钢蓝与建筑灰构筑的暗色史诗，时间折叠的建筑感构图中，黑洞暖橙与记忆金是理性迷宫里唯一的情感坐标。配色：主色 `#0C1420` 占 30%，辅色 冷钢蓝 `#2A4060` 占 22%、建筑灰 `#6E7580` 占 16%、玉米金 `#C9A44C` 占 12%，点缀 暖棕木色 `#7A5C3E` 占 11%、虚空墨黑 `#060A10` 占 9%。让主色占主导，其余按比例递减。光线：主光：IMAX 大画幅硬光，自然光为主，建筑感定向光，极少散射；高光偏冷钢蓝/金（现实冷蓝 vs 梦境/记忆暖金，诺兰标志性冷暖二元）；阴影偏深蓝黑偏墨色（IMAX 暗部浓郁，纯黑死黑区域）；对比度：极高对比（75-90%），IMAX 画幅特有的大光比；整体：暗色史诗，65% 冷蓝灰 + 35% 暖金棕橙，现实冷 vs 梦境暖。运镜与构图：IMAX 巨幅构图、建筑感对称、透视纵深走廊、折叠城市、低角度仰拍、大远景人物渺小、实用特效实拍、旋转走廊、时间逆向运动、交叉蒙太奇。色彩与光影：IMAX 冷钢蓝、建筑混凝土灰、玉米金暖光、黑洞暖橙、梦境琥珀暖调、蝙蝠侠黑、时间灰白、实拍质感、大光比、冷暖二元对立。氛围与情绪：时间迷宫、存在主义、记忆执念、暗色史诗、理性与情感、道德困境、宏大叙事、智识悬疑、父爱/执念、诺兰式精密。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 2：盗梦空间 · 折叠巴黎

```text
【运镜】建筑感对称构图（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在折叠巴黎里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《盗梦空间》的折叠巴黎；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】IMAX 巨幕下冷钢蓝与建筑灰构筑的暗色史诗，时间折叠的建筑感构图中，黑洞暖橙与记忆金是理性迷宫里唯一的情感坐标。配色：主色 `#0C1420` 占 30%，辅色 冷钢蓝 `#2A4060` 占 22%、建筑灰 `#6E7580` 占 16%、玉米金 `#C9A44C` 占 12%，点缀 暖棕木色 `#7A5C3E` 占 11%、虚空墨黑 `#060A10` 占 9%。让主色占主导，其余按比例递减。光线：主光：IMAX 大画幅硬光，自然光为主，建筑感定向光，极少散射；高光偏冷钢蓝/金（现实冷蓝 vs 梦境/记忆暖金，诺兰标志性冷暖二元）；阴影偏深蓝黑偏墨色（IMAX 暗部浓郁，纯黑死黑区域）；对比度：极高对比（75-90%），IMAX 画幅特有的大光比；整体：暗色史诗，65% 冷蓝灰 + 35% 暖金棕橙，现实冷 vs 梦境暖。运镜与构图：IMAX 巨幅构图、建筑感对称、透视纵深走廊、折叠城市、低角度仰拍、大远景人物渺小、实用特效实拍、旋转走廊、时间逆向运动、交叉蒙太奇。色彩与光影：IMAX 冷钢蓝、建筑混凝土灰、玉米金暖光、黑洞暖橙、梦境琥珀暖调、蝙蝠侠黑、时间灰白、实拍质感、大光比、冷暖二元对立。氛围与情绪：时间迷宫、存在主义、记忆执念、暗色史诗、理性与情感、道德困境、宏大叙事、智识悬疑、父爱/执念、诺兰式精密。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 3：黑暗骑士 · 哥谭夜景

```text
【运镜】旋转/折叠环境（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在哥谭夜景里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《黑暗骑士》的哥谭夜景；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】IMAX 巨幕下冷钢蓝与建筑灰构筑的暗色史诗，时间折叠的建筑感构图中，黑洞暖橙与记忆金是理性迷宫里唯一的情感坐标。配色：主色 `#0C1420` 占 30%，辅色 冷钢蓝 `#2A4060` 占 22%、建筑灰 `#6E7580` 占 16%、玉米金 `#C9A44C` 占 12%，点缀 暖棕木色 `#7A5C3E` 占 11%、虚空墨黑 `#060A10` 占 9%。让主色占主导，其余按比例递减。光线：主光：IMAX 大画幅硬光，自然光为主，建筑感定向光，极少散射；高光偏冷钢蓝/金（现实冷蓝 vs 梦境/记忆暖金，诺兰标志性冷暖二元）；阴影偏深蓝黑偏墨色（IMAX 暗部浓郁，纯黑死黑区域）；对比度：极高对比（75-90%），IMAX 画幅特有的大光比；整体：暗色史诗，65% 冷蓝灰 + 35% 暖金棕橙，现实冷 vs 梦境暖。运镜与构图：IMAX 巨幅构图、建筑感对称、透视纵深走廊、折叠城市、低角度仰拍、大远景人物渺小、实用特效实拍、旋转走廊、时间逆向运动、交叉蒙太奇。色彩与光影：IMAX 冷钢蓝、建筑混凝土灰、玉米金暖光、黑洞暖橙、梦境琥珀暖调、蝙蝠侠黑、时间灰白、实拍质感、大光比、冷暖二元对立。氛围与情绪：时间迷宫、存在主义、记忆执念、暗色史诗、理性与情感、道德困境、宏大叙事、智识悬疑、父爱/执念、诺兰式精密。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```


### 3.2 本导演可用的运镜（挑一个，别叠加）

- **IMAX巨幅大远景** —— 70mm IMAX 大画幅，人物在宏阔空间中渺小（例：《星际穿越》太空、《蝙蝠侠》哥谭全景）
- **建筑感对称构图** —— 几何精确的建筑对称，理性秩序感（例：《盗梦空间》折叠巴黎、《信条》建筑）
- **旋转/折叠环境** —— 实际搭建的旋转装置拍摄失重/折叠（例：《盗梦空间》旋转走廊、折叠城市）
- **低角度仰拍英雄** —— 英雄人物的雕塑感低角度（例：《蝙蝠侠》蝙蝠侠登场、《星际穿越》宇航员）
- **时间逆向运动** —— 正向与逆向动作同时呈现（例：《信条》逆时间战斗、倒放爆炸）
- **交叉蒙太奇** —— 多线叙事平行剪辑，时间层交织（例：《盗梦空间》多层梦境、《敦刻尔克》三线）

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
画面抖动，多余肢体，手指畸形，面部漂移，文字水印，物体变形，闪烁跳帧，重复物体，光线杂乱，全局青橙，晃动动作，科幻霓虹泛滥，无动机环绕和随机变焦，用统一滤镜替代色彩比例，光源和材质。
```

---

## 四、MiniMax H3（海螺）

H3 按时间戳写，不分镜头。**声音要单独成段**。

```text
【核心创意】IMAX 巨幕下冷钢蓝与建筑灰构筑的暗色史诗，时间折叠的建筑感构图中，黑洞暖橙与记忆金是理性迷宫里唯一的情感坐标。
［主体］在玉米地追逐。

【分段过程描述】
[0–4s] 开场：星际穿越 式空间。［主体动作：缓慢抬手 / 微微低头 / 顺势坐下，写清幅度和速度］。
[4–8s] 中段：［主体动作承接上一拍，写惯性衔接］。
[8–12s] 收尾：［主体停住，画面定格在 玉米金+尘土灰+蓝天 的调子上］。

【声音】
overall_soundscape：（环境声 + 物理声 + 有无对白）
non_diegetic_music：（配乐；不想要就写「无配乐」）

【结束状态】画面收在［想要的那一帧］。
```

> 提示词上限约 **7000 字符**，写长不是问题，**糊成一段不分层才是**。

---

## 五、Runway / Pika

## 二、场景镜头模板

### 镜头 1：IMAX太空建立（Space Establishing）

**提示词：**
```
Vast IMAX shot of a spacecraft silently drifting through deep space,
Christopher Nolan Interstellar style,
endless deep blue-black void with distant pinprick stars,
the spacecraft is small against the cosmic scale,
Saturn visible in the distance with its rings glowing faintly,
cold blue-white light from a distant star illuminates the ship,
absolute silence and isolation,
the camera slowly pans revealing the immensity,
70mm IMAX film texture, deep black shadows,
cold steel blue palette with warmth from ship windows,
monumental cosmic scale, existential awe,
2.35:1 anamorphic aspect ratio, extremely slow camera movement
```

**镜头参数：**
- 时长：8-10秒
- 运镜：极慢横摇（extremely slow pan）
- 节奏：极慢、宏大、敬畏

---

### 镜头 2：折叠城市（Folding City）

**提示词：**
```
A wide shot of a Parisian street as the entire city begins to fold upward,
Christopher Nolan Inception style,
buildings and streets curve and bend overhead creating an impossible geometric arch,
concrete and stone architecture bending like paper,
cold steel blue sky above, warm amber light from cafe windows,
a lone man in a dark suit stands in the street watching,
debris floats in the gravity-defying space,
practical effects aesthetic, realistic physics,
the folding happens slowly and majestically,
geometric precision, mind-bending architecture,
IMAX cinematic shot, slow tilt up following the fold,
16:9 aspect ratio, high contrast film look
```

**镜头参数：**
- 时长：7-9秒
- 运镜：缓慢上摇（slow tilt up）
- 节奏：慢→震撼揭示

---

### 镜头 3：旋转走廊打斗（Rotating Hallway Fight）

**提示词：**
```
Two men fighting in a rotating hotel hallway,
Christopher Nolan Inception style,
the entire corridor slowly rotates around them causing them to slide and fall,
practical rotating set, no CGI,
warm amber wood paneling on walls, cold blue light from windows,
one man in a suit, the other in tactical gear,
gravity shifts as the hallway turns,
furniture slides across the room,
zero-gravity combat, disorienting,
long take following the action as the world turns,
high contrast lighting, deep shadows,
practical effects cinema, 16:9 aspect ratio
```

**镜头参数：**
- 时长：6-8秒
- 运镜：长镜头跟随旋转（long take rotating with set）
- 节奏：紧张、失重、动作

---

### 镜头 4：哥谭暗夜骑士降临（Dark Knight Rooftop）

**提示词：**
```
A dark caped figure perches on the edge of a Gotham skyscraper at night,
Christopher Nolan The Dark Knight style,
rain pours down, wind blows his cape dramatically,
he looks down at the city below,
cold steel blue city lights stretch to the horizon,
police searchlights sweep the sky including a bat-signal on the clouds,
lightning flashes briefly illuminating the dark figure,
he steps off the edge and glides down into the city,
low angle shot looking up, then following him down,
dark gothic architecture, grounded realism,
IMAX dark epic, deep blacks, rain-slick reflections,
2.35:1 aspect ratio, dramatic and heroic
```

**镜头参数：**
- 时长：6-8秒
- 运镜：低角度→跟随俯冲（low angle to follow glide）
- 节奏：戏剧性、英雄、暗黑史诗

---

### 镜头 5：时间逆向战斗（Time Reverse Fight）

**提示词：**
```
A fight scene where one fighter moves forward in time while the other moves in reverse,
Christopher Nolan Tenet style,
a building explodes in reverse -- debris flying back together,
window glass reassembling from shards,
one character moves normally, the other moves backward,
muzzle flashes suck inward instead of bursting out,
cold gray-blue palette of the opera house/freeport,
practical reverse photography effects,
staccato rhythmic action,
time flows in two directions simultaneously,
intellectual action cinema, disorienting yet precise,
medium wide shot, 16:9 aspect ratio
```

**镜头参数：**
- 时长：5-7秒
- 运镜：固定/微幅手持，逆向动作
- 节奏：智识化动作、时间悖论

---

### 镜头 6：核爆火球升起（Nuclear Fireball Rise）

**提示词：**
```
Extreme wide shot of the Trinity nuclear test explosion,
Christopher Nolan Oppenheimer style,
a blinding white fireball rises from the New Mexico desert floor,
orange and yellow flames expanding outward in a perfect sphere,
the shockwave ripples across the desert sand,
scientists in silhouette watch from a bunker miles away,
the fire illuminates their faces in bright orange light,
then the shockwave hits with visible force,
terrifying sublime beauty, apocalyptic power,
practical explosion, IMAX black and white to color shift,
extreme contrast, bright white core to deep shadows,
70mm IMAX, 2.35:1 aspect ratio
```

**镜头参数：**
- 时长：7-9秒
- 运镜：固定远景（static wide shot）→冲击波震动
- 节奏：寂静→爆发→震撼

---

## 三、运镜关键词速查

| 运镜效果 | 英文关键词 |
|---------|-----------|
| IMAX巨幅远景 | IMAX extreme wide shot, vast scale, monumental framing |
| 建筑几何对称 | geometric symmetry, architectural composition, precise framing |
| 缓慢推轨 | slow dolly push, deliberate camera movement, creeping forward |
| 低角度英雄 | low angle heroic shot, looking up at imposing figure |
| 交叉蒙太奇 | cross-cutting between scenes, parallel action, intercutting |
| 实拍长镜头 | long take, practical effects shot, continuous camera |
| 旋转跟拍 | rotating camera following action, spinning corridor |
| 时间逆向 | reverse motion photography, time inversion, backward action |

---

## 四、颜色与光影关键词

| 效果 | 英文关键词 |
|------|-----------|
| 冷钢蓝现实 | cold steel blue, corporate blue-gray, cool blue reality |
| 暖琥珀梦境 | warm amber light, golden dream tones, nostalgic warmth |
| IMAX深邃黑 | deep black shadows, rich dark tones, IMAX contrast |
| 建筑灰 | architectural gray, concrete tones, stone and steel |
| 玉米金 | golden cornfield light, wheat gold, warm earth tones |
| 黑洞橙 | black hole warm orange, tesseract glow, fiery orange light |
| 蝙蝠侠黑 | dark knight black, gothic shadow, vigilante darkness |
| 70mm胶片 | 70mm film grain, large format texture, IMAX film look |

---

## 五、负面描述（避免的效果）

```
CGI overload, cartoon comic book style, marvel superhero look,
bright saturated colors, fantasy magic, fast cgi cuts,
shaky cam overload, music video style editing,
anime, pixar, cartoon animation,
flat lighting, low contrast, bright overexposed image,
sleek futuristic utopia, apple store aesthetic,
romantic comedy, warm cozy lighting, handheld documentary feel,
romantic golden hour beauty, lens flare overload
```

---

> 本文件由 `色卡主文档.md` 派生（运镜特征表 / 经典场景表 / 色板 / 光影），未新增事实。
> Seedance 2.5 段的结构规则来自本机技能库 `film-cinedance/references/seedance-25-prompt-format.md`。
> 图像提示词见 `midjourney_prompts.md` · `conversational_prompts.md`。
