# 对话式模型提示词 — 加斯帕·诺埃 Gaspar Noé 风格

> **适用**：Nano Banana（Gemini 2.5 Flash Image / Pro）· GPT-Image（含 2.5）· 即梦 · 豆包 等**对话式**生图模型
> 编号 `023` ｜ 分类 02 霓虹黑色与赛博未来 ｜ 国籍 法/阿根廷

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

光线处理：主光是 strobing neon, disorienting colored sources, extreme low-angle；高光偏 strobing red/blue/magenta club lights；阴影偏 pure black void；画面对比 extreme 85-95%；色调整体 psychedelic neon dark 50/50。

画面构图上，360 degree rotating camera、extreme low angle、long unbroken takes、first person POV、stroboscopic editing、overhead bird's eye、extreme close-up body、inverted camera。

情绪是 extreme cinema、sensory overload、primal desire、violence and sexuality、drug experience、existential void、death transcendence、audience confrontation。整体基调是迷幻频闪与霓虹红蓝交织的夜店色温，感官过载中直面欲望与死亡的极端影像。色彩与光影上还要照顾到 strobing red-blue neon、psychedelic magenta、nightclub color temperature、saturated violence red、drug hallucination colors、strobe light flicker、blacklight UV glow、disorienting color shifts。

配色：主色 迷幻深黑 `#0A000F` 占 30%，辅色 频闪纯红 `#FF0000` 占 18%、电音深蓝 `#0000FF` 占 15%、裸肤 `#E8BEAC` 占 15%，点缀 夜店洋红 `#FF00FF` 占 12%、迷幻金 `#FFD700` 占 10%。情绪色只少量加入：欲望粉 `#FF1493`（性欲肉体）、毒幻青 `#00FFFF`（毒瘾幻觉）。让主色占绝对主导，其余颜色按上面的比例依次递减。
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
| 不可撤销 | 隧道暴力 | 迷幻深黑+频闪纯红 | 极端暴力 |
| 遁入虚无 | 东京俯瞰 | 迷幻金+夜店洋红 | 灵魂出窍 |
| 爱恋 | 3D性爱 | 裸肤+欲望粉 | 情欲记忆 |
| 高潮 | 集体舞蹈 | 频闪纯红+电音深蓝 | 迷狂 |
| 独自站立 | 屠夫独白 | 迷幻深黑+暴力橙红 | 愤怒暴力 |
| 永恒之光 | 老年迷幻 | 迷幻紫+毒幻青 | 死亡超越 |

**接法**（直接接在 §一 结尾）：

> ……（§一 的整段）。场景参考《不可撤销》隧道暴力：迷幻深黑+频闪纯红，情绪是极端暴力。

---

## 三、导演名怎么写

**要写，但后面必须补具体描述。** 只写「Gaspar Noé 风格」，模型会随机甩你一部代表作，风格完全跑偏。

✅ 正确：`Gaspar Noé 风格，迷幻频闪与霓虹红蓝交织的夜店色温，感官过载中直面欲望与死亡的极端影像。`

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
