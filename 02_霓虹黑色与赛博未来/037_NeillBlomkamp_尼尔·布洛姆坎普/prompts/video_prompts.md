# 视频提示词 — 布洛姆坎普 Neill Blomkamp 风格

> **一个文件，四套规则。你用哪个模型，就用哪一段。**
> 编号 `037` ｜ 分类 02 霓虹黑色与赛博未来 ｜ 国籍 南非/加拿大

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
手持纪实镜头下约翰内斯堡贫民窟的脏橙铁锈与外星流体绿灰，贫富对峙中的尘土科幻与社会寓言。配色：主色 铁锈棕 `#6B4A32` 占 28%，辅色 脏橙贫民 `#C4722E` 占 22%、外星油绿灰 `#5A6B55` 占 15%、混凝土灰 `#8A8078` 占 13%，点缀 沙尘米黄 `#C2A06A` 占 12%、军警蓝灰 `#2A3A48` 占 10%。让主色占主导，其余按比例递减。光线：主光：自然硬光（非洲烈日）+手持纪实光，夜间警灯红蓝闪烁；高光偏脏橙/暖黄（非洲阳光、火光、爆炸）；阴影偏铁锈棕绿偏灰（铁皮阴影、油污暗部、建筑阴影）；对比度：高对比（70-85%），烈日下硬阴影，夜间强明暗；整体：脏调纪实科幻，70% 暖橙棕铁锈 + 30% 冷蓝绿外星/军警。运镜与构图：手持纪实晃动、伪纪录片采访、监控新闻画面、低角度仰拍机甲、尘土飞扬纵深、贫富对比构图、特写血迹/伤口、跟拍奔跑、新闻字幕叠加、军事 POV。色彩与光影：脏橙铁锈、尘土米黄、外星流体绿、军警蓝灰、警灯红蓝、爆炸火橙、硬光烈日、油污质感、垃圾美学、外星银金属。氛围与情绪：社会寓言、种族隔离隐喻、贫富悬殊、纪实科幻、暴力真实、人性灰度、企业邪恶、草根反抗、外星难民、非洲粗粝。
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
[总控] 30 秒 ｜ 竖版 9:16 ｜ 手持纪实镜头下约翰内斯堡贫民窟的脏橙铁锈与外星流体绿灰，贫富对峙中的尘土科幻与社会寓言。 ｜ 单主角 ｜ 有对白 / 无对白
[参考素材职责] 见 2.2，只留这次真正用到的

[0–4 秒 镜头 S01]《第九区》·贫民窟铁皮屋全景：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[4–9 秒 镜头 S02]《极乐空间》·地球贫民窟：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[9–16 秒 镜头 S03]《超能查派》·约堡街头黑帮：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。

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

#### 镜头 1：第九区 · 贫民窟铁皮屋全景

```text
【运镜】手持纪实晃动（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在贫民窟铁皮屋全景里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《第九区》的贫民窟铁皮屋全景；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】手持纪实镜头下约翰内斯堡贫民窟的脏橙铁锈与外星流体绿灰，贫富对峙中的尘土科幻与社会寓言。配色：主色 铁锈棕 `#6B4A32` 占 28%，辅色 脏橙贫民 `#C4722E` 占 22%、外星油绿灰 `#5A6B55` 占 15%、混凝土灰 `#8A8078` 占 13%，点缀 沙尘米黄 `#C2A06A` 占 12%、军警蓝灰 `#2A3A48` 占 10%。让主色占主导，其余按比例递减。光线：主光：自然硬光（非洲烈日）+手持纪实光，夜间警灯红蓝闪烁；高光偏脏橙/暖黄（非洲阳光、火光、爆炸）；阴影偏铁锈棕绿偏灰（铁皮阴影、油污暗部、建筑阴影）；对比度：高对比（70-85%），烈日下硬阴影，夜间强明暗；整体：脏调纪实科幻，70% 暖橙棕铁锈 + 30% 冷蓝绿外星/军警。运镜与构图：手持纪实晃动、伪纪录片采访、监控新闻画面、低角度仰拍机甲、尘土飞扬纵深、贫富对比构图、特写血迹/伤口、跟拍奔跑、新闻字幕叠加、军事 POV。色彩与光影：脏橙铁锈、尘土米黄、外星流体绿、军警蓝灰、警灯红蓝、爆炸火橙、硬光烈日、油污质感、垃圾美学、外星银金属。氛围与情绪：社会寓言、种族隔离隐喻、贫富悬殊、纪实科幻、暴力真实、人性灰度、企业邪恶、草根反抗、外星难民、非洲粗粝。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 2：极乐空间 · 地球贫民窟

