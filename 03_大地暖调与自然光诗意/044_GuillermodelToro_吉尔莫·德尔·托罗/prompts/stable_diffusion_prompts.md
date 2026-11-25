# Stable Diffusion 提示词模板 — 吉尔莫·德尔·托罗 Guillermo del Toro 风格

---

## 风格触发词
`guillermo del toro style, del Toro film aesthetic, amber fairy tale, warm black gothic, cinematic film still`

## 正向提示词
```
masterpiece, best quality, ultra detailed, 8k,
cinematic film still, in the style of Guillermo del Toro,
amber fairy tale palette, warm black gothic atmosphere,
dark gold mythic tones, honey light diffusion,
warm side lighting, candlelit interior, warm black shadows,
sympathetic creature design, gothic architecture,
fantasy magical realism, melancholic beauty,
cinematic lighting, 35mm film grain, anamorphic lens, depth of field
```

## 反向提示词
```
(worst quality, low quality:1.4), neon cyberpunk, bright cheerful,
cold blue shadows, cartoon, anime, 3d render,
modern digital look, clean sterile, flat lighting,
overexposed, blurry, deformed, text, watermark
```

## ControlNet推荐
| 效果 | 模型 | 强度 |
|------|------|------|
| 对称构图 | Canny/LineArt | 0.8-0.9 |
| 生物设计 | Depth+IP-Adapter | 0.6-0.8 |
| 琥珀色调 | IP-Adapter(电影截图) | 0.5-0.7 |
| 建筑细节 | ControlNet Tile | 0.6-0.8 |

## LoRA训练建议
- 推荐训练集：《潘神的迷宫》《水形物语》《猩红山峰》高清截图各30-50张
- 重点标签：amber palette, warm black, gothic, fairy tale, creature
- 训练步数：3000-4000步，强调色彩与光影氛围

## 采样参数
Steps:30-40, CFG:6-9, Sampler:DPM++ 2M Karras, 分辨率:1536x1024
