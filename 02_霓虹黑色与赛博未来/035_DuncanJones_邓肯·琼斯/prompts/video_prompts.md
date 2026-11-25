# 视频提示词 — 邓肯·琼斯 Duncan Jones 风格

> **一个文件，四套规则。你用哪个模型，就用哪一段。**
> 编号 `035` ｜ 分类 02 霓虹黑色与赛博未来 ｜ 国籍 英国

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
低预算科幻冷调中的孤独灰蓝，时间循环的机械冰冷与记忆暖光在密闭空间中交织的存在主义寓言。配色：主色 月基深灰蓝 `#1A2535` 占 32%，辅色 冷金属灰 `#8A95A5` 占 20%、屏幕蓝光 `#3D6B99` 占 18%、警报暖橙 `#C46B2E` 占 12%，点缀 无菌白 `#D9D2C4` 占 10%、兽人绿棕 `#2E4A3A` 占 8%。让主色占主导，其余按比例递减。光线：主光：冷顶光+屏幕侧光，人工光源为主，极少自然光；高光偏冷蓝/屏幕蓝光（显示器、全息投影、仪表灯）；阴影偏深灰蓝偏黑（金属阴影、密闭空间角落、太空暗部）；对比度：中高对比（65-80%），冷蓝调中暖橙点缀；整体：冷调科幻，75% 冷蓝灰 + 25% 暖橙金点缀。运镜与构图：密闭空间构图、对称框架、反射镜像、舱门/通道纵深、监视器视角、缓慢推轨、机械重复、克隆对称、屏幕画框、孤独远景。色彩与光影：冷灰蓝基调、屏幕蓝光、无菌白、警报暖橙、金属质感、记忆暖金、工业冷光、霓虹全息、低饱和科幻、冷暖对峙。氛围与情绪：存在主义孤独、密闭压抑、身份追问、时间循环、人机温情、反乌托邦、记忆执念、工业冷感、人性微光、哲学科幻。
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
[总控] 30 秒 ｜ 竖版 9:16 ｜ 低预算科幻冷调中的孤独灰蓝，时间循环的机械冰冷与记忆暖光在密闭空间中交织的存在主义寓言。 ｜ 单主角 ｜ 有对白 / 无对白
[参考素材职责] 见 2.2，只留这次真正用到的

[0–4 秒 镜头 S01]《月球》·Sam发现克隆人：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[4–9 秒 镜头 S02]《源代码》·列车上反复醒来：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[9–16 秒 镜头 S03]《魔兽》·兽人营地：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[16–30 秒 镜头 S04]《静音》·未来柏林酒吧：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。

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

#### 镜头 1：月球 · Sam发现克隆人

```text
【运镜】密闭空间框中框（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在Sam发现克隆人里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《月球》的Sam发现克隆人；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】低预算科幻冷调中的孤独灰蓝，时间循环的机械冰冷与记忆暖光在密闭空间中交织的存在主义寓言。配色：主色 月基深灰蓝 `#1A2535` 占 32%，辅色 冷金属灰 `#8A95A5` 占 20%、屏幕蓝光 `#3D6B99` 占 18%、警报暖橙 `#C46B2E` 占 12%，点缀 无菌白 `#D9D2C4` 占 10%、兽人绿棕 `#2E4A3A` 占 8%。让主色占主导，其余按比例递减。光线：主光：冷顶光+屏幕侧光，人工光源为主，极少自然光；高光偏冷蓝/屏幕蓝光（显示器、全息投影、仪表灯）；阴影偏深灰蓝偏黑（金属阴影、密闭空间角落、太空暗部）；对比度：中高对比（65-80%），冷蓝调中暖橙点缀；整体：冷调科幻，75% 冷蓝灰 + 25% 暖橙金点缀。运镜与构图：密闭空间构图、对称框架、反射镜像、舱门/通道纵深、监视器视角、缓慢推轨、机械重复、克隆对称、屏幕画框、孤独远景。色彩与光影：冷灰蓝基调、屏幕蓝光、无菌白、警报暖橙、金属质感、记忆暖金、工业冷光、霓虹全息、低饱和科幻、冷暖对峙。氛围与情绪：存在主义孤独、密闭压抑、身份追问、时间循环、人机温情、反乌托邦、记忆执念、工业冷感、人性微光、哲学科幻。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 2：源代码 · 列车上反复醒来

