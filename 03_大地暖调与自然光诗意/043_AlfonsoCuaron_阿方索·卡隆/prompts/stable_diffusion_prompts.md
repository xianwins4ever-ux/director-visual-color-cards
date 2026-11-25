# Stable Diffusion 提示词模板 — 阿方索·卡隆 Alfonso Cuarón 风格

---

## 风格触发词
`alfonso cuaron style, Cuarón film aesthetic, long take immersion, warm golden memory, cinematic film still`

## 正向提示词
```
masterpiece, best quality, ultra detailed, 8k,
cinematic film still, in the style of Alfonso Cuarón,
long take immersion, warm golden memory tones,
poetic realism, natural available light, soft window bounce,
warm gold earth palette, cool steel blue accents,
handheld documentary feel, child's eye perspective,
cinematic lighting, 35mm film grain, anamorphic lens, depth of field
```

## 反向提示词
```
(worst quality, low quality:1.4), neon cyberpunk,
oversaturated colors, cartoon, anime, 3d render,
studio portrait lighting, flat lighting,
fast cut composition, overexposed, blurry, deformed, text, watermark
```

## ControlNet推荐
| 效果 | 模型 | 强度 |
|------|------|------|
| 长镜头构图 | Canny/LineArt | 0.7-0.9 |
| 空间深度 | Depth | 0.7-0.8 |
| 色彩参考 | IP-Adapter(电影截图) | 0.5-0.7 |
| 人物姿态 | OpenPose | 0.6-0.8 |

## LoRA训练建议
- 推荐训练集：《罗马》《地心引力》《人类之子》高清截图各30-50张
- 重点标签：long take, warm memory, natural light, space
- 训练步数：2500-3500步，保留空间纵深感

## 采样参数
Steps:30-40, CFG:6-9, Sampler:DPM++ 2M Karras, 分辨率:1536x1024
