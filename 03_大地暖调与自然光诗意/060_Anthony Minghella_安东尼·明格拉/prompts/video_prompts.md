# 视频提示词 — 安东尼·明格拉 Anthony Minghella 风格

> **一个文件，四套规则。你用哪个模型，就用哪一段。**
> 编号 `060` ｜ 分类 03 大地暖调与自然光诗意 ｜ 国籍 英国

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
沙漠金暖与柔光回忆交织的史诗浪漫，文学改编的影像诗人。配色：主色 沙漠流金 `#D4A76A` 占 22%，辅色 橄榄暗金 `#8B6914` 占 18%、深褐木影 `#5C4A3D` 占 15%、柔光米色 `#E8D4B0` 占 15%，点缀 橄榄灰绿 `#6B7A5A` 占 15%、陶土砖红 `#A0673D` 占 15%。让主色占主导，其余按比例递减。光线：主光：golden desert haze, soft memory diffusion, romantic natural light；高光偏 warm honey gold / sand amber；阴影偏 umber brown / olive green；对比度：medium-low 50-65%；整体：warm golden romantic, 70% warm + 30% cool。运镜与构图：sweeping desert vistas、soft focus memory、romantic close-up、period costume detail、window light portrait、epic landscape framing、slow dissolve transition、mirrored reflections。色彩与光影：sahara desert gold、tuscan olive green、soft cream memory、terracotta warm red、honey amber sunset、dusty golden haze、warm skin tones、literary romantic palette。氛围与情绪：epic romance、wartime longing、memory and nostalgia、literary tragedy、mediterranean warmth、unspoken desire、soulful melancholy、grand human drama。
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
[总控] 30 秒 ｜ 竖版 9:16 ｜ 沙漠金暖与柔光回忆交织的史诗浪漫，文学改编的影像诗人。 ｜ 单主角 ｜ 有对白 / 无对白
[参考素材职责] 见 2.2，只留这次真正用到的

[0–4 秒 镜头 S01]《英国病人》·撒哈拉沙漠：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[4–9 秒 镜头 S02]《天才雷普利》·意大利海岸：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[9–16 秒 镜头 S03]《冷山》·南北战争：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。

[声音] 环境声：（照场景补）／对白：<写准确台词，不要写「说点什么」>／配乐：（不想要就写「无配乐」）

[场景特定限制] 冷白硬光，快速切镜，过度饱和，现代锐利调色，用统一滤镜替代精心营造的柔光与空气感
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

#### 镜头 1：英国病人 · 撒哈拉沙漠

```text
【运镜】沙漠远景（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在撒哈拉沙漠里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《英国病人》的撒哈拉沙漠；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】沙漠金暖与柔光回忆交织的史诗浪漫，文学改编的影像诗人。配色：主色 沙漠流金 `#D4A76A` 占 22%，辅色 橄榄暗金 `#8B6914` 占 18%、深褐木影 `#5C4A3D` 占 15%、柔光米色 `#E8D4B0` 占 15%，点缀 橄榄灰绿 `#6B7A5A` 占 15%、陶土砖红 `#A0673D` 占 15%。让主色占主导，其余按比例递减。光线：主光：golden desert haze, soft memory diffusion, romantic natural light；高光偏 warm honey gold / sand amber；阴影偏 umber brown / olive green；对比度：medium-low 50-65%；整体：warm golden romantic, 70% warm + 30% cool。运镜与构图：sweeping desert vistas、soft focus memory、romantic close-up、period costume detail、window light portrait、epic landscape framing、slow dissolve transition、mirrored reflections。色彩与光影：sahara desert gold、tuscan olive green、soft cream memory、terracotta warm red、honey amber sunset、dusty golden haze、warm skin tones、literary romantic palette。氛围与情绪：epic romance、wartime longing、memory and nostalgia、literary tragedy、mediterranean warmth、unspoken desire、soulful melancholy、grand human drama。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 2：天才雷普利 · 意大利海岸

```text
【运镜】柔光回忆（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在意大利海岸里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《天才雷普利》的意大利海岸；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】沙漠金暖与柔光回忆交织的史诗浪漫，文学改编的影像诗人。配色：主色 沙漠流金 `#D4A76A` 占 22%，辅色 橄榄暗金 `#8B6914` 占 18%、深褐木影 `#5C4A3D` 占 15%、柔光米色 `#E8D4B0` 占 15%，点缀 橄榄灰绿 `#6B7A5A` 占 15%、陶土砖红 `#A0673D` 占 15%。让主色占主导，其余按比例递减。光线：主光：golden desert haze, soft memory diffusion, romantic natural light；高光偏 warm honey gold / sand amber；阴影偏 umber brown / olive green；对比度：medium-low 50-65%；整体：warm golden romantic, 70% warm + 30% cool。运镜与构图：sweeping desert vistas、soft focus memory、romantic close-up、period costume detail、window light portrait、epic landscape framing、slow dissolve transition、mirrored reflections。色彩与光影：sahara desert gold、tuscan olive green、soft cream memory、terracotta warm red、honey amber sunset、dusty golden haze、warm skin tones、literary romantic palette。氛围与情绪：epic romance、wartime longing、memory and nostalgia、literary tragedy、mediterranean warmth、unspoken desire、soulful melancholy、grand human drama。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 3：冷山 · 南北战争

