# vuepress-theme-carbon

<p align="center"><img align="center" height="300px" src="https://github.com/lupas/vuepress-theme-carbon/blob/master/misc/hero_vuepress-theme-carbon.png?raw=true"/></p>

<p align="center">
  <a href="https://www.npmjs.com/package/vuepress-theme-carbon"><img src="https://badgen.net/npm/dm/vuepress-theme-carbon" alt="Downloads"></a>
  <a href="https://www.npmjs.com/package/vuepress-theme-carbon"><img src="https://badgen.net/npm/v/vuepress-theme-carbon" alt="Version"></a>
  <a href="https://www.npmjs.com/package/vuepress-theme-carbon"><img src="https://badgen.net/npm/license/vuepress-theme-carbon" alt="License"></a>
 </p>
</p>

> Inspired from the _Carbon Ads_ integration in the official [vuepress documentation](https://vuepress.vuejs.org/guide/) and its source code, this theme extends the default vuepress theme with a __Carbon Ads__ slot in the sidebar.

## Demo / Example

* [@nuxtjs/firebase Documentation](https://firebase.nuxtjs.org/guide/getting-started/) 

## Install

```bash
yarn add vuepress-theme-carbon -D
# OR npm install vuepress-theme-carbon -D
```

## Usage

```js
// .vuepress/config.js
module.exports = {
  theme: 'carbon',
  themeConfig: {
    // Your ad-id and placement from your Carbon Ads tag;
    carbonAds: {
      serve: "yourServeId",
      placement: "yourPlacementLabel"
    },
    // All the other themeConfig options from the default theme.
  }
}
```

## Credits

Thanks to [Vuepress](https://github.com/vuejs/vuepress).

## License

MIT - [Pascal Luther](https://github.com/lupas)