<p align="center">
  <img width="200" src="https://github.com/idrawjs/idraw/assets/8216630/bcf8fbc6-6374-4cb9-a67f-1687d029a863" alt="iDraw.js Logo" />
</p>


<h1 align="center">iDraw.js</h1>

<p align="center">iDraw.js is a simple JavaScript framework for Drawing on the web.</p>

<p align="center">一个面向Web绘图的JavaScript框架</p>


<p align="center"><a href="https://idrawjs.com">idrawjs.com</a></p>



<p align="center">

  <a title="CI" href="https://github.com/idrawjs/idraw/actions/workflows/node.js.yml">
    <img src="https://github.com/idrawjs/idraw/actions/workflows/node.js.yml/badge.svg?branch=main" alt="CI">
  <a>

  <!-- <a href="https://codecov.io/gh/idrawjs/idraw">
    <img src="https://codecov.io/gh/idrawjs/idraw/branch/main/graph/badge.svg?token=MICIC9SCKY"/>
  </a> -->
    
  <a href="https://www.npmjs.com/package/idraw">
    <img src="https://img.shields.io/npm/v/idraw.svg?sanitize=idraw" alt="Version">
  </a>
  <a href="https://www.npmjs.com/package/idraw">
    <img src="https://img.shields.io/npm/l/idraw.svg?sanitize=true" alt="License">
  </a>
</p>



<!-- [![Node.js CI](https://github.com/idrawjs/idraw/actions/workflows/node.js.yml/badge.svg?branch=main)](https://github.com/idrawjs/idraw/actions/workflows/node.js.yml) -->

<hr/>


- [Documents](https://idrawjs.com/docs/en-US/) | [中文文档](https://idrawjs.com/docs/zh-CN/) 
- [Online Playground](https://idrawjs.com/playground/) | [在线API示例](https://idrawjs.com/playground/)
- [Online Studio](https://idrawjs.com/studio/) | [在线绘图演示](https://idrawjs.com/studio/)
 

## Sponsors

iDraw.js is an MIT-licensed open source project with its ongoing development made possible entirely by the support of these awesome backers. If you'd like to join them, please consider [sponsoring iDrawjs's development](https://opencollective.com/idrawjs).

[![Become a Backer](https://opencollective.com/idrawjs/tiers/backers.svg?avatarHeight=48)](https://opencollective.com/idrawjs)


## @idraw/studio Preview

The preview of `@idraw/studo`. Click [here](https://github.com/idrawjs/studio) to get it.

<p align="center">

  <img width="700" alt="idraw-studio-light-theme" src="https://github.com/idrawjs/studio/assets/8216630/8a49bab8-1e4a-44dd-9836-b6ce3861aaea" />

  <img width="700" alt="idraw-studio-dark-theme" src="https://github.com/idrawjs/studio/assets/8216630/479fce0b-891f-47f2-ace8-d91580e68b4b" />

</p>




## Install

```
npm i idraw
```

## Getting Started

### Common

```js
import { iDraw } from 'idraw';

const idraw = new iDraw(
  document.querySelector('#app'),
  {
    width: 600,
    height: 400,
    devicePixelRatio: 1,
  }
);
idraw.addElement({
  name: "rect-1",
  x: 140,
  y: 120,
  w: 200,
  h: 100,
  type: "rect",
  detail: {
    background: "#f7d3c1",
    borderRadius: 20,
    borderWidth: 4,
    borderColor: "#ff6032",
  },
});
```

### React

```jsx
import { iDraw } from 'idraw';
import { useEffect, useRef } from 'react';

function Demo() {
  const ref = useRef(null);
  useEffect(() => {
    const idraw = new iDraw(ref.current, {
      width: 600,
      height: 400, 
      devicePixelRatio: 1,
    });
    idraw.addElement({
      name: "rect-001",
      x: 140,
      y: 120,
      w: 200,
      h: 100,
      type: "rect",
      detail: {
        background: "#f7d3c1",
        borderRadius: 20,
        borderWidth: 4,
        borderColor: "#ff6032",
      },
    })
  }, []);

  return (
    <div ref={ref}></div>
  )
}
```

### Vue

```html
<template>
  <div ref="mount"></div>
</template>

<script setup >
import { iDraw } from 'idraw';
import { ref, onMounted } from 'vue'
const mount = ref();

onMounted(() => {
  const idraw = new iDraw(mount.value, {
    width: 600,
    height: 400, 
    devicePixelRatio: 1,
  });
  idraw.addElement({
    name: "rect-001",
    x: 140,
    y: 120,
    w: 200,
    h: 100,
    type: "rect",
    detail: {
      background: "#f7d3c1",
      borderRadius: 20,
      borderWidth: 4,
      borderColor: "#ff6032",
    },
  })
})
</script>
```


## Contributing

We appreciate your help!

To contribute, please follow the steps:
 

- `git clone git@github.com:idrawjs/idraw.git`
- `cd idraw`
- `pnpm i`
- `npm run dev`
 
 