
# Jupyter to reveal through markdown

---

## What we will do:
- Earlier we saw we can convert Jupyter notebooks to revealjs
- We used Pandoc to convert the markdown
- This time we will directly input the markdown
- Host it on github

---


## What we will specifically do:
- Write the content in jupyter
- Use jupyter nbconvert to convert it to markdown
- Use a barebones template for reveal
- Externally source the markdown and all resources
- Serve over github

---
# Create the boilerplate first { .slide: data-background="#ff0000"}

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


