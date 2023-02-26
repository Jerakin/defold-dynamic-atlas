# Dynamic Atlas

This serves as both an exampel and a library to help you create dynamic atlases in run time.

> WARNING! You can not use this functionallity in GUI yet. It has been reported to Defold https://github.com/defold/defold/issues/7423


## Installation
You can use the dynamic atlas in your own project by adding this project as a [Defold library dependency](http://www.defold.com/manuals/libraries/). Open your game.project file and in the dependencies field under project add:

https://github.com/Jerakin/defold-dynamic-atlas/archive/refs/heads/main.zip

Or point to the ZIP file of a [specific release](https://github.com/Jerakin/defold-dynamic-atlas/releases).

## Quick Start
You only need to supply a list of images as well as width and height to `dynatlas.pack()` use it.

```lua
local atlas_entries = {
	"example/assets/images/image0.png", "example/assets/images/image1.png
}

local atlas_id = dynatlas.pack("example", atlas_entries, 256, 256)
	
go.set("#sprite", "image", atlas_id)
sprite.play_flipbook("#sprite", "image0.png")
```

The images added will be added with the full file name as the id. This always includes the `.png`.
