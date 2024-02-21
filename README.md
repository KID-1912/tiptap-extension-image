# tiptap-extension-image

<h3 align="center">
    Make tiptap support image tags to provide predefined styles for img.
</h3>

<br/>

<p align="center">
  <a href="https://www.npmjs.com/package/tiptap-extension-image">
    <img
     alt="NPM URL"
     src="https://img.shields.io/badge/npm-tiptapExtensionImage?logo=npm">
  </a>
  <img
     alt="version"
     src="https://img.shields.io/badge/version-1.0.0-blue">
</p>

<br>

---

## Install

```shell
npm install tiptap-extension-image -S
```

## Usage

```js
import Image from "tiptap-extension-image";

const editor = new Editor({
  element: document.querySelector(".editor"),
  extensions: [
    StarterKit,
    Image.configure({ inline: true, allowBase64: true })
  ],
});

editor
  .chain()
  .focus()
  .setImage({
    src: dataString,
  })
  .run();
```

Supports the presence of the style attribute of the inserted img as `baseStyle`.

```js
const html = `<img style="width: 100%; display: inline-block" src="/88f84b8.png"/>`

editor
  .chain()
  .focus()
  .insertContent(html, {
    parseOptions: {
      preserveWhitespace: false,
    },
  })
  .run();
// baseStyle: "width: 100%; display: inline-block"
```

## Relations

**@tiptap/extension-image:** https://github.com/ueberdosis/tiptap/tree/develop/packages/extension-image

**tiptap-appmsg-editor:** https://github.com/KID-1912/tiptap-appmsg-editor
