# 视频提示词 — 希区柯克 Alfred Hitchcock 风格

> **一个文件，四套规则。你用哪个模型，就用哪一段。**
> 编号 `001` ｜ 分类 01 黑色悬疑与冷调惊悚 ｜ 国籍 英/美

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
精致对称构图下的互补色对比戏剧，阴影与眩晕感交织的悬疑美学。配色：主色 深夜暗蓝 `#1A2332` 占 40%，辅色 雾霭钢蓝 `#3D5A6C` 占 20%、暗金琥珀 `#8B6914` 占 15%、深墨绿 `#2E4A38` 占 12%，点缀 恐惧猩红 `#C41E3A` 占 8%、暖米肤 `#D4C5A9` 占 5%。让主色占主导，其余按比例递减。光线：主光：3/4 侧光，硬边阴影，chiaroscuro light-dark 对比强烈；高光偏暖金偏黄（烛光/钨丝灯）；阴影偏冷蓝偏青（夜色/心理恐惧）；对比度：高对比（75-85%）；整体：偏冷偏暗，65% 冷调 + 35% 暖色点缀。运镜与构图：对称构图、低角度仰拍、高角度俯拍、眩晕镜头（dolly zoom）、窥视视角、楼梯构图、剪影光、窗框取景、镜子反射、长镜头跟踪。色彩与光影：互补色红蓝对比、暗调低调照明、chiaroscuro light-dark 法、金色暖烛光、冷蓝夜色、红色警告点光源、金发逆光、阴影中藏人。氛围与情绪：悬疑张力、心理恐惧、优雅的危险、黑色电影、中产焦虑、窥视欲、错视与误解、时间的悬停。
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
[总控] 30 秒 ｜ 竖版 9:16 ｜ 精致对称构图下的互补色对比戏剧，阴影与眩晕感交织的悬疑美学。 ｜ 单主角 ｜ 有对白 / 无对白
[参考素材职责] 见 2.2，只留这次真正用到的

[0–4 秒 镜头 S01]《迷魂记 Vertigo》·钟楼坠落：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[4–9 秒 镜头 S02]《后窗 Rear Window》·公寓雨夜：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[9–16 秒 镜头 S03]《惊魂记 Psycho》·浴室谋杀：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[16–30 秒 镜头 S04]《西北偏北》·麦田飞机追杀：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。

[声音] 环境声：（照场景补）／对白：<写准确台词，不要写「说点什么」>／配乐：（不想要就写「无配乐」）

[场景特定限制] 红绿全程铺满，廉价黑场，随机手持，无动机环绕和随机变焦，用统一滤镜替代色彩比例，光源和材质。
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

#### 镜头 1：迷魂记 Vertigo · 钟楼坠落

```text
【运镜】眩晕镜头 (Dolly Zoom)（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在钟楼坠落里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《迷魂记 Vertigo》的钟楼坠落；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】精致对称构图下的互补色对比戏剧，阴影与眩晕感交织的悬疑美学。配色：主色 深夜暗蓝 `#1A2332` 占 40%，辅色 雾霭钢蓝 `#3D5A6C` 占 20%、暗金琥珀 `#8B6914` 占 15%、深墨绿 `#2E4A38` 占 12%，点缀 恐惧猩红 `#C41E3A` 占 8%、暖米肤 `#D4C5A9` 占 5%。让主色占主导，其余按比例递减。光线：主光：3/4 侧光，硬边阴影，chiaroscuro light-dark 对比强烈；高光偏暖金偏黄（烛光/钨丝灯）；阴影偏冷蓝偏青（夜色/心理恐惧）；对比度：高对比（75-85%）；整体：偏冷偏暗，65% 冷调 + 35% 暖色点缀。运镜与构图：对称构图、低角度仰拍、高角度俯拍、眩晕镜头（dolly zoom）、窥视视角、楼梯构图、剪影光、窗框取景、镜子反射、长镜头跟踪。色彩与光影：互补色红蓝对比、暗调低调照明、chiaroscuro light-dark 法、金色暖烛光、冷蓝夜色、红色警告点光源、金发逆光、阴影中藏人。氛围与情绪：悬疑张力、心理恐惧、优雅的危险、黑色电影、中产焦虑、窥视欲、错视与误解、时间的悬停。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 2：后窗 Rear Window · 公寓雨夜

