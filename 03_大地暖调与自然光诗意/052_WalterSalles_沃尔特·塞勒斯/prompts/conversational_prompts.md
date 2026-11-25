# 对话式模型提示词 — 沃尔特·塞勒斯 Walter Salles 风格

> **适用**：Nano Banana（Gemini 2.5 Flash Image / Pro）· GPT-Image（含 2.5）· 即梦 · 豆包 等**对话式**生图模型
> 编号 `052` ｜ 分类 03 大地暖调与自然光诗意 ｜ 国籍 巴西

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

光线处理：主光是 warm tropical sunlight, golden hour side light, dust motes in sun；高光偏 golden amber / warm yellow；阴影偏 deep umber / red-brown earth；画面对比 medium-high 60-75%, warm sun contrast；色调整体 warm earthy golden, 80% warm + 20% cool。

画面构图上，road movie traveling shots、south american landscape、golden hour natural light、moving vehicle perspective、handheld intimacy、wide horizon lines、dust and heat haze、historical road trip。

情绪是 latin american journey、coming of age on road、discovery of self and continent、paternal/mentor bond、working class warmth、political awakening、nostalgia for home、expansive freedom。整体基调是南美大地暖色与公路金黄交织的旅程诗，移动摄影机里流溢着拉美大地的温柔与辽阔。色彩与光影上还要照顾到 brazilian savanna ochre、andean mountain brown、highway golden dust、tropical sunset orange、caramel skin tone、cerrado green foliage、vintage leather brown、dusty bus window。

配色：主色 南美赭黄 `#C48A3A` 占 22%，辅色 红土褐 `#8B5A2B` 占 18%、公路金黄 `#D4A855` 占 16%、焦糖肤 `#E8C68A` 占 16%，点缀 旧皮褐 `#6B4A3A` 占 16%、塞拉多绿 `#5A6B3A` 占 12%。情绪色只少量加入：金穗黄 `#F2D299`（希望启程）、深棕褐 `#4A3728`（乡愁沉淀）。让主色占绝对主导，其余颜色按上面的比例依次递减。
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
| 中央车站 | 中央车站 | 南美赭黄+焦糖肤 | 寻亲旅途 |
| 摩托日记 | 摩托日记 | 公路金黄+旧皮褐 | 青春觉醒 |
| 摩托日记山路 | 摩托日记山路 | 红土褐+塞拉多绿 | 大陆辽阔 |
| 中央车站东北 | 中央车站东北 | 南美赭黄+金穗黄 | 贫穷诗意 |
| 摩托日记麻风村 | 摩托日记麻风村 | 草原青+落日橙 | 理想主义 |
| 越位 | 越位 | 焦糖肤+红土褐 | 伊朗青春 |

**接法**（直接接在 §一 结尾）：

> ……（§一 的整段）。场景参考《中央车站》中央车站：南美赭黄+焦糖肤，情绪是寻亲旅途。

---

## 三、导演名怎么写

**要写，但后面必须补具体描述。** 只写「Walter Salles 风格」，模型会随机甩你一部代表作，风格完全跑偏。

✅ 正确：`Walter Salles 风格，南美大地暖色与公路金黄交织的旅程诗，移动摄影机里流溢着拉美大地的温柔与辽阔。`

---

## 四、否定词怎么处理

**本导演要避开的效果**（来自色卡主文档 `style_profile.avoid`）：

- 避免人工光感
- 避免冷色调主导
- 避免过度饱和

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
