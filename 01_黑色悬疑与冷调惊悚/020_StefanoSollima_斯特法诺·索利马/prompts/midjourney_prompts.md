# Midjourney 提示词模板 — Stefano Sollima 斯特法诺·索利马风格

> 使用方法：将 `[SUBJECT]` 替换为你的主体描述，按需调整参数

---

## 一、通用风格标签（Universal Style Tags）

```
in the style of Stefano Sollima, dark thriller film still,
dark cold action, grey-blue tactical, urban noir,
moral grey area mood, realism,
cinematic film grain, moody atmosphere
```

---

## 二、人物肖像模板

### 模板 A：主角肖像

```
[SUBJECT: a mysterious figure in a dark coat],
in the style of Stefano Sollima,
tactical cinematography, cool natural light, hard-edged shadows, realism,
dark cold action shadows with cool white-blue highlights,
moral grey area expression, mundane violence atmosphere,
cinematic medium close-up shot, film grain,
desert earth tone --ar 3:4 --style raw --s 750 --v 6
```

### 模板 B：剪影人物

```
[SUBJECT: a silhouetted figure standing in a doorway],
Stefano Sollima style, dark thriller,
handheld tracking shot,
dark cold action, dramatic backlighting,
realism, state apparatus,
car interior composition,
grainy cinematic texture --ar 2:3 --style raw --s 500 --v 6
```

---

## 三、场景环境模板

### 模板 C：经典场景

```
[SUBJECT: border night raid],
in the style of Stefano Sollima,
dark cold action, late night iron grey+tactical blue,
wide-angle action,
moral grey area atmosphere, black ops, moral ambiguity, state violence,
cinematic wide shot, film grain, dramatic lighting,
--ar 16:9 --style raw --s 700 --v 6
```

### 模板 D：室内氛围

```
[SUBJECT: a dimly lit interior room with urban noir],
Stefano Sollima film aesthetic,
cool natural light, hard-edged shadows, realism, grey-blue tactical,
car interior composition,
mundane violence, criminal network,
cinematic atmosphere, film grain --ar 16:9 --style raw --s 650 --v 6
```

---

## 四、静物与道具模板

### 模板 G：象征静物

```
[SUBJECT: a symbolic object on a dark table],
Stefano Sollima style still life,
cool natural light, hard-edged shadows, realism, creating long shadows,
dark cold action ambient light, grey-blue tactical,
moral grey area, mysterious atmosphere,
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
| 道德灰色氛围 | 提示词中加 `暗冷动作, 现实主义` |