# C# Types

```csharp
// Can put a semi colon after namespace and everything in file will be part of namespace
namespace Program;
public class Program 
{
    public static void Main(string[] args)
    {
        // highlight-next-line
        Console.WriteLine("Hello, World!");
    }
}

```

Formatting
- Right click file, add item, editor config
    - This will then set the default styling for the project and will override the default VS styling for the project
- dotnet format .\name.csproj
    - Will format the project using the editor config

## Value Types
Value types have their memory managed automatically and their life and scope is predictable.

The "value" lives on the stack. It is automatically removed from the stack when the variable goes out of scope.

Value types are structs in C#.

## Reference Types
Reference types have values that live on the "managed" heap.

The stack has a refecence to the value on the heap.

The memory is allocated automatically, and de-allocated using a generational garbage collection algorithm.

