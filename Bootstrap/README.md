# freecodecamp - Front End Development Libraries - Bootstrap

Bootstrap is a front-end framework used to design responsive web pages and applications.
It takes a mobile-first approach to web development and includes pre-built CSS styles and classes,
in addition to some JavaScript features.

In this course, you will learn how to create responsive websites with Bootstrap,
and will use the classes it has to style buttons, images, forms, navigation and other common elements.


### Use responsive design with Bootstrap fluid containers

Use responsive design with Bootstrap fluid containers
In the HTML5 and CSS section of freeCodeCamp we built a Cat Photos application.

Now let's get back to her.
This time, we will style using the popular responsive CSS framework known as Bootstrap.

Bootstrap will discover the width of the screen and respond by resizing the HTML elements -
hence the name responsive design.

With a responsive design, there is no need to design a mobile version of your website.
It will look good on devices with screens of any width.

You can include Bootstrap in any application by adding the following code to the top of the HTML:

```html
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css"
       integrity="sha384-BVYiiSIFeK1dGmJRAkycuHAHRg32OmUcww7on3RYdg4Va+PmSTsz/K68vbdEjh4u"
       crossorigin="anonymous"/>
```

In this case, we have already added it for you to this behind-the-scenes page.
Note that using the > or /> tag to close the link tag is acceptable.

To start, we must nest all of the HTML (except the link tag and the style element) in a div element with the
container-fluid class.

```html
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css"
       integrity="sha384-BVYiiSIFeK1dGmJRAkycuHAHRg32OmUcww7on3RYdg4Va+PmSTsz/K68vbdEjh4u"
       crossorigin="anonymous"/>
<link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css"/>
<style>
     .red-text {
         color: red;
     }

     h2 {
         font-family: Lobster, Monospace;
     }

     P {
         font-size: 16px;
         font-family: Monospace;
     }

     .thick-green-border {
         border-color: green;
         border-width: 10px;
         border-style: solid;
         border-radius: 50%;
     }

     .smaller-image {
         width: 100px;
     }
</style>
<div class="container-fluid">
     <h2 class="red-text">CatPhotoApp</h2>

     <p>Click here for <a href="#">cat photos</a>.</p>

     <a href="#">
         <img class="smaller-image thick-green-border"
              src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg"
              alt="A cute orange cat lying on its back.">
     </a>

     <p>Things cats love:</p>
     <ul>
         <li>cat nip</li>
         <li>laser pointers</li>
         <li>lasagna</li>
     </ul>
     <p>Top 3 things cats hate:</p>
     <ol>
         <li>flea treatment</li>
         <li>thunder</li>
         <li>other cats</li>
     </ol>
     <form action="https://freecatphotoapp.com/submit-cat-photo">
         <label><input type="radio" name="indoor-outdoor"> Indoor</label>
         <label><input type="radio" name="indoor-outdoor"> Outdoor</label>
         <label><input type="checkbox" name="personality"> Loving</label>
         <label><input type="checkbox" name="personality"> Lazy</label>
         <label><input type="checkbox" name="personality"> Crazy</label>
         <input type="text" placeholder="cat photo URL" required>
         <button type="submit">Submit</button>
     </form>
</div>
```

Tests:
- The div element must have the container-fluid class.
- Waiting: The div element must have a closing tag.
- Waiting: All HTML elements after the closing style tag must be nested within .container-fluid.


### Make images mobile responsive

First, add a new image below the existing one.
Set your src attribute to `https://cdn.freecodecamp.org/curriculum/cat-photo-app/running-cats.jpg`.

It would be great if this image could be exactly the size of our cell phone screen.

Fortunately, with Bootstrap, all we need to do is add the `img-responsive` class to our image.
Do this, and the image should fit perfectly within the width of the page.

```html
<img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/running-cats.jpg" class="img-responsive"/>
```

Tests
- You must have a total of two images.
- The new image must be below the old one and have the img-responsive class.
- The new image must not have the smaller-image class.
- The new image must have a src of `https://cdn.freecodecamp.org/curriculum/cat-photo-app/running-cats.jpg`.
- The new img element must have a closing tag.


### Center text with Bootstrap

Now that we're using Bootstrap, we can center our header elements to make them look better.
All we need to do is add the text-center class to our h2 element.

Remember that you can add multiple classes to the same element by separating each one with a space, like this:

