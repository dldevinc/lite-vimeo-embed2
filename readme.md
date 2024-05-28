> 🙋 Using YouTube? Check out the original [lite-youtube-embed](https://github.com/paulirish/lite-youtube-embed).

# Lite Vimeo Embed [![NPM lite-vimeo-embed2 package](https://img.shields.io/npm/v/lite-vimeo-embed2.svg)](https://npmjs.org/package/lite-vimeo-embed2)

> #### Renders faster than a sneeze.

Provide videos with a supercharged focus on visual performance.
This custom element renders just like the real thing but approximately 224× faster.

Demo: https://dldevinc.github.io/lite-vimeo-embed2/

## Comparison

| Normal `<iframe>` Vimeo embed                                                                                                                                                                                                                                                                                                                                                                                                       | `lite-vimeo-embed`                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![Screen Shot 2019-11-03 at 5 23 50 PM](https://user-images.githubusercontent.com/39191/68095560-5c930d00-fe5f-11e9-8104-e73e77a21287.png)   ![Screen Shot 2019-11-03 at 5 21 05 PM](https://user-images.githubusercontent.com/39191/68095562-5d2ba380-fe5f-11e9-8b5f-18f451b0716d.png)  ![Screen Shot 2019-11-03 at 5 19 35 PM](https://user-images.githubusercontent.com/39191/68095565-5d2ba380-fe5f-11e9-835d-85d37df71f52.png) | ![Screen Shot 2019-11-03 at 5 23 27 PM](https://user-images.githubusercontent.com/39191/68095561-5d2ba380-fe5f-11e9-9393-e2206a64c8bf.png) ![Screen Shot 2019-11-03 at 5 20 55 PM](https://user-images.githubusercontent.com/39191/68095563-5d2ba380-fe5f-11e9-8f9a-f5c4a774cd56.png)  ![Screen Shot 2019-11-03 at 5 20 16 PM](https://user-images.githubusercontent.com/39191/68095564-5d2ba380-fe5f-11e9-908f-7e12eab8b2ad.png) |

## Basic usage

Use the [`lite-vimeo-embed2` npm package](https://www.npmjs.com/package/lite-vimeo-embed2) or download from this repo and use `src/`.

To use the custom element you will need to:

1. Include the stylesheet within your application
1. Include the script as well
1. Use the `lite-vimeo` tag via HTML or JS.
1. Be happy that you're providing a better user experience to your visitors

```html
<!-- Include the CSS & JS. (This could be direct from the package or bundled) -->
<link rel="stylesheet" href="node_modules/lite-vimeo-embed2/src/lite-vimeo-embed.css" />

<script src="node_modules/lite-vimeo-embed2/src/lite-vimeo-embed.js"></script>

<!-- Use the element. You may use it before the lite-vimeo-embed2 JS is executed. -->
<lite-vimeo videoid="347119375" playlabel="Play: Sample Video"></lite-vimeo>
```

## Pro-usage: load w/ JS deferred (aka progressive enhancement)

Use this as your HTML, load the script asynchronously, and let the JS progressively enhance it.

```html
<lite-vimeo videoid="347119375" style="background-image: url('https://i.vimeocdn.com/video/797382244-0106ae13e902e09d0f02d8f404fa80581f38d1b8b7846b3f8e87ef391ffb8c99-d_640');">
  <a href="https://vimeo.com/347119375" class="lvm-playbtn" title="Play Video">
    <span class="lvm-visually-hidden">Play Video: Sample Video</span>
  </a>
</lite-vimeo>
```

[Demo: progressive enhancement](https://dldevinc.github.io/lite-vimeo-embed2/variants/pe.html)

## Add a video title

If you want to display a title prior to loading the full embed, set the `title` attribute:
```html
<lite-vimeo videoid="347119375" title="Sample Video"></lite-vimeo>
```

[Demo: visible title](https://dldevinc.github.io/lite-vimeo-embed2/variants/title.html)

### Custom Player Parameters

Vimeo supports a variety of [player parameters](https://help.vimeo.com/hc/en-us/articles/12426260232977-Player-parameters-overview)
to control the iframe's behavior and appearance. These may be applied by using the `params` attribute.

```html
<!-- Example to show a video player without controls, starting at 10s in, ending at 20s,
     with modest branding *and* enabling the JS API -->
<lite-vimeo videoid="347119375" params="controls=0&loop=1#t=10s"></lite-vimeo>
```

Note that lite-vimeo uses `autoplay=1` by default.

[Demo: Custom player parameters](https://dldevinc.github.io/lite-vimeo-embed2/variants/params.html)
