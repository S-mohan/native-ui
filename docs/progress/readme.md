# Progress

> `progress`元素用来显示一项任务的完成进度

## [example](https://s-mohan.github.io/native-ui/progress/example.html)

## 自定义样式

![样式对比](https://s-mohan.github.io/native-ui/img/progress.png)

## 使用
```html
<!-- primary -->
<progress max="100" value="20" class="nui-progress"></progress>
<!-- success -->
<progress max="100" value="46" class="nui-progress nui-progress--success"></progress>
<!-- warning -->
<progress max="100" value="55" class="nui-progress nui-progress--warning"></progress>
<!-- danger -->
<progress max="100" value="78" class="nui-progress nui-progress--c"></progress>
<!-- striped 斑马纹 -->
<progress max="100" value="25" class="nui-progress nui-progress--striped"></progress>
<progress max="100" value="50" class="nui-progress nui-progress--striped nui-progress--success"></progress>
<progress max="100" value="65" class="nui-progress nui-progress--striped nui-progress--warning"></progress>
<progress max="100" value="75" class="nui-progress nui-progress--striped nui-progress--danger"></progress>
```

## polyfill

[polyfill](http://lea.verou.me/polyfills/progress/)