```text
【运镜】监控/新闻画面（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在地球贫民窟里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《极乐空间》的地球贫民窟；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】手持纪实镜头下约翰内斯堡贫民窟的脏橙铁锈与外星流体绿灰，贫富对峙中的尘土科幻与社会寓言。配色：主色 铁锈棕 `#6B4A32` 占 28%，辅色 脏橙贫民 `#C4722E` 占 22%、外星油绿灰 `#5A6B55` 占 15%、混凝土灰 `#8A8078` 占 13%，点缀 沙尘米黄 `#C2A06A` 占 12%、军警蓝灰 `#2A3A48` 占 10%。让主色占主导，其余按比例递减。光线：主光：自然硬光（非洲烈日）+手持纪实光，夜间警灯红蓝闪烁；高光偏脏橙/暖黄（非洲阳光、火光、爆炸）；阴影偏铁锈棕绿偏灰（铁皮阴影、油污暗部、建筑阴影）；对比度：高对比（70-85%），烈日下硬阴影，夜间强明暗；整体：脏调纪实科幻，70% 暖橙棕铁锈 + 30% 冷蓝绿外星/军警。运镜与构图：手持纪实晃动、伪纪录片采访、监控新闻画面、低角度仰拍机甲、尘土飞扬纵深、贫富对比构图、特写血迹/伤口、跟拍奔跑、新闻字幕叠加、军事 POV。色彩与光影：脏橙铁锈、尘土米黄、外星流体绿、军警蓝灰、警灯红蓝、爆炸火橙、硬光烈日、油污质感、垃圾美学、外星银金属。氛围与情绪：社会寓言、种族隔离隐喻、贫富悬殊、纪实科幻、暴力真实、人性灰度、企业邪恶、草根反抗、外星难民、非洲粗粝。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 3：超能查派 · 约堡街头黑帮

```text
【运镜】低角度仰拍机甲（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在约堡街头黑帮里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《超能查派》的约堡街头黑帮；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】手持纪实镜头下约翰内斯堡贫民窟的脏橙铁锈与外星流体绿灰，贫富对峙中的尘土科幻与社会寓言。配色：主色 铁锈棕 `#6B4A32` 占 28%，辅色 脏橙贫民 `#C4722E` 占 22%、外星油绿灰 `#5A6B55` 占 15%、混凝土灰 `#8A8078` 占 13%，点缀 沙尘米黄 `#C2A06A` 占 12%、军警蓝灰 `#2A3A48` 占 10%。让主色占主导，其余按比例递减。光线：主光：自然硬光（非洲烈日）+手持纪实光，夜间警灯红蓝闪烁；高光偏脏橙/暖黄（非洲阳光、火光、爆炸）；阴影偏铁锈棕绿偏灰（铁皮阴影、油污暗部、建筑阴影）；对比度：高对比（70-85%），烈日下硬阴影，夜间强明暗；整体：脏调纪实科幻，70% 暖橙棕铁锈 + 30% 冷蓝绿外星/军警。运镜与构图：手持纪实晃动、伪纪录片采访、监控新闻画面、低角度仰拍机甲、尘土飞扬纵深、贫富对比构图、特写血迹/伤口、跟拍奔跑、新闻字幕叠加、军事 POV。色彩与光影：脏橙铁锈、尘土米黄、外星流体绿、军警蓝灰、警灯红蓝、爆炸火橙、硬光烈日、油污质感、垃圾美学、外星银金属。氛围与情绪：社会寓言、种族隔离隐喻、贫富悬殊、纪实科幻、暴力真实、人性灰度、企业邪恶、草根反抗、外星难民、非洲粗粝。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```


### 3.2 本导演可用的运镜（挑一个，别叠加）

