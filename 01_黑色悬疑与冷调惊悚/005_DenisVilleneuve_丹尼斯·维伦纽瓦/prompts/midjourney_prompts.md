# Midjourney 提示词模板 — Denis Villeneuve 丹尼斯·维伦纽瓦风格

> 使用方法：将 `[SUBJECT]` 替换为你的主体描述，按需调整参数

---

## 一、通用风格标签（Universal Style Tags）

```
in the style of Denis Villeneuve, dark thriller film still,
hazy grey-orange, desert dust color palette, cool yellow tone,
existential awe mood, cosmic scale,
cinematic film grain, moody atmosphere
```

---

## 二、人物肖像模板

### 模板 A：主角肖像

```
[SUBJECT: a mysterious figure in a dark coat],
in the style of Denis Villeneuve,
massive scale composition, soft side backlight, predominantly natural light sources, strong sense of scale,
hazy grey-orange shadows with dusty orange-yellow highlights,
existential awe expression, weight of time atmosphere,
cinematic medium close-up shot, film grain,
desaturated treatment --ar 3:4 --style raw --s 750 --v 6
```

### 模板 B：剪影人物

```
[SUBJECT: a silhouetted figure standing in a doorway],
Denis Villeneuve style, dark thriller,
symmetrical geometry,
hazy grey-orange, dramatic backlighting,
cosmic scale, fear of the unknown,
wide-angle long shot,
grainy cinematic texture --ar 2:3 --style raw --s 500 --v 6
```

---

## 三、场景环境模板

### 模板 C：经典场景

```
[SUBJECT: desert border dusk],
in the style of Denis Villeneuve,
hazy grey-orange, dusty orange-yellow+dusty grey-brown,
wide-angle long shot,
existential awe atmosphere, critical, dangerous, edge of the law,
cinematic wide shot, film grain, dramatic lighting,
--ar 16:9 --style raw --s 700 --v 6
```

### 模板 D：室内氛围

```
[SUBJECT: a dimly lit interior room with cool yellow tone],
Denis Villeneuve film aesthetic,
soft side backlight, predominantly natural light sources, strong sense of scale, desert dust color palette,
hazy atmospheric perspective,
weight of time, ethical dilemma,
cinematic atmosphere, film grain --ar 16:9 --style raw --s 650 --v 6
```

---

## 四、静物与道具模板

### 模板 G：象征静物

```
[SUBJECT: a symbolic object on a dark table],
Denis Villeneuve style still life,
soft side backlight, predominantly natural light sources, strong sense of scale, creating long shadows,
hazy grey-orange ambient light, desert dust color palette,
existential awe, mysterious atmosphere,
extreme close-up macro shot, cinematic lighting,
film grain --ar 1:1 --style raw --s 650 --v 6
```

---

## 五、负面提示词

```
--no bright colors, cartoon style, anime,
happy cheerful expression, flat lighting,
overexposed, low contrast, blurry,
modern smartphone, digital displays
```

---

## 六、参数速查

| 效果 | 参数 |
|------|------|
| 电影感最强 | `--s 750 --style raw --v 6` |
| 更写实/更低干预 | `--s 250 --style raw --v 6` |
| 更艺术化 | `--s 900 --v 6` |
| 宽银幕电影 | `--ar 16:9` |
| 肖像竖版 | `--ar 3:4` |
| IMAX 宽屏 | `--ar 2.35:1` |
| 存在主义敬畏氛围 | 提示词中加 `雾霾灰橙, 宇宙尺度` |