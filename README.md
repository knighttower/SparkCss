---
# ⚠ ATTENTION: 
## This repo has been moved as part of a monorepo to -> https://github.com/knighttower/JsUtility

---

# Bootstrap Mini

Built on top of Bootstrap but modified to have only the basic utilities classes and the grid system. This is a (very) lightweight CSS version that can be used to build websites and web applications.
<br>
It is not meant to replace the full functionality of Bootstrap, only to abstract the basic utilities to use in quick prototypes, small projects or to compliment other frameworks since it does not add any root styles, resets or normalize, colors or other theme styles that would override or conflict. It can also be customized with a few variables before importing the file to load only a few utilities or the full set.
<br>
Compressed: 72.5 KiB  
Uncompressed: 104 KiB  
GZip: 8 KiB  
Brotli: 5 KiB
<br>

<br>
Usage:  <br>

```
npm install @knighttower/bootstrapmini -D
```

```
yarn add @knighttower/bootstrapmini -D
```

```scss
@import '~@knighttower/bootstrapmini/src/bootstrapmini.scss';
```

<br>
or as a drop-in css file into vite or webpack
<br>  

```  
import "@knighttower/bootstrapmini/dist/bootstrapmini.css"  
```  

<br>

If using the sass file, some variables are available to be modified before importing the file. These are the defaults

```scss  
$miniPrefix: bs-;
$miniColumns: 12;
$miniGutterWidth: 1.5rem;
$miniRowColumns: 6;
$miniFontSizeBase: 1rem;

$miniEnableMargins: true;
$miniEnablePadding: true;
$miniEnableWidth: true;
$miniEnableHeight: true;
$miniEnableZIndex: true;
$miniEnableFlex: true;
$miniEnableFloat: true;
$miniEnablePosition: true;
$miniEnableDisplay: true;
$miniEnableVisibility: true;
$miniEnableContainer: true;
$miniEnableGridClasses: true;
$miniEnableCssGrid: true;
```  

<br>
Then do:
<br>  

```scss  
$miniEnableMargins: false;  
//... other overrides before the import  
@import '~@knighttower/bootstrapmini/src/bootstrapmini';  
````

<br><br>

### It includes

-   Width
-   Height
-   Z-index
-   Flex
-   Flexbox
-   Grid
-   CSS grid
-   Spacing
-   Columns
-   Position
-   Display
-   Sizing
-   Margin
-   Padding
-   Float
-   Clear
-   Utilities
-   Mixins

<br>

## It does not include

-   No javascript
-   No images
-   No fonts
-   No icons
-   No javascript plugins
-   No components
-   No animations
-   No transitions
-   No colors
-   No themes
-   No resets
-   No negative margins or paddings
-   No negative width or height
-   No negative z-index
-   No buttons
-   No forms
-   No tables
-   No typography
-   No print styles

**--> Told ya! It's tiny!**

<br>
<br> 

## Features  

-   Cool set of mixins (in addition to the bootstrap default ones)  

```scss
/**
* @mixin breakpoint
* BreakPoint print utility
* @param {String} $screen <breakdown name>|size in px
* @param {Null|String} $param Keywords:landscape, portrait|<custom query>ex:max-width:800px
* @param {Null|Bool} $exclude null | true to negate the query use with caution.
* @return Media Query
* @example
* @include breakpoint(<breakdown name>){rules...}; or
* @include breakpoint(000px,'max-width:800px'){rules...}; or
* @include breakpoint(<breakdown name>,landscape){rules...}; or
* @include breakpoint(<breakdown name>,'max-width:800px'){rules...};, etc...
*/
.ex-class {
    @include breakpoint(lg) {
        // rules
    }
    @include breakpoint(mobile) {
        // only applies to 0-599 px
        // rules
    }
}
````

<br>

-   A set of utility classes that can be used to build websites and web applications. Only the most used classes are included. The rest can be added by the user.  

    -- Common Bootstrap classes:  
    --- Flex, Flexbox, Grid, Spacing, Text, Display, Position, Visibility, Sizing, Margin, Padding, Css grid, Columns  

-   Modified classes:  
    -- ml (margin-left), mr (margin-right), pr (padding-right), pl (padding-left), float-left, float-right  

-   Additional classes:  
    -- Width (w-) increments in 10, ex: w-10, w-20, w-30, etc... up to 100%  
    --- Widht special: w-25, w-33, w-50, w-66, w-75, w-100 (25%, 33%, 50%, 66%, 75%, 100%)  
    -- Height (h-) increments in 10, ex: h-10, h-20, h-30, etc... up to 100% and 'vh' for viewport height  
    -- Zindex (z-) increments in 10, ex: z-10, z-20, z-30, etc... up to 50
    

-   Screen Sizes:  
    -- mobile: 0-599px (targets only this braket)  
    -- tablet: 600-1023px (targets only this braket)  
    -- desktop: 1024 (targets from here up)  
    -- sm: 576 (targets from here up (bootstrap default behavior))  
    -- md: 768 (targets from here up (bootstrap default behavior))  
    -- lg: 992 (targets from here up (bootstrap default behavior))  
    -- xl: 1200 (targets from here up (bootstrap default behavior))  
    -- xxl: 1400 (targets from here up (bootstrap default behavior))  
    <br>
    

<br>  


### Why?

Most CSS frameworks come loaded with themes, or bulky in general that makes it hard the quick use without getting the full package or having to modified them to get only what you need. I also (IMO) think that the grid system bootstrap offers, has simple and versitile enough to be used in quick projects. (I'll discuss that in a future post).  
Please notice, that there are things that are not included in this tyny version, the intention of this it to be basic, and if more functionality is needed, or theme styles need to be applied, then you should go full framework with Bootstrap [https://getbootstrap.com], Tachyons [https://tachyons.io], unoCSS [https://unocss.dev] (I have my eye on this one), etc...

PS: as of the writting of this, I have been implementing the minibootstrap (only the grid and cssgrid) along with UnoCss and this is a killer combo. (notice that UnoCss does not provide a strong grid but bootstrap does). I'll talk about this more at https://knighttower.io

<br> 

Credits to the Bootstrap team for the great work they have done.
