# 视频提示词 — 扎克·施奈德 Zack Snyder 风格

> **一个文件，四套规则。你用哪个模型，就用哪一段。**
> 编号 `034` ｜ 分类 02 霓虹黑色与赛博未来 ｜ 国籍 美国

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
暗金油画质感与高反差深黑阴影构筑的漫画史诗中，慢镜飞溅的血滴与闪电白的速度力交汇成视觉暴力的暗黑神话。配色：主色 深黑墨影 `#0A0A0A` 占 25%，辅色 暗金铜锈 `#8B6914` 占 22%、血锈红 `#8B0000` 占 15%、`#6B4226` 占 13%，点缀 霓虹玫红 `#E91E63` 占 13%、冷钢灰 `#4A5568` 占 12%。让主色占主导，其余按比例递减。光线：主光：极端侧光/逆光为主，硬光切割，暗部几乎纯黑，高光处爆发闪电白；高光偏闪电白/暗金（速度力高光/古铜金光/神圣光芒）；阴影偏深黑墨影（暗部几乎无细节，纯黑阴影，Snyder 标志性暗场）；对比度：极高对比（85-98%），油画质感暗调，高光刺眼，暗部深邃；整体：暗调油画，60% 暗金褐黑 + 40% 血锈红/冷钢灰/霓虹玫红。运镜与构图：慢镜飞溅、速度力推进、漫画分镜构图、低角度英雄、油画质感画面、对称史诗、速度线爆发、剪影英雄、雨滴慢镜、上帝视角俯拍。色彩与光影：暗金铜锈、深黑墨影、血锈红、冷钢灰、闪电白、高反差暗调、油画质感、sepia 尘褐、霓虹玫红、烈焰橙。氛围与情绪：暗黑神话、漫画史诗、英雄悲壮、暴力美学、男性荷尔蒙、神与人、慢镜仪式、宿命感、黑暗骑士、僵尸末日。
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
[总控] 30 秒 ｜ 竖版 9:16 ｜ 暗金油画质感与高反差深黑阴影构筑的漫画史诗中，慢镜飞溅的血滴与闪电白的速度力交汇成视觉暴力的暗黑神话。 ｜ 单主角 ｜ 有对白 / 无对白
[参考素材职责] 见 2.2，只留这次真正用到的

[0–4 秒 镜头 S01]《300勇士》·温泉关列阵：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[4–9 秒 镜头 S02]《守望者》·笑匠之死/雨夜：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[9–16 秒 镜头 S03]《活死人军团》·维加斯末日：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[16–30 秒 镜头 S04]《扎克·施奈德版正义联盟》·闪电侠速度力：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。

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

#### 镜头 1：300勇士 · 温泉关列阵

```text
【运镜】慢镜血滴飞溅（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在温泉关列阵里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《300勇士》的温泉关列阵；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】暗金油画质感与高反差深黑阴影构筑的漫画史诗中，慢镜飞溅的血滴与闪电白的速度力交汇成视觉暴力的暗黑神话。配色：主色 深黑墨影 `#0A0A0A` 占 25%，辅色 暗金铜锈 `#8B6914` 占 22%、血锈红 `#8B0000` 占 15%、`#6B4226` 占 13%，点缀 霓虹玫红 `#E91E63` 占 13%、冷钢灰 `#4A5568` 占 12%。让主色占主导，其余按比例递减。光线：主光：极端侧光/逆光为主，硬光切割，暗部几乎纯黑，高光处爆发闪电白；高光偏闪电白/暗金（速度力高光/古铜金光/神圣光芒）；阴影偏深黑墨影（暗部几乎无细节，纯黑阴影，Snyder 标志性暗场）；对比度：极高对比（85-98%），油画质感暗调，高光刺眼，暗部深邃；整体：暗调油画，60% 暗金褐黑 + 40% 血锈红/冷钢灰/霓虹玫红。运镜与构图：慢镜飞溅、速度力推进、漫画分镜构图、低角度英雄、油画质感画面、对称史诗、速度线爆发、剪影英雄、雨滴慢镜、上帝视角俯拍。色彩与光影：暗金铜锈、深黑墨影、血锈红、冷钢灰、闪电白、高反差暗调、油画质感、sepia 尘褐、霓虹玫红、烈焰橙。氛围与情绪：暗黑神话、漫画史诗、英雄悲壮、暴力美学、男性荷尔蒙、神与人、慢镜仪式、宿命感、黑暗骑士、僵尸末日。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 2：守望者 · 笑匠之死/雨夜

