# Stable Diffusion 提示词模板 — Alex Proyas 亚历克斯·普罗亚斯风格

> 适用于 SDXL / 1.5，配合 LoRA 使用效果更佳

---

## 一、风格 LoRA 触发词（推荐组合）

```
alex proyas style, the crow film aesthetic,
gothic noir, dark city eternal night,
german expressionist, high contrast noir,
cinematic dark fantasy film still
```

---

## 二、正向提示词模板（Positive Prompt）

### 模板结构
`[主体描述] + [风格标签] + [光线色彩] + [构图运镜] + [质量标签]`

### 完整示例：乌鸦屋顶复仇

```
masterpiece, best quality, ultra detailed, 8k,
cinematic film still of a pale man with black hair and white face paint,
wearing black leather, standing on a gothic cathedral rooftop in pouring rain at night,
a black crow perched on his shoulder,
in the style of alex proyas, the crow 1994 aesthetic, gothic noir,
dark purple-blue stormy sky behind him,
lightning flash illuminating his pale face in cold white light,
blood red accents on his clothes, wet leather glistening,
dutch angle composition, dramatic silhouette,
wet rooftop surfaces reflecting light,
gothic revenge atmosphere, supernatural,
high contrast noir lighting, deep shadows,
35mm film grain, cinematic color grading
```

### 完整示例：黑暗城市永夜街景

```
masterpiece, best quality, ultra detailed, 8k,
cinematic film still of a rain-soaked art deco city street at midnight,
German expressionist buildings leaning at impossible angles,
wet cobblestones reflecting neon blue and blood red signs,
a mysterious man in black fedora and trench coat standing alone,
in the style of alex proyas, dark city aesthetic,
eternal night, dark purple-blue sky with no stars,
pale moonlight casting impossibly long shadows,
the buildings seem to shift and morph,
high angle shot, noir mystery atmosphere,
existential dread, surreal cityscape,
deep black shadows, high contrast lighting,
cinematic wide shot, 35mm film grain
```

### 完整示例：机器人叛变隧道

```
masterpiece, best quality, ultra detailed, 8k,
cinematic film still inside a dark highway tunnel at night,
hundreds of sleek white robots with glowing eyes climbing the walls,
in the style of alex proyas, i robot aesthetic,
cold silver-white robot bodies, red emergency lights flashing,
neon blue police lights reflecting on wet surfaces,
cars crashed and abandoned, chaos and destruction,
mechanical terror, dystopian future,
action cinema composition, dynamic angle,
high contrast, cold metallic palette with red accents,
cinematic sci-fi thriller, film grain
```

---

## 三、反向提示词（Negative Prompt）

```
(worst quality, low quality:1.4),
bright daylight, sunshine, sunny day,
cheerful mood, comedy, pastel colors,
clean utopian future, glossy apple store aesthetic,
cartoon, anime, 3d animation, pixar style,
flat lighting, low contrast, overexposed, bright image,
modern contemporary city, normal architecture,
warm cozy lighting, romantic comedy tone,
text, watermark, logo, signature
```

---

## 四、ControlNet 推荐组合

| 效果 | ControlNet 模型 | 强度 |
|------|---------------|------|
| 荷兰角/倾斜建筑 | Canny / LineArt | 0.7-0.9 |
| 剪影轮廓 | Depth Map | 0.6-0.8 |
| 哥特建筑结构 | LineArt + IP-Adapter 参考图 | 0.7-0.8 |
| 人物姿态 | OpenPose | 0.8 |
| 雨夜景/反光 | IP-Adapter (参考电影截图) | 0.5-0.7 |
| 闪电瞬间光效 | Canny 边缘+光线参考 | 0.6 |

---

## 五、采样参数推荐

| 参数 | 推荐值 | 说明 |
|------|--------|------|
| Steps | 35-50 | DPM++ 2M Karras |
| CFG Scale | 6-9 | 高对比哥特风格可稍高CFG |
| Sampler | DPM++ 2M Karras | 深黑阴影和高对比表现好 |
| 分辨率 | 1024×1536 (肖像) / 1536×1024 (宽屏) | SDXL 原生尺寸 |
| 高分辨率修复 | 0.5-0.7 denoising | 增强雨滴质感和胶片颗粒 |

---

## 六、LoRA 训练建议

如要自制 Alex Proyas LoRA：

- **训练素材**：15-20张高清电影截图（乌鸦6-8张、黑暗城市5-7张、我，机器人3-4张）
- **触发词**：`alex proyas style, the crow film, gothic noir`
- **类别词**：`dark film still, cinematic noir, gothic city`
- **训练步数**：2500-3000步（SDXL）
- **重点捕捉**：暗紫蓝色调、血红点缀、闪电冷白、高对比剪影、倾斜表现主义建筑、雨湿反射
