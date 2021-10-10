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

![VS2022 Screenshot](https://raw.githubusercontent.com/jpobst/classic-dotnet-templates/main/docs/vs-new-project.png "VS2022 Screenshot")

Using this template will allow you to select which template features to use:

![VS2022 Screenshot](https://raw.githubusercontent.com/jpobst/classic-dotnet-templates/main/docs/vs-options.png "VS2022 Screenshot")

### Use from CLI

To create a new project from the command line:

`dotnet new console-classic`

Template features can be toggled:

`dotnet new console-classic --topLevelProgram=false --nrt=true --implicitUsings=false`

Available options:
```
--nrt: If true, turns on nullable reference types. [defaults to 'true']
--topLevelProgram: If true, auto-generates the top level statements, skipping explicit main methods, class and namespace. [defaults to 'false']
--implicitUsings: If true, auto-imports many common using statements. [defaults to 'false']
```

### Uninstall

This template pack can be uninstalled with:

`dotnet new -u Classic.Console.Templates`
