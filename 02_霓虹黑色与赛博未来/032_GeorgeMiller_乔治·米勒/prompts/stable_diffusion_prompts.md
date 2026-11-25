# Stable Diffusion 提示词模板 — George Miller 乔治·米勒风格

> 适用于 SDXL / 1.5，配合 LoRA 使用效果更佳

---

## 一、风格 LoRA 触发词（推荐组合）

```
george miller style, mad max fury road aesthetic,
post-apocalyptic wasteland, high saturation orange desert,
extreme complementary color contrast, kinetic action,
wide angle lens distortion, practical effects action
```

---

## 二、正向提示词模板（Positive Prompt）

### 模板结构
`[主体描述] + [风格标签] + [光线色彩] + [构图运镜] + [质量标签]`

### 完整示例：废土追车大战

```
masterpiece, best quality, ultra detailed, 8k,
cinematic film still of a massive highway chase in post-apocalyptic desert,
multiple customized war vehicles speeding across orange sand,
flame-throwing vehicle, explosions and orange fireballs,
warriors with white war paint, chrome and rust vehicles,
in the style of george miller, mad max fury road,
highly saturated orange desert, deep blue sky extreme contrast,
dust trails and sand flying, kinetic action energy,
wide angle lens distortion, low angle,
high contrast complementary colors, orange vs blue,
practical effects, film grain, gritty texture,
cinematic action chaos, epic scale, 2.35:1 aspect
```

### 完整示例：沙尘暴

```
masterpiece, best quality, ultra detailed, 8k,
massive towering wall of ochre dust storm approaching across desert,
vehicles driving toward the storm,
swirling orange and brown sand, dark indigo sky above,
lightning within the dust cloud,
in the style of george miller, mad max fury road,
apocalyptic scale, nature's destructive power,
extreme wide shot, high contrast,
orange dust against dark blue-indigo sky,
cinematic, dramatic lighting, film grain,
wasteland aesthetic
```

### 完整示例：弗瑞奥萨战车

```
masterpiece, best quality, ultra detailed, 8k,
a fierce female warrior with mechanical arm driving a massive war rig,
short hair, black war paint on face, determined expression,
driving through orange desert at high speed,
fire and explosions behind the vehicle,
in the style of george miller, mad max fury road,
deep blue sky contrasting with orange desert,
dust swirling around the massive truck,
chrome and rust vehicle details,
dynamic action composition, cinematic,
high contrast, high saturation, film grain,
medium shot from inside vehicle looking out
```

---

## 三、反向提示词（Negative Prompt）

```
(worst quality, low quality:1.4),
green forests, lush vegetation, clean cities,
futuristic clean sci-fi, sterile environments,
soft pastel, muted desaturated colors,
peaceful calm, romantic lighting,
cartoon, anime, CGI video game look,
snow, ice, cold, water, ocean,
blurry, deformed, ugly, bad anatomy,
text, watermark, logo, signature
```

---

## 四、ControlNet 推荐组合

| 效果 | ControlNet 模型 | 强度 |
|------|---------------|------|
| 追车/战车构图 | Canny / LineArt | 0.7-0.9 |
| 速度/动感 | Motion Brush / LineArt | 0.6-0.8 |
| 人物姿态（驾驶/战斗） | OpenPose / DWPose | 0.8 |
| 沙漠景深 | Depth Map | 0.7 |
| 色彩匹配（狂暴之路截图） | IP-Adapter (参考电影截图) | 0.5-0.7 |

---

## 五、采样参数推荐

| 参数 | 推荐值 | 说明 |
|------|--------|------|
| Steps | 30-50 | DPM++ 2M Karras |
| CFG Scale | 7-10 | 高饱和需要较高CFG |
| Sampler | DPM++ 2M Karras | 高对比动作场景效果好 |
| 分辨率 | 1536×1024 (宽屏) / 2048×856 (超宽) | SDXL 原生尺寸 |
| 高分辨率修复 | 0.4-0.6 denoising | 增强火焰/爆炸/金属质感 |

---

## 六、LoRA 训练建议

如要自制 Miller LoRA：

- **训练素材**：15-20张高清截图（疯狂的麦克斯4为主，各5-7张；麦克斯2补充3-5张）
- **触发词**：`george miller style, mad max fury road aesthetic`
- **类别词**：`post-apocalyptic film, action movie still, wasteland cinema`
- **训练步数**：2000-3000步（SDXL）
- **重点捕捉**：高饱和橙蓝对比、沙漠烈日硬光、铬银反光、尘暴赭色调、广角畸变
