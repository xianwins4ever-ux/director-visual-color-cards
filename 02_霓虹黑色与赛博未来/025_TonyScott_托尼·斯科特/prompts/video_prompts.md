# 视频提示词 — 托尼·斯科特 Tony Scott 风格

> **一个文件，四套规则。你用哪个模型，就用哪一段。**
> 编号 `025` ｜ 分类 02 霓虹黑色与赛博未来 ｜ 国籍 英国

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
高速剪辑与橙蓝对比交织的过曝逆光，商业动作片最鲜艳的视觉烟花。配色：主色 深蓝夜幕 `#0D1B2A` 占 25%，辅色 烈焰橙 `#FF6B00` 占 18%、电光蓝 `#1E90FF` 占 15%、暖金阳光 `#DAA520` 占 15%，点缀 小麦肤 `#F5DEB3` 占 15%、深红行动 `#8B0000` 占 12%。让主色占主导，其余按比例递减。光线：主光：backlit golden hour, overexposed highlights, strong orange-blue；高光偏 orange-gold sunset backlight explosion；阴影偏 deep navy blue；对比度：high 75-85%；整体：high-saturation orange-blue 50/50。运镜与构图：rapid montage editing、helicopter aerial shots、backlit silhouettes、slow motion action、360 degree orbits、low angle hero、lens flares、smoke steam。色彩与光影：orange-blue complementary、backlit golden hour、overexposed highlights、teal and orange grade、lens flare streaks、sunset orange glow、navy blue night、saturated commercial。氛围与情绪：high-octane action、commercial slickness、heroic masculinity、romantic tension、adrenaline rush、patriotic americana、glamorous danger、pop entertainment。
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
[总控] 30 秒 ｜ 竖版 9:16 ｜ 高速剪辑与橙蓝对比交织的过曝逆光，商业动作片最鲜艳的视觉烟花。 ｜ 单主角 ｜ 有对白 / 无对白
[参考素材职责] 见 2.2，只留这次真正用到的

[0–4 秒 镜头 S01]《壮志凌云》·飞行甲板：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[4–9 秒 镜头 S02]《怒火救援》·墨西哥城：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[9–16 秒 镜头 S03]《间谍游戏》·全球谍战：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[16–30 秒 镜头 S04]《红潮风暴》·潜艇对峙：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。

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

#### 镜头 1：壮志凌云 · 飞行甲板

```text
【运镜】直升机航拍（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在飞行甲板里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《壮志凌云》的飞行甲板；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】高速剪辑与橙蓝对比交织的过曝逆光，商业动作片最鲜艳的视觉烟花。配色：主色 深蓝夜幕 `#0D1B2A` 占 25%，辅色 烈焰橙 `#FF6B00` 占 18%、电光蓝 `#1E90FF` 占 15%、暖金阳光 `#DAA520` 占 15%，点缀 小麦肤 `#F5DEB3` 占 15%、深红行动 `#8B0000` 占 12%。让主色占主导，其余按比例递减。光线：主光：backlit golden hour, overexposed highlights, strong orange-blue；高光偏 orange-gold sunset backlight explosion；阴影偏 deep navy blue；对比度：high 75-85%；整体：high-saturation orange-blue 50/50。运镜与构图：rapid montage editing、helicopter aerial shots、backlit silhouettes、slow motion action、360 degree orbits、low angle hero、lens flares、smoke steam。色彩与光影：orange-blue complementary、backlit golden hour、overexposed highlights、teal and orange grade、lens flare streaks、sunset orange glow、navy blue night、saturated commercial。氛围与情绪：high-octane action、commercial slickness、heroic masculinity、romantic tension、adrenaline rush、patriotic americana、glamorous danger、pop entertainment。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 2：怒火救援 · 墨西哥城

```text
【运镜】逆光剪影（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在墨西哥城里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《怒火救援》的墨西哥城；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】高速剪辑与橙蓝对比交织的过曝逆光，商业动作片最鲜艳的视觉烟花。配色：主色 深蓝夜幕 `#0D1B2A` 占 25%，辅色 烈焰橙 `#FF6B00` 占 18%、电光蓝 `#1E90FF` 占 15%、暖金阳光 `#DAA520` 占 15%，点缀 小麦肤 `#F5DEB3` 占 15%、深红行动 `#8B0000` 占 12%。让主色占主导，其余按比例递减。光线：主光：backlit golden hour, overexposed highlights, strong orange-blue；高光偏 orange-gold sunset backlight explosion；阴影偏 deep navy blue；对比度：high 75-85%；整体：high-saturation orange-blue 50/50。运镜与构图：rapid montage editing、helicopter aerial shots、backlit silhouettes、slow motion action、360 degree orbits、low angle hero、lens flares、smoke steam。色彩与光影：orange-blue complementary、backlit golden hour、overexposed highlights、teal and orange grade、lens flare streaks、sunset orange glow、navy blue night、saturated commercial。氛围与情绪：high-octane action、commercial slickness、heroic masculinity、romantic tension、adrenaline rush、patriotic americana、glamorous danger、pop entertainment。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 3：间谍游戏 · 全球谍战