- **手持纪实晃动** —— 伪纪录片风格，新闻采访质感（例：《第九区》全片纪实风格、采访镜头）
- **监控/新闻画面** —— 穿插 CCTV/新闻直播画面（例：《第九区》新闻播报、MNU 监控）
- **低角度仰拍机甲** —— 机甲/外星武器的压迫感（例：《第九区》外骨骼机甲、《极乐空间》守卫机器人）
- **尘土纵深跟拍** —— 尘土飞扬中跟拍人物奔跑（例：《第九区》贫民窟穿行、《查派》约堡街头）
- **特写创伤变形** —— 伤口/变异/机械改造的特写（例：《第九区》Wikus 手臂变异、外星流体）
- **贫富并置构图** —— 同一画面中贫/富两个世界（例：《极乐空间》地球贫民窟 vs 太空站）

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
【核心创意】手持纪实镜头下约翰内斯堡贫民窟的脏橙铁锈与外星流体绿灰，贫富对峙中的尘土科幻与社会寓言。
［主体］在贫民窟铁皮屋全景。

【分段过程描述】
[0–4s] 开场：第九区 式空间。［主体动作：缓慢抬手 / 微微低头 / 顺势坐下，写清幅度和速度］。
[4–8s] 中段：［主体动作承接上一拍，写惯性衔接］。
[8–12s] 收尾：［主体停住，画面定格在 脏橙贫民+铁锈棕+沙尘米黄 的调子上］。

【声音】
overall_soundscape：（环境声 + 物理声 + 有无对白）
non_diegetic_music：（配乐；不想要就写「无配乐」）

