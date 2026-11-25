# Stable Diffusion 提示词模板 — Robert Rodriguez 罗伯特·罗德里格兹风格

> 适用于 SDXL / 1.5，配合 LoRA 使用效果更佳

---

## 一、风格 LoRA 触发词（推荐组合）

```
robert rodriguez style, sin city comic noir,
extreme high contrast black and white, selective red color,
graphic novel aesthetic, frank miller comic style,
hard-boiled film noir, digital cyberpunk neon
```

---

## 二、正向提示词模板（Positive Prompt）

### 模板结构
`[主体描述] + [风格标签] + [光线色彩] + [构图运镜] + [质量标签]`

### 完整示例：罪城雨夜

```
masterpiece, best quality, ultra detailed, 8k,
cinematic film still of a dark city street in heavy rain at night,
a lone figure in trench coat walking with umbrella,
extreme high contrast black and white, pure black shadows,
stark white street lights reflecting on wet pavement,
rain streaks visible in light beams,
selective red color on a neon sign,
in the style of robert rodriguez, sin city aesthetic,
hard-boiled film noir, graphic novel comic look,
hard edge lighting, sharp shadows,
comic book panel composition,
film grain, stark monochrome with red accent,
cinematic wide shot
```

### 完整示例：阿丽塔赛博城

```
masterpiece, best quality, ultra detailed, 8k,
a young female cyborg warrior with large expressive eyes standing in neon cyberpunk street,
mechanical cybernetic body visible, fierce determined expression,
neon magenta and cyan signs reflecting on wet streets,
dark black sky, holographic advertisements,
in the style of robert rodriguez, alita battle angel aesthetic,
digital cyberpunk, high contrast neon glow,
orange and magenta neon light on face,
crowded futuristic street with cyborgs,
cinematic portrait, film grain, cyberpunk atmosphere,
high contrast, dramatic lighting
```

### 完整示例：墨西哥酒吧

```
masterpiece, best quality, ultra detailed, 8k,
a Mexican bar at dusk, dusty border town cantina,
golden desert light through windows,
warm amber interior lighting, red neon sign,
mariachi with guitar case at the bar,
tequila bottles, dust motes in light beams,
in the style of robert rodriguez, desperado aesthetic,
latin noir atmosphere, warm desert golden brown palette,
wide angle establishing shot,
cinematic film look, film grain, border town violence vibe
```

---

## 三、反向提示词（Negative Prompt）

```
(worst quality, low quality:1.4),
soft pastel colors, diffused soft lighting,
grey middle tones, muted, washed out, low contrast,
bright cheerful, sunny day, romantic comedy,
3d render, CGI video game look,
watercolor, impressionist, fine art painting,
medieval, fantasy magic, dragon,
blurry, deformed, ugly, bad anatomy,
text, watermark, logo, signature
```

---

## 四、ControlNet 推荐组合

| 效果 | ControlNet 模型 | 强度 |
|------|---------------|------|
| 漫画分镜构图 | Canny / LineArt | 0.7-0.9 |
| 高对比光影 | Depth + IP-Adapter 参考图 | 0.6-0.8 |
| 人物姿态 | OpenPose / DWPose | 0.8 |
| 城市/街道景深 | Depth Map | 0.7 |
| 色彩匹配（罪恶之城截图） | IP-Adapter (参考电影截图) | 0.5-0.7 |

---

## 五、采样参数推荐

| 参数 | 推荐值 | 说明 |
|------|--------|------|
| Steps | 30-50 | DPM++ 2M Karras |
| CFG Scale | 7-10 | 高对比风格需较高CFG |
| Sampler | DPM++ 2M Karras | 硬边高对比效果好 |
| 分辨率 | 1536×1024 (宽屏) / 1024×1536 (竖版) | SDXL 原生尺寸 |
| 高分辨率修复 | 0.4-0.6 denoising | 增强漫画线条和霓虹质感 |

---

## 六、LoRA 训练建议

如要自制 Rodriguez LoRA：

- **训练素材**：15-20张高清截图（罪恶之城为主8-10张、阿丽塔5张、杀出个黎明3-5张）
- **触发词**：`robert rodriguez style, sin city aesthetic`
- **类别词**：`comic book film noir, graphic novel cinema, high contrast black and white`
- **训练步数**：2000-3000步（SDXL）
- **重点捕捉**：极端黑白色调对比、选择性红色着色、硬边光影切割、数码霓虹粉青、漫画分镜构图
