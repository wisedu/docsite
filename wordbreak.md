# css单词断词、换行

word-break 当行尾放不下一个单词时，决定单词内部该怎么摆放。 
* break-all: 强行上，挤不下的话剩下的就换下一行显示呗。霸道型。 
* keep-all: 放不下我了，那我就另起一行展示，再放不下，我也不退缩。傲骄型。

word-wrap 当行尾放不下时，决定单词内是否允许换行 
* normal: 单词太长，换行显示，再超过一行就溢出显示。 
* break-word: 当单词太长时，先尝试换行，换行后还是太长，单词内还可以换行。
* 上面这些换行神马的都是针对英文单词，像CJK(中文/日文/韩文)这样的语言就算了，因为他们不需要，不信你读一下下面的文字

研表究明，汉字的序顺并不定一能影阅响读，比如当你看完这句话后，才发这现里的字全是都乱的。

这样子都可以流畅阅读，更别说断词了…

<iframe width="100%" height="1600" src="//jsrun.net/tMpKp/embedded/all/light/" allowfullscreen="allowfullscreen" frameborder="0"></iframe>