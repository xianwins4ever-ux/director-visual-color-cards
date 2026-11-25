# 对话式模型提示词 — 凯瑞·福永 Cary Fukunaga 风格

> **适用**：Nano Banana（Gemini 2.5 Flash Image / Pro）· GPT-Image（含 2.5）· 即梦 · 豆包 等**对话式**生图模型
> 编号 `057` ｜ 分类 03 大地暖调与自然光诗意 ｜ 国籍 美国

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

光线处理：主光是 golden hour desert light, soft dust diffusion, naturalism with poetic framing；高光偏 warm ochre / golden desert；阴影偏 deep umber / swamp teal；画面对比 medium-high 65-80%；色调整体 warm earth tones, 65% warm + 35% cool。

画面构图上，long tracking shots、elegant slow pan、symmetrical violence、low angle heroic、silhouette against sunset、dust particles in light、depth through doorways、lingering wide shots。

情绪是 quiet violence、existential dread、african resilience、southern gothic、elegant brutality、nostalgic warmth、moral ambiguity、lonesome journey。整体基调是暖土战地与金色非洲交织的优雅暴力，在荒凉中开出的诗意美学。色彩与光影上还要照顾到 desert sand ochre、burnt earth brown、swamp moss green、golden african sunset、warm dust haze、blood orange violence、teal-green shadows、natural skin warmth。

配色：主色 沙漠土黄 `#B8864A` 占 22%，辅色 焦土棕褐 `#8B5A2B` 占 18%、沼泽深绿 `#3D5A3D` 占 15%、暖沙肤色 `#D4B896` 占 15%，点缀 深棕暗影 `#5C4033` 占 15%、金晖夕照 `#C9A26A` 占 15%。情绪色只少量加入：战场血橙 `#FF6347`（残酷暴力）、非洲金 `#DAA520`（希望与求生）。让主色占绝对主导，其余颜色按上面的比例依次递减。
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
| 007：无暇赴死 | 沙漠古巴追逐 | 沙漠土黄+金晖夕照 | 优雅特工 |
| 真探第一季 | 路易斯安那沼泽 | 沼泽深绿+焦土棕褐 | 南方哥特 |
| 无境之兽 | 非洲丛林战争 | 沙漠土黄+暖沙肤色 | 童兵悲剧 |
| 简爱 | 桑菲尔德庄园 | 深棕暗影+暖沙肤色 | 哥特爱情 |
| 边境风云 | 墨西哥火车顶 | 焦土棕褐+沙漠土黄 | 移民求生 |
| 疯子 | 纽约心理实验 | 沼泽蓝灰+金晖夕照 | 迷幻心理 |

**接法**（直接接在 §一 结尾）：

> ……（§一 的整段）。场景参考《007：无暇赴死》沙漠古巴追逐：沙漠土黄+金晖夕照，情绪是优雅特工。

---

## 三、导演名怎么写

**要写，但后面必须补具体描述。** 只写「Cary Fukunaga 风格」，模型会随机甩你一部代表作，风格完全跑偏。

✅ 正确：`Cary Fukunaga 风格，暖土战地与金色非洲交织的优雅暴力，在荒凉中开出的诗意美学。`

---

## 四、否定词怎么处理

**本导演要避开的效果**（来自色卡主文档 `style_profile.avoid`）：

- 过度手持晃动
- 冷白现代调色
- 快速碎切暴力
- 塑料质感 CG
- 用统一滤镜替代地域光线与质地

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
