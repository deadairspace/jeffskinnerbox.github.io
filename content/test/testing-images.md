Title: Testing: Images
Slug: testing-images
Status: hidden

## The Back Story
Python Markdown comes with several [extras][02], and one of the extension supported is called [CodeHilite][03].
To get this all to work, you must include something like this in your `pelicanconf.py` file:

```
# List of the extensions that the Markdown processor will use.
MD_EXTENSIONS = ['extra', 'codehilite(noclasses=True, pygments_style=manni, guess_lang=False)']
```

## Markdown Image Formatting
Markdown uses a syntax like `[text](link-URL)` to support hyperlinks in text.
It uses a similar syntax for images, like

```no-highlight
![alt text](image-URL "hover text")
[![alt text](image-URL "hover text")](link-URL)
```

Here is an example when using a file stored within the pelican directory structure
(also hover the mouse over the image to see the text):

```

![Wolf Trap]({filename}/images/wolf_trap.jpg "Wolf Trap, 1645 Trap Road Vienna, Virginia, 22182")
```

![Wolf Trap]({filename}/images/wolf_trap.jpg "Wolf Trap, 1645 Trap Road Vienna, Virginia, 22182")

Here is an another example using a file from the web
(also hover the mouse over the image to see the text):

```md
Full image is placed here
![alt text](http://content.answcdn.com/main/content/img/oxford/Oxford_Mind/0198162246.skinner-box.1.jpg "Skinner Box:  operant conditioning cage")
Lorem ipsum dolor sit amet, ....
```

