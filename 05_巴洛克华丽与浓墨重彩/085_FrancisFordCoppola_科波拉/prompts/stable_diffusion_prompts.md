# 科波拉 — Stable Diffusion 提示词

> 风格：暗金烛光、烟雾阴影、史诗暗调、家族荣耀

---

## 正向提示词（通用）

```
masterpiece, best quality, cinematic, film still, in the style of FrancisFordCoppola,
暗金烛光、烟雾阴影、史诗暗调、家族荣耀,
暗金烛光, 棕木色调, 烟雾阴影, 教父调色,
教父式构图, 家族群像, 烟雾光影,
家族荣耀 atmosphere, 美国梦碎,
暗调侧光、烛火暖金、烟雾光束、黄昏逆光,
35mm film, film grain, grainy, rich colors, baroque, ornate,
cinematic composition, rule of thirds, depth of field, dramatic lighting
```

## 反向提示词

```
bright, pastel colors, low saturation, cartoon, anime, illustration, 3d render,
overexposed, modern, clean, minimal,
text, watermark, logo, frame, border,
flat lighting, low contrast, washed out
```

---

## ControlNet 建议

| 类型 | 强度 | 用途 |
|------|------|------|
| Canny | 0.6-0.8 | 保持华丽线条 |
| Depth | 0.7-0.9 | 保持空间纵深 |
| Line Art | 0.5-0.7 | 保持装饰细节 |
| OpenPose | 0.7-0.9 | 人物姿态控制 |

---

## LoRA 训练建议

- **推荐模型**：SD 1.5 / SDXL
- **训练图片**：20-30 张代表性电影截图
- **触发词**：`francisfordcoppola_style`
- **训练步数**：3000-5000 步
- **重点标签**：色彩、装饰、光影
