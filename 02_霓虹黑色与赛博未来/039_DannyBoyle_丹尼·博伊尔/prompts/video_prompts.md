# 视频提示词 — 丹尼·博伊尔 Danny Boyle 风格

> **一个文件，四套规则。你用哪个模型，就用哪一段。**
> 编号 `039` ｜ 分类 02 霓虹黑色与赛博未来 ｜ 国籍 英国

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
快速剪辑下迷幻脏绿与霓虹都市的癫狂碰撞，孟买暖黄与病毒冷绿的两极跳跃，毒品、爱情与末日的视觉肾上腺素。配色：主色 迷幻脏绿 `#3D5C28` 占 22%，辅色 孟买暖黄 `#D4A020` 占 20%、霓虹橙红 `#E04020` 占 16%、毒幻蓝紫 `#3A2E5C` 占 14%，点缀 废弃灰 `#707068` 占 14%、皮肤暖棕 `#A07048` 占 14%。让主色占主导，其余按比例递减。光线：主光：狂乱手持+快速跳切光，极端冷暖交替，自然光与色光混用；高光偏暖黄/霓虹橙（阳光、毒品狂躁、印度暖光）；阴影偏脏绿/蓝紫（毒幻、末日、病态暗部）；对比度：高对比但饱和度跳跃（60-90% 两极），从极度去饱和到极度饱和；整体：迷幻两极，50% 暖黄橙红 + 50% 冷绿蓝紫，快速剪辑跳跃。运镜与构图：快速跳切、手持狂晃、鱼眼畸变、低角度扭曲、主观毒幻视角、奔跑跟拍、字幕插入、分割画面、极速推拉、超现实插入。色彩与光影：迷幻脏绿、孟买暖黄、霓虹橙红、毒幻蓝紫、末日冷绿、狂喜金黄、病毒血红、高饱和跳跃、极端冷暖、色光染色。氛围与情绪：狂躁能量、毒品迷幻、底层生命力、末日恐惧、黑色幽默、爱与救赎、英国愤怒、印度喧嚣、肾上腺素、存在荒诞。
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
[总控] 30 秒 ｜ 竖版 9:16 ｜ 快速剪辑下迷幻脏绿与霓虹都市的癫狂碰撞，孟买暖黄与病毒冷绿的两极跳跃，毒品、爱情与末日的视觉肾上腺素。 ｜ 单主角 ｜ 有对白 / 无对白
[参考素材职责] 见 2.2，只留这次真正用到的

[0–4 秒 镜头 S01]《猜火车》·开场"选择生活"奔跑：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[4–9 秒 镜头 S02]《贫民窟》·孟买贫民窟童年：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[9–16 秒 镜头 S03]《28天后》·空城伦敦：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。
[16–30 秒 镜头 S04]《太阳浩劫》·太阳接近：<先写首帧完整状态：人物／位置／朝向／姿势／道具／场景／光源／轴线>，然后<动作 ＋ 表演 ＋ 准确对白 ＋ 摄影机运动 ＋ 结束状态>。

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

#### 镜头 1：猜火车 · 开场"选择生活"奔跑

```text
【运镜】快速跳切剪辑（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在开场"选择生活"奔跑里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《猜火车》的开场"选择生活"奔跑；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】快速剪辑下迷幻脏绿与霓虹都市的癫狂碰撞，孟买暖黄与病毒冷绿的两极跳跃，毒品、爱情与末日的视觉肾上腺素。配色：主色 迷幻脏绿 `#3D5C28` 占 22%，辅色 孟买暖黄 `#D4A020` 占 20%、霓虹橙红 `#E04020` 占 16%、毒幻蓝紫 `#3A2E5C` 占 14%，点缀 废弃灰 `#707068` 占 14%、皮肤暖棕 `#A07048` 占 14%。让主色占主导，其余按比例递减。光线：主光：狂乱手持+快速跳切光，极端冷暖交替，自然光与色光混用；高光偏暖黄/霓虹橙（阳光、毒品狂躁、印度暖光）；阴影偏脏绿/蓝紫（毒幻、末日、病态暗部）；对比度：高对比但饱和度跳跃（60-90% 两极），从极度去饱和到极度饱和；整体：迷幻两极，50% 暖黄橙红 + 50% 冷绿蓝紫，快速剪辑跳跃。运镜与构图：快速跳切、手持狂晃、鱼眼畸变、低角度扭曲、主观毒幻视角、奔跑跟拍、字幕插入、分割画面、极速推拉、超现实插入。色彩与光影：迷幻脏绿、孟买暖黄、霓虹橙红、毒幻蓝紫、末日冷绿、狂喜金黄、病毒血红、高饱和跳跃、极端冷暖、色光染色。氛围与情绪：狂躁能量、毒品迷幻、底层生命力、末日恐惧、黑色幽默、爱与救赎、英国愤怒、印度喧嚣、肾上腺素、存在荒诞。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 2：贫民窟 · 孟买贫民窟童年

