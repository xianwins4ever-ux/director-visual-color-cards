# Stable Diffusion 提示词模板 — 巴里·詹金斯 Barry Jenkins 风格

---

## 风格触发词
`barry jenkins style, Jenkins film aesthetic, saturated warm brown skin, twilight purple-blue, cinematic film still`

## 正向提示词
```
masterpiece, best quality, ultra detailed, 8k,
cinematic film still, in the style of Barry Jenkins,
saturated warm brown skin, dark skin warm tone,
twilight purple-blue palette, teal and purple night,
soft shallow focus, slow push-in intimacy, centered portrait,
tender intimacy, urban poetry, queer love,
warm golden hour and cool night contrast,
cinematic lighting, 35mm film grain, anamorphic lens, depth of field
```

## 反向提示词
```
(worst quality, low quality:1.4), cold flat lighting,
desaturated skin, ashen skin tone,
cartoon, anime, 3d render, stereotype,
harsh contrast, overexposed, blurry, deformed, text, watermark
```

## ControlNet推荐
| 效果 | 模型 | 强度 |
|------|------|------|
| 肖像构图 | Canny/LineArt | 0.7-0.9 |
| 暖肤光效 | Depth+IP-Adapter | 0.6-0.8 |
| 色彩参考 | IP-Adapter(电影截图) | 0.5-0.7 |
| 双人姿态 | OpenPose | 0.7-0.8 |

## LoRA训练建议
- 推荐训练集：《月光男孩》《假若比尔街能说话》高清截图各40-60张
- 重点标签：warm brown skin, twilight purple, tender portrait, teal
- 训练步数：3000-4000步，重点保留肤色质感

## 采样参数
Steps:30-40, CFG:6-9, Sampler:DPM++ 2M Karras, 分辨率:1536x1024
