layout:true
name: invert-layout
class: azc-green-invert azl-topic
---
layout: true
class: azc-green azl-topic

---
class: azl-title
# Cheat Sheet

---
# Separating Slides

```md
# Slide 1
This is slide 1
---
# Slide 2
This is slide 2
```

---
# Incremental Slide
--


```md
# Slide

- bullet 1
--

- bullet 2
```

---
# Slide Note

```md
# Slide

Some content.

???
Some note.
```

Push `p` to show the note of this slide.

???
Some note.

---
name: naming-slide
# Naming a Slide
```markdonw
name: slidename
```

* Link to a slide using URL fragment like [this](#naming-slide)

* access from remark.js API like
```js
slideshow.gotoSlide('slidename')
```

* used as id of slide's DOM like
```html
<div id="slidename" class="remark-slide-content">
```

* reference of [template](#template)


---
# Specify CSS's Class
* to a slide
```md
class: classname
```
* to text-block
```md
.classname[inner text]
```

---
background-image: url(./images/cheat-sheet/sannaimaruyama.jpg)
# Background Image
```md
background-image: url(./images/cheat-sheet/sannaimaruyama.jpg)
```

---
count: false
# Skip Count
```md
count: false
```

---
name: template
# Template
```md
template: other-slidename
```
* name and layout properties are not inherited
* class properties are merged, preserving class order
* including position can be specified as {`{content}`}

---
template: invert-layout
# Layout Slide
* slide to specify layout and not to be shown itself in slide-show
* define layout slide and apply it to subsequent slides:
```md
layout: true
(name: my-layout)
class: foo, bar
```
* if you want to apply layout slides explicitly:
```md
template: my-layout
# Slide with MyLayout
```

---
# Exclude
```md
exclude: true
```

---
# Slide-show configuration
see [official wiki](https://github.com/gnab/remark/wiki/Configuration)

---
# images
* use markdown syntax
```md
.center[![meanless-graph](./images/cheat-sheet/meanless-graph.png)]
```

.center[![meanless-graph](./images/cheat-sheet/meanless-graph.png)]

---
# KaTeX (broken?)
1. This is an inline integral: \(\int_a^bf(x)dx\)
2. More \(x={a \over b}\) formulae.

Display formula:

$$e^{i\pi} + 1 = 0$$

---
# Mermaid (broken?)
.mermaid[graph LR
        A-->B
        B-->C
        C-->A
        D-->C]