```text
【运镜】手持狂晃奔跑（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在孟买贫民窟童年里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《贫民窟》的孟买贫民窟童年；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】快速剪辑下迷幻脏绿与霓虹都市的癫狂碰撞，孟买暖黄与病毒冷绿的两极跳跃，毒品、爱情与末日的视觉肾上腺素。配色：主色 迷幻脏绿 `#3D5C28` 占 22%，辅色 孟买暖黄 `#D4A020` 占 20%、霓虹橙红 `#E04020` 占 16%、毒幻蓝紫 `#3A2E5C` 占 14%，点缀 废弃灰 `#707068` 占 14%、皮肤暖棕 `#A07048` 占 14%。让主色占主导，其余按比例递减。光线：主光：狂乱手持+快速跳切光，极端冷暖交替，自然光与色光混用；高光偏暖黄/霓虹橙（阳光、毒品狂躁、印度暖光）；阴影偏脏绿/蓝紫（毒幻、末日、病态暗部）；对比度：高对比但饱和度跳跃（60-90% 两极），从极度去饱和到极度饱和；整体：迷幻两极，50% 暖黄橙红 + 50% 冷绿蓝紫，快速剪辑跳跃。运镜与构图：快速跳切、手持狂晃、鱼眼畸变、低角度扭曲、主观毒幻视角、奔跑跟拍、字幕插入、分割画面、极速推拉、超现实插入。色彩与光影：迷幻脏绿、孟买暖黄、霓虹橙红、毒幻蓝紫、末日冷绿、狂喜金黄、病毒血红、高饱和跳跃、极端冷暖、色光染色。氛围与情绪：狂躁能量、毒品迷幻、底层生命力、末日恐惧、黑色幽默、爱与救赎、英国愤怒、印度喧嚣、肾上腺素、存在荒诞。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```

#### 镜头 3：28天后 · 空城伦敦

```text
【运镜】毒幻主观视角（只写这一种），速度缓慢、稳定
【主体动作与表情】［主体动作］在空城伦敦里，写清肢体部位、幅度与速度
【位置或空间变化】空间参考《28天后》的空城伦敦；主体位置与前后景关系写一句
【音频】环境声：（照场景补）；有无对白要写清
【风格与画质】快速剪辑下迷幻脏绿与霓虹都市的癫狂碰撞，孟买暖黄与病毒冷绿的两极跳跃，毒品、爱情与末日的视觉肾上腺素。配色：主色 迷幻脏绿 `#3D5C28` 占 22%，辅色 孟买暖黄 `#D4A020` 占 20%、霓虹橙红 `#E04020` 占 16%、毒幻蓝紫 `#3A2E5C` 占 14%，点缀 废弃灰 `#707068` 占 14%、皮肤暖棕 `#A07048` 占 14%。让主色占主导，其余按比例递减。光线：主光：狂乱手持+快速跳切光，极端冷暖交替，自然光与色光混用；高光偏暖黄/霓虹橙（阳光、毒品狂躁、印度暖光）；阴影偏脏绿/蓝紫（毒幻、末日、病态暗部）；对比度：高对比但饱和度跳跃（60-90% 两极），从极度去饱和到极度饱和；整体：迷幻两极，50% 暖黄橙红 + 50% 冷绿蓝紫，快速剪辑跳跃。运镜与构图：快速跳切、手持狂晃、鱼眼畸变、低角度扭曲、主观毒幻视角、奔跑跟拍、字幕插入、分割画面、极速推拉、超现实插入。色彩与光影：迷幻脏绿、孟买暖黄、霓虹橙红、毒幻蓝紫、末日冷绿、狂喜金黄、病毒血红、高饱和跳跃、极端冷暖、色光染色。氛围与情绪：狂躁能量、毒品迷幻、底层生命力、末日恐惧、黑色幽默、爱与救赎、英国愤怒、印度喧嚣、肾上腺素、存在荒诞。
【约束】画面抖动、多余肢体、手指畸形、面部漂移、文字水印、物体变形、闪烁跳帧、重复物体、光线杂乱
```


### 3.2 本导演可用的运镜（挑一个，别叠加）

- **快速跳切剪辑** —— 极短镜头快速切换，肾上腺素感（例：《猜火车》开场选择生活、《贫民窟》问答闪回）
- **手持狂晃奔跑** —— 跟拍人物奔跑的手持晃动（例：《猜火车》街头奔跑、《28 天后》空城奔跑）
- **毒幻主观视角** —— 吸毒后的扭曲/畸变/超现实画面（例：《猜火车》钻入马桶、天花板婴儿）
- **鱼眼/广角畸变** —— 极端广角造成的空间扭曲感（例：《猜火车》戒毒房间、《28 天后》空城）
- **字幕/文字插入** —— 画面中直接插入文字、选择项（例：《猜火车》"Choose Life"开场）
- **交叉闪回** —— 多条时间线快速交叉剪辑（例：《贫民窟》节目问答闪回、《127 小时》回忆）

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
【核心创意】快速剪辑下迷幻脏绿与霓虹都市的癫狂碰撞，孟买暖黄与病毒冷绿的两极跳跃，毒品、爱情与末日的视觉肾上腺素。
［主体］在开场"选择生活"奔跑。

【分段过程描述】
[0–4s] 开场：猜火车 式空间。［主体动作：缓慢抬手 / 微微低头 / 顺势坐下，写清幅度和速度］。
[4–8s] 中段：［主体动作承接上一拍，写惯性衔接］。
[8–12s] 收尾：［主体停住，画面定格在 霓虹橙红+废弃灰+迷幻脏绿 的调子上］。

【声音】
overall_soundscape：（环境声 + 物理声 + 有无对白）
non_diegetic_music：（配乐；不想要就写「无配乐」）

【结束状态】画面收在［想要的那一帧］。
```

