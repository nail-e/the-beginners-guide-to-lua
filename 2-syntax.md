# Chapter 2 - Syntax
This chapter contains information about Lua code and examples in text. This chapter is formatted in a cheatsheet like format.

### Table of Contents
- Code comments & imports
- Printing & Variables
- Operations
- Conditions
- Functions
- Loops
- Tables

## Code Comments & Imports
Adding code comments can improve visibilty of your code
```lua
-- This is a code comment on Lua
```

The require function imports code from other files in the same environment to the current script
```lua
require("filename")
```

## Printing & Variables
The print function on Lua is the most basic piece of code on Lua 
```lua
print("Hello World!")
```

Variables can have a local tag for a variable to become local or no tag to become global 
Global variables is the default scope type and can be called by other modules. It's bad practice to not decalre variables as local if you don't intend to import the variable to another script.
```lua
a = hello             -- global variable
-- or
local _G.a = world    -- also a global variable ( )
```
Local variables is a scope type that has to be declared. It's faster to call a local variable than a global variable if executing from the same script.
```lua
local a = hello       -- local variable  
```
