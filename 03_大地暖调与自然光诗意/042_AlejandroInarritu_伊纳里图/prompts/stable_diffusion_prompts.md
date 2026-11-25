# Stable Diffusion 提示词模板 — 伊纳里图 Alejandro G. Iñárritu 风格

---

## 风格触发词
`alejandro inarritu style, Iñárritu film aesthetic, natural available light, visceral cinematic film still`

## 正向提示词
```
masterpiece, best quality, ultra detailed, 8k,
cinematic film still, in the style of Alejandro G. Iñárritu,
natural available light, mud and blood warm earth tones,
handheld intimate camera, long take composition,
amber interior glow, cold winter grey-blue, warm skin under stress,
dirt and sweat, visceral physicality, existential weight,
cinematic lighting, 35mm film grain, anamorphic lens, depth of field
```

## 反向提示词
```
(worst quality, low quality:1.4), soft filter, studio lighting,
clean pristine look, cartoon, anime, 3d render,
oversaturated colors, romanticized, perfect skin,
overexposed, blurry, deformed, text, watermark
```

## ControlNet推荐
| 效果 | 模型 | 强度 |
|------|------|------|
| 长镜头构图 | Canny/LineArt | 0.7-0.9 |
| 自然光效 | Depth+IP-Adapter | 0.6-0.8 |
| 色彩参考 | IP-Adapter(电影截图) | 0.5-0.7 |
| 人物表情 | IP-Adapter(面孔) | 0.6-0.8 |

## LoRA训练建议
- 推荐训练集：《荒野猎人》《鸟人》《巴别塔》高清截图各30-50张
- 重点标签：natural light, long take, mud blood, handheld
- 训练步数：2500-3500步，保留场景真实质感

## 采样参数
Steps:30-40, CFG:6-9, Sampler:DPM++ 2M Karras, 分辨率:1536x1024