> 提示词上限约 **7000 字符**，写长不是问题，**糊成一段不分层才是**。

---

## 五、Runway / Pika

## 二、场景镜头模板

### 镜头 1：选择生活开场（Choose Life Opening）

**提示词：**
```
Fast-paced opening sequence of young men running through gray Edinburgh streets,
Danny Boyle Trainspotting style,
neon orange text flashes "CHOOSE LIFE" on screen,
handheld camera sprinting with them, shaky energetic movement,
they laugh and run from security/police,
quick jump cuts between their faces and the street,
sickly green Scottish architecture, gray concrete,
neon orange and red energy pulses through the scene,
narcotic euphoria, punk rock energy,
quick cuts, fast pace, adrenaline pumping,
opening credits style text inserts,
16mm film grain, hyper saturated, 16:9 aspect ratio
```

**镜头参数：**
- 时长：7-9秒
- 运镜：手持冲刺跟拍（handheld sprint）
- 节奏：极快、跳切、肾上腺素

---

### 镜头 2：钻入马桶（Worst Toilet Dive）

**提示词：**
```
A desperate young man dives headfirst into the filthiest toilet in Scotland,
Danny Boyle Trainspotting style,
the moment he submerges the world transforms --
he's suddenly swimming in crystal clear blue ocean depths,
narcotic blue-purple underwater lighting,
sickly green replaced by beautiful clear blue,
surreal drug-trip transition,
he swims deeper searching for something,
psychedelic underwater beauty,
the camera follows him diving down,
extreme visual contrast between filthy and beautiful,
dark comedy, surreal drug sequence,
transition shot, color palette shifts dramatically, 16:9
```

**镜头参数：**
- 时长：5-7秒
- 运镜：跟随下潜（follow dive）
- 节奏：恶心→超现实转换，毒幻感

---

### 镜头 3：空城伦敦漫步（Empty London Walk）

**提示词：**
```
A man in hospital scrubs walks alone through completely empty London streets,
Danny Boyle 28 Days Later style,
eerie cold green-gray light, completely deserted,
no cars, no people, papers blowing in the wind,
he stops and looks around in confusion and fear,
red double-decker bus abandoned sideways in the road,
his footsteps echo on empty pavement,
the camera slowly circles him in the vast emptiness,
sickly pale green overcast sky,
post-apocalyptic silence and dread,
wide-angle lens making spaces feel larger and lonelier,
slow deliberate camera, haunting atmosphere,
16:9 aspect ratio, cold green-gray palette
```

**镜头参数：**
- 时长：8-10秒
- 运镜：缓慢环绕（slow circling / orbit）
- 节奏：极慢、恐怖、死寂

---

### 镜头 4：孟买追逐（Mumbai Chase）

