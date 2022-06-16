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
Local variables is a scope type that has to be declared. It's faster to call a local variable than a global variable if executing from the same script. For clarity and reinforcing good practice, all variables on this chapter from here on out will be local.
```lua
local a = hello       -- local variable  
```

Variables can have different data types
```lua
print("")                   -- Function
local name = "Jimmy"        -- String
local username = "J-immy"   -- String
local age = 16              -- Number
local height = 165.5        -- Number 
local inSchool = true       -- Boolean
local money = nil           -- Nil 
```
- **Function**s are reserved keywords that is written in Lua
- **String**s are ASCII text values
- **Number** can be decimal or integer values (also known as floats in other languages)
- **Boolean** is exclusively true or false as values
- **Nil** all variables nil by default until given a value
