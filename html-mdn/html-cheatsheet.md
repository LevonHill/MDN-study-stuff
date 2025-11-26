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


LIST OF GLOBAL attributes 

accesskey
Provides a hint for generating a keyboard shortcut for the current element. This attribute consists of a space-separated list of characters. The browser should use the first one that exists on the computer keyboard layout.

anchor Non-standard
Associates a positioned element with an anchor element. The attribute's value is the id value of the element you want to anchor the positioned element to. The element can then be positioned using CSS anchor positioning.

autocapitalize
Controls whether inputted text is automatically capitalized and, if so, in what manner.

autocorrect
Controls whether input text is automatically corrected for spelling errors. This can be applied to elements that have editable text except for <input> elements with the attribute: type="password", type="email", or type="url".

autofocus
Indicates that an element is to be focused on page load, or as soon as the <dialog> it is part of is displayed. This attribute is a boolean, initially false.

class
A space-separated list of the classes of the element. Classes allow CSS and JavaScript to select and access specific elements via the class selectors or functions like the method Document.getElementsByClassName().

contenteditable
An enumerated attribute indicating if the element should be editable by the user. If so, the browser modifies its widget to allow editing. The attribute must take one of the following values:

true or the empty string, which indicates that the element must be editable;
false, which indicates that the element must not be editable.
plaintext-only, which indicates the element's raw text is editable, but rich text formatting is disabled.
data-*
Forms a class of attributes, called custom data attributes, that allow proprietary information to be exchanged between the HTML and its DOM representation that may be used by scripts. All such custom data are available via the HTMLElement interface of the element the attribute is set on. The HTMLElement.dataset property gives access to them.

dir
An enumerated attribute indicating the directionality of the element's text. It can have the following values:

ltr, which means left to right and is to be used for languages that are written from the left to the right (like English);
rtl, which means right to left and is to be used for languages that are written from the right to the left (like Arabic);
auto, which lets the user agent decide. It uses a basic algorithm as it parses the characters inside the element until it finds a character with a strong directionality, then it applies that directionality to the whole element.
draggable
An enumerated attribute indicating whether the element can be dragged, using the Drag and Drop API. It can have the following values:

true, which indicates that the element may be dragged
false, which indicates that the element may not be dragged.
enterkeyhint
Hints what action label (or icon) to present for the enter key on virtual keyboards.

exportparts
Used to transitively export shadow parts from a nested shadow tree into a containing light tree.

hidden
An enumerated attribute indicating that the element is not yet, or is no longer, relevant. For example, it can be used to hide elements of the page that can't be used until the login process has been completed. The browser won't render such elements. This attribute must not be used to hide content that could legitimately be shown.

id
Defines a unique identifier (ID) which must be unique in the whole document. Its purpose is to identify the element when linking (using a fragment identifier), scripting, or styling (with CSS).

inert
A boolean value that makes the browser disregard user input events for the element. Useful when click events are present.

inputmode
Provides a hint to browsers about the type of virtual keyboard configuration to use when editing this element or its contents. Used primarily on <input> elements, but is usable on any element while in contenteditable mode.

is
Allows you to specify that a standard HTML element should behave like a registered customized built-in element (see Using custom elements for more details).

Note: The item* attributes are part of the WHATWG HTML Microdata feature.

itemid
The unique, global identifier of an item.

itemprop
Used to add properties to an item. Every HTML element may have an itemprop attribute specified, where an itemprop consists of a name and value pair.

itemref
Properties that are not descendants of an element with the itemscope attribute can be associated with the item using an itemref. It provides a list of element ids (not itemids) with additional properties elsewhere in the document.

itemscope
itemscope (usually) works along with itemtype to specify that the HTML contained in a block is about a particular item. itemscope creates the Item and defines the scope of the itemtype associated with it. itemtype is a valid URL of a vocabulary (such as schema.org) that describes the item and its properties context.

itemtype
Specifies the URL of the vocabulary that will be used to define itemprops (item properties) in the data structure. itemscope is used to set the scope of where in the data structure the vocabulary set by itemtype will be active.

lang
Helps define the language of an element: the language that non-editable elements are in, or the language that editable elements should be written in by the user. The attribute should contain a valid BCP 47 language tag. xml:lang has priority over it.

nonce
A cryptographic nonce ("number used once") which can be used by Content Security Policy to determine whether or not a given fetch will be allowed to proceed.

part
A space-separated list of the part names of the element. Part names allows CSS to select and style specific elements in a shadow tree via the ::part pseudo-element.

popover
Used to designate an element as a popover element (see Popover API). Popover elements are hidden via display: none until opened via an invoking/control element (i.e., a <button> or <input type="button"> with a popovertarget attribute) or a HTMLElement.showPopover() call.

