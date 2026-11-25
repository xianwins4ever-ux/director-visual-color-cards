# 对话式模型提示词 — 乔治·卢卡斯 George Lucas 风格

> **适用**：Nano Banana（Gemini 2.5 Flash Image / Pro）· GPT-Image（含 2.5）· 即梦 · 豆包 等**对话式**生图模型
> 编号 `054` ｜ 分类 03 大地暖调与自然光诗意 ｜ 国籍 美国

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

光线处理：主光是 warm desert sun, dual sunset rim light, practical source lighting；高光偏 warm golden orange / sand yellow；阴影偏 deep blue-purple space shadow；画面对比 high 70-85%, strong key to fill ratio；色调整体 warm desert space opera, 70% warm + 30% cool。

画面构图上，silent film composition、wipe transitions、low angle hero reveal、epic wide establishing、binary sunset framing、lightsaber glow practical、cockpit point of view、horizon line composition。

情绪是 space opera mythology、hero's journey epic、archetypal good vs evil、cosmic family saga、nostalgic childhood wonder、samurai western fusion、used universe grime、mythic destiny。整体基调是太空歌剧色与沙漠双日落交织的史诗暖调，用光剑与原力点燃一代人的星际童年。色彩与光影上还要照顾到 tatooine desert gold、binary sunset orange、deep space navy blue、jedi robe brown、sith lightsaber red、coruscant city gold、hoth ice blue、endor forest green。

配色：主色 塔图因砂金 `#E8A954` 占 22%，辅色 双日落橙 `#C25A2A` 占 18%、绝地褐 `#4A4035` 占 18%、深空蓝灰 `#2A3A4C` 占 15%，点缀 沙粒肤 `#D4C3A0` 占 15%、沙堡褐 `#7A6448` 占 12%。情绪色只少量加入：双日辉光 `#FFE6B3`（冒险希望）、星夜蓝黑 `#1A2430`（原力黑暗面）。让主色占绝对主导，其余颜色按上面的比例依次递减。
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
| 星球大战IV：新希望 | 星球大战IV：新希望 | 塔图因砂金+双日落橙 | 英雄启程 |
| 星球大战V：帝国反击战 | 星球大战V：帝国反击战 | 深空蓝灰+旧共和国金 | 命运挣扎 |
| 星球大战VI：绝地归来 | 星球大战VI：绝地归来 | 沙粒肤+绝地褐 | 救赎回归 |
| 星球大战I：幽灵的威胁 | 星球大战I：幽灵的威胁 | 旧共和国金+塔图因砂金 | 前传辉煌 |
| 印第安纳琼斯 | 印第安纳琼斯 | 沙堡褐+双日落橙 | 冒险寻宝 |
| 美国风情画 | 美国风情画 | 沙粒肤+塔图因砂金 | 青春怀旧 |

**接法**（直接接在 §一 结尾）：

> ……（§一 的整段）。场景参考《星球大战IV：新希望》星球大战IV：新希望：塔图因砂金+双日落橙，情绪是英雄启程。

---

## 三、导演名怎么写

**要写，但后面必须补具体描述。** 只写「George Lucas 风格」，模型会随机甩你一部代表作，风格完全跑偏。

✅ 正确：`George Lucas 风格，太空歌剧色与沙漠双日落交织的史诗暖调，用光剑与原力点燃一代人的星际童年。`

---

## 四、否定词怎么处理

**本导演要避开的效果**（来自色卡主文档 `style_profile.avoid`）：

- 现代写实感
- 低饱和性冷淡风
- 手持晃动摄影机
- 没有神话感的平庸构图
- 用 CG 质感替代胶片颗粒和实际光源

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
