jQuery.smartModal
=================

A simple, lightweight jQuery modal plugin that's highly configurable, easy-to-use &amp; implement. Includes multiple implementation options like timed, automatic, sticky modals and more!

## Installation

Include the `jquery.smartModal.js` script *after* the jQuery library (unless you are packaging scripts somehow else):

```html
<script src='jquery.smartModal.js'></script>
```

**Do not include the script directly from GitHub**. The file is being served as text/plain and as such being blocked in Internet Explorer on Windows 7 for instance (because of the wrong MIME type). Bottom line: GitHub is not a CDN.

Add the CSS from the `jquery.smartModal.css` to your exisiting CSS or link to it directly:

```html
<link rel='stylesheet' href='jquery.smartModal.css'>
```

*Feel free to edit the CSS to suit your site's needs.*

## Usage

To get started, create your modal box by adding the class, `smartmodal` to it. You can define a *trigger class* by specifying the `id` attribute:

```html
<div class="smartmodal" id="triggerID">I'm a normal modal!</div>
<a href="#" class="triggerID">Click me</a> to trigger a normal modal.
```

Now when a user clicks on an element with the `triggerID` class, the modal will popup.

### Examples

A basic modal with a trigger:

```html
<div class="smartmodal" id="triggerID">I'm a normal modal!</div>
<a href="#" class="triggerID">Click me</a>
```

A modal that only get's shown once:

```html
<div class="smartmodal once" id="triggerID" data-expires="7">I'll only get shown once!</div>
<a href="#" class="triggerID">Click me</a>
```

A modal that disappears after so many seconds:

```html
<div class="smartmodal" id="triggerID" data-time="5">I'm a timed modal!</div>
<a href="#" class="triggerID">Click me</a>
```

A modal that disappears and shows the number of remaining seconds left:

```html
<div class="smartmodal" id="triggerID" data-time="10">I'm a timed modal <span class="sec"></span> seconds before I close!</div>
<a href="#" class="triggerID">Click me</a>
```

A modal that automatically pops up after the page loads:

```html
<div class="smartmodal auto">I'm automatic after page load!</div>
```

A modal that automatically pops up after a specified number of seconds:

```html
<div class="smartmodal auto" data-wait="10">I'm automatic after 10 seconds!</div>
```

A modal that can't be closed:

```html
<div class="smartmodal sticky auto">I can't be closed!</div>
```

## Configuration

*smartModal* allows for additional configuration options to allow for more flexibility and control over the modals.

### Modal Class Attribute Options

| Class | Description |
| --- | --- |
| `once` | Will only show the modal once per page load. [jquery.cookie](https://github.com/carhartl/jquery-cookie) will need to be loaded to enable modals to be shown once per visit. |
| `auto` | Enables the modal to popup automatically when the page is loaded. You can specify the `data-wait` attribute to set the number of seconds before the modal pops up. |
| `sticky` | Disables the ability to close the modal. |

### Modal Attribute Options

| Attribute | Description |
| --- | --- |
| `data-expires` | *Integer.* Specify the number of days until the cookie expires. |
| `data-time` | *Integer.* Specify the number of seconds the modal should be visible. |
| `data-wait` | *Integer.* Specify the number of seconds before the modal should popup. Should be used with the `auto` class. |

### Additional Modal Options

#### Show number of seconds remaining

You can display the number of remaining seconds until the modal disappears within the modal by applying the `sec` class to an element:

```html
<div class="smartmodal" data-time="10">I'm a timed modal <span class="sec"></span> seconds before I close!</div>
```

## Development

* Source hosted at [GitHub](https://github.com/bmarshall511/jquery-smartModal)
* Report issues, questions, feature requests on [GitHub Issues](https://github.com/bmarshall511/jquery-smartModal/issues)

## Authors

[Ben Marshall](http://www.benmarshall.me)