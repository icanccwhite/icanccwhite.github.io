```markdown
title: "patchwork (R package) tips"
author: icanccwhite
output:
  html_document: default
date: "9/Nov./2025"
```





patchwork包使用注意事项：

1. 每一个分图的细节参数补充完善后组装，简化组装过程。组装过程中很可能会返修分图代码，应尽量保证分图代码的可读性。
2. 水平方向上的组图，减少“+”号的使用，以“|”代替；组图后及时在plot_layout添加widths和heights参数设置，减少分歧。
3. 每一个分图ggplot + theme 制图过程减少函数多层嵌套重复使用，易导致代码换乱。各个分图的theme内置参数保持一致有利于组图更高效规范，避免无效代码。
4. 复杂组图分步实现（辅助检查每一步），最后组装成一行代码，减少组图信息混乱，用括号包裹住组图后添加相应的layout信息。例如如下：

```
((p2 / p3 + plot_layout(guides = 'auto')) | p1) + plot_layout(guides = 'collect')
```

![img](https://patchwork.data-imaginist.com/articles/guides/layout_files/figure-html/unnamed-chunk-22-1.png)



```
((p2 / p3 + plot_layout(guides = 'keep')) | p1) + plot_layout(guides = 'collect')
```

![img](https://patchwork.data-imaginist.com/articles/guides/layout_files/figure-html/unnamed-chunk-23-1.png)



5. 组图过程虽然复杂，但是尽量不要通过System.sleep()延长时间。理应返修，寻找真正的影响效率的代码块并修改提升。

---

<div align="center">

[🏠 Home](/) | [📁 Archives](/archives) | [📧 Contact](mailto:icanccwhite@icloud.com)

</div>

---

<div align="center">
<p><em>✨ Life is a journey of continuous learning and discovery ✨<em><p>

</div>
