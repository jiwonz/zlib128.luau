# Note
- Unlike [zlib91.lua](https://github.com/jiwonz/zlib91.lua), This library does not support pure lua.
- This library shares almost identical usage with [zlib91.lua](https://github.com/jiwonz/zlib91.lua)
# Important
- Since this library uses the base128 function, which is part of rstk's BitBuffer library, due to the operating principle of the bit buffer, it may not be compatible with the general base128(ex. Python base128 library) at all or the data size may be slightly larger.
- If you want better compatibility, you can also look into [zlib91.lua](https://github.com/jiwonz/zlib91.lua), although it may have some disadvantages as it can grow slightly more data than base128.
# Roblox Luau
- Supports luau type autocompletes
- (btw, I just personally prefer to use UpperCamelCase with modules for roblox)
## import Zlib128 module
```lua
local Zlib128 = require(script.zlib128)
```
## Zlib128.compress(data :string, useSingleQuote? :boolean, level :number, strategy :"dynamic"|"fixed"|"huffman_only") -> compressedData :string
```lua
local compressedData = Zlib128.compress("example data")
```
## Zlib128.decompress(compressedData :string, useSingleQuote? :boolean) -> decompressedData :string
```lua
local decompressedData = Zlib128.decompress(compressedData)
```
## Available strategies:
- "dynamic"
- "fixed"
- "huffman_only"
# Credits
- [Zlib compression module for Lua](https://devforum.roblox.com/t/string-compression-zlibdeflate/755687)
- [Base128 with rstk's BitBuffer](https://github.com/rstk/BitBuffer)
