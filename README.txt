------------------------------------------------------------------------
canhaz generator tool

Author: Brian Cavalier
------------------------------------------------------------------------

Canhaz is a project bootstrapping tool for generating stub files,
similar to generator tools found in frameworks such as Ruby on Rails.
The main difference is that canhaz is completely framework-independent,
and highly-extensible through plugin generators.

------------------------------------------------------------------------
Quick Start
------------------------------------------------------------------------

canhaz [--force] [type] module_path [generators]

Example: canhaz jquery:widget js/ui.myWidget
Creates the directory js, if necessary, and generates:
 ui.myWidget.js  - jQuery widget skeleton, fill in your code!
 ui.myWidget.css - CSS skeleton for your widget

------------------------------------------------------------------------
Options
------------------------------------------------------------------------

--force
Force overwriting an existing dir.  By default canhaz will not overwrite
an existing leaf dir, and it will warn you if you try to do so.  If you
really want to overwrite it, use the --force :)

type (optional)
Type of "thing" to generate.  The default is "view", which generates
all the files necessary for a new View (see above in Quick Start).
Look in the generators directory to see the kinds of "things" that
canhaz supports.

module_path
Path of the thing to generate.  You can think of this as an AMD
module id, or as a relative filesystem path.  The last part of the
path will be the name of the thing.  Different generators may use
this information in slightly different ways.

generators (optional)
You can list a subset of the components you'd like to generate.  For
example, when generating a view, if you don't need a strings file, you
could do: canhaz my/view/MyView js scss css html test (i.e. leaving
out strings)

------------------------------------------------------------------------
License
------------------------------------------------------------------------

Canhaz is available under the MIT license.  See LICENSE.txt for details.