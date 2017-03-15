# css单词断词、换行

word-break 当行尾放不下一个单词时，决定单词内部该怎么摆放。 
* break-all: 强行上，挤不下的话剩下的就换下一行显示呗。霸道型。 
* keep-all: 放不下我了，那我就另起一行展示，再放不下，我也不退缩。傲骄型。

word-wrap 当行尾放不下时，决定单词内是否允许换行 
* normal: 单词太长，换行显示，再超过一行就溢出显示。 
* break-word: 当单词太长时，先尝试换行，换行后还是太长，单词内还可以换行。

white-space
* pre: 保留所有的空格和回车，且不允许折行。 
* pre-wrap: 保留所有的空格和回车，但是允许折行。 
* pre-line: 会合并空格，且允许折行

```css 
word-break: keep-all;
word-wrap: break-word;
white-space: pre-wrap;
```

<iframe width="100%" height="1600" src="//jsrun.net/tMpKp/embedded/all/light/" allowfullscreen="allowfullscreen" frameborder="0"></iframe>