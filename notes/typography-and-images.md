# Text Rendering
Here's a question for you: if you took the exact same HTML and CSS and viewed it in two different browsers, would it appear identical? No! it's not identical. Why?

## Kerning
To the best of my understanding, the reason that the letter placement is slightly different between browsers is that the browsers implement different kerning algorithms.

Kerning refers to the spacing between individual characters. Characters are nudged left or right so that they "feel" right. This process is half art, half science.

Naturally, the browser doesn't do any kerning for monospaced fonts, since those characters need to align neatly into columns.

Using CSS, we can opt to disable kerning altogether with font-kerning: none, but we aren't offered any fine-grained control. letter-spacing, the property that allows us to increase/decrease the space between individual characters, acts as a "kerning multiplier" — it amplifies whatever kerning the browser decides on.

<br>

## Text Rasterization
To understand why the text looks so different across machines, we need to learn about rasterization and anti-aliasing.

In the very early days of computing, fonts were essentially collections of images. Each character was represented by a single picture. A "font" was a big repository of images, one for each character at each font size. This is known as a "bitmap font".

Bitmap fonts are still a thing today, but they're rare. It's much more common for fonts to use vector formats like ttf, otf, svg, and woff/woff2. In a vector font, we store a mathematical set of instructions for each character.

The main benefit to a vector font is that it can be scaled to any size without the letters becoming pixellated and blurry.

In order to turn a vector font into characters on a screen, though, the browser has to figure out which color to make each pixel, a process known as rasterization.

<br>

## Just what is “WebKit”, anyway?
WebKit is a browser rendering engine created by Apple, and used in Safari on MacOS, and all mobile browsers on iOS.

Early versions of Chrome and Opera also used WebKit, across all platforms (Windows, MacOS, Android). In 2013, Google announced that it was forking WebKit to create its own rendering engine, Blink.

Nowadays, Chrome and Microsoft Edge also use Blink as their rendering engine.

This means that just about every major browser has its roots in the WebKit codebase. This history helps explain why -webkit prefixes are supported in many non-Safari browsers!

<br>
<br>

# Images
The img HTML tag has two required attributes:

- `src`
- `alt`

`alt` is a property that allows you to specify "alternative text". It's meant to serve as a description of what the image contains.

You've probably heard that alt text is important. It provides critical context to folks who aren't able to see the images, whether because of a visual disability or because of a faulty network connection.

Not all images require alternative text. If the image is purely decorative and has no semantic value, you can specify alt="" to indicate that screen readers can ignore it.

## Writing effective alt text
There is a lot of confusion around how to write effective alternative text.

The goal with alternative text should be to convey the semantic meaning of the image to the user.

source: https://www.deque.com/blog/great-alt-text-introduction/