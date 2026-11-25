# 对话式模型提示词 — 罗杰·迪金斯 Roger Deakins 风格

> **适用**：Nano Banana（Gemini 2.5 Flash Image / Pro）· GPT-Image（含 2.5）· 即梦 · 豆包 等**对话式**生图模型
> 编号 `058` ｜ 分类 03 大地暖调与自然光诗意 ｜ 国籍 英国

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

光线处理：主光是 natural window light, precise silhouette framing, foggy blue-grey diffusion；高光偏 warm amber gold / pale cream；阴影偏 cool slate blue / deep charcoal；画面对比 high 70-85%；色调整体 balanced naturalism, 50% warm + 50% cool。

画面构图上，precision framing、natural window light、foggy atmosphere、silhouette against light、long takes (1917)、negative space、geometric composition、painterly chiaroscuro。

情绪是 quiet contemplation、existential precision、dystopian beauty、wartime desolation、western stoicism、visual poetry、moral ambiguity、cinematic meditation。整体基调是自然光大师的剪影窗光与雾蓝暖黄，精准如古典绘画的光影哲学。色彩与光影上还要照顾到 foggy slate blue、amber tungsten warm、charcoal deep shadow、parchment skin tone、desert sand gold、cyberpunk neon blue、window rim light、natural daylight precision。

配色：主色 雾霭蓝灰 `#6B7B8C` 占 22%，辅色 琥珀暖黄 `#C49A5C` 占 18%、深炭暗影 `#2A2E33` 占 15%、羊皮纸米 `#D9CDB8` 占 15%，点缀 钢蓝冷调 `#4A5568` 占 15%、沙土金棕 `#8B6F47` 占 15%。情绪色只少量加入：窗光金 `#D4AF37`（宁静启示）、赛博蓝 `#00BFFF`（未来疏离）。让主色占绝对主导，其余颜色按上面的比例依次递减。
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
| 1917 | 战壕穿越 | 雾霭蓝灰+羊皮纸米 | 战争虚无 |
| 银翼杀手2049 | 洛杉矶废墟 | 钢蓝冷调+深炭暗影 | 未来疏离 |
| 老无所依 | 德州公路追杀 | 琥珀暖黄+沙土金棕 | 西部宿命 |
| 肖申克的救赎 | 监狱逃狱 | 羊皮纸米+深炭暗影 | 希望与自由 |
| 神枪手之死 | 草原传奇 | 沙土金棕+雾霭蓝灰 | 传奇黄昏 |
| 逃狱三王 | 密西西比乡村 | 琥珀暖黄+沙土金棕 | 南方民谣 |

**接法**（直接接在 §一 结尾）：

> ……（§一 的整段）。场景参考《1917》战壕穿越：雾霭蓝灰+羊皮纸米，情绪是战争虚无。

---

## 三、导演名怎么写

**要写，但后面必须补具体描述。** 只写「Roger Deakins 风格」，模型会随机甩你一部代表作，风格完全跑偏。

✅ 正确：`Roger Deakins 风格，自然光大师的剪影窗光与雾蓝暖黄，精准如古典绘画的光影哲学。`

---

## 四、否定词怎么处理

**本导演要避开的效果**（来自色卡主文档 `style_profile.avoid`）：

- 色偏过重
- 过度饱和
- 无动机光源
- 炫光滥用
- 用统一滤镜替代精心设计的自然光效

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
