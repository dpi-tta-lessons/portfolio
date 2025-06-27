# Build Your Portfolio Page

Create a personal portfolio webpage to showcase your work and make it easy for others to find your projects online.

<!-- TODO: screenshot of completed portfolio -->
![Screenshot of finished portfolio](assets/finished-portfolio-example.png)

## Why You Need a Portfolio

As a developer, having a portfolio gives you a space to:

- Share your projects
- Tell your story
- Show off your skills
- Be discoverable by employers or collaborators

In this lesson, you'll build a personal web page using HTML and CSS inside a GitHub Codespace.

## 1. Use Your Codespace

<!-- TODO: show how to access codespaces in GitHub (screenshots)  -->
Open the same Codespace you used in the GitHub + Codespaces lesson to create your `<h1>Hello, world!</h1>` app. You can access your codespaces here [https://github.com/codespaces](https://github.com/codespaces).

Alternatively, navigate to the repository where you created your Codespace (e.g. `your-username/hello-world`). Click the green **Code** button and then the **Codespaces** tab to reopen your environment.

![Access from repo](assets/access-codespace-from-repo.png)

<aside class="warning">
  If you haven’t set up a Codespace before, start with this lesson (<a href="" target="_blank">Getting Started with GitHub Codespaces</a>) to create a new repo from the <a href="https://github.com/dpi-tta-projects/static-html-template" target="_blank">static-html-template</a>.
</aside>

<!-- Create a new file inside your project folder: -->

Open the `index.html` file we created in <a href="" target="_blank">Getting Started with GitHub Codespaces</a> and get ready to write the HTML and CSS we need for your portfolio.

## 2. Gather Your Content

You'll need:

- A headshot or avatar image
- A short bio or tagline
- Links to projects or social media (+ images or icons)

## 3. Start with the HTML Boilerplate

<aside class="tip">
  <strong>What does "boilerplate" mean?</strong><br>
  In programming, "boilerplate" refers to snippets of code that are repeated multiple times with little (or no) variation. When using languages that are considered verbose, programmers must write a lot of boilerplate code to accomplish only minor functionality.
</aside>

Here's a complete basic layout:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>Your Title Goes Here</title>
  </head>
  <body>
    <!-- Your content goes here -->
  </body>
</html>
```
{: .repl }

<aside class="tip">
  You wont see anything rendered when you click `run` because we haven't added any content inside the <code>body</code>.
</aside>

Replace your `<h1>Hello, world</h1>` with this layout in your `index.html` file. We'll add content to the body in the [next step](#4-build-the-page-layout).

### What Each Line Does

#### Doctype

```html
<!DOCTYPE html>
```

Declares that this file uses HTML5 — the current standard.

#### HTML lang Attribute

```html
<html lang="en">
```
Starts the HTML document. The `lang="en"` tells browsers (and screen readers) that the content is in English.

#### Head

```html
<head>
```

The head section contains setup info about your page — like the title, fonts, or meta tags. This content doesn’t appear directly on the page.

<aside class="tip">
  We call this machine-readable information "metadata". Metadata is data that describes data. For example, an HTML document is data, but HTML can also contain metadata in its <code>head</code> element that describes the document.

  <cite>
    <a href="https://developer.mozilla.org/en-US/docs/Glossary/Metadata">
      MDN
    </a>
  </cite>
</aside>

#### Charset

```html
<meta charset="UTF-8">
```

Makes sure your page can display all types of characters — symbols, emojis, accents, etc. It is used to ensure that the browser correctly interprets the characters and symbols on the webpage, commonly set as UTF-8 for universal character support across languages and symbols.

#### Title

```html
<title>Your Title Goes Here</title>
```

Sets the text that appears in the browser tab.

![title in tab](assets/title-tab.png)

<aside class="warning">
  Make sure to change this to something relevant for your website. 😄
</aside>

#### Body

```html
<body>
```

This is the visible part of your site — everything inside the `<body>` tags show up in the browser window.

## 4. Build the Page Layout

Add this basic structure to your body, replacing the `<!-- Your content goes here -->` comment.

```html
<header>
  <img src="assets/avatar.jpg" alt="Portrait of Ian Heraty">
  <h1>Ian Heraty</h1>
  <h3>
    Software Development Educator at Discovery Partners Institute
  </h3>
  <p>
    Ian is a technical instructor who helps trainees master full stack web development in preparation for technology roles. Before joining Discovery Partners Institute, Ian worked for several years as a software developer and digital consultant. Following a successful career in custom software development and digital consulting, Ian now guides trainees in building robust web applications and developing industry-ready skills. Ian enjoys music, tennis, and exploring new technologies.
  </p>
</header>

<main>
  <section>
    <h3>Social Links</h3>
    <ul>
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
        <a href="mailto:ihera2@uillinois.edu" target="_blank">
          Email
        </a>
      </li>
    </ul>
  </section>

  <section>
    <h3>Blog Posts</h3>
    <ul>
      <li>
        <a href="https://paulgraham.com/startupideas.html" target="_blank">
          How to Get Startup Ideas
        </a>
      </li>
      <li>
        <a href="https://foundersatwork.posthaven.com/find-your-people" target="_blank">
          Find Your People
        </a>
      </li>
      <li>
        <a href="https://a16z.com/why-software-is-eating-the-world/" target="_blank">
          Why Software Is Eating the World
        </a>
      </li>
    </ul>
  </section>
</main>
```
{: .repl }

<!-- TODO: add screenshot -->
<aside class="tip">
  Notice how we use indents to indicate nesting. Typically, opening and closing tags should be either on the same line or vertically aligned. This helps us humans read the code and more easily identify bugs.
</aside>

| Tag        | What it does                                                                 |
|------------|------------------------------------------------------------------------------|
| `<header>` | Contains introductory content (like your name and avatar)                   |
| `<main>`   | Main content of the document (what the page is about)                       |
| `<section>`| A thematically grouped chunk of content                                     |
| `<h1>`–`<h6>` | Headings; use only one `<h1>` per page (the title), then subheadings     |
| `<p>`      | Paragraph of text                                                            |
| `<a>`      | Anchor (link) element                                                        |
| `<ul>` / `<li>` | Unordered list and list items                                           |
| `<img>`    | Image element                                                                |
| `<div>`    | Generic container with no semantic meaning (use when nothing else fits)     |

<aside class="tip">
  Use all lowercase kebab-case for filenames (eg my-avatar.jpg) to avoid broken links and stay consistent across platforms. Even though filename casing does not affect functionality, it's a good practice to follow a convention and be consistent. Also, casing becomes very important in some languages.
</aside>

![basic page layout](assets/basic-layout.png)

Now you can replace all the placeholder images, links, and text with your own content. When you've got all your own content setup, you can move on to [styling](#5-styling) so it looks professional.

### Missing Image Icon

![broken image icon](assets/broken-image-icon.png)

You will likely notice a 'broken image icon' after pasting in the basic layout code. This happens when the browser can not find the image at the given path, `src=""`. When this happens, the browser falls back to the value set to `alt`, in our case `"Portrait of Ian Heraty"`.

<!-- TODO: explain how paths work with `/` -->

Let's add our image to the codespace so we can fix this broken image. A standard practice is to have an `assets` folder for images, stylesheets, and scripts needed to run our app. Create the `assets` folder and another folder inside called `images`. Now we'll update the `src` attribute to point to our avatar image `assets/images/my-avatar-file`.

<video src="assets/fix-broken-image.mp4" autoplay loop muted playsinline></video>

### Add a Debug Border

To visualize layout areas during development, add this to your CSS:

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
  <p>The * selector targets all elements. Notice how every element is wrapped in a border.</p>
</div>
```
{: .repl }

Add this debug border to your portfolio page while building out the layout.

![debug border portfolio](assets/debug-border-example.png)

You can remove this style rule later once the layout looks good.

<!-- TODO:

add these to our portfolio step by step
start with inline styles, then <style> tags (with element/id/class selectors), then css stylesheet 

-->
## 5. Style

Now that you have your HTML layout in place, let's start styling it. You'll first apply inline styles directly to elements, then refactor those into a `<style>` tag in the `<head>`, and finally move them to a `.css` file for a clean, professional structure.

<aside class="tip">
  The "Cascading" in Cascading Style Sheets means that <strong>styles get applied in order</strong>. If two styles conflict, the last one usually wins.

  For example:
  <pre>
    <code>
      p {
        color: red;
      }

      p {
        color: blue;
      }
    </code>
  </pre>

  The paragraph text will be blue, because it’s the last rule declared.
</aside>

<!--
TODO: maybe put this in a css reference?

break this down by style rule (eg font-family, margin, padding, text-align, etc. 

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

```css
margin: auto;
padding: 1rem;
border-radius: 8px;
box-shadow: 0 4px 6px rgba(0,0,0,0.1);
```
-->



## 6. Make It Responsive

Most people will view your site on their phones. Responsive design ensures it looks good on all screen sizes.

<!-- TODO:

Explaining the viewport meta tag
Avoiding fixed widths (width: 500px) in favor of percentages or max-width

-->

In the `<head>`, make sure this tag is present:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
{: .copyable }

<!-- TODO: explain viewport -->

<!-- TODO: explain -->
Use relative units (em, %) in your styles and avoid fixed pixel widths when possible.

## 7. Use Font Awesome Icons

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

## 8. Make Your Link Previews Stand Out

<!-- TODO: make port public to use on metatags io. (does this work?) -->

To make your page look great when shared, use MetaTags.io to generate a preview and copy the meta tags into your HTML.

<aside class="tip">
  Meta tags help social platforms like LinkedIn or Twitter show a nice preview when someone shares your link.
</aside>

<!-- TODO: add screenshot -->

<!-- TOOD: add practical meta tag examples 

<meta property="og:title" content="Ian Heraty's Portfolio">
<meta property="og:image" content="/assets/avatar.jpg">
<meta property="og:description" content="Software Development Educator and Mentor">
<meta property="og:url" content="https://yourdomain.com">

-->

<!-- TODO: Create a new `style.css` file next to your HTML file. -->

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


<!-- TODO

add aside on indents and formatting to improve readability 

maybe do this in a subsequent "code review" lesson?

In VS Code, use Cmd+Shift+P (Mac) or Ctrl+Shift+P (Windows), then search “Format Document” to clean up your HTML or CSS automatically.
-->

<!-- TODO: refactoring

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
Ensures the layout adjusts properly on mobile devices (very important for responsive design!).

stylesheet 

refactor and move to `styles/application.css`

```html
<link rel="stylesheet" href="styles/application.css">
```
Connects your HTML to an external CSS file so you can style your page.

-->

## Using Devtools

### View Page Source

In Chrome, right-click anywhere on a webpage and choose `View Page Source`. This helps you learn how other websites are built!

<video src="assets/view-page-source.mp4" autoplay loop muted playsinline></video>

Keyboard Shortcut:

- Ctrl + U (Windows)
- Command ⌘ + Option ⌥ + U (Mac)

### Inspector

In Chrome, right-click anywhere on a webpage and choose `Inspect`. This allows you to click on any element and see the code.

<video src="assets/inspector.mp4" autoplay loop muted playsinline></video>
  
Keyboard Shortcut:

- Ctrl + I (Windows)
- Command ⌘ + Option ⌥ + I (Mac)

### Toggle Device Toolbar

To preview how your site looks on different screen sizes:

- Right-click your site → **Inspect**
- Click the **Toggle device toolbar** icon

Keyboard Shortcut:

- Ctrl + Shift + M (Windows)
- Command ⌘ + Shift + M (Mac)

This simulates phones and tablets in your browser.

![mobile view toggle](assets/devtools-mobile-toggle.png)

## Validate Your HTML

Use the [W3C Validator](https://validator.w3.org/) to check your code for mistakes. Paste your HTML code or upload the file to check for typos or unclosed tags. This can be a life saver when you can't figure out what's breaking your HTML.

## What’s Next?

You now have a static site ready to deploy!

<aside class="danger">
  ⚠️ Codespaces shut down after ~30 minutes of inactivity. In the next lesson, you'll learn how to deploy your site so it's available 24/7.
</aside>

In the next lessons, you’ll:

- Host your page online to make it available 24/7
- Get your first "code review"
- Connect a custom domain (optional)

## Practice Challenge

- Add at least 3 links with Font Awesome icons
- Try using a new font from Google Fonts
- Add a background image to your page
