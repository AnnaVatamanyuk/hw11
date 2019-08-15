#hw11

This file describe the structure and operation of the project, the principles of page layout.

---

##This project has the following structure:

- index.html;

- fonts - project fonts directory;

- img - directory with images for the project;

- css file directory:

  - style.css - a file that contains the main project styles;
  - et-line.css - a file containing the styles for the project icons;
  - slick.css and slick-theme.css - files with basic styles for slider section;

- file folder:
 
  - script.js - which contains the main functions for the project;
  - slick.min.js - function for slider section.

---

This page consists of: header, 12 sections and footer. Each section has its own classes and is stylized according to the layout.

---
###Default classes

Class **container** - having a fixed width and lateral indentation, sed in almost all sections of the project.

```/*css*/
.container {
    margin: 0 auto;
    width: 100%;
    max-width: 1200px;
    padding: 0 15px;
}
```

Class **default_section** - adds top and bottom indentation in blocks.

```/*css*/
.default_section {
    padding: 140px 0;
}
```

Class **.btn_default** - sets the styling for the buttons on the page.

```/*css*/
.btn_default {
    background-color: #cfcfcf;
    color: #111;
    text-transform: uppercase;
    line-height: 1;
    padding: 15px 40px;
}
```

Class **text_center** - center alignment.

```/*css*/
.text_center {
    text-align: center;
}
```

The size, thickness and name of the page font:

```/*css*/
body {
    font: 400 15px/1.7333 'open_sanslight', sans-serif;
}

h2{
     font-size:18px;
 }
 
 h3{
     font-size:15px;
 }
```

---

In the **about_section** section of the **usr_info** class we use transformation

```/*css*/
.user_info img:hover {
    filter: none;
    transform: rotateZ(360deg);
}
```

---

**services_section** has a **services_tabs** class, which is responsible for tab work, also in the mobile version of the website, we connect the **click ()** function to quickly scroll through the content.

```javascript
 $('.services_list li a').click(function () {
        if ($(window).width() <= 425) {
            var self = this;
            $([document.documentElement, document.body]).animate({
                scrollTop: $($(self).attr('href')).offset().top
            }, 500);
        }
    })
```

---

**maps_section**, a section using google maps. Its zoom in on hover.

```/*css*/
.map_holder:hover iframe{
    background-color: transparent;
    transform: scale(1.3);
}
```
