# Stable Diffusion 提示词模板 — Katsuhiro Otomo 大友克洋风格

> 适用于 SDXL / 1.5，配合 LoRA 使用效果更佳

---

## 一、风格 LoRA 触发词（推荐组合）

```
katsuhiro otomo style, akira 1988 anime aesthetic,
neo-tokyo cyberpunk, post-apocalyptic anime,
80s anime film, high saturation colors, explosive energy
```

---

## 二、正向提示词模板（Positive Prompt）

### 模板结构
`[主体描述] + [风格标签] + [光线色彩] + [构图运镜] + [质量标签]`

### 完整示例：新东京爆炸

```
masterpiece, best quality, ultra detailed, 8k,
neo-Tokyo city being consumed by a massive explosion,
massive orange-red fireball expanding outward from the center,
buildings crumbling and being sucked inward,
debris and rubble flying through the air,
nuclear white-yellow core of pure energy,
shockwave ring of dust and destruction,
in the style of katsuhiro otomo, akira 1988,
high saturation colors, extreme contrast,
hard edge lighting, self-illuminated energy,
80s anime film aesthetic, cel shading, film grain,
extreme wide shot, apocalyptic epic destruction,
detailed mechanical ruins, cinematic composition
```

### 完整示例：赛博街道飙车

```
masterpiece, best quality, ultra detailed, 8k,
red futuristic motorcycles speeding through neo-Tokyo streets at night,
in the style of katsuhiro otomo, akira 1988 anime,
speed lines and motion blur, velocity effect,
neon signs in orange-red and energy blue,
wet streets reflecting neon lights,
buildings towering in deep perspective,
taillights leaving red light streaks,
smoke and exhaust trails,
dynamic diagonal composition, cyberpunk chase,
80s anime cinematic, film grain, cel style,
high contrast, high saturation
```

### 完整示例：铁雄觉醒

```
masterpiece, best quality, ultra detailed, 8k,
a teenage boy with energy erupting from his body,
his body glowing with nuclear white-yellow and psychic purple energy,
explosive orange-red shockwave expanding outward,
buildings crumbling around him, debris flying,
expression of pain and transcendence,
in the style of katsuhiro otomo, akira anime,
self-illuminated energy lighting everything,
extreme power and destruction, psychic energy,
anime cinematic, dramatic high contrast,
80s anime cel style, film grain, epic scale
```

---

## 三、反向提示词（Negative Prompt）

```
(worst quality, low quality:1.4),
soft pastel colors, watercolor, muted tones,
cute, moe, chibi, super deformed,
cheerful, peaceful, calm, slice of life,
3d render, cgi, photorealistic, live action,
simple design, minimalist, empty background,
romance, comedy, fantasy magic,
blurry, deformed, ugly,
text, watermark, logo, signature
```

---

## 四、ControlNet 推荐组合

| 效果 | ControlNet 模型 | 强度 |
|------|---------------|------|
| 爆炸/废墟精确构图 | Canny / LineArt | 0.7-0.9 |
| 速度线/运动感 | LineArt + Motion Brush | 0.6-0.8 |
| 人物动态姿态 | OpenPose / DWPose | 0.8 |
| 城市景深透视 | Depth Map | 0.7 |
| 色彩匹配（阿基拉截图） | IP-Adapter (参考电影截图) | 0.5-0.7 |

---

## 五、采样参数推荐

| 参数 | 推荐值 | 说明 |
|------|--------|------|
| Steps | 30-50 | DPM++ 2M Karras |
| CFG Scale | 7-10 | 高饱和风格需较高CFG |
| Sampler | DPM++ 2M Karras | 高对比动画效果好 |
| 分辨率 | 1536×1024 (宽屏) / 1024×1536 (竖版) | SDXL 原生尺寸 |
| 高分辨率修复 | 0.4-0.6 denoising | 增强机械细节和爆炸质感 |

---

## 六、LoRA 训练建议

如要自制 Otomo LoRA：

- **训练素材**：15-20张高清截图（阿基拉/回忆三部曲/蒸汽男孩各4-6张）
- **触发词**：`katsuhiro otomo style, akira anime aesthetic`
- **类别词**：`80s anime, cyberpunk anime, cinematic anime film still`
- **训练步数**：2000-3000步（SDXL）
- **重点捕捉**：爆炸橙红色调、高饱和色块碰撞、机械细节、废墟透视、硬边光影
