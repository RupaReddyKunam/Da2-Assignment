# Part A — Theory Questions

This document contains answers to the ten theory questions for the HTML5 Basics assignment (Section 25, Page 92).

---

### 1. Explain the full form of HTML and what each word means.

The full form of **HTML** is **HyperText Markup Language**. Each word carries a specific meaning that defines the purpose and functionality of the language:
*   **HyperText**: Refers to text that contains links (hyperlinks) connecting one document to another. Clicking a link allows a user to "jump" to a different web page or another section of the same page, moving beyond linear text reading.
*   **Markup**: Refers to a system of labels (tags) that "mark up" plain text to describe its structure and meaning. These labels instruct the web browser on how to interpret and display the raw text content.
*   **Language**: Refers to a defined set of rules, syntax, and vocabulary (tags and attributes) that the web browser understands and executes.

---

### 2. Why is HTML called a markup language and not a programming language?

HTML is a **markup language** because its primary role is to describe the structure, content, and layout of a document. It does not contain programming logic.
*   A **programming language** (like JavaScript, Python, or C++) can perform calculations, make decisions based on logical conditions (if/else), use variables to store state, run loops, and execute algorithms.
*   HTML cannot perform any of these actions. It has no logic or computational capabilities; it simply wraps existing content in tags to tell the browser: *"This is a heading," "This is a paragraph,"* or *"This is an image."* It represents the static skeleton of a web page.

---

### 3. Describe the difference between the `<head>` and `<body>` sections.

An HTML document is split into two primary sections, each serving a different purpose:
*   **`<head>` (Metadata Section)**: Contains information *about* the page (metadata) that is not directly displayed in the main browser window. This includes the page title (shown on the browser tab), character encoding (e.g., UTF-8), viewport settings for mobile responsiveness, search engine descriptions (SEO), links to CSS stylesheets, and references to JavaScript files.
*   **`<body>` (Visible Content Section)**: Contains all the actual content that users see and interact with on the screen. This includes headings, paragraphs, lists, tables, images, hyperlinks, forms, audio, and video elements.

---

### 4. Explain the difference between a tag, an element, and an attribute, with an example of each.

These three terms represent different components of HTML syntax:
*   **Tag**: The individual labels written in angle brackets used to mark the start or end of an element.
    *   *Example*: `<p>` is the opening tag; `</p>` is the closing tag.
*   **Element**: The complete building block of HTML, consisting of the opening tag, the content inside it, and the closing tag altogether. (Note: Some elements called "empty tags" or "void elements," like `<img>` or `<br>`, do not have content or closing tags).
    *   *Example*: `<p>This is a paragraph.</p>` represents the entire paragraph element.
*   **Attribute**: Extra information added to an element's opening tag to configure or modify its behavior or appearance. Attributes are written as name-value pairs (e.g., `name="value"`).
    *   *Example*: In the element `<a href="https://www.google.com">Google</a>`, the string `href="https://www.google.com"` is the attribute, where `href` is the attribute name and `https://www.google.com` is the attribute value.

---

### 5. What is the difference between `id` and `class`? When would you use each?

Both `id` and `class` are global attributes used to select elements for styling (CSS) or manipulation (JavaScript), but they have different uniqueness rules:
*   **`id` (Unique Identifier)**:
    *   An `id` value must be unique within a single HTML page. No two elements on the same page can share the same `id`.
    *   *When to use*: Use it to target a single, specific element that appears only once on a page (e.g., a site header, a main navigation bar, or a specific section anchor like `#contact`).
*   **`class` (Classification / Grouping)**:
    *   A `class` value does not have to be unique. Multiple elements on the same page can share the same class name, and a single element can have multiple classes (separated by spaces).
    *   *When to use*: Use it to group multiple elements together so they can share the same styling rules or behavior (e.g., applying a class of `btn` to all buttons, or `card` to multiple product panels).

---

### 6. Why are the `alt` attribute and the `<label>` element important for accessibility?

Accessibility (a11y) ensures that web pages are usable by everyone, including people with physical or cognitive disabilities:
*   **`alt` Attribute (Alternative Text for Images)**:
    *   Screen readers (software used by visually impaired users) read the `alt` text aloud to describe the image content.
    *   If an image fails to load due to a slow connection or a broken path, the browser displays the `alt` text as a fallback.
    *   Search engine bots use it to understand and index the image contents, improving SEO.