【结束状态】画面收在［想要的那一帧］。
```

> 提示词上限约 **7000 字符**，写长不是问题，**糊成一段不分层才是**。

---

## 五、Runway / Pika

## 二、场景镜头模板

### 镜头 1：贫民窟建立镜头（Establishing Shot）

**提示词：**
```
Aerial documentary shot slowly panning over a vast shantytown,
Neill Blomkamp District 9 style,
endless corrugated iron shacks in dirty orange and rust brown,
dirt roads winding between the shacks,
a massive alien spacecraft hovering silently above the settlement,
MNU military trucks driving along a road, dust trailing behind,
hard African sunlight bleaching everything with warm orange tones,
sand and dust blowing across the landscape,
small human and alien figures moving below,
documentary news footage aesthetic, handheld camera feel,
text overlay graphics suggesting news report,
gritty social sci-fi, wide shot,
16:9 aspect ratio, slow pan movement
```

**镜头参数：**
- 时长：7-9秒
- 运镜：缓慢航拍横摇（slow aerial pan）
- 节奏：缓慢、纪实、压抑

---

### 镜头 2：手持奔跑追逐（Handheld Chase）

**提示词：**
```
Handheld camera running through narrow dirt alleyways between corrugated iron shacks,
Neill Blomkamp District 9 style,
following a man in a stained shirt running desperately,
dust kicking up under his feet,
alien graffiti on shack walls,
hard sunlight creating sharp shadows between buildings,
he looks back over his shoulder in panic,
military shouts heard off screen,
a mech suit appears at the end of the alley,
shaky documentary camera, found footage feel,
dirty orange rust and beige color palette,
fast pace, urgent breathing implied,
16:9 aspect ratio, hand-held running camera
```

**镜头参数：**
- 时长：5-7秒
- 运镜：手持奔跑跟拍（handheld running POV）
- 节奏：快速、紧张、恐慌

---

### 镜头 3：外星武器交易（Alien Weapon Deal）

**提示词：**
```
Inside a dark corrugated iron shack, dimly lit by a single bare bulb,
Neill Blomkamp District 9 style,
an alien prawn creature with insect-like face hands over a bizarre bio-mechanical weapon,
the weapon pulses with faint alien green-gray energy,
a Nigerian gang leader in a suit takes it, examining it greedily,
rusted walls, stacks of alien technology canisters,
dust motes floating in the dirty orange light beam,
close quarters, tense atmosphere,
documentary close-up style, subtle handheld movement,
gritty hyperrealism, low light,
16:9 aspect ratio, slow push in
```

**镜头参数：**
- 时长：5-7秒
- 运镜：缓慢推近（slow push in），微幅手持
- 节奏：紧张、压抑、危险

---

### 镜头 4：外骨骼机甲崛起（Mech Suit Rise）

**提示词：**
```
A man in a bio-mechanical alien exosuit rises from dust and debris in a slum street,
Neill Blomkamp District 9 style,
the suit is a mix of rust brown metal and alien silver organic components,
hydraulics hiss as he stands up to full height,
hard backlight from an explosion behind casting orange fire glow,
MNU soldiers freeze in fear,
the mech suit's alien weapons power up with blue energy glow,
dust and debris blow in the shockwave,
low angle shot looking up at the imposing figure,
slow motion as he rises, heroic yet terrifying,
gritty action cinema, explosion fire lighting,
16:9 aspect ratio, slow motion low angle
```

**镜头参数：**
- 时长：6-8秒
- 运镜：低角度慢动作（low angle slow motion）
- 节奏：慢动作、悲壮、力量爆发

---

### 镜头 5：极乐空间俯瞰（Elysium Overview）

**提示词：**
```
From low Earth orbit looking down at a smog-choked Los Angeles,
Neill Blomkamp Elysium style,
the planet surface is covered in dirty orange smog and endless sprawl,
above in orbit, the pristine silver-white ring of Elysium space station gleams,
perfect green atmosphere and mansions visible on the station,
sharp contrast between polluted Earth and utopian station,
police drones fly between the two worlds,
the camera slowly pulls back revealing more of the class divide,
cold silver of space station against warm orange of Earth,
epic sci-fi cinematic shot, slow pull back,
2.35:1 anamorphic aspect ratio, film grain
```

**镜头参数：**
- 时长：6-8秒
- 运镜：缓慢拉远（slow pull back from orbit）
- 节奏：宏大、冰冷、阶级对比

---

### 镜头 6：查派夜间诞生（Chappie Night Birth）

**提示词：**
```
A damaged yellow police robot powers on in a Johannesburg warehouse at night,
Neill Blomkamp Chappie style,
his LED eyes flicker to life with warm yellow glow,
red and blue police lights flash through broken windows,
gang members with gold chains watch in amazement,
the robot looks at his own metal hands with childlike wonder,
sparks fly from damaged wiring on his shoulder,
dirty orange sodium light spills in from street outside,
rain visible through the broken windows,
graffiti covers the walls,
the robot takes his first wobbly steps,
documentary handheld medium shot,
red blue orange color palette,
16:9 aspect ratio, intimate handheld movement
```

**镜头参数：**
- 时长：6-8秒
- 运镜：手持中近景（intimate handheld medium shot）
- 节奏：奇迹感、纯真诞生、粗粝中的温柔

---

## 三、运镜关键词速查

| 运镜效果 | 英文关键词 |
|---------|-----------|
| 手持纪实 | handheld camera, documentary style, found footage, shaky cam |
| 跟拍奔跑 | running chase, tracking through alleys, following on foot |
| 低角度机甲 | low angle mech shot, looking up at robot, towering exosuit |
| 航拍建立 | aerial establishing shot, drone documentary view, news helicopter |
| 监控新闻 | security camera POV, CCTV footage, news broadcast overlay |
| 慢动作爆炸 | slow motion explosion, fire blast shockwave, debris flying |
| 警灯闪烁 | red and blue police lights flashing, siren light pulse |
| 尘土飞扬 | dust blowing, dirt kick up, sand particles in air |

---

## 四、颜色与光影关键词

| 效果 | 英文关键词 |
|------|-----------|
| 脏橙铁锈 | dirty orange rust, corrugated iron brown, rust palette |
| 非洲烈日 | hard African sunlight, harsh midday sun, sharp shadows |
| 沙尘米黄 | sand dust beige, dust haze, dry earth tones |
| 外星绿灰 | alien green-gray fluid, bio-mechanical growth, organic tech |
| 军警蓝灰 | military blue-gray, armor plate, corporate police |
| 警灯红蓝 | red and blue police lights, siren flash, emergency lighting |
| 爆炸火橙 | explosion fire orange, muzzle flash, blast glow |
| 外星银 | alien silver tech, bio-mechanical metal, otherworldly alloy |

---

## 五、负面描述（避免的效果）

```
clean future, utopian city, sleek polished surfaces,
glossy CGI effects, star wars, star trek,
bright saturated colors, fantasy magic, superheroes,
lush green forests, blue sky paradise, nature,
anime style, cartoon, pixar animation,
steady smooth camera, steadycam perfection,
wealthy interiors, luxury, clean laboratories,
romantic lighting, golden hour beauty, fashion photography
```

---

> 本文件由 `色卡主文档.md` 派生（运镜特征表 / 经典场景表 / 色板 / 光影），未新增事实。
> Seedance 2.5 段的结构规则来自本机技能库 `film-cinedance/references/seedance-25-prompt-format.md`。
> 图像提示词见 `midjourney_prompts.md` · `conversational_prompts.md`。
