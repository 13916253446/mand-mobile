---
title: Swiper
preview: https://didi.github.io/mand-mobile/examples/#/swiper
---

Carousel, used to cycle through a set of pictures or cards


### Import

```javascript
import { Swiper, SwiperItem } from 'mand-mobile'

Vue.component(Swiper.name, Swiper)
Vue.component(SwiperItem.name, SwiperItem)
```

### Code Examples
<!-- DEMO -->

### API

#### Swiper Props

| Props | Description | Type | Default | Note |
|---|---|---|---|---|
|autoplay|the interval (ms) of autoplay; set `0` to disable autoplay|Number|`3000`|`0`, `[500, +Int.Max)`|
|transition|animation effects|String|`slide`|`slide`, `slideY`, `fade`, `fade`|
|default-index|default selected index|Number|`0`|`[0, length - 1]`|
|has-dots|whether to display the indication dots|Boolean|`true`|`true`, `false`|
|is-prevent|whether to prevent the default event|Boolean|`true`|`true`, `false`|
|is-loop|whether is infinite loop|Boolean|`true`|`true`, `false`|
|dragable|whether is dragable|Boolean|`true`|`true`, `false`|

#### Swiper Methods

##### play(autoplay)
enable autoplay

| Args | Description | Type | Default | Note |
|---|---|---|---|---|
|autoplay|the interval of autoplay|Number|`3000`|`[500, +Int.Max)`|

```js
vm.$refs.swiper.play(5000)
```

##### stop()
stop autoplay

```js
vm.$refs.swiper.stop()
```

##### pre()
switch to the previous item

```js
vm.$refs.swiper.pre()
```

##### next()
switch to the next item

```js
vm.$refs.swiper.next()
```

##### goto(index)
switch to `index`

| Args | Description | Type | Default | Note |
|---|---|---|---|---|
|index|the index to be shown|Number|`0`|`[0, length - 1]`|
```js
vm.$refs.swiper.goto(2)
```

##### getIndex()
get the index on display

| Args | Description | Type |
|---|---|---|
|index|the index on display|Number|

```js
var index = vm.$refs.swiper.getIndex()
```

#### Swiper Events
##### @beforeChange(from, to)
event to be triggered before the slide is changed

| Args | Description | Type |
|----|-----|------|
| from     | the current index | Number          |
| to     | the next index | Number          |

##### @afterChange(from, to)
event to be triggered after the slide is changed

| Args | Description | Type |
|----|-----|------|
| from   | the current index | Number          |
| to     | the next index  | Number          |