role
Roles define the semantic meaning of content, allowing screen readers and other tools to present and support interaction with an object in a way that is consistent with user expectations of that type of object. roles are added to HTML elements using role="role_type", where role_type is the name of a role in the ARIA specification.

slot
Assigns a slot in a shadow DOM shadow tree to an element: An element with a slot attribute is assigned to the slot created by the <slot> element whose name attribute's value matches that slot attribute's value.

spellcheck
An enumerated attribute defines whether the element may be checked for spelling errors. It may have the following values:

empty string or true, which indicates that the element should be, if possible, checked for spelling errors;
false, which indicates that the element should not be checked for spelling errors.
style
Contains CSS styling declarations to be applied to the element. Note that it is recommended for styles to be defined in a separate file or files. This attribute and the <style> element have mainly the purpose of allowing for quick styling, for example for testing purposes.

tabindex
An integer attribute indicating if the element can take input focus (is focusable), if it should participate to sequential keyboard navigation, and if so, at what position. It can take several values:

a negative value means that the element should be focusable, but should not be reachable via sequential keyboard navigation;
0 means that the element should be focusable and reachable via sequential keyboard navigation, but its relative order is defined by the platform convention;
a positive value means that the element should be focusable and reachable via sequential keyboard navigation; the order in which the elements are focused is the increasing value of the tabindex. If several elements share the same tabindex, their relative order follows their relative positions in the document.
title
Contains a text representing advisory information related to the element it belongs to. Such information can typically, but not necessarily, be presented to the user as a tooltip.

translate
An enumerated attribute that is used to specify whether an element's attribute values and the values of its Text node children are to be translated when the page is localized, or whether to leave them unchanged. It can have the following values:

empty string or yes, which indicates that the element will be translated.
no, which indicates that the element will not be translated.
virtualkeyboardpolicy Experimental
An enumerated attribute used to control the on-screen virtual keyboard behavior on devices such as tablets, mobile phones, or other devices where a hardware keyboard may not be available for elements that its content is editable (for example, it is an <input> or <textarea> element, or an element with the contenteditable attribute set).

auto or an empty string, which automatically shows the virtual keyboard when the element is focused or tapped.
manual, which decouples focus and tap on the element from the virtual keyboard's state.
writingsuggestions
An enumerated attribute indicating if browser-provided writing suggestions should be enabled under the scope of the element or not.

false, which disables the browser's writing suggestions.
true or an empty string, which enables writing suggestions.
List of global event handler attributes
HTML event handler attributes are discouraged; see HTML attribute reference for how they work.

While the attributes listed below apply to all elements, they are not useful on all elements. For example, onvolumechange HTML attribute is accepted by all elements and attaches an event listener for volumechange, but only media elements will ever receive a volumechange event fired by the browser. For other elements, you can only use EventTarget.dispatchEvent() to manually dispatch one. Some attributes can be specified on <body>, but they would instead listen to events on window.

onabort
onanimationcancel
onanimationend
onanimationiteration
onanimationstart
onauxclick
onbeforeinput
onbeforematch
onbeforetoggle
onblur
oncancel
oncanplay
oncanplaythrough
onchange
onclick
onclose
oncommand
oncontentvisibilityautostatechange
oncontextlost
oncontextmenu
oncontextrestored
oncopy
oncuechange
oncut
ondblclick
ondrag
ondragend
ondragenter
ondragleave
ondragover
ondragstart
ondrop
ondurationchange
onemptied
onended
onerror
onfocus
onfocusin
onfocusout
onformdata
onfullscreenchange
onfullscreenerror
ongesturechange Non-standard
ongestureend Non-standard
ongesturestart Non-standard
ongotpointercapture
oninput
oninvalid
onkeydown
onkeypress Deprecated
onkeyup
onload
onloadeddata
onloadedmetadata
onloadstart
onlostpointercapture
onmousedown
onmouseenter
onmouseleave
onmousemove
onmouseout
onmouseover
onmouseup
onmousewheel Deprecated Non-standard
onpaste
onpause
onplay
onplaying
onpointercancel
onpointerdown
onpointerenter
onpointerleave
onpointermove
onpointerout
onpointerover
onpointerrawupdate
onpointerup
onprogress
onratechange
onreset
onresize
onscroll
onscrollend
onscrollsnapchange Experimental
onscrollsnapchanging Experimental
onsecuritypolicyviolation
onseeked
onseeking
onselect
onselectionchange
onselectstart
onslotchange
onstalled
onsubmit
onsuspend
ontimeupdate
ontoggle
ontouchcancel
ontouchend
ontouchmove
ontouchstart
ontransitioncancel
ontransitionend
ontransitionrun
ontransitionstart
onvolumechange
onwaiting
onwebkitmouseforcechanged Non-standard
onwebkitmouseforcedown Non-standard
onwebkitmouseforceup Non-standard
onwebkitmouseforcewillbegin Non-standard
onwheel