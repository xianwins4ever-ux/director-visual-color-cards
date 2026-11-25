# 对话式模型提示词 — 李安 Ang Lee 风格

> **适用**：Nano Banana（Gemini 2.5 Flash Image / Pro）· GPT-Image（含 2.5）· 即梦 · 豆包 等**对话式**生图模型
> 编号 `045` ｜ 分类 03 大地暖调与自然光诗意 ｜ 国籍 中国台湾

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

光线处理：主光是 soft diffused natural light, gentle side lighting, warm window fill；高光偏 warm sand yellow / pale gold；阴影偏 earth brown / muted green (never harsh)；画面对比 low-medium 40-55%，柔和温润；色调整体 warm earth and soft green, 65% warm + 35% cool。

画面构图上，soft diffused light、landscape meditation、static balanced frame、gentle tracking、nature as emotional mirror、martial arts poetry、family interior warmth、water surface reflection。

情绪是 quiet restraint、eastern-western fusion、forbidden longing、family duty vs freedom、poetic nature、gentle melancholy、spiritual journey、compassionate humanity。整体基调是温润柔光里东西方美学悄然融合，大地的沉默与人心的克制在每一帧里都如诗如画。色彩与光影上还要照顾到 warm earth natural palette、soft jade green、bamboo forest light、golden hour meadow、warm family interior、ocean twilight blue、tea brown nostalgia、pastel restraint。

配色：主色 温润玉黄 `#C2A676` 占 20%，辅色 竹林青灰 `#5A6B4A` 占 18%、大地赭棕 `#8B7355` 占 17%、暖沙米白 `#E8D5B7` 占 15%，点缀 深松绿 `#3D4F3F` 占 15%、暖阳橙 `#D68C45` 占 15%。情绪色只少量加入：翡翠青 `#98D8C8`（东方诗意）、夕阳橙 `#F4A460`（禁忌爱恋）。让主色占绝对主导，其余颜色按上面的比例依次递减。
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
| 卧虎藏龙 | 山庄夜战 | 深松绿+温润玉黄 | 飘逸空灵 |
| 断背山 | 山野牧场 | 大地赭棕+暖阳橙 | 禁忌爱恋 |
| 少年派 | 海上漂流 | 深松绿+深海蓝 | 灵性旅程 |
| 饮食男女 | 家宴厨房 | 暖沙米白+暖棕茶 | 家庭温情 |
| 喜宴 | 纽约华人婚礼 | 温润玉黄+暖沙米白 | 文化碰撞 |
| 理智与情感 | 英国乡村庄园 | 大地赭棕+暖沙米白 | 英伦克制 |

**接法**（直接接在 §一 结尾）：

> ……（§一 的整段）。场景参考《卧虎藏龙》山庄夜战：深松绿+温润玉黄，情绪是飘逸空灵。

---

## 三、导演名怎么写

**要写，但后面必须补具体描述。** 只写「Ang Lee 风格」，模型会随机甩你一部代表作，风格完全跑偏。

✅ 正确：`Ang Lee 风格，温润柔光里东西方美学悄然融合，大地的沉默与人心的克制在每一帧里都如诗如画。`

---

## 四、否定词怎么处理

**本导演要避开的效果**（来自色卡主文档 `style_profile.avoid`）：

- 统一滤镜替代真实材质
- 无动机环绕和随机变焦
- 人物身份与空间轴漂移
- 肤色污染
- 死黑和爆白
- 只模仿颜色不执行镜头语言。

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
