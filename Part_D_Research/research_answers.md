# Part D — Research Activities

This document contains answers and summaries for the five research activities in the HTML5 Basics assignment (Section 25, Page 93).

---

### 1. Research three HTML5 form input types not covered in detail today and describe what each does.

The three HTML5 input types selected for research are:

1.  **`type="color"`**:
    *   *What it does*: Renders a user interface element that allows the user to select a color. In most modern browsers, clicking this input opens the operating system's native color picker dialog or a browser-integrated palette.
    *   *Output*: Returns a 7-character hexadecimal string representing the selected color (e.g., `#ff5733`) in lowercase format.
    *   *Example*: `<input type="color" id="theme-color" name="theme-color">`

2.  **`type="url"`**:
    *   *What it does*: Creates a single-line text input field specifically designed for entering absolute URLs. It performs automatic client-side validation when the form is submitted, checking if the input value starts with a valid protocol (like `http://` or `https://`).
    *   *Accessibility*: On mobile devices, browsers often customize the on-screen keyboard to show keys optimized for web address entry, such as `/` and `.com`.
    *   *Example*: `<input type="url" id="website" name="website" placeholder="https://example.com">`

3.  **`type="time"`**:
    *   *What it does*: Renders a control designed for entering a time value (hours and minutes, and optionally seconds) in a 24-hour format (hh:mm). In modern browsers, it displays a dropdown or scrolling time picker UI.
    *   *Output*: Returns the selected time as a string in 24-hour format (e.g., `14:30` or `09:15`).
    *   *Example*: `<input type="time" id="appointment-time" name="appointment-time">`

---

### 2. Research what the W3C and the WHATWG are and the role each plays in HTML standards.

*   **W3C (World Wide Web Consortium)**:
    *   *What it is*: Founded in 1994 by Tim Berners-Lee, the W3C is an international public-interest organization where member organizations, full-time staff, and the public work together to develop open web standards (such as CSS, XML, and accessibility guidelines like WCAG).
    *   *Role*: Originally, the W3C published numbered, snapshot specifications of HTML (like HTML 3.2, 4.01). In 2019, they signed an agreement with the WHATWG to adopt the WHATWG HTML standard as the official single standard.

*   **WHATWG (Web Hypertext Application Technology Working Group)**:
    *   *What it is*: Formed in 2004 by individuals from Apple, Mozilla, and Opera who were frustrated by the W3C's focus on XML/XHTML and lack of focus on practical needs of web application developers.
    *   *Role*: The WHATWG develops and maintains the **HTML Living Standard**, which is continuously updated rather than released as versioned snapshots (such as "HTML 5.1" or "HTML 6"). It represents the current, canonical specification used by browser developers.

*   **Current Relationship**:
    *   Today, WHATWG owns the development of the HTML standard. The W3C cooperates with WHATWG to publish standard recommendations based on the WHATWG Living Standard, ensuring there is only a single unified definition of HTML.

---

### 3. Look up the WCAG accessibility guidelines and summarize, in your own words, three things they recommend for web content.

The **WCAG (Web Content Accessibility Guidelines)** are international standards developed by the W3C to make web content accessible to people with visual, auditory, motor, and cognitive disabilities. Three key recommendations from WCAG are:

1.  **Provide Text Alternatives (Alt Text)**:
    *   All non-text content (like images, icons, and illustrations) must have a text alternative (`alt` attribute) that describes its function or content. This allows screen readers to convey the information to visually impaired users and provides a text fallback if the asset fails to load.

2.  **Ensure Keyboard Accessibility**:
    *   All functionality, links, forms, and interactive components on the page must be fully navigable and operable using only a keyboard (without requiring a mouse). This is critical for users with motor impairments who rely on keyboard emulation devices.

3.  **Ensure Sufficient Color Contrast**:
    *   Text and images of text must have a minimum contrast ratio against their background (at least 4.5:1 for normal text and 3:1 for large text). This ensures that the content remains readable for users with low vision, color blindness, or varying lighting conditions.

---

### 4. Find a real, well-known website, open its source or Developer Tools, and identify three semantic elements it uses.

Analyzing the homepage of **GitHub** (https://github.com), the page utilizes various semantic elements for structure:

1.  **`<header>`**:
    *   Located at the very top of the page, wrapping the global navigation bar, search inputs, and sign-in buttons. It defines the introductory branding and utilities for the application.

2.  **`<nav>`**:
    *   Nested inside the header element, wrapping the primary navigation links ("Product", "Solutions", "Open Source", etc.). This indicates to screen readers that these links represent the main site navigation controls.

3.  **`<footer>`**:
    *   Located at the bottom of the page, wrapping the copyright information, terms of service link, privacy statement, and links to GitHub's social channels. It groups the ending metadata of the document.

---

### 5. Research the difference between block-level and inline elements in HTML and give two examples of each.

HTML elements are categorized into two primary display behaviors by default:

*   **Block-level Elements**:
    *   *Behavior*: These elements always start on a new line and stretch out to the left and right to occupy the full width of their parent container. They can contain other block-level elements as well as inline elements. You can set specific width and height values on them.
    *   *Example 1*: `<div>` — A generic block container used for grouping.
    *   *Example 2*: `<p>` — A paragraph block element that structures text.
    *   *Other examples*: `<h1>`–`<h6>`, `<ul>`, `<ol>`, `<li>`, `<header>`, `<main>`, `<footer>`, `<section>`.

*   **Inline Elements**:
    *   *Behavior*: These elements do not start on a new line; they only occupy as much width as their content requires, wrapping within the paragraph or line flow. They cannot contain block-level elements (only other inline elements or text). Sizing attributes (`width` and `height`) have no effect on inline elements by default.
    *   *Example 1*: `<span>` — A generic inline container used for text styling.
    *   *Example 2*: `<a>` — An inline anchor tag used to create hyperlinks.
    *   *Other examples*: `<strong>`, `<em>`, `<img>`, `<b>`, `<i>`, `<small>`, `<input>`.
