---
title: "A simple presentation"
author: "Petros Grammatikopoulos"
---

# The Beginning

When people ask me to talk about topics I like, I notice I have a tendency to present the topics to them. This gave birth to a need: I had to find the way that makes creating presentations:

- Quick
- Easy
- Accessible
- Uniform

# Pandoc and Markdown

<u>[Pandoc](https://pandoc.org/)</u> is an awesome tool that converts documents from one format to another. It supports many standards out of the box. This benefited my work, because I could use markdown, an easy markup language, in order to create presentations for others, quickly, in a format they can access online and navigate easily.

# A small usability test

Let's see how it handles subsections with code:

## Subsection sample

```java
public class HelloWorld {

    public static void main(String[] args) {
        // Prints "Hello, World" to the terminal window.
        System.out.println("Hello, World");
    }

}
```

# What about images?

Not only does this form of presentations handle all of markdown's features, like <u>[links](https://commonmark.org/)</u>

It also handles images, even ones that are already online, hosted in a different website than the presentation itself.

![](https://cdn.pixabay.com/photo/2012/05/07/13/18/cheetah-48433_960_720.png){ height=256 }

And it can also be enhanced with HTML features, to cover edge cases!

---

The source markdown code of this presentation will be included here for reference

````markdown
---
title: "A simple presentation"
author: "Petros Grammatikopoulos"
---

# The Beginning

When people ask me to talk about topics I like, I notice I have a tendency to present the topics to them. This gave birth to a need: I had to find the way that makes creating presentations:

- Quick
- Easy
- Accessible
- Uniform

# Pandoc and Markdown

<u>[Pandoc](https://pandoc.org/)</u> is an awesome tool that converts documents from one format to another. It supports many standards out of the box. This benefited my work, because I could use markdown, an easy markup language, in order to create presentations for others, quickly, in a format they can access online and navigate easily.

# A small usability test

Let's see how it handles subsections with code:

## Subsection sample

```java
public class HelloWorld {

    public static void main(String[] args) {
        // Prints "Hello, World" to the terminal window.
        System.out.println("Hello, World");
    }

}
```

# What about images?

Not only does this form of presentations handle all of markdown's features, like <u>[links](https://commonmark.org/)</u>

It also handles images, even ones that are already online, hosted in a different website than the presentation itself.

![](https://cdn.pixabay.com/photo/2012/05/07/13/18/cheetah-48433_960_720.png){ height=256 }

And it can also be enhanced with HTML features, to cover edge cases!
````

In order to produce a codeblock, that in turn includes other codeblocks, we just add an extra backtick when initiating it, like so:

`````markdown
````markdown
```java
```
````
`````

---

To produce this presentation I executed the <u>[following command](https://pandoc.org/demos.html)</u>:

```bash
pandoc -s --webtex -i -t slidy presentation.md -o index.html
```

This ensures that the presentation is interactive (as seen with items like bullet points) and that TeX formulas are converted to `<img>` representations (see <u>[here](https://pandoc.org/MANUAL.html#option--webtex)</u>).

---

<div style="margin: 0;position: absolute;top: 50%;left: 50%;margin-right: -50%;transform: translate(-50%, -50%);">Thank you!</div>