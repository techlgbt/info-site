---
layout: default
title: Assets
permalink: /assets/
---

# Tech.LGBT Assets

The following assets for the tech.lgbt instance are available for reuse under the [Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0) Creative Commons License](https://creativecommons.org/licenses/by-nc-sa/4.0/).

You are free to:
- Share — copy and redistribute the material in any medium or format
- Adapt — remix, transform, and build upon the material

Under the following terms:
- Attribution — You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.
- NonCommercial — You may not use the material for commercial purposes.
- ShareAlike — If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original.
- No additional restrictions — You may not apply legal terms or technological measures that legally restrict others from doing anything the license permits.



## Attributions

Props to [@malle_yeno@tech.lgbt](https://tech.lgbt/@malle_yeno/) for the instance branding art!

## Images

### PNG
| description | image |

| ----------- | ----- |

| tech.lgbt logo in color with a thick black outline - PNG                          | ![tech.lgbt logo in color with a thick black outline - PNG](assets/images/techlgbt_color_black_outline.png)                            |
| tech.lgbt logo in color with a thick black outline and a thin white outline - PNG | ![tech.lgbt logo in color with a thick black outline and a thin white outline - PNG](assets/images/techlgbt_logo_bw_white_outline.png) |
| tech.lgbt logo in color - PNG                                                     | ![tech.lgbt logo in color - PNG](assets/images/techlgbt_logo_color.png)                                                                |
| tech.lgbt logo in color with a thin white outline - PNG                           | ![tech.lgbt logo in color with a thin white outline - PNG](assets/images/techlgbt_logo_white_outline.png)                              |

### SVG
| description                                              | image                                                                                          |
| -------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| tech.lgbt logo in color with a thick black outline - SVG | ![tech.lgbt logo in color with a thick black outline - SVG](assets/images/techlgbtlogo_bw.svg) |
| tech.lgbt logo in black and white - SVG                  | ![tech.lgbt logo in black and white - SVG](assets/images/techlgbtlogo_color.svg)               |
| tech.lgbt logo in color - SVG                            | ![tech.lgbt logo in color - SVG](assets/images/techlgbt_logo_emote.svg)                        |


## Custom CSS
This is not a complete list of customizations that we have made to our instance for the web interface, but they are some of the more notable changes that could be reused on other instances.

### Add underlines to links for accessibility
```
/* Why would we want to remove the underline from links? */
a.status-link:not(.mention) {
  text-decoration: underline;
}
```

### Align the instance art to the bottom center of the compose column
```
/* Bottom center that instance mascot! */
.drawer__inner__mastodon > img {
  -o-object-position: bottom center;
  object-position: bottom center;
  margin: 0 auto;
}
```

### Make Trends more visible on the screen
```
/* Let's make trends fit on the screen better */
.getting-started__trends .trends__item:nth-of-type(2),
.getting-started__trends .trends__item:nth-of-type(3) {
  display: flex !important;
}
```


### Make the "Why do you want to join?" more obvious on signup
```
/* Make the "Why do you want to join?" more obvious on signup */
#new_user .user_invite_request_text > label,
#new_user .user_invite_request_text > .hint {
  font-size: 16px;
  line-height: 1.5;
}
```


### Make DMs more distinct from other replies, with a progress pride flag sidebar
```
/* We're making DMs more obvious and queer! */
.status__wrapper-direct,
.status-direct.status__wrapper-reply,
.detailed-status-direct,
.status-direct.status--in-thread  {
  border-left: solid 5px transparent !important;
  position: relative;
}

.status__wrapper-direct::before,
.status-direct.status__wrapper-reply::before,
.detailed-status-direct::before,
.status-direct.status--in-thread::before {
  content: '';
  position: absolute;
  width: 5px;
  max-width: 5px;
  height: calc(100% - 16px);
  top: 8px; right: 0; bottom: 8px; left: 0;
  z-index: 1;
  margin-left: -5px;
  background: linear-gradient(to bottom, #000 0%, #784f16 15%, #e40303 20%, #ff8c00 30%, #ffed00 40%, #008026 50%, #004dff 60%, #750787 70%, #f6a8b7 85%, #5ccefa 100%);
  border-radius: 0 5px 5px 0;
}
```

### Increase emoji size on hover
```
/* Increase emoji size slightly on hover */
.status__content:not(.status__content--collapsed) {
  overflow: visible;
}

.status__content .emojione, .account__header__bio .emojione {
    transition:transform .2s, filter .2s;
}

.status__content .emojione:hover, .account__header__bio .emojione:hover {
    transform: scale(2.2);
    filter: drop-shadow(0 0 3px #202020);
}
```


### Make remove button on list modal more distinct
```
/* Make remove button on list modal more distinct */
.list-adder__lists .account__relationship button > .fa-times {
    color: #cc5959 !important;
}
```


### Make pinned statuses more noticeable on a profile
```
/* Make pinned statuses more noticeable */
.status[data-featured="true"] .status__prepend span {
  background-color: #d3dbe9;
  padding: 0.25rem 0.5rem;
  width: auto;
  display: inline-block;
  border: 1px solid rgba(40,44,55,.5);
  border-radius: 3px;
}

.skin-default .status[data-featured="true"] .status__prepend span {
  background-color: #424754;
  border: 1px solid rgba(217,225,232,.5);
  color: #fff;
}
```