```text
【运镜】长镜头跟踪（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在公寓雨夜里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《后窗 Rear Window》的公寓雨夜；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】精致对称构图下的互补色对比戏剧，阴影与眩晕感交织的悬疑美学。配色：主色 深夜暗蓝 `#1A2332` 占 40%，辅色 雾霭钢蓝 `#3D5A6C` 占 20%、暗金琥珀 `#8B6914` 占 15%、深墨绿 `#2E4A38` 占 12%，点缀 恐惧猩红 `#C41E3A` 占 8%、暖米肤 `#D4C5A9` 占 5%。让主色占主导，其余按比例递减。光线：主光：3/4 侧光，硬边阴影，chiaroscuro light-dark 对比强烈；高光偏暖金偏黄（烛光/钨丝灯）；阴影偏冷蓝偏青（夜色/心理恐惧）；对比度：高对比（75-85%）；整体：偏冷偏暗，65% 冷调 + 35% 暖色点缀。运镜与构图：对称构图、低角度仰拍、高角度俯拍、眩晕镜头（dolly zoom）、窥视视角、楼梯构图、剪影光、窗框取景、镜子反射、长镜头跟踪。色彩与光影：互补色红蓝对比、暗调低调照明、chiaroscuro light-dark 法、金色暖烛光、冷蓝夜色、红色警告点光源、金发逆光、阴影中藏人。氛围与情绪：悬疑张力、心理恐惧、优雅的危险、黑色电影、中产焦虑、窥视欲、错视与误解、时间的悬停。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 3：惊魂记 Psycho · 浴室谋杀

```text
【运镜】高角度俯拍（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在浴室谋杀里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《惊魂记 Psycho》的浴室谋杀；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】精致对称构图下的互补色对比戏剧，阴影与眩晕感交织的悬疑美学。配色：主色 深夜暗蓝 `#1A2332` 占 40%，辅色 雾霭钢蓝 `#3D5A6C` 占 20%、暗金琥珀 `#8B6914` 占 15%、深墨绿 `#2E4A38` 占 12%，点缀 恐惧猩红 `#C41E3A` 占 8%、暖米肤 `#D4C5A9` 占 5%。让主色占主导，其余按比例递减。光线：主光：3/4 侧光，硬边阴影，chiaroscuro light-dark 对比强烈；高光偏暖金偏黄（烛光/钨丝灯）；阴影偏冷蓝偏青（夜色/心理恐惧）；对比度：高对比（75-85%）；整体：偏冷偏暗，65% 冷调 + 35% 暖色点缀。运镜与构图：对称构图、低角度仰拍、高角度俯拍、眩晕镜头（dolly zoom）、窥视视角、楼梯构图、剪影光、窗框取景、镜子反射、长镜头跟踪。色彩与光影：互补色红蓝对比、暗调低调照明、chiaroscuro light-dark 法、金色暖烛光、冷蓝夜色、红色警告点光源、金发逆光、阴影中藏人。氛围与情绪：悬疑张力、心理恐惧、优雅的危险、黑色电影、中产焦虑、窥视欲、错视与误解、时间的悬停。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```


### 3.2 本导演可用的运镜（挑一个，别叠加）