```text
【运镜】速度力推进（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在笑匠之死/雨夜里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《守望者》的笑匠之死/雨夜；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】暗金油画质感与高反差深黑阴影构筑的漫画史诗中，慢镜飞溅的血滴与闪电白的速度力交汇成视觉暴力的暗黑神话。配色：主色 深黑墨影 `#0A0A0A` 占 25%，辅色 暗金铜锈 `#8B6914` 占 22%、血锈红 `#8B0000` 占 15%、`#6B4226` 占 13%，点缀 霓虹玫红 `#E91E63` 占 13%、冷钢灰 `#4A5568` 占 12%。让主色占主导，其余按比例递减。光线：主光：极端侧光/逆光为主，硬光切割，暗部几乎纯黑，高光处爆发闪电白；高光偏闪电白/暗金（速度力高光/古铜金光/神圣光芒）；阴影偏深黑墨影（暗部几乎无细节，纯黑阴影，Snyder 标志性暗场）；对比度：极高对比（85-98%），油画质感暗调，高光刺眼，暗部深邃；整体：暗调油画，60% 暗金褐黑 + 40% 血锈红/冷钢灰/霓虹玫红。运镜与构图：慢镜飞溅、速度力推进、漫画分镜构图、低角度英雄、油画质感画面、对称史诗、速度线爆发、剪影英雄、雨滴慢镜、上帝视角俯拍。色彩与光影：暗金铜锈、深黑墨影、血锈红、冷钢灰、闪电白、高反差暗调、油画质感、sepia 尘褐、霓虹玫红、烈焰橙。氛围与情绪：暗黑神话、漫画史诗、英雄悲壮、暴力美学、男性荷尔蒙、神与人、慢镜仪式、宿命感、黑暗骑士、僵尸末日。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 3：活死人军团 · 维加斯末日

```text
【运镜】漫画分镜构图（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在维加斯末日里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《活死人军团》的维加斯末日；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】暗金油画质感与高反差深黑阴影构筑的漫画史诗中，慢镜飞溅的血滴与闪电白的速度力交汇成视觉暴力的暗黑神话。配色：主色 深黑墨影 `#0A0A0A` 占 25%，辅色 暗金铜锈 `#8B6914` 占 22%、血锈红 `#8B0000` 占 15%、`#6B4226` 占 13%，点缀 霓虹玫红 `#E91E63` 占 13%、冷钢灰 `#4A5568` 占 12%。让主色占主导，其余按比例递减。光线：主光：极端侧光/逆光为主，硬光切割，暗部几乎纯黑，高光处爆发闪电白；高光偏闪电白/暗金（速度力高光/古铜金光/神圣光芒）；阴影偏深黑墨影（暗部几乎无细节，纯黑阴影，Snyder 标志性暗场）；对比度：极高对比（85-98%），油画质感暗调，高光刺眼，暗部深邃；整体：暗调油画，60% 暗金褐黑 + 40% 血锈红/冷钢灰/霓虹玫红。运镜与构图：慢镜飞溅、速度力推进、漫画分镜构图、低角度英雄、油画质感画面、对称史诗、速度线爆发、剪影英雄、雨滴慢镜、上帝视角俯拍。色彩与光影：暗金铜锈、深黑墨影、血锈红、冷钢灰、闪电白、高反差暗调、油画质感、sepia 尘褐、霓虹玫红、烈焰橙。氛围与情绪：暗黑神话、漫画史诗、英雄悲壮、暴力美学、男性荷尔蒙、神与人、慢镜仪式、宿命感、黑暗骑士、僵尸末日。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```


### 3.2 本导演可用的运镜（挑一个，别叠加）

