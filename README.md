# mgn-scroll-effect ( Don't Need jQuery )


Implement element animation when start scrolling. On the library side, animation is operated with css using transition, transform just by adding and removing class.

- Target browser : IE11+

___

# Install

```
npm i mgn-scroll-effect -S
```

___

# Import

```
import mgnScrollEffect from "mgn-scroll-effect"
```

___

# Constructor

```
new mgnScrollEffect(element [, option]);
```
|Argument|Data type|Default|Descroption|
|:-------|:--------|:------|:----------|
|element|String|-(Required)|Specify target element.<br>ex) ".j-scroll-effect"|
option|Object|-|ex)<br>option = {<br>addClass: "active",<br>ajustVal: 100,<br>}|


|Option|Data type|Default|Descroption|
|:-------|:--------|:------|:----------|
|addClass|String|"start"|Specify assigned class name when igniting event.<br>When ".j-scroll-effect" is specified in parameter [element], <br> class="j-scroll-effect_start"is assigned by default.|
|ajustVal|Number|0|Adjust event igniting position. The larger the value, the slower the ignition timing.|


___

# Demo

[https://frontend-isobar-jp.github.io/mgn-scroll-effect/](https://frontend-isobar-jp.github.io/mgn-scroll-effect/)

When execute mgnScrollEffect with **".j-scroll-effect"**,  
**".j-scroll-effect_transition"** is assigned before the event is ignited.  
Please do setting for css transition here.

**".j-scroll-effect_transition"** is deleted after **".j-scroll-effect_start"** assigned **transition** is completed.

```
import mgnScrollEffect from "mgn-scroll-effect"

new mgnScrollEffect( ".j-scroll-effect", {
    ajustVal: 400
});
```
