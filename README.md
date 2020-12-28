![Build with bob](https://github.com/JustAPotota/defold-lz4/workflows/Build%20with%20bob/badge.svg)

# defold-lz4
Port of [witchu/lua-lz4](https://github.com/witchu/lua-lz4) to [Defold](https://www.defold.com/)'s native extension format.

## Installation
You can use defold-lz4 in your own project by adding it as a [Defold library dependency](https://defold.com/manuals/libraries/). Open your game.project file and in the dependencies field add:

https://github.com/JustAPotota/defold-lz4/archive/master.zip

Or point to the ZIP file of a specific release, e.g. https://github.com/JustAPotota/defold-lz4/archive/v1.0.zip.

## Usage
Refer to [lua-lz4](https://github.com/witchu/lua-lz4) for documentation. Quick example:
```lua
function init(self)
	local s = "LZ4 is a very fast compression and decompression algorithm."
	print("Original: " .. s)
	
	local compressed = lz4.block_compress(s)
	print("Compressed: " .. compressed)
	
	local decompressed = lz4.block_decompress_safe(compressed, #s)
	print("Decompressed: " .. decompressed)
end
```
