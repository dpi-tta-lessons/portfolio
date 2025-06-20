# Build Your Portfolio Page

Create a personal portfolio webpage to showcase your work and make it easy for others to find your projects online.

<!-- TODO: screenshot of completed portfolio -->

## Why You Need a Portfolio

As a developer, having a portfolio gives you a space to:

- Share your projects
- Tell your story
- Show off your skills
- Be discoverable by employers or collaborators

In this lesson, you'll build a personal web page using HTML and CSS inside a GitHub Codespace.

## 1. Use Your Codespace

<!-- TODO: link to lesson here -->
Open the same Codespace you used in the GitHub + Codespaces lesson. You can access your codespaces here [https://github.com/codespaces](https://github.com/codespaces).

<!-- TODO: show how to access codespaces in GitHub (screenshots) -->

<!-- Create a new file inside your project folder: -->

Open `index.html` and get ready to write your HTML.

<!-- TODO

https://developer.mozilla.org/en-US/docs/Learn_web_development/Getting_started/Environment_setup/Dealing_with_files#what_structure_should_a_website_have

The root directory is where the main HTML files, such as index.html, are stored.
 Additionally, it is common to have a dedicated folder for static assets like images, stylesheets, and JavaScript files.
 This helps keep the project organized and makes it easier to manage and scale the website as it grows. For a basic static website, having all HTML pages in the same root directory might work, but as the site becomes more complex, organizing pages into subdirectories can improve manageability.

/
index.html
images/
styles/
pages/

-->

<!-- TODO: How to view source in Chrome -->

## 2. Gather Your Content

You'll need:

- A headshot or avatar image
- A short bio or tagline
- Links to projects or social media (+ images or icons)

## 3. Start with the HTML Boilerplate

<!-- TODO: break this down. what is each element doing? -->
Here's a complete basic layout:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ian Heraty</title>
    <link rel="stylesheet" href="style.css">
  </head>
  <body>
    <!-- Your content goes here -->
  </body>
</html>
```
{: .repl }

Create a new `style.css` file next to your HTML file.

## 4. Add a Debug Border

To visualize layout areas, add this to your CSS:

```css
* {
  border: 1px solid red;
}
```
{: .copyable }

```html
<style>
* {
  border: 1px solid red;
}
</style>

<div>
  <p>Notice how this element is wrapped in a border</p>
</div>
```
{: .repl }

You can remove this later once layout looks good.

## 5. Build the Page Layout

Add this basic structure to your body:

```html
<header>
  <img src="assets/avatar.jpg" alt="Ian Heraty">
  <h1>Ian Heraty</h1>
  <p>
    Software Development Educator at Discovery Partners Institute. Ian is a technical instructor who helps trainees master full stack web development in preparation for technology roles. Before joining Discovery Partners Institute, Ian worked for several years as a software developer and digital consultant. Following a successful career in custom software development and digital consulting, Ian now guides trainees in building robust web applications and developing industry-ready skills. Ian enjoys music, tennis, and exploring new technologies.
  <p>
</header>

<main>
  <h2>Links</h2>
  <ul>
    <!-- TODO: Add Icons -->
    <li>
      <a href="https://www.linkedin.com/in/ianheraty/" target="_blank">
        LinkedIn
      </a>
    </li>
    <li>
      <a href="https://github.com/heratyian" target="_blank">
        GitHub
      </a>
    </li>
    <li>
      <a href="https://www.youtube.com/@dpi-tta" target="_blank">
        Tech Talent Accelerator YouTube Page
      </a>
    </li>
  </ul>
</main>
```
{: .repl }

<!-- TODO: adding images -->

<!-- TODO

note on renaming and using standard / consistent casing in images 
(kebab-case is good)
this makes it easier for us 

-->

<!-- TODO: start with <style> tags in the <head> 

then refactor and move to `styles/application.css`

-->
## 6. Clean Styling in `style.css`

```css
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  text-align: center;
  background: linear-gradient(to right, #ece9e6, #ffffff);
  min-height: 100vh;
}

img {
  width: 150px;
  border-radius: 50%;
  box-shadow: 0 0 10px rgba(0,0,0,0.2);
}
```
{: .copyable }

### Common CSS Properties

<!-- TODO: break this up and explain (using practical examples for each: margin, padding, border-radius, box-shadow) -->
```css
margin: auto;
padding: 1rem;
border-radius: 8px;
box-shadow: 0 4px 6px rgba(0,0,0,0.1);
```

## 7. Make It Responsive

<!-- TODO: explain why responsive is important. mobile first. how to use the inspector mobile view -->
In the `<head>`, make sure this tag is present:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
{: .copyable }

<!-- TODO: explain -->
Use relative units (em, %) in your styles and avoid fixed pixel widths when possible.

## 8. Use Font Awesome Icons

Add this to your `<head>`:

```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.7.2/css/all.min.css" />
```
{: .copyable }

Now you can use icons like:

```html
<i class="fab fa-github"></i> GitHub
```
{: .copyable }

```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.7.2/css/all.min.css" />


<i class="fab fa-github"></i> GitHub
```
{: .repl}

## 9. Make Your Link Previews Stand Out

<!-- TODO: make port public to use on metatags io. (does this work?) -->

To make your page look great when shared, use MetaTags.io to generate a preview and copy the meta tags into your HTML.

<aside class="tip">
  Meta tags help social platforms like LinkedIn or Twitter show a nice preview when someone shares your link.
</aside>

<!-- TODO: add screenshot -->

<!-- TOOD: add practical meta tag examples -->

## 10. Validate Your HTML

Use the W3C Validator to check your code for mistakes.

<!-- TODO: link -->

<!-- TODO: mention that codespaces shut down after 30 minutes of inactivity. need to make it available 24/7 -->

<!-- TODO: add aside on indents and formatting to improve readability -->

<!-- TODO: add aside on using vs code format document cmd + shift + p and type "Format document" -->

## What’s Next?

You now have a static site ready to deploy!

In the next lesson, you’ll:

- Host your page online
- Make it available 24/7
- Connect a custom domain

## Practice Challenge

- Add at least 3 links with Font Awesome icons
- Try using a new font from Google Fonts
- Add a background image to your page
