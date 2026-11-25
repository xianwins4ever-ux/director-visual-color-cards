# Midjourney 提示词模板 — Nicolas Winding Refn 尼古拉斯·雷弗恩风格

> 使用方法：将 `[SUBJECT]` 替换为你的主体描述，按需调整参数

---

## 一、通用风格标签（Universal Style Tags）

```
in the style of Nicolas Winding Refn, dark thriller film still,
neon cool blue, electronic colors, highly saturated colored point light sources,
nihilism mood, urban loneliness,
cinematic film grain, moody atmosphere
```

---

## 二、人物肖像模板

### 模板 A：主角肖像

```
[SUBJECT: a mysterious figure in a dark coat],
in the style of Nicolas Winding Refn,
minimal composition, direct colored light sources, predominantly neon, hard-edged light effects,
neon cool blue shadows with neon blue pink gold highlights,
nihilism expression, stylized violence atmosphere,
cinematic medium close-up shot, film grain,
dark night black --ar 3:4 --style raw --s 750 --v 6
```

### 模板 B：剪影人物

```
[SUBJECT: a silhouetted figure standing in a doorway],
Nicolas Winding Refn style, dark thriller,
symmetrical center composition,
neon cool blue, dramatic backlighting,
urban loneliness, speed and passion,
long take tracking shot,
grainy cinematic texture --ar 2:3 --style raw --s 500 --v 6
```

---

## 三、场景环境模板

### 模板 C：经典场景

```
[SUBJECT: elevator violence],
in the style of Nicolas Winding Refn,
neon cool blue, neon cool blue+scarlet warning,
slow motion,
nihilism atmosphere, silent eruption, romance and violence,
cinematic wide shot, film grain, dramatic lighting,
--ar 16:9 --style raw --s 700 --v 6
```

### 模板 D：室内氛围

```
[SUBJECT: a dimly lit interior room with highly saturated colored point light sources],
Nicolas Winding Refn film aesthetic,
direct colored light sources, predominantly neon, hard-edged light effects, electronic colors,
mirror reflection,
stylized violence, silent protagonist,
cinematic atmosphere, film grain --ar 16:9 --style raw --s 650 --v 6
```

---

## 四、静物与道具模板

### 模板 G：象征静物

```
[SUBJECT: a symbolic object on a dark table],
Nicolas Winding Refn style still life,
direct colored light sources, predominantly neon, hard-edged light effects, creating long shadows,
neon cool blue ambient light, electronic colors,
nihilism, mysterious atmosphere,
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
| 虚无主义氛围 | 提示词中加 `霓虹冷蓝, 都市孤独` |