# Animation

# ABOUT
ANIMISTA IS A PLACE WHERE YOU CAN PLAY WITH A COLLECTION OF PRE-MADE CSS ANIMATIONS, TWEAK THEM AND GET ONLY THOSE YOU WILL ACTUALLY USE.

Animista started out as a small side-project of mine. As I was increasingly using CSS animations, I thought it would come in handy to have them organised in a meaningful and accessible way so that they can be easily reused on different projects.

The idea was to create a playground of a sorts where a collection of pre-made animations could be tested and tweaked before actually using them. Seeing how various options like easing, delay, duration and others affect the animation proved to be very useful. And basically that is how Animista was born.

I have been using Animista for a while now and I hope some of you will find it useful as well. It is still very much a work in progress and hopefully it will evolve over the time :)

Huge thanks to @sergej108 for helping me out with the JS part and for supporting and encouraging me to publish this project. Animista wouldn't be possible without him.

Get in touch
Should you decide to use Animista for your next cool project or have any suggestions/feedback it would be awesome if you gave me a shout at cssanimista(at)gmail.com!


# Animate Css
# Animate.css is a library of ready-to-use, cross-browser animations for use in your web projects. Great for emphasis, home pages, sliders, and attention-guiding hints.

Installation and Usage
Installing
Install with npm:

$ npm install animate.css --save
Or install with Yarn (this will only work with appropriate tooling like Webpack, Parcel, etc. If you are not using any tool for packing or bundling your code, you can simply use the CDN method below):

$ yarn add animate.css
Import it into your file:

import 'animate.css';
Or add it directly to your webpage using a CDN:

<head>
  <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css"
  />
</head>
Basic usage
After installing Animate.css, add the class animate__animated to an element, along with any of the animation names (don't forget the animate__ prefix!):

<h1 class="animate__animated animate__bounce">An animated element</h1>
That's it! You've got a CSS animated element. Super!

Animations can improve the UX of an interface, but keep in mind that they can also get in the way of your users! Please read the best practices and gotchas sections to bring your web-things to life in the best way possible.

Using @keyframes
Even though the library provides you a few helper classes like the animated class to get you up running quickly, you can directly use the provided animations keyframes. This provides a flexible way to use Animate.css with your current projects without having to refactor your HTML code.

Example:

.my-element {
  display: inline-block;
  margin: 0 0.5rem;

  animation: bounce; /* referring directly to the animation's @keyframe declaration */
  animation-duration: 2s; /* don't forget to set a duration! */
}
Be aware that some animations are dependent on the animation-timing property set on the animation's class. Changing or not declaring it might lead to unexpected results.

CSS Custom Properties (CSS Variables)
Since version 4, Animate.css uses custom properties (also known as CSS variables) to define the animation's duration, delay, and iterations. This makes Animate.css very flexible and customizable. Need to change an animation duration? Just set a new value globally or locally.

Example:

/* This only changes this particular animation duration */
.animate__animated.animate__bounce {
  --animate-duration: 2s;
}

/* This changes all the animations globally */
:root {
  --animate-duration: 800ms;
  --animate-delay: 0.9s;
}
Custom properties also make it easy to change all your animation's time-constrained properties on the fly. It means that you can have a slow-motion or time-lapse effect with a javascript one-liner:

// All animations will take twice the time to accomplish
document.documentElement.style.setProperty('--animate-duration', '2s');

// All animations will take half the time to accomplish
document.documentElement.style.setProperty('--animate-duration', '.5s');
Even though some aging browsers do not support custom properties, Animate.css provides a proper fallback, widening its support for any browser that supports CSS animations.

Edit this on GitHub

Utility Classes
Animate.css comes packed with a few utility classes to simplify its use.

Delay classes
You can add delays directly on the element's class attribute, just like this:

<div class="animate__animated animate__bounce animate__delay-2s">Example</div>
Animate.css provides the following delays:

Class name	Default delay time
animate__delay-2s	2s
animate__delay-3s	3s
animate__delay-4s	4s
animate__delay-5s	5s
The provided delays are from 1 to 5 seconds. You can customize them setting the --animate-delay property to a longer or a shorter duration:

/* All delay classes will take 2x longer to start */
:root {
  --animate-delay: 2s;
}

/* All delay classes will take half the time to start */
:root {
  --animate-delay: 0.5s;
}