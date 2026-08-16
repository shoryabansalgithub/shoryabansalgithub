## Shorya Bansal

I build web tools that have something technically real underneath a small surface. Mostly TypeScript and Next.js, usually with a design problem sitting in the middle of the engineering one.

---

### [font-download](https://github.com/shoryabansalgithub/font-download) &nbsp;·&nbsp; [font-stealer.vercel.app](https://font-stealer.vercel.app)

Paste any URL, get every font the page uses, preview it live, download WOFF / WOFF2 / TTF / OTF. Around 200k people have used it.

The part worth reading is the "find a free alternative" path. It parses the font binary with opentype.js and reduces each face to a 15-dimension feature vector: x-height and cap-height ratios, stroke contrast, an italic angle, a serif score computed from the glyph outlines, and roundness measured as curve commands over total path commands. Matching is a weighted nearest-neighbour search against a precomputed database of 1,920 Google Fonts families. The weights are hand-tuned rather than learned, and the reasoning is in the source: `isMonospace` is 3.0 because monospace is a different universe, `serifScore` is 1.8 because serif versus sans is the biggest visual class a reader notices, `xHeightRatio` is 1.3 because it is the strongest proportional differentiator. Iconic families like Helvetica and SF Pro bypass the metric entirely and hit a hand-curated override table, because for those, curation beats the algorithm.

It is a tool called font-stealer that ships a licensing disclaimer and a built-in path to legal alternatives.

`Next.js 15 App Router` `TypeScript` `opentype.js` `Tailwind` `Framer Motion`

### [Metagame](https://github.com/shoryabansalgithub/hack-ideas-) &nbsp;·&nbsp; [hack-ideas-nu.vercel.app](https://hack-ideas-nu.vercel.app)

An evidence-grounded hackathon strategist built on a hand-assembled dataset of 176 events and 412 verified winning projects, distilled into 23 named patterns. Ships the same knowledge three ways: an agent skill, an MCP server over stdio, and a web app. The dataset has an integrity validator and the MCP server has a smoke test, because a dataset nobody checks is a dataset nobody should trust.

`TypeScript` `MCP` `Next.js`

### [texty](https://github.com/shoryabansalgithub/texty)

A Chrome extension that puts a typography inspection layer over any page. The browser already knows the font, size, line-height, colour and spacing of every piece of text on screen. Texty hands that to you on hover, instead of making you open DevTools and translate implementation detail back into design detail.

`Chrome MV3` `vanilla JS`

---

### Open source

One merged contribution to a major project: [client-side rate limiting and caching for the Planet API](https://github.com/sugarlabs/musicblocks/pull/5098) in **sugarlabs/musicblocks**, merged Feb 2026.

Attempts at other orgs that did not land: sanitizing API-supplied HTML with DOMPurify in [openfoodfacts-explorer](https://github.com/openfoodfacts/openfoodfacts-explorer/pulls?q=author%3Ashoryabansalgithub), and a JavaScript-to-TypeScript module migration in [CircuitVerse/cv-frontend-vue](https://github.com/CircuitVerse/cv-frontend-vue/pulls?q=author%3Ashoryabansalgithub).

I have more merged PRs than that, but most of them are team work on a collaborator's product, which is not the same thing, so I am not counting them here.

---

### Not public

Most of what I build is not. Some of it is worth mentioning: a design-capture system spanning a Chrome MV3 extension, a Next.js canvas app and an MCP server that share a written integration contract, so a coding agent can read the design vault directly; a shadcn-style component registry; and a multi-tenant retail operations app on MySQL and Redis. Happy to walk through any of it.

Reach me at [bansalshorya13@gmail.com](mailto:bansalshorya13@gmail.com).
