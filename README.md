## Komodo New Source Tree (Symbols Tree)

This plugin adds a filterable code tree view for the current open file.
Backbone.js classes don't show up in most source tree plugins so I've modified
NST to show Backbone.js class declerations like the one below.

```javascript
Product.Views.ProductSearch = Backbone.View.extend({
    el: '#search_bar',
    template: _.template($('#product_search_template').html()),
    initialize: function (){
        console.log('Product.Views.ProductSearch init');
        this.render();
    },
    render: function () {
        $(this.el).empty();
        $(this.el).append(this.template());
    },
    drop : function() {
        this.undelegateEvents();
        $(this.el).empty();
    }
});
```
![Image of NST](NST_example.png)

Original readme is below:
----

Code Browser -like extension for Komodo Edit

by Adam Łyskawa

Contributors:
See content/NST.js

PLEASE - UPDATE COMMENT IN content/NST.js, or I could miss your contribution
on ActiveState Community website! And I don't want to!

Since I'm too busy with my current work to update NST, please feel free to
update the code as you like, fix bugs, implement new features.

Then test it, e-mail me it works and I'll release it as new version
on ActiveState Community website.

You don't need to fork the project, if you need anything, like privileges,
just ask. I don't use GIT everyday, so I don't even know how to grant them,
but I'll find it out.

I would love NST to become community project. It's my "baby", but I can't
find time to develop it anymore. Maybe if I ever change my job to more
related with what NST does or how it works...

http://www.youtube.com/watch?v=dj2nqILbPdA

Thank you for all the support. Feel free to change this README too.

-----------
-- Notes --
-----------

Please don't change code formatting:
2 spaces for indentation, opening braces on the same line.

Or if you convinced 4 spaces indentation would look more
readable (well, we have bigger screens now) - change the indentation
globally in each file, let it be consistent at least.

Please document your changes using JSDoc syntax.

THANK YOU.

-------------------
-- License (BSD) --
-------------------
Copyright (c) 2010-2013, Adam Łyskawa
All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:

Redistributions of source code must retain the above copyright notice,
this list of conditions and the following disclaimer.
Redistributions in binary form must reproduce the above copyright
notice, this list of conditions and the following disclaimer in the
documentation and/or other materials provided with the distribution.
Neither the name of nor the names of its contributors may be used to
endorse or promote products derived from this software without specific
prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE
ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT OWNER OR CONTRIBUTORS BE
LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR
CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF
SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS
INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN
CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE)
ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE
POSSIBILITY OF SUCH DAMAGE.
