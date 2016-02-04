startpage
====

![example screenshot](/images/screenshots/2015-12-26-closed.png?raw=true)
![example screenshot open](/images/screenshots/2015-12-26-open.png?raw=true)


<br>
###### Configuration Menu
The menu will be displayed the first time the page is loaded. It can be opened anytime by entering ```-c``` into the search field.
If you have removed the search field from the html file you can still open it by entering ```search("-c")``` into the browser's console.

<br>
###### JSON
| attribute         | if true                                          |
| ----------------- | ------------------------------------------------ |
| borders           | enables borders on top and bottom                |
| alwaysopen        | makes all squares open on load                   |
| mascot            | enables image in the bottom right hand corner    |
| allowVersionCheck | allows to check for the latest Version on github |
| privateMode       | will always load config.json                     |

The version is only checked for if the help popup shows up.
Set privateMode to ```true``` if you're always using private mode.

The _images_ array is a list of all mascot images to be used. If you want to use only one image just create an array with one item.

<br>
###### HTML
To add/remove a square just add/remove a _div .sqr_ within _div #cell_.<br>
Keep the structure like this:
```
<div class="sqr">
    <span>HEADING</span>
    <div class="content">
        <a href="URL">LINK TITLE</a><br>
        <a href="URL">LINK TITLE</a><br>
        ...
        <a href="URL">LINK TITLE</a>
    </div>
</div>
```

<br>
###### search
```
-c      Opens the configuration menu
-h      Show this list
-g      Google (default)
-w      Wikipedia
-a      ArchWiki
-d      danbooru
-y      YouTube
-n      niconicodouga
-p      pixiv
```
The following example will search for _github_ using _DuckDuckGo_:<br>
-a github<br>
If an invalid search option or none at all is specified, Google is used.
For danbooru, use underscores (_) for tags with more than one word and separate multiple tags with space (e.g.: school_uniform 1girl).