```html
<h2 class="red-text text-center">your text</h2>
```

Tests:
- The h2 element must be centered when applying the `text-center` class;
- The h2 element must still have the class `red-text`.


### Create a Bootstrap button

Bootstrap has its own styles for button elements, which look much better than those
buttons in pure HTML.

Create a new button element below the large kitten photo.
Give it the btn and btn-default classes, as well as the Like text.

```html
<button class="btn btn-default">Like</button>
```

Tests:
- You must create a new button element with the text Like.
- The new button must have two classes: btn and btn-default.
- All button elements must have closing tags.


### Create a Bootstrap block element button

Typically, button elements with the btn and btn-default classes are only as large as the text they contain.
they contain.

For example:
```html
<button class="btn btn-default">Submit</button>
```
This button would only be as wide as the word Submit.

By making them block elements with the additional btn-block class, the button will stretch to fill the entire space
horizontal of your page and any following elements will flow to a new line below the block.

```html
<button class="btn btn-default btn-block">Submit</button>
```

This button would take up 100% of the available width.

Note that these buttons still need the btn class.

Add the Bootstrap btn-block class to the Bootstrap button.

```html
<button class="btn btn-default btn-block">Like</button>
```

Tests:
- The button must still have the btn and btn-default classes.
- The button must have the btn-block class.
- All your button elements must have closing tags.


### Try the rainbow-colored Bootstrap button

The btn-primary class has the main color that you will use in your app.
It's useful for highlighting actions you want the user to do.

Replace Bootstrap's btn-default class with btn-primary in the button.

Note that this button still needs the btn and btn-block classes.

```html
<button class="btn btn-primary btn-block">Like</button>
```

Tests:
- The button must have the btn-primary class.
- The button must still have the btn and btn-block classes.
- All button elements must have closing tags.


### Call optional actions with btn-info

Bootstrap comes with several predefined button colors.
The btn-info class is used to draw attention to optional actions that the user can take.

Create a block-level Bootstrap button below the Like button with the text Info, adding to it the
Bootstrap btn-info class.

Note that these buttons still need the btn and btn-block classes.

```html
<button class="btn btn-info btn-block">Info</button>
```

Tests
- You must create a new button element with the text Info.
- Both Bootstrap buttons must have the btn and btn-block classes.
- The new button must have the btn-info class.
- All button elements must have closing tags.


### Warn users about a dangerous action with btn-danger

Bootstrap comes with several predefined button colors.
The btn-danger class is the button color you will use to notify your users that the button performs a
destructive action, such as deleting a cat photo.

Create a button with the text Delete and give it the class btn-danger.

Note that these buttons still need the btn and btn-block classes.

```html
<button class="btn btn-danger btn-block">Delete</button>
```

Tests:
- You must create a new button element with the text Delete.
- All Bootstrap buttons must have the btn and btn-block classes.
- The new button must have the btn-danger class.
- All button elements must have closing tags.


### Use Bootstrap Grid to place elements side by side

Bootstrap uses the responsive 12-column grid system, which makes it super easy to place elements in rows
and specify each relative width of an element.

Most Bootstrap classes can be applied to a div element.

Bootstrap has different column width attributes, which are used depending on the width
of the user's screen.

For example, cell phones have narrow screens, while laptops have wider screens.

Take Bootstrap's `col-md-*` class as an example.
Here, md means medium, and * is a number specifying how many columns wide the element should be.
In this case, the column width of an element on a medium-sized screen, such as a laptop, is being specified.

In the Cat Photos app we are building, we will use `col-xs-*`, where xs means extra small
(like an extra-small mobile phone screen), and * is a number of columns specifying how many columns of
width the element must have.

Place the Like, Info, and Delete buttons side by side by nesting all three in a `<div class="row">` element.
Then place each of them inside a `<div class="col-xs-4">` element.

The row class is applied to the div. The buttons themselves can be nested inside it.

```html
<div class="row">
     <div class="col-xs-4">
         <button class="btn btn-primary btn-block">Like</button>
     </div>
      <div class="col-xs-4">
         <button class="btn btn-info btn-block">Info</button>
     </div>
     <div class="col-xs-4">
         <button class="btn btn-danger btn-block">Delete</button>
     </div>
</div>
```

Tests:
- The buttons must be nested within the same div element with the row class.
- Each of the Bootstrap buttons must be nested within its own div element with class col-xs-4.
- Each of the button elements must have a closing tag.
- Each of the div elements must have a closing tag.


