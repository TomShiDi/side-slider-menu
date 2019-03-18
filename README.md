# side-slider-menu
This is a component design by vue 

## gif may cannot be viewed

![](https://i.imgur.com/NEdcmxL.gif)

## how to use it

    <side-slider-menu v-bind:menu-list="menus" head-image-src='/static/icon/head-icon-1.jpg'></side-slider-menu>

## params 

|param name| explanation|
|:----------:|:------------:|
|menu-list|the item in menu-list will become a menu-item|
|head-image-src|the url of head-image|

## data-form of menu-list
    menus: [{
        url: "#",
        icon: "fa-mars",
        text: "Mars"
      },
        {
          url: "#",
          icon: "fa-space-shuttle",
          text: "Space Shuttle"
        },
        {
          url: "#",
          icon: "fa-youtube-play",
          text: "Youtube Play"
        },
        {
          url: "#",
          icon: "fa-envira",
          text: "Envira"
        },
        {
          url: "#",
          icon: "fa-facebook",
          text: "Facebook"
        },
        {
          url: "#",
          icon: "fa-github",
          text: "Github"
        },
        {
          url: "#",
          icon: "fa-google-plus",
          text: "Google Plus"
        }
      ]



