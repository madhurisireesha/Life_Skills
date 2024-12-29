# 1.Box Model
The CSS Box MOdel is a fundamental concept that describes how HTML elements are structured and displayed on a webpage. The CSS box model is essentially a box that wraps around every HTML element.

## Components of CSS Box MOdel.
* Content
* Padding
* Border
* Margin

### Illustration of Box Model.
![Box Model](https://media.gcflearnfree.org/content/5ef2084faaf0ac46dc9c10be_06_23_2020/box_model.png)

#### Content:
This is the innermost part where text and images appear.THe size of the content area can be defined using width and height properties.
### Padding:
PAdding is the space between content and border.It creates space inside box,making sure the content isnot squeezed against the border.We can set different padding values for each side(top,right,bottom,left) using properties like padding-top, padding-right, padding-bottom, and padding-left.
### Border:
THe border wraps around the padding and content. It can have different styles (solid,dashed,dotted,etc),wdths,colors. WE can control each of the border individually using properties like border-top, border-right, border-bottom, and border-left.
### Margin:
Margin is the space outside the border. It seperates the element from other elemrnts on the page.
We can set different margin values for each side using properties like margin-top,margin-right,margin-bottom and margin-left.
#### Width and Height of an element.
Inorder to set the width and height of an element correctly in all browsers, we need to know hoew the box model works.
##### Important:When we set the width and height properties of an element with CSS, we just set the width and height of the content area. To calculate the total width and height of anelement, we must also include the padding and borders.
The total width of an element should be calculated as:

Total element width=width+left padding+right padding+left border+right border

THe total height of an element should be calculated as:
Total element height=height+top padding+top border+bottom border.

# 2.Inline Verses Block ELements:
* CSS displays different display types for elements,including block-levrl and inline-elements.
* Block-level elements start on a new line and take up the full width available, while inline elements do not start on new line and only take up as much width as necessary.  

|Inline ELements|Block Elements|
|---------------|--------------|
|Inline elements occupy only sufficient width required|Block elements occupy the full width irrespective of their sufficiency|
|Inline elements don't start in a new line|Block elements always start in a line|
|Inline elements allow other inline elements to sit behind|Block elements doesn't allow other elements to sit behind.|
|Inline elements don't have top and bottom margin|Block elements have top and bottom margin|
|Examples:h1,h6,div,hr,li,ul,ol,p,table|Examples:input.img,span,b,label.|

# 3.Positioning:Relative/Absolute:

The position property specifies the type of positioning method used for an element(static,relative,fixed,absolute or sticky).

## Relative Positioning:
* An element with position:relative; is positiioned relative to its normal position.
* We can use top,right,bottom and left properties to move the element from its original position.
* The space for the element in the normal document flow is preserved.
##### syntax:position:relative
##### Example:If we use top:10px; on a relatively positiioned element,it will move 10 pixels down from its original position.

#####Ex:
```
<!DOCTYPE html>
<html>
    <head>
    <style>
        div.relative{
            position:relative;
            left:50px;
            border:3px solid #73AD21;
        }
    </style>
    </head>
    <body>
    <h1>positon:relative;</h1>
    <div class="relative">
        This element has position:relative;
    </div>
</body>
</html>
```
![](https://media.geeksforgeeks.org/wp-content/uploads/20201208190504/re.PNG)

## Absolute Positioning:
* An element with position:absolute; is positioned relative to its nearest positioned anscestor(anything with a position other than static),or if none,relative to the initial containing block(usually the <html> element).
* It is taken out of the normal flow,so it doesn't affect the position of other elements.We can use top,right,bottom, and left properties to place the element exactly where we want.
##### Example:If we use top:10px;left:20px; on an absolutely positioned element, it will  be placed 10 pixe;s below and 20 pixels from the left edge of its containing element.
##### syntax:position:absolute.
###### Ex:
```
<!DOCTYPE html>
<html>

<head>
    <style>
        div.relative {
            position: relative;
            left: 50px;
            border: 3px solid #73AD21;
        }
    </style>
</head>

<body>
    <h1>position: relative;</h1>

    <div class="relative">
        This element has position:relative;
    </div>
</body>

</html>
```

![](https://media.geeksforgeeks.org/wp-content/uploads/20201208190503/abs.PNG)

# 4.CSS structural classes:
CSS structural classes that help organize and style the layout of the webpages
#### Container Classes:
This class is used to create a fixed-width container for the content. It centers the content and adds some paddiing.
* .container:Centers content with a fixed width.
* .container-fluid:Stretches content to full width of the viewport.

        .container{
            width:80%;
            margin:0 auto;
        }

        .container-fluid{
            width:100%;
        }
#### Row and Column Classes:
* .row:The .row class is used to create a horizontal group of colums.It ensures the columns are aligned properly.
* .Column:Columns are used inside rows to create a grid layout. Classes like .col, .col-6, .col-md-4, etc define the width of the columns.
##### Example:
```
<div class="row">
    <div class="col-6">Column 1</div>
    <div class="col-6">Column 2</div>
</div>
```
THe numbers (like 6) indicate how many parts of the 12-part grid the column should takr up..col-6 takes up half the row .col-4 takes up a third ,etc.
#### Flexbox/Grid Classes:
* d-flex: Applies display:flex;
* d-grid: Applies display:grid;
* justify:Centers items horizontally.
* .align-center:Centers items vertically.
###### Example:
    .d-flex{
        display:flex;
    }
    .justify-center{
        justify-content:center;
    }
    .align-center{
        align-items:center;
    }

#### Spacing Classes:
* .p-1,.p-2,.p-3:Padding classes(small to large)
* .m-1,.m-2,.m-3:Margin classes(small to large).
###### Example:
    .p-2{
        padding:1rem;
    }
    .m-2{
        margin:1rem;
    }
#### Text Utility Classes:
* .text-center:aligns text to center.
* .text-left:aligns text to the left.
* .text-right:aligns text to the right.

        .text-center{
            text-align:center;
        }

#### Visibility Classes:
* .hidden:It hides element.
* .visible:It makes the element visible.
* .d-none-It applies display:none;

###### Example:
    .hidden{
        visibility:hidden;
    }
    .d-none{
        display:none;
    }
#### Background and Border Classes:
* .bg-light:This class applies light background.
* .bg-dark:This class applies dark background.
* .border:This class adds simple border.
* .rounded:This class applies light border-radius.
###### Example:
    .bg-dark{
        background-color:#333;
    }
    .rounded{
        border-radius:8px;
    }
#### Width and Height Classes:
* .w-100:This class applies full width.
* .h-100:This class applies full height.
* .w-50:This class applies 50% width.
###### Example:
    .w-100{
        width:100%;
    }

# 5. Common CSS styling classes:
CSS styling classes to enhance the visual presentation of elements.
#### Text Styling:
* .text-bold:To makes the text bold.
* .text-underline:To make the underlined text.
* .text-lowercase:To make the text to lowercase.
* .text-uppercase:To make the text to uppercase.
* .text-italic:To make the text Italic.
* .text-capitalize:To make the first letter of each word capitalize.

###### Example:
    .text-bold{
        font-weight:bold;
    }
    .text-underline{
        text-decoration:underline;
    }
#### Color and Background:
* .text-primary:Applies primary text color(blue)
* text-secondary:A\Applies secondary text color(gray).
* .text-danger:Applies red text (error).
* .bg-primary:Applies primary background color.
* .bg-secondary:Applies Gray background.
* .bg-success:Applies green background(success).
* .bg-warning:Applies yellow background(warning).

###### Example:
    .text-primary{
        color:#007bff;
    }
    .bg-success{
        background-color:#28a745;
    }
#### Border and Outline:
* .border:.border adds a thin border.
* .border-none:This class removes the border.
* .border-rounded:This classs applies rounded corners.
* .border-thick:This class applies thick border.

###### Example:
    .border{
        border:2px solid red;
    }
    .border-rounded{
        border-radius:5px;
    }
#### Box Shadow and Effects:
* .shadow-sm:This class is used for applying small shadow.
* .shadow-ld:This class is used for applying large shadow.
* .box-shadow:This class is used for applying custom shadow effect.

##### Example:
    .shadow-sm{
        box-shadow:0 1px 3px black;
    }

#### Buttton Styling:
* .btn:This class is used for applying basic button styling.
* .btn-primary:This class is used for creating blue button.
* .btn-danger:This class is used for applying red button.
* .btn-outline:THis class is used for creating transparent button with a border.
##### Example:
    .btn{
        padding:10px;
        border:none;
    }
#### Display and Layout:
* .d-inline:This class is used for Inine display.
* .d-block:This class is used for Block display.
* .d-inline-block:This class is used for INline-block display.
* .d-flex:This class is used for creating flex container.
* .d-grid:This class is used for creating grid container.

###### EXample:
    .d-flex{
        display:flex;
    }
#### Positioning:
* .postion:relative-Used for displaying element position as relative.
* .postion:absolute-Used for displaying element position as absolute.
* .postion:fixed-Used for making the position of element as fixed.

#### Opacity and Visibility:
* .opacity:0 Fully transparent
* .opacity:50 50% opacity.
* .opacity:100 fully opaque
* .visible:Makes element visible.
* .hidden:Hides element.
###### Example:
.opacity-50{
    opacity:0.5;
} 

# 6.CSS Specificity:
Specificity determines which CSS rule is applied by the browser when multiple rules could apply to the same element.

##### Element and pseudo-elements:
* Target basic HTML tags like div,h1,and ::after with low specificity.
##### Class,Attribute,Pseudo-classes:
* Use .class.[attribute],and :hover to style group of elements with medium specifity.
##### ID Selectors:
* #id uniquely identifies and styles one element with high specificity.
##### Inline Styles:
* Directly applied styles(e.g. style="color:red") override most CSS rules with very high specificity.
##### !important:
* Forces a rule to apply, ignoring all specificity calculations but can complicate debugging.

### How can we calculate spedcificity:
##### Inline styles:10000
##### ID Selectors:100 points each
##### Class selectors, attribute selectors, and pseudo-classes:10 points each.
##### ELement selectors and pseudo-elements:1 point each.

#### Example:
#header .nav li a=100(ID)+10(class)+1(element)+1(element)=112
.main-content p=10(class)+1(element)=11
div =1(element)
The higher the specificity score, the more specfic the rule is, and it will be applied over the others.

# 7.CSS Responsive Queries:
CSS responsive queries, also known as media queries. THey help make our website look good on all devices by applying different styles based on the screen size or other characteristics.
### Common Media Query Syntax:

@media(condition){
    /* CSS rules here */
}


### Common Media Queries:

#### 1.Mobile First(small screens):
Targets small screens like phones for compact layouts(max-width:480px)
##### Example:
```
@media(max-width:480px){
    .container{
        font-size:14px;
    }
}
```
#### 2.Tablet(Medium Screens):

Adjusts styles for medium screens such as tablets(481px to 768px)
##### Example:
```
@media(min-width:481px) and (max-width:760px){
    .container{
        font-size:16px;
    }
}
```
#### 3.Desktop(Large Screens):
Applies styles to larger screens like desktops(min-width:769px).
##### Example:
```
@media(min-width:481px) and (max-width:768px){
    .container{
        font-size:16px;
    }
}
```

#### 4.High-Resolution Screens(min-resolution:2dppx):
Optimizes for retina and high-resolution displays.
##### Example:
```
@media(min-resolution:2dppx){
    img{
        max-width:100%;
    }
}
```
### Breakpoints:
* Breakpoints are specific scren widths where we change the design.
* 320px:Mobile devices(potrait)
* 480px:Mobile devices(landscape)
* 768px:Tablets(portrait)
* 1024px:Tablets(landscape) and small desktops.
* 1200px:Large desktops.

# 8.FlexBox/Grid:

Flexbox is best 1D layouts, aligning items in either a row or a column, while GRid excels 2D layouts,allowing control over both rows and columns simultaneously.

Flexbox is designed for one-dimensioanl layouts, either in a row (horizontal) or column(vertical) direction. It allows for flexible resizing and alignment of items within a container.
## Keyproperties of flexbox:
### display:flex:
This makes the container a flex container and its children(direct child elements) become flex items.
```
    .container{
        display:flex;
    }
```
### flex-direction:
Defines the direction in which the flex items are placed inside the flex container.The default is row(left to right).
* row(default):Items are laid out.
* column:Items are laid out vertically(top to bottom).
* row-reverse:Items are laid out horizontally in reverse order.
* column-reverse:Items are laid out vertically in reverse order.
```
.container{
    display:flex;
}
```
### flex-direction:
Defines the direction in which the flex items are placed inside the inside the flex container. The default is row(left to right).

* row(default):Items are laid out horizontally(left to right).
* column:Items are laid out vertically(top to bottom).
* row-reverse:Items are laid out horizontallly in reverse order.
* column-reverse:Items are laid out vertically in reverse order.
```
.container{
    display:flex;
    flex-direction:row;/*or column,row-reverse,column-reverse*/    

}
```

### justify-content:
Aligns the items along the main axis(horizontal if flex-direction) :row,vertical if flex-direction:column).
* flex-start:Aligns the items along the main axis (horizontal if flex-direction:row,vertical if flex-direction:column).
* flex-end:Aligns items to the end.
* stretch:Stretches items to fill the container.
```
.container{
    display;flex;
    align-items:center;
}
```
### align-self:
Allows individual flex items to be alogned differently from other items(overrides align-items).
```
.item{
    align-self:center;
}
```
### flex-wrap:
Specifies whether items should wrap onto multiple lines if there's not enough space in the container.

* nowrap(default):Items will not wrap and will be placed on one line.
* wrap:ITems will wrap to the next line when necessary.
* wrap-reverse:Items will wrap in reverse order.

#### Sample Code:

    .container{
        display:flex;
        flex-wrap:wrap;
    }
    


HTML:
```
    <div class="container">
        <div class="item">Item 1</div>
        <div class="item">Item 2</div>
        <div class="item">Item 3</div>
    </div>

```
CSS:

    .container{
        display:flex;
        justify-content:space-between;
        align-items:center;
        flex-wrap:wrap;
    }
    
    
    .item{
        width:30%;/*Each item takes 30% of the coantainer */
        padding:10px;
        background-color:lightblue;
        text-align:center;
    }
    

## CSS Grid Layout:
CSS Grid is atwo-dimensional layout system,meaning it allows you to arrange items both horizontally and vertically. It's ideal for more complex layouts that require precise control over both dimensions.

### display:grid:
This makes the container a grid container and its direct children become grid items.

    .container{
        display:grid;
    }

### grid-template-columns and grid-template-rows:
These properties define the number of columns and rows in the grid.WE can define fixed,fractional, or auto sizes for columns/rows.

    .container{
        display:grid;
        grid-template-columns:1fr 1fr;/*3 columns with different widths*/
        grid-template-rows:100px 200px;/*2 rows with fixed heights*/

    }


* 1fr:Represents a fraction of the available space in the container.
* auto:Allows items to size themselves based on their content.

### grid-gap(or gap):
Sets the gap between grid rows and columns.

    .container{
        display:grid;
        grid-template-colums:repeat(3,1fr);
        gap:20px;/*Space between grid items*/

    }


### grid-column and grid-row;
These properties allow we to place grid items in specific grid cells by specifying which column and row they should start ande end on.
* grid-column:start/end;
* grid-row:start/end;

#### Sample Code:

    .item{
        grid-column:1/3;/*spans from the first to the third column */
        grid-row:1/2;/*Spans the first row */

    }

#### justify-items:
Aligns grid items horizontally within their grid area.

* start:Align items to the start.
* center:Align items to the center.
* end:Align items to the end.
* stretch(default):Stretch items to fill the grid area.

#### Sample Code:
    .container{
        display:grid;
        justify-items:center;
    }

### align-items:
Aligns grid items vertically within their grid area.
* start:Align items to the top.
* center:Align items to the middle.
* end:Align items to the bottom.
* stretch(default):stretch items to fill the grid area.

#### Sample Code:
    .container{
        display:flex;
        justify-content:space-between;
        align-content:center;
    }

Example:
HTML:

```
<div class="container">
    <div class="item">Item 1</div>
    <div class="item">Item 2<</div>
    <div class="item">Item 3</div>
</div>
```
    .container{
        display:grid;
        grid-template-columns:repeat(3,1fr);/* equal-width columns*/
        gap:20px;/* Gap between items */
        
    }

# 9.Common Header Meta tags:
* Meta tags in HTML are used for SEO, responsiveness, and better control over page behaviour.
* Meta tags in the <head> section of an HTML document provide metadata about the webpage, which can affect how it appears in search engines,social media, and browsers, Here are some commonly used meta tags:
### Character Set(character encoding)
Specifies the character encoding for the document.

    <meta charset="UTF-8">

### Viewport(Responsive DEsign):
Helps make the website mobile-friendly by controlling layout on different screens sizes.

    <meta name="viewport" content="width=device-width,initial-scale=1.0">
### Description:
Provides a brief description of the webpage content, often shown in search engine results.

    <meta name="description" content="short description upto 100 characters">
### Keywords:
Lists keywords related to the page(less commonly used today for SEO purposes).

    <meta name="keywords" content="HTML, CSS, Javascript, Meta Tags">
### Author:
Specifies the author of the webpage.

    <meta name="author" content="name of author">
### Robots:
Controls how search engine crawlers index the page and follow its links.

    <meta name="robots" content="index.follow">

# 10.Hyperlinks:
* Hyperlinks allows users to navigate to different web pages, sections, or edxternal resources.
* We use <a> tag to create hyperlink.
### Syntax:
<a href="url">link text</a>
The most important attribute of the <a> element is the href attribute, which indicates the link's destination.
The link text is the part that will be visible to the reader.
Clicking on the link text, will send the reader to the specified URL address.
### HTML Links-The target Attribute:
By default, the linked page will be displayed in the current browser window. To change this we must specify another target for the link.
The target attribute specifies where to open the linked document.
THe target attribute can have one of the following values:
* _self:Default, Opens the document in the same window/tab as it was clicked.
* _blank:Opens the document in a new window or tab.
* _parent:Opens the document in the parent frame.
* _top:Opens the document in the full body of the window.
##### Example:
    <a href="https://www.w3schools.com/" target="_blank">Visit W3Schools!</a> 

#### Absolute URLs versus Relative URLs

An absolute URL provides the complete address of a webpage or file on the internet,including the protocol "http:// or https://" domain, and path to the resource.
    eg. https://www.example.com/images/logo.png

Relative URLs:
A relative URL specifies the path to a resource about the current document's path or the base URL of the website, without the domain nanme and protocol.'

    Example: If the current URL is "https://www.example.com/about/team.html", a relative URL to another page in the same directory like contact.html would simply be contact.html.





























      
    
