*   **`<label>` Element (Input Form Labels)**:
    *   Screen readers read the label text when a user focuses on the corresponding input field, explaining what information is required.
    *   It improves usability on all devices: clicking or tapping a `<label>` automatically focuses its associated input field, making it much easier to click small checkboxes or radio buttons.
    *   It is linked to an input using the `for` attribute on the label matching the `id` attribute of the input.

---

### 7. Explain the difference between `<strong>` / `<em>` and `<b>` / `<i>`.

While they look identical in a standard browser by default (bold and italic, respectively), they differ fundamentally in semantic meaning:
*   **`<strong>` vs `<b>`**:
    *   `<strong>` is a **semantic** tag indicating that the wrapped text is of strong importance, seriousness, or urgency. Screen readers will emphasize this text with a different tone of voice.
    *   `<b>` is a **presentational** tag that makes text bold visually for aesthetic purposes without adding any extra semantic importance or meaning.
*   **`<em>` vs `<i>`**:
    *   `<em>` is a **semantic** tag indicating emphasis (stress) on a word or phrase, which alters the meaning of the sentence. Screen readers will pronounce it with physical emphasis.
    *   `<i>` is a **presentational** tag that italicizes text visually (used conventionally for technical terms, foreign words, thoughts, or book titles) without adding semantic emphasis.

*Industry best practices dictate using semantic tags (`<strong>` and `<em>`) by default when meaning is implied, and reserving presentational tags (`<b>` and `<i>`) strictly for visual style adjustments.*

---

### 8. What is semantic HTML and why does it matter for SEO and accessibility?

**Semantic HTML** is the practice of using HTML tags that describe the structural meaning of the content they contain (e.g., `<header>`, `<nav>`, `<main>`, `<article>`, `<section>`, `<footer>`) rather than generic containers that carry no meaning (like `<div>` or `<span>`).

It matters for two key reasons:
1.  **Accessibility (a11y)**: Screen readers and assistive technologies use semantic tags to map the layout of the page. This allows users with visual impairments to navigate the document easily, jumping straight to the navigation menu (`<nav>`), the main content (`<main>`), or the footer (`<footer>`).
2.  **SEO (Search Engine Optimization)**: Search engine crawlers (like Googlebot) read the HTML code to index a site. Semantic elements clearly define what sections of the page are headers, primary articles, or footers, allowing search engines to understand the relevance and hierarchy of the content, which improves search ranking.

---

### 9. Explain the security risk of `target="_blank"` and how to prevent it.

When you create a hyperlink that opens in a new tab using `target="_blank"`, it introduces a vulnerability known as **tabnabbing**:
*   **Security Risk**: The newly opened page gains a reference back to the original page via the JavaScript property `window.opener`. A malicious site opened via this link can modify the original tab's destination URL (e.g., redirecting it to a fake login/phishing page) without the user noticing, leading to credential theft.
*   **Prevention**: Always append the attribute `rel="noopener noreferrer"` to any link that uses `target="_blank"`.
    *   `noopener` instructs the browser to set `window.opener` to `null`, severing the connection between the tabs.
    *   `noreferrer` prevents the browser from sending the referrer header, meaning the target page won't know the URL of the page the link was clicked from.

---

### 10. List four qualities of professional, industry-standard HTML.

Professional, high-quality HTML code is judged by these four overlapping qualities:
1.  **Clean Code / Structure**: Well-indented code that uses consistent formatting, lowercase tags and attributes, quoted attribute values, and properly closed/nested tags. It includes helpful comments for complex sections and avoids inline styles (separating structure from CSS presentation).
2.  **Accessibility (a11y)**: Built to be usable by everyone, utilizing descriptive image `alt` tags, linked input-label pairings, and a logical heading hierarchy (`<h1>` to `<h6>` in sequential order).
3.  **SEO-Friendly**: Employs descriptive title tags, meta descriptions, unique single `<h1>` headings, and semantic layouts to allow search engines to parse and rank the document effectively.
4.  **Maintainability**: Code that is self-documenting and organized using reusable patterns and semantic elements. This makes it easy for other developers (or the original developer in the future) to read, update, and debug.
