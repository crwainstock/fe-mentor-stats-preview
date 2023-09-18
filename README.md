# Frontend Mentor - Stats preview card component

![Design preview for the Stats preview card component coding challenge](.//Project%20Requirements//design/desktop-preview.jpg)

## 🌍 Overview

This component is a beginner project from [Frontend Mentor](https://www.frontendmentor.io/challenges/stats-preview-card-component-8JqbgoU62?ref=challenge-roadmap). I wanted to build this project to stay connected to my CSS skills.

As with any skill, if you don't use it, you lose it. 😫 So this little build is a part of my ongoing professional development.

You can see a couple of other little, cutie builds [here](https://github.com/crwainstock/fe-mentor-qr) and [here](https://github.com/crwainstock/fe-mentor-3-column-preview-card) and [here](https://github.com/crwainstock/fe-mentor-single-price-grid) and [here](https://github.com/crwainstock/fe-mentor-order-summary)

## 🛠️ Technologies & Dependencies

This component was built with HTML and vanilla CSS. No dependencies! 🥳 I also used [PerfectPixel](https://www.welldonecode.com/perfectpixel/) and the [Eye Dropper/Color Picker](https://eyedropper.org/) browser extensions to help with the build.

I deployed the component with Netlify, though, so check that out [here](https://mellow-faun-84807a.netlify.app/).

## 🤔 Reflection

This build allowed me to use some of the same tools I've used in the last couple of Frontend Mentor builds, namely using grid to put the layout together. But, this build also required that I use a couple of new things.

First, I used the [::before pseudo-element](https://developer.mozilla.org/en-US/docs/Web/CSS/::before) for the first time in this build to implement the purple overlay on top of the image. The image provided is black and white, so I created a pseudo-element that basically sits on top of the image using CSS.

```
.img-container::before {
  content: "";
  position: absolute;
  width: 100%;
  height: 98%;
  background-color: hsla(277, 64%, 61%, 0.509);
  z-index: 1;
  border-radius: 8px 8px 0 0;
}
```

It took a little trial and error to get the overlay as close as it is to the image in the brief, and I think the color is still slightly lighter than it needs to be. But I'm happy with how it turned out, overall.

The brief also provided two different images (slightly different sizes, I believe) for mobile and desktop views. In order to use both images, I tried to use the [<picture> and <source> elements in HTML](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/picture), but I didn't quite get it to work as intended yet.

```
      <div class="img-container">
        <picture>
          <source
            media="(min-width:660px)"
            srcset="./Project Requirements/images/image-header-desktop.jpg"
          />
          <img
            src="./Project Requirements/images/image-header-mobile.jpg"
            alt="people working at a desk"
          />
        </picture>
      </div>
```

My first thought when tasked with using two different images for the different screen sizes is to use conditional rendering with JavaScript. But, this build is just HTML and CSS, so I wanted to try to implement it without using JavaScript.

## 👀 Demo & Live Version

Check out the live version of this component [here](https://mellow-faun-84807a.netlify.app/).