_Full image is placed here_
![alt text](http://content.answcdn.com/main/content/img/oxford/Oxford_Mind/0198162246.skinner-box.1.jpg "Skinner Box:  operant conditioning cage")
_[Lorem ipsum][01] dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum._
_Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum._

You can also access some of the HTML features

```html
Lorem ipsum dolor sit amet, ....
[<img src="http://www.google.com.au/images/nav_logo7.png">](http://google.com.au/)
Lorem ipsum dolor sit amet, ....
```

_[Lorem ipsum][01] dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum._
[<img src="http://www.google.com.au/images/nav_logo7.png">](http://google.com.au/)
_[Lorem ipsum][01] dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum._

And now for something different

```html
Lorem ipsum dolor sit amet, ....
[![Foo](http://www.google.com.au/images/nav_logo7.png)](http://google.com.au/)
```

_[Lorem ipsum][01] dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum._
[![Foo](http://www.google.com.au/images/nav_logo7.png)](http://google.com.au/)

## HTML Image Formatting
You can also use standard HTML image syntax, which allows you to scale the width and height of the image.

```html
100 x 100 pixel image is here
<img src="http://content.answcdn.com/main/content/img/oxford/Oxford_Mind/0198162246.skinner-box.1.jpg" title="Some text for you" width="100" height="100">
Lorem ipsum dolor sit amet, ....
```

_100 x 100 pixel image is here_
<img src="http://content.answcdn.com/main/content/img/oxford/Oxford_Mind/0198162246.skinner-box.1.jpg" title="Some text for you" width="100" height="100">
_Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum._
_Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum._

### Float Image
By using some more HTML mojo, you float the image left or right.

```html
<div style="float: left">
    <img src="http://content.answcdn.com/main/content/img/oxford/Oxford_Mind/0198162246.skinner-box.1.jpg" width="200" height="200">
</div>
Lorem ipsum dolor sit amet, ....
```

<div style="float: left">
    <img src="http://content.answcdn.com/main/content/img/oxford/Oxford_Mind/0198162246.skinner-box.1.jpg" width="200" height="200">
</div>
_Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum._
_Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum._

### Selectable Image
And using a little more HTML mojo, you can make the image take you to a URL (select the image below with the mouse):

```html
<div style="float: right">
    <a href="http://webspace.ship.edu/cgboer/skinner.html">
        <img src="http://content.answcdn.com/main/content/img/oxford/Oxford_Mind/0198162246.skinner-box.1.jpg" width="200" height="200">
    </a>
</div>
Lorem ipsum dolor sit amet, ....
```

<div style="float: right">
    <a href="http://webspace.ship.edu/cgboer/skinner.html">
        <img src="http://content.answcdn.com/main/content/img/oxford/Oxford_Mind/0198162246.skinner-box.1.jpg" width="200" height="200">
    </a>
</div>
_Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum._
_Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum._

### Adding Formating Features to the Image
You can also add additional features to the image, like rounded corners

```html
<div style="float: right">
    <a href="http://www.seagate.com/external-hard-drives/desktop-hard-drives/backup-plus-desk/">
        <img class="img-rounded" title="Seagate Backup Plus" alt="Backup Plus Pic" src="http://www.hotcouponworld.com/wp-content/uploads/2013/03/4tb.jpg" width="200" height="200" /></a>
</div>
Lorem ipsum dolor sit amet, ....
```

<div style="float: right">
    <a href="http://www.seagate.com/external-hard-drives/desktop-hard-drives/backup-plus-desk/">
        <img class="img-rounded" title="Seagate Backup Plus" alt="Backup Plus Pic" src="http://www.hotcouponworld.com/wp-content/uploads/2013/03/4tb.jpg" width="200" height="200" /></a>
</div>
_Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum._
_Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum._

Now lets place somes border space around the image so the text isn't touching it.

```html
<a href="http://www.seagate.com/external-hard-drives/desktop-hard-drives/backup-plus-desk/">
    <img class="img-rounded" style="margin: 0px 8px; float: left" title="Seagate Backup Plus" alt="Backup Plus Pic" src="http://www.hotcouponworld.com/wp-content/uploads/2013/03/4tb.jpg" width="150" height="150" /></a>
Lorem ipsum dolor sit amet, ....
```

<a href="http://www.seagate.com/external-hard-drives/desktop-hard-drives/backup-plus-desk/">
    <img class="img-rounded" style="margin: 0px 8px; float: left" title="Seagate Backup Plus" alt="Backup Plus Pic" src="http://www.hotcouponworld.com/wp-content/uploads/2013/03/4tb.jpg" width="150" height="150" /></a>
_Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum._
_Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum._

### Retrieving Images From Different Locations
Now lets do a image that is stored within the directory `content/images`:

```html
<img class="img-rounded" style="margin: 0px 8px; float: left" title="Wolf Trap, 1645 Trap Road Vienna, Virginia, 22182" alt="Wolf Trap" src="{filename}/images/wolf_trap.jpg" width="150" height="150" />
Lorem ipsum dolor sit amet, ....
```

<img class="img-rounded" style="margin: 0px 8px; float: left" title="Wolf Trap, 1645 Trap Road Vienna, Virginia, 22182" alt="Wolf Trap" src="{filename}/images/wolf_trap.jpg" width="150" height="150" />
_Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum._
_Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum._

Now trying some tricks from the web, but using Markdown:

```markdown
![Wolf Trap]({filename}/images/wolf_trap.jpg =200x200 "Wolf Trap, 1645 Trap Road Vienna, Virginia, 22182")
Lorem ipsum dolor sit amet, ....
```

![Wolf Trap]({filename}/images/wolf_trap.jpg =200x200 "Wolf Trap, 1645 Trap Road Vienna, Virginia, 22182")
_Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum._
_Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum._

Now pull the image file for the blogs directory system and modify it default format:

```markdown
![Wolf Trap]({filename}/images/wolf_trap.jpg "Wolf Trap, 1645 Trap Road Vienna, Virginia, 22182" { margin: 0px 8px; float: left; width: 200px height: 200px; })
Lorem ipsum dolor sit amet, ....
```

![Wolf Trap]({filename}/images/wolf_trap.jpg "Wolf Trap, 1645 Trap Road Vienna, Virginia, 22182" { margin: 0px 8px; float: left; width: 200px height: 200px; })
_Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum._
_Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum._

### Pull Images from Flickr
You can just as easily retrive images from personal stach maintained in Flickr.

```html
<img class="img-rounded" style="margin: 0px 8px; float: left" title="HP Omni Book XE3 being used as a X Terminal using Tiny Core Linux" alt="Laptop X Terminal" src="https://farm8.staticflickr.com/7524/15871118402_2996fc7d79_b.jpg" width="25%" height="25%"/>
I store some of my blog photos on Flickr. ....
```

<img class="img-rounded" style="margin: 0px 8px; float: left" title="HP Omni Book XE3 being used as a X Terminal using Tiny Core Linux" alt="Laptop X Terminal" src="https://farm8.staticflickr.com/7524/15871118402_2996fc7d79_b.jpg" width="25%" height="25%"/>
I store some of my blog photos on Flickr.
To [get the URL of a Flickr photo][04]:

1. Click on the photo you want to share to open it.
1. Click the **Download icon**.
1. Click **View all sizes**.
1. Select the size of photo you want.
1. Right-click the image | select **Copy image URL**.

_Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum._
_Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum._



[01]:http://www.lipsum.com/
[02]:http://docs.getpelican.com/en/3.3.0/
[03]:http://jeffskinnerbox.wordpress.com/
[04]:https://help.yahoo.com/kb/flickr/SLN15714.html