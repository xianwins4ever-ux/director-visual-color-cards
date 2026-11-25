# 对话式模型提示词 — 卢贝兹基 Emmanuel Lubezki 风格

> **适用**：Nano Banana（Gemini 2.5 Flash Image / Pro）· GPT-Image（含 2.5）· 即梦 · 豆包 等**对话式**生图模型
> 编号 `059` ｜ 分类 03 大地暖调与自然光诗意 ｜ 国籍 墨西哥

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

光线处理：主光是 natural light only, golden hour magic hour, soft overcast diffusion；高光偏 golden amber / sunrise orange；阴影偏 cool forest green / blue-grey；画面对比 medium 55-70%；色调整体 warm natural light, 60% warm + 40% cool。

画面构图上，long continuous take、360-degree camera movement、natural light only、golden hour magic hour、handheld intimacy、wide-angle immersion、breathing camera、nature as character。

情绪是 spiritual transcendence、primal survival、theatrical intimacy、cosmic wonder、breathing existence、raw nature power、human vulnerability、dreamlike flow。整体基调是自然光长镜头与黄金时刻的呼吸感，光影如生命般流动的诗意影像。色彩与光影上还要照顾到 golden hour sunrise、tundra moss green、frosty blue-grey、warm skin tones、earth ochre brown、dawn twilight purple、firelight orange、snowy white purity。

配色：主色 黄金时刻 `#E6B86A` 占 22%，辅色 苔原冷绿 `#4A6B5C` 占 18%、黎明深灰 `#2E3138` 占 15%、暖沙肤色 `#D9C2A0` 占 15%，点缀 冰湖蓝灰 `#6B8E9A` 占 15%、大地赭石 `#9B7E5C` 占 15%。情绪色只少量加入：日出火 `#FF7F50`（生命觉醒）、极光紫 `#9370DB`（神秘超越）。让主色占绝对主导，其余颜色按上面的比例依次递减。
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
| 荒野猎人 | 雪林求生 | 黄金时刻+苔原冷绿 | 原始生存 |
| 鸟人 | 百老汇后台 | 黎明深灰+暖沙肤色 | 戏剧迷狂 |
| 地心引力 | 太空漂浮 | 冰湖蓝灰+暖沙肤色 | 宇宙孤独 |
| 人类之子 | 末世伦敦 | 大地赭石+苔原冷绿 | 末世希望 |
| 生命之树 | 童年回忆 | 黄金时刻+霜雾白 | 宇宙诗意 |
| 大鱼 | 奇幻旅程 | 黄金时刻+暖沙肤色 | 童话回忆 |

**接法**（直接接在 §一 结尾）：

> ……（§一 的整段）。场景参考《荒野猎人》雪林求生：黄金时刻+苔原冷绿，情绪是原始生存。

---

## 三、导演名怎么写

**要写，但后面必须补具体描述。** 只写「Emmanuel Lubezki 风格」，模型会随机甩你一部代表作，风格完全跑偏。

✅ 正确：`Emmanuel Lubezki 风格，自然光长镜头与黄金时刻的呼吸感，光影如生命般流动的诗意影像。`

---

## 四、否定词怎么处理

**本导演要避开的效果**（来自色卡主文档 `style_profile.avoid`）：

- 人工打光痕迹
- 统一调色滤镜
- 快速剪辑碎切
- 稳定器过度平滑
- 用棚拍光效替代真实自然光影

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