### Clean up custom CSS for Bootstrap

We can clean up our code and make the cat photo app look more conventional by using the
Bootstrap's native styles instead of the custom styles we created earlier.

Don't worry - there will be plenty of time to customize our CSS later.

Delete the `.red-text`, `p`, and `.smaller-image` CSS declarations from the style element so that the only remaining declarations
in the style element are `h2` and `thick-green-border`.

Then delete the p element that contains a dead link.
After that, remove the `red-text` class from the h2 element and replace it with Bootstrap's `text-primary` class.

Finally, remove the `smaller-image` class from the first img element and replace it with the `img-responsive` class.

Tests:
- The h2 element should no longer contain the red-text class.
- The h2 element must now have the text-primary class.
- Paragraph elements should no longer use the Monospace font.
- The smaller-image class must be removed from the top image.
- You must add the img-responsive class to the top image.


### Use a span to point to elements on the same line

You can use spans to create elements on the same line.
Remember when we used the btn-block class to make the button fill the entire row?

This illustrates the difference between an "inline" element and a "block" element.

By using the inline span element, you can place several elements on the same line, and even style different
parts of the same line differently.

Using a span element, nest the word love inside the p element that currently has the text Things cats love.
Then give the span the class `text-danger` to make the text red.

Here is how you would do it for the p element that has the text Top 3 things cats hate:

```html
<p>Top 3 things cats <span class="text-danger">hate:</span></p>
```

```html
<p>Things cats <span class="text-danger">love</span>:</p>
```

Tests:
- The span element must be inside the p element.
- The span element must only have the text love.
- The span element must have the text-danger class.
- The span element must have a closing tag.


### Create a custom title

Let's make a simple title for our cat photo by placing the title and the relaxing cat image on the same line.

Remember: Bootstrap uses the responsive grid system, which makes it easy to place elements in line and
specify each relative width of an element.

Most Bootstrap classes can be applied to a div element.

Nest your first image and its h2 element inside a single `<div class="row">` element.

Nest your h2 element inside a `<div class="col-xs-8">` and your image inside a `<div class="col-xs-4">`
so that they are on the same line.

Did you notice how the image is now the exact size to fit the text?

```html
<div class="row">
     <div class="col-xs-8">
         <h2 class="text-primary text-center">CatPhotoApp</h2>
     </div>
     <div class="col-xs-4">
         <a href="#">
             <img class="img-responsive thick-green-border"
                  src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg"
                  alt="A cute orange cat lying on its back."/>
         </a>
     </div>
</div>
```

Tests:
- The h2 element and the topmost img element must be nested together inside a div element with the row class.
- The top img element must be nested inside a div with class col-xs-4.
- The h2 element must be nested inside a div with class col-xs-8.
- All div elements must have closing tags.

### Add Font Awesome icons to our buttons

Add Font Awesome icons to our buttons
Font Awesome is a convenient icon library.

These icons can be web fonts or vector graphics.
These icons are treated just like fonts.
You can specify their size using pixels, and they will take on the font size of their parent elements in the HTML.

You can include Font Awesome in any application by adding the following code to the top of your HTML:

```html
<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.8.1/css/all.css"
       integrity="sha384-50oBUHEmvpQ+1lW4y57PTFmhCaXp0ML5d60M1M7uH2+nqUivzIebhndOJK28anvf"
       crossorigin="anonymous">
```
In this case, we have already added it for you to this behind-the-scenes page.

The i element was originally used to make other elements italic, but is now commonly used for icons.

You can add Font Awesome classes to the i element to turn it into an icon, for example:
```html
<i class="fas fa-info-circle"></i>
```

Note that the span element is also acceptable for use with icons.

Use Font Awesome to add a thumbs-up icon to the like button,
giving it an i element with classes `fas` and `fa-thumbs-up`.
Make sure to keep the Like text next to the icon.

```html
<button class="btn btn-primary btn-block">
     <i class="fas e fa-thumbs-up">Like</i>
</button>
```

Tests:
- You must add an i element with the fas and fa-thumbs-up classes.
- The fa-thumbs-up icon must be located inside the Like button.
- The i element must be inside the new button element.
- The icon element must have a closing tag.


### Add Font Awesome icons to all buttons

