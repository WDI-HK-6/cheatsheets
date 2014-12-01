#HTML Cheatsheet

HTML is never used solely for styling.

https://developer.mozilla.org/en/docs/Web/Guide/HTML/HTML5/HTML5_element_list

```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<title>My Title</title>
		<link rel="stylesheet" type="text/css" href="/css/styles.css">
		<script type="text/javascript" src="/js/scripts.js"></script>
	</head>
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
</html>
```

##Forms

```<form>``` - https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Forms_in_HTML

```<input>``` - https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Input

```<textarea>``` - https://developer.mozilla.org/en-US/docs/Web/HTML/Element/textarea

```<select>``` - https://developer.mozilla.org/en-US/docs/Web/HTML/Element/select

```html
<form action="" name="contact-form">

	<label for="userEmail">Enter Your Email</label>
	<input type="email" name="userEmail" placeholder="example@none.com">
	
	<label for="title">Subject:</label>
	<input type="text" name="title" placeholder="Title of Your Email">
	
	<label for="content">Email Content:</label>
	<textarea name="content" rows="4"></textarea>
	
	<label for="gender">Are you Male or Female?</label>
	<input type="radio" name="gender" value="male" checked>Male
	<input type="radio" name="gender" value="female">Female

    <label for="ownsCar">Do you have a car?</label>
	<input type="checkbox" name="ownsCar">
    <label for="hasPets">Do you have a pet?</label>
	<input type="checkbox" name="hasPets">
	
	<label for="country">Please Select Your Country</label>
	<select name="country">
	  <option value="HK" selected>Hong Kong</option>
	  <option value="US">United States</option>
	  <option value="UK">United Kingdom</option>
	  <option value="AUS">Australia</option>
	</select>
	
	<input type="submit" value="Submit">
</form>
```