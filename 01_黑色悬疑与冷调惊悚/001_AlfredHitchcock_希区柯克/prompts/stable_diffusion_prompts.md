# Stable Diffusion 提示词模板 — Alfred Hitchcock 希区柯克风格

> 适用于 SDXL / 1.5，配合 LoRA 使用效果更佳

---

## 一、风格 LoRA 触发词（推荐组合）

```
hitchcock style, alfred hitchcock film aesthetic,
film noir, chiaroscuro lighting, cinematic film still
```

---

## 二、正向提示词模板（Positive Prompt）

### 模板结构
`[主体描述] + [风格标签] + [光线色彩] + [构图运镜] + [质量标签]`

### 完整示例：后窗公寓雨夜

```
masterpiece, best quality, ultra detailed, 8k,
cinematic film still of a 1950s apartment building courtyard at night,
rainy night, looking through a window frame,
in the style of alfred hitchcock, film noir thriller,
chiaroscuro lighting, warm yellow window lights against steel blue night sky,
one mysterious figure silhouette in a dark window,
symmetrical composition, voyeuristic pov shot,
heavy rain, wet surfaces reflecting light,
mist and fog in the air,
1950s technicolor aesthetic, film grain,
depth of field, cinematic wide shot,
dark mood, suspense atmosphere
```

### 完整示例：迷魂记钟楼眩晕

```
masterpiece, best quality, ultra detailed, 8k,
looking down a spiral staircase in an old bell tower,
dolly zoom vertigo effect, stone steps spiraling into darkness,
faint golden light from above, cold blue shadows in the depths,
in the style of alfred hitchcock, film noir thriller,
high angle shot, symmetrical composition,
gothic architecture, dust particles in light beams,
psychological thriller atmosphere, disorienting,
chiaroscuro lighting, dramatic contrast,
1950s technicolor, film grain,
epic composition, cinematic lighting
```

### 完整示例：金发女郎肖像

```
masterpiece, best quality, ultra detailed, 8k,
portrait of a beautiful blonde woman in a green tailored suit,
she looks over her shoulder with a hint of fear,
in the style of alfred hitchcock, film noir heroine,
chiaroscuro side lighting casting dramatic shadows on her face,
cold blue background with warm amber key light,
her hair glowing with rim light,
1950s hairstyle and fashion,
medium close-up shot, film grain,
suspenseful mood, emotional tension
```

---

## 三、反向提示词（Negative Prompt）

```
(worst quality, low quality:1.4),
modern buildings, smartphones, digital devices,
cartoon, anime, 3d render,
bright pastel colors, cheerful happy mood,
flat lighting, overexposed, low contrast,
blurry face, deformed, ugly,
text, watermark, logo, signature
```

---

## 四、ControlNet 推荐组合

| 效果 | ControlNet 模型 | 强度 |
|------|---------------|------|
| 精确构图（对称/几何） | Canny / LineArt | 0.7-0.9 |
| 光线控制 | Depth + IP-Adapter 参考图 | 0.6-0.8 |
| 人物姿态 | OpenPose | 0.8 |
| 场景深度 | Depth Map | 0.7 |
| 色彩匹配 | IP-Adapter (参考电影截图) | 0.5-0.7 |

---

## 五、采样参数推荐

| 参数 | 推荐值 | 说明 |
|------|--------|------|
| Steps | 30-50 | Euler a / DPM++ 2M Karras |
| CFG Scale | 5-8 | 希区柯克风格不要过高CFG |
| Sampler | DPM++ 2M Karras | 细腻光影表现好 |
| 分辨率 | 1024×1536 (肖像) / 1536×1024 (宽屏) | SDXL 原生尺寸 |
| 高分辨率修复 | 0.5-0.7 denoising | 增强胶片颗粒感 |

---

## 六、LoRA 训练建议

如要自制 Hitchcock LoRA：

- **训练素材**：15-20张高清电影截图（迷魂记/后窗/惊魂记/西北偏北各3-5张）
- **触发词**：`hitchcock style, alfred hitchcock film`
- **类别词**：`film noir, cinematic film still, movie scene`
- **训练步数**：2000-3000步（SDXL）
- **重点捕捉**：色彩对比、光影特征、构图规律
