# lua-multipart [![Build Status](https://travis-ci.org/Mashape/lua-multipart.svg)](https://travis-ci.org/Mashape/lua-multipart)

A Lua library to parse and edit `multipart/form-data` data.

# Usage

```lua
local Multipart = require("multipart")

-- Initialize with a body
local multipart_data = Multipart(body, content_type_header)

-- Reading parameters
local parameter = multipart_data:get("param-name")

parameter.value -- The value
parameter.headers -- A table with the headers associated with the parameter

-- Setting a new parameter
multipart_data:set_simple("some-param-name", "some-value")

-- Deleting a parameter
multipart_data:delete("param-name")

-- Get a multipart/form-data representation of the object
local body = multipart_data:tostring()
```

# Contribute

This library is a work in progress, pull-requests are welcomed.