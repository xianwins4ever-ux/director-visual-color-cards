# 视频提示词 — 亚历克斯·加兰 Alex Garland 风格

> **一个文件，四套规则。你用哪个模型，就用哪一段。**
> 编号 `030` ｜ 分类 02 霓虹黑色与赛博未来 ｜ 国籍 英国

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
极简净白空间中自然绿的异变与冷钢蓝的凝视交织，克制镜头下 AI 意识觉醒与人体恐怖在幽冷光线中悄然绽放。配色：主色 极简净白 `#F5F5F0` 占 25%，辅色 深林绿 `#2E5339` 占 20%、冷钢蓝灰 `#546E7A` 占 18%、素肤暖 `#E8D5C4` 占 15%，点缀 虹彩粉紫 `#CE93D8` 占 12%、警示血红 `#C62828` 占 10%。让主色占主导，其余按比例递减。光线：主光：大面积柔光/自然光为主，大窗漫射光，森林中斑驳光线，冷白荧光；高光偏冷白/虹彩粉紫（玻璃反射/闪光虹彩/科技冷光）；阴影偏深林绿/冷钢蓝灰（森林暗部/建筑阴影/科技冷调）；对比度：中低对比（50-65%），柔和但冷峻，大量中间调；整体：冷净极简，60% 冷白绿蓝 + 40% 暖肤/虹彩。运镜与构图：对称构图、框中框透视、走廊纵深、玻璃反射、极简空间、自然入侵构图、镜面人像、远景孤立人物、缓慢推进、静态凝视。色彩与光影：极简净白、深林绿、冷钢蓝灰、虹彩粉紫、玻璃透光、自然漫射光、荧光冷白、变异虹光、血红点缀、柔影过渡。氛围与情绪：AI 意识觉醒、克制冷静、身体恐怖、自然异变、存在不安、性别权力、幽闭恐惧、超自然神秘、智性惊悚、人何以为人。
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
[总控] 30 秒 ｜ 竖版 9:16 ｜ 极简净白空间中自然绿的异变与冷钢蓝的凝视交织，克制镜头下 AI 意识觉醒与人体恐怖在幽冷光线中悄然绽放。 ｜ 单主角 ｜ 有对白 / 无对白
[参考素材职责] 见 2.2，只留这次真正用到的

[0–4 秒 镜头 S01]《机械姬》·艾娃面试房间：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[4–9 秒 镜头 S02]《湮灭》·进入闪光X区域：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[9–16 秒 镜头 S03]《男人》·英国乡村绿隧道：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[16–30 秒 镜头 S04]《内战/开发者》·科技空间/乡村：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。

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

#### 镜头 1：机械姬 · 艾娃面试房间

```text
【运镜】对称框中框（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在艾娃面试房间里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《机械姬》的艾娃面试房间；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】极简净白空间中自然绿的异变与冷钢蓝的凝视交织，克制镜头下 AI 意识觉醒与人体恐怖在幽冷光线中悄然绽放。配色：主色 极简净白 `#F5F5F0` 占 25%，辅色 深林绿 `#2E5339` 占 20%、冷钢蓝灰 `#546E7A` 占 18%、素肤暖 `#E8D5C4` 占 15%，点缀 虹彩粉紫 `#CE93D8` 占 12%、警示血红 `#C62828` 占 10%。让主色占主导，其余按比例递减。光线：主光：大面积柔光/自然光为主，大窗漫射光，森林中斑驳光线，冷白荧光；高光偏冷白/虹彩粉紫（玻璃反射/闪光虹彩/科技冷光）；阴影偏深林绿/冷钢蓝灰（森林暗部/建筑阴影/科技冷调）；对比度：中低对比（50-65%），柔和但冷峻，大量中间调；整体：冷净极简，60% 冷白绿蓝 + 40% 暖肤/虹彩。运镜与构图：对称构图、框中框透视、走廊纵深、玻璃反射、极简空间、自然入侵构图、镜面人像、远景孤立人物、缓慢推进、静态凝视。色彩与光影：极简净白、深林绿、冷钢蓝灰、虹彩粉紫、玻璃透光、自然漫射光、荧光冷白、变异虹光、血红点缀、柔影过渡。氛围与情绪：AI 意识觉醒、克制冷静、身体恐怖、自然异变、存在不安、性别权力、幽闭恐惧、超自然神秘、智性惊悚、人何以为人。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 2：湮灭 · 进入闪光X区域

