# Stable Diffusion 提示词模板 — Mamoru Oshii 押井守风格

> 适用于 SDXL / 1.5，配合 LoRA 使用效果更佳

---

## 一、风格 LoRA 触发词（推荐组合）

```
mamoru oshii style, ghost in the shell aesthetic,
90s anime cyberpunk, cinematic anime film still,
rain-soaked cyberpunk city, philosophical sci-fi
```

---

## 二、正向提示词模板（Positive Prompt）

### 模板结构
`[主体描述] + [风格标签] + [光线色彩] + [构图运镜] + [质量标签]`

### 完整示例：雨城赛博街道

```
masterpiece, best quality, ultra detailed, 8k,
cinematic anime film still of a rain-drenched cyberpunk city street at night,
tall dark buildings vanishing into fog and heavy rain,
neon cyan and data green signs reflecting in deep puddles on wet asphalt,
a lone female cyborg with short purple hair walks down the empty street,
in the style of mamoru oshii, ghost in the shell 1995 aesthetic,
cold blue-grey atmosphere, wet surfaces mirroring neon lights,
water droplets on glass and metal, atmospheric haze and fog,
90s anime style, film grain, cel shading,
wide shot, extreme depth of field, cityscape panorama,
contemplative philosophical mood, cyberpunk noir
```

### 完整示例：黑客数据流入侵

```
masterpiece, best quality, ultra detailed, 8k,
a hacker seated before multiple holographic screens in a dark room,
cascading data green code streams surrounding the figure,
neon cyan holographic projections floating in darkness,
face illuminated by green terminal glow reflecting in eyes,
mechanical grey equipment, cables everywhere,
in the style of mamoru oshii, cyberpunk anime,
cold blue-grey darkness punctuated by green and cyan light,
digital rain overlay,
medium shot, cyberpunk interior,
anime film still, cinematic lighting, atmospheric,
90s anime aesthetic, film grain
```

### 完整示例：水面对话/运河场景

```
masterpiece, best quality, ultra detailed, 8k,
a figure sitting in a small boat on dark canal water at night,
neon-lit cyberpunk city buildings reflected perfectly in still dark water,
raindrops creating ripples distorting the reflections,
data green and neon cyan lights mirrored on water surface,
cold blue-grey night atmosphere,
in the style of mamoru oshii, ghost in the shell,
philosophical contemplative mood,
wide shot with strong water reflection symmetry,
anime cinematic, film grain, melancholic atmosphere,
90s anime cel style
```

---

## 三、反向提示词（Negative Prompt）

```
(worst quality, low quality:1.4),
3d render, photorealistic, live action,
bright saturated colors, warm sunny lighting,
chibi, super deformed, cartoonish exaggeration,
cheerful happy mood, vibrant rainbow colors,
fantasy, medieval, steampunk, magic,
blurry face, deformed, ugly,
text, watermark, logo, signature,
western cartoon style, disney style
```

---

## 四、ControlNet 推荐组合

| 效果 | ControlNet 模型 | 强度 |
|------|---------------|------|
| 赛博城市精确构图 | Canny / LineArt | 0.7-0.9 |
| 雨/水/雾氛围控制 | Depth + IP-Adapter 参考图 | 0.6-0.8 |
| 人物姿态（坐姿/行走） | OpenPose | 0.8 |
| 城市景深与透视 | Depth Map | 0.7 |
| 色彩匹配（攻壳截图） | IP-Adapter (参考电影截图) | 0.5-0.7 |

---

## 五、采样参数推荐

| 参数 | 推荐值 | 说明 |
|------|--------|------|
| Steps | 30-50 | DPM++ 2M Karras / Euler a |
| CFG Scale | 6-9 | 赛博风格可稍高CFG以强化色彩 |
| Sampler | DPM++ 2M Karras | 动画质感表现好 |
| 分辨率 | 1536×1024 (宽屏) / 1024×1536 (竖版) | SDXL 原生尺寸 |
| 高分辨率修复 | 0.4-0.6 denoising | 增强胶片颗粒感和动画质感 |

---

## 六、LoRA 训练建议

如要自制 Mamoru Oshii LoRA：

- **训练素材**：15-20张高清截图（攻壳机动队1995/无罪/空中杀手/人狼各3-5张）
- **触发词**：`mamoru oshii style, ghost in the shell aesthetic`
- **类别词**：`90s anime, cyberpunk anime, cinematic anime film still`
- **训练步数**：2000-3000步（SDXL）
- **重点捕捉**：数据绿/霓虹青色调、雨景水面反射、城市远景透视、静止人物构图
