# Chapter 2 - Syntax
This chapter contains information about Lua code and examples in text. This chapter is formatted in a cheatsheet like format. 

### Table of Contents
- Code Comments & Imports
- Printing
- Variables
- Variable Assignment
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

## Printing
The print function on Lua is the most basic piece of code on Lua 
```lua
print("Hello World!")
```

## Variables

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

- **Function**s are reserved keywords that is written in Lua or pointed out by the user
```lua
function studentId(IdNo)
  end
print(type(studentId))  -- function
```
- **String**s are ASCII text values
```lua
name = Jimmy

print(type(name))       -- string
```
- **Number** can be decimal or integer values (also known as floats in other languages)
```lua
local age = 16
local height = 165.5

print(type(age))        -- number
print(type(height))     -- number
```
- **Boolean** is exclusively true or false as values
```lua
local inSchool = false

print(type(inSchool))   -- boolean
```
- **Nil** all variables nil by default until given a value. Signifies error or no value.
```lua
local money = x

print(type(money))      -- nil
```

## Variable Assignment

Values can be assigned to variables in multiple ways

- **Chained assignment** is variable assignment that gives the same value to multiple variables
```lua
a = 5
b = 0
c = 0
d = 0

a = b
b = c
c = d

print(d) -- 5
```

- **Compound assignment** is variable assignment using operators that increment the current value by a certain amount.
```lua
a = a + 1

print(a) -- 6
```

- **Parallel assignment** is variable assignment that gives different variables different values in a single line of code
```lua
a, b, c, d = 1, 2, 3, 4

print(a) -- 1
print(b) -- 2
print(c) -- 3
print(d) -- 4

-- Parallel assignments can be changed to reassign values further in the code

print(a, b) -- 1 2
a, b = b, a
print(a, b) -- 2 1
```

## Operators
Like other languages, Lua has 8 operators that can be used
```lua
=   -- Equal to (Arithmetic operator only)
+   -- Addition
-   -- Subtract
*   -- Multiply
/   -- Divide
^   -- Power
%   -- Modulo (Mod)
..  -- Concatenate String
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

g = name .. "'s score is " .. y .. " out of " x   -- name from previous section concatenated with local variables
print(g)  -- Jimmy's score is 5 out of 10       
```

Operators and Comparison Operators are two different things. Operators are used in arithmetic equations while Comparison Operators are used to compare two or more statements. 

## Condition & Comparison Operators
Conditions are reserved keywords that execute code if a certain condition is met
```lua
if        -- Indicates the start of a conditional statement, is the initial statement a comparison operator follows
elseif    -- Is the secondary statement a comparison operator follows. Can be used as many times in a conditional statement
else      -- Executes code if no previous statements are met. Can only be used once and must be last in conditon statements
then      -- Follows if and elseif to the end of the condition
end       -- Ends a conditional statement or a loop
```

Condition operators are operators that compare two or more statements.
```lua
==   -- Equal to (Condition operator only)
~=   -- Not Equal to
>    -- Greater than
<    -- Less than
>=   -- Greater than or equal to
<=   -- Less than or equal to
```

