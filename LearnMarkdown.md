# markdown学习笔记

<p style="text-align: right;">
by dangerousD9R4
</p>

## What is Markdown?

Markdown是一种轻量级的标记语言，它允许你以纯文本格式编写格式化内容，主要用于生成结构化的文本内容，并能轻松转换为HTML或其他格式。Markdown的语法简单、直观，通常用于写博客、文档、笔记、代码注释、电子书等内容。

## Markdown是如何工作的

当你在Markdown文件中写作时，文本被存储在一个纯文本文件中，文件扩展名通常为.md或.markdown。这些文件本身只包含文本和一些特定的标记（例如 #、*、- 等）来表示不同的格式。

然而，Markdown文件本身并不能直接在浏览器中显示出格式化的效果。为了将这些格式化文本呈现出来，你需要一个 Markdown应用程序。这个应用程序会处理（解析）这些 Markdown 格式的文本，并将其转换成HTML，这样就可以在浏览器中显示为一个格式化的文档。

Markdown应用程序：这是你用来编辑和处理Markdown文件的软件。它包括两个部分：

编辑器：让你输入Markdown语法和内容。

处理器：解析Markdown语法并将其转换成HTML。

例如，像Dillinger这样的Markdown编辑器就是一个Markdown应用程序。它会接收你输入的Markdown内容，并通过其Markdown处理器转换成HTML格式。

GitHub其实就是一个Markdown应用程序，它为你提供了一个平台来编辑、查看、甚至是渲染Markdown文件。GitHub会自动将你上传的.md文件转化为HTML格式，然后在浏览器中呈现出来。所以，GitHub不仅仅是一个代码托管平台，它也集成了一个Markdown处理器来渲染和展示你的Markdown文件。

## Markdown基本语法

### 创建标题

要创建一个标题，在一个单词或短语前添加井号（#）。你使用的井号数量应与标题级别对应。例如，要创建三级标题（`<h3>`），使用三个井号（例如`### My Header`）。

#### 创建标题替代语法

在文本下面的行上添加任意数量的==字符来表示一级标题，或者添加--字符来表示二级标题。

#### 创建标题最佳实践

Markdown 应用程序对于井号（#）和标题名称之间是否需要空格的处理并不一致。为了兼容性，始终在井号和标题名称之间添加一个空格。为了兼容性，你还应该在标题前后添加空行。

### 段落

要创建段落，请使用空行来分隔一行或多行文本。

#### 段落最佳实践

除非段落位于列表中，否则不要使用空格或制表符来缩进段落。

在Markdown中，制表符和空格具有特殊的含义。你可以使用尾随空格来创建换行，也可以使用制表符来创建代码块。但如果你想像传统方式那样使用制表键来缩进段落呢？Markdown并没有提供一个简单的方式来实现这一点。

你的最佳选择可能是使用支持缩进的Markdown编辑器。这在那些更多面向桌面排版的应用程序中比较常见。例如，iA Writer允许你在应用程序的偏好设置中自定义编辑器的缩进设置。它还提供模板自定义选项，这样你可以使渲染后的文档看起来符合预期，包括缩进。

另一种选择是，如果你的Markdown处理器支持HTML，可以使用HTML实体&nbsp; 来插入不间断空格。这通常是最后的选择，因为它可能会显得有些笨拙。基本上Markdown源代码中的每个&nbsp; 都会在渲染后的输出中被替换成一个空格。所以，如果你在段落前放入四个&nbsp;，该段落就会看起来像是缩进了四个空格。

### 换行

要创建换行或新的一行（`<br>`），在行尾添加两个或更多空格，然后按回车键。

#### 换行最佳实践

你可以在几乎所有的Markdown应用程序中使用两个或更多空格（通常称为“尾随空格”）来创建换行，但这是一种有争议的做法。在编辑器中很难看到尾随空格，而且很多人会在每个句子后不小心或故意加上两个空格。因此，你可能希望使用其他方式来创建换行。如果你的Markdown应用程序支持HTML，你可以使用`<br>`HTML 标签。

