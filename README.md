> [nolimits4web](https://github.com/nolimits4web)'s [Swiper](https://github.com/nolimits4web/swiper/) as a react component

### Demo

demo的源码在demo文件夹    
http://liu-dongyu.github.io/react-swiper/

### Usage
#### Example
    import React, { Component } from 'react';
    import ReactDOM from 'react-dom';
    import ReactSwiper from '../dist/react-swiper';
    
    class Page extends Component {
      constructor(props) {
        super(props);
        this.prev = this.prev.bind(this);
        this.next = this.next.bind(this);
      }
      next() {
        this.refs.reactSwiper.next();
      }
      prev() {
        this.refs.reactSwiper.prev();
      }
      render() {
        const style = {
          height: '600px',
          width: '100%',
        };
        return (
          <div>
            {/* style or className is allow */}
            <ReactSwiper ref="reactSwiper" swipeOptions={{}}>
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
    
### 说明

swipeOptions可以传递[Swiper](https://github.com/nolimits4web/swiper/)的option

一些暂未整合到react-swiper中的配置    
1. observer(监视器)    
2. callbacks(回调函数)    
3. properties(Swiper属性)    
4. controller(双向控制)    
    
---

**MIT Licensed**