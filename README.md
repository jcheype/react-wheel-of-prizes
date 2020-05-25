# react-wheel-of-prizes

> It is a wheel of prizes game build using reactjs

[![NPM](https://img.shields.io/npm/v/react-wheel-of-prizes.svg)](https://www.npmjs.com/package/react-wheel-of-prizes) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

## Install

```bash
npm install --save react-wheel-of-prizes
```

![this is how it looks](./screenshot.png)
This component package is fully configurable. you should pass your own array of seg_colors, array of segments. these are compulsory while winning_segment is optional. if it is not provided then it will be completely rendom. there is a callbak function onFinished where you will get the winning segment.

## Usage

```jsx
import React, { Component } from 'react'

import WheelComponent from 'react-wheel-of-prizes'
import 'react-wheel-of-prizes/dist/index.css'

const App = () => {
  const segments = ['better luck next time', 'won 70', 'won 10','better luck next time', 'won 2', 'won uber pass', 'better luck next time', 'won a voucher'];
  const seg_colors = [
    "#EE4040",
    "#F0CF50",
    "#815CD1",
    "#3DA5E0",
    "#34A24F",
    "#F9AA1F",
    "#EC3F3F",
    "#FF9000",
  ];
  const onFinished = (winner) => {
    console.log(winner);
  }
  return <WheelComponent
  segments = {segments}
  seg_colors = {seg_colors} 
  winning_segment ='won 10'
  onFinished={(winner)=>onFinished(winner)}/>
}
```

## License

GNU General Public License v3.0 © [shekharramola](https://github.com/shekharramola)