**提示词：**
```
Young Indian boys running at full speed through Mumbai slum alleyways,
Danny Boyle Slumdog Millionaire style,
warm golden hour sunlight flooding narrow corridors,
vibrant pink and orange saris hanging on lines brushing past them,
they weave through crowds, jump over obstacles,
dust and golden particles in the air,
colorful street vendors and shouting people on all sides,
handheld camera running right behind them,
quick jump cuts between their laughing determined faces and the chaos,
warm yellow and gold with explosions of red and pink,
pure kinetic energy and life force,
poverty but with enormous vitality,
fast paced chase, 16:9 aspect ratio
```

**镜头参数：**
- 时长：6-8秒
- 运镜：手持奔跑跟拍（handheld running chase）
- 节奏：极快、生命力、喧嚣

---

### 镜头 5：太阳之死（Sun Death）

**提示词：**
```
Astronauts on a spaceship facing the massive overwhelming sun,
Danny Boyle Sunshine style,
blinding ecstatic golden yellow light floods everything,
the sun's surface roils with golden plasma and solar flares,
golden light bleaches the frame almost to white,
cold deep blue-black space visible at edges,
one astronaut reaches out toward the light,
religious awe, existential sacrifice,
the camera slowly pushes into the golden light,
overwhelming brilliance and heat implied,
gold and black extreme contrast,
beautiful and terrifying simultaneously,
epic cinematic, 2.35:1 aspect ratio
```

**镜头参数：**
- 时长：6-8秒
- 运镜：缓慢推入金光（slow push into gold light）
- 节奏：庄严肃穆、超验、神性

---

### 镜头 6：峡谷卡住觉醒（Canyon Realization）

**提示词：**
```
A man trapped between canyon walls looks up at the narrow strip of blue sky above,
Danny Boyle 127 Hours style,
red-orange canyon rock walls pressing in on him,
bright blue sky visible only in a thin strip far above,
sunlight moves across the rock face as time passes,
flashbacks flicker briefly -- memories, people, moments --
quick surreal inserts of his past life flashing before him,
warm orange-red rock against blue sky,
his face shows determination and terror,
time-lapse sun movement implied,
kinetic survival energy,
close-up to extreme wide contrast,
warm canyon palette with blue sky, 16:9 aspect ratio
```

**镜头参数：**
- 时长：6-8秒
- 运镜：近景→远景闪回切换
- 节奏：绝境→闪回→求生决心

---

## 三、运镜关键词速查

| 运镜效果 | 英文关键词 |
|---------|-----------|
| 手持冲刺 | handheld running, sprinting camera, shaky chase cam |
| 快速跳切 | fast jump cuts, rapid editing, staccato cuts, quick inserts |
| 鱼眼广角 | fisheye lens, extreme wide angle, distorted perspective |
| 毒幻主观 | subjective drug POV, hallucination camera, warping lens |
| 字幕插入 | text on screen, title cards, words flashing, typography |
| 交叉闪回 | flash cuts, memory inserts, quick cross-cutting timelines |
| 慢→快转换 | slow to fast contrast, building speed, accelerating pace |
| 超现实插入 | surreal inserts, fantasy sequences, animation cutaways |

---

## 四、颜色与光影关键词

| 效果 | 英文关键词 |
|------|-----------|
| 迷幻脏绿 | sickly green, psychedelic green, narcotic green haze |
| 霓虹橙红 | neon orange-red, fiery orange glow, punk orange |
| 孟买暖黄 | golden Mumbai sunlight, warm saffron yellow, Indian gold |
| 毒幻蓝紫 | narcotic blue-purple, drug haze purple, club violet |
| 末日冷绿 | cold apocalypse green, eerie gray-green, infected green tint |
| 狂喜金黄 | blinding golden light, ecstatic yellow, sun worship gold |
| 病毒血红 | blood red violence, virus red, rage crimson |
| 高饱和跳跃 | extreme color saturation, color jumps, palette shifts |

---

## 五、负面描述（避免的效果）

```
slow cinema, meditative pace, static camera,
clean polished aesthetic, sterile white rooms,
calm peaceful mood, serene tranquil,
steady tripod shots, smooth hollywood camera,
anime style, cartoon, pixar animation,
low contrast, flat desaturated gray, muted tones,
luxury settings, wealthy interiors,
romantic comedy, warm cozy lighting,
studio gloss, cgi overload, superhero style
```

---

> 本文件由 `色卡主文档.md` 派生（运镜特征表 / 经典场景表 / 色板 / 光影），未新增事实。
> Seedance 2.5 段的结构规则来自本机技能库 `film-cinedance/references/seedance-25-prompt-format.md`。
> 图像提示词见 `midjourney_prompts.md` · `conversational_prompts.md`。
