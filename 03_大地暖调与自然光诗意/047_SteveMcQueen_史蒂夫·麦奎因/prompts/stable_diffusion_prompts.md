# Stable Diffusion 提示词模板 — 史蒂夫·麦奎因 Steve McQueen 风格

---

## 风格触发词
`steve mcqueen style, McQueen film aesthetic, painterly historical, warm brown ochre, cinematic film still`

## 正向提示词
```
masterpiece, best quality, ultra detailed, 8k,
cinematic film still, in the style of Steve McQueen,
painterly warm brown palette, ochre historical tones,
natural available light, painterly side lighting, chiaroscuro,
warm brown skin tones, deep umber shadows, honey gold highlights,
historical weight, human dignity, quiet resistance,
long take stillness, restrained but visceral emotion,
cinematic lighting, 35mm film grain, anamorphic lens, depth of field
```

## 反向提示词
```
(worst quality, low quality:1.4), bright saturated colors,
neon cyberpunk, cartoon, anime, 3d render,
romanticized violence, melodramatic,
oversaturated, overexposed, blurry, deformed, text, watermark
```

## ControlNet推荐
| 效果 | 模型 | 强度 |
|------|------|------|
| 油画构图 | Canny/LineArt | 0.7-0.9 |
| 明暗对比 | Depth+IP-Adapter | 0.7-0.8 |
| 色彩参考 | IP-Adapter(电影截图) | 0.5-0.7 |
| 群像调度 | OpenPose + ControlNet | 0.6-0.8 |

## LoRA训练建议
- 推荐训练集：《为奴十二年》《羞耻》《饥饿》高清截图各30-50张
- 重点标签：painterly, warm brown, historical, long take
- 训练步数：3000-4000步，保留油画般厚重质感

## 采样参数
Steps:30-40, CFG:6-9, Sampler:DPM++ 2M Karras, 分辨率:1536x1024
