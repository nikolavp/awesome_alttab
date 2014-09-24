Integrate familiar Alt-Tab functionality in Awesome WM 3.5, tested only on 3.5.5

Features:
* Live previews while alt-tabbing
* No previews when alt-tab is released within some time-frame
* Backward cycle using shift
* Intuitive order, respecting your client history
* Includes minimized clients (in contrast to some of the default window-switching utilies)


## Installation

    cd ~/.config/awesome
    git clone https://github.com/jorenheit/awesome_alttab.git alttab

## in your rc.lua:

    -- load the function somewhere
    local alttab = require("alttab")

    -- Add this to your key-bindings table so you will setup the keys:
    -- ....
    awful.key({ "Mod1",           }, "Tab",
        function ()
           alttab(1, "Alt_L", "Tab", "ISO_Left_Tab")
        end
    ),
    awful.key({ "Mod1", "Shift"   }, "Tab",
        function ()
           alttab(-1, "Alt_L", "Tab", "ISO_Left_Tab")
        end
    ),
    -- ...


