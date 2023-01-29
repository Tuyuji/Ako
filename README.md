# Ako
A simple config language that's inspired by games cvar / autoexec format.

## Sample
```ako
window [
    #Vectors in code are just arrays of ints or floats, they can't contain spaces.
    size 1280x720
    title "My \"Window\""
    # +, -, ;, & are reserved as they represent
    #true, false, null, short type
    +fullscreen
    #Setting subsystem to null so we get the default
    subsystem;
]

wayland.display "wayland-1"

player."Full name" "John Smith"
```
Short types are prefixed with &
Depending on the Ako library used it could be a string
or in [AkoSharp's](https://github.com/Tuyuji/AkoSharp) case a C# Type.
```ako
player.items [[
    &Items.Sword
    &Items.Shield 
]]
#Hex uses suffex `x 
teams.ct.color `x3287a8
```

## Types
- Null ;
- String ""
- Int 12
- Float 1.54 or 1.54f
- ShortType &
- Bool +, -
- Table \[\]
- Array \[\[\]\]

## Todo
 - [ ] Schema 