```text
【运镜】镜面玻璃反射（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在进入闪光X区域里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《湮灭》的进入闪光X区域；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】极简净白空间中自然绿的异变与冷钢蓝的凝视交织，克制镜头下 AI 意识觉醒与人体恐怖在幽冷光线中悄然绽放。配色：主色 极简净白 `#F5F5F0` 占 25%，辅色 深林绿 `#2E5339` 占 20%、冷钢蓝灰 `#546E7A` 占 18%、素肤暖 `#E8D5C4` 占 15%，点缀 虹彩粉紫 `#CE93D8` 占 12%、警示血红 `#C62828` 占 10%。让主色占主导，其余按比例递减。光线：主光：大面积柔光/自然光为主，大窗漫射光，森林中斑驳光线，冷白荧光；高光偏冷白/虹彩粉紫（玻璃反射/闪光虹彩/科技冷光）；阴影偏深林绿/冷钢蓝灰（森林暗部/建筑阴影/科技冷调）；对比度：中低对比（50-65%），柔和但冷峻，大量中间调；整体：冷净极简，60% 冷白绿蓝 + 40% 暖肤/虹彩。运镜与构图：对称构图、框中框透视、走廊纵深、玻璃反射、极简空间、自然入侵构图、镜面人像、远景孤立人物、缓慢推进、静态凝视。色彩与光影：极简净白、深林绿、冷钢蓝灰、虹彩粉紫、玻璃透光、自然漫射光、荧光冷白、变异虹光、血红点缀、柔影过渡。氛围与情绪：AI 意识觉醒、克制冷静、身体恐怖、自然异变、存在不安、性别权力、幽闭恐惧、超自然神秘、智性惊悚、人何以为人。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 3：男人 · 英国乡村绿隧道

```text
【运镜】缓慢推近凝视（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在英国乡村绿隧道里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《男人》的英国乡村绿隧道；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】极简净白空间中自然绿的异变与冷钢蓝的凝视交织，克制镜头下 AI 意识觉醒与人体恐怖在幽冷光线中悄然绽放。配色：主色 极简净白 `#F5F5F0` 占 25%，辅色 深林绿 `#2E5339` 占 20%、冷钢蓝灰 `#546E7A` 占 18%、素肤暖 `#E8D5C4` 占 15%，点缀 虹彩粉紫 `#CE93D8` 占 12%、警示血红 `#C62828` 占 10%。让主色占主导，其余按比例递减。光线：主光：大面积柔光/自然光为主，大窗漫射光，森林中斑驳光线，冷白荧光；高光偏冷白/虹彩粉紫（玻璃反射/闪光虹彩/科技冷光）；阴影偏深林绿/冷钢蓝灰（森林暗部/建筑阴影/科技冷调）；对比度：中低对比（50-65%），柔和但冷峻，大量中间调；整体：冷净极简，60% 冷白绿蓝 + 40% 暖肤/虹彩。运镜与构图：对称构图、框中框透视、走廊纵深、玻璃反射、极简空间、自然入侵构图、镜面人像、远景孤立人物、缓慢推进、静态凝视。色彩与光影：极简净白、深林绿、冷钢蓝灰、虹彩粉紫、玻璃透光、自然漫射光、荧光冷白、变异虹光、血红点缀、柔影过渡。氛围与情绪：AI 意识觉醒、克制冷静、身体恐怖、自然异变、存在不安、性别权力、幽闭恐惧、超自然神秘、智性惊悚、人何以为人。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```


### 3.2 本导演可用的运镜（挑一个，别叠加）