为了兼容性，建议在行尾使用尾随空格或`<br>`HTML标签。

有两个其他的选项我不推荐使用。CommonMark和一些其他轻量级标记语言允许你在行尾输入一个反斜杠（\），但并不是所有的Markdown应用程序都支持这种做法，因此从兼容性角度来看，它不是一个很好的选择。而且，至少有一些轻量级标记语言不要求行尾加任何东西——只需按回车键，它们就会自动创建换行。

### 强调

你可以通过加粗或斜体来添加文本的强调。

##### 加粗

要加粗文本，在单词或短语的前后添加两个星号（`**`）或下划线（`__`）。如果需要对单词中间部分加粗以强调，可以在字母周围添加两个星号，但不要有空格。

##### 加粗最佳实践

Markdown应用程序对于单词中间使用下划线的处理方式并不一致。为了兼容性，请使用星号（`**`）来对单词中间的部分进行加粗强调。

#### 斜体

要使文本斜体，在单词或短语的前后添加一个星号（`*`）或下划线（`_`）。如果需要对单词中间部分斜体以强调，可以在字母周围添加一个星号，但不要有空格。

##### 斜体最佳实践

Markdown应用程序对于单词中间使用下划线的处理方式并不一致。为了兼容性，请使用星号（`*`）来对单词中间的部分进行斜体强调。

#### 加粗和斜体

要同时以加粗和斜体形式强调文本，在单词或短语的前后添加三个星号（`***`）或下划线（`___`）。如果需要对单词中间部分同时加粗和斜体以强调，可以在字母周围添加三个星号，但不要有空格。

##### 加粗和斜体最佳实践

Markdown应用程序对于单词中间使用下划线的处理方式并不一致。为了兼容性，请使用星号（`***`）来对单词中间的部分同时进行加粗和斜体强调。

### 引用块

要创建一个引用块，在段落前添加一个 `>` 符号。

例如：

```markdown
> Dorothy followed her through many of the beautiful rooms in her castle.
```

渲染后的输出看起来如下：

> Dorothy followed her through many of the beautiful rooms in her castle.

#### 带有多段内容的引用块

引用块可以包含多个段落。在段落之间的空行上也需要添加 `>`。

例如：

```markdown
> Dorothy followed her through many of the beautiful rooms in her castle.
>
> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.
```

渲染后的输出看起来如下：

> Dorothy followed her through many of the beautiful rooms in her castle.  
>  
> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

#### 嵌套引用块

引用块可以嵌套。要嵌套一个段落，在该段落前添加 `>>`。

例如：

```markdown
> Dorothy followed her through many of the beautiful rooms in her castle.
>
>> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.
```

渲染后的输出看起来如下：

> Dorothy followed her through many of the beautiful rooms in her castle.  
>
>> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

#### 包含其他元素的引用块   

引用块可以包含其他格式化的 Markdown 元素。并非所有元素都能使用——你需要进行一些实验来看看哪些能正常工作。

例如：

```markdown
> #### The quarterly results look great!
>
> - Revenue was off the chart.
> - Profits were higher than ever.
>
>  *Everything* is going according to **plan**.
```

渲染后的输出看起来如下：

> The quarterly results look great!  
> - Revenue was off the chart.  
> - Profits were higher than ever.  
>  
> *Everything* is going according to **plan**.

#### 引用块最佳实践

为了兼容性，在引用块前后添加空行。

### 列表

你可以将项目组织成有序列表和无序列表。

#### 有序列表

要创建一个有序列表，添加带有数字和句点的列表项。数字不必按顺序排列，但列表应该从数字 1 开始。

##### 有序列表最佳实践

CommonMark和一些其他轻量级标记语言允许你使用括号 `())` 作为分隔符（例如，`1) First item`），但并不是所有的Markdown应用程序都支持这种写法，因此从兼容性的角度来看，这不是一个很好的选择。为了兼容性，建议只使用句点。

#### 无序列表

要创建一个无序列表，在列表项前添加破折号（`-`）、星号（`*`）或加号（`+`）。要创建嵌套列表，可以对一个或多个项目进行缩进。

##### 以数字开始无序列表项

如果你需要以数字后跟句点的形式开始无序列表项，可以使用反斜杠（`\`）来转义句点。

##### 无序列表最佳实践

Markdown应用程序对于在同一列表中使用不同分隔符的处理方式并不一致。为了兼容性，不要在同一列表中混用分隔符——选择一种并保持一致。

#### 在列表中添加元素

要在列表中添加另一个元素并保持列表的连续性，可以将该元素缩进四个空格或一个制表符

提示：如果显示的效果与预期不符，请仔细检查你是否将列表中的元素缩进了四个空格或一个制表符。

### 代码

要将某个单词或短语表示为代码，用反引号（`` ` ``）将其括起来。

#### 转义反引号

如果你想标记为代码的单词或短语中包含一个或多个反引号，你可以通过用双反引号（``）将该单词或短语括起来来转义它。

#### 代码块

要创建代码块，将块中每一行缩进至少四个空格或一个制表符。渲染后的输出如下：

    <html>
      <head>
      </head>
    </html>

注意：如果不想通过缩进行来创建代码块，可以使用围栏代码块（fenced code blocks）。围栏代码块是一种用来展示多行代码的方式，不需要依赖行首缩进，只需要用一组三个反引号 (```) 或三个波浪号 (~~~) 将代码包裹起来即可。

### 水平分割线

要创建一条水平分割线，可以在单独一行上使用三个或更多的星号（***）、破折号（---）或下划线（___）。三种方式的渲染结果是相同的。

#### 水平分割线最佳实践

为了兼容性，在水平分割线前后留空行。

### 链接

要创建一个链接，将链接文本用方括号括起来，然后紧跟着用圆括号括起 URL。没有前面的 [] 也可以被识别为链接，但前提是该内容必须是一个有效的 URL，并且通常以 http:// 或 https:// 开头。Markdown 处理器会自动将这些内容识别为可点击的链接并进行渲染。下面是一个示例。

```
My favorite search engine is [Duck Duck Go](https://duckduckgo.com).
```

渲染结果如下：<br>
My favorite search engine is [Duck Duck Go](https://duckduckgo.com).

#### 添加标题

你可以为链接可选地添加一个标题。当用户将鼠标悬停在链接上时，标题将显示为工具提示。要添加标题，只需在 URL 后面用双引号括起标题文本。下面是一个示例。

```
My favorite search engine is [Duck Duck Go](https://duckduckgo.com "The best search engine for privacy").
```

渲染效果如下：<br>
My favorite search engine is [Duck Duck Go](https://duckduckgo.com "The best search engine for privacy").

当用户将鼠标悬停在 "Duck Duck Go" 链接上时，会显示工具提示："The best search engine for privacy"。<br>
说明：
- 在链接的 URL 后，添加 `"标题文本"` 即可。
- 标题文本会在用户将鼠标悬停在链接上时作为提示出现。

#### URLs 和电子邮件地址

要快速将 URL 或电子邮件地址转化为链接，只需将其括在尖括号 `< >` 中。

示例：

```
<https://www.markdownguide.org>
<fake@example.com>
```

渲染效果如下：<br>
<https://www.markdownguide.org> <br>
<fake@example.com>

说明：
- 使用尖括号 `< >` 括起来的 URL 或电子邮件地址会自动转化为可点击的链接。

#### 格式化链接

要强调链接，可以在方括号和圆括号之前和之后添加星号（`*`）。要将链接标记为代码，可以在方括号中添加反引号（`` ` ``）。

示例：

```
- I love supporting the **[EFF](https://eff.org)**.
- This is the *[Markdown Guide](https://www.markdownguide.org)*.
```

渲染效果：
- I love supporting the **[EFF](https://eff.org)**.
- This is the *[Markdown Guide](https://www.markdownguide.org)*.

#### 引用式链接

引用式链接是一种特殊的链接格式，使得在 Markdown 中显示和阅读 URL 更加方便。引用式链接由两部分组成：一部分是你在文本中保留的部分，另一部分是你将 URL 存储在文件的其他地方，这样做可以让文本更易读。<br>

引用式链接的第一部分使用两组方括号。第一组方括号包围着应该显示为链接的文本。第二组方括号显示一个标签，用于指向你在文档其他地方存储的链接。

尽管不是必需的，但你可以在第一组和第二组方括号之间加一个空格。第二组方括号中的标签是不区分大小写的，并且可以包含字母、数字、空格或标点符号。

这意味着以下示例格式在链接的第一部分上是大致相同的：

```
[hobbit-hole][1]
[hobbit-hole] [1]
```

简而言之，第一部分的格式就是将链接文本放在第一组方括号中，第二组方括号包含一个标签，指向文档其他地方存储的 URL。

引用式链接的第二部分使用以下格式：

- 标签，放在方括号中，紧跟着一个冒号和至少一个空格（例如，`[label]: `）。
- 链接的 URL，可以选择用尖括号包围。
- 可选的链接标题，可以使用双引号、单引号或圆括号包围。

这意味着以下格式在链接的第二部分上是大致相同的：

```
[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle
[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles"
[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle 'Hobbit lifestyles'
[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle (Hobbit lifestyles)
[1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> "Hobbit lifestyles"
[1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> 'Hobbit lifestyles'
[1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> (Hobbit lifestyles)
```

你可以将链接的第二部分放置在 Markdown 文档的任何位置。有些人会将其紧跟在链接所在的段落后面，而其他人则将其放在文档的末尾（类似于尾注或脚注）。

以下是使用引用式链接的一个示例：<br>
这是一个示例，点击它你将访问 [markdownguide网站][1]。

[1]: https://www.markdownguide.org/

这样，整个 Markdown 文档的正文就不再有冗长的 URL，提高了可读性，同时保持了链接的功能性。

#### 链接最佳实践

Markdown 应用程序在处理 URL 中间的空格时可能存在不同的处理方式。为了兼容性，尽量使用 `%20` 来对空格进行 URL 编码。或者，如果你的 Markdown 应用程序支持 HTML，可以使用 HTML 标签。URL 中间的括号也可能会引发问题。为了兼容性，尽量使用 URL 编码来处理括号：将开括号 `(` 编码为 `%28`，将闭括号 `)` 编码为 `%29`。或者，如果你的 Markdown 应用程序支持 HTML，可以使用 HTML 标签。

### 图片
要添加图片，首先加上一个感叹号（!），然后在方括号中添加替代文本，再在圆括号中添加图片资源的路径或 URL。你可以选择性地在路径或 URL 后面加上标题，标题用引号括起来。<br>
注意：替代文本和链接的方括号中的文本作用不同，替代文本是用来描述 图片内容的，而链接中的文本则是用户可点击的显示内容。在 Markdown 中，图片的替代文本（alt text）是可选的，你可以不填写替代文本，但方括号 [] 还是需要保留。如果你不需要描述图片，只需留空方括号即可。<br>
下面是一个示例。<br>

```
![初音未来](./hatsune1.png)
```

渲染效果：<br>

![初音未来](./hatsune1.png)
![初音未来2](./hatsune2.png)

注意：./表示相对路径，从当前目录开始寻找文件。

#### 链接图片
要为图片添加链接，将图片的 Markdown 语法用方括号括起来，然后在后面加上链接的圆括号。<br>
以下是一个示例：<br>

```
[![An old rock in the desert](/assets/images/shiprock.jpg "Shiprock, New Mexico by Beau Rogers")](https://www.flickr.com/photos/beaurogers/31833779864/in/photolist-Qv3rFw-34mt9F-a9Cmfy-5Ha3Zi-9msKdv-o3hgjr-hWpUte-4WMsJ1-KUQ8N-deshUb-vssBD-6CQci6-8AFCiD-zsJWT-nNfsgB-dPDwZJ-bn9JGn-5HtSXY-6CUhAL-a4UTXB-ugPum-KUPSo-fBLNm-6CUmpy-4WMsc9-8a7D3T-83KJev-6CQ2bK-nNusHJ-a78rQH-nw3NvT-7aq2qf-8wwBso-3nNceh-ugSKP-4mh4kh-bbeeqH-a7biME-q3PtTf-brFpgb-cg38zw-bXMZc-nJPELD-f58Lmo-bXMYG-bz8AAi-bxNtNT-bXMYi-bXMY6-bXMYv)
```

### 转义字符
如果需要在 Markdown 文档中显示一个原本会用来格式化文本的特殊字符，可以在该字符前添加一个反斜杠 (`\`)。

例如：
`\* Without the backslash, this would be a bullet in an unordered list.`  
渲染输出如下：<br>
\* Without the backslash, this would be a bullet in an unordered list.  

#### 可以转义的字符
你可以使用反斜杠（`\`）转义以下字符：

| 字符 | 名称 |
|------|------|
| `\`  | 反斜杠 |
| `` ` `` | 反引号（另见代码中的反引号转义）|
| `*`  | 星号 |
| `_`  | 下划线 |
| `{ }` | 大括号 |
| `[ ]` | 方括号 |
| `< >` | 尖括号 |
| `( )` | 圆括号 |
| `#`  | 井号 |
| `+`  | 加号 |
| `-`  | 减号（或连字符）|
| `.`  | 点号 |
| `!`  | 感叹号 |
| `\|`  | 管道符号（另见表格中的管道符转义）|

表格的语法规则：
- 每行用管道符号 `|` 分隔列。
- 第一行是表头，后面用至少三个减号 `---` 表示表头与内容的分隔线。
- 第二行之后是表格的内容部分。

注意：
- `|------|------|`是 Markdown 表格 的一部分，它定义了表格中列与列之间的分隔线。
- 表格中每列的宽度由内容决定，管道符号 `|` 可以在左右加空格，便于对齐代码，但渲染时空格不会显示。
- 列之间的 `-` 数量可以多于三个，只要有三个即可符合语法要求。
- 表格分割线必须使用 `---`。
- 其他符号如 `***` 或 `___` 是水平分割线，而不是表格语法的一部分。
- 为了在表格内容中正常显示管道符号，你可以选择任意一种方式:使用反斜杠转义 `\|`，或者使用 HTML 转义字符 `&#124`;。

### HTML

许多 Markdown 应用允许在 Markdown 格式的文本中使用 HTML 标签。这在以下情况下非常有用：

- 如果你更喜欢用 HTML 标签而不是 Markdown 语法，例如一些人更习惯用 HTML 标签来插入图片。
- 当需要更改元素的属性时（例如指定文本颜色或更改图片宽度），HTML 标签也是非常实用的。

要使用 HTML，只需将 HTML 标签插入到 Markdown 格式的文件文本中。

示例代码：
```markdown
This **word** is bold. This <em>word</em> is italic.
```

渲染输出如下：

This **word** is bold. This <em>word</em> is italic.

#### HTML 最佳实践

出于安全考虑，并非所有 Markdown 应用都支持在 Markdown 文档中使用 HTML。当有疑问时，请查阅所使用 Markdown 应用的文档。某些应用只支持部分 HTML 标签。

- 使用空行将块级 HTML 元素（例如 `<div>`、`<table>`、`<pre>` 和 `<p>`）与周围内容分隔开。
- 尽量不要用制表符或空格缩进 HTML 标签，这可能会干扰格式化。

需要注意的是，Markdown 语法无法在块级 HTML 标签内使用。例如，以下代码将无法正常渲染：

```html
<p>italic and **bold**</p>
```