Font Awesome is a convenient icon library.
These icons can be web fonts or vector graphics.
These icons are treated just like fonts.
You can specify their size using pixels, and they will take on the font size of their parent elements in the HTML.

Use Font Awesome to add an info-circle icon to the info button and a trash icon to the delete button.

Note: You can use the i or span elements to complete this challenge.

```html
<div class="col-xs-4">
     <button class="btn btn-info btn-block">
         <i class="fas fa-info-circle">Info</i>
     </button>
</div>
<div class="col-xs-4">
     <button class="btn btn-danger btn-block">
         <i class="fas fa-trash">Delete</i>
     </button>
</div>
```

Tests:
- You must add a `<i class="fas fa-info-circle"></i>` inside the info button element.
- You must add a `<i class="fas fa-trash"></i>` inside the delete button element.
- Each of the i elements must have a closing tag and `<i class="fas fa-thumbs-up"></i>` is in the element of
  like button.


### Create responsive style radio buttons

You can use Bootstrap's `col-xs-*` classes in form elements too!
This way, our option buttons will be symmetrically distributed across the page,
regardless of the width of the screen resolution.

Nest radio buttons inside a `<div class="row">` element.
Then nest each of them inside a `<div class="col-xs-6">` element.

Note: As a reminder, radio buttons are input elements of type radio.

```html
<div class="row">
     <div class="col-xs-6">
         <label><input type="radio" name="indoor-outdoor"> Indoor</label>
     </div>
     <div class="col-xs-6">
         <label><input type="radio" name="indoor-outdoor"> Outdoor</label>
     </div>
</div>
```

Tests:
- All radio buttons must be nested inside a div with class `row`.
- Each of the radio buttons must be nested in their own div with the class `col-xs-6`.
- All div elements must have closing tags.


### Understand responsive checkboxes

Since Bootstrap's `col-xs-*` classes are applicable to all form elements,
you can also use them in checkboxes!

This way, the selection boxes will be symmetrically distributed across the page,
regardless of the width of the screen resolution.

Nest the three checkboxes in a `<div class="row">` element.
Then nest each of them in the `<div class="col-xs-4">` element.

```html
<div class="row">
     <div class="col-xs-4">
         <label><input type="checkbox" name="personality"> Loving</label>
     </div>
     <div class="col-xs-4">
         <label><input type="checkbox" name="personality"> Lazy</label>
     </div>
     <div class="col-xs-4">
         <label><input type="checkbox" name="personality"> Crazy</label>
     </div>
</div>
```

Tests:
- All checkboxes must be nested inside a div with the row class.
- Each of the checkboxes must be nested within its own div with class `col-xs-4`.
- All div elements must have closing tags.


### Style text inputs as form controls

You can add the Font Awesome `fa-paper-plane` icon by including `<i class="fa fa-paper-plane"></i>`
inside the submit button element.

Give the form's text input field the class `form-control`.
Give the form submit button the classes `btn btn-primary`.
Also give this button the Font Awesome icon `fa-paper-plane`.

All text in the elements `<input>`, `<textarea>` and `<select>` with the class `.form-control` have a width of 100%.


```html
<input type="text" placeholder="cat photo URL" class="form-control" required/>
<button type="submit" class="btn btn-primary">
     <i class="fa fa-paper-plane">Submit</i>
</button>
```

Tests:
- The submit button on your form must have the class `btn btn-primary`.
- You must add a `<i class="fa fa-paper-plane"></i>` inside the submit button element.
- The text input in the form must have the class `form-control`.
- All your i elements must have a closing tag.


### Align form elements responsively with Bootstrap

Now let's put the input and the form submit button on the same line.
We will do this the same way we did before:
using a div element with the row class and other div elements within the first div using the `col-xs-*` class.

Nest the text input and form submit button inside a div with class `row`.
Nest the form input text inside a div with class `col-xs-7`.
Nest the form submit button in a div with class `col-xs-5`.

This is the last challenge we will do for our cat photo app for now.
We hope you enjoyed learning Font Awesome, Bootstrap, and responsive design!

```html
<div class="row">
     <div class="col-xs-7">
         <input type="text" placeholder="cat photo URL" class="form-control" required/>
     </div>
     <div class="col-xs-5">
         <button type="submit" class="btn btn-primary">
             <i class="fa fa-paper-plane">Submit</i>
         </button>
     </div>
</div>
```

