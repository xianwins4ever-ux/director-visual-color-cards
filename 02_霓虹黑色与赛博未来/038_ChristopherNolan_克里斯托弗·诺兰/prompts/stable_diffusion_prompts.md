# Stable Diffusion 提示词模板 — Christopher Nolan 克里斯托弗·诺兰风格

> 适用于 SDXL / 1.5，配合 LoRA 使用效果更佳

---

## 一、风格 LoRA 触发词（推荐组合）

```
christopher nolan style, nolan film aesthetic,
IMAX cinematic epic, 70mm film,
cold blue and warm amber color palette,
practical effects cinematography,
architectural geometric composition
```

---

## 二、正向提示词模板（Positive Prompt）

### 模板结构
`[主体描述] + [风格标签] + [光线色彩] + [构图运镜] + [质量标签]`

### 完整示例：星际穿越五维空间

```
masterpiece, best quality, ultra detailed, 8k,
cinematic film still of an astronaut floating inside a tesseract dimension,
in the style of christopher nolan, interstellar aesthetic,
surrounded by infinite bookshelves and warm orange glowing dimensional lines,
deep black space stretching beyond the structure,
his face visible through helmet visor, expression of awe and longing,
cold deep blue-black of space contrasting with warm orange tesseract light,
IMAX large format composition, monumental scale,
practical lighting effects, emotional science fiction,
love transcending dimensions,
deep shadows, high contrast, 70mm film grain texture,
cold blue and warm orange color palette
```

### 完整示例：盗梦空间折叠巴黎

```
masterpiece, best quality, ultra detailed, 8k,
cinematic film still of a Parisian boulevard impossibly folding upward onto itself,
buildings curving over the street creating a gravity-defying arch,
in the style of christopher nolan, inception aesthetic,
cold steel blue sky, Haussmann architecture in gray stone,
warm amber light glowing from cafe windows below,
a lone man in a dark suit standing in the empty street looking up,
geometric precision, impossible architecture,
practical effects aesthetic, no CGI overload,
IMAX wide composition, deep black shadows,
cold blue reality vs warm amber dream,
high contrast lighting, 70mm film grain
```

### 完整示例：黑暗骑士哥谭

```
masterpiece, best quality, ultra detailed, 8k,
cinematic film still of a dark caped vigilante standing on a skyscraper edge at night,
overlooking a vast gothic city,
in the style of christopher nolan, dark knight aesthetic,
dark armored silhouette against cold steel blue city lights,
Gotham city in architectural gray and dark tones,
rain falling, wet surfaces reflecting light,
police searchlight with bat symbol in clouds,
low angle shot, imposing heroic figure,
grounded realistic superhero film,
deep black shadows, high contrast noir lighting,
IMAX cinematography, 70mm film grain,
dark epic atmosphere, moral complexity
```

---

## 三、反向提示词（Negative Prompt）

```
(worst quality, low quality:1.4),
CGI overload, cartoon comic book style,
marvel cinematic universe look, saturated superhero colors,
bright cheerful colors, fantasy magic,
anime, cartoon, pixar, animation style,
fast shaky cam overload, music video editing,
flat lighting, low contrast, overexposed image,
sleek apple store futurism, star trek utopia,
romantic comedy, warm cozy golden hour beauty,
text, watermark, logo, signature
```

---

## 四、ControlNet 推荐组合

| 效果 | ControlNet 模型 | 强度 |
|------|---------------|------|
| 建筑几何构图 | Canny / LineArt | 0.7-0.9 |
| 透视纵深 | Depth Map | 0.7-0.9 |
| 人物姿态 | OpenPose | 0.8 |
| IMAX大画幅感 | IP-Adapter (参考电影截图) | 0.5-0.7 |
| 旋转/折叠环境 | Depth + 多角度参考 | 0.6-0.8 |
| 冷暖对比色调 | IP-Adapter 色彩参考 | 0.5-0.6 |

---

## 五、采样参数推荐

| 参数 | 推荐值 | 说明 |
|------|--------|------|
| Steps | 35-50 | DPM++ 2M Karras |
| CFG Scale | 6-8 | 史诗感可稍高，但避免过度饱和 |
| Sampler | DPM++ 2M Karras | 大光比和深邃暗部表现好 |
| 分辨率 | 1536×1024 (宽屏IMAX) / 1024×1536 (肖像) | SDXL 原生尺寸 |
| 高分辨率修复 | 0.5-0.7 denoising | 增强70mm胶片颗粒感和建筑纹理 |

---

## 六、LoRA 训练建议

如要自制 Christopher Nolan LoRA：

- **训练素材**：20-25张高清电影截图（星际穿越5-6张、盗梦空间5-6张、蝙蝠侠4-5张、敦刻尔克/信条/奥本海默各2-3张）
- **触发词**：`christopher nolan style, nolan IMAX film`
- **类别词**：`cinematic film still, IMAX cinematography, epic movie scene`
- **训练步数**：2500-3000步（SDXL）
- **重点捕捉**：冷钢蓝vs暖琥珀的冷暖二元、IMAX大画幅构图、建筑几何感、深邃暗部、70mm胶片质感
