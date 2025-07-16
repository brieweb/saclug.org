Title: July General Meeting
Tags: general meeting
Event: 2025-07-15 6:30 pm to 8:30 pm
Speaker: Brian Lavender
Location: Strad Meadery
Author: Brian E. Lavender
Slug: july-2025

We will discuss C# on GNU/Linux. 

Strad Meadery graciously provided their 
facility to us for hosting the meeting. James (from Strad Meadery) says that if we plan to eat during
the meeting that we should bring our own food or order food for delivery.

## C# discussion agenda

This is a loose collection of notes and links for our dicsussion during the meeting.

* [Install the .NET SDK or the .NET Runtime on Fedora](https://learn.microsoft.com/en-us/dotnet/core/install/linux-fedora?tabs=dotnet9)
* [Install Visual Studio Code](https://code.visualstudio.com/docs/setup/linux#_rhel-fedora-and-centos-based-distributions)

Microsoft only allows the use of vsdbg from within VSCode. Samsung has a [Command line debugger](https://github.com/Samsung/netcoredbg).

Command line project creation

```
dotnet new console -o ./CsharpProjects/TestProject
```

The namespace declaration provides a way to logically organize your code. 

* [Program structure](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/program-structure/)
* [C# if statements and loops - conditional logic tutorial](https://learn.microsoft.com/en-us/dotnet/csharp/tour-of-csharp/tutorials/branches-and-loops)

* [Learn C#](https://learn.microsoft.com/en-us/collections/yz26f8y64n7k07)

* [Nullable types](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types)

* [Tuples and Types](https://learn.microsoft.com/en-us/dotnet/csharp/tour-of-csharp/tutorials/tuples-and-types)


* [Asynchronous Programming](https://learn.microsoft.com/en-us/dotnet/csharp/asynchronous-programming/)

* [Object Oriented programming](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/tutorials/classes)

* [MVC tutorial Csharp](https://learn.microsoft.com/en-us/aspnet/core/tutorials/first-mvc-app/start-mvc?view=aspnetcore-9.0&tabs=visual-studio-code)

Add dependency to CSharp project such as [IText](https://www.nuget.org/packages/itext)

```
dotnet add package itext --version 9.2.0
```







