#jQuery component

jQuery with [component](https://github.com/component/component) support

Automatically synchronized with basic `jquery/jquery` repository with [componentor](http://github.com/edjafarov/componentor)

#### jquery decomposed
Instead of using custom builds the jQuery was decomposed on separate components per existing configuration:
```javascript
{ flag: "wrap", src: "src/wrap.js" },
{ flag: "css", src: "src/css.js" },
{ flag: "event-alias", src: "src/event-alias.js" },
{ flag: "ajax", src: "src/ajax.js" },
{ flag: "ajax/script", src: "src/ajax/script.js", needs: ["ajax"]  },
{ flag: "ajax/jsonp", src: "src/ajax/jsonp.js", needs: [ "ajax", "ajax/script" ]  },
{ flag: "ajax/xhr", src: "src/ajax/xhr.js", needs: ["ajax"]  },
{ flag: "effects", src: "src/effects.js", needs: ["css"] },
{ flag: "offset", src: "src/offset.js", needs: ["css"] },
{ flag: "dimensions", src: "src/dimensions.js", needs: ["css"] },
{ flag: "deprecated", src: "src/deprecated.js" },

```
* jqcomp/jquery - complete jquery framework build
* jqcomp/core - core jquery with sizzler
* jqcomp/wrap
* jqcomp/css
* jqcomp/event-alias
* jqcomp/ajax
* jqcomp/ajax-script
* jqcomp/ajax-jsonp
* jqcomp/ajax-xhr
* jqcomp/effects
* jqcomp/offset
* jqcomp/dimensions
* jqcomp/deprecated

dependencies for separate components will be resolved automatically by component  framework.

#### usage

I assume you use [component](https://github.com/component/component) or [compy](https://github.com/edjafarov/compy)

```
$ component install jqcomp/jquery
//or
$ compy install jqcomp/jquery
```
in the code
```
var $ = require('jqcomp/jquery');
```

##### made by [@edjafarov](https://twitter.com/edjafarov)
