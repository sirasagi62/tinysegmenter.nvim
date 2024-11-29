# TinySegmenter.nvim
TinySegmenter.nvim is a plugin that provides a Lua port of TinySegmenter, an ultra-minimal Japanese tokenizer. Since the plugin depends only on the Lua standard library, it can be executed anywhere that supports Lua 5.1 or later.

## Install
```lua
-- tani/vim-jetpack
Jetpack "sirasagi62/tinysegmenter.nvim"
```

## Usage
```lua
local tinysegmenter = require("tinysegmenter")

-- return table like {"これ","は","文章","です","。"}
local parsed_text = tinysegmenter.segment("これは文章です。")

-- これ|は|文章|です|。
print(table.concat(parsed_text,"|"))

```

## API
### `tinysegmenter.segment(string)`
Returns a table of Japanese sentences split into words.

## License
This program is provided under BSD-3-Clause.

Copyright information is here: `./lua/tinysegmenter.lua`

## Acknowledgments
This program is originally created by Taku Kudo in 2008, modified for ES module by Taisuke Fukuno in 2022.
Also, `utf8.lua` is provided under CC0 by NAKAI Tsuyoshi.