```text
【运镜】慢镜动作（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在全球谍战里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《间谍游戏》的全球谍战；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】高速剪辑与橙蓝对比交织的过曝逆光，商业动作片最鲜艳的视觉烟花。配色：主色 深蓝夜幕 `#0D1B2A` 占 25%，辅色 烈焰橙 `#FF6B00` 占 18%、电光蓝 `#1E90FF` 占 15%、暖金阳光 `#DAA520` 占 15%，点缀 小麦肤 `#F5DEB3` 占 15%、深红行动 `#8B0000` 占 12%。让主色占主导，其余按比例递减。光线：主光：backlit golden hour, overexposed highlights, strong orange-blue；高光偏 orange-gold sunset backlight explosion；阴影偏 deep navy blue；对比度：high 75-85%；整体：high-saturation orange-blue 50/50。运镜与构图：rapid montage editing、helicopter aerial shots、backlit silhouettes、slow motion action、360 degree orbits、low angle hero、lens flares、smoke steam。色彩与光影：orange-blue complementary、backlit golden hour、overexposed highlights、teal and orange grade、lens flare streaks、sunset orange glow、navy blue night、saturated commercial。氛围与情绪：high-octane action、commercial slickness、heroic masculinity、romantic tension、adrenaline rush、patriotic americana、glamorous danger、pop entertainment。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```


### 3.2 本导演可用的运镜（挑一个，别叠加）

- **直升机航拍** —— 壮丽空拍（例：《壮志凌云》飞行）
- **逆光剪影** —— 人物背光剪影（例：《壮志凌云》日落）
- **慢镜动作** —— 慢动作放大（例：《怒火救援》暴力）
- **360环绕** —— 环绕人物旋转（例：《壮志凌云》飞行员）
- **低角度英雄** —— 仰视英雄（例：《壮志凌云》航母）
- **镜头光晕** —— 光斑闪耀（例：《壮志凌云》天空）

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
【核心创意】高速剪辑与橙蓝对比交织的过曝逆光，商业动作片最鲜艳的视觉烟花。
［主体］在飞行甲板。

【分段过程描述】
[0–4s] 开场：壮志凌云 式空间。［主体动作：缓慢抬手 / 微微低头 / 顺势坐下，写清幅度和速度］。
[4–8s] 中段：［主体动作承接上一拍，写惯性衔接］。
[8–12s] 收尾：［主体停住，画面定格在 电光蓝+深蓝夜幕 的调子上］。

【声音】
overall_soundscape：（环境声 + 物理声 + 有无对白）
non_diegetic_music：（配乐；不想要就写「无配乐」）

【结束状态】画面收在［想要的那一帧］。
```

> 提示词上限约 **7000 字符**，写长不是问题，**糊成一段不分层才是**。

---

## 五、Runway / Pika

# 视频提示词模板 — 托尼·斯科特 Tony Scott风格

---

## 镜头脚本
| 镜头 | 运镜 |
|------|------|
| 镜头1 | rapid montage editing |
| 镜头2 | helicopter aerial shots |
| 镜头3 | backlit silhouettes |
| 镜头4 | slow motion action |
| 镜头5 | 360 degree orbits |
| 镜头6 | low angle hero |

## 运镜关键词
rapid montage editing, helicopter aerial shots, backlit silhouettes, slow motion action, 360 degree orbits, low angle hero, lens flares, smoke steam

## 色彩关键词
orange-blue complementary, backlit golden hour, overexposed highlights, teal and orange grade, lens flare streaks, sunset orange glow, navy blue night, saturated commercial

## 视频公式
```
A high-octane action scene in Tony Scott style, orange blue contrast, backlit golden hour lens flares, 360 camera orbit, slow motion action, helicopter aerials, heroic adrenaline, dynamic movement
```

## 负面描述
bright cheerful lighting, steady locked-off camera, clean digital look

---

> 本文件由 `色卡主文档.md` 派生（运镜特征表 / 经典场景表 / 色板 / 光影），未新增事实。
> Seedance 2.5 段的结构规则来自本机技能库 `film-cinedance/references/seedance-25-prompt-format.md`。
> 图像提示词见 `midjourney_prompts.md` · `conversational_prompts.md`。
