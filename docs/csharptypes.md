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