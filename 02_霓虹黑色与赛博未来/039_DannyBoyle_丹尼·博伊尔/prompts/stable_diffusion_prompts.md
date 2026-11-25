# Stable Diffusion 提示词模板 — Danny Boyle 丹尼·博伊尔风格

> 适用于 SDXL / 1.5，配合 LoRA 使用效果更佳

---

## 一、风格 LoRA 触发词（推荐组合）

```
danny boyle style, trainspotting aesthetic,
hyperkinetic filmmaking, psychedelic grunge,
warm golden and sickly green palette,
handheld camera energy, gritty urban britain,
cinematic adrenaline, grainy film texture
```

---

## 二、正向提示词模板（Positive Prompt）

### 模板结构
`[主体描述] + [风格标签] + [光线色彩] + [构图运镜] + [质量标签]`

### 完整示例：猜火车开场奔跑

```
masterpiece, best quality, ultra detailed, 8k,
cinematic film still of a skinny pale young man running through gray Edinburgh streets,
shaven head, wearing a dirty 1990s tracksuit, wild euphoric expression,
in the style of danny boyle, trainspotting aesthetic,
neon orange and red energy, sickly green undertones,
scottish gray concrete buildings behind him,
chaotic handheld camera feel, wide-angle slight distortion,
narcotic energy, british youth culture, heroin subculture,
hyper saturated with gritty texture,
choose life kinetic energy,
extreme contrast and color,
16mm film grain, grainy texture,
gritty urban britain, adrenaline rush
```

### 完整示例：28天后空城伦敦

```
masterpiece, best quality, ultra detailed, 8k,
cinematic film still of a completely empty London street,
abandoned red double-decker bus, scattered debris blowing,
a lone man in hospital scrubs standing alone in the distance,
in the style of danny boyle, 28 days later aesthetic,
eerie cold green-gray atmosphere, desaturated palette,
sickly pale green light filtering through overcast clouds,
papers and leaves blowing in empty wind,
post-apocalyptic desolation, zombie virus horror,
wide-angle lens, DV-like documentary texture,
haunting silence and isolation,
cold green and gray color palette,
cinematic horror, film grain
```

### 完整示例：孟买贫民窟

```
masterpiece, best quality, ultra detailed, 8k,
cinematic film still of young Indian boys running through narrow Mumbai slum alleyways,
warm golden hour sunlight flooding the streets,
vibrant pink and orange fabrics hanging on lines,
colorful chaos, children laughing, dust particles in light beams,
in the style of danny boyle, slumdog millionaire aesthetic,
warm yellow and gold palette with bursts of saturated red and pink,
makeshift corrugated shacks, street vendors,
handheld running camera energy, kinetic vitality,
poverty yet full of life and color,
indian street life vibrancy, saturated warm tones,
documentary vibrancy, 35mm film grain
```

---

## 三、反向提示词（Negative Prompt）

```
(worst quality, low quality:1.4),
clean polished aesthetic, sterile white rooms,
steady static camera, slow cinema, boring composition,
calm serene mood, peaceful meditation,
anime, cartoon, pixar, 3d render,
luxury settings, mansions, wealth,
hollywood gloss, smooth cgi, studio lighting,
romantic beauty, fashion photography,
flat lighting, low contrast, overexposed,
text, watermark, logo, signature
```

---

## 四、ControlNet 推荐组合

| 效果 | ControlNet 模型 | 强度 |
|------|---------------|------|
| 奔跑动态感 | OpenPose + 运动参考 | 0.7-0.8 |
| 鱼眼/广角畸变 | Canny / LineArt (广角参考) | 0.6-0.8 |
| 毒幻扭曲空间 | Depth + IP-Adapter 参考图 | 0.6-0.7 |
| 贫民窟透视 | Depth Map | 0.7-0.8 |
| 色彩饱和度跳跃 | IP-Adapter (参考电影截图) | 0.5-0.7 |
| 手持晃动感 | 视频参考/运动模糊 | 0.5-0.6 |

---

## 五、采样参数推荐

| 参数 | 推荐值 | 说明 |
|------|--------|------|
| Steps | 30-45 | Euler a（迷幻感）/ DPM++ 2M Karras |
| CFG Scale | 6-9 | 高饱和迷幻可稍高CFG |
| Sampler | Euler a / DPM++ 2M Karras | Euler a更适合迷幻畸变感 |
| 分辨率 | 1024×1536 (肖像) / 1536×1024 (宽屏) | SDXL 原生尺寸 |
| 高分辨率修复 | 0.5-0.7 denoising | 增强16mm胶片颗粒感 |

---

## 六、LoRA 训练建议

如要自制 Danny Boyle LoRA：

- **训练素材**：20-25张高清电影截图（猜火车6-8张、贫民窟5-6张、28天后4-5张、太阳浩劫2-3张）
- **触发词**：`danny boyle style, trainspotting film`
- **类别词**：`cinematic film still, gritty urban, hyperkinetic cinema`
- **训练步数**：2500-3000步（SDXL）
- **重点捕捉**：迷幻脏绿、霓虹橙红、孟买暖黄、末日冷绿两极色彩、手持晃动感、高饱和跳跃、快速剪辑感
