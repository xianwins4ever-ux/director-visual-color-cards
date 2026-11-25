# Stable Diffusion 提示词模板 — Duncan Jones 邓肯·琼斯风格

> 适用于 SDXL / 1.5，配合 LoRA 使用效果更佳

---

## 一、风格 LoRA 触发词（推荐组合）

```
duncan jones style, moon 2009 film aesthetic,
low budget sci-fi, cold blue-gray interior,
sterile space station, cinematic film still
```

---

## 二、正向提示词模板（Positive Prompt）

### 模板结构
`[主体描述] + [风格标签] + [光线色彩] + [构图运镜] + [质量标签]`

### 完整示例：月球基地孤独宇航员

```
masterpiece, best quality, ultra detailed, 8k,
cinematic film still of a lone astronaut sitting in a sterile lunar base module,
tired expression, wearing a worn gray jumpsuit,
in the style of duncan jones, low budget sci-fi,
cool blue-gray ambient light from monitor screens illuminating his face,
screen glow blue on skin, warm amber desk lamp in background,
metal walls with subtle reflections, narrow confinement space,
claustrophobic composition, close-up shot,
existential loneliness, human warmth in cold industrial setting,
35mm film grain, depth of field,
muted color palette, cool tones with warm accent
```

### 完整示例：时间循环列车

```
masterpiece, best quality, ultra detailed, 8k,
cinematic film still inside a modern commuter train,
a man in casual clothes sitting by the window looking confused,
in the style of duncan jones, source code aesthetic,
cold blue-gray train interior, metallic surfaces,
warm orange explosion light flickering from outside the window,
holographic blue light reflections on seats,
time loop tension, disorienting atmosphere,
cinematic medium shot, film grain,
cool and warm color contrast, muted sci-fi palette
```

### 完整示例：GERTY机器人场景

```
masterpiece, best quality, ultra detailed, 8k,
a white robot with a simple screen face showing a smiley emoji,
suspended from a ceiling rail in a lunar base control room,
in the style of duncan jones, moon film aesthetic,
the screen casting soft blue glow on surrounding surfaces,
warm golden task lamp on a nearby desk,
scratched metal surfaces, personal items scattered,
human-machine companionship, intimate and melancholy,
cinematic medium shot, low-key lighting,
35mm film grain, depth of field, cool blue and warm amber contrast
```

---

## 三、反向提示词（Negative Prompt）

```
(worst quality, low quality:1.4),
bright saturated colors, fantasy elements, magic,
clean utopian future, star trek, star wars,
lush green planets, daylight exterior, bright sunlight,
cartoon, anime, 3d render, smooth CGI look,
apple store aesthetic, glossy plastic, oversaturated,
cheerful happy mood, comedy tone,
text, watermark, logo, signature
```

---

## 四、ControlNet 推荐组合

| 效果 | ControlNet 模型 | 强度 |
|------|---------------|------|
| 密闭空间透视 | Depth Map | 0.7-0.9 |
| 反射镜像效果 | Canny / LineArt + IP-Adapter 参考图 | 0.6-0.8 |
| 人物姿态 | OpenPose | 0.8 |
| 屏幕光/色彩氛围 | IP-Adapter (参考电影截图) | 0.5-0.7 |
| 框中框构图 | Canny 边缘检测 | 0.7 |

---

## 五、采样参数推荐

| 参数 | 推荐值 | 说明 |
|------|--------|------|
| Steps | 30-45 | DPM++ 2M Karras |
| CFG Scale | 5-7 | 冷调风格不要过高CFG，避免色彩过饱和 |
| Sampler | DPM++ 2M Karras | 细腻金属质感表现好 |
| 分辨率 | 1024×1536 (肖像) / 1536×1024 (宽屏) | SDXL 原生尺寸 |
| 高分辨率修复 | 0.4-0.6 denoising | 增强胶片颗粒和金属质感 |

---

## 六、LoRA 训练建议

如要自制 Duncan Jones LoRA：

- **训练素材**：15-20张高清电影截图（月球5-8张、源代码4-6张、静音2-3张）
- **触发词**：`duncan jones style, moon film aesthetic`
- **类别词**：`sci-fi film still, cinematic, cold blue-gray interior`
- **训练步数**：2000-2500步（SDXL）
- **重点捕捉**：冷蓝灰色调、屏幕蓝光、暖橙点缀、密闭空间构图、金属反射
