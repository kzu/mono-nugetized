# mono-nugetized

Nugetizes some of Mono assemblies for easier consumption

| Assembly      | Package     |
| ------------- | ------------- |
| Mono.Posix    | [![Version](https://img.shields.io/nuget/v/Mono.Posix.svg)](https://www.nuget.org/packages/Mono.Posix) | [![Downloads](https://img.shields.io/nuget/dt/Mono.Posix.svg)](https://www.nuget.org/packages/Mono.Posix) |
| Mono.Security | [![Version](https://img.shields.io/nuget/v/Mono.Security.svg)](https://www.nuget.org/packages/Mono.Security) | [![Downloads](https://img.shields.io/nuget/dt/Mono.Security.svg)](https://www.nuget.org/packages/Mono.Security) |

# How to nugetize

If you need to create a nuget package for another assembly, these are the steps:

1. Copy [Mono.Posix.targets](https://github.com/kzu/mono-nugetized/blob/master/package/Mono.Posix.targets) to 
   use as a baseline. 
2. Replace the assembly and filename with the one you will include in the nuget package. 
3. Update [build.proj](https://github.com/kzu/mono-nugetized/blob/master/build.proj) to include a new `NuGetize` 
   item for the assembly to nugetize, including a `Description` metadata to include in the package.