Crypt
=====

A persistent data storage library for Corona that is designed from the ground up to use encryption.

Basic Usage
-------------------------

##### Require the code
```lua
local crypt = require( "crypt" )
```
##### Create or load a box
```lua
local box = crypt:new( "sample", "pa55w0rd" )
```

##### Load the box
```lua
box:load()
```

##### Set some values
```lua
box:set( "message", "Hello, world!" )
box:set( "score", 42 )
```

##### Get a value
```lua
print( box:get( "message" ) ) -- prints 'Hello, world!'
```

##### Increment a value
```lua
box:increment( "score", 5 )
```

##### Check if a value exists
```lua
if box:isSet( "score" ) then
  print( "YAY!" )
end 
```

##### Set a new value but only if it's higher than the current one
```lua
Crypt:setIfHigher( "score", 34 )
```

##### Save the box
```lua
box:save()
```

##### Enable or disable iCloud backup
```lua
box:setSync( true )
box:setSync( false )
```
