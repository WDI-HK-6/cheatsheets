#CSS Cheatsheet

##Pattern

```css
selector(s) {
	css-property: value;
	css-property: value;
}
```
HTML:

```html

<body>
	<header>
		<nav>
			<ul>
				<li class="nav-link"><a href="/">Home</a></li>
				<li class="nav-link"><a href="/about">About</a></li>
				<li class="nav-link"><a href="/contact">Contact</a></li>
			</ul>
		</nav>
	</header>
	<main>
		<section>
			<article>
				<h1 id="first-article-title" class="article-title"></h1>
				<p></p>
			</article>
			<aside></aside>
		</section>
		<section>
			<article>
				<h1 class="article-title"></h1>
				<p></p>
			</article>
			<aside></aside>
		</section>
	</main>
	<footer>
		<address id="campus1">33 Des Vouex Rd</address>
		<address id="campus2">Cyberport Core 3 SmartSpace 3</address>
	</footer>
</body>

```
CSS:

```css

nav {
	background-color: "black";
}

.nav-link {
	color: "white"
}

.nav-link a {
	text-decoration: none;
}

.nav-link a:link {
	text-decoration: none;
}

.nav-link a:hover {
	text-decoration: none;
}

.nav-link a:visited {
	text-decoration: none;
}

.nav-link a:focus {
	text-decoration: none;
}

.nav-link a:active {
	text-decoration: none;
}

h1 {
	font-weight: 600;
}

h1.article-title {
	color: "blue";
}

#first-article-title {
	font-weight: 800;
}

```