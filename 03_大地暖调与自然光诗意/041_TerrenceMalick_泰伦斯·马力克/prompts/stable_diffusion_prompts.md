# Stable Diffusion 提示词模板 — 泰伦斯·马力克 Terrence Malick 风格

---

## 风格触发词
`terrence malick style, Malick film aesthetic, golden hour natural light, cinematic film still`

## 正向提示词
```
masterpiece, best quality, ultra detailed, 8k,
cinematic film still, in the style of Terrence Malick,
golden hour natural light, warm earth tone palette,
wide-angle landscape, soft natural backlight, lens flare divine,
wheat field, meadow green, warm sand beige, honey highlight,
transcendental spiritual atmosphere, nature and human,
cinematic lighting, 35mm film grain, anamorphic lens, depth of field
```

## 反向提示词
```
(worst quality, low quality:1.4), harsh artificial light,
urban neon, cyberpunk, cartoon, anime, 3d render,
oversaturated colors, sharp digital look,
overexposed, blurry, deformed, text, watermark
```

## ControlNet推荐
| 效果 | 模型 | 强度 |
|------|------|------|
| 风景构图 | Canny/LineArt | 0.6-0.8 |
| 自然光效 | Depth+IP-Adapter | 0.6-0.8 |
| 色彩参考 | IP-Adapter(电影截图) | 0.5-0.7 |
| 人物姿态 | OpenPose | 0.7-0.9 |

## LoRA训练建议
- 推荐训练集：《天堂之日》《生命之树》《细细的红线》高清截图各30-50张
- 重点标签：golden hour, wheat field, divine light, nature landscape
- 训练步数：2000-3000步，建议保留更多环境背景

## 采样参数
Steps:30-40, CFG:6-9, Sampler:DPM++ 2M Karras, 分辨率:1536x1024