Tests:
- The submit button and form text input must be nested inside a div with class `row`.
- The form's text input must be nested inside a div with class `col-xs-7`.
- The form submit button must be nested inside a div with class `col-xs-5`.
- All div elements must have closing tags.


### Create a title with Bootstrap

Now let's build something from scratch to practice our HTML, CSS and Bootstrap skills.

Let's build a jQuery playground, which we will soon put to use in jQuery challenges.

To get started, create an h3 element, with the text jQuery Playground.

Give the h3 element a color with the text-primary class, and center it with the Bootstrap text-center class.

```html
<h3 class="text-primary text-center">jQuery Playground</h3>
```

Tests
- You must add an h3 element to the page.
- The h3 element must have a closing tag.
- The h3 element must be colored when applying the `text-primary` class
- The h3 element must be centered when applying the `text-center` class
- The h3 element must have the text jQuery Playground.

### Host our page in a Bootstrap fluid container div

Now, let's make sure all the content on your page is mobile responsive.

Let's nest our h3 element inside a div element with class `container-fluid`.

```html
<div class="container-fluid">
     <h3 class="text-primary text-center">jQuery Playground</h3>
</div>
```

Tests:
- The div element must have the container-fluid class.
- Each of your div elements must have closing tags.
- The h3 element must be nesting inside a div element.


### Create a Bootstrap row

Now let's create a Bootstrap row for our inline elements.

Create a div element below the h3 tag, with class `row`.

```html
```

Tests:
- You must add the div element below the h3 element.
- The div element must have the row class
- The row div must be nested inside the container-fluid div
- The div element must have a closing tag.


### Split your Bootstrap line

Now that we have a Bootstrap row, let's split it into two columns to house our elements.

Create two div elements within the row, both with the class `col-xs-6`.

```html
<div class="row">
     <div class="col-xs-6"></div>
     <div class="col-xs-6"></div>
</div>
```

Tests:
- Two `div class="col-xs-6"` elements must be nested inside the `div class="row"` element.
- All div elements must have closing tags.


### Create Bootstrap wells

Bootstrap has a class called well that can create a visual sense of depth for your columns.

Nest a div element with the class well inside each of your col-xs-6 div elements.

```html
     <div class="row">
     <div class="col-xs-6">
         <div class="well"></div>
     </div>
     <div class="col-xs-6">
         <div class="well"></div>
     </div>
</div>
```

Tests:
- You must add a div element with class `well` inside each of the `div elements with class col-xs-6`
- Both div elements with class `col-xs-6` must be nested inside the `div element with class row`.
- All div elements must have closing tags.


### Add elements to wells in Bootstrap

Now we are at the depth of several div elements in each column of our row.
This is as deep as we need to go. Now we can add our button elements.

Nest three button elements inside each of the div elements containing the class name well.

```html
<div class="col-xs-6">
     <div class="well">
         <button></button>
         <button></button>
         <button></button>
     </div>
</div>
<div class="col-xs-6">
     <div class="well">
         <button></button>
         <button></button>
         <button></button>
     </div>
</div>
```

Tests:
- Three button elements must be nested inside each of the div elements with the well class.
- You must have a total of 6 button elements.
- All button elements must have closing tags.


### Apply default Bootstrap button styling

Bootstrap has another button class called btn-default.

Apply both the btn and btn-default classes to each of the button elements.

```html
  <div class="row">
     <div class="col-xs-6">
         <div class="well">
             <button class="btn btn-default"></button>
             <button class="btn btn-default"></button>
             <button class="btn btn-default"></button>
         </div>
     </div>
     <div class="col-xs-6">
         <div class="well">
             <button class="btn btn-default"></button>
             <button class="btn btn-default"></button>
             <button class="btn btn-default"></button>
         </div>
     </div>
</div>
```

Tests:
- You must apply the btn class to each of the button elements.
- You must apply the btn-default class to each of the button elements.


### Create a class to select with jQuery Selectors

Not all classes need to have corresponding CSS.
Sometimes we create classes just for the purpose of selecting these elements more easily using jQuery.

Give each of the button elements the target class.

```html
<div class="row">
     <div class="col-xs-6">
         <div class="well">
             <button class="btn btn-default target"></button>
             <button class="btn btn-default target"></button>
             <button class="btn btn-default target"></button>
         </div>
     </div>
     <div class="col-xs-6">
         <div class="well">
             <button class="btn btn-default target"></button>
             <button class="btn btn-default target"></button>
             <button class="btn btn-default target"></button>
         </div>
     </div>
</div>
```