- **慢镜血滴飞溅** —— 暴力瞬间的极慢镜头，血滴/碎片悬浮（例：《300 勇士》砍杀慢镜、《守望者》笑匠之死）
- **速度力推进** —— 极速者的闪电特效和速度线推进（例：《扎克、施奈德版正义联盟》闪电侠）
- **漫画分镜构图** —— 直接复刻漫画经典分格画面（例：《守望者》、《300 勇士》逐帧还原漫画）
- **低角度英雄** —— 极低角度仰拍英雄/战士的伟岸（例：《300 勇士》列奥尼达、《蝙蝠侠》）
- **油画质感画面** —— 棕褐色调+暗金光泽的油画质感（例：《300 勇士》全片油画风格）
- **雨滴慢镜** —— 雨滴/水花的极致慢镜拍摄（例：《守望者》雨战、《活死人军团》片头）

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
【核心创意】暗金油画质感与高反差深黑阴影构筑的漫画史诗中，慢镜飞溅的血滴与闪电白的速度力交汇成视觉暴力的暗黑神话。
［主体］在温泉关列阵。

【分段过程描述】
[0–4s] 开场：300勇士 式空间。［主体动作：缓慢抬手 / 微微低头 / 顺势坐下，写清幅度和速度］。
[4–8s] 中段：［主体动作承接上一拍，写惯性衔接］。
[8–12s] 收尾：［主体停住，画面定格在 暗金铜锈+血锈红+尘褐 的调子上］。

【声音】
overall_soundscape：（环境声 + 物理声 + 有无对白）
non_diegetic_music：（配乐；不想要就写「无配乐」）

