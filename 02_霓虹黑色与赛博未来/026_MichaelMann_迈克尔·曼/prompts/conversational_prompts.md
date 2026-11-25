# 对话式模型提示词 — 迈克尔·曼 Michael Mann 风格

> **适用**：Nano Banana（Gemini 2.5 Flash Image / Pro）· GPT-Image（含 2.5）· 即梦 · 豆包 等**对话式**生图模型
> 编号 `026` ｜ 分类 02 霓虹黑色与赛博未来 ｜ 国籍 美国

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

光线处理：主光是 digital cold blue night, practical sources, tungsten warm accents；高光偏 electronic cold blue screens neon；阴影偏 deep digital blue-black；画面对比 medium-high 65-80%；色调整体 cool steel blue noir 75/25。

画面构图上，digital cinematography、practical light sources、city night aerial、wide anamorphic framing、gunfight choreography、reflections glass water、driving plates、architectural framing。

情绪是 professional criminals、existential male loneliness、urban alienation、precision craft、fate destiny、noir fatalism、cool professionalism、LA nocturne。整体基调是数码深蓝与城市钢灰交织的夜景冷调，专业主义男性在夜色中的孤独与宿命。色彩与光影上还要照顾到 digital cold blue、steel grey urban、tungsten warm accent、practical neon、LA night chrome、anamorphic lens flares、ocean blue night、wet street reflections。

配色：主色 数码深蓝 `#0A1628` 占 35%，辅色 城市钢灰 `#2C3E50` 占 20%、电子冷蓝 `#4A90D9` 占 12%、都市暖钨 `#C4A35A` 占 12%，点缀 皮革棕 `#8B4513` 占 11%、冷钢肤 `#B0C4DE` 占 10%。情绪色只少量加入：枪口蓝 `#1E90FF`（专业精准）、枪火橙 `#FF6B35`（暴力瞬间）。让主色占绝对主导，其余颜色按上面的比例依次递减。
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
| 盗火线 | 银行枪战 | 数码深蓝+枪火橙 | 精确暴力 |
| 借刀杀人 | 出租车夜行 | 数码深蓝+电子冷蓝 | 杀手哲学 |
| 迈阿密风云 | 游艇夜色 | 电子冷蓝+暖钨灯 | 毒枭卧底 |
| 公众之敌 | 大萧条 | 皮革棕+暖钨灯 | 历史黑帮 |
| 大盗独行 | 钻石盗窃 | 数码深蓝+皮革棕 | 职业犯罪 |

**接法**（直接接在 §一 结尾）：

> ……（§一 的整段）。场景参考《盗火线》银行枪战：数码深蓝+枪火橙，情绪是精确暴力。

---

## 三、导演名怎么写

**要写，但后面必须补具体描述。** 只写「Michael Mann 风格」，模型会随机甩你一部代表作，风格完全跑偏。

✅ 正确：`Michael Mann 风格，数码深蓝与城市钢灰交织的夜景冷调，专业主义男性在夜色中的孤独与宿命。`

---

## 四、否定词怎么处理

**本导演要避开的效果**（来自色卡主文档 `style_profile.avoid`）：

- 霓虹糖果色
- 过度降噪
- 肤色橙
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