Tests
- You must apply the target class to each of the button elements.


## Add id attributes to Bootstrap elements

Remember that in addition to class attributes, you can give each of your elements an id attribute.

Each id must be unique for a specific element and used only once per page.

Let's give a unique id to each of our div elements with class well.

Remember that you can give an element an id like this:

```html
<div class="well" id="center-well">
```

Give the well on the left the id left-well. Give the well on the right the id right-well.

```html
<div class="well" id="left-well"></div>
<div class="well" id="right-well"></div>
```

Tests:
- The well on the left must have the id left-well.
- The well on the right must have the id right-well.


### Label Bootstrap wells

To make it clear, let's label our two wells with their ids.

Above the left well, inside the col-xs-6 div element, add an h4 element with the text #left-well.

Above the right well, inside the col-xs-6 div element, add an h4 element with the text #right-well.

```html
<h4>#left-well</h4>
<h4>#right-well</h4>
```

Tests:
- You must add an h4 element to each of the `<div class="col-xs-6">` elements.
- An h4 element must have the text #left-well.
- An h4 element must have the text #right-well.
- All h4 elements must have closing tags.


### Give each element a unique id

We also want to be able to use jQuery to select each button by its unique id.

Give each of the buttons a unique id, starting with target1 and ending with target6.

Make sure target1 through target3 are in #left-well, and target4 through target6 are in #right-well.

```html
<div class="row">
     <div class="col-xs-6">
         <h4>#left-well</h4>
         <div class="well" id="left-well">
             <button class="btn btn-default target" id="target1"></button>
             <button class="btn btn-default target" id="target2"></button>
             <button class="btn btn-default target" id="target3"></button>
         </div>
     </div>
     <div class="col-xs-6">
         <h4>#right-well</h4>
         <div class="well" id="right-well">
             <button class="btn btn-default target" id="target4"></button>
             <button class="btn btn-default target" id="target5"></button>
             <button class="btn btn-default target" id="target6"></button>
         </div>
     </div>
</div>
```

Tests:
- A button element must have the id target1.
- A button element must have the id target2.
- A button element must have the id target3.
- A button element must have the id target4.
- A button element must have the id target5.
- A button element must have the id target6.


### Label Bootstrap buttons

Just like we did with our wells, we also want to give our buttons a label.

Give each of your button elements the text that corresponds to your id selector.

```html
         <div class="row">
     <div class="col-xs-6">
         <h4>#left-well</h4>
         <div class="well" id="left-well">
             <button class="btn btn-default target" id="target1">#target1</button>
             <button class="btn btn-default target" id="target2">#target2</button>
             <button class="btn btn-default target" id="target3">#target3</button>
         </div>
     </div>
     <div class="col-xs-6">
         <h4>#right-well</h4>
         <div class="well" id="right-well">
             <button class="btn btn-default target" id="target4">#target4</button>
             <button class="btn btn-default target" id="target5">#target5</button>
             <button class="btn btn-default target" id="target6">#target6</button>
         </div>
     </div>
</div>
```

Tests:
- The button element with the id target1 must have the text #target1.
- The button element with the id target2 must have the text #target2.
- The button element with the id target3 must have the text #target3.
- The button element with the id target4 must have the text #target4.
- Your button element with the id target5 must have the text #target5.
- Your button element with the id target6 must have the text #target6.


### Use comments to make code clearer

When we start using jQuery, we will modify HTML elements without the need
to actually change them in the HTML.

Let's make sure everyone knows that they shouldn't actually modify any of this code directly.

Remember that you can ` start a comment with <!-- and end a comment with -->`

Add a comment at the top of the HTML that says Code below this line should not be changed

```html
<!--Code below this line should not be changed-->
```

Tests:
- You must start a `comment with <!--` at the top of the HTML.
- The comment must have the text Code below this line should not be changed.
- You must close the `comment with -->`.
- You must have the same number of opening and closing comments.


## Comments
Import bootstrap with the link tag;
Place all the body code inside a div with the class `container-fluid`;
Create responsive images with the `img-responsive` class;
Create button with class `btn` followed by other classes for color and block;
Create div with row class, and inside them place div with classes to define the columns whose total should be 12.


## References
https://www.freecodecamp.org/learn/front-end-development-libraries/