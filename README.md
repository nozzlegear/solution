# Solution

Solution is a command-line utility for manipulating .NET solution files, creating new solutions, adding projects to a solution, and adding files to a project. I've started this project because currently there's no reliable way to create or manipulate new .NET or C# projects from the command line. Visual Studio is heavy, and it's not available at all on Unix or OSX, and I dream of a world where I can work on C# projects completely from the command line, without ever opening Visual Studio.

**But what about the new dotnet CLI?** I'm super excited for DotNet-Core, and especially for its new command line integration. Unfortunately, the `dotnet` CLI is strictly for working with new DotNet-Core projects, and doesn't currently support "older" .NET framework projects. 

This project has just been started! Follow [@nozzlegear](https://twitter.com/nozzlegear) on Twitter for project updates.

## Paket

This project shirks the NuGet package manager in favor of [Paket](https://github.com/fsprojects/paket), another C#/F# package manager more widely used by the F# community. **Paket fully supports packages from not only NuGet**, but also from GitHub and the file system. 

The biggest advantage of Paket over NuGet, though, is that you don't have to open Visual Studio to use it. It just works, right out of the box, on your command line on both Windows and Unix machines. 

While NuGet does have a CLI, it's pretty barebones; it only supports downloading packages and placing them in a folder, but **it doesn't add the package references to your .csproj file**. Paket handles all of that and more.