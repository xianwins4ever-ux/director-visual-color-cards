# Stable Diffusion 提示词模板 — Curtis Hanson 柯蒂斯·汉森风格

> 适用于 SDXL / 1.5，配合 LoRA 使用效果更佳

---

## 一、风格 LoRA 触发词（推荐组合）

```
curtis_hanson_style, curtis hanson film aesthetic,
dark thriller film, cinematic film still
```

---

## 二、正向提示词模板（Positive Prompt）

### 模板结构
`[主体描述] + [风格标签] + [光线色彩] + [构图运镜] + [质量标签]`

### 完整示例：经典场景

```
masterpiece, best quality, ultra detailed, 8k,
cinematic film still of bar confrontation,
in the style of Curtis Hanson, dark thriller film,
neo-noir dark tone, dark amber gold+night deep indigo,
side backlight combined with soft light, classic film noir lighting,
neo-noir composition, window frame composition,
neo-noir film atmosphere, tension, probing, cat-and-mouse game,
film grain, cinematic wide shot, depth of field,
dark mood, dramatic lighting
```

### 完整示例：人物肖像

```
masterpiece, best quality, ultra detailed, 8k,
portrait of a character in Curtis Hanson film style,
in the style of Curtis Hanson, dark thriller protagonist,
side backlight combined with soft light, classic film noir lighting casting dramatic shadows on face,
neo-noir dark tone background, dark golden warm yellow key light,
neo-noir film expression, cop vs criminal showdown atmosphere,
medium close-up shot, film grain, cinematic texture
```

---

## 三、反向提示词（Negative Prompt）

```
(worst quality, low quality:1.4),
bright pastel colors, cheerful happy mood,
cartoon, anime, 3d render,
flat lighting, overexposed, low contrast,
blurry face, deformed, ugly,
text, watermark, logo, signature
```

---

## 四、ControlNet 推荐组合

| 效果 | ControlNet 模型 | 强度 |
|------|---------------|------|
| 精确构图 | Canny / LineArt | 0.7-0.9 |
| 光线控制 | Depth + IP-Adapter 参考图 | 0.6-0.8 |
| 人物姿态 | OpenPose | 0.8 |
| 场景深度 | Depth Map | 0.7 |
| 色彩匹配 | IP-Adapter (参考电影截图) | 0.5-0.7 |

---

## 五、采样参数推荐

| 参数 | 推荐值 | 说明 |
|------|--------|------|
| Steps | 30-50 | Euler a / DPM++ 2M Karras |
| CFG Scale | 5-8 | 冷调悬疑风格不要过高CFG |
| Sampler | DPM++ 2M Karras | 细腻光影表现好 |
| 分辨率 | 1024×1536 (肖像) / 1536×1024 (宽屏) | SDXL 原生尺寸 |
| 高分辨率修复 | 0.5-0.7 denoising | 增强胶片颗粒感 |

---

## 六、LoRA 训练建议

如要自制 柯蒂斯·汉森 LoRA：

- **训练素材**：15-20张高清电影截图（从代表作中各选3-5张）
- **触发词**：`curtis_hanson_style, curtis hanson film`
- **类别词**：`dark thriller film, cinematic film still, movie scene`
- **训练步数**：2000-3000步（SDXL）
- **重点捕捉**：色彩对比、光影特征、构图规律