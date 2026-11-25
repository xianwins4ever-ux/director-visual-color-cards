# Stable Diffusion 提示词模板 — Neill Blomkamp 尼尔·布洛姆坎普风格

> 适用于 SDXL / 1.5，配合 LoRA 使用效果更佳

---

## 一、风格 LoRA 触发词（推荐组合）

```
neill blomkamp style, district 9 aesthetic,
gritty documentary sci-fi,
dirty orange johannesburg slums,
found footage, hyperrealistic grit,
cinematic social science fiction
```

---

## 二、正向提示词模板（Positive Prompt）

### 模板结构
`[主体描述] + [风格标签] + [光线色彩] + [构图运镜] + [质量标签]`

### 完整示例：第九区贫民窟全景

```
masterpiece, best quality, ultra detailed, 8k,
cinematic film still of vast Johannesburg shantytown,
endless corrugated iron shacks in dirty orange and rust brown,
a massive alien spacecraft hovering above the settlement,
MNU military armored vehicles patrolling dirt roads,
alien prawn figures among the shacks,
in the style of neill blomkamp, district 9 documentary sci-fi,
hard midday African sunlight casting sharp shadows,
dust blowing across the settlement, sand beige atmosphere,
gritty hyperrealism, found footage aesthetic,
social commentary, apartheid metaphor,
aerial wide shot, documentary photography style,
dirty orange rust palette, desaturated gritty tones,
35mm film grain, handheld camera feel
```

### 完整示例：Wikus变异特写

```
masterpiece, best quality, ultra detailed, 8k,
cinematic close-up of a middle-aged man in a stained shirt,
staring in horror at his right arm which is mutating,
biomechanical alien growths spreading up his arm in green-gray,
in the style of neill blomkamp, district 9 body horror,
inside a corrugated iron shack,
hard sunlight streaming through gaps in metal walls,
dust particles visible in light beams,
dirty orange rust walls, sweat and grime on his face,
documentary interview framing, handheld camera aesthetic,
realistic body horror, visceral transformation,
shallow depth of field, 35mm film grain,
gritty color palette, cool alien tones against warm rust
```

### 完整示例：查派夜间街头

```
masterpiece, best quality, ultra detailed, 8k,
cinematic film still of a yellow police robot covered in graffiti,
wearing gold chains, sitting on a car roof in Johannesburg slum at night,
in the style of neill blomkamp, chappie aesthetic,
red and blue police lights flashing reflecting on metal surface,
dirty orange sodium street lights,
gang members in background with guns,
rusted cars and shacks lining the street,
dust and litter on the ground,
childlike AI robot, urban sci-fi,
gritty night photography, handheld camera feel,
red blue and orange color palette,
35mm film grain, cinematic lighting
```

---

## 三、反向提示词（Negative Prompt）

```
(worst quality, low quality:1.4),
clean futuristic utopia, sleek polished surfaces,
glossy CGI, apple store aesthetic, star trek,
bright saturated colors, fantasy, magic,
lush green forests, grass, blue sky with white clouds,
cartoon, anime, pixar, 3d animation,
sterile white rooms, clean laboratory,
wealthy luxury environments, mansions,
romantic warm lighting, golden hour beauty,
overexposed, flat lighting, low contrast,
text, watermark, logo, signature
```

---

## 四、ControlNet 推荐组合

| 效果 | ControlNet 模型 | 强度 |
|------|---------------|------|
| 机甲/机械结构 | Canny / LineArt | 0.7-0.9 |
| 贫民窟透视 | Depth Map | 0.7-0.8 |
| 人物姿态/动作 | OpenPose | 0.8 |
| 纪实镜头感 | IP-Adapter (参考电影截图) | 0.5-0.7 |
| 警灯红蓝闪光 | IP-Adapter + 色彩参考 | 0.6 |
| 尘土飞扬氛围 | Depth + Reference | 0.5-0.6 |

---

## 五、采样参数推荐

| 参数 | 推荐值 | 说明 |
|------|--------|------|
| Steps | 30-45 | DPM++ 2M Karras |
| CFG Scale | 5-8 | 纪实风格不要过高CFG |
| Sampler | DPM++ 2M Karras | 粗糙纹理和真实感表现好 |
| 分辨率 | 1024×1536 (肖像) / 1536×1024 (宽屏) | SDXL 原生尺寸 |
| 高分辨率修复 | 0.5-0.7 denoising | 增强尘土颗粒和锈蚀质感 |

---

## 六、LoRA 训练建议

如要自制 Neill Blomkamp LoRA：

- **训练素材**：15-20张高清电影截图（第九区8-10张、极乐空间3-4张、查派3-4张）
- **触发词**：`neill blomkamp style, district 9 aesthetic`
- **类别词**：`gritty sci-fi film still, documentary cinematography`
- **训练步数**：2000-2800步（SDXL）
- **重点捕捉**：脏橙铁锈色调、非洲硬光、尘土质感、手持纪实感、外星生物机械、贫富对比
