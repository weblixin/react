# react
学习react小书

### 组件的内容编写顺序
  <ol>
    <li>static 开头的类属性，如 defaultProps、propTypes。</li>
    <li>构造函数，constructor。</li>
    <li>getter/setter（还不了解的同学可以暂时忽略）。</li>
    <li>组件生命周期。</li>
    <li>_ 开头的私有方法。</li>
    <li>事件监听方法，handle*。</li>
    <li>render*开头的方法，有时候 render() 方法里面的内容会分开到不同函数里面进行，这些函数都以 render* 开头。</li>
    <li>render() 方法。
  </ol>
  
### 组件方法命名方式

  > 组件的私有方法都用 _ 开头，所有事件监听的方法都用 handle 开头。把事件监听方法传给组件的时候，属性名用 on 开头。例如：
  ```javascript
      <CommentInput onSubmit={this.handleSubmitComment.bind(this)} />
  ```
  >这样统一规范处理事件命名会给我们带来语义化组件的好处，监听（on）CommentInput 的 Submit 事件，并且交给 this 去处理（handle）。这种规范在多人协作的时候也会非常方便。