```text
【运镜】反射镜像对称（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在列车上反复醒来里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《源代码》的列车上反复醒来；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】低预算科幻冷调中的孤独灰蓝，时间循环的机械冰冷与记忆暖光在密闭空间中交织的存在主义寓言。配色：主色 月基深灰蓝 `#1A2535` 占 32%，辅色 冷金属灰 `#8A95A5` 占 20%、屏幕蓝光 `#3D6B99` 占 18%、警报暖橙 `#C46B2E` 占 12%，点缀 无菌白 `#D9D2C4` 占 10%、兽人绿棕 `#2E4A3A` 占 8%。让主色占主导，其余按比例递减。光线：主光：冷顶光+屏幕侧光，人工光源为主，极少自然光；高光偏冷蓝/屏幕蓝光（显示器、全息投影、仪表灯）；阴影偏深灰蓝偏黑（金属阴影、密闭空间角落、太空暗部）；对比度：中高对比（65-80%），冷蓝调中暖橙点缀；整体：冷调科幻，75% 冷蓝灰 + 25% 暖橙金点缀。运镜与构图：密闭空间构图、对称框架、反射镜像、舱门/通道纵深、监视器视角、缓慢推轨、机械重复、克隆对称、屏幕画框、孤独远景。色彩与光影：冷灰蓝基调、屏幕蓝光、无菌白、警报暖橙、金属质感、记忆暖金、工业冷光、霓虹全息、低饱和科幻、冷暖对峙。氛围与情绪：存在主义孤独、密闭压抑、身份追问、时间循环、人机温情、反乌托邦、记忆执念、工业冷感、人性微光、哲学科幻。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 3：魔兽 · 兽人营地

```text
【运镜】监视器POV（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在兽人营地里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《魔兽》的兽人营地；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】低预算科幻冷调中的孤独灰蓝，时间循环的机械冰冷与记忆暖光在密闭空间中交织的存在主义寓言。配色：主色 月基深灰蓝 `#1A2535` 占 32%，辅色 冷金属灰 `#8A95A5` 占 20%、屏幕蓝光 `#3D6B99` 占 18%、警报暖橙 `#C46B2E` 占 12%，点缀 无菌白 `#D9D2C4` 占 10%、兽人绿棕 `#2E4A3A` 占 8%。让主色占主导，其余按比例递减。光线：主光：冷顶光+屏幕侧光，人工光源为主，极少自然光；高光偏冷蓝/屏幕蓝光（显示器、全息投影、仪表灯）；阴影偏深灰蓝偏黑（金属阴影、密闭空间角落、太空暗部）；对比度：中高对比（65-80%），冷蓝调中暖橙点缀；整体：冷调科幻，75% 冷蓝灰 + 25% 暖橙金点缀。运镜与构图：密闭空间构图、对称框架、反射镜像、舱门/通道纵深、监视器视角、缓慢推轨、机械重复、克隆对称、屏幕画框、孤独远景。色彩与光影：冷灰蓝基调、屏幕蓝光、无菌白、警报暖橙、金属质感、记忆暖金、工业冷光、霓虹全息、低饱和科幻、冷暖对峙。氛围与情绪：存在主义孤独、密闭压抑、身份追问、时间循环、人机温情、反乌托邦、记忆执念、工业冷感、人性微光、哲学科幻。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```


### 3.2 本导演可用的运镜（挑一个，别叠加）

