# Stable Diffusion 提示词模板 — John McTiernan 约翰·麦克蒂尔南风格

> 适用于 SDXL / 1.5，配合 LoRA 使用效果更佳

---

## 一、风格 LoRA 触发词（推荐组合）

```
john mctiernan style, 80s action film,
die hard aesthetic, dark moody action,
steel blue and dark green palette,
smoke and shadow atmosphere, classic action cinema,
35mm film, tough guy lighting
```

---

## 二、正向提示词模板（Positive Prompt）

### 模板结构
`[主体描述] + [风格标签] + [光线色彩] + [构图运镜] + [质量标签]`

### 完整示例：虎胆龙威通风管

```
masterpiece, best quality, ultra detailed, 8k,
cinematic film still of a tough barefoot man in a dirty white tank top,
crawling through a narrow ventilation duct in an office building at night,
holding a beretta pistol, sweat and dirt on his face,
in the style of john mctiernan, die hard aesthetic,
steel blue fluorescent light filtering through vent grates,
smoke filling the narrow space,
warm orange fire glow from below illuminating his face,
hard side lighting, gritty and realistic,
exhausted determined expression, bare feet on metal,
classic 80s action hero,
claustrophobic enclosure composition,
high contrast lighting, deep shadows,
35mm film grain, gritty texture
```

### 完整示例：铁血战士丛林

```
masterpiece, best quality, ultra detailed, 8k,
cinematic film still of special forces soldiers in a dense dark jungle,
military khaki uniforms, faces camouflaged with mud and sweat,
holding assault rifles in ready positions,
in the style of john mctiernan, predator aesthetic,
dark green jungle foliage pressing in from all sides,
dappled sunlight filtering through thick canopy,
humidity and heat visible in air,
one soldier looks up sensing something watching,
thermal imaging perspective implied, unknown threat,
military action tension,
hard natural lighting, deep green shadows,
jungle darkness, 35mm film grain, gritty war aesthetic
```

### 完整示例：潜艇对峙

```
masterpiece, best quality, ultra detailed, 8k,
cinematic film still inside a narrow nuclear submarine corridor,
soviet naval officers in dark uniforms standing tense,
in the style of john mctiernan, hunt for red october aesthetic,
steel blue bulkheads and metal surfaces with condensation,
dark red emergency alarm lights flashing casting crimson glow,
sonar screens glowing green in background,
smoke or steam from pipe leak,
cold war military tension, claustrophobic atmosphere,
hard metallic lighting, deep shadows,
naval warfare thriller,
35mm film grain, cool blue and dark red palette
```

---

## 三、反向提示词（Negative Prompt）

```
(worst quality, low quality:1.4),
superhero costumes, marvel CGI, john wick neon aesthetic,
bright saturated colors, cartoon violence,
sleek modern guns, clean polished look,
anime, cartoon, pixar, video game graphics,
daylight exterior, bright sunny scenes,
wire fu, martial arts, slow motion cgi,
romantic subplot, comedy tone,
flat lighting, low contrast, overexposed,
text, watermark, logo, signature
```

---

## 四、ControlNet 推荐组合

| 效果 | ControlNet 模型 | 强度 |
|------|---------------|------|
| 硬汉人物姿态 | OpenPose | 0.8 |
| 烟雾纵深层次 | Depth Map | 0.7-0.8 |
| 封闭空间透视 | Canny / LineArt | 0.7-0.9 |
| 枪械/道具精准 | Canny + IP-Adapter 参考图 | 0.6-0.8 |
| 热成像效果 | IP-Adapter (参考电影截图) | 0.5-0.7 |
| 爆炸逆光 | Depth + 光线参考 | 0.6-0.7 |

---

## 五、采样参数推荐

| 参数 | 推荐值 | 说明 |
|------|--------|------|
| Steps | 30-45 | DPM++ 2M Karras |
| CFG Scale | 6-8 | 动作片风格适中CFG |
| Sampler | DPM++ 2M Karras | 烟雾、火焰、金属质感表现好 |
| 分辨率 | 1536×1024 (宽屏动作) / 1024×1536 (肖像) | SDXL 原生尺寸 |
| 高分辨率修复 | 0.5-0.7 denoising | 增强35mm颗粒和烟雾质感 |

---

## 六、LoRA 训练建议

如要自制 John McTiernan LoRA：

- **训练素材**：15-20张高清电影截图（虎胆龙威6-8张、铁血战士5-6张、猎杀红色十月3-4张）
- **触发词**：`john mctiernan style, 80s action film`
- **类别词**：`action film still, cinematic action, tough guy movie`
- **训练步数**：2000-2500步（SDXL）
- **重点捕捉**：钢蓝冷调、丛林暗绿、烟雾纵深、爆炸暖橙逆光、硬汉侧光、汗水泥污质感、80年代胶片颗粒
