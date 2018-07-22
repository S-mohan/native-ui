# Collapse

> 利用`details`和`summary`标签，可以实现折叠面板的效果，加少许javascript代码，我们甚至可以实现手风琴效果。

## [example](https://s-mohan.github.io/native-ui/collapse/example.html)

## 自定义样式

![样式对比](https://s-mohan.github.io/native-ui/img/collapse.jpg)

## 使用
```html
<details class="nui-collapse nui-collapse--right">
  <summary class="nui-collapse__title">title</summary>
  <p class="nui-collapse__body">content</p>
</details>

<!-- accordion -->
<section class="nui-collapse-accordion">
  <details class="nui-collapse nui-collapse--right">
    <summary class="nui-collapse__title">title</summary>
    <p class="nui-collapse__body">content</p>
  </details>
  <details class="nui-collapse nui-collapse--right">
    <summary class="nui-collapse__title">title</summary>
    <p class="nui-collapse__body">content</p>
  </details>
  <details class="nui-collapse nui-collapse--right">
    <summary class="nui-collapse__title">title</summary>
    <p class="nui-collapse__body">content</p>
  </details>
</section>

<script>
var ARRAY_SLICE = Array.prototype.slice
document.addEventListener('click', function(e) {
  var target = e.target
  var selector = '.nui-collapse-accordion .nui-collapse__title'
  if (target.matches(selector) || target.closest(selector)) {
    var collapse = target.closest('.nui-collapse')
    if (collapse) {
      var group = collapse.closest('.nui-collapse-accordion')
      if (group) {
        ARRAY_SLICE.call(group.querySelectorAll('.nui-collapse')).forEach(function(el) {
          if (el !== collapse) {
            el.open = false
          }
        })
      }
    }
  }
})
</script>  
```