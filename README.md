**Based on:** https://github.com/isagalaev/highlight.js

**Based on:** https://github.com/posquit0/dokuwiki-plugin-syntaxhighlightjs

This plugin gives you the ability to highlight the code using [Highlight.JS Plugin](https://highlightjs.org) inside containers (pre > code) with following options:
  * a programming language
  * a width
  * a certain class (with loads of useful preset classes, ex. center, round)


## Screenshot

![screenshot](https://github.com/douglasqsantos/dokuwiki-plugin-syntaxhighlightjs/blob/master/examples.png)

## Installation

Use the following path to install the plugin: https://github.com/douglasqsantos/dokuwiki-plugin-syntaxhighlightjs/archive/master.zip

Download and install the plugin using the [Plugin Manager](https://www.dokuwiki.org/plugin:plugin) using the URL given above. Refer to Plugins on how to install plugins manually.

If you install this plugin manually, make sure it is installed in
lib/plugins/highlightjs/ - if the folder is called different it
will not work!

Please refer to http://www.dokuwiki.org/plugins for additional info
on how to install plugins in DokuWiki.

## Syntax
Basic Syntax:
```
<sxh language width classes>
  source code
</sxh>
```

## Examples

### A simple usage:

```
<sxh python>
  from sys import exit

  def main():
      sys.exit(0)

  if __name__ == '__main__':
    main()
</sxh>
```

### Some more complex usage

**Using only 80% of the width for the syntax language js**

```
  <sxh js 70%>
  var gulp = require('gulp');

  gulp.task('default', function() {
    // place code for your default task here
  });
  </sxh>
```

**Using only 60% of the width and putting align in the center for the cs syntax language**

```
  <sxh cs 60% center>
  Private newPropertyValue As String
  Public Property NewProperty() As String
    Get
        Return newPropertyValue
    End Get
    Set(ByVal value As String)
        newPropertyValue = value
    End Set
  End Property
  </sxh>
```

**Using border rounded for the cpp syntax language**
```
<sxh cpp round>
#if 0
#include "pch.h"  // or whatever line you had selected
#endif // 0
</sxh>
```

## Configuration and Settings


| Option               | Description                                                 | Default value |
| ---                  | ---                                                         | ---           |
|**syntax**            | Which name to use for syntax                                | sxh           |
|**theme**             | theme for styling your code                                 | default       |
|**restrictedClasses** | restrict usage of plugin to these (comma separated) classes | empty         |

-----
-Copyright (C) Claud D. Park <posquit0.bj@gmail.com>
-
-This program is free software; you can redistribute it and/or modify
-it under the terms of the GNU General Public License as published by
-the Free Software Foundation; version 2 of the License
-
-This program is distributed in the hope that it will be useful,
-but WITHOUT ANY WARRANTY; without even the implied warranty of
-MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-GNU General Public License for more details.
-
-See the COPYING file in your DokuWiki folder for details
