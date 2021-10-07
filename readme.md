# classic-dotnet-templates

Provides .NET 6+ project templates that do not use top-level statements.

Installing this package using `dotnet` will make the templates available in both Visual Studio 2022 and the `dotnet new` CLI command.

### Install from NuGet

`dotnet new -i Classic.Console.Templates`

### What Is This?

Beginning with .NET 6, project templates for Console applications use new features called "global usings" and "top-level statements".

This means a new Console project's `Program.cs` looks like this:

```
// See https://aka.ms/new-console-template for more information
Console.WriteLine("Hello, World!");
```

Instead of the "classic" `Program.cs` which looks like this:
```
using System;

namespace MyProject
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello, World!");
        }
    }
}
```

There is currently no option to use the "classic" template if you wish.  Installing this template pack will add a "classic" template to VS2022:

![VS2022 Screenshot](https://github.com/jpobst/classic-dotnet-templates/blob/main/docs/vs-new-project.png "VS2022 Screenshot")

### Use from CLI

To create a new project from the command line:

`dotnet new console-classic`

### Uninstall

This template pack can be uninstalled with:

`dotnet new -u Classic.Console.Templates`