```text
【运镜】窗光肖像（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在南北战争里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《冷山》的南北战争；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】沙漠金暖与柔光回忆交织的史诗浪漫，文学改编的影像诗人。配色：主色 沙漠流金 `#D4A76A` 占 22%，辅色 橄榄暗金 `#8B6914` 占 18%、深褐木影 `#5C4A3D` 占 15%、柔光米色 `#E8D4B0` 占 15%，点缀 橄榄灰绿 `#6B7A5A` 占 15%、陶土砖红 `#A0673D` 占 15%。让主色占主导，其余按比例递减。光线：主光：golden desert haze, soft memory diffusion, romantic natural light；高光偏 warm honey gold / sand amber；阴影偏 umber brown / olive green；对比度：medium-low 50-65%；整体：warm golden romantic, 70% warm + 30% cool。运镜与构图：sweeping desert vistas、soft focus memory、romantic close-up、period costume detail、window light portrait、epic landscape framing、slow dissolve transition、mirrored reflections。色彩与光影：sahara desert gold、tuscan olive green、soft cream memory、terracotta warm red、honey amber sunset、dusty golden haze、warm skin tones、literary romantic palette。氛围与情绪：epic romance、wartime longing、memory and nostalgia、literary tragedy、mediterranean warmth、unspoken desire、soulful melancholy、grand human drama。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```


### 3.2 本导演可用的运镜（挑一个，别叠加）

- **沙漠远景** —— 浩瀚沙漠中的渺小人物（例：《英国病人》撒哈拉）
- **柔光回忆** —— 柔焦处理记忆片段（例：《英国病人》闪回）
- **窗光肖像** —— 窗光勾勒面部轮廓（例：《天才雷普利》肖像）
- **史诗长镜** —— 宏大战争场面调度（例：《冷山》战役）
- **慢溶转场** —— 回忆与现实交融（例：《英国病人》时空交错）
- **镜子反射** —— 人物内心镜像（例：《天才雷普利》威尼斯）

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
画面抖动，多余肢体，手指畸形，面部漂移，文字水印，物体变形，闪烁跳帧，重复物体，光线杂乱，冷白硬光，快速切镜，过度饱和，现代锐利调色，用统一滤镜替代精心营造的柔光与空气感
```

---

## 四、MiniMax H3（海螺）

H3 按时间戳写，不分镜头。**声音要单独成段**。

```text
【核心创意】沙漠金暖与柔光回忆交织的史诗浪漫，文学改编的影像诗人。
［主体］在撒哈拉沙漠。

【分段过程描述】
[0–4s] 开场：英国病人 式空间。［主体动作：缓慢抬手 / 微微低头 / 顺势坐下，写清幅度和速度］。
[4–8s] 中段：［主体动作承接上一拍，写惯性衔接］。
[8–12s] 收尾：［主体停住，画面定格在 沙漠流金+柔光米色 的调子上］。

【声音】
overall_soundscape：（环境声 + 物理声 + 有无对白）
non_diegetic_music：（配乐；不想要就写「无配乐」）

【结束状态】画面收在［想要的那一帧］。
```

> 提示词上限约 **7000 字符**，写长不是问题，**糊成一段不分层才是**。

---

## 五、Runway / Pika

# 视频提示词模板 — 安东尼·明格拉 Anthony Minghella风格

---

## 镜头脚本
| 镜头 | 运镜 |
|------|------|
| 镜头1 | sweeping desert vistas |
| 镜头2 | soft focus memory |
| 镜头3 | romantic close-up |
| 镜头4 | period costume detail |
| 镜头5 | window light portrait |
| 镜头6 | epic landscape framing |

## 运镜关键词
sweeping desert vistas, soft focus memory, romantic close-up, period costume detail, window light portrait, epic landscape framing, slow dissolve transition, mirrored reflections

## 色彩关键词
sahara desert gold, tuscan olive green, soft cream memory, terracotta warm red, honey amber sunset, dusty golden haze, warm skin tones, literary romantic palette

## 视频公式
```
A cinematic scene in Anthony Minghella style, golden desert haze, soft memory diffusion, romantic natural light, sahara desert gold, sweeping desert vistas, epic romance, memory and nostalgia, epic atmosphere, cinematic movement
```

## 负面描述
flat lighting, steady locked-off camera, clean digital look, fast cuts, cartoon style

---

> 本文件由 `色卡主文档.md` 派生（运镜特征表 / 经典场景表 / 色板 / 光影），未新增事实。
> Seedance 2.5 段的结构规则来自本机技能库 `film-cinedance/references/seedance-25-prompt-format.md`。
> 图像提示词见 `midjourney_prompts.md` · `conversational_prompts.md`。