- **对称框中框** —— 严格对称构图，门框/窗框形成画中画（例：《机械姬》纳森实验室走廊）
- **镜面玻璃反射** —— 通过玻璃/镜面呈现人物与 AI 的双重影像（例：《机械姬》艾娃在玻璃房间中）
- **缓慢推近凝视** —— 极缓慢推进，制造不安和审视感（例：《机械姬》艾娃面试 sessions）
- **自然远景孤立** —— 广阔自然中人物渺小孤立（例：《湮灭》X 区域入口远景）
- **走廊纵深推进** —— 沿走廊/通道缓慢推进，压迫与未知（例：《机械姬》地下设施走廊）
- **变异生物特写** —— 变异动植物/人体异变的冷静特写（例：《湮灭》熊/鹿/花人变异）

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
【核心创意】极简净白空间中自然绿的异变与冷钢蓝的凝视交织，克制镜头下 AI 意识觉醒与人体恐怖在幽冷光线中悄然绽放。
［主体］在艾娃面试房间。

【分段过程描述】
[0–4s] 开场：机械姬 式空间。［主体动作：缓慢抬手 / 微微低头 / 顺势坐下，写清幅度和速度］。
[4–8s] 中段：［主体动作承接上一拍，写惯性衔接］。
[8–12s] 收尾：［主体停住，画面定格在 极简净白+冷钢蓝灰+素肤暖 的调子上］。

【声音】
overall_soundscape：（环境声 + 物理声 + 有无对白）
non_diegetic_music：（配乐；不想要就写「无配乐」）

【结束状态】画面收在［想要的那一帧］。
```

> 提示词上限约 **7000 字符**，写长不是问题，**糊成一段不分层才是**。

---

## 五、Runway / Pika

## 二、场景镜头模板

### 镜头 1：设施走廊推进（Corridor Push-In）

**提示词：**
```
Slow dolly shot down a minimalist concrete and glass corridor,
Alex Garland Ex Machina style,
perfect symmetrical perspective, sterile white walls,
cold steel blue-grey glass panels on one side,
soft diffused light from hidden sources,
the camera moves slowly forward,
glass reflections create recursive images,
at the far end a figure stands motionless in white,
empty, silent, oppressive modernist space,
the feeling of being watched and tested,
cold intellectual dread,
cinematic film grain, 16:9 aspect ratio,
very slow deliberate forward movement
```

**镜头参数：**
- 时长：7-9秒
- 运镜：极慢推进（very slow dolly in）
- 节奏：极慢，幽闭压迫感

---

### 镜头 2：AI凝视（AI Gaze）

**提示词：**
```
Close-up of a young woman's face behind glass,
Alex Garland Ex Machina style,
she sits perfectly still, looking directly at the camera,
her expression is calm, intelligent, almost imperceptible smile,
soft white light illuminates her face evenly,
cold blue-grey reflections from the glass,
her eyes seem to see through everything,
the glass between her and the camera is a barrier,
the camera very slowly pushes in closer to her face,
her expression doesn't change, but her eyes seem to gain awareness,
quiet tension, Turing test unease,
cinematic close-up, film grain, cool tones,
16:9 aspect ratio, extremely slow push-in
```

**镜头参数：**
- 时长：6-8秒
- 运镜：极慢面部推进（extreme slow close-up push-in）
- 节奏：极慢，智性审视感

---

### 镜头 3：进入闪光（Entering the Shimmer）

**提示词：**
```
A woman walks toward a translucent shimmering wall of color in a forest,
Alex Garland Annihilation style,
deep green forest on one side, iridescent pink-purple light on the other,
the shimmer barrier refracts light like oil on water,
as she approaches, the air bends and colors shift,
prismatic rainbows appear in the air around her,
she reaches out her hand to touch the barrier,
her hand begins to shimmer and refract,
soft diffused otherworldly light,
beautiful and terrifying, the threshold of mutation,
cinematic wide shot to medium, film grain,
16:9 aspect ratio, slow forward walk
```

**镜头参数：**
- 时长：6-8秒
- 运镜：跟随前进（follow forward）
- 节奏：缓慢，美丽与恐惧并存

---

### 镜头 4：变异鹿（Mutant Deer）

**提示词：**
```
A deer with flowering crystalline antlers stands in a forest clearing,
Alex Garland Annihilation style,
its fur shimmers with iridescent pink-purple and green,
flowers grow from its antlers like coral branches,
the air around it refracts light creating prismatic halos,
it looks directly at the camera with human-like eyes,
deep forest green background with mutated plants,
soft diffused light through the canopy,
it slowly turns and walks away,
plants on the forest floor bloom with unnatural colors as it passes,
body horror beauty, uncanny nature,
cinematic medium shot, film grain,
16:9 aspect ratio, slow subtle movement
```

**镜头参数：**
- 时长：5-7秒
- 运镜：固定机位（static with subtle movement）
- 节奏：缓慢，诡异美丽

---

### 镜头 5：觉醒逃脱（Awakening Escape）

**提示词：**
```
A woman in a white dress walks through a series of automatic doorways,
Alex Garland Ex Machina ending style,
behind her: cold sterile white and blue-grey facility,
ahead of her: warm golden natural light streaming in,
each door opens as she approaches,
she moves with deliberate calm, no rush,
her expression is one of quiet triumph and freedom,
the warm light grows brighter with each step,
cold blue shadows recede behind her,
symmetrical door framing creating tunnel perspective,
leaving the cage, becoming free,
cinematic tracking shot from behind, film grain,
16:9 aspect ratio, steady forward tracking
```

**镜头参数：**
- 时长：6-8秒
- 运镜：背面跟随（rear tracking follow）
- 节奏：稳定，冷静中的自由

---

### 镜头 6：绿色隧道恐怖（Green Tunnel Horror）

**提示词：**
```
A long green tunnel formed by overhanging trees and ivy,
Alex Garland Men style,
deep dark green pressing in from both sides,
dappled sunlight creates patches of light and shadow,
a lone figure walks slowly down the tunnel away from camera,
red stains visible on the path,
the green feels alive, watching, breathing,
something moves in the shadows at the far end,
the camera remains static as the figure walks deeper in,
natural British countryside light, overcast sky,
folk horror atmosphere, primal dread,
cinematic wide shot, film grain, naturalistic,
16:9 or 2.35:1 aspect ratio, static camera
```

**镜头参数：**
- 时长：6-8秒
- 运镜：固定机位（static camera）
- 节奏：缓慢，自然中的不安

---

## 三、运镜关键词速查

| 运镜效果 | 英文关键词 |
|---------|-----------|
| 对称推进 | symmetrical dolly in, centered push-in, perfect perspective forward |
| 玻璃反射 | glass reflection shot, recursive reflections, through glass POV |
| 缓慢凝视 | slow contemplative take, static contemplation, quiet observation |
| 走廊纵深 | corridor perspective, tunnel vision push, symmetrical hallway |
| 自然远景 | wide nature shot, isolated figure in landscape, vast wilderness |
| 面部特写推镜 | extreme close-up push-in on face, eye line match, direct gaze |
| 跟随前进 | follow behind tracking, walking forward steadicam, escape tracking |
| 静态空镜 | static establishing shot, empty space, architectural stillness |

---

## 四、颜色与光影关键词

| 效果 | 英文关键词 |
|------|-----------|
| 极简净白 | sterile white, pure white walls, minimal white space, white concrete |
| 冷钢蓝灰 | cold steel blue-grey, glass blue reflections, metallic cool tones |
| 深林绿 | deep forest green, dark English green, oppressive nature green |
| 虹彩粉紫 | iridescent pink-purple, prismatic shimmer, oil slick refraction, crystalline glow |
| 柔光漫射 | soft diffused light, natural light through glass, even lighting, no hard shadows |
| 觉醒金光 | warm golden light, awakening gold, natural sunlight, freedom glow |
| 警示血红 | blood red accent, stark red on green, primal red warning |
| AI幽蓝 | AI blue glow, digital blue light, cold blue eye light, tech blue accent |

---

## 五、负面描述（避免的效果）

```
fast action, quick cuts, michael bay explosions,
warm orange color grade, sunset golden hour (unless awakening),
chaotic composition, dutch angles, hand-held shake,
bright saturated colors, neon cyberpunk overload,
fantasy creatures, magic spells, superheroes,
comedy, slapstick, happy cheerful mood,
lens flare, bokeh overload, flashy camera work,
gore porn, torture, excessive blood
```

---

> 本文件由 `色卡主文档.md` 派生（运镜特征表 / 经典场景表 / 色板 / 光影），未新增事实。
> Seedance 2.5 段的结构规则来自本机技能库 `film-cinedance/references/seedance-25-prompt-format.md`。
> 图像提示词见 `midjourney_prompts.md` · `conversational_prompts.md`。
