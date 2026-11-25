# 对话式模型提示词 — 史蒂夫·麦奎因 Steve McQueen 风格

> **适用**：Nano Banana（Gemini 2.5 Flash Image / Pro）· GPT-Image（含 2.5）· 即梦 · 豆包 等**对话式**生图模型
> 编号 `047` ｜ 分类 03 大地暖调与自然光诗意 ｜ 国籍 英国

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

光线处理：主光是 painterly side lighting, natural available light, warm window bounce；高光偏 ochre gold / honey amber；阴影偏 warm brown-black / deep umber (never cool)；画面对比 medium-high 65-75%，油画般层次；色调整体 warm earth historical, 85% warm + 15% cool。

画面构图上，painterly composition、long static take、close-up endurance、natural framing、shallow depth of field isolation、handheld urgency、historical tableaux、intimate suffering。

情绪是 historical weight、quiet resistance、human dignity、intimate trauma、systemic injustice、visceral physicality、restrained passion、moral urgency。整体基调是油画般的暖暗肤色在历史的重量中静默，克制的镜头里苦难与尊严在同一束光中并存。色彩与光影上还要照顾到 warm brown skin tones、ochre historical palette、painterly chiaroscuro、deep umber shadows、honey gold highlights、earth red soil、muted desaturated color、natural daylight realism。

配色：主色 深棕油画 `#3D2817` 占 25%，辅色 赭石暖肤 `#8B6239` 占 20%、泥土红棕 `#6B4423` 占 15%、暗金历史 `#B8860B` 占 15%，点缀 暖棕墨黑 `#2C2418` 占 15%、暖土金 `#D4A574` 占 10%。情绪色只少量加入：赭红愤怒 `#A0522D`（反抗与力量）、橄榄军绿 `#556B2F`（压迫秩序）。让主色占绝对主导，其余颜色按上面的比例依次递减。
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
| 为奴十二年 | 棉花田劳作 | 深棕油画+赭石暖肤 | 历史苦难 |
| 羞耻 | 纽约都市 | 泥土红棕+冷钢灰 | 都市沉沦 |
| 寡妇联盟 | 抢劫行动 | 暖棕墨黑+暗金历史 | 女性力量 |
| 饥饿 | 监狱绝食 | 深棕油画+橄榄军绿 | 政治抗争 |
| 小斧子 | 伦敦社区 | 赭石暖肤+暖土金 | 集体记忆 |
| 红树林 | 法庭审判 | 深棕油画+赭石暖肤 | 种族正义 |

**接法**（直接接在 §一 结尾）：

> ……（§一 的整段）。场景参考《为奴十二年》棉花田劳作：深棕油画+赭石暖肤，情绪是历史苦难。

---

## 三、导演名怎么写

**要写，但后面必须补具体描述。** 只写「Steve McQueen 风格」，模型会随机甩你一部代表作，风格完全跑偏。

✅ 正确：`Steve McQueen 风格，油画般的暖暗肤色在历史的重量中静默，克制的镜头里苦难与尊严在同一束光中并存。`

---

## 四、否定词怎么处理

**本导演要避开的效果**（来自色卡主文档 `style_profile.avoid`）：

- 高饱和亮色
- 青橙调色
- 快速剪辑
- 煽情配乐与镜头
- 浪漫化苦难

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
