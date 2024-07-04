# CompilerAPI
## About
it's a 'Compiler_Library' that contains method's to run diffirent type's of coding medout needing to download em.

## Docs
### how to use
#### add to References
in '**Visual Studio**' left click on the '**References**' and, click on '**Add Reference**' and, select the '**CompilerAPI_Library**'
#### Scripting
exsample

```cs
using CompilerAPI_Library.Engines;

// im using Lua Engine for this exsample:
LuaEngine luaEngine;

// Choose the appropriate Lua engine version
luaEngine = new LuaEngine54();



using (luaEngine)
{
    string script = @"
            print('Hello, Lua from .NET Framework!')
            local x = 10
            local y = 20
            print('Sum:', x + y);
            print(_VERSION)
    ";

    luaEngine.Execute(script);
}
```
Output:
```txt
Hello, Lua from .NET Framework!
Sum:	30
Lua 5.4
```
