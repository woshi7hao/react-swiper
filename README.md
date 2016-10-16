> [nolimits4web](https://github.com/nolimits4web)'s [Swiper](https://github.com/nolimits4web/swiper/) as a react component

## 修复react 15.0.2版本以后ref报错问题
使用请下载引用dist里的react-swiper.js或react-swiper.min.js

### Install

  npm install swiper --save

### Demo

demo的源码在demo文件夹    
[live demo](http://liu-dongyu.github.io/react-swiper/)

### Usage
#### Example
```javascript
    import React, { Component } from 'react';
    import ReactDOM from 'react-dom';
    import 'swiper/dist/css/swiper.css';
    import ReactSwiper from './ReactSwiper';
    
    class Page extends Component {
      constructor(props) {
        super(props);
        this.prev = this.prev.bind(this);
        this.next = this.next.bind(this);
      }
      next() {
        this.reactSwiper.next();
      }
      prev() {
        this.reactSwiper.prev();
      }
      render() {
        const style = {
          height: '600px',
          width: '100%',
        };
        return (
          <div>
            {/* style or className is allow */}
            <ReactSwiper ref={(el) => this.reactSwiper=el} swipeOptions={{}}>
              <div style={style}>page one</div>
              <div style={style}>page two</div>
              <div style={style}>page three</div>
            </ReactSwiper>
            <div>
              <button type="button" onClick={this.prev}>Prev</button>
              <button type="button" onClick={this.next}>Next</button>
            </div>
          </div>
        );
      }
    }
    
    ReactDOM.render(
      <Page />,
      document.getElementById('app')
    );
```
### 注意

需要自行引入swiper依赖的css文件    

    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/Swiper/3.x.x/css/swiper.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/Swiper/3.x.x/css/swiper.min.css">

or

    // es6
    import 'swiper/dist/css/swiper.css';
    
    //es5
    require('swiper/dist/css/swiper.css')

### 说明

swipeOptions可以传递[Swiper](https://github.com/nolimits4web/swiper/)的option
 
---

**MIT Licensed**
