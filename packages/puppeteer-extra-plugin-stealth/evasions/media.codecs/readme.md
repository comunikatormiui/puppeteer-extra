## API

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

#### Table of Contents

- [class: Plugin](#class-plugin)
- [parseInput(arg)](#parseinputarg)

### class: [Plugin](https://github.com/berstend/puppeteer-extra/blob/6d452681fe832a6d864616ee8fa79134ebd19be7/packages/puppeteer-extra-plugin-stealth/evasions/media.codecs/index.js#L9-L85)

- `opts` (optional, default `{}`)

**Extends: PuppeteerExtraPlugin**

Fix Chromium not reporting "probably" to codecs like `videoEl.canPlayType('video/mp4; codecs="avc1.42E01E"')`.
(Chromium doesn't support proprietary codecs, only Chrome does)

---

### [parseInput(arg)](https://github.com/berstend/puppeteer-extra/blob/6d452681fe832a6d864616ee8fa79134ebd19be7/packages/puppeteer-extra-plugin-stealth/evasions/media.codecs/index.js#L31-L45)

- `arg` **[String](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)**

Input might look funky, we need to normalize it so e.g. whitespace isn't an issue for our spoofing.

Example:

```javascript
video / webm
codecs = 'vp8, vorbis'
video / mp4
codecs = 'avc1.42E01E'
audio / x - m4a
audio / ogg
codecs = 'vorbis'
```

---
