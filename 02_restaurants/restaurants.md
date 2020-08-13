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
      - [Icon](#icon)
      - [How to create underline and center](#how-to-create-underline-and-center)
      - [transition scale](#transition-scale)

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
4. กำหนดค่าต่างๆ ให้กับ Hover ว่าต้องการให้  Hover ทำงานอย่างไร 

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

`class="btn-full"` and `class="btn-ghost"` จะเป็นการกำหนดค่าให้กับ btn ต่างๆ ว่ามีขนาดเท่าไหร่ สีอะไร 

``` css
.btn-full:link,
.btn-full:visited {
    background-color: #f67f47;
    border: 1px solid #f67f47;
    color: #fff;
    margin-right: 15px;
}

.btn-ghost:link,
.btn-ghost:visited {
    border: 1px solid #f45d16;
    color: #f45d16;
}
```

`.btn:hover` เมื่อเราเอาเมาส์ไปคลิเราต้องการให้มีสีที่เปลี่ยนแปลง และมีการหน่วงระยะเวลาเพิ่มขึ้นเพื่อความสวยงาม

``` css
/*----------BUTTON HOVER----------*/
.btn:hover,
.btn:active {
    background-color: #f45d16;
}

.btn-full:hover,
.btn-full:active {
    background-color: #f45d16;
    border: 1px solid #f45d16;
    color: #fff;
}

.btn-ghost:hover,
.btn-ghost:active {
    background-color: #f45d16;
    border: 1px solid #f45d16;
    color: #fff;
}
```

#### Icon

[Ionicons](https://ionicons.com/v2/#cdn)

1. Install icon or link like CDN from the website
2. choose the icon on the website and get that class element

   
**Example code**

``` html
<div class="col span-1-of-4 box">
    <i class="icon-big ion-ios-stopwatch-outline"></i>
    <h3>Ready in 20 minutes</h3>
    <p>
        You're only twenty minutes away from your delicious and super healthy meals delivered right to your
        home. We work with the best chefs in each town to ensure that you're 100% happy.
    </p>
</div>
```

**optimization with css**
``` css 
.icon-big {

    font-size: 350%;
    display: block;
    color: #f67f47;

}

``` 

#### How to create underline and center

``` css
h2 {
    font-size: 180%;
    word-spacing: 2px;
    text-align: center;
    margin-bottom: 30px;
}

/* Underline  */
h2:after {
    display: block;
    height: 2px;
    background-color: #f67f47;
    content: "";
    width: 100px;
    margin: 0 auto;
    margin-top: 30px;
}
```

#### transition scale

``` css
.meal-photo {
    width: 100%;
    margin: 0;
    overflow: hidden;
    background-color: black;
}

/* Transition scale */
.meal-photo img {
    opacity: 0.7;
    width: 100%;
    height: auto;
    transform: scale(1.15);
    transition: transform 1s, opacity 0.5s;
}

.meal-photo img:hover {
    opacity: 1;
    transform: scale(1.03);
}
```
