# Code Refactor Starter Code

## Get Started

- Clone your starter code (https://github.com/coding-boot-camp/urban-octo-telegram.git)
- Refactor the code

## Refactor the code in HTML

1. Give the title unique, concise and descriptive title <br>

```html
<head>
    <meta charset="UTF-8" />
    <link rel="stylesheet" href="./assets/css/style.css">
    <title>Horiseon Social Solution Services</title>
</head>
```

2. Create id = "search-engine-optimization" to make the link working and <br>
   Create alt Attribute: to provide alternative information for an image if a users for some reason commit view it or if the users use a screen reader. To meet the web accessibility

```html
<section>
        <div class="content">
            <!-- create new-class content-text and content-img -->
            <div id="search-engine-optimization" class="content-text content-img">
                <img src="./assets/images/search-engine-optimization.jpg" class="float-left" alt="search engine optimization photo" />              
            <div id="online-reputation-management" class="content-text content-img">
                <img src="./assets/images/online-reputation-management.jpg" class="float-right" alt="online reputation management photo" />               
            </div>
            <div id="social-media-marketing" class="content-text content-img">
                <img src="./assets/images/social-media-marketing.jpg" class="float-left" alt="social media marketing photo" />
            </div>
        </div>
        <!-- Benefits content section -->
        <div class="benefits">
            <!-- create new-class benefit-content and benefit-image-->
            <div class="benefit-content benefit-image">
                <h3>Lead Generation</h3>
                <img src="./assets/images/lead-generation.png" alt="lead generation icon" />
            </div>
            <div class="benefit-content benefit-image">
                <h3>Brand Awareness</h3>
                <img src="./assets/images/brand-awareness.png" alt="brand awareness icon" />
            </div>
            <div class="benefit-content benefit-image">
                <h3>Cost Management</h3>
                <img src="./assets/images/cost-management.png" alt="cost management icon" />
            </div>
        </div>
    </section>
```


3 Use header, nav, footer element itself instead of div

```html
<header>
        <h1>Hori<span class="seo">seo</span>n</h1>
        <nav>
            <ul>
                <li>
                    <a href="#search-engine-optimization">Search Engine Optimization</a>
                </li>
                <li>
                    <a href="#online-reputation-management">Online Reputation Management</a>
                </li>
                <li>
                    <a href="#social-media-marketing">Social Media Marketing</a>
                </li>
            </ul>
        </nav>
</header>
```

```html
<footer>
        <h2>Made with ❤️️ by Horiseon</h2>
        <p>
            &copy; 2019 Horiseon Social Solution Services, Inc.
        </p>
</footer>
```

## Refactor the code in CSS

- Delete all classes that contains the same properties and values and create new selector at once
- CSS selectors and properties are consolidated and organized 
- Contain properly commented

```css
* {
    box-sizing: border-box;
    padding: 0;
    margin: 0;
}

body {
    background-color: #d9dcd6;
    font-size: 16px;
    color: #ffffff;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
}

h2 {
    margin-bottom: 20px;
    font-size: 36px;
}

h3 {
    margin-bottom: 10px;
    text-align: center;
}

/* apply style to header section */

header {
    padding: 20px;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    background-color: #2a607c;
}

header h1 {
    display: inline-block;
    font-size: 48px;
}

header h1 .seo {
    color: #d9dcd6;
}

header nav {
    padding-top: 15px;
    margin-right: 20px;
    float: right;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    font-size: 20px;
}

header nav ul li {
    display: inline-block;
    margin-left: 25px;
    list-style-type: none;
}

a {
    color: #ffffff;
    text-decoration: none;
}

/* Hero section */

.hero {
    height: 800px;
    width: 100%;
    margin-bottom: 25px;
    background-image: url("../images/digital-marketing-meeting.jpg");
    background-size: cover;
    background-position: center;
}

.float-left {
    float: left;
    margin-right: 25px;
}

.float-right {
    float: right;
    margin-left: 25px;
}

/* Content section */

.content {
    width: 75%;
    display: inline-block;
    margin-left: 20px;
}

.benefits {
    margin-right: 20px;
    padding: 20px;
    clear: both;
    float: right;
    width: 20%;
    height: 100%;
    background-color: #2589bd;
}

.benefit-content {
    margin-bottom: 32px;
}

/* delete all these selector and create selector with benefit-content beacuse all them have the same properties and values.

.benefit-lead {
    margin-bottom: 32px;
    color: #ffffff;
}
.benefit-brand {
    margin-bottom: 32px;
    color: #ffffff;
}
.benefit-cost {
    margin-bottom: 32px;
    color: #ffffff;
} 

*/

.benefit-image img {
    display: block;
    margin: 10px auto;
    max-width: 150px;
}

/* create new-class benefit-image for image selector. They are all the same properties and values.

.benefit-lead img {
    display: block;
    margin: 10px auto;
    max-width: 150px;
}
.benefit-brand img {
    display: block;
    margin: 10px auto;
    max-width: 150px;
}
.benefit-cost img {
    display: block;
    margin: 10px auto;
    max-width: 150px;
} 

*/

.content-text {
    margin-bottom: 20px;
    padding: 50px;
    height: 300px;
    background-color: #0072bb;
}

/* create new-class content-text in HTML and use this css selector for content section.

.search-engine-optimization {
    margin-bottom: 20px;
    padding: 50px;
    height: 300px;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    background-color: #0072bb;
    color: #ffffff;
}
.online-reputation-management {
    margin-bottom: 20px;
    padding: 50px;
    height: 300px;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    background-color: #0072bb;
    color: #ffffff;
}
.social-media-marketing {
    margin-bottom: 20px;
    padding: 50px;
    height: 300px;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    background-color: #0072bb;
    color: #ffffff;
} 

*/

.content-img img {
    max-height: 200px;
}

/* create new-class content-img for image selector. They are all the same properties and values.

.search-engine-optimization img {
    max-height: 200px;
}
.online-reputation-management img {
    max-height: 200px;
}
.social-media-marketing img {
    max-height: 200px;
} 

*/

/* Footer section */

footer {
    padding: 30px;
    clear: both;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    text-align: center;
    color: #000;
}

footer h2 {
    font-size: 20px;
    margin-bottom: 0px;
}

/* They are all the same properties and values. Delete all them and create h2 selector by using all the same properties and values.

.search-engine-optimization h2 {
    margin-bottom: 20px;
    font-size: 36px;
}
.online-reputation-management h2 {
    margin-bottom: 20px;
    font-size: 36px;
}
.social-media-marketing h2 {
    margin-bottom: 20px;
    font-size: 36px;
} 


They are all the same properties and values. Delete all them and create h3 selector by using all the same properties and values.

.benefit-lead h3 {
    margin-bottom: 10px;
    text-align: center;
}
.benefit-brand h3 {
    margin-bottom: 10px;
    text-align: center;
}
.benefit-cost h3 {
    margin-bottom: 10px;
    text-align: center;
}

*/
```

## Submit the Challenge and Add to git and push

- Make sure links working and resemble the Mock-up
- After you've all changed and filled your README.md file, you should push it to your GitHub project:

```
git add .
git commit -m "descriptive message"
git push
```

## Contributing
This is a code refactor of the first class bootcamp project, and all feedback is welcome. Please open an issue, as the direction still needs some adjustments.

## Licensing

The code in this project is cloning from https://github.com/coding-boot-camp/urban-octo-telegram# code-refactor-challenge-1
