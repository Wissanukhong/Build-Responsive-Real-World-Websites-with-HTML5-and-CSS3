# Restaurants Project

## Table of contents

- [Restaurants Project](#restaurants-project)
  - [Table of contents](#table-of-contents)
    - [The 7 real-world steps to a fully functional website](#the-7-real-world-steps-to-a-fully-functional-website)
    - [setup project](#setup-project)
    - [What we will learn in this project](#what-we-will-learn-in-this-project)
    - [Header background](#header-background)
    - [How to make a button and hover effect](#how-to-make-a-button-and-hover-effect)
      - [html](#html)
      - [css](#css)

### The 7 real-world steps to a fully functional website

1. Define your project
2. Plan out everything
3. Sketch your ideas before you design
4. Design and develop your website
5. It's not done yet: optimization
6. Launch the masterpiece
7. Site maintenance

### setup project

![sepupProjcet](assest/resources/img/setupProject.png)

### What we will learn in this project

* html, header, nave, ul, li
* put text on an image: make image darker
* How to make that image as high as the browser iewport
* How to male a vertically a norizontally centered box
* How to design buttons

### Header background

**How to put iamge background**

``` css
header {
    background-image: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url(/02_restaurants/assest/resources/img/hero.jpg);
    background-size: cover;
    background-position: center;
    height: 100vh;
    color: #ffffff;
}
```

**How to set text center**

``` css
.hero-text-box {
    position: absolute;
    width: 1140px;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
```

**Result**

![center](assest/resources/img/center.png)

### How to make a button and hover effect

**Note :** 

* a:link = เชื่อมโยง  
* a:visited =  มาเยือน
* a:hover = เลื่อนเมาส์ใกล้
* a:active = การใช้งาน

#### html

``` html
 <header>
     <a class="btn btn-full" href="#">I’m hungry</a>
     <a class="btn btn-ghost" href="#">Show me more</a>
 </header>
```

1. สร้าง Element html ที่เราต้องการ ในที่นี่ใช้ Tag a เพื่อเป็นการคลิกเพื่อ Link ไปยังหน้าที่ต้องการ
2. สร้าง class ให้กับ Element ที่เราต้องการตกแต่ง ในที่นี่ใช้ btn
3. สร้าง child Element ที่เราต้องการตกแต่งให้ต่างจากที่มีอยู่ ในที่นี่ใช้ btn-full, btn-ghost

#### css 

`class="btn"` เพื่อเป็นการห่อหุ้มและการตกแต่งเบื้องต้น 

``` css
.btn:link,
.btn:visited {
    display: inline-block;
    padding: 10px 30px;
    font-weight: 300;
    text-decoration: none;
    border-radius: 200px;
    transition: background-color 0.2s, border 0.2s, color 0.2s;
}
```