- **眩晕镜头 (Dolly Zoom)** —— 推拉变焦，营造空间扭曲与心理失衡（例：《迷魂记》钟楼下坠）
- **长镜头跟踪** —— 跟随角色移动，让观众代入紧张感（例：《惊魂记》车驶入庄园）
- **高角度俯拍** —— 上帝视角，角色被命运支配（例：《迷魂记》屋顶追逐）
- **低角度仰拍** —— 压迫感，权力结构展现（例：《美人计》楼梯间）
- **窥视视角 (POV)** —— 望远镜/钥匙孔/窗户取景，观众同谋（例：《后窗》全程）
- **楼梯构图** —— 危险上升/坠落的视觉隐喻（例：《迷魂记》钟楼）

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
画面抖动，多余肢体，手指畸形，面部漂移，文字水印，物体变形，闪烁跳帧，重复物体，光线杂乱，红绿全程铺满，廉价黑场，随机手持，无动机环绕和随机变焦，用统一滤镜替代色彩比例，光源和材质。
```

---

## 四、MiniMax H3（海螺）

H3 按时间戳写，不分镜头。**声音要单独成段**。

```text
【核心创意】精致对称构图下的互补色对比戏剧，阴影与眩晕感交织的悬疑美学。
［主体］在钟楼坠落。

【分段过程描述】
[0–4s] 开场：迷魂记 Vertigo 式空间。［主体动作：缓慢抬手 / 微微低头 / 顺势坐下，写清幅度和速度］。
[4–8s] 中段：［主体动作承接上一拍，写惯性衔接］。
[8–12s] 收尾：［主体停住，画面定格在 暗蓝+眩晕金 的调子上］。

【声音】
overall_soundscape：（环境声 + 物理声 + 有无对白）
non_diegetic_music：（配乐；不想要就写「无配乐」）

