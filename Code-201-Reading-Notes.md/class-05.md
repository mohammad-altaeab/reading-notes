## images
***There are many reasons why you might want to add an image to a web page: you might want to include a logo, photograph, illustration, diagram, or chart.***
+ Include an image in your web pages using HTML
+  Pick which image format to use
+ Show an image at the right size
+ Optimize an image for use on the web to make pages load faster 
        A picture can say a thousand words, and great images help make the difference between an average-looking site and a really engaging one
#### Images should...
+ Be relevant
+ Convey information
+ Convey the right mood
+ Be instantly recognisable
+ Fit the color palette
#### Stock photos
+ [www.istockphoto.com](www.istockphoto.com)
+ [www.gettyimages.com](www.gettyimages.com)
+ [www.veer.com](www.veer.com)
+ [www.sxc.hu](www.sxc.hu)
+ [www.fotolia.com](www.fotolia.com)
### Storing Images on Your Site
**If you are building a site from scratch, it is good
practice to create a folder for all of the images
the site uses.**   
As a website grows, keeping images in a separate folder helps you understand how the site is organized. Here you can see an example of the files for a website; all of the images are
stored in a folder called **images**.
On a big site you might like to add subfolders inside the images folder. For example, images such as logos and buttons might sit in a folder called interface, product photographs might sit in a page called products, and images related to news might live in a folder called news. If you are using a content management system or blogging platform, there are usually tools built into the admin site that allow you to upload images, and the program will probably already have a separate folder for image files and any other uploads.
![https://zemez.io/wordpress/wp-content/uploads/sites/2/2017/07/1-69.png](https://zemez.io/wordpress/wp-content/uploads/sites/2/2017/07/1-69.png)

### Adding Images
```
<img src="images/quokka.jpg" alt="A family of
quokka" title="The quokka is an Australian
marsupial that is similar in size to the
domestic cat." />
```
### Height & Width of Images
```
<img src="images/quokka.jpg" alt="A family of
quokka" width="600" height="450" />
```
### Where to Place Images in Your Code
```
<img src="images/bird.gif" alt="Bird" width="100"
height="100" />
<p>There are around 10,000 living species of birds
that inhabit different ecosystems from the
Arctic to the Antarctic. Many species undertake
long distance annual migrations, and many more
perform shorter irregular journeys.</p>
<hr />
<p><img src="images/bird.gif" alt="Bird" width="100"
height="100" />There are around 10,000 living
species of birds that inhabit different
ecosystems from the Arctic to the Antarctic. Many
species undertake long distance annual
migrations, and many more perform shorter
irregular journeys.</p>
<hr />
<p>There are around 10,000 living species of birds
that inhabit different ecosystems from the
Arctic to the Antarctic.<img
src="images/bird.gif" alt="Bird" width="100"
height="100" />Many species undertake long
distance annual migrations, and many more perform
shorter irregular journeys.</p>
```
#### Old Code: Aligning Images Horizontally
```
<p><img src="images/bird.gif" alt="Bird" width="100"
height="100" align="left" />There are around
10,000 living species of birds that inhabit
different ecosystems from the Arctic to the
Antarctic. Many species undertake long distance
annual migrations, and many more perform shorter
irregular journeys.</p>
<hr />
<p><img src="images/bird.gif" alt="Bird" width="100"
height="100" align="right" />There are around
10,000 living species of birds that inhabit
different ecosystems from the Arctic to the
Antarctic. Many species undertake long distance
annual migrations, and many more perform shorter
irregular journeys.</p>
``` 
# Color
## Foreground Color

##### color
The color property allows you to specify the color of text inside an element. You can specify any color in CSS in one of three ways:
##### rgb values
These express colors in terms of how much red, green and blue are used to make it up. For example: rgb(100,100,90)
##### hex codes
These are six-digit codes that represent the amount of red, green and blue in a color, preceded by a pound or hash # sign. For example: #ee3e80
##### color names
There are 147 predefined color names that are recognized by browsers. For example: DarkCyan
```
/* color name */
h1 {
color: DarkCyan;}
/* hex code */
h2 {
color: #ee3e80;}
/* rgb value */
p {
color: rgb(100,100,90);}
```
##### background-color
CSS treats each HTML element as if it appears in a box, and the background-color property sets the color of the background for that box.
You can specify your choice of background color in the same three ways you can specify foreground colors: RGB values, hex codes, and color names (covered on the next page).
```
body {
background-color: rgb(200,200,200);}
h1 {
background-color: DarkCyan;}
h2 {
background-color: #ee3e80;}
p {
background-color: white;}
```
![https://cdn.educba.com/academy/wp-content/uploads/2020/03/CSS-Color-Codes.jpg.webp](https://cdn.educba.com/academy/wp-content/uploads/2020/03/CSS-Color-Codes.jpg.webp)
# Text
The formatting of your text can have a significant effect on how readable your pages are. As we look through these properties I will also give you some design tips on how to display your type.   


|Weight|Style|Stretch|
|------|-----|-------|
Light  |Normal|Extended|
Medium |*Italic*|Regular|
Bold   |**Oblique**|Condensed|
Black|      |    |



## Size of Type font-size
The font-size property enables
you to specify a size for the
font. There are several ways to
specify the size of a font. The
most common are:
pixels
Pixels are commonly used
because they allow web
designers very precise control
over how much space their text
takes up. The number of pixels is
followed by the letters px.
percentages
The default size of text in
browsers is 16px. So a size of
75% would be the equivalent of
12px, and 200% would be 32px.

```
body {
font-family: Arial, Verdana, sans-serif;
font-size: 12px;}
h1 {
font-size: 200%;}
h2 {
font-size: 1.3em;}
```
### Specifying Typefaces font-family
The font-family property
allows you to specify the
typeface that should be used for
any text inside the element(s) to
which a CSS rule applies.
The value of this property is the
name of the typeface you want
to use.
The people who are visiting
your site need the typeface you
have specified installed on their
computer in order for it to be
displayed.
You can specify a list of fonts
separated by commas so that,
if the user does not have your
first choice of typeface installed,
the browser can try to use an
alternative font from the list.


# **JPEG** vs **PNG** vs **GIF**
## TL;DR
Use JPEG format for all images that contain a natural scene or photograph where variation in colour and intensity is smooth. Use PNG format for any image that needs transparency or for images with text & objects with sharp contrast edges like logos. Use GIF format for images that contain animations

## **JPEG**
is a lossy compression specification that takes advantage of human perception. It can achieve compression ratios of 1:10 without any perceivable difference in quality. Beyond this, the compression artefacts become more prominent. Because JPEG compression works by averaging out colours of nearby pixels (read Discrete Cosine Transform), JPEG images are best suited for photographs and paintings of natural scenes where the variations in colour and intensity are smooth. However, if an image contains text or lines, where a sharp contrast between adjacent pixels is desired to highlight the proper shape, this lossy compression technique does not yield good results.

## **PNG**
 images support transparency in two ways — inserting an alpha channel that allows partial transparency or by declaring a single colour as transparent (index transparency). Partial transparency makes the edges blend smoothly into the background. PNG8 images (discussed in the “Colours” section below) can support only index transparency whereas PNG24 images can support alpha channel transparency.
## **GIF** 
images support transparency by declaring a single colour in the colour palette as transparent (index transparency). Because of absence of partial transparency, the edges (specially rounded or too-detailed edges) get a poor jagged effect. Though this can be solved to some extent using dithering, with improved PNG support, GIF is unsuitable for images with transparent backgrounds.
![](https://img.pagecloud.com/wAegMZSQrxtIBtV-i7jBCW-Ho7Y=/1000x0/filters:no_upscale()/blogmerge/cf67f56e-00e6-48c0-a1a4-31a8e3baf0de.jpeg)
![](https://miro.medium.com/max/400/1*ON0B-_gy1JK0YbGBOqkB6A.png)

