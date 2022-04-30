# Guide to Markdown

# Markdown

## Reference
- [Markdown Syntax 'getgrav'](https://learn.getgrav.org/17/content/markdown)

- [教你Markdown+VSCODE实现最完美流畅写作体验](https://www.bilibili.com/video/BV1si4y1472o)



## Markdown notes

### heading

```markdown
## h2 Heading
### h3 Heading
#### h4 Heading
##### h5 Heading
###### h6 Heading
```

### 开头空格
```markdown
&emsp;
```
&emsp;&emsp;This is the main body of the text.This is the main body of the text.This is the main body of the text.This is the main body of the text.This 

### 空行
```markdown
The second paragraph
<br><br><br>
The third paragraph
```
The second paragraph
<br><br><br>
The third paragraph

### Blockquotes
```markdown
>Blockquotes
```

### insert image
```markdown
![steve and MacBook Air 2](Steve_Jobs_with_MacBook_Air_2.jpg "Steve Jobs with MacBook Air2")
```
![steve and MacBook Air 2](Steve_Jobs_with_MacBook_Air_2.jpg "Steve Jobs with MacBook Air2")

### insert link 
```markdown
[homepage](https://lianfengyeo.github.io)
```
[homepage](https://lianfengyeo.github.io)  

### justify (html)
```markdown
<p align = "justify"> 
Markdown is a lightweight markup language with plain-text-formatting syntax. Its design allows it to be converted to many output formats, but the original tool by the same name only supports HTML.[9] 
</p>
```
<p align = "justify"> 
Markdown is a lightweight markup language with plain-text-formatting syntax. Its design allows it to be converted to many output formats, but the original tool by the same name only supports HTML.[9] 
</p>

### 左对齐
```markdown
<p align="left">左对齐</p>
```
<p align="left">左对齐</p>

### 右对齐
```markdown
<p align="right">右对齐</p>
```
<p align="right">右对齐</p>

### 居中
```markdown
<center>居中</center>
```
<center>居中</center>

### equation
默认的行内公式分割符是 `$equ$` 和 `\\( equ \\)`
默认的公式块分割符是 `$$ equ $$` 和 `\\[ equ \\]`
```markdown
#行内公式
$c = \pm\sqrt{a^2 + b^2}$
#公式块
$$
c = \pm\sqrt{a^2 + b^2}
$$
```
$c = \pm\sqrt{a^2 + b^2}$

$$
c = \pm\sqrt{a^2 + b^2}
$$


等号对齐
```
$$
\begin{align}

F(x) & =  {\frac {1}{\sqrt {2\pi }}}\int _{-\infty }^{x}e^{-t^{2}/2}\,dt \\
     & =  {\frac {1}{2}}\left[1+\operatorname {erf} \left({\frac {x}{\sqrt {2}}}\right)\right]

\end{align}
$$
```










### bold
```markdown
**This is bold fonts**
```
**This is bold fonts**

### italic
```markdown
*italic*
```

### emoji render
Download icon from:  
[fontawesome](https://fontawesome.com/icons?d=gallery)  

<!-- 不渲染emoji时，前面的：变成{?:} eg:{?:}joy:    -->

```markdown
去露营啦! :(fas fa-campground fa-fw): 很快就回来.

真开心! :(far fa-grin-tears):

Gone camping! :tent: Be back soon.

That is so funny! :joy:

Gone camping! {?:}tent: Be back soon.

That is so funny! {?:}joy:
```
去露营啦! :(fas fa-campground fa-fw): 很快就回来.

真开心! :(far fa-grin-tears):

Gone camping! :tent: Be back soon.

That is so funny! :joy:

Gone camping! {?:}tent: Be back soon.

That is so funny! {?:}joy:



# BUILD-IN SHORTCODE 

## tweet

[`tweet` 的文档](https://gohugo.io/content-management/shortcodes#tweet)

一个 `tweet` 示例:

```markdown
{{</* tweet 877500564405444608 */>}}
```

呈现的输出效果如下:

{{< tweet 877500564405444608 >}}

## vimeo

[`vimeo` 的文档](https://gohugo.io/content-management/shortcodes#vimeo)

一个 `vimeo` 示例:

```markdown
{{</* vimeo 146022717 */>}}
```

呈现的输出效果如下:

{{< vimeo 146022717 >}}

## youtube

[`youtube` 的文档](https://gohugo.io/content-management/shortcodes#youtube)

一个 `youtube` 示例:

```markdown
{{</* youtube w7Ft2ymGmfc */>}}
```

呈现的输出效果如下:

{{< youtube w7Ft2ymGmfc >}}

<br>
<br>


# EXTENDED SHORTCODE
## 1 style

{{< version 0.2.0 changed >}}

{{< admonition >}}
Hugo **extended** version is necessary for `style` shortcode.
{{< /admonition >}}

`style` is a shortcode to insert custom style in your post.

The `style` shortcode has two positional parameters.

The **first** one is the custom style content,
which supports nesting syntax in [:(fab fa-sass fa-fw): SASS](https://sass-lang.com/documentation/style-rules/declarations#nesting)
and `&` referring to this parent HTML element.

And the **second** one is the tag name of the HTML element wrapping the content you want to change style, and whose default value is `div`.

Example `style` input:

```markdown
{{</* style "text-align:right; strong{color:#00b1ff;}" */>}}
This is a **right-aligned** paragraph.
{{</* /style */>}}
```

The rendered output looks like this:

{{< style "text-align:right; strong{color:#00b1ff;}" >}}
This is a **right-aligned** paragraph.
{{< /style >}}

## 2 link

{{< version 0.2.0 >}}

`link` shortcode is an alternative to [Markdown link syntax](../basic-markdown-syntax#links). `link` shortcode can provide some other features and can be used in code blocks.

{{< version 0.2.10 >}} The complete usage of [local resource references](../theme-documentation-content#contents-organization) is supported.

The `link` shortcode has the following named parameters:

* **href** *[required]* (**first** positional parameter)

    Destination of the link.

* **content** *[optional]* (**second** positional parameter)

    Content of the link, default value is the value of **href** parameter.

    *Markdown or HTML format is supported.*

* **title** *[optional]* (**third** positional parameter)

    `title` attribute of the HTML `a` tag, which will be shown when hovering on the link.

* **class** *[optional]*

    `class` attribute of the HTML `a` tag.

* **rel** *[optional]*

    Additional `rel` attributes of the HTML `a` tag.

Example `link` input:

```markdown
{{</* link "https://assemble.io" */>}}
Or
{{</* link href="https://assemble.io" */>}}

{{</* link "mailto:contact@revolunet.com" */>}}
Or
{{</* link href="mailto:contact@revolunet.com" */>}}

{{</* link "https://assemble.io" Assemble */>}}
Or
{{</* link href="https://assemble.io" content=Assemble */>}}
```

The rendered output looks like this:

* {{< link "https://assemble.io" >}}
* {{< link "mailto:contact@revolunet.com" >}}
* {{< link "https://assemble.io" Assemble >}}

Example `link` input with a title:

```markdown
{{</* link "https://github.com/upstage/" Upstage "Visit Upstage!" */>}}
Or
{{</* link href="https://github.com/upstage/" content=Upstage title="Visit Upstage!" */>}}
```

The rendered output looks like this (hover over the link, there should be a tooltip):

{{< link "https://github.com/upstage/" Upstage "Visit Upstage!" >}}

## 3 image {#image}

{{< version 0.2.0 changed >}}

`image` shortcode is an alternative to [`figure` shortcode](../theme-documentation-built-in-shortcodes#figure). `image` shortcode can take full advantage of the dependent libraries of [lazysizes](https://github.com/aFarkas/lazysizes) and [lightgallery.js](https://github.com/sachinchoolur/lightgallery.js).

{{< version 0.2.10 >}} The complete usage of [local resource references](../theme-documentation-content#contents-organization) is supported.

The `image` shortcode has the following named parameters:

* **src** *[required]* (**first** positional parameter)

    URL of the image to be displayed.

* **alt** *[optional]* (**second** positional parameter)

    Alternate text for the image if the image cannot be displayed, default value is the value of **src** parameter.

    *Markdown or HTML format is supported.*

* **caption** *[optional]* (**third** positional parameter)

    Image caption.

    *Markdown or HTML format is supported.*

* **title** *[optional]*

    Image title that will be shown when hovering on the image.

* **class** *[optional]*

    `class` attribute of the HTML `figure` tag.

* **src_s** *[optional]*

    URL of the image thumbnail, used for lightgallery, default value is the value of **src** parameter.

* **src_l** *[optional]*

    URL of the HD image, used for lightgallery, default value is the value of **src** parameter.

* **height** *[optional]*

    `height` attribute of the image.

* **width** *[optional]*

    `width` attribute of the image.

* **linked** *[optional]*

    Whether the image needs to be hyperlinked, default value is `true`.

* **rel** *[optional]*

    Additional `rel` attributes of the HTML `a` tag, if **linked** parameter is set to `true`.

Example `image` input:

```markdown
{{</* image src="/images/lighthouse.jpg" caption="Lighthouse (`image`)" src_s="/images/lighthouse-small.jpg" src_l="/images/lighthouse-large.jpg" */>}}
```

The rendered output looks like this:

{{< image src="/images/lighthouse.jpg" caption="Lighthouse (`image`)" src_s="/images/lighthouse-small.jpg" src_l="/images/lighthouse-large.jpg" >}}

## 4 admonition

The `admonition` shortcode supports **12** types of banners to help you put notice in your page.

*Markdown or HTML format in the content is supported.*

{{< admonition >}}
A **note** banner
{{< /admonition >}}

{{< admonition abstract >}}
An **abstract** banner
{{< /admonition >}}

{{< admonition info >}}
A **info** banner
{{< /admonition >}}

{{< admonition tip >}}
A **tip** banner
{{< /admonition >}}

{{< admonition success >}}
A **success** banner
{{< /admonition >}}

{{< admonition question >}}
A **question** banner
{{< /admonition >}}

{{< admonition warning >}}
A **warning** banner
{{< /admonition >}}

{{< admonition failure >}}
A **failure** banner
{{< /admonition >}}

{{< admonition danger >}}
A **danger** banner
{{< /admonition >}}

{{< admonition bug >}}
A **bug** banner
{{< /admonition >}}

{{< admonition example >}}
An **example** banner
{{< /admonition >}}

{{< admonition quote >}}
A **quote** banner
{{< /admonition >}}

The `admonition` shortcode has the following named parameters:

* **type** *[optional]* (**first** positional parameter)

    Type of the `admonition` banner, default value is `note`.

* **title** *[optional]* (**second** positional parameter)

    Title of the `admonition` banner, default value is the value of **type** parameter.

* **open** *[optional]* (**third** positional parameter) {{< version 0.2.0 changed >}}

    Whether the content will be expandable by default, default value is `true`.

Example `admonition` input:

```markdown
{{</* admonition type=tip title="This is a tip" open=false */>}}
A **tip** banner
{{</* /admonition */>}}
Or
{{</* admonition tip "This is a tip" false */>}}
A **tip** banner
{{</* /admonition */>}}
```

The rendered output looks like this:

{{< admonition tip "This is a tip" false >}}
A **tip** banner
{{< /admonition >}}

## 5 mermaid

[mermaid](https://mermaidjs.github.io/) is a library helping you to generate diagram and flowcharts from text, in a similar manner as Markdown.

Just insert your mermaid code in the `mermaid` shortcode and that’s it.

### 5.1 Flowchart {#flowchart}

Example **flowchart** `mermaid` input:

```markdown
{{</* mermaid */>}}
graph LR;
    A[Hard edge] -->|Link text| B(Round edge)
    B --> C{Decision}
    C -->|One| D[Result one]
    C -->|Two| E[Result two]
{{</* /mermaid */>}}
```

The rendered output looks like this:

{{< mermaid >}}
graph LR;
    A[Hard edge] -->|Link text| B(Round edge)
    B --> C{Decision}
    C -->|One| D[Result one]
    C -->|Two| E[Result two]
{{< /mermaid >}}

### 5.2 Sequence Diagram {#sequence-diagram}

Example **sequence diagram** `mermaid` input:

```markdown
{{</* mermaid */>}}
sequenceDiagram
    participant Alice
    participant Bob
    Alice->>John: Hello John, how are you?
    loop Healthcheck
        John->John: Fight against hypochondria
    end
    Note right of John: Rational thoughts <br/>prevail...
    John-->Alice: Great!
    John->Bob: How about you?
    Bob-->John: Jolly good!
{{</* /mermaid */>}}
```

The rendered output looks like this:

{{< mermaid >}}
sequenceDiagram
    participant Alice
    participant Bob
    Alice->>John: Hello John, how are you?
    loop Healthcheck
        John->John: Fight against hypochondria
    end
    Note right of John: Rational thoughts <br/>prevail...
    John-->Alice: Great!
    John->Bob: How about you?
    Bob-->John: Jolly good!
{{< /mermaid >}}

### 5.3 GANTT {#gantt}

Example **GANTT** `mermaid` input:

```markdown
{{</* mermaid */>}}
gantt
    dateFormat  YYYY-MM-DD
    title Adding GANTT diagram functionality to mermaid
    section A section
    Completed task            :done,    des1, 2014-01-06,2014-01-08
    Active task               :active,  des2, 2014-01-09, 3d
    Future task               :         des3, after des2, 5d
    Future task2               :         des4, after des3, 5d
    section Critical tasks
    Completed task in the critical line :crit, done, 2014-01-06,24h
    Implement parser and jison          :crit, done, after des1, 2d
    Create tests for parser             :crit, active, 3d
    Future task in critical line        :crit, 5d
    Create tests for renderer           :2d
    Add to mermaid                      :1d
{{</* /mermaid */>}}
```

The rendered output looks like this:

{{< mermaid >}}
gantt
    dateFormat  YYYY-MM-DD
    title Adding GANTT diagram functionality to mermaid
    section A section
    Completed task            :done,    des1, 2014-01-06,2014-01-08
    Active task               :active,  des2, 2014-01-09, 3d
    Future task               :         des3, after des2, 5d
    Future task2               :         des4, after des3, 5d
    section Critical tasks
    Completed task in the critical line :crit, done, 2014-01-06,24h
    Implement parser and jison          :crit, done, after des1, 2d
    Create tests for parser             :crit, active, 3d
    Future task in critical line        :crit, 5d
    Create tests for renderer           :2d
    Add to mermaid                      :1d
{{< /mermaid >}}

### 5.4 Class Diagram {#class-diagram}

Example **class diagram** `mermaid` input:

```markdown
{{</* mermaid */>}}
classDiagram
    Class01 <|-- AveryLongClass : Cool
    Class03 *-- Class04
    Class05 o-- Class06
    Class07 .. Class08
    Class09 --> C2 : Where am i?
    Class09 --* C3
    Class09 --|> Class07
    Class07 : equals()
    Class07 : Object[] elementData
    Class01 : size()
    Class01 : int chimp
    Class01 : int gorilla
    Class08 <--> C2: Cool label
{{</* /mermaid */>}}
```

The rendered output looks like this:

{{< mermaid >}}
classDiagram
    Class01 <|-- AveryLongClass : Cool
    Class03 *-- Class04
    Class05 o-- Class06
    Class07 .. Class08
    Class09 --> C2 : Where am i?
    Class09 --* C3
    Class09 --|> Class07
    Class07 : equals()
    Class07 : Object[] elementData
    Class01 : size()
    Class01 : int chimp
    Class01 : int gorilla
    Class08 <--> C2: Cool label
{{< /mermaid >}}

### 5.5 State Diagram {#state-diagram}

Example **state diagram** `mermaid` input:

```markdown
{{</* mermaid */>}}
stateDiagram
    [*] --> Still
    Still --> [*]
    Still --> Moving
    Moving --> Still
    Moving --> Crash
    Crash --> [*]
{{</* /mermaid */>}}
```

The rendered output looks like this:

{{< mermaid >}}
stateDiagram
    [*] --> Still
    Still --> [*]
    Still --> Moving
    Moving --> Still
    Moving --> Crash
    Crash --> [*]
{{< /mermaid >}}

### 5.6 Git Graph {#git-graph}

Example **git graph** `mermaid` input:

```markdown
{{</* mermaid */>}}
gitGraph:
options
{
    "nodeSpacing": 100,
    "nodeRadius": 10
}
end
    commit
    branch newbranch
    checkout newbranch
    commit
    commit
    checkout master
    commit
    commit
    merge newbranch
{{</* /mermaid */>}}
```

The rendered output looks like this:

{{< mermaid >}}
gitGraph:
options
{
    "nodeSpacing": 100,
    "nodeRadius": 10
}
end
    commit
    branch newbranch
    checkout newbranch
    commit
    commit
    checkout master
    commit
    commit
    merge newbranch
{{< /mermaid >}}

### 5.7 Pie {#pie}

Example **pie** `mermaid` input:

```markdown
{{</* mermaid */>}}
pie
    "Dogs" : 386
    "Cats" : 85
    "Rats" : 15
{{</* /mermaid */>}}
```

The rendered output looks like this:

{{< mermaid >}}
pie
    "Dogs" : 386
    "Cats" : 85
    "Rats" : 15
{{< /mermaid >}}

## 6 echarts

[ECharts](https://echarts.apache.org/) is a library helping you to generate interactive data visualization.

The basic chart types ECharts supports include [line series](https://echarts.apache.org/en/option.html#series-line), [bar series](https://echarts.apache.org/en/option.html#series-line), [scatter series](https://echarts.apache.org/en/option.html#series-scatter), [pie charts](https://echarts.apache.org/en/option.html#series-pie), [candle-stick series](https://echarts.apache.org/en/option.html#series-candlestick), [boxplot series](https://echarts.apache.org/en/option.html#series-boxplot) for statistics, [map series](https://echarts.apache.org/en/option.html#series-map), [heatmap series](https://echarts.apache.org/en/option.html#series-heatmap), [lines series](https://echarts.apache.org/en/option.html#series-lines) for directional information, [graph series](https://echarts.apache.org/en/option.html#series-graph) for relationships, [treemap series](https://echarts.apache.org/en/option.html#series-treemap), [sunburst series](https://echarts.apache.org/en/option.html#series-sunburst), [parallel series](https://echarts.apache.org/en/option.html#series-parallel) for multi-dimensional data, [funnel series](https://echarts.apache.org/en/option.html#series-funnel), [gauge series](https://echarts.apache.org/en/option.html#series-gauge). And it's extremely easy to create a combinition of them with ECharts.

Just insert your ECharts option in `JSON`/`YAML`/`TOML` format in the `echarts` shortcode and that’s it.

Example `echarts` input in `JSON` format:

```json
{{</* echarts */>}}
{
  "title": {
    "text": "Summary Line Chart",
    "top": "2%",
    "left": "center"
  },
  "tooltip": {
    "trigger": "axis"
  },
  "legend": {
    "data": ["Email Marketing", "Affiliate Advertising", "Video Advertising", "Direct View", "Search Engine"],
    "top": "10%"
  },
  "grid": {
    "left": "5%",
    "right": "5%",
    "bottom": "5%",
    "top": "20%",
    "containLabel": true
  },
  "toolbox": {
    "feature": {
      "saveAsImage": {
        "title": "Save as Image"
      }
    }
  },
  "xAxis": {
    "type": "category",
    "boundaryGap": false,
    "data": ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday", "Sunday"]
  },
  "yAxis": {
    "type": "value"
  },
  "series": [
    {
      "name": "Email Marketing",
      "type": "line",
      "stack": "Total",
      "data": [120, 132, 101, 134, 90, 230, 210]
    },
    {
      "name": "Affiliate Advertising",
      "type": "line",
      "stack": "Total",
      "data": [220, 182, 191, 234, 290, 330, 310]
    },
    {
      "name": "Video Advertising",
      "type": "line",
      "stack": "Total",
      "data": [150, 232, 201, 154, 190, 330, 410]
    },
    {
      "name": "Direct View",
      "type": "line",
      "stack": "Total",
      "data": [320, 332, 301, 334, 390, 330, 320]
    },
    {
      "name": "Search Engine",
      "type": "line",
      "stack": "Total",
      "data": [820, 932, 901, 934, 1290, 1330, 1320]
    }
  ]
}
{{</* /echarts */>}}
```

The same in `YAML` format:

```yaml
{{</* echarts */>}}
title:
    text: Summary Line Chart
    top: 2%
    left: center
tooltip:
    trigger: axis
legend:
    data:
        - Email Marketing
        - Affiliate Advertising
        - Video Advertising
        - Direct View
        - Search Engine
    top: 10%
grid:
    left: 5%
    right: 5%
    bottom: 5%
    top: 20%
    containLabel: true
toolbox:
    feature:
        saveAsImage:
            title: Save as Image
xAxis:
    type: category
    boundaryGap: false
    data:
        - Monday
        - Tuesday
        - Wednesday
        - Thursday
        - Friday
        - Saturday
        - Sunday
yAxis:
    type: value
series:
    - name: Email Marketing
      type: line
      stack: Total
      data:
          - 120
          - 132
          - 101
          - 134
          - 90
          - 230
          - 210
    - name: Affiliate Advertising
      type: line
      stack: Total
      data:
          - 220
          - 182
          - 191
          - 234
          - 290
          - 330
          - 310
    - name: Video Advertising
      type: line
      stack: Total
      data:
          - 150
          - 232
          - 201
          - 154
          - 190
          - 330
          - 410
    - name: Direct View
      type: line
      stack: Total
      data:
          - 320
          - 332
          - 301
          - 334
          - 390
          - 330
          - 320
    - name: Search Engine
      type: line
      stack: Total
      data:
          - 820
          - 932
          - 901
          - 934
          - 1290
          - 1330
          - 1320
{{</* /echarts */>}}
```

The same in `TOML` format:

```toml
{{</* echarts */>}}
[title]
text = "Summary Line Chart"
top = "2%"
left = "center"

[tooltip]
trigger = "axis"

[legend]
data = [
  "Email Marketing",
  "Affiliate Advertising",
  "Video Advertising",
  "Direct View",
  "Search Engine"
]
top = "10%"

[grid]
left = "5%"
right = "5%"
bottom = "5%"
top = "20%"
containLabel = true

[toolbox]
[toolbox.feature]
[toolbox.feature.saveAsImage]
title = "Save as Image"

[xAxis]
type = "category"
boundaryGap = false
data = [
  "Monday",
  "Tuesday",
  "Wednesday",
  "Thursday",
  "Friday",
  "Saturday",
  "Sunday"
]

[yAxis]
type = "value"

[[series]]
name = "Email Marketing"
type = "line"
stack = "Total"
data = [
  120.0,
  132.0,
  101.0,
  134.0,
  90.0,
  230.0,
  210.0
]

[[series]]
name = "Affiliate Advertising"
type = "line"
stack = "Total"
data = [
  220.0,
  182.0,
  191.0,
  234.0,
  290.0,
  330.0,
  310.0
]

[[series]]
name = "Video Advertising"
type = "line"
stack = "Total"
data = [
  150.0,
  232.0,
  201.0,
  154.0,
  190.0,
  330.0,
  410.0
]

[[series]]
name = "Direct View"
type = "line"
stack = "Total"
data = [
  320.0,
  332.0,
  301.0,
  334.0,
  390.0,
  330.0,
  320.0
]

[[series]]
name = "Search Engine"
type = "line"
stack = "Total"
data = [
  820.0,
  932.0,
  901.0,
  934.0,
  1290.0,
  1330.0,
  1320.0
]
{{</* /echarts */>}}
```

The rendered output looks like this:

{{< echarts >}}
{
  "title": {
    "text": "Summary Line Chart",
    "top": "2%",
    "left": "center"
  },
  "tooltip": {
    "trigger": "axis"
  },
  "legend": {
    "data": ["Email Marketing", "Affiliate Advertising", "Video Advertising", "Direct View", "Search Engine"],
    "top": "10%"
  },
  "grid": {
    "left": "5%",
    "right": "5%",
    "bottom": "5%",
    "top": "20%",
    "containLabel": true
  },
  "toolbox": {
    "feature": {
      "saveAsImage": {
        "title": "Save as Image"
      }
    }
  },
  "xAxis": {
    "type": "category",
    "boundaryGap": false,
    "data": ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday", "Sunday"]
  },
  "yAxis": {
    "type": "value"
  },
  "series": [
    {
      "name": "Email Marketing",
      "type": "line",
      "stack": "Total",
      "data": [120, 132, 101, 134, 90, 230, 210]
    },
    {
      "name": "Affiliate Advertising",
      "type": "line",
      "stack": "Total",
      "data": [220, 182, 191, 234, 290, 330, 310]
    },
    {
      "name": "Video Advertising",
      "type": "line",
      "stack": "Total",
      "data": [150, 232, 201, 154, 190, 330, 410]
    },
    {
      "name": "Direct View",
      "type": "line",
      "stack": "Total",
      "data": [320, 332, 301, 334, 390, 330, 320]
    },
    {
      "name": "Search Engine",
      "type": "line",
      "stack": "Total",
      "data": [820, 932, 901, 934, 1290, 1330, 1320]
    }
  ]
}
{{< /echarts >}}

The `echarts` shortcode has also the following named parameters:

* **width** *[optional]* (**first** positional parameter)

    {{< version 0.2.0 >}} Width of the data visualization, default value is `100%`.

* **height** *[optional]* (**second** positional parameter)

    {{< version 0.2.0 >}} Height of the data visualization, default value is `30rem`.

## 7 mapbox

{{< version 0.2.0 >}}

[Mapbox GL JS](https://docs.mapbox.com/mapbox-gl-js) is a JavaScript library that uses WebGL to render interactive maps from [vector tiles](https://docs.mapbox.com/help/glossary/vector-tiles/) and [Mapbox styles](https://docs.mapbox.com/mapbox-gl-js/style-spec/).

The `mapbox` shortcode has the following named parameters to use Mapbox GL JS:

* **lng** *[required]* (**first** positional parameter)

    Longitude of the inital centerpoint of the map, measured in degrees.

* **lat** *[required]* (**second** positional parameter)

    Latitude of the inital centerpoint of the map, measured in degrees.

* **zoom** *[optional]* (**third** positional parameter)

    The initial zoom level of the map, default value is `10`.

* **marked** *[optional]* (**fourth** positional parameter)

    Whether to add a marker at the inital centerpoint of the map, default value is `true`.

* **light-style** *[optional]* (**fifth** positional parameter)

    Style for the light theme, default value is the value set in the [front matter](../theme-documentation-content#front-matter) or the [site configuration](../theme-documentation-basics#site-configuration).

* **dark-style** *[optional]* (**sixth** positional parameter)

    Style for the dark theme, default value is the value set in the [front matter](../theme-documentation-content#front-matter) or the [site configuration](../theme-documentation-basics#site-configuration).

* **navigation** *[optional]*

    Whether to add [NavigationControl](https://docs.mapbox.com/mapbox-gl-js/api#navigationcontrol), default value is the value set in the [front matter](../theme-documentation-content#front-matter) or the [site configuration](../theme-documentation-basics#site-configuration).

* **geolocate** *[optional]*

    Whether to add [GeolocateControl](https://docs.mapbox.com/mapbox-gl-js/api#geolocatecontrol), default value is the value set in the [front matter](../theme-documentation-content#front-matter) or the [site configuration](../theme-documentation-basics#site-configuration).

* **scale** *[optional]*

    Whether to add [ScaleControl](https://docs.mapbox.com/mapbox-gl-js/api#scalecontrol), default value is the value set in the [front matter](../theme-documentation-content#front-matter) or the [site configuration](../theme-documentation-basics#site-configuration).

* **fullscreen** *[optional]*

    Whether to add [FullscreenControl](https://docs.mapbox.com/mapbox-gl-js/api#fullscreencontrol), default value is the value set in the [front matter](../theme-documentation-content#front-matter) or the [site configuration](../theme-documentation-basics#site-configuration).

* **width** *[optional]*

    Width of the map, default value is `100%`.

* **height** *[optional]*

    Height of the map, default value is `20rem`.

Example simple `mapbox` input:

```markdown
{{</* mapbox 121.485 31.233 12 */>}}
Or
{{</* mapbox lng=121.485 lat=31.233 zoom=12 */>}}
```

The rendered output looks like this:

{{< mapbox 121.485 31.233 12 >}}

Example `mapbox` input with the custom style:

```markdown
{{</* mapbox -122.252 37.453 10 false "mapbox://styles/mapbox/navigation-preview-day-v4" "mapbox://styles/mapbox/navigation-preview-night-v4" */>}}
Or
{{</* mapbox lng=-122.252 lat=37.453 zoom=10 marked=false light-style="mapbox://styles/mapbox/navigation-preview-day-v4" dark-style="mapbox://styles/mapbox/navigation-preview-night-v4" */>}}
```

The rendered output looks like this:

{{< mapbox -122.252 37.453 10 false "mapbox://styles/mapbox/navigation-preview-day-v4?optimize=true" "mapbox://styles/mapbox/navigation-preview-night-v4?optimize=true" >}}

## 8 music

The `music` shortcode embeds a responsive music player based on [APlayer](https://github.com/MoePlayer/APlayer) and [MetingJS](https://github.com/metowolf/MetingJS).

There are three ways to use it the `music` shortcode.

### 8.1 Custom Music URL {#custom-music-url}

{{< version 0.2.10 >}} The complete usage of [local resource references](../theme-documentation-content#contents-organization) is supported.

The `music` shortcode has the following named parameters by custom music URL:

* **server** *[required]*

    URL of the custom music.

* **name** *[optional]*

    Name of the custom music.

* **artist** *[optional]*

    Artist of the custom music.

* **cover** *[required]*

    URL of the custom music cover.

Example `music` input by custom music URL:

```markdown
{{</* music url="/music/Wavelength.mp3" name=Wavelength artist=oldmanyoung cover="/images/Wavelength.jpg" */>}}
```

The rendered output looks like this:

{{< music url="/music/Wavelength.mp3" name=Wavelength artist=oldmanyoung cover="/images/Wavelength.jpg" >}}

### 8.2 Music Platform URL Automatic Identification {#automatic-identification}

The `music` shortcode has one named parameter by music platform URL automatic identification:

* **auto** *[required]* (**first** positional parameter)

    URL of the music platform URL for automatic identification,
    which supports `netease`, `tencent` and `xiami` music platform.

Example `music` input by music platform URL automatic identification:

```markdown
{{</* music auto="https://music.163.com/#/playlist?id=60198" */>}}
Or
{{</* music "https://music.163.com/#/playlist?id=60198" */>}}
```

The rendered output looks like this:

{{< music auto="https://music.163.com/#/playlist?id=60198" >}}

### 8.3 Custom Server, Type and ID {#custom-server}

The `music` shortcode has the following named parameters by custom music platform:

* **server** *[required]* (**first** positional parameter)

    [`netease`, `tencent`, `kugou`, `xiami`, `baidu`]

    Music platform.

* **type** *[required]* (**second** positional parameter)

    [`song`, `playlist`, `album`, `search`, `artist`]

    Type of the music.

* **id** *[required]* (**third** positional parameter)

    Song ID, or playlist ID, or album ID, or search keyword, or artist ID.

Example `music` input by custom music platform:

```markdown
{{</* music server="netease" type="song" id="1868553" */>}}
Or
{{</* music netease song 1868553 */>}}
```

The rendered output looks like this:

{{< music netease song 1868553 >}}

### 8.4 Other Parameters {#other-parameters}

The `music` shortcode has other named parameters applying to the above three ways:

* **theme** *[optional]*

    {{< version 0.2.0 changed >}} Main color of the music player, default value is `#448aff`.

* **fixed** *[optional]*

    Whether to enable fixed mode, default value is `false`.

* **mini** *[optional]*

    Whether to enable mini mode, default value is `false`.

* **autoplay** *[optional]*

    Whether to autoplay music, default value is `false`.

* **volume** *[optional]*

    Default volume when the player is first opened, which will be remembered in the browser, default value is `0.7`.

* **mutex** *[optional]*

    Whether to pause other players when this player starts playing, default value is `true`.

The `music` shortcode has the following named parameters only applying to the type of music list:

* **loop** *[optional]*

    [`all`, `one`, `none`]

    Loop mode of the music list, default value is `none`.

* **order** *[optional]*

    [`list`, `random`]

    Play order of the music list, default value is `list`.

* **list-folded** *[optional]*

    Whether the music list should be folded at first, default value is `false`.

* **list-max-height** *[optional]*

    Max height of the music list, default value is `340px`.

## 9 bilibili

{{< version 0.2.0 changed >}}

The `bilibili` shortcode embeds a responsive video player for bilibili videos.

When the video only has one part, only the BV `id` of the video is required, e.g.:

```code
https://www.bilibili.com/video/BV1Sx411T7QQ
```

Example `bilibili` input:

```markdown
{{</* bilibili BV1Sx411T7QQ */>}}
Or
{{</* bilibili id=BV1Sx411T7QQ */>}}
```

The rendered output looks like this:

{{< bilibili id=BV1Sx411T7QQ >}}

When the video has multiple parts, in addition to the BV `id` of the video,
`p` is also required, whose default value is `1`, e.g.:

```code
https://www.bilibili.com/video/BV1TJ411C7An?p=3
```

Example `bilibili` input with `p`:

```markdown
{{</* bilibili BV1TJ411C7An 3 */>}}
Or
{{</* bilibili id=BV1TJ411C7An p=3 */>}}
```

The rendered output looks like this:

{{< bilibili id=BV1TJ411C7An p=3 >}}

## 10 typeit

The `typeit` shortcode provides typing animation based on [TypeIt](https://typeitjs.com/).

Just insert your content in the `typeit` shortcode and that’s it.

### 10.1 Simple Content {#simple-content}

Simple content is allowed in `Markdown` format and **without** rich block content such as images and more...

Example `typeit` input:

```markdown
{{</* typeit */>}}
This is a *paragraph* with **typing animation** based on [TypeIt](https://typeitjs.com/)...
{{</* /typeit */>}}
```

The rendered output looks like this:

{{< typeit >}}
This is a *paragraph* with **typing animation** based on [TypeIt](https://typeitjs.com/)...
{{< /typeit >}}

Alternatively, you can use custom **HTML tags**.

Example `typeit` input with `h4` tag:

```markdown
{{</* typeit tag=h4 */>}}
This is a *paragraph* with **typing animation** based on [TypeIt](https://typeitjs.com/)...
{{</* /typeit */>}}
```

The rendered output looks like this:

{{< typeit tag=h4 >}}
This is a *paragraph* with **typing animation** based on [TypeIt](https://typeitjs.com/)...
{{< /typeit >}}

### 10.2 Code Content {#code-content}

Code content is allowed and will be highlighted by named parameter `code` for the type of code language.

Example `typeit` input with `code`:

```markdown
{{</* typeit code=java */>}}
public class HelloWorld {
    public static void main(String []args) {
        System.out.println("Hello World");
    }
}
{{</* /typeit */>}}
```

The rendered output looks like this:

{{< typeit code=java >}}
public class HelloWorld {
    public static void main(String []args) {
        System.out.println("Hello World");
    }
}
{{< /typeit >}}

### 10.3 Group Content {#group-content}

All typing animations start at the same time by default.
But sometimes you may want to start a set of `typeit` contents in order.

A set of `typeit` contents with the same value of named parameter `group` will start typing animation in sequence.

Example `typeit` input with `group`:

```markdown
{{</* typeit group=paragraph */>}}
**First** this paragraph begins
{{</* /typeit */>}}

{{</* typeit group=paragraph */>}}
**Then** this paragraph begins
{{</* /typeit */>}}
```

The rendered output looks like this:

{{< typeit group=paragraph >}}
**First** this paragraph begins
{{< /typeit >}}

{{< typeit group=paragraph >}}
**Then** this paragraph begins
{{< /typeit >}}

## 11 script

{{< version 0.2.8 >}}

`script` is a shortcode to insert custom **:(fab fa-js fa-fw): Javascript** in your post.

{{< admonition >}}
The script content can be guaranteed to be executed in order after all third-party libraries are loaded. So you are free to use third-party libraries.
{{< /admonition >}}

Example `script` input:

```markdown
{{</* script */>}}
console.log('Hello LoveIt!');
{{</* /script */>}}
```

You can see the output in the console of the developer tool.

{{< script >}}
console.log('Hello LoveIt!');
{{< /script >}}







# EMOJI
## Smileys & Emotion
### Face Smiling

|          icon           | code                          |        icon        | code               |
| :---------------------: | ----------------------------- | :----------------: | ------------------ |
|       :grinning:        | `grinning`                    |      :smiley:      | `smiley`           |
|         :smile:         | `smile`                       |       :grin:       | `grin`             |
|       :laughing:        | `laughing` <br /> `satisfied` |   :sweat_smile:    | `sweat_smile`      |
|         :rofl:          | `rofl`                        |       :joy:        | `joy`              |
| :slightly_smiling_face: | `slightly_smiling_face`       | :upside_down_face: | `upside_down_face` |
|         :wink:          | `wink`                        |      :blush:       | `blush`            |
|       :innocent:        | `innocent`                    |                    |                    |

### Face Affection

|         icon          | code                  |          icon          | code                   |
| :-------------------: | --------------------- | :--------------------: | ---------------------- |
|     :heart_eyes:      | `heart_eyes`          |    :kissing_heart:     | `kissing_heart`        |
|       :kissing:       | `kissing`             |       :relaxed:        | `relaxed`              |
| :kissing_closed_eyes: | `kissing_closed_eyes` | :kissing_smiling_eyes: | `kissing_smiling_eyes` |

### Face Tongue

|              icon              | code                           |              icon              | code                           |
| :----------------------------: | ------------------------------ | :----------------------------: | ------------------------------ |
|             :yum:              | `yum`                          |       :stuck_out_tongue:       | `stuck_out_tongue`             |
| :stuck_out_tongue_winking_eye: | `stuck_out_tongue_winking_eye` | :stuck_out_tongue_closed_eyes: | `stuck_out_tongue_closed_eyes` |
|       :money_mouth_face:       | `money_mouth_face`             |                                |                                |

### Face Hand

|  icon  | code   |    icon    | code       |
| :----: | ------ | :--------: | ---------- |
| :hugs: | `hugs` | :thinking: | `thinking` |

### Face Neutral Skeptical

|        icon         | code                |      icon      | code           |
| :-----------------: | ------------------- | :------------: | -------------- |
| :zipper_mouth_face: | `zipper_mouth_face` | :neutral_face: | `neutral_face` |
|  :expressionless:   | `expressionless`    |   :no_mouth:   | `no_mouth`     |
|       :smirk:       | `smirk`             |   :unamused:   | `unamused`     |
|     :roll_eyes:     | `roll_eyes`         |  :grimacing:   | `grimacing`    |
|    :lying_face:     | `lying_face`        |                |                |

### Face Sleepy

|    icon    | code       |      icon       | code            |
| :--------: | ---------- | :-------------: | --------------- |
| :relieved: | `relieved` |    :pensive:    | `pensive`       |
|  :sleepy:  | `sleepy`   | :drooling_face: | `drooling_face` |
| :sleeping: | `sleeping` |                 |                 |

### Face Unwell

|           icon           | code                     |          icon           | code                    |
| :----------------------: | ------------------------ | :---------------------: | ----------------------- |
|          :mask:          | `mask`                   | :face_with_thermometer: | `face_with_thermometer` |
| :face_with_head_bandage: | `face_with_head_bandage` |    :nauseated_face:     | `nauseated_face`        |
|     :sneezing_face:      | `sneezing_face`          |      :dizzy_face:       | `dizzy_face`            |

### Face Hat

|       icon        | code              | icon  | code |
| :---------------: | ----------------- | :---: | ---- |
| :cowboy_hat_face: | `cowboy_hat_face` |       |      |

### Face Glasses

|     icon     | code         |    icon     | code        |
| :----------: | ------------ | :---------: | ----------- |
| :sunglasses: | `sunglasses` | :nerd_face: | `nerd_face` |

### Face Concerned

|           icon           | code                     |      icon       | code            |
| :----------------------: | ------------------------ | :-------------: | --------------- |
|        :confused:        | `confused`               |    :worried:    | `worried`       |
| :slightly_frowning_face: | `slightly_frowning_face` | :frowning_face: | `frowning_face` |
|       :open_mouth:       | `open_mouth`             |    :hushed:     | `hushed`        |
|       :astonished:       | `astonished`             |    :flushed:    | `flushed`       |
|        :frowning:        | `frowning`               |   :anguished:   | `anguished`     |
|        :fearful:         | `fearful`                |  :cold_sweat:   | `cold_sweat`    |
| :disappointed_relieved:  | `disappointed_relieved`  |      :cry:      | `cry`           |
|          :sob:           | `sob`                    |    :scream:     | `scream`        |
|       :confounded:       | `confounded`             |   :persevere:   | `persevere`     |
|      :disappointed:      | `disappointed`           |     :sweat:     | `sweat`         |
|         :weary:          | `weary`                  |  :tired_face:   | `tired_face`    |

### Face Negative

|          icon          | code                   |     icon      | code                 |
| :--------------------: | ---------------------- | :-----------: | -------------------- |
|       :triumph:        | `triumph`              |    :pout:     | `pout` <br /> `rage` |
|        :angry:         | `angry`                | :smiling_imp: | `smiling_imp`        |
|         :imp:          | `imp`                  |    :skull:    | `skull`              |
| :skull_and_crossbones: | `skull_and_crossbones` |               |                      |

### Face Costume

|      icon       | code                                 |       icon        | code              |
| :-------------: | ------------------------------------ | :---------------: | ----------------- |
|    :hankey:     | `hankey` <br /> `poop` <br /> `shit` |   :clown_face:    | `clown_face`      |
| :japanese_ogre: | `japanese_ogre`                      | :japanese_goblin: | `japanese_goblin` |
|     :ghost:     | `ghost`                              |      :alien:      | `alien`           |
| :space_invader: | `space_invader`                      |      :robot:      | `robot`           |

### Cat Face

|     icon      | code          |       icon        | code              |
| :-----------: | ------------- | :---------------: | ----------------- |
| :smiley_cat:  | `smiley_cat`  |    :smile_cat:    | `smile_cat`       |
|   :joy_cat:   | `joy_cat`     | :heart_eyes_cat:  | `heart_eyes_cat`  |
|  :smirk_cat:  | `smirk_cat`   |   :kissing_cat:   | `kissing_cat`     |
| :scream_cat:  | `scream_cat`  | :crying_cat_face: | `crying_cat_face` |
| :pouting_cat: | `pouting_cat` |                   |                   |

### Monkey Face

|      icon       | code            |      icon      | code           |
| :-------------: | --------------- | :------------: | -------------- |
|  :see_no_evil:  | `see_no_evil`   | :hear_no_evil: | `hear_no_evil` |
| :speak_no_evil: | `speak_no_evil` |                |                |

### Emotion

|           icon            | code                      |        icon         | code                |
| :-----------------------: | ------------------------- | :-----------------: | ------------------- |
|          :kiss:           | `kiss`                    |    :love_letter:    | `love_letter`       |
|          :cupid:          | `cupid`                   |    :gift_heart:     | `gift_heart`        |
|     :sparkling_heart:     | `sparkling_heart`         |    :heartpulse:     | `heartpulse`        |
|        :heartbeat:        | `heartbeat`               | :revolving_hearts:  | `revolving_hearts`  |
|       :two_hearts:        | `two_hearts`              | :heart_decoration:  | `heart_decoration`  |
| :heavy_heart_exclamation: | `heavy_heart_exclamation` |   :broken_heart:    | `broken_heart`      |
|          :heart:          | `heart`                   |   :yellow_heart:    | `yellow_heart`      |
|       :green_heart:       | `green_heart`             |    :blue_heart:     | `blue_heart`        |
|      :purple_heart:       | `purple_heart`            |    :black_heart:    | `black_heart`       |
|           :100:           | `100`                     |       :anger:       | `anger`             |
|          :boom:           | `boom` <br /> `collision` |       :dizzy:       | `dizzy`             |
|       :sweat_drops:       | `sweat_drops`             |       :dash:        | `dash`              |
|          :hole:           | `hole`                    |       :bomb:        | `bomb`              |
|     :speech_balloon:      | `speech_balloon`          | :eye_speech_bubble: | `eye_speech_bubble` |
|   :right_anger_bubble:    | `right_anger_bubble`      |  :thought_balloon:  | `thought_balloon`   |
|           :zzz:           | `zzz`                     |                     |                     |

## People & Body

### Hand Fingers Open

|                icon                | code                               |         icon          | code                        |
| :--------------------------------: | ---------------------------------- | :-------------------: | --------------------------- |
|               :wave:               | `wave`                             | :raised_back_of_hand: | `raised_back_of_hand`       |
| :raised_hand_with_fingers_splayed: | `raised_hand_with_fingers_splayed` |        :hand:         | `hand` <br /> `raised_hand` |
|          :vulcan_salute:           | `vulcan_salute`                    |                       |                             |

### Hand Fingers Partial

|       icon        | code              |  icon   | code    |
| :---------------: | ----------------- | :-----: | ------- |
|     :ok_hand:     | `ok_hand`         |   :v:   | `v`     |
| :crossed_fingers: | `crossed_fingers` | :metal: | `metal` |
|  :call_me_hand:   | `call_me_hand`    |         |         |

### Hand Single Finger

|     icon     | code         |     icon      | code                        |
| :----------: | ------------ | :-----------: | --------------------------- |
| :point_left: | `point_left` | :point_right: | `point_right`               |
| :point_up_2: | `point_up_2` |     :fu:      | `fu` <br /> `middle_finger` |
| :point_down: | `point_down` |  :point_up:   | `point_up`                  |

### Hand Fingers Closed

|    icon     | code                        |     icon     | code                                              |
| :---------: | --------------------------- | :----------: | ------------------------------------------------- |
|    :+1:     | `+1` <br /> `thumbsup`      |     :-1:     | `-1` <br /> `thumbsdown`                          |
|   :fist:    | `fist` <br /> `fist_raised` | :facepunch:  | `facepunch` <br /> `fist_oncoming` <br /> `punch` |
| :fist_left: | `fist_left`                 | :fist_right: | `fist_right`                                      |

### Hands

|     icon     | code         |      icon      | code           |
| :----------: | ------------ | :------------: | -------------- |
|    :clap:    | `clap`       | :raised_hands: | `raised_hands` |
| :open_hands: | `open_hands` |  :handshake:   | `handshake`    |
|    :pray:    | `pray`       |                |                |

### Hand Prop

|      icon      | code           |    icon     | code        |
| :------------: | -------------- | :---------: | ----------- |
| :writing_hand: | `writing_hand` | :nail_care: | `nail_care` |
|    :selfie:    | `selfie`       |             |             |

### Body Parts

|   icon   | code     |   icon   | code     |
| :------: | -------- | :------: | -------- |
| :muscle: | `muscle` |  :ear:   | `ear`    |
|  :nose:  | `nose`   |  :eyes:  | `eyes`   |
|  :eye:   | `eye`    | :tongue: | `tongue` |
|  :lips:  | `lips`   |          |          |

### Person

|      icon      | code           |     icon     | code                                         |
| :------------: | -------------- | :----------: | -------------------------------------------- |
|     :baby:     | `baby`         |    :boy:     | `boy`                                        |
|     :girl:     | `girl`         | :blonde_man: | `blonde_man` <br /> `person_with_blond_hair` |
|     :man:      | `man`          |   :woman:    | `woman`                                      |
| :blonde_woman: | `blonde_woman` | :older_man:  | `older_man`                                  |
| :older_woman:  | `older_woman`  |              |                                              |

### Person Gesture

|            icon            | code                                                                       |        icon         | code                                  |
| :------------------------: | -------------------------------------------------------------------------- | :-----------------: | ------------------------------------- |
|      :frowning_woman:      | `frowning_woman` <br /> `person_frowning`                                  |   :frowning_man:    | `frowning_man`                        |
| :person_with_pouting_face: | `person_with_pouting_face` <br /> `pouting_woman`                          |    :pouting_man:    | `pouting_man`                         |
|         :ng_woman:         | `ng_woman` <br /> `no_good` <br /> `no_good_woman`                         |      :ng_man:       | `ng_man` <br /> `no_good_man`         |
|         :ok_woman:         | `ok_woman`                                                                 |      :ok_man:       | `ok_man`                              |
| :information_desk_person:  | `information_desk_person` <br /> `sassy_woman` <br /> `tipping_hand_woman` |     :sassy_man:     | `sassy_man` <br /> `tipping_hand_man` |
|       :raising_hand:       | `raising_hand` <br /> `raising_hand_woman`                                 | :raising_hand_man:  | `raising_hand_man`                    |
|           :bow:            | `bow` <br /> `bowing_man`                                                  |   :bowing_woman:    | `bowing_woman`                        |
|     :man_facepalming:      | `man_facepalming`                                                          | :woman_facepalming: | `woman_facepalming`                   |
|      :man_shrugging:       | `man_shrugging`                                                            |  :woman_shrugging:  | `woman_shrugging`                     |

### Person Role

|         icon          | code                                                   |            icon             | code                        |
| :-------------------: | ------------------------------------------------------ | :-------------------------: | --------------------------- |
|  :man_health_worker:  | `man_health_worker`                                    |    :woman_health_worker:    | `woman_health_worker`       |
|     :man_student:     | `man_student`                                          |       :woman_student:       | `woman_student`             |
|     :man_teacher:     | `man_teacher`                                          |       :woman_teacher:       | `woman_teacher`             |
|      :man_judge:      | `man_judge`                                            |        :woman_judge:        | `woman_judge`               |
|     :man_farmer:      | `man_farmer`                                           |       :woman_farmer:        | `woman_farmer`              |
|      :man_cook:       | `man_cook`                                             |        :woman_cook:         | `woman_cook`                |
|    :man_mechanic:     | `man_mechanic`                                         |      :woman_mechanic:       | `woman_mechanic`            |
| :man_factory_worker:  | `man_factory_worker`                                   |   :woman_factory_worker:    | `woman_factory_worker`      |
|  :man_office_worker:  | `man_office_worker`                                    |    :woman_office_worker:    | `woman_office_worker`       |
|    :man_scientist:    | `man_scientist`                                        |      :woman_scientist:      | `woman_scientist`           |
|  :man_technologist:   | `man_technologist`                                     |    :woman_technologist:     | `woman_technologist`        |
|     :man_singer:      | `man_singer`                                           |       :woman_singer:        | `woman_singer`              |
|     :man_artist:      | `man_artist`                                           |       :woman_artist:        | `woman_artist`              |
|      :man_pilot:      | `man_pilot`                                            |        :woman_pilot:        | `woman_pilot`               |
|    :man_astronaut:    | `man_astronaut`                                        |      :woman_astronaut:      | `woman_astronaut`           |
|   :man_firefighter:   | `man_firefighter`                                      |     :woman_firefighter:     | `woman_firefighter`         |
|         :cop:         | `cop` <br /> `policeman`                               |        :policewoman:        | `policewoman`               |
|      :detective:      | `detective` <br /> `male_detective`                    |     :female_detective:      | `female_detective`          |
|      :guardsman:      | `guardsman`                                            |        :guardswoman:        | `guardswoman`               |
| :construction_worker: | `construction_worker` <br /> `construction_worker_man` | :construction_worker_woman: | `construction_worker_woman` |
|       :prince:        | `prince`                                               |         :princess:          | `princess`                  |
|   :man_with_turban:   | `man_with_turban`                                      |     :woman_with_turban:     | `woman_with_turban`         |
| :man_with_gua_pi_mao: | `man_with_gua_pi_mao`                                  |       :man_in_tuxedo:       | `man_in_tuxedo`             |
|   :bride_with_veil:   | `bride_with_veil`                                      |      :pregnant_woman:       | `pregnant_woman`            |

### Person Fantasy

|    icon     | code        |  icon   | code    |
| :---------: | ----------- | :-----: | ------- |
|   :angel:   | `angel`     | :santa: | `santa` |
| :mrs_claus: | `mrs_claus` |         |         |

### Person Activity

|            icon            | code                                           |      icon       | code                             |
| :------------------------: | ---------------------------------------------- | :-------------: | -------------------------------- |
|         :massage:          | `massage` <br /> `massage_woman`               |  :massage_man:  | `massage_man`                    |
|         :haircut:          | `haircut` <br /> `haircut_woman`               |  :haircut_man:  | `haircut_man`                    |
|         :walking:          | `walking` <br /> `walking_man`                 | :walking_woman: | `walking_woman`                  |
|          :runner:          | `runner` <br /> `running` <br /> `running_man` | :running_woman: | `running_woman`                  |
|          :dancer:          | `dancer`                                       |  :man_dancing:  | `man_dancing`                    |
| :business_suit_levitating: | `business_suit_levitating`                     |    :dancers:    | `dancers` <br /> `dancing_women` |
|       :dancing_men:        | `dancing_men`                                  |                 |                                  |

### Person Sport

|           icon           | code                                              |            icon            | code                       |
| :----------------------: | ------------------------------------------------- | :------------------------: | -------------------------- |
|     :person_fencing:     | `person_fencing`                                  |       :horse_racing:       | `horse_racing`             |
|         :skier:          | `skier`                                           |       :snowboarder:        | `snowboarder`              |
|      :golfing_man:       | `golfing_man`                                     |      :golfing_woman:       | `golfing_woman`            |
|         :surfer:         | `surfer` <br /> `surfing_man`                     |      :surfing_woman:       | `surfing_woman`            |
|        :rowboat:         | `rowboat` <br /> `rowing_man`                     |       :rowing_woman:       | `rowing_woman`             |
|        :swimmer:         | `swimmer` <br /> `swimming_man`                   |      :swimming_woman:      | `swimming_woman`           |
|     :basketball_man:     | `basketball_man`                                  |     :basketball_woman:     | `basketball_woman`         |
|   :weight_lifting_man:   | `weight_lifting_man`                              |   :weight_lifting_woman:   | `weight_lifting_woman`     |
|       :bicyclist:        | `bicyclist` <br /> `biking_man`                   |       :biking_woman:       | `biking_woman`             |
|   :mountain_bicyclist:   | `mountain_bicyclist` <br /> `mountain_biking_man` |  :mountain_biking_woman:   | `mountain_biking_woman`    |
|    :man_cartwheeling:    | `man_cartwheeling`                                |    :woman_cartwheeling:    | `woman_cartwheeling`       |
|     :men_wrestling:      | `men_wrestling`                                   |     :women_wrestling:      | `women_wrestling`          |
| :man_playing_water_polo: | `man_playing_water_polo`                          | :woman_playing_water_polo: | `woman_playing_water_polo` |
|  :man_playing_handball:  | `man_playing_handball`                            |  :woman_playing_handball:  | `woman_playing_handball`   |
|      :man_juggling:      | `man_juggling`                                    |      :woman_juggling:      | `woman_juggling`           |

### Person Resting

|  icon  | code   |      icon      | code           |
| :----: | ------ | :------------: | -------------- |
| :bath: | `bath` | :sleeping_bed: | `sleeping_bed` |

### Family

|              icon               | code                                                     |              icon              | code                                   |
| :-----------------------------: | -------------------------------------------------------- | :----------------------------: | -------------------------------------- |
|    :two_women_holding_hands:    | `two_women_holding_hands`                                |            :couple:            | `couple`                               |
|     :two_men_holding_hands:     | `two_men_holding_hands`                                  |     :couplekiss_man_woman:     | `couplekiss_man_woman`                 |
|      :couplekiss_man_man:       | `couplekiss_man_man`                                     |    :couplekiss_woman_woman:    | `couplekiss_woman_woman`               |
|       :couple_with_heart:       | `couple_with_heart` <br /> `couple_with_heart_woman_man` |  :couple_with_heart_man_man:   | `couple_with_heart_man_man`            |
| :couple_with_heart_woman_woman: | `couple_with_heart_woman_woman`                          |            :family:            | `family` <br /> `family_man_woman_boy` |
|     :family_man_woman_girl:     | `family_man_woman_girl`                                  |  :family_man_woman_girl_boy:   | `family_man_woman_girl_boy`            |
|   :family_man_woman_boy_boy:    | `family_man_woman_boy_boy`                               |  :family_man_woman_girl_girl:  | `family_man_woman_girl_girl`           |
|      :family_man_man_boy:       | `family_man_man_boy`                                     |     :family_man_man_girl:      | `family_man_man_girl`                  |
|    :family_man_man_girl_boy:    | `family_man_man_girl_boy`                                |    :family_man_man_boy_boy:    | `family_man_man_boy_boy`               |
|   :family_man_man_girl_girl:    | `family_man_man_girl_girl`                               |    :family_woman_woman_boy:    | `family_woman_woman_boy`               |
|    :family_woman_woman_girl:    | `family_woman_woman_girl`                                | :family_woman_woman_girl_boy:  | `family_woman_woman_girl_boy`          |
|  :family_woman_woman_boy_boy:   | `family_woman_woman_boy_boy`                             | :family_woman_woman_girl_girl: | `family_woman_woman_girl_girl`         |
|        :family_man_boy:         | `family_man_boy`                                         |      :family_man_boy_boy:      | `family_man_boy_boy`                   |
|        :family_man_girl:        | `family_man_girl`                                        |     :family_man_girl_boy:      | `family_man_girl_boy`                  |
|     :family_man_girl_girl:      | `family_man_girl_girl`                                   |       :family_woman_boy:       | `family_woman_boy`                     |
|     :family_woman_boy_boy:      | `family_woman_boy_boy`                                   |      :family_woman_girl:       | `family_woman_girl`                    |
|     :family_woman_girl_boy:     | `family_woman_girl_boy`                                  |    :family_woman_girl_girl:    | `family_woman_girl_girl`               |

### Person Symbol

|         icon          | code                  |         icon         | code                 |
| :-------------------: | --------------------- | :------------------: | -------------------- |
|    :speaking_head:    | `speaking_head`       | :bust_in_silhouette: | `bust_in_silhouette` |
| :busts_in_silhouette: | `busts_in_silhouette` |     :footprints:     | `footprints`         |

## Animals & Nature

### Animal Mammal

|      icon       | code                       |       icon        | code              |
| :-------------: | -------------------------- | :---------------: | ----------------- |
|  :monkey_face:  | `monkey_face`              |     :monkey:      | `monkey`          |
|    :gorilla:    | `gorilla`                  |       :dog:       | `dog`             |
|     :dog2:      | `dog2`                     |     :poodle:      | `poodle`          |
|     :wolf:      | `wolf`                     |    :fox_face:     | `fox_face`        |
|      :cat:      | `cat`                      |      :cat2:       | `cat2`            |
|     :lion:      | `lion`                     |      :tiger:      | `tiger`           |
|    :tiger2:     | `tiger2`                   |     :leopard:     | `leopard`         |
|     :horse:     | `horse`                    |    :racehorse:    | `racehorse`       |
|    :unicorn:    | `unicorn`                  |      :deer:       | `deer`            |
|      :cow:      | `cow`                      |       :ox:        | `ox`              |
| :water_buffalo: | `water_buffalo`            |      :cow2:       | `cow2`            |
|      :pig:      | `pig`                      |      :pig2:       | `pig2`            |
|     :boar:      | `boar`                     |    :pig_nose:     | `pig_nose`        |
|      :ram:      | `ram`                      |      :sheep:      | `sheep`           |
|     :goat:      | `goat`                     | :dromedary_camel: | `dromedary_camel` |
|     :camel:     | `camel`                    |    :elephant:     | `elephant`        |
|  :rhinoceros:   | `rhinoceros`               |      :mouse:      | `mouse`           |
|    :mouse2:     | `mouse2`                   |       :rat:       | `rat`             |
|    :hamster:    | `hamster`                  |     :rabbit:      | `rabbit`          |
|    :rabbit2:    | `rabbit2`                  |    :chipmunk:     | `chipmunk`        |
|      :bat:      | `bat`                      |      :bear:       | `bear`            |
|     :koala:     | `koala`                    |   :panda_face:    | `panda_face`      |
|     :feet:      | `feet` <br /> `paw_prints` |                   |                   |

### Animal Bird

|     icon     | code         |       icon       | code             |
| :----------: | ------------ | :--------------: | ---------------- |
|   :turkey:   | `turkey`     |    :chicken:     | `chicken`        |
|  :rooster:   | `rooster`    | :hatching_chick: | `hatching_chick` |
| :baby_chick: | `baby_chick` | :hatched_chick:  | `hatched_chick`  |
|    :bird:    | `bird`       |    :penguin:     | `penguin`        |
|    :dove:    | `dove`       |     :eagle:      | `eagle`          |
|    :duck:    | `duck`       |      :owl:       | `owl`            |

### Animal Amphibian

|  icon  | code   | icon  | code |
| :----: | ------ | :---: | ---- |
| :frog: | `frog` |

### Animal Reptile

|     icon      | code          |   icon   | code     |
| :-----------: | ------------- | :------: | -------- |
|  :crocodile:  | `crocodile`   | :turtle: | `turtle` |
|   :lizard:    | `lizard`      | :snake:  | `snake`  |
| :dragon_face: | `dragon_face` | :dragon: | `dragon` |

### Animal Marine

|      icon       | code                       |    icon    | code       |
| :-------------: | -------------------------- | :--------: | ---------- |
|     :whale:     | `whale`                    |  :whale2:  | `whale2`   |
|    :dolphin:    | `dolphin` <br /> `flipper` |   :fish:   | `fish`     |
| :tropical_fish: | `tropical_fish`            | :blowfish: | `blowfish` |
|     :shark:     | `shark`                    | :octopus:  | `octopus`  |
|     :shell:     | `shell`                    |            |            |

### Animal Bug

|    icon    | code                    |     icon     | code         |
| :--------: | ----------------------- | :----------: | ------------ |
|  :snail:   | `snail`                 | :butterfly:  | `butterfly`  |
|   :bug:    | `bug`                   |    :ant:     | `ant`        |
|   :bee:    | `bee` <br /> `honeybee` |   :beetle:   | `beetle`     |
|  :spider:  | `spider`                | :spider_web: | `spider_web` |
| :scorpion: | `scorpion`              |              |              |

### Plant Flower

|      icon      | code           |       icon       | code             |
| :------------: | -------------- | :--------------: | ---------------- |
|   :bouquet:    | `bouquet`      | :cherry_blossom: | `cherry_blossom` |
| :white_flower: | `white_flower` |    :rosette:     | `rosette`        |
|     :rose:     | `rose`         | :wilted_flower:  | `wilted_flower`  |
|   :hibiscus:   | `hibiscus`     |   :sunflower:    | `sunflower`      |
|   :blossom:    | `blossom`      |     :tulip:      | `tulip`          |

### Plant Other

|        icon        | code               |       icon       | code             |
| :----------------: | ------------------ | :--------------: | ---------------- |
|     :seedling:     | `seedling`         | :evergreen_tree: | `evergreen_tree` |
|  :deciduous_tree:  | `deciduous_tree`   |   :palm_tree:    | `palm_tree`      |
|      :cactus:      | `cactus`           |  :ear_of_rice:   | `ear_of_rice`    |
|       :herb:       | `herb`             |    :shamrock:    | `shamrock`       |
| :four_leaf_clover: | `four_leaf_clover` |   :maple_leaf:   | `maple_leaf`     |
|   :fallen_leaf:    | `fallen_leaf`      |     :leaves:     | `leaves`         |

## Food & Drink

### Food Fruit

|     icon      | code          |     icon     | code                                          |
| :-----------: | ------------- | :----------: | --------------------------------------------- |
|   :grapes:    | `grapes`      |   :melon:    | `melon`                                       |
| :watermelon:  | `watermelon`  |  :mandarin:  | `mandarin` <br /> `orange` <br /> `tangerine` |
|    :lemon:    | `lemon`       |   :banana:   | `banana`                                      |
|  :pineapple:  | `pineapple`   |   :apple:    | `apple`                                       |
| :green_apple: | `green_apple` |    :pear:    | `pear`                                        |
|    :peach:    | `peach`       |  :cherries:  | `cherries`                                    |
| :strawberry:  | `strawberry`  | :kiwi_fruit: | `kiwi_fruit`                                  |
|   :tomato:    | `tomato`      |              |                                               |

### Food Vegetable

|    icon    | code       |     icon     | code         |
| :--------: | ---------- | :----------: | ------------ |
| :avocado:  | `avocado`  |  :eggplant:  | `eggplant`   |
|  :potato:  | `potato`   |   :carrot:   | `carrot`     |
|   :corn:   | `corn`     | :hot_pepper: | `hot_pepper` |
| :cucumber: | `cucumber` |  :mushroom:  | `mushroom`   |
| :peanuts:  | `peanuts`  |  :chestnut:  | `chestnut`   |

### Food Prepared

|        icon         | code                |         icon          | code                  |
| :-----------------: | ------------------- | :-------------------: | --------------------- |
|       :bread:       | `bread`             |      :croissant:      | `croissant`           |
|  :baguette_bread:   | `baguette_bread`    |      :pancakes:       | `pancakes`            |
|      :cheese:       | `cheese`            |    :meat_on_bone:     | `meat_on_bone`        |
|    :poultry_leg:    | `poultry_leg`       |        :bacon:        | `bacon`               |
|     :hamburger:     | `hamburger`         |        :fries:        | `fries`               |
|       :pizza:       | `pizza`             |       :hotdog:        | `hotdog`              |
|       :taco:        | `taco`              |       :burrito:       | `burrito`             |
| :stuffed_flatbread: | `stuffed_flatbread` |         :egg:         | `egg`                 |
|     :fried_egg:     | `fried_egg`         | :shallow_pan_of_food: | `shallow_pan_of_food` |
|       :stew:        | `stew`              |     :green_salad:     | `green_salad`         |
|      :popcorn:      | `popcorn`           |                       |                       |

### Food Asian

|      icon      | code           |      icon      | code           |
| :------------: | -------------- | :------------: | -------------- |
|    :bento:     | `bento`        | :rice_cracker: | `rice_cracker` |
|  :rice_ball:   | `rice_ball`    |     :rice:     | `rice`         |
|    :curry:     | `curry`        |    :ramen:     | `ramen`        |
|  :spaghetti:   | `spaghetti`    | :sweet_potato: | `sweet_potato` |
|     :oden:     | `oden`         |    :sushi:     | `sushi`        |
| :fried_shrimp: | `fried_shrimp` |  :fish_cake:   | `fish_cake`    |
|    :dango:     | `dango`        |                |                |

### Food Marine

|  icon   | code    |   icon   | code     |
| :-----: | ------- | :------: | -------- |
| :crab:  | `crab`  | :shrimp: | `shrimp` |
| :squid: | `squid` |          |          |

### Food Sweet

|    icon     | code        |      icon       | code            |
| :---------: | ----------- | :-------------: | --------------- |
| :icecream:  | `icecream`  |  :shaved_ice:   | `shaved_ice`    |
| :ice_cream: | `ice_cream` |   :doughnut:    | `doughnut`      |
|  :cookie:   | `cookie`    |   :birthday:    | `birthday`      |
|   :cake:    | `cake`      | :chocolate_bar: | `chocolate_bar` |
|   :candy:   | `candy`     |   :lollipop:    | `lollipop`      |
|  :custard:  | `custard`   |   :honey_pot:   | `honey_pot`     |

### Drink

|       icon       | code             |        icon        | code               |
| :--------------: | ---------------- | :----------------: | ------------------ |
|  :baby_bottle:   | `baby_bottle`    |    :milk_glass:    | `milk_glass`       |
|     :coffee:     | `coffee`         |       :tea:        | `tea`              |
|      :sake:      | `sake`           |    :champagne:     | `champagne`        |
|   :wine_glass:   | `wine_glass`     |     :cocktail:     | `cocktail`         |
| :tropical_drink: | `tropical_drink` |       :beer:       | `beer`             |
|     :beers:      | `beers`          | :clinking_glasses: | `clinking_glasses` |
| :tumbler_glass:  | `tumbler_glass`  |                    |                    |

### Dishware

|         icon         | code                 |       icon       | code                   |
| :------------------: | -------------------- | :--------------: | ---------------------- |
| :plate_with_cutlery: | `plate_with_cutlery` | :fork_and_knife: | `fork_and_knife`       |
|       :spoon:        | `spoon`              |     :hocho:      | `hocho` <br /> `knife` |
|      :amphora:       | `amphora`            |                  |                        |

## Travel & Places

### Place Map

|      icon      | code           |          icon          | code                   |
| :------------: | -------------- | :--------------------: | ---------------------- |
| :earth_africa: | `earth_africa` |    :earth_americas:    | `earth_americas`       |
|  :earth_asia:  | `earth_asia`   | :globe_with_meridians: | `globe_with_meridians` |
|  :world_map:   | `world_map`    |        :japan:         | `japan`                |

### Place Geographic

|      icon       | code            |       icon       | code             |
| :-------------: | --------------- | :--------------: | ---------------- |
| :mountain_snow: | `mountain_snow` |    :mountain:    | `mountain`       |
|    :volcano:    | `volcano`       |   :mount_fuji:   | `mount_fuji`     |
|    :camping:    | `camping`       | :beach_umbrella: | `beach_umbrella` |
|    :desert:     | `desert`        | :desert_island:  | `desert_island`  |
| :national_park: | `national_park` |                  |                  |

### Place Building

|          icon           | code                    |          icon          | code                   |
| :---------------------: | ----------------------- | :--------------------: | ---------------------- |
|        :stadium:        | `stadium`               |  :classical_building:  | `classical_building`   |
| :building_construction: | `building_construction` |        :houses:        | `houses`               |
|    :derelict_house:     | `derelict_house`        |        :house:         | `house`                |
|   :house_with_garden:   | `house_with_garden`     |        :office:        | `office`               |
|      :post_office:      | `post_office`           | :european_post_office: | `european_post_office` |
|       :hospital:        | `hospital`              |         :bank:         | `bank`                 |
|         :hotel:         | `hotel`                 |      :love_hotel:      | `love_hotel`           |
|   :convenience_store:   | `convenience_store`     |        :school:        | `school`               |
|   :department_store:    | `department_store`      |       :factory:        | `factory`              |
|    :japanese_castle:    | `japanese_castle`       |   :european_castle:    | `european_castle`      |
|        :wedding:        | `wedding`               |     :tokyo_tower:      | `tokyo_tower`          |
|   :statue_of_liberty:   | `statue_of_liberty`     |                        |                        |

### Place Religious

|    icon     | code        |      icon       | code            |
| :---------: | ----------- | :-------------: | --------------- |
|  :church:   | `church`    |    :mosque:     | `mosque`        |
| :synagogue: | `synagogue` | :shinto_shrine: | `shinto_shrine` |
|   :kaaba:   | `kaaba`     |                 |                 |

### Place Other

|      icon      | code           |           icon           | code                     |
| :------------: | -------------- | :----------------------: | ------------------------ |
|   :fountain:   | `fountain`     |          :tent:          | `tent`                   |
|    :foggy:     | `foggy`        |    :night_with_stars:    | `night_with_stars`       |
|  :cityscape:   | `cityscape`    | :sunrise_over_mountains: | `sunrise_over_mountains` |
|   :sunrise:    | `sunrise`      |      :city_sunset:       | `city_sunset`            |
| :city_sunrise: | `city_sunrise` |    :bridge_at_night:     | `bridge_at_night`        |
|  :hotsprings:  | `hotsprings`   |     :carousel_horse:     | `carousel_horse`         |
| :ferris_wheel: | `ferris_wheel` |     :roller_coaster:     | `roller_coaster`         |
|    :barber:    | `barber`       |      :circus_tent:       | `circus_tent`            |

### Transport Ground

|           icon           | code                     |         icon          | code                  |
| :----------------------: | ------------------------ | :-------------------: | --------------------- |
|    :steam_locomotive:    | `steam_locomotive`       |     :railway_car:     | `railway_car`         |
|    :bullettrain_side:    | `bullettrain_side`       |  :bullettrain_front:  | `bullettrain_front`   |
|         :train2:         | `train2`                 |        :metro:        | `metro`               |
|       :light_rail:       | `light_rail`             |       :station:       | `station`             |
|          :tram:          | `tram`                   |      :monorail:       | `monorail`            |
|    :mountain_railway:    | `mountain_railway`       |        :train:        | `train`               |
|          :bus:           | `bus`                    |    :oncoming_bus:     | `oncoming_bus`        |
|       :trolleybus:       | `trolleybus`             |       :minibus:       | `minibus`             |
|       :ambulance:        | `ambulance`              |     :fire_engine:     | `fire_engine`         |
|       :police_car:       | `police_car`             | :oncoming_police_car: | `oncoming_police_car` |
|          :taxi:          | `taxi`                   |    :oncoming_taxi:    | `oncoming_taxi`       |
|          :car:           | `car` <br /> `red_car`   | :oncoming_automobile: | `oncoming_automobile` |
|        :blue_car:        | `blue_car`               |        :truck:        | `truck`               |
|   :articulated_lorry:    | `articulated_lorry`      |       :tractor:       | `tractor`             |
|       :racing_car:       | `racing_car`             |     :motorcycle:      | `motorcycle`          |
|     :motor_scooter:      | `motor_scooter`          |        :bike:         | `bike`                |
|      :kick_scooter:      | `kick_scooter`           |       :busstop:       | `busstop`             |
|        :motorway:        | `motorway`               |    :railway_track:    | `railway_track`       |
|        :oil_drum:        | `oil_drum`               |      :fuelpump:       | `fuelpump`            |
|     :rotating_light:     | `rotating_light`         |    :traffic_light:    | `traffic_light`       |
| :vertical_traffic_light: | `vertical_traffic_light` |      :stop_sign:      | `stop_sign`           |
|      :construction:      | `construction`           |                       |                       |

### Transport Water

|       icon       | code             |    icon     | code                     |
| :--------------: | ---------------- | :---------: | ------------------------ |
|     :anchor:     | `anchor`         |   :boat:    | `boat` <br /> `sailboat` |
|     :canoe:      | `canoe`          | :speedboat: | `speedboat`              |
| :passenger_ship: | `passenger_ship` |   :ferry:   | `ferry`                  |
|   :motor_boat:   | `motor_boat`     |   :ship:    | `ship`                   |

### Transport Air

|         icon         | code                 |          icon          | code                   |
| :------------------: | -------------------- | :--------------------: | ---------------------- |
|      :airplane:      | `airplane`           |    :small_airplane:    | `small_airplane`       |
|  :flight_departure:  | `flight_departure`   |    :flight_arrival:    | `flight_arrival`       |
|        :seat:        | `seat`               |      :helicopter:      | `helicopter`           |
| :suspension_railway: | `suspension_railway` |  :mountain_cableway:   | `mountain_cableway`    |
|   :aerial_tramway:   | `aerial_tramway`     | :artificial_satellite: | `artificial_satellite` |
|       :rocket:       | `rocket`             |                        |                        |

### Hotel

|      icon      | code           | icon  | code |
| :------------: | -------------- | :---: | ---- |
| :bellhop_bell: | `bellhop_bell` |

### Time

|        icon         | code                |           icon           | code                     |
| :-----------------: | ------------------- | :----------------------: | ------------------------ |
|     :hourglass:     | `hourglass`         | :hourglass_flowing_sand: | `hourglass_flowing_sand` |
|       :watch:       | `watch`             |      :alarm_clock:       | `alarm_clock`            |
|     :stopwatch:     | `stopwatch`         |      :timer_clock:       | `timer_clock`            |
| :mantelpiece_clock: | `mantelpiece_clock` |        :clock12:         | `clock12`                |
|     :clock1230:     | `clock1230`         |         :clock1:         | `clock1`                 |
|     :clock130:      | `clock130`          |         :clock2:         | `clock2`                 |
|     :clock230:      | `clock230`          |         :clock3:         | `clock3`                 |
|     :clock330:      | `clock330`          |         :clock4:         | `clock4`                 |
|     :clock430:      | `clock430`          |         :clock5:         | `clock5`                 |
|     :clock530:      | `clock530`          |         :clock6:         | `clock6`                 |
|     :clock630:      | `clock630`          |         :clock7:         | `clock7`                 |
|     :clock730:      | `clock730`          |         :clock8:         | `clock8`                 |
|     :clock830:      | `clock830`          |         :clock9:         | `clock9`                 |
|     :clock930:      | `clock930`          |        :clock10:         | `clock10`                |
|     :clock1030:     | `clock1030`         |        :clock11:         | `clock11`                |
|     :clock1130:     | `clock1130`         |                          |                          |

### Sky & Weather

|              icon               | code                            |             icon              | code                                |
| :-----------------------------: | ------------------------------- | :---------------------------: | ----------------------------------- |
|           :new_moon:            | `new_moon`                      |    :waxing_crescent_moon:     | `waxing_crescent_moon`              |
|      :first_quarter_moon:       | `first_quarter_moon`            |            :moon:             | `moon` <br /> `waxing_gibbous_moon` |
|           :full_moon:           | `full_moon`                     |     :waning_gibbous_moon:     | `waning_gibbous_moon`               |
|       :last_quarter_moon:       | `last_quarter_moon`             |    :waning_crescent_moon:     | `waning_crescent_moon`              |
|         :crescent_moon:         | `crescent_moon`                 |     :new_moon_with_face:      | `new_moon_with_face`                |
| :first_quarter_moon_with_face:  | `first_quarter_moon_with_face`  | :last_quarter_moon_with_face: | `last_quarter_moon_with_face`       |
|          :thermometer:          | `thermometer`                   |            :sunny:            | `sunny`                             |
|      :full_moon_with_face:      | `full_moon_with_face`           |        :sun_with_face:        | `sun_with_face`                     |
|             :star:              | `star`                          |            :star2:            | `star2`                             |
|             :stars:             | `stars`                         |          :milky_way:          | `milky_way`                         |
|             :cloud:             | `cloud`                         |        :partly_sunny:         | `partly_sunny`                      |
| :cloud_with_lightning_and_rain: | `cloud_with_lightning_and_rain` |   :sun_behind_small_cloud:    | `sun_behind_small_cloud`            |
|    :sun_behind_large_cloud:     | `sun_behind_large_cloud`        |    :sun_behind_rain_cloud:    | `sun_behind_rain_cloud`             |
|        :cloud_with_rain:        | `cloud_with_rain`               |       :cloud_with_snow:       | `cloud_with_snow`                   |
|     :cloud_with_lightning:      | `cloud_with_lightning`          |           :tornado:           | `tornado`                           |
|              :fog:              | `fog`                           |          :wind_face:          | `wind_face`                         |
|            :cyclone:            | `cyclone`                       |           :rainbow:           | `rainbow`                           |
|        :closed_umbrella:        | `closed_umbrella`               |        :open_umbrella:        | `open_umbrella`                     |
|           :umbrella:            | `umbrella`                      |      :parasol_on_ground:      | `parasol_on_ground`                 |
|              :zap:              | `zap`                           |          :snowflake:          | `snowflake`                         |
|       :snowman_with_snow:       | `snowman_with_snow`             |           :snowman:           | `snowman`                           |
|             :comet:             | `comet`                         |            :fire:             | `fire`                              |
|            :droplet:            | `droplet`                       |            :ocean:            | `ocean`                             |

## Activities

### Event

|       icon        | code              |       icon       | code             |
| :---------------: | ----------------- | :--------------: | ---------------- |
| :jack_o_lantern:  | `jack_o_lantern`  | :christmas_tree: | `christmas_tree` |
|    :fireworks:    | `fireworks`       |    :sparkler:    | `sparkler`       |
|    :sparkles:     | `sparkles`        |    :balloon:     | `balloon`        |
|      :tada:       | `tada`            | :confetti_ball:  | `confetti_ball`  |
|  :tanabata_tree:  | `tanabata_tree`   |     :bamboo:     | `bamboo`         |
|      :dolls:      | `dolls`           |     :flags:      | `flags`          |
|   :wind_chime:    | `wind_chime`      |   :rice_scene:   | `rice_scene`     |
|     :ribbon:      | `ribbon`          |      :gift:      | `gift`           |
| :reminder_ribbon: | `reminder_ribbon` |    :tickets:     | `tickets`        |
|     :ticket:      | `ticket`          |                  |                  |

### Award Medal

|       icon        | code              |       icon        | code              |
| :---------------: | ----------------- | :---------------: | ----------------- |
| :medal_military:  | `medal_military`  |     :trophy:      | `trophy`          |
|  :medal_sports:   | `medal_sports`    | :1st_place_medal: | `1st_place_medal` |
| :2nd_place_medal: | `2nd_place_medal` | :3rd_place_medal: | `3rd_place_medal` |

### Sport

|          icon           | code                    |           icon            | code                      |
| :---------------------: | ----------------------- | :-----------------------: | ------------------------- |
|        :soccer:         | `soccer`                |        :baseball:         | `baseball`                |
|      :basketball:       | `basketball`            |       :volleyball:        | `volleyball`              |
|       :football:        | `football`              |     :rugby_football:      | `rugby_football`          |
|        :tennis:         | `tennis`                |         :bowling:         | `bowling`                 |
|        :cricket:        | `cricket`               |      :field_hockey:       | `field_hockey`            |
|      :ice_hockey:       | `ice_hockey`            |        :ping_pong:        | `ping_pong`               |
|       :badminton:       | `badminton`             |      :boxing_glove:       | `boxing_glove`            |
| :martial_arts_uniform:  | `martial_arts_uniform`  |        :goal_net:         | `goal_net`                |
|         :golf:          | `golf`                  |        :ice_skate:        | `ice_skate`               |
| :fishing_pole_and_fish: | `fishing_pole_and_fish` | :running_shirt_with_sash: | `running_shirt_with_sash` |
|          :ski:          | `ski`                   |                           |                           |

### Game

|      icon      | code           |          icon          | code                   |
| :------------: | -------------- | :--------------------: | ---------------------- |
|     :dart:     | `dart`         |        :8ball:         | `8ball`                |
| :crystal_ball: | `crystal_ball` |      :video_game:      | `video_game`           |
|   :joystick:   | `joystick`     |     :slot_machine:     | `slot_machine`         |
|   :game_die:   | `game_die`     |        :spades:        | `spades`               |
|    :hearts:    | `hearts`       |       :diamonds:       | `diamonds`             |
|    :clubs:     | `clubs`        |     :black_joker:      | `black_joker`          |
|   :mahjong:    | `mahjong`      | :flower_playing_cards: | `flower_playing_cards` |

### Arts & Crafts

|       icon        | code              |       icon       | code             |
| :---------------: | ----------------- | :--------------: | ---------------- |
| :performing_arts: | `performing_arts` | :framed_picture: | `framed_picture` |
|       :art:       | `art`             |                  |                  |

## Objects

### Clothing

|       icon       | code                      |          icon          | code                    |
| :--------------: | ------------------------- | :--------------------: | ----------------------- |
|   :eyeglasses:   | `eyeglasses`              |   :dark_sunglasses:    | `dark_sunglasses`       |
|    :necktie:     | `necktie`                 |        :shirt:         | `shirt` <br /> `tshirt` |
|     :jeans:      | `jeans`                   |        :dress:         | `dress`                 |
|     :kimono:     | `kimono`                  |        :bikini:        | `bikini`                |
| :womans_clothes: | `womans_clothes`          |        :purse:         | `purse`                 |
|    :handbag:     | `handbag`                 |        :pouch:         | `pouch`                 |
|    :shopping:    | `shopping`                |    :school_satchel:    | `school_satchel`        |
|   :mans_shoe:    | `mans_shoe` <br /> `shoe` |    :athletic_shoe:     | `athletic_shoe`         |
|   :high_heel:    | `high_heel`               |        :sandal:        | `sandal`                |
|      :boot:      | `boot`                    |        :crown:         | `crown`                 |
|   :womans_hat:   | `womans_hat`              |        :tophat:        | `tophat`                |
|  :mortar_board:  | `mortar_board`            | :rescue_worker_helmet: | `rescue_worker_helmet`  |
|  :prayer_beads:  | `prayer_beads`            |       :lipstick:       | `lipstick`              |
|      :ring:      | `ring`                    |         :gem:          | `gem`                   |

### Sound

|     icon      | code          |     icon     | code         |
| :-----------: | ------------- | :----------: | ------------ |
|    :mute:     | `mute`        |  :speaker:   | `speaker`    |
|    :sound:    | `sound`       | :loud_sound: | `loud_sound` |
| :loudspeaker: | `loudspeaker` |    :mega:    | `mega`       |
| :postal_horn: | `postal_horn` |    :bell:    | `bell`       |
|   :no_bell:   | `no_bell`     |              |              |

### Music

|      icon       | code            |        icon         | code                |
| :-------------: | --------------- | :-----------------: | ------------------- |
| :musical_score: | `musical_score` |   :musical_note:    | `musical_note`      |
|     :notes:     | `notes`         | :studio_microphone: | `studio_microphone` |
| :level_slider:  | `level_slider`  |   :control_knobs:   | `control_knobs`     |
|  :microphone:   | `microphone`    |    :headphones:     | `headphones`        |
|     :radio:     | `radio`         |                     |                     |

### Musical Instrument

|        icon        | code               |   icon    | code      |
| :----------------: | ------------------ | :-------: | --------- |
|    :saxophone:     | `saxophone`        | :guitar:  | `guitar`  |
| :musical_keyboard: | `musical_keyboard` | :trumpet: | `trumpet` |
|      :violin:      | `violin`           |  :drum:   | `drum`    |

### Phone

|   icon   | code                       |         icon         | code                 |
| :------: | -------------------------- | :------------------: | -------------------- |
| :iphone: | `iphone`                   |      :calling:       | `calling`            |
| :phone:  | `phone` <br /> `telephone` | :telephone_receiver: | `telephone_receiver` |
| :pager:  | `pager`                    |        :fax:         | `fax`                |

### Computer

|       icon       | code             |        icon        | code               |
| :--------------: | ---------------- | :----------------: | ------------------ |
|    :battery:     | `battery`        |  :electric_plug:   | `electric_plug`    |
|    :computer:    | `computer`       | :desktop_computer: | `desktop_computer` |
|    :printer:     | `printer`        |     :keyboard:     | `keyboard`         |
| :computer_mouse: | `computer_mouse` |    :trackball:     | `trackball`        |
|    :minidisc:    | `minidisc`       |   :floppy_disk:    | `floppy_disk`      |
|       :cd:       | `cd`             |       :dvd:        | `dvd`              |

### Light & Video

|       icon        | code                               |      icon      | code           |
| :---------------: | ---------------------------------- | :------------: | -------------- |
|  :movie_camera:   | `movie_camera`                     |  :film_strip:  | `film_strip`   |
| :film_projector:  | `film_projector`                   |   :clapper:    | `clapper`      |
|       :tv:        | `tv`                               |    :camera:    | `camera`       |
|  :camera_flash:   | `camera_flash`                     | :video_camera: | `video_camera` |
|       :vhs:       | `vhs`                              |     :mag:      | `mag`          |
|    :mag_right:    | `mag_right`                        |    :candle:    | `candle`       |
|      :bulb:       | `bulb`                             |  :flashlight:  | `flashlight`   |
| :izakaya_lantern: | `izakaya_lantern` <br /> `lantern` |                |                |

### Book Paper

|               icon               | code                             |       icon       | code             |
| :------------------------------: | -------------------------------- | :--------------: | ---------------- |
| :notebook_with_decorative_cover: | `notebook_with_decorative_cover` |  :closed_book:   | `closed_book`    |
|              :book:              | `book` <br /> `open_book`        |   :green_book:   | `green_book`     |
|           :blue_book:            | `blue_book`                      |  :orange_book:   | `orange_book`    |
|             :books:              | `books`                          |    :notebook:    | `notebook`       |
|             :ledger:             | `ledger`                         | :page_with_curl: | `page_with_curl` |
|             :scroll:             | `scroll`                         | :page_facing_up: | `page_facing_up` |
|           :newspaper:            | `newspaper`                      | :newspaper_roll: | `newspaper_roll` |
|         :bookmark_tabs:          | `bookmark_tabs`                  |    :bookmark:    | `bookmark`       |
|             :label:              | `label`                          |                  |                  |

### Money

|     icon      | code          |        icon        | code               |
| :-----------: | ------------- | :----------------: | ------------------ |
|  :moneybag:   | `moneybag`    |       :yen:        | `yen`              |
|   :dollar:    | `dollar`      |       :euro:       | `euro`             |
|    :pound:    | `pound`       | :money_with_wings: | `money_with_wings` |
| :credit_card: | `credit_card` |      :chart:       | `chart`            |

### Mail

|          icon          | code                      |         icon          | code                  |
| :--------------------: | ------------------------- | :-------------------: | --------------------- |
|        :email:         | `email` <br /> `envelope` |       :e-mail:        | `:e-mail:`            |
|  :incoming_envelope:   | `incoming_envelope`       | :envelope_with_arrow: | `envelope_with_arrow` |
|     :outbox_tray:      | `outbox_tray`             |     :inbox_tray:      | `inbox_tray`          |
|       :package:        | `package`                 |       :mailbox:       | `mailbox`             |
|    :mailbox_closed:    | `mailbox_closed`          |  :mailbox_with_mail:  | `mailbox_with_mail`   |
| :mailbox_with_no_mail: | `mailbox_with_no_mail`    |       :postbox:       | `postbox`             |
|      :ballot_box:      | `ballot_box`              |                       |                       |

### Writing

|      icon      | code                   |    icon     | code        |
| :------------: | ---------------------- | :---------: | ----------- |
|   :pencil2:    | `pencil2`              | :black_nib: | `black_nib` |
| :fountain_pen: | `fountain_pen`         |    :pen:    | `pen`       |
|  :paintbrush:  | `paintbrush`           |  :crayon:   | `crayon`    |
|     :memo:     | `memo` <br /> `pencil` |             |             |

### Office

|             icon             | code                         |            icon            | code                       |
| :--------------------------: | ---------------------------- | :------------------------: | -------------------------- |
|         :briefcase:          | `briefcase`                  |       :file_folder:        | `file_folder`              |
|      :open_file_folder:      | `open_file_folder`           |   :card_index_dividers:    | `card_index_dividers`      |
|            :date:            | `date`                       |         :calendar:         | `calendar`                 |
|       :spiral_notepad:       | `spiral_notepad`             |     :spiral_calendar:      | `spiral_calendar`          |
|         :card_index:         | `card_index`                 | :chart_with_upwards_trend: | `chart_with_upwards_trend` |
| :chart_with_downwards_trend: | `chart_with_downwards_trend` |        :bar_chart:         | `bar_chart`                |
|         :clipboard:          | `clipboard`                  |         :pushpin:          | `pushpin`                  |
|       :round_pushpin:        | `round_pushpin`              |        :paperclip:         | `paperclip`                |
|         :paperclips:         | `paperclips`                 |      :straight_ruler:      | `straight_ruler`           |
|      :triangular_ruler:      | `triangular_ruler`           |         :scissors:         | `scissors`                 |
|       :card_file_box:        | `card_file_box`              |       :file_cabinet:       | `file_cabinet`             |
|        :wastebasket:         | `wastebasket`                |                            |                            |

### Lock

|        icon         | code                |          icon          | code                   |
| :-----------------: | ------------------- | :--------------------: | ---------------------- |
|       :lock:        | `lock`              |        :unlock:        | `unlock`               |
| :lock_with_ink_pen: | `lock_with_ink_pen` | :closed_lock_with_key: | `closed_lock_with_key` |
|        :key:        | `key`               |       :old_key:        | `old_key`              |

### Tool

|       icon        | code              |        icon         | code                |
| :---------------: | ----------------- | :-----------------: | ------------------- |
|     :hammer:      | `hammer`          |       :pick:        | `pick`              |
| :hammer_and_pick: | `hammer_and_pick` | :hammer_and_wrench: | `hammer_and_wrench` |
|     :dagger:      | `dagger`          |  :crossed_swords:   | `crossed_swords`    |
|       :gun:       | `gun`             |   :bow_and_arrow:   | `bow_and_arrow`     |
|     :shield:      | `shield`          |      :wrench:       | `wrench`            |
|  :nut_and_bolt:   | `nut_and_bolt`    |       :gear:        | `gear`              |
|      :clamp:      | `clamp`           |   :balance_scale:   | `balance_scale`     |
|      :link:       | `link`            |      :chains:       | `chains`            |

### Science

|    icon     | code        |     icon     | code         |
| :---------: | ----------- | :----------: | ------------ |
|  :alembic:  | `alembic`   | :microscope: | `microscope` |
| :telescope: | `telescope` | :satellite:  | `satellite`  |

### Medical

|   icon    | code      |  icon  | code   |
| :-------: | --------- | :----: | ------ |
| :syringe: | `syringe` | :pill: | `pill` |

### Household

|       icon       | code             |   icon    | code      |
| :--------------: | ---------------- | :-------: | --------- |
|      :door:      | `door`           |   :bed:   | `bed`     |
| :couch_and_lamp: | `couch_and_lamp` | :toilet:  | `toilet`  |
|     :shower:     | `shower`         | :bathtub: | `bathtub` |
| :shopping_cart:  | `shopping_cart`  |           |           |

### Other Object

|     icon      | code          |   icon   | code     |
| :-----------: | ------------- | :------: | -------- |
|   :smoking:   | `smoking`     | :coffin: | `coffin` |
| :funeral_urn: | `funeral_urn` | :moyai:  | `moyai`  |

## Symbols

### Transport Sign

|      icon       | code            |           icon            | code                      |
| :-------------: | --------------- | :-----------------------: | ------------------------- |
|      :atm:      | `atm`           | :put_litter_in_its_place: | `put_litter_in_its_place` |
| :potable_water: | `potable_water` |       :wheelchair:        | `wheelchair`              |
|     :mens:      | `mens`          |         :womens:          | `womens`                  |
|   :restroom:    | `restroom`      |       :baby_symbol:       | `baby_symbol`             |
|      :wc:       | `wc`            |    :passport_control:     | `passport_control`        |
|    :customs:    | `customs`       |      :baggage_claim:      | `baggage_claim`           |
| :left_luggage:  | `left_luggage`  |                           |                           |

### Warning

|       icon       | code             |        icon         | code                  |
| :--------------: | ---------------- | :-----------------: | --------------------- |
|    :warning:     | `warning`        | :children_crossing: | `children_crossing`   |
|    :no_entry:    | `no_entry`       |   :no_entry_sign:   | `no_entry_sign`       |
|  :no_bicycles:   | `no_bicycles`    |    :no_smoking:     | `no_smoking`          |
| :do_not_litter:  | `do_not_litter`  | :non-potable_water: | `:non-potable_water:` |
| :no_pedestrians: | `no_pedestrians` | :no_mobile_phones:  | `no_mobile_phones`    |
|    :underage:    | `underage`       |    :radioactive:    | `radioactive`         |
|   :biohazard:    | `biohazard`      |                     |                       |

### Arrow

|            icon             | code                        |           icon            | code                      |
| :-------------------------: | --------------------------- | :-----------------------: | ------------------------- |
|         :arrow_up:          | `arrow_up`                  |    :arrow_upper_right:    | `arrow_upper_right`       |
|        :arrow_right:        | `arrow_right`               |    :arrow_lower_right:    | `arrow_lower_right`       |
|        :arrow_down:         | `arrow_down`                |    :arrow_lower_left:     | `arrow_lower_left`        |
|        :arrow_left:         | `arrow_left`                |    :arrow_upper_left:     | `arrow_upper_left`        |
|       :arrow_up_down:       | `arrow_up_down`             |    :left_right_arrow:     | `left_right_arrow`        |
| :leftwards_arrow_with_hook: | `leftwards_arrow_with_hook` |    :arrow_right_hook:     | `arrow_right_hook`        |
|     :arrow_heading_up:      | `arrow_heading_up`          |   :arrow_heading_down:    | `arrow_heading_down`      |
|     :arrows_clockwise:      | `arrows_clockwise`          | :arrows_counterclockwise: | `arrows_counterclockwise` |
|           :back:            | `back`                      |           :end:           | `end`                     |
|            :on:             | `on`                        |          :soon:           | `soon`                    |
|            :top:            | `top`                       |                           |                           |

### Religion

|        icon         | code                |        icon        | code               |
| :-----------------: | ------------------- | :----------------: | ------------------ |
| :place_of_worship:  | `place_of_worship`  |   :atom_symbol:    | `atom_symbol`      |
|        :om:         | `om`                |  :star_of_david:   | `star_of_david`    |
|  :wheel_of_dharma:  | `wheel_of_dharma`   |     :yin_yang:     | `yin_yang`         |
|    :latin_cross:    | `latin_cross`       |  :orthodox_cross:  | `orthodox_cross`   |
| :star_and_crescent: | `star_and_crescent` |   :peace_symbol:   | `peace_symbol`     |
|      :menorah:      | `menorah`           | :six_pointed_star: | `six_pointed_star` |

### Zodiac

|     icon      | code          |    icon     | code        |
| :-----------: | ------------- | :---------: | ----------- |
|    :aries:    | `aries`       |  :taurus:   | `taurus`    |
|   :gemini:    | `gemini`      |  :cancer:   | `cancer`    |
|     :leo:     | `leo`         |   :virgo:   | `virgo`     |
|    :libra:    | `libra`       | :scorpius:  | `scorpius`  |
| :sagittarius: | `sagittarius` | :capricorn: | `capricorn` |
|  :aquarius:   | `aquarius`    |  :pisces:   | `pisces`    |
|  :ophiuchus:  | `ophiuchus`   |             |             |

### Av Symbol

|            icon             | code                        |          icon           | code                    |
| :-------------------------: | --------------------------- | :---------------------: | ----------------------- |
| :twisted_rightwards_arrows: | `twisted_rightwards_arrows` |        :repeat:         | `repeat`                |
|        :repeat_one:         | `repeat_one`                |     :arrow_forward:     | `arrow_forward`         |
|       :fast_forward:        | `fast_forward`              |   :next_track_button:   | `next_track_button`     |
|   :play_or_pause_button:    | `play_or_pause_button`      |    :arrow_backward:     | `arrow_backward`        |
|          :rewind:           | `rewind`                    | :previous_track_button: | `previous_track_button` |
|      :arrow_up_small:       | `arrow_up_small`            |    :arrow_double_up:    | `arrow_double_up`       |
|     :arrow_down_small:      | `arrow_down_small`          |   :arrow_double_down:   | `arrow_double_down`     |
|       :pause_button:        | `pause_button`              |      :stop_button:      | `stop_button`           |
|       :record_button:       | `record_button`             |        :cinema:         | `cinema`                |
|      :low_brightness:       | `low_brightness`            |    :high_brightness:    | `high_brightness`       |
|      :signal_strength:      | `signal_strength`           |    :vibration_mode:     | `vibration_mode`        |
|     :mobile_phone_off:      | `mobile_phone_off`          |                         |                         |

### Math

|           icon           | code                     |         icon          | code                  |
| :----------------------: | ------------------------ | :-------------------: | --------------------- |
| :heavy_multiplication_x: | `heavy_multiplication_x` |   :heavy_plus_sign:   | `heavy_plus_sign`     |
|    :heavy_minus_sign:    | `heavy_minus_sign`       | :heavy_division_sign: | `heavy_division_sign` |

### Punctuation

|        icon        | code               |      icon       | code                                          |
| :----------------: | ------------------ | :-------------: | --------------------------------------------- |
|     :bangbang:     | `bangbang`         |  :interrobang:  | `interrobang`                                 |
|     :question:     | `question`         | :grey_question: | `grey_question`                               |
| :grey_exclamation: | `grey_exclamation` |  :exclamation:  | `exclamation` <br /> `heavy_exclamation_mark` |
|    :wavy_dash:     | `wavy_dash`        |                 |                                               |

### Currency

|        icon         | code                |        icon         | code                |
| :-----------------: | ------------------- | :-----------------: | ------------------- |
| :currency_exchange: | `currency_exchange` | :heavy_dollar_sign: | `heavy_dollar_sign` |

### Keycap

|     icon     | code         |    icon    | code       |
| :----------: | ------------ | :--------: | ---------- |
|    :hash:    | `hash`       | :asterisk: | `asterisk` |
|    :zero:    | `zero`       |   :one:    | `one`      |
|    :two:     | `two`        |  :three:   | `three`    |
|    :four:    | `four`       |   :five:   | `five`     |
|    :six:     | `six`        |  :seven:   | `seven`    |
|   :eight:    | `eight`      |   :nine:   | `nine`     |
| :keycap_ten: | `keycap_ten` |            |            |

### Alphabet

|      icon      | code           |         icon          | code                  |
| :------------: | -------------- | :-------------------: | --------------------- |
| :capital_abcd: | `capital_abcd` |        :abcd:         | `abcd`                |
|     :1234:     | `1234`         |       :symbols:       | `symbols`             |
|     :abc:      | `abc`          |          :a:          | `a`                   |
|      :ab:      | `ab`           |          :b:          | `b`                   |
|      :cl:      | `cl`           |        :cool:         | `cool`                |
|     :free:     | `free`         | :information_source:  | `information_source`  |
|      :id:      | `id`           |          :m:          | `m`                   |
|     :new:      | `new`          |         :ng:          | `ng`                  |
|      :o2:      | `o2`           |         :ok:          | `ok`                  |
|   :parking:    | `parking`      |         :sos:         | `sos`                 |
|      :up:      | `up`           |         :vs:          | `vs`                  |
|     :koko:     | `koko`         |         :sa:          | `sa`                  |
|    :u6708:     | `u6708`        |        :u6709:        | `u6709`               |
|    :u6307:     | `u6307`        | :ideograph_advantage: | `ideograph_advantage` |
|    :u5272:     | `u5272`        |        :u7121:        | `u7121`               |
|    :u7981:     | `u7981`        |       :accept:        | `accept`              |
|    :u7533:     | `u7533`        |        :u5408:        | `u5408`               |
|    :u7a7a:     | `u7a7a`        |   :congratulations:   | `congratulations`     |
|    :secret:    | `secret`       |        :u55b6:        | `u55b6`               |
|    :u6e80:     | `u6e80`        |                       |                       |

### Geometric

|               icon                | code                              |            icon             | code                        |
| :-------------------------------: | --------------------------------- | :-------------------------: | --------------------------- |
|           :red_circle:            | `red_circle`                      |     :large_blue_circle:     | `large_blue_circle`         |
|          :black_circle:           | `black_circle`                    |       :white_circle:        | `white_circle`              |
|       :black_large_square:        | `black_large_square`              |    :white_large_square:     | `white_large_square`        |
|       :black_medium_square:       | `black_medium_square`             |    :white_medium_square:    | `white_medium_square`       |
|    :black_medium_small_square:    | `black_medium_small_square`       | :white_medium_small_square: | `white_medium_small_square` |
|       :black_small_square:        | `black_small_square`              |    :white_small_square:     | `white_small_square`        |
|      :large_orange_diamond:       | `large_orange_diamond`            |    :large_blue_diamond:     | `large_blue_diamond`        |
|      :small_orange_diamond:       | `small_orange_diamond`            |    :small_blue_diamond:     | `small_blue_diamond`        |
|       :small_red_triangle:        | `small_red_triangle`              |  :small_red_triangle_down:  | `small_red_triangle_down`   |
| :diamond_shape_with_a_dot_inside: | `diamond_shape_with_a_dot_inside` |       :radio_button:        | `radio_button`              |
|       :white_square_button:       | `white_square_button`             |    :black_square_button:    | `black_square_button`       |

### Other Symbol

|             icon              | code                          |            icon            | code                       |
| :---------------------------: | ----------------------------- | :------------------------: | -------------------------- |
|           :recycle:           | `recycle`                     |       :fleur_de_lis:       | `fleur_de_lis`             |
|           :trident:           | `trident`                     |        :name_badge:        | `name_badge`               |
|          :beginner:           | `beginner`                    |            :o:             | `o`                        |
|      :white_check_mark:       | `white_check_mark`            |  :ballot_box_with_check:   | `ballot_box_with_check`    |
|      :heavy_check_mark:       | `heavy_check_mark`            |            :x:             | `x`                        |
| :negative_squared_cross_mark: | `negative_squared_cross_mark` |        :curly_loop:        | `curly_loop`               |
|            :loop:             | `loop`                        |  :part_alternation_mark:   | `part_alternation_mark`    |
|    :eight_spoked_asterisk:    | `eight_spoked_asterisk`       | :eight_pointed_black_star: | `eight_pointed_black_star` |
|           :sparkle:           | `sparkle`                     |        :copyright:         | `copyright`                |
|         :registered:          | `registered`                  |            :tm:            | `tm`                       |

## Flags

### Common Flags

|       icon       | code             |           icon            | code                      |
| :--------------: | ---------------- | :-----------------------: | ------------------------- |
| :checkered_flag: | `checkered_flag` | :triangular_flag_on_post: | `triangular_flag_on_post` |
| :crossed_flags:  | `crossed_flags`  |       :black_flag:        | `black_flag`              |
|   :white_flag:   | `white_flag`     |      :rainbow_flag:       | `rainbow_flag`            |

### Country and Region Flags

|         icon         | code                         |                  icon                  | code                                   |
| :------------------: | ---------------------------- | :------------------------------------: | -------------------------------------- |
|      :andorra:       | `andorra`                    |         :united_arab_emirates:         | `united_arab_emirates`                 |
|    :afghanistan:     | `afghanistan`                |           :antigua_barbuda:            | `antigua_barbuda`                      |
|      :anguilla:      | `anguilla`                   |               :albania:                | `albania`                              |
|      :armenia:       | `armenia`                    |                :angola:                | `angola`                               |
|     :antarctica:     | `antarctica`                 |              :argentina:               | `argentina`                            |
|   :american_samoa:   | `american_samoa`             |               :austria:                | `austria`                              |
|     :australia:      | `australia`                  |                :aruba:                 | `aruba`                                |
|   :aland_islands:    | `aland_islands`              |              :azerbaijan:              | `azerbaijan`                           |
| :bosnia_herzegovina: | `bosnia_herzegovina`         |               :barbados:               | `barbados`                             |
|     :bangladesh:     | `bangladesh`                 |               :belgium:                | `belgium`                              |
|    :burkina_faso:    | `burkina_faso`               |               :bulgaria:               | `bulgaria`                             |
|      :bahrain:       | `bahrain`                    |               :burundi:                | `burundi`                              |
|       :benin:        | `benin`                      |            :st_barthelemy:             | `st_barthelemy`                        |
|      :bermuda:       | `bermuda`                    |                :brunei:                | `brunei`                               |
|      :bolivia:       | `bolivia`                    |        :caribbean_netherlands:         | `caribbean_netherlands`                |
|       :brazil:       | `brazil`                     |               :bahamas:                | `bahamas`                              |
|       :bhutan:       | `bhutan`                     |               :botswana:               | `botswana`                             |
|      :belarus:       | `belarus`                    |                :belize:                | `belize`                               |
|       :canada:       | `canada`                     |            :cocos_islands:             | `cocos_islands`                        |
|   :congo_kinshasa:   | `congo_kinshasa`             |       :central_african_republic:       | `central_african_republic`             |
| :congo_brazzaville:  | `congo_brazzaville`          |             :switzerland:              | `switzerland`                          |
|    :cote_divoire:    | `cote_divoire`               |             :cook_islands:             | `cook_islands`                         |
|       :chile:        | `chile`                      |               :cameroon:               | `cameroon`                             |
|         :cn:         | `cn`                         |               :colombia:               | `colombia`                             |
|     :costa_rica:     | `costa_rica`                 |                 :cuba:                 | `cuba`                                 |
|     :cape_verde:     | `cape_verde`                 |               :curacao:                | `curacao`                              |
|  :christmas_island:  | `christmas_island`           |                :cyprus:                | `cyprus`                               |
|   :czech_republic:   | `czech_republic`             |                  :de:                  | `de`                                   |
|      :djibouti:      | `djibouti`                   |               :denmark:                | `denmark`                              |
|      :dominica:      | `dominica`                   |          :dominican_republic:          | `dominican_republic`                   |
|      :algeria:       | `algeria`                    |               :ecuador:                | `ecuador`                              |
|      :estonia:       | `estonia`                    |                :egypt:                 | `egypt`                                |
|   :western_sahara:   | `western_sahara`             |               :eritrea:                | `eritrea`                              |
|         :es:         | `es`                         |               :ethiopia:               | `ethiopia`                             |
|         :eu:         | `eu` <br /> `european_union` |               :finland:                | `finland`                              |
|        :fiji:        | `fiji`                       |           :falkland_islands:           | `falkland_islands`                     |
|     :micronesia:     | `micronesia`                 |            :faroe_islands:             | `faroe_islands`                        |
|         :fr:         | `fr`                         |                :gabon:                 | `gabon`                                |
|         :gb:         | `gb` <br /> `uk`             |               :grenada:                | `grenada`                              |
|      :georgia:       | `georgia`                    |            :french_guiana:             | `french_guiana`                        |
|      :guernsey:      | `guernsey`                   |                :ghana:                 | `ghana`                                |
|     :gibraltar:      | `gibraltar`                  |              :greenland:               | `greenland`                            |
|       :gambia:       | `gambia`                     |                :guinea:                | `guinea`                               |
|     :guadeloupe:     | `guadeloupe`                 |          :equatorial_guinea:           | `equatorial_guinea`                    |
|       :greece:       | `greece`                     | :south_georgia_south_sandwich_islands: | `south_georgia_south_sandwich_islands` |
|     :guatemala:      | `guatemala`                  |                 :guam:                 | `guam`                                 |
|   :guinea_bissau:    | `guinea_bissau`              |                :guyana:                | `guyana`                               |
|     :hong_kong:      | `hong_kong`                  |               :honduras:               | `honduras`                             |
|      :croatia:       | `croatia`                    |                :haiti:                 | `haiti`                                |
|      :hungary:       | `hungary`                    |            :canary_islands:            | `canary_islands`                       |
|     :indonesia:      | `indonesia`                  |               :ireland:                | `ireland`                              |
|       :israel:       | `israel`                     |             :isle_of_man:              | `isle_of_man`                          |
|       :india:        | `india`                      |    :british_indian_ocean_territory:    | `british_indian_ocean_territory`       |
|        :iraq:        | `iraq`                       |                 :iran:                 | `iran`                                 |
|      :iceland:       | `iceland`                    |                  :it:                  | `it`                                   |
|       :jersey:       | `jersey`                     |               :jamaica:                | `jamaica`                              |
|       :jordan:       | `jordan`                     |                  :jp:                  | `jp`                                   |
|       :kenya:        | `kenya`                      |              :kyrgyzstan:              | `kyrgyzstan`                           |
|      :cambodia:      | `cambodia`                   |               :kiribati:               | `kiribati`                             |
|      :comoros:       | `comoros`                    |            :st_kitts_nevis:            | `st_kitts_nevis`                       |
|    :north_korea:     | `north_korea`                |                  :kr:                  | `kr`                                   |
|       :kuwait:       | `kuwait`                     |            :cayman_islands:            | `cayman_islands`                       |
|     :kazakhstan:     | `kazakhstan`                 |                 :laos:                 | `laos`                                 |
|      :lebanon:       | `lebanon`                    |               :st_lucia:               | `st_lucia`                             |
|   :liechtenstein:    | `liechtenstein`              |              :sri_lanka:               | `sri_lanka`                            |
|      :liberia:       | `liberia`                    |               :lesotho:                | `lesotho`                              |
|     :lithuania:      | `lithuania`                  |              :luxembourg:              | `luxembourg`                           |
|       :latvia:       | `latvia`                     |                :libya:                 | `libya`                                |
|      :morocco:       | `morocco`                    |                :monaco:                | `monaco`                               |
|      :moldova:       | `moldova`                    |              :montenegro:              | `montenegro`                           |
|     :madagascar:     | `madagascar`                 |           :marshall_islands:           | `marshall_islands`                     |
|     :macedonia:      | `macedonia`                  |                 :mali:                 | `mali`                                 |
|      :myanmar:       | `myanmar`                    |               :mongolia:               | `mongolia`                             |
|       :macau:        | `macau`                      |       :northern_mariana_islands:       | `northern_mariana_islands`             |
|     :martinique:     | `martinique`                 |              :mauritania:              | `mauritania`                           |
|     :montserrat:     | `montserrat`                 |                :malta:                 | `malta`                                |
|     :mauritius:      | `mauritius`                  |               :maldives:               | `maldives`                             |
|       :malawi:       | `malawi`                     |                :mexico:                | `mexico`                               |
|      :malaysia:      | `malaysia`                   |              :mozambique:              | `mozambique`                           |
|      :namibia:       | `namibia`                    |            :new_caledonia:             | `new_caledonia`                        |
|       :niger:        | `niger`                      |            :norfolk_island:            | `norfolk_island`                       |
|      :nigeria:       | `nigeria`                    |              :nicaragua:               | `nicaragua`                            |
|    :netherlands:     | `netherlands`                |                :norway:                | `norway`                               |
|       :nepal:        | `nepal`                      |                :nauru:                 | `nauru`                                |
|        :niue:        | `niue`                       |             :new_zealand:              | `new_zealand`                          |
|        :oman:        | `oman`                       |                :panama:                | `panama`                               |
|        :peru:        | `peru`                       |           :french_polynesia:           | `french_polynesia`                     |
|  :papua_new_guinea:  | `papua_new_guinea`           |             :philippines:              | `philippines`                          |
|      :pakistan:      | `pakistan`                   |                :poland:                | `poland`                               |
| :st_pierre_miquelon: | `st_pierre_miquelon`         |           :pitcairn_islands:           | `pitcairn_islands`                     |
|    :puerto_rico:     | `puerto_rico`                |       :palestinian_territories:        | `palestinian_territories`              |
|      :portugal:      | `portugal`                   |                :palau:                 | `palau`                                |
|      :paraguay:      | `paraguay`                   |                :qatar:                 | `qatar`                                |
|      :reunion:       | `reunion`                    |               :romania:                | `romania`                              |
|       :serbia:       | `serbia`                     |                  :ru:                  | `ru`                                   |
|       :rwanda:       | `rwanda`                     |             :saudi_arabia:             | `saudi_arabia`                         |
|  :solomon_islands:   | `solomon_islands`            |              :seychelles:              | `seychelles`                           |
|       :sudan:        | `sudan`                      |                :sweden:                | `sweden`                               |
|     :singapore:      | `singapore`                  |              :st_helena:               | `st_helena`                            |
|      :slovenia:      | `slovenia`                   |               :slovakia:               | `slovakia`                             |
|    :sierra_leone:    | `sierra_leone`               |              :san_marino:              | `san_marino`                           |
|      :senegal:       | `senegal`                    |               :somalia:                | `somalia`                              |
|      :suriname:      | `suriname`                   |             :south_sudan:              | `south_sudan`                          |
| :sao_tome_principe:  | `sao_tome_principe`          |             :el_salvador:              | `el_salvador`                          |
|    :sint_maarten:    | `sint_maarten`               |                :syria:                 | `syria`                                |
|     :swaziland:      | `swaziland`                  |         :turks_caicos_islands:         | `turks_caicos_islands`                 |
|        :chad:        | `chad`                       |     :french_southern_territories:      | `french_southern_territories`          |
|        :togo:        | `togo`                       |               :thailand:               | `thailand`                             |
|     :tajikistan:     | `tajikistan`                 |               :tokelau:                | `tokelau`                              |
|    :timor_leste:     | `timor_leste`                |             :turkmenistan:             | `turkmenistan`                         |
|      :tunisia:       | `tunisia`                    |                :tonga:                 | `tonga`                                |
|         :tr:         | `tr`                         |           :trinidad_tobago:            | `trinidad_tobago`                      |
|       :tuvalu:       | `tuvalu`                     |                :taiwan:                | `taiwan`                               |
|      :tanzania:      | `tanzania`                   |               :ukraine:                | `ukraine`                              |
|       :uganda:       | `uganda`                     |                  :us:                  | `us`                                   |
|      :uruguay:       | `uruguay`                    |              :uzbekistan:              | `uzbekistan`                           |
|    :vatican_city:    | `vatican_city`               |        :st_vincent_grenadines:         | `st_vincent_grenadines`                |
|     :venezuela:      | `venezuela`                  |        :british_virgin_islands:        | `british_virgin_islands`               |
| :us_virgin_islands:  | `us_virgin_islands`          |               :vietnam:                | `vietnam`                              |
|      :vanuatu:       | `vanuatu`                    |            :wallis_futuna:             | `wallis_futuna`                        |
|       :samoa:        | `samoa`                      |                :kosovo:                | `kosovo`                               |
|       :yemen:        | `yemen`                      |               :mayotte:                | `mayotte`                              |
|    :south_africa:    | `south_africa`               |                :zambia:                | `zambia`                               |
|      :zimbabwe:      | `zimbabwe`                   |                                        |                                        |






