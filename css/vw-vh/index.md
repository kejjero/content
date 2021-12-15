---
title: "`vw`, `vh`, `vmin`, `vmax`"
authors:
  - ezhkov
keywords:
  - относительные размеры
tags:
  - doka
---

## Кратко

Это относительные единицы измерения. Все они задают размер относительно размеров окна браузера (viewport), то есть видимой части документа.

## Пример

Высота блока будет равна 30% ширины вьюпорта, а высота — 50% высоты вьюпорта:

```css
div {
  min-width: 30vw;
  height: 50vh;
}
```

## Как это понять

Часто возникает необходимость задавать такой размер блока, который зависел бы не от размера родителя, а напрямую от размеров вьюпорта. Например, указать, что секция должна быть высотой ровно один экран.

### `vh`

Размер указывается в процентах от **высоты** вьюпорта (**v**iewport **h**eight). `100vh` соответствует полной высоте вьюпорта. `1vh` = 1% высоты вьюпорта.

<iframe title="Слайды на всю высоту окна браузера" src="demos/vh/" height="300"></iframe>

### `vw`

Размер в процентах от **ширины** вьюпорта (**v**iewport **w**idth). `100vw` соответствует полной ширине вьюпорта. `1vw` = 1% ширины вьюпорта.

### `vmin`

Размер в процентах от **меньшей** размерности вьюпорта. Если высота меньше ширины (например, горизонтальная ориентация телефона), то расчёт будет вестись относительно высоты.

<iframe title="Шапка с паддингами в vmin" src="demos/vmin/" height="500"></iframe>

### `vmax`

Размер в процентах от **большей** размерности вьюпорта. Если высота больше ширины (например, нормальная ориентация телефона), то расчёт будет вестись относительно высоты.