- **密闭空间框中框** —— 利用舱门/走廊/屏幕构成多重框架（例：《月球》基地走廊、《源代码》列车车厢）
- **反射镜像对称** —— 玻璃/屏幕/面罩反射，暗示双重身份（例：《月球》Sam 与克隆人对视）
- **监视器POV** —— 监控摄像头视角，冰冷观察感（例：《月球》GERTY 视角、基地监控）
- **缓慢推轨特写** —— 缓慢推向演员面部，揭示情绪（例：《月球》Sam 发现真相的特写）
- **重复循环剪辑** —— 相同场景的微妙变化，暗示时间循环（例：《源代码》反复醒来的列车场景）
- **太空孤独远景** —— 极远景中人物渺小，宇宙空旷（例：《月球》表面作业、基地远景）

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
【核心创意】低预算科幻冷调中的孤独灰蓝，时间循环的机械冰冷与记忆暖光在密闭空间中交织的存在主义寓言。
［主体］在Sam发现克隆人。

【分段过程描述】
[0–4s] 开场：月球 式空间。［主体动作：缓慢抬手 / 微微低头 / 顺势坐下，写清幅度和速度］。
[4–8s] 中段：［主体动作承接上一拍，写惯性衔接］。
[8–12s] 收尾：［主体停住，画面定格在 月基深灰蓝+冷金属灰+屏幕蓝光 的调子上］。

【声音】
overall_soundscape：（环境声 + 物理声 + 有无对白）
non_diegetic_music：（配乐；不想要就写「无配乐」）

【结束状态】画面收在［想要的那一帧］。
```

> 提示词上限约 **7000 字符**，写长不是问题，**糊成一段不分层才是**。

---

## 五、Runway / Pika

## 二、场景镜头模板

### 镜头 1：基地走廊推进（Establishing Shot）

**提示词：**
```
Slow dolly shot down a narrow white corridor in a lunar base,
Duncan Jones Moon style,
sterile white metal walls with cool blue light strips along the floor,
warning orange lights pulsing rhythmically at the far end,
a lone man in a gray jumpsuit walking slowly away from camera,
his reflection faintly visible on polished metal surfaces,
the camera moves steadily forward creating confinement tension,
no sound except distant hum implied,
cool blue-gray color palette with warm orange accents,
cinematic wide shot, 16:9 aspect ratio, slow deliberate movement
```

**镜头参数：**
- 时长：6-8秒
- 运镜：缓慢推进（dolly in / tracking forward）
- 节奏：慢，压抑的孤独感

---

### 镜头 2：屏幕光映脸（Screen Glow Close-up）

**提示词：**
```
Extreme close-up of a man's face illuminated only by monitor screen glow,
Duncan Jones Moon style,
cool blue light flickering across his tired eyes and unshaven face,
sweat droplets catching the light on his forehead,
his eyes slowly shift as he reads something disturbing on screen,
behind him the room is dark except for a faint warm amber desk lamp,
the blue light pulses subtly suggesting data processing,
intimate and claustrophobic,
shallow depth of field, film grain,
16:9 aspect ratio, almost static camera with micro-movements
```

**镜头参数：**
- 时长：5-7秒
- 运镜：近乎静止，微幅呼吸感
- 节奏：极慢，情绪积累

---

### 镜头 3：克隆人反射（Clone Reflection Reveal）

**提示词：**
```
A man in a spacesuit stands looking at his reflection in a glass panel,
Duncan Jones Moon style,
in the reflection we see another identical version of himself standing behind him,
cool blue light from the base interior illuminates both figures,
the man slowly reaches up to touch the glass,
his reflection does the same but with a subtle delay,
identity crisis, existential horror dawning,
metallic surfaces, cold industrial setting,
medium shot, slow push in toward the reflection,
cinematic sci-fi, film grain, 16:9 aspect ratio
```

**镜头参数：**
- 时长：6-8秒
- 运镜：缓慢推近（slow push in）
- 节奏：慢→震惊揭示

---

### 镜头 4：列车醒来循环（Train Loop Wake）

**提示词：**
```
A man jolts awake in a commuter train seat, disoriented,
Duncan Jones Source Code style,
he looks around the cold blue-gray train carriage at other passengers,
everything seems normal but slightly off,
outside the window a bright orange explosion light flashes,
he freezes, then everything resets -- passengers reset positions,
the same woman across from him repeats her greeting,
time loop, d�ej�e vu, disorientation,
warm orange explosion light contrasts with cold blue interior,
medium shot, subtle handheld movement,
cinematic thriller, film grain, 16:9 aspect ratio
```

**镜头参数：**
- 时长：7-9秒
- 运镜：微幅手持晃动，快速切换暗示重置
- 节奏：困惑→爆炸→重置循环

---

### 镜头 5：全息界面浮现（Holographic Interface）

**提示词：**
```
A man in a dark capsule chamber surrounded by floating holographic blue screens,
Duncan Jones Source Code style,
transparent blue data displays materialize around him showing code and maps,
his face lit by the holographic blue glow,
warning red indicators flash on one screen,
he reaches out to touch a holographic element,
the screens ripple with light at his touch,
futuristic interface, virtual reality pod,
cool blue dominant with red warning accents,
close-up to medium shot, slow orbit camera,
cinematic sci-fi, film grain, 16:9 aspect ratio
```

**镜头参数：**
- 时长：5-7秒
- 运镜：微环绕（slow orbit / arc shot）
- 节奏：科技感，信息涌来

---

### 镜头 6：月球表面远景（Lunar Surface Wide）

**提示词：**
```
Extreme wide shot of a tiny figure in a spacesuit standing on the gray lunar surface,
Duncan Jones Moon style,
vast empty crater landscape stretching to the curved horizon,
Earth visible as a small blue marble in the black sky above,
the lunar base visible as a small cluster of white structures far away,
cool gray moon dust, deep black space, harsh sunlight casting long shadows,
complete isolation, existential smallness,
the figure slowly raises a hand toward Earth,
epic yet intimate loneliness,
cinematic extreme wide shot, slow pull back,
2.35:1 anamorphic aspect ratio, film grain
```

**镜头参数：**
- 时长：6-8秒
- 运镜：极慢拉远（slow pull back / crane up）
- 节奏：缓慢，史诗般的孤独

---

## 三、运镜关键词速查

| 运镜效果 | 英文关键词 |
|---------|-----------|
| 密闭空间推进 | slow dolly in, tracking shot through corridors, confined movement |
| 反射揭示 | reflection reveal, mirror shot, glass pane reflection |
| 屏幕光特写 | screen glow close-up, face illuminated by monitor, blue light on skin |
| 监视器视角 | security camera POV, fixed angle surveillance, monitor view |
| 循环重复 | repeating action, time loop reset, deja vu camera reset |
| 孤独远景 | extreme wide shot, tiny figure against vastness, isolation framing |
| 手持紧张感 | subtle handheld, shaky cam tension, documentary feel |
| 缓慢推轨 | slow tracking shot, creeping camera, deliberate movement |

---

## 四、颜色与光影关键词

| 效果 | 英文关键词 |
|------|-----------|
| 冷蓝基调 | cool blue-gray palette, steel blue tones, desaturated cold tones |
| 屏幕蓝光 | screen glow blue, monitor light cast, CRT flicker, hologram blue |
| 暖橙警报 | warm amber warning light, orange indicator pulse, alert glow |
| 无菌白 | sterile white walls, clinical white surfaces, clean industrial |
| 金属反射 | metallic reflections, polished steel, chrome surfaces, aluminum |
| 冷暖对峙 | cool and warm contrast, blue versus amber, cold interior warm accent |
| 太空黑 | deep space black, void darkness, absolute shadow corners |
| 胶片颗粒 | 35mm film grain, cinematic texture, grainy sci-fi look |

---

## 五、负面描述（避免的效果）

```
bright saturated colors, fantasy magic, lush planets,
clean utopian future, glossy CGI, blockbuster superhero look,
fast paced action editing, shaky cam overload,
daylight exterior scenes, green forests, natural sunlight,
romantic comedy tone, cheerful atmosphere,
star wars, star trek aesthetic, smooth plastic surfaces
```

---

> 本文件由 `色卡主文档.md` 派生（运镜特征表 / 经典场景表 / 色板 / 光影），未新增事实。
> Seedance 2.5 段的结构规则来自本机技能库 `film-cinedance/references/seedance-25-prompt-format.md`。
> 图像提示词见 `midjourney_prompts.md` · `conversational_prompts.md`。