【结束状态】画面收在［想要的那一帧］。
```

> 提示词上限约 **7000 字符**，写长不是问题，**糊成一段不分层才是**。

---

## 五、Runway / Pika

## 二、场景镜头模板

### 镜头 1：窥视开篇（Establishing Shot）

**提示词：**
```
A slow tracking shot moving across a row of apartment windows at night,
Alfred Hitchcock Rear Window style,
warm yellow lights glowing from inside each window,
cold blue rain falling outside,
we see glimpses of different people's lives through each window,
the camera slowly moves to focus on one dark window where a shadow moves,
film noir aesthetic, 1950s technicolor,
chiaroscuro lighting, suspense building,
rain sounds implied, cinematic wide shot,
16:9 aspect ratio, slow and deliberate camera movement
```

**镜头参数：**
- 时长：6-8秒
- 运镜：缓慢横移（tracking shot）
- 节奏：慢，压抑的窥视感

---

### 镜头 2：楼梯上升（Staircase Ascent）

**提示词：**
```
A woman in a green dress slowly walking up a dark spiral staircase,
Alfred Hitchcock Vertigo style,
dolly zoom vertigo effect making the staircase feel like it's stretching,
warm candlelight from above casting long shadows on the stone walls,
cold blue shadows in the corners,
her footsteps are deliberate and tense,
the camera follows her from behind,
suspense building with each step,
film noir aesthetic, 1950s cinematic,
chiaroscuro lighting, dramatic contrast,
16:9 aspect ratio, slow upward movement with dolly zoom
```

**镜头参数：**
- 时长：5-7秒
- 运镜：跟随 + 眩晕推拉变焦
- 节奏：渐快，呼吸感增强

---

### 镜头 3：浴室门帘（Shower Curtain Tension）

**提示词：**
```
Extreme close-up of a shower curtain slowly being pulled aside,
Alfred Hitchcock Psycho style,
dim bathroom with cold blue tiles,
water droplets on the curtain,
steam creating hazy atmosphere,
we see the silhouette of a figure through the translucent curtain,
the light flickers slightly,
extreme tension and dread,
chiaroscuro lighting, high contrast shadows,
film noir horror aesthetic, dark and menacing,
slow, deliberate movement, 16:9 aspect ratio
```

**镜头参数：**
- 时长：4-6秒
- 运镜：固定机位，慢速推进
- 节奏：极慢，压抑到爆发前

---

### 镜头 4：麦田飞机（Crop Duster Chase）

**提示词：**
```
A man in a grey suit running through vast golden wheat fields,
Alfred Hitchcock North by Northwest style,
a small airplane diving toward him from the blue sky,
dust and wheat flying up as he runs,
extreme wide shot making the man look tiny against the landscape,
isolation and desperation,
high contrast between golden wheat and deep blue sky,
cinematic epic scope, 1950s technicolor,
the camera pulls back to reveal the vastness,
thriller action, suspenseful chase,
2.35:1 cinemascope aspect ratio
```

**镜头参数：**
- 时长：6-8秒
- 运镜：拉远（pull back）+ 跟随
- 节奏：快速，紧急

---

### 镜头 5：镜子反射（Mirror Reveal）

**提示词：**
```
A woman looking at herself in an ornate mirror,
Alfred Hitchcock film noir style,
warm vanity light illuminating her face,
cold blue shadows in the room behind her,
she adjusts her hair nervously,
in the mirror reflection we see a figure appear in the doorway behind her,
she doesn't notice, the figure stands still in shadow,
dramatic irony, suspense building,
chiaroscuro lighting, 1950s aesthetic,
medium shot, slow and deliberate,
16:9 aspect ratio
```

**镜头参数：**
- 时长：5-6秒
- 运镜：固定机位，缓慢推近
- 节奏：渐强，观众知道而角色不知道

---

### 镜头 6：钟楼下坠（Bell Tower Fall）

**提示词：**
```
Vertigo dolly zoom shot looking down from the top of a bell tower,
Alfred Hitchcock Vertigo style,
the stone staircase spiraling down into darkness,
the camera pushes forward while zooming out creating the vertigo effect,
faint golden light from above,
dust particles floating in the light beams,
disorienting, dizzy, psychological terror,
cold blue shadows, gothic architecture,
film noir thriller, 1950s cinematic,
extreme high angle, spinning sensation,
9:16 or 16:9 aspect ratio
```

**镜头参数：**
- 时长：5-7秒
- 运镜：眩晕推拉变焦（dolly zoom）
- 节奏：加速旋转，心理失控感

---

## 三、运镜关键词速查

| 运镜效果 | 英文关键词 |
|---------|-----------|
| 眩晕推拉变焦 | dolly zoom, vertigo effect, push in while zooming out |
| 长镜头跟踪 | long tracking shot, follow shot, continuous take |
| 高角度俯拍 | high angle shot, looking down, bird's eye view |
| 低角度仰拍 | low angle shot, looking up, imposing |
| 窥视视角 | voyeuristic POV, through a window, keyhole view |
| 缓慢推进 | slow push in, creeping forward, dolly in |
| 拉远揭示 | pull back to reveal, zoom out, crane up |
| 蒙太奇剪辑 | montage, quick cuts, fragmented editing |

---

## 四、颜色与光影关键词

| 效果 | 英文关键词 |
|------|-----------|
| light-dark对比法 | chiaroscuro lighting, high contrast shadows |
| 低调照明 | low-key lighting, dark atmosphere, moody |
| 暖金烛光 | warm candlelight, golden tungsten light, amber glow |
| 冷蓝夜色 | cold blue night, steel blue shadows, moonlit |
| 红色警告 | red warning light, scarlet accent, blood red |
| 金发逆光 | blonde backlight, rim lighting, hair glow |
| 雨夜景 | rainy night, wet surfaces, neon reflections |
| 雾霭朦胧 | misty, foggy, atmospheric haze, smog |

---

## 五、负面描述（避免的效果）

```
modern clothing, smartphones, digital screens,
bright cheerful colors, cartoon style, anime,
fast shaky cam, found footage,
overexposed, flat lighting, low quality,
happy ending, romantic comedy tone
```

---

> 本文件由 `色卡主文档.md` 派生（运镜特征表 / 经典场景表 / 色板 / 光影），未新增事实。
> Seedance 2.5 段的结构规则来自本机技能库 `film-cinedance/references/seedance-25-prompt-format.md`。
> 图像提示词见 `midjourney_prompts.md` · `conversational_prompts.md`。
