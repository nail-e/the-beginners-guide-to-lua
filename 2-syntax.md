# Chapter 2 - Syntax
This chapter contains information about Lua code and examples in text. This chapter is formatted in a cheatsheet like format. 

### Table of Contents
- Code comments & imports
- Printing & Variables
- Operators 
- Conditions & Comparison Operators 
- Loops
- Functions
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

## Operators
Like other languages, Lua has 7 operators that can be used
```lua
= -- Equal to
+ -- Addition
- -- Subtract
* -- Multiply
/ -- Divide
^ -- Power
% -- Modulo (Mod)
```

```lua
local x = 10
local y = 5

local a = x + y   -- 10 plus 5
print(a)  -- 15

local b = x - y   -- 10 minus 5
print(b)  -- 5 

local c = x * y   -- 10 times 5
print(c)  -- 50

local d = x / y   -- 10 by 5
print(d)  -- 3

local e = x ^ y   -- 10 to the power of 5
print(e)  -- 10000

local f = y % x   -- 5 modulo 10 (remainder of 5 by 10)
print(f)  -- 5    
```

Operators and Comparison Operators are two different things. Operators are used in arithmetic equations while Comparison Operators are used to compare two or more statements. Comparison Operators will be explained more in-depth in the next section.
