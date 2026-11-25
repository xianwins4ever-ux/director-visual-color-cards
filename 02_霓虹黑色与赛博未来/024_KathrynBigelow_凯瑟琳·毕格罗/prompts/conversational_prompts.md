# 对话式模型提示词 — 毕格罗 Kathryn Bigelow 风格

> **适用**：Nano Banana（Gemini 2.5 Flash Image / Pro）· GPT-Image（含 2.5）· 即梦 · 豆包 等**对话式**生图模型
> 编号 `024` ｜ 分类 02 霓虹黑色与赛博未来 ｜ 国籍 美国

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

光线处理：主光是 handheld documentary natural light, harsh desert sun, night vision green；高光偏 desert gold/orange explosion；阴影偏 deep olive green-black；画面对比 high 70-85%；色调整体 cool military desaturated 60/40。

画面构图上，handheld documentary camera、shaky cam immediacy、night vision POV、wide desert vistas、tactical POV、slow motion tension、explosion aftermath、close-up on faces。

情绪是 war realism、documentary intensity、masculine violence、tactical tension、moral ambiguity、desert isolation、combat stress、anti-war。整体基调是军绿夜视与手持纪实交织的冷蓝沙漠，战争机器的肌理与男性暴力的真实凝视。色彩与光影上还要照顾到 military night vision green、desert sand ochre、olive drab military、tactical cold blue、explosion orange fire、dust and haze、desaturated war tone、documentary grain。

配色：主色 夜视深绿 `#0F1B0F` 占 30%，辅色 军绿橄榄 `#4A5D23` 占 20%、沙漠土黄 `#C4A35A` 占 15%、沙尘肤 `#B8A88A` 占 13%，点缀 战术冷蓝 `#1E3A5F` 占 12%、暗红血锈 `#8B0000` 占 10%。情绪色只少量加入：夜视绿 `#00FF00`（战术军事）、爆炸橙 `#FF4500`（战争暴力）。让主色占绝对主导，其余颜色按上面的比例依次递减。
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
| 拆弹部队 | 沙漠拆弹 | 军绿橄榄+沙漠土黄 | 紧张生存 |
| 猎杀本拉登 | 夜间突袭 | 夜视深绿+战术灰 | 战术CIA |
| 惊爆点 | 冲浪抢劫 | 战术冷蓝+沙漠金 | 极限运动 |
| K-19 | 潜艇 | 战术冷蓝+暗红血锈 | 冷战核恐惧 |
| 底特律 | 城市骚乱 | 暗红血锈+战术灰 | 种族暴力 |

**接法**（直接接在 §一 结尾）：

> ……（§一 的整段）。场景参考《拆弹部队》沙漠拆弹：军绿橄榄+沙漠土黄，情绪是紧张生存。

---

## 三、导演名怎么写

**要写，但后面必须补具体描述。** 只写「Kathryn Bigelow 风格」，模型会随机甩你一部代表作，风格完全跑偏。

✅ 正确：`Kathryn Bigelow 风格，军绿夜视与手持纪实交织的冷蓝沙漠，战争机器的肌理与男性暴力的真实凝视。`

---

## 四、否定词怎么处理

**本导演要避开的效果**（来自色卡主文档 `style_profile.avoid`）：

- 避免平光照明
- 避免色彩杂乱
- 避免构图失衡。

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
