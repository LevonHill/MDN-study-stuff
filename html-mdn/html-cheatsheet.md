<!-- @format -->

HTML cheatsheet for syntax and common tasks

While using HTML it can be very handy to have an easy way to remember how to use HTML tags properly and how to apply them. MDN provides you with extended HTML reference documentation as well as a deep instructional set of HTML guides. However, in many cases we just need some quick hints as we go. That's the whole purpose of the cheat sheet, to give you some quick accurate ready to use code snippets for common usages.

Inline Elements

An "element" is a single part of a webpage. Some elements are large and hold smaller elements like containers. Some elements are small and are "nested" inside larger ones. By default, "inline elements" appear next to one another in a webpage. They take up only as much width as they need in a page and fit together horizontally like words in a sentence or books shelved side-by-side in a row. All inline elements can be placed within the <body> element.

Document Root & Metadata

<html>: The root element of an HTML document — all other elements are descendants.

<head>: Contains metadata (title, links to styles/scripts, meta tags).

<title>: The document’s title shown in the browser tab.

<meta>: Metadata about the document (charset, viewport, etc).

<link>: Relationship to external resources (CSS, icons).

<body>: The content of the document (what is displayed to the user)

//
Sectioning / Semantic Structure

<header>: Introductory section of a page or a section (often contains navigation, logo).

<nav>: Navigation links section.

<main>: The main content area of the document (one per page).

<section>: A thematic grouping of content, usually with a heading.

<article>: A self-contained composition in the document (blog post, forum post, product card). 
<aside>: Content related to the main content but separate (sidebar, call-out box).

<footer>: Footer for its nearest ancestor sectioning or root element (author info, copyright, links).

<address>: Contact information for author or organization

Text Content & Inline Semantics

<h1> … <h6>: Headings levels 1 through 6, defining document outline. 
Wikipedia
+1
<p>: Paragraph of text.

<blockquote>: A section quoted from another source.

<em>: Emphasized text (semantically important).

<strong>: Strong importance (semantic bold).

<small>: Smaller print for fine print or disclaimers.

<mark>: Marked or highlighted text.
FreeCodeCamp

<del> / <ins>: Text that has been deleted / inserted (for revision records).

<sub> / <sup>: Subscript / superscript text (H₂O, x²).

<span>: Generic inline container for text (no semantic meaning).

<div>: Generic block container (no semantic meaning).

Lists & Links

<a>: Anchor element, hyperlink to another page or location.

<ul>: Unordered list.

<ol>: Ordered list.

<li>: List item (inside ul or ol).

<dl>: Description list (terms and descriptions).

<dt>: Term/name in description list.

<dd>: Description of a term in description list.

Media / Embedded Content

<img>: Embed an image.

<figure>: Content with optional caption (image, chart, etc).

<figcaption>: Caption for the figure.

<audio>: Embed audio content.

<video>: Embed video content.

<source>: Specify multiple media sources for audio/video elements.

<picture>: Responsive images container for multiple sources.

<canvas>: A drawing surface for graphics via JavaScript.

<svg>: Scalable Vector Graphics markup for vector images.

<embed> / <object> / <iframe>: Embedding other content (plugins, external documents).

Tables

<table>: Table container for tabular data.

<thead>: Header section of a table.

<tbody>: Body section of a table.

<tfoot>: Footer section of a table.

<tr>: Table row.

<th>: Table header cell.

<td>: Table data cell.

<caption>: A caption for the table.

<colgroup> / <col>: Grouping and styling columns.

Forms & Interactive Elements

<form>: Form container for user input.

<input>: Input control (text, checkbox, radio, etc).

<textarea>: Multi-line text input.

<select>: Drop-down list.

<option>: Option in a select list.

<label>: Label for a form control.

<button>: Clickable button.

<fieldset>: Group related controls within a form.

<legend>: Caption for a fieldset.

<datalist>: List of predefined options for an input.

<output>: Represents the result of a calculation.

<progress>: Represents progress of a task.

<meter>: Represents a scalar measurement within a known range.

<details>: Disclosure widget which the user can open/close.

<summary>: Summary, caption, or legend for the details element.

Scripting & Programming

<script>: JavaScript code or link to a script.

<noscript>: Content to be shown if scripting is disabled.

<template>: Client-side template for HTML that isn't rendered immediately.

<slot>: A placeholder inside a Web Component where external content is inserted.

Miscellaneous / Utility

<meta>: Metadata about the page (already listed under metadata).

<link>: External resource linking (listed under metadata).

<style>: Embedded CSS styles within HTML.

<blockquote>: Quoted section (listed earlier).

<time>: Represents a specific time or date and can include a datetime attribute for machine readability. 

<wbr>: Word-break opportunity—indicates where the browser may break a line.
