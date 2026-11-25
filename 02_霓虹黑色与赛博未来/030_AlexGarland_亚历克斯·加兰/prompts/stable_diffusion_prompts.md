# Stable Diffusion 提示词模板 — Alex Garland 亚历克斯·加兰风格

> 适用于 SDXL / 1.5，配合 LoRA 使用效果更佳

---

## 一、风格 LoRA 触发词（推荐组合）

```
alex garland style, ex machina aesthetic,
minimalist sci-fi thriller, annihilation sci-fi horror,
sterile modernist spaces, soft diffused natural lighting,
intellectual science fiction, symmetrical composition
```

---

## 二、正向提示词模板（Positive Prompt）

### 模板结构
`[主体描述] + [风格标签] + [光线色彩] + [构图运镜] + [质量标签]`

### 完整示例：极简AI实验室

```
masterpiece, best quality, ultra detailed, 8k,
cinematic film still of a minimalist underground research facility,
glass walls and steel partitions, sterile white concrete architecture,
soft diffused natural light from large windows,
a young woman in white dress visible through glass layers,
recursive reflections in glass surfaces,
in the style of alex garland, ex machina aesthetic,
cold steel blue-grey tones, pure white walls,
perfect symmetrical perspective down corridors,
intellectual sci-fi atmosphere, quiet tension,
modernist architecture, bunker-like facility,
cinematic lighting, film grain, shallow depth of field,
wide shot, contemplative mood
```

### 完整示例：湮灭变异森林

```
masterpiece, best quality, ultra detailed, 8k,
a woman in hazmat suit standing in an otherworldly mutated forest,
deep forest green with iridescent pink-purple shimmer,
crystalline trees, genetically fused flora, prismatic light refractions,
the shimmer barrier as translucent wall of color,
deer with flowering antlers in background,
in the style of alex garland, annihilation aesthetic,
soft diffused otherworldly light, body horror beauty,
beautiful and deeply unsettling, symmetrical forest path,
cinematic wide shot, film grain, atmospheric dread,
natural light refracting through mutated atmosphere
```

### 完整示例：机械姬肖像

```
masterpiece, best quality, ultra detailed, 8k,
portrait of a young female AI with short dark hair in white dress,
seated in a glass room, looking directly at camera,
calm intelligent unreadable expression, knowing gaze,
soft diffused white light, cold blue-grey glass reflections,
in the style of alex garland, ex machina,
sterile minimalist interior, glass walls creating reflections,
symmetrical composition through glass frame,
cinematic portrait lighting, film grain, cool color palette,
medium close-up shot, intellectual thriller atmosphere
```

---

## 三、反向提示词（Negative Prompt）

```
(worst quality, low quality:1.4),
warm orange color grading, cluttered messy space,
baroque ornamentation, busy colorful design,
action explosions, fast paced, michael bay,
bright cheerful sunny, romantic comedy,
cartoon, anime, superhero, fantasy magic,
oversaturated, lens flare abuse, bokeh overload,
dutch angle, hand-held shaky cam,
blurry face, deformed, ugly,
text, watermark, logo, signature
```

---

## 四、ControlNet 推荐组合

| 效果 | ControlNet 模型 | 强度 |
|------|---------------|------|
| 对称构图/走廊透视 | Canny / LineArt | 0.7-0.9 |
| 光线控制（柔光/自然光） | Depth + IP-Adapter | 0.6-0.8 |
| 人物姿态（坐姿/站姿） | OpenPose | 0.8 |
| 建筑空间深度 | Depth Map | 0.7-0.8 |
| 色彩匹配（机械姬截图） | IP-Adapter (参考电影截图) | 0.5-0.7 |

---

## 五、采样参数推荐

| 参数 | 推荐值 | 说明 |
|------|--------|------|
| Steps | 30-45 | DPM++ 2M Karras |
| CFG Scale | 5-8 | 加兰风格需要克制，CFG不宜过高 |
| Sampler | DPM++ 2M Karras / Euler a | 柔和过渡表现好 |
| 分辨率 | 1536×1024 (宽屏) / 1024×1536 (竖版) | SDXL 原生尺寸 |
| 高分辨率修复 | 0.4-0.6 denoising | 增强玻璃反射和建筑细节 |

---

## 六、LoRA 训练建议

如要自制 Alex Garland LoRA：

- **训练素材**：15-20张高清截图（机械姬/湮灭/男人各5-7张）
- **触发词**：`alex garland style, ex machina aesthetic`
- **类别词**：`minimalist sci-fi, cinematic film still, intellectual thriller`
- **训练步数**：2000-3000步（SDXL）
- **重点捕捉**：极简净白空间、冷钢蓝灰色调、对称构图、玻璃反射、虹彩自然异变
