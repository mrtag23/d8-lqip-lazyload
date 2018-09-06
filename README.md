# Drupal8 lazy loading with LQIP technique.

> This is a really simple demonstration on how to implement lazy loading for images with LQIP approach in a D8 project.


## Prerequisites
- [**lazysizes**](https://github.com/aFarkas/lazysizes) will provide all lazy loading functionality.
- Drupal's `image styles` will generate our lqip(low quality image placeholder).

## Tools used in this example
-  `SCSS` as CSS preprocessor.
- [**mappy breakpoints**](https://github.com/zellwk/mappy-breakpoints) for media rules.

## Implementation
1. Create the `lazysizes` library so we can call it only when we need it. 
2. Create an image style that will generate a scaled image with 15px width.
3. Override `responsive-image.html.twig` template.
4. Write a preprocess function for `responsive_image` where we remove default `src` attribute and substitute it with `data-src` or other required by `lazysizes` attributes.
5. Define basic styles for new picture template and add some additional magic for blurry effects and transitions.
