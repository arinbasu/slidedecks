
# Jupyter to reveal through markdown

---

## What we will do:
- Earlier we saw we can convert Jupyter notebooks to revealjs
- We used Pandoc to convert the markdown
- This time we will directly input the markdown
- Host it on github

---


## What we will specifically do:
- Write the content in jupyter <!-- .element: class="fragment" data-fragment-index="1" -->
- Use jupyter nbconvert to convert it to markdown <!-- .element: class="fragment" data-fragment-index="2" -->
- Use a barebones template for reveal <!-- .element: class="fragment" data-fragment-index="3" -->
- Externally source the markdown and all resources <!-- .element: class="fragment" data-fragment-index="4" -->
- Serve over github <!-- .element: class="fragment" data-fragment-index="5" -->

---
<!-- .slide: data-background="#ff0000" -->
# Create the boilerplate first 

---

```html
<html>
	<head>
		<link rel="stylesheet" href="reveal.js-master/css/reveal.css">
		<link rel="stylesheet" href="reveal.js-master/css/theme/white.css">
	</head>
	<body>
		<div class="reveal">
			<div class="slides">
				<section data-markdown="filename.md"
                data-separator="^\r?\n---\r?\n$"
                data-separator-vertical="^\r?\n--\r?\n$"
                >
                
                </section>
				
			</div>
		</div>
		<script src="reveal-js.master/js/reveal.js"></script>
		<script>
			Reveal.initialize();
		</script>
	</body>
</html>
```

---


