# 视频提示词 — 普罗亚斯 Alex Proyas 风格

> **一个文件，四套规则。你用哪个模型，就用哪一段。**
> 编号 `036` ｜ 分类 02 霓虹黑色与赛博未来 ｜ 国籍 澳大利亚

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
哥特暗夜里永恒雨幕下的机械都市，黑紫蓝色调中复仇血红燃烧，漫画式黑色剪影构筑的存在主义黑暗寓言。配色：主色 哥特永夜黑 `#0A0A12` 占 35%，辅色 暗夜紫蓝 `#1E1A35` 占 22%、雨夜钢蓝 `#2C3A50` 占 15%、血色暗红 `#5C1A20` 占 12%，点缀 漫画银灰 `#8A8C98` 占 9%、冷白月光 `#C8CCD4` 占 7%。让主色占主导，其余按比例递减。光线：主光：低角度硬光+顶部闪电光，雨夜湿面反射，强烈明暗切割；高光偏冷白/银蓝（闪电、月光、机器人眼、屏幕光）；阴影偏深紫蓝偏黑（哥特暗夜、建筑阴影、永夜角落）；对比度：极高对比（80-95%），黑暗吞噬大部分画面；整体：极暗哥特，85% 冷黑紫蓝 + 15% 血红/暖金点缀。运镜与构图：荷兰角倾斜、哥特剪影、低角度仰拍、雨幕纵深感、漫画分格构图、德国表现主义建筑、镜像水面反射、十字架/墓碑构图、闪电瞬间定格、长阴影投射。色彩与光影：哥特暗黑、紫蓝雨幕、血红点缀、银白闪电、漫画高对比、湿面反光、机械冷银、烛金暖光、永恒黑夜、黑色剪影。氛围与情绪：哥特复仇、存在主义荒诞、永夜囚禁、死亡归来、机械冰冷、黑色漫画、命运宿命、超自然、都市哥特、反乌托邦孤独。
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
[总控] 30 秒 ｜ 竖版 9:16 ｜ 哥特暗夜里永恒雨幕下的机械都市，黑紫蓝色调中复仇血红燃烧，漫画式黑色剪影构筑的存在主义黑暗寓言。 ｜ 单主角 ｜ 有对白 / 无对白
[参考素材职责] 见 2.2，只留这次真正用到的

[0–4 秒 镜头 S01]《乌鸦》·屋顶吉他复仇：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[4–9 秒 镜头 S02]《黑暗城市》·城市调谐：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[9–16 秒 镜头 S03]《我，机器人》·隧道机器人叛变：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[16–30 秒 镜头 S04]《先知》·末日灾难：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。

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

#### 镜头 1：乌鸦 · 屋顶吉他复仇

```text
【运镜】荷兰角倾斜（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在屋顶吉他复仇里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《乌鸦》的屋顶吉他复仇；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】哥特暗夜里永恒雨幕下的机械都市，黑紫蓝色调中复仇血红燃烧，漫画式黑色剪影构筑的存在主义黑暗寓言。配色：主色 哥特永夜黑 `#0A0A12` 占 35%，辅色 暗夜紫蓝 `#1E1A35` 占 22%、雨夜钢蓝 `#2C3A50` 占 15%、血色暗红 `#5C1A20` 占 12%，点缀 漫画银灰 `#8A8C98` 占 9%、冷白月光 `#C8CCD4` 占 7%。让主色占主导，其余按比例递减。光线：主光：低角度硬光+顶部闪电光，雨夜湿面反射，强烈明暗切割；高光偏冷白/银蓝（闪电、月光、机器人眼、屏幕光）；阴影偏深紫蓝偏黑（哥特暗夜、建筑阴影、永夜角落）；对比度：极高对比（80-95%），黑暗吞噬大部分画面；整体：极暗哥特，85% 冷黑紫蓝 + 15% 血红/暖金点缀。运镜与构图：荷兰角倾斜、哥特剪影、低角度仰拍、雨幕纵深感、漫画分格构图、德国表现主义建筑、镜像水面反射、十字架/墓碑构图、闪电瞬间定格、长阴影投射。色彩与光影：哥特暗黑、紫蓝雨幕、血红点缀、银白闪电、漫画高对比、湿面反光、机械冷银、烛金暖光、永恒黑夜、黑色剪影。氛围与情绪：哥特复仇、存在主义荒诞、永夜囚禁、死亡归来、机械冰冷、黑色漫画、命运宿命、超自然、都市哥特、反乌托邦孤独。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 2：黑暗城市 · 城市调谐

```text
【运镜】哥特剪影构图（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在城市调谐里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《黑暗城市》的城市调谐；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】哥特暗夜里永恒雨幕下的机械都市，黑紫蓝色调中复仇血红燃烧，漫画式黑色剪影构筑的存在主义黑暗寓言。配色：主色 哥特永夜黑 `#0A0A12` 占 35%，辅色 暗夜紫蓝 `#1E1A35` 占 22%、雨夜钢蓝 `#2C3A50` 占 15%、血色暗红 `#5C1A20` 占 12%，点缀 漫画银灰 `#8A8C98` 占 9%、冷白月光 `#C8CCD4` 占 7%。让主色占主导，其余按比例递减。光线：主光：低角度硬光+顶部闪电光，雨夜湿面反射，强烈明暗切割；高光偏冷白/银蓝（闪电、月光、机器人眼、屏幕光）；阴影偏深紫蓝偏黑（哥特暗夜、建筑阴影、永夜角落）；对比度：极高对比（80-95%），黑暗吞噬大部分画面；整体：极暗哥特，85% 冷黑紫蓝 + 15% 血红/暖金点缀。运镜与构图：荷兰角倾斜、哥特剪影、低角度仰拍、雨幕纵深感、漫画分格构图、德国表现主义建筑、镜像水面反射、十字架/墓碑构图、闪电瞬间定格、长阴影投射。色彩与光影：哥特暗黑、紫蓝雨幕、血红点缀、银白闪电、漫画高对比、湿面反光、机械冷银、烛金暖光、永恒黑夜、黑色剪影。氛围与情绪：哥特复仇、存在主义荒诞、永夜囚禁、死亡归来、机械冰冷、黑色漫画、命运宿命、超自然、都市哥特、反乌托邦孤独。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 3：我，机器人 · 隧道机器人叛变

```text
【运镜】雨幕纵深推轨（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在隧道机器人叛变里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《我，机器人》的隧道机器人叛变；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】哥特暗夜里永恒雨幕下的机械都市，黑紫蓝色调中复仇血红燃烧，漫画式黑色剪影构筑的存在主义黑暗寓言。配色：主色 哥特永夜黑 `#0A0A12` 占 35%，辅色 暗夜紫蓝 `#1E1A35` 占 22%、雨夜钢蓝 `#2C3A50` 占 15%、血色暗红 `#5C1A20` 占 12%，点缀 漫画银灰 `#8A8C98` 占 9%、冷白月光 `#C8CCD4` 占 7%。让主色占主导，其余按比例递减。光线：主光：低角度硬光+顶部闪电光，雨夜湿面反射，强烈明暗切割；高光偏冷白/银蓝（闪电、月光、机器人眼、屏幕光）；阴影偏深紫蓝偏黑（哥特暗夜、建筑阴影、永夜角落）；对比度：极高对比（80-95%），黑暗吞噬大部分画面；整体：极暗哥特，85% 冷黑紫蓝 + 15% 血红/暖金点缀。运镜与构图：荷兰角倾斜、哥特剪影、低角度仰拍、雨幕纵深感、漫画分格构图、德国表现主义建筑、镜像水面反射、十字架/墓碑构图、闪电瞬间定格、长阴影投射。色彩与光影：哥特暗黑、紫蓝雨幕、血红点缀、银白闪电、漫画高对比、湿面反光、机械冷银、烛金暖光、永恒黑夜、黑色剪影。氛围与情绪：哥特复仇、存在主义荒诞、永夜囚禁、死亡归来、机械冰冷、黑色漫画、命运宿命、超自然、都市哥特、反乌托邦孤独。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```


### 3.2 本导演可用的运镜（挑一个，别叠加）

- **荷兰角倾斜** —— 倾斜构图营造不安与超现实（例：《乌鸦》复仇场景、《黑暗城市》调谐）
- **哥特剪影构图** —— 人物在窗前/闪电前的黑色剪影（例：《乌鸦》屋顶吉他剪影、《黑暗城市》陌生人剪影）
- **雨幕纵深推轨** —— 雨水在前景纵深层次，镜头推进（例：《乌鸦》雨夜街道穿行）
- **低角度仰拍建筑** —— 表现主义建筑压迫感，倾斜建筑（例：《黑暗城市》城市变形、建筑升起）
- **闪电瞬间定格** —— 闪电瞬间照亮一切的定格感（例：《乌鸦》闪电揭示、《我，机器人》隧道）
- **水面/湿面反射** —— 雨水路面倒影对称构图（例：《乌鸦》街道水洼反射、《黑暗城市》时钟倒影）

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
【核心创意】哥特暗夜里永恒雨幕下的机械都市，黑紫蓝色调中复仇血红燃烧，漫画式黑色剪影构筑的存在主义黑暗寓言。
［主体］在屋顶吉他复仇。

【分段过程描述】
[0–4s] 开场：乌鸦 式空间。［主体动作：缓慢抬手 / 微微低头 / 顺势坐下，写清幅度和速度］。
[4–8s] 中段：［主体动作承接上一拍，写惯性衔接］。
[8–12s] 收尾：［主体停住，画面定格在 哥特永夜黑+乌鸦血红+冷白闪电 的调子上］。

【声音】
overall_soundscape：（环境声 + 物理声 + 有无对白）
non_diegetic_music：（配乐；不想要就写「无配乐」）

【结束状态】画面收在［想要的那一帧］。
```

> 提示词上限约 **7000 字符**，写长不是问题，**糊成一段不分层才是**。

---

## 五、Runway / Pika

## 二、场景镜头模板

### 镜头 1：永夜城市建立镜头（Establishing Shot）

**提示词：**
```
Extreme high angle shot looking down at a vast gothic city in eternal night,
Alex Proyas Dark City style,
dark purple-blue sky with no stars or moon visible,
German expressionist skyscrapers with art deco details,
pouring rain falling on wet streets that reflect neon blue and blood red signs,
lightning flashes silently in the distance illuminating the skyline in cold white,
a giant clock tower shows midnight,
the buildings seem to subtly shift and morph,
no cars, no people, an empty dreamlike city,
gothic noir atmosphere, eternal night,
cinematic wide shot, slow crane down movement,
2.35:1 anamorphic aspect ratio, film grain
```

**镜头参数：**
- 时长：7-9秒
- 运镜：缓慢下降（crane down）
- 节奏：缓慢、梦境感、神秘

---

### 镜头 2：乌鸦屋顶剪影（Crow Rooftop Silhouette）

**提示词：**
```
A pale man in black leather stands on the edge of a gothic rooftop in pouring rain,
Alex Proyas The Crow style,
he holds an electric guitar, lightning flashes behind him creating a perfect silhouette,
a crow flies around him and lands on his shoulder,
rain pours down, water streams off his black coat,
his face painted white with black eyes, he looks up at the sky,
blood red bandana on his arm,
dutch angle tilted composition,
the gothic cathedral spires rise behind him,
dramatic revenge atmosphere, supernatural,
medium shot, slow push in toward him,
lightning flashes intermittently, 16:9 aspect ratio
```

**镜头参数：**
- 时长：6-8秒
- 运镜：缓慢推近+荷兰角倾斜
- 节奏：戏剧性、复仇燃感

---

### 镜头 3：雨街行走（Rain Walk）

**提示词：**
```
A man in a black trench coat and fedora walks slowly down a rain-soaked city street at night,
Alex Proyas Dark City style,
dark purple-blue night, neon signs reflecting on wet cobblestones,
he walks past art deco buildings that seem to lean and tilt at impossible angles,
his long shadow stretches before him cast by pale moonlight breaking through clouds,
rain falls steadily, puddles splash under his boots,
he pauses and looks up at the shifting buildings,
noir mystery, existential stranger,
tracking shot following him from behind,
wet surfaces shimmer, deep shadows,
cinematic film noir, 16:9 aspect ratio
```

**镜头参数：**
- 时长：7-9秒
- 运镜：跟拍（tracking shot from behind）
- 节奏：缓慢、神秘、黑色电影

---

### 镜头 4：墓地复活（Grave Resurrection）

**提示词：**
```
A muddy hand bursts out of a grave in a gothic cemetery during a storm,
Alex Proyas The Crow style,
lightning flashes illuminating crooked tombstones and iron crosses,
a pale man pulls himself out of the muddy grave,
rain pouring down washing mud off his white face,
his eyes open, dark and intense,
supernatural resurrection, return from death,
the camera circles slowly around him as he rises from the grave,
dark purple-blue sky, cold white lightning,
a single crow watches from a tombstone,
gothic horror, dramatic rebirth,
low angle circling shot, 16:9 aspect ratio
```

**镜头参数：**
- 时长：6-8秒
- 运镜：环绕（arc shot / circling）
- 节奏：慢→力量爆发

---

### 镜头 5：机器人隧道涌来（Robot Tunnel Swarm）

**提示词：**
```
Hundreds of sleek white robots pour through a dark highway tunnel,
Alex Proyas I Robot style,
the robots climb on walls, ceiling, and wrecked cars,
their eyes glowing cold white/blue,
red emergency lights flash rhythmically casting red pulses,
neon blue police lights reflecting on wet concrete,
a man runs toward camera looking back in terror,
cars are crashed and overturned, sparks fly,
mechanical swarm, dystopian future chaos,
handheld camera running backward with the protagonist,
fast paced action, intense,
cinematic sci-fi action, 16:9 aspect ratio
```

**镜头参数：**
- 时长：5-7秒
- 运镜：手持后撤跟拍（handheld running backward）
- 节奏：快速、紧张、压迫

---

### 镜头 6：闪电对决（Lightning Showdown）

**提示词：**
```
Two figures face each other on a gothic rooftop in a thunderstorm,
Alex Proyas The Crow style,
lightning flashes illuminating them in stark white silhouette,
one man in black leather with white face paint,
rain whipping horizontally between them,
gargoyles and spires frame the composition,
dark purple-blue sky churns with storm clouds,
a crow circles above in the lightning flashes,
they begin to walk toward each other,
final confrontation, gothic western standoff,
extreme wide shot, slow dolly forward,
dramatic tension, high contrast noir, 2.35:1 aspect ratio
```

**镜头参数：**
- 时长：6-8秒
- 运镜：缓慢推进（slow dolly forward）
- 节奏：对峙、慢→决战前

---

## 三、运镜关键词速查

| 运镜效果 | 英文关键词 |
|---------|-----------|
| 荷兰角倾斜 | dutch angle, tilted frame, canted camera, off-kilter |
| 剪影构图 | silhouette against lightning, backlit dark outline, shadow figure |
| 雨幕跟拍 | rain walk tracking, following through rain, wet street tracking |
| 闪电瞬间 | lightning flash reveal, strobe lightning, flash illumination |
| 低角度仰拍 | low angle looking up, imposing architecture shot, towering gothic |
| 环绕揭示 | circling shot, arc around subject, slow orbit reveal |
| 高空俯拍 | extreme high angle, bird's eye city, god's eye view |
| 手持紧张 | handheld chase, shaky cam tension, running backward shot |

---

## 四、颜色与光影关键词

| 效果 | 英文关键词 |
|------|-----------|
| 哥特暗黑 | deep black shadows, pitch black night, gothic darkness, inky blacks |
| 紫蓝夜色 | dark purple-blue night, indigo sky, violet shadows, midnight blue |
| 血红点缀 | blood red accents, crimson light, red neon glow, dark red highlights |
| 闪电冷白 | silver-white lightning, cold white flash, pale moonlight, stark white |
| 雨湿反射 | rain-soaked reflections, wet cobblestone mirror, puddle reflection |
| 霓虹雨蓝 | neon blue rain signs, electric blue reflection, cyan glow on wet streets |
| 哥特金 | candlelight gold, art deco gold warmth, antique amber light |
| 高对比 | extreme high contrast, chiaroscuro noir, hard shadows, graphic black |

---

## 五、负面描述（避免的效果）

```
bright daylight, sunny day, blue sky,
warm golden hour, romantic lighting, pastel colors,
comedy, cheerful mood, happy ending,
sleek modern future, apple store aesthetic, glossy CGI,
anime style, cartoon, pixar animation,
fast chaotic editing, music video style,
lush green forests, natural landscapes, daylight exteriors
```

---

> 本文件由 `色卡主文档.md` 派生（运镜特征表 / 经典场景表 / 色板 / 光影），未新增事实。
> Seedance 2.5 段的结构规则来自本机技能库 `film-cinedance/references/seedance-25-prompt-format.md`。
> 图像提示词见 `midjourney_prompts.md` · `conversational_prompts.md`。