【结束状态】画面收在［想要的那一帧］。
```

> 提示词上限约 **7000 字符**，写长不是问题，**糊成一段不分层才是**。

---

## 五、Runway / Pika

## 二、场景镜头模板

### 镜头 1：This is Sparta! （Hero Kick）

**提示词：**
```
A muscular warrior in red cape kicks an envoy into a dark pit,
Zack Snyder 300 style,
the kick connects in extreme slow motion,
dark gold bronze sepia tones, deep black pit below,
red cape billowing dramatically,
dust and embers float suspended in the air,
oil painting texture on skin and armor,
the camera is at low angle looking up,
dramatic backlight creates rim light on the warrior,
blood spittle flies from the envoy's mouth in slow motion,
epic mythic moment, legendary defiance,
cinematic 2.35:1 aspect ratio, extreme slow motion
```

**镜头参数：**
- 时长：5-7秒
- 运镜：低角度仰拍极慢镜（low angle extreme slow-mo）
- 节奏：极慢镜，神话时刻

---

### 镜头 2：盾牌阵列推进（Phalanx Advance）

**提示词：**
```
A wall of Spartan warriors with shields advances through dust and fire,
Zack Snyder 300 style,
bronze shields form an unbroken wall, red capes flow behind,
dark gold sepia tones, blood and dust in the air,
warriors march in perfect slow-motion unison,
arrows bounce off shields, spears thrust forward,
deep black shadows contrast with orange firelight,
the camera tracks alongside the phalanx at shield level,
oil painting texture, every muscle and wound visible,
overwhelming force and discipline,
epic battle, film grain,
2.35:1 aspect ratio, slow lateral tracking
```

**镜头参数：**
- 时长：6-8秒
- 运镜：盾牌高度侧跟慢镜（shield-level slow lateral track）
- 节奏：慢镜推进，不可阻挡

---

### 镜头 3：雨夜黑暗骑士（Rain Knight）

**提示词：**
```
A dark caped figure stands on a gothic rooftop in torrential rain,
Zack Snyder Batman style,
black armor silhouette against lightning-lit sky,
cold steel grey rain drops suspended mid-air around him,
lightning flashes white illuminating his cape and armor,
the cape flows in slow motion wind,
deep black shadows, only lightning reveals detail,
gargoyles and gothic architecture in dark background,
wet cape and armor glistening,
the camera slowly circles around him,
dark brooding, vengeance personified,
cinematic noir, film grain,
2.35:1 aspect ratio, slow orbit camera
```

**镜头参数：**
- 时长：6-8秒
- 运镜：慢环绕（slow orbit/circling）
- 节奏：缓慢，黑暗骑士的压迫感

---

### 镜头 4：慢镜血溅（Slow-Motion Blood）

**提示词：**
```
A sword slash in extreme slow motion on a battlefield,
Zack Snyder 300 style,
dark gold bronze sepia palette,
bright red blood sprays outward in a perfect arc,
blood droplets hang suspended in the air like rubies,
dust particles and embers frozen mid-flight,
deep black background, firelight from the side,
oil painting texture on skin and metal,
the blade glints with dark gold light,
every droplet catches the firelight,
violence made beautiful through slow motion,
graphic comic book violence aesthetic,
16:9 or 2.35:1 aspect ratio, extreme slow motion close-up
```

**镜头参数：**
- 时长：4-6秒
- 运镜：固定机位极慢镜特写（static extreme slow-mo close-up）
- 节奏：极慢镜，暴力美学化

---

### 镜头 5：闪电侠速度力（Speed Force Run）

**提示词：**
```
A speedster in red suit runs at impossible speed,
Zack Snyder Justice League style,
electric white-blue lightning trails crackle behind him,
the world around him is completely frozen in time,
rain drops hang motionless in the air,
people and cars frozen mid-motion,
sparks of white lightning illuminate the dark scene,
blue and white electric energy builds around him,
the camera follows him from behind as he races forward,
buildings and street blur with speed,
time itself bending, god-like power,
epic superhero moment, high contrast,
16:9 or 2.35:1 aspect ratio, high speed forward tracking
```

**镜头参数：**
- 时长：5-7秒
- 运镜：背面高速跟随（rear high-speed tracking）
- 节奏：极速但周围静止，速度力

---

### 镜头 6：维加斯霓虹僵尸（Vegas Neon Zombies）

**提示词：**
```
A zombie horde stumbles down a neon-lit Las Vegas strip,
Zack Snyder Army of the Dead style,
neon rose pink and orange casino signs flicker,
broken neon reflects in shattered glass and blood,
zombies with glowing eyes move through the ruins,
fire burns in the distance, smoke billows,
pink and orange neon glow on decayed faces,
deep black shadows between the neon pools of light,
the camera slowly pulls back revealing more zombies,
abandoned tanks and cars block the street,
neon noir zombie apocalypse,
cinematic, high contrast, film grain,
2.35:1 aspect ratio, slow pull-back reveal
```

**镜头参数：**
- 时长：6-8秒
- 运镜：缓慢拉远揭示（slow pull-back reveal）
- 节奏：缓慢，僵尸末日的压抑

---

## 三、运镜关键词速查

| 运镜效果 | 英文关键词 |
|---------|-----------|
| 极慢镜暴力 | extreme slow motion, suspended droplets, frozen debris, blood in air |
| 低角度英雄 | low angle heroic shot, looking up at warrior, imposing angle |
| 漫画分镜 | comic book panel, splash page composition, graphic novel framing |
| 速度力 | speed force running, lightning trail, frozen time, electric energy |
| 剪影逆光 | silhouette against light, backlight rim, dark figure against fire/lightning |
| 油画质感 | oil painting texture, painterly, brush stroke texture, desaturated sepia |
| 雨滴慢镜 | rain drops suspended, water in slow motion, droplets in air |
| 史诗远景 | epic wide battle shot, god's eye view, massive army panorama |

---

## 四、颜色与光影关键词

| 效果 | 英文关键词 |
|------|-----------|
| 暗金铜锈 | dark gold bronze, sepia desaturated, bronze skin tone, copper patina |
| 深黑墨影 | deep ink black, pure black shadows, crushed blacks, no detail in shadow |
| 血锈红 | blood red accent, dark crimson, rust red, red cape against sepia |
| 冷钢灰 | cold steel grey, metallic armor grey, dark iron, batman grey-black |
| 闪电白 | lightning white, bright white rim light, electric sparks, blown-out highlights |
| 曼哈顿蓝 | dr manhattan blue, glowing blue, atomic blue god, nuclear blue |
| 烈焰橙 | blaze orange fire, explosion orange, firelight, warm flame glow |
| 霓虹玫红 | neon rose pink, magenta neon, vegas neon, hot pink glow |

---

## 五、负面描述（避免的效果）

```
bright cheerful colors, soft pastel, romantic lighting,
natural daylight, bright sun, overexposed,
hand-held shaky cam, found footage, documentary look,
comedy, slapstick, lighthearted tone,
subtle quiet film, minimalist indie aesthetic,
CGI cartoon, pixar animation, anime style,
flat even lighting, low contrast, grey muddy tones
```

---

> 本文件由 `色卡主文档.md` 派生（运镜特征表 / 经典场景表 / 色板 / 光影），未新增事实。
> Seedance 2.5 段的结构规则来自本机技能库 `film-cinedance/references/seedance-25-prompt-format.md`。
> 图像提示词见 `midjourney_prompts.md` · `conversational_prompts.md`。
