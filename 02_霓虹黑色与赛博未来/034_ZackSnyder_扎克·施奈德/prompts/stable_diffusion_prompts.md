# Stable Diffusion 提示词模板 — Zack Snyder 扎克·施奈德风格

> 适用于 SDXL / 1.5，配合 LoRA 使用效果更佳

---

## 一、风格 LoRA 触发词（推荐组合）

```
zack snyder style, dark comic book epic,
300 spartan aesthetic, dark gold bronze tones,
high contrast chiaroscuro, oil painting texture,
slow-motion cinematic, comic book panel composition
```

---

## 二、正向提示词模板（Positive Prompt）

### 模板结构
`[主体描述] + [风格标签] + [光线色彩] + [构图运镜] + [质量标签]`

### 完整示例：300斯巴达战场

```
masterpiece, best quality, ultra detailed, 8k,
cinematic film still of Spartan warriors in phalanx formation,
battlefield with dust and fire, warriors in red capes,
dark gold bronze sepia tones, oil painting texture,
blood droplets suspended in slow motion,
deep black shadows contrasting with orange firelight,
in the style of zack snyder, 300 aesthetic,
extreme high contrast chiaroscuro lighting,
dramatic backlight rim lighting,
desaturated warm palette with blood red accents,
low angle heroic composition, epic scale,
film grain, slow motion battle chaos,
wide epic shot
```

### 完整示例：黑暗骑士雨夜

```
masterpiece, best quality, ultra detailed, 8k,
a dark caped figure in black armor standing in heavy rain on a rooftop,
cold steel grey armor, deep black shadows,
rain drops suspended in air around him,
lightning white flashes illuminating dark gothic city,
wet surfaces reflecting faint light,
in the style of zack snyder, batman aesthetic,
dark brooding atmosphere, comic book noir,
high contrast chiaroscuro, silhouette against lightning,
low angle imposing shot, graphic novel composition,
film grain, dark moody cinematic
```

### 完整示例：闪电侠速度力

```
masterpiece, best quality, ultra detailed, 8k,
a speedster running at super speed with lightning energy,
bright electric white-blue lightning trails,
world frozen in slow motion around him,
rain drops suspended mid-air,
sparks and electricity crackling,
in the style of zack snyder, justice league aesthetic,
dark background with brilliant white-blue energy,
motion blur and speed lines,
dynamic forward composition, epic superhero moment,
high contrast, cinematic lighting, film grain
```

---

## 三、反向提示词（Negative Prompt）

```
(worst quality, low quality:1.4),
bright pastel colors, cheerful happy mood,
soft focus, diffused gentle lighting,
flat lighting, low contrast, grey middle tones,
cartoon, anime, pixar, CGI kids movie,
comedy tone, romantic, slice of life,
shaky cam found footage, phone camera,
blurry, deformed, ugly, bad anatomy,
text, watermark, logo, signature
```

---

## 四、ControlNet 推荐组合

| 效果 | ControlNet 模型 | 强度 |
|------|---------------|------|
| 史诗构图/英雄姿态 | Canny / LineArt | 0.7-0.9 |
| 慢镜动作/速度感 | Motion Brush / LineArt | 0.6-0.8 |
| 人物姿态（英雄姿势） | OpenPose / DWPose | 0.8 |
| 战场/城市景深 | Depth Map | 0.7 |
| 色彩匹配（300/守望者截图） | IP-Adapter (参考电影截图) | 0.5-0.7 |

---

## 五、采样参数推荐

| 参数 | 推荐值 | 说明 |
|------|--------|------|
| Steps | 30-50 | DPM++ 2M Karras |
| CFG Scale | 7-10 | 高对比暗调需较高CFG |
| Sampler | DPM++ 2M Karras | 油画质感和高对比表现好 |
| 分辨率 | 1536×1024 (宽屏) / 2048×856 (超宽) | SDXL 原生尺寸 |
| 高分辨率修复 | 0.4-0.6 denoising | 增强油画质感和慢镜细节 |

---

## 六、LoRA 训练建议

如要自制 Snyder LoRA：

- **训练素材**：20-25张高清截图（300勇士8张、守望者5张、正义联盟5张、活死人军团3-4张）
- **触发词**：`zack snyder style, 300 spartan aesthetic`
- **类别词**：`dark comic book film, epic cinematic, graphic novel movie still`
- **训练步数**：2500-3500步（SDXL）
- **重点捕捉**：暗金铜锈色调、高反差深黑阴影、血锈红色彩、油画质感、慢镜悬浮碎片、低角度英雄构图
