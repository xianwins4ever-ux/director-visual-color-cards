# 对话式模型提示词 — 阿方索·卡隆 Alfonso Cuarón 风格

> **适用**：Nano Banana（Gemini 2.5 Flash Image / Pro）· GPT-Image（含 2.5）· 即梦 · 豆包 等**对话式**生图模型
> 编号 `043` ｜ 分类 03 大地暖调与自然光诗意 ｜ 国籍 墨西哥

---

## 0 · 用之前先知道这三条

1. **吃自然语言段落，不吃逗号堆叠的关键词** —— 把 §一 整段复制进去，**不要拆成标签**
2. **不认 `--ar` `--s` `--style raw` 这类参数** —— 画幅在界面里选
3. **否定词基本无效** —— 写「不要出现车」反而会给你车，要改成正向描述（见 §四）

> ▶ **想要风格最接近原片，优先用 `midjourney_prompts.md`。** 原因见文末 §五。

---

## 一、通用描述段（整段复制，只改「［主体］」）

```text
创建一张电影感画面。［主体］。

光线处理：主光是 natural available light, long take continuous lighting, soft window bounce；高光偏 warm gold / amber memory；阴影偏 cool steel blue / warm umber；画面对比 medium 50-65%，依场景跨度极大；色调整体 warm memory + cold reality, 60% warm + 40% cool。

画面构图上，long take immersion、zero-gravity fluid camera、wide-angle depth、handheld documentary、child's eye low angle、360-degree spatial camera、natural framing、silent long shot。

情绪是 memory and longing、isolation in vastness、childhood innocence lost、human connection、gravity and weightlessness、political urgency、poetic realism、quiet resilience。整体基调是长镜头沉浸于记忆与宇宙之间，暖金色的回忆柔光与黑白纪实的冷峻诗意在银幕上彼此呼应。色彩与光影上还要照顾到 warm golden memory tones、black and white stark realism、cool steel blue space、earth brown post-apocalypse、soft morning light、dust motes in sunbeam、rain-washed street、fire in darkness。

配色：主色 暖金回忆 `#D4A574` 占 22%，辅色 土黄街景 `#B89968` 占 18%、深空黑 `#2C2C2C` 占 15%、冷钢蓝灰 `#6B8E9A` 占 15%，点缀 橄榄棕 `#8B7355` 占 15%、柔光米白 `#E8D5B7` 占 15%。情绪色只少量加入：记忆金 `#F4C430`（童年回望）、太空蓝 `#4A6FA5`（孤独浩瀚）。让主色占绝对主导，其余颜色按上面的比例依次递减。
```

> **「［主体］」写什么？** 越具体越好 —— 谁、在做什么、穿什么、周围有什么。
> 不写「一个女孩」，写「一个穿深绿色套装的女性，站在昏暗走廊尽头，回头看镜头」。
>
> **画幅不用写进上面那段**，在界面里选（竖版 / 方图 / 宽银幕）。

---

## 二、经典场景怎么套

从下面挑一个，接在 §一 后面当第二句：

| 电影 | 场景 | 主导色 | 色彩氛围 |
|---|---|---|---|
| 罗马 | 街区日常 | 暖金回忆+土黄街景 | 童年诗意 |
| 地心引力 | 太空漂流 | 深空黑+冷钢蓝灰 | 孤独浩瀚 |
| 人类之子 | 末世街道 | 橄榄棕+赭石红 | 末世人性 |
| 阿兹卡班 | 魔法校园 | 冷钢蓝灰+暖金回忆 | 魔法青春 |
| 你妈妈也一样 | 公路旅行 | 土黄街景+暖金回忆 | 青春觉醒 |
| 哈利波特与阿兹卡班的囚徒 | 哈利波特与阿兹卡班的囚徒 | 冷钢蓝灰+暖金回忆 | 魔法青春 |

**接法**（直接接在 §一 结尾）：

> ……（§一 的整段）。场景参考《罗马》街区日常：暖金回忆+土黄街景，情绪是童年诗意。

---

## 三、导演名怎么写

**要写，但后面必须补具体描述。** 只写「Alfonso Cuarón 风格」，模型会随机甩你一部代表作，风格完全跑偏。

✅ 正确：`Alfonso Cuarón 风格，长镜头沉浸于记忆与宇宙之间，暖金色的回忆柔光与黑白纪实的冷峻诗意在银幕上彼此呼应。`

---

## 四、否定词怎么处理

**本导演要避开的效果**（来自色卡主文档 `style_profile.avoid`）：

- 炫彩 LUT
- 切碎长动作
- 不连续曝光
- 无动机环绕和随机变焦
- 用统一滤镜替代色彩比例
- 光源和材质。

**别写成「不要 XXX」**，改成正向描述。
例：把「不要廉价黑场」写成「暗部保留层次，阴影里有可辨认的细节」。

---

## 五、为什么推荐优先用 Midjourney

**同样一条提示词，MJ 出来的风格最接近原片。** 三个原因：

1. **MJ 是「审美优先」，这两类是「听话优先」。**
   MJ 会替你往艺术方向处理（氛围、光比、质感）；Nano Banana / GPT-Image 更擅长**精确执行你的字面指令** ——
   你说什么它给什么，但不会主动帮你加电影感。同一句描述，MJ 的成片往往是画册级，这两类是「干净但偏平」。
2. **这套提示词本来就是按 MJ 的原生语法蒸馏的**（逗号标签 + 权重排序 + 参数）。
   在 MJ 上它是「母语」，在对话式模型上要**转译**，一转译必然有损耗。
3. **MJ 有 `--s`（stylize）这个「艺术化总旋钮」**，可以整体加强风格浓度；
   对话式模型没有这个旋钮，只能靠把风格写得更细来补。

**什么时候反而该用它们**

| 场景 | 用谁 |
|---|---|
| 要出一张**惊艳的风格图** | ✅ **Midjourney** |
| 要**改图**（换背景、保脸、多图融合） | Nano Banana |
| 图里要**写准确文字**、严格按排版出图 | GPT-Image |
| 要**批量、快速、便宜**试方向 | Nano Banana（对话式改起来最快） |
| 要**连续短视频镜头** | `video_prompts.md`（Seedance / 可灵） |

---

> 本文件由 `色卡主文档.md` 与 `palette.json` 派生，未新增事实。
> 完整色板与来源说明见 `色卡主文档.md`；英文参数版见 `midjourney_prompts.md`。
