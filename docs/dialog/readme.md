# Dialog

> `dialog`元素表示一个对话框或者交互式窗口组件

## [example](https://s-mohan.github.io/native-ui/dialog/example.html)

## javascript 方法
- `show` : 基于DOM流的位置显示元素
- `showModal`: 默认显示在页面的中心位子，并且常驻顶层（无需设置`z-index`）
- `close`: 用来关闭`dialog`

## 事件
- `close` : `dialog` 关闭时触发
- `cancel` : `dialog` 取消（如按`esc`键）时触发

```javascript
dialog.addEventListener('close', handle)
dialog.addEventListener('cancel', handle)
```

## 自定义样式
可以通过自定义`dialog`以及`dialog::backdrop`的样式来修改其默认样式,设置可以为其添加动画效果

![样式对比](https://s-mohan.github.io/native-ui/img/dialog.jpg)

## 使用
```html
<dialog class="nui-dialog nui-dialog--animated">
  <header class="nui-dialog__head">
    <h3 class="nui-dialog__title">Dialog</h3>
    <button type="button" class="nui-dialog__close" data-dismiss="modal" aria-label="Close">
      <span aria-hidden="true">&times;</span>
    </button>
  </header>
  <div class="nui-dialog__body">
    ...
    content
    ...
  </div>
  <footer class="nui-dialog__foot">
    <button class="nui-dialog__btn" data-dismiss="modal" aria-label="Close">Cancel</button>
    <button class="nui-dialog__btn btn-confirm">Confirm</button>
  </footer>
</dialog> 
```

## polyfill
[dialog-polyfill](https://github.com/GoogleChrome/dialog-polyfill)