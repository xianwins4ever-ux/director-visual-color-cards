# 汤姆·霍珀 — Stable Diffusion 提示词

> 风格：广角畸变、油画柔光、英伦古典、对称构图

---

## 正向提示词（通用）

```
masterpiece, best quality, cinematic, film still, in the style of TomHooper,
广角畸变、油画柔光、英伦古典、对称构图,
英伦古典色, 油画暖调, 历史质感, 钢蓝与金,
广角畸变, 对称构图, 历史场景,
历史传记 atmosphere, 人性尊严,
油画柔光、窗光侧照、蜡烛暖光、自然冷调,
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
- **触发词**：`tomhooper_style`
- **训练步数**：3000-5000 步
- **重点标签**：色彩、装饰、光影
