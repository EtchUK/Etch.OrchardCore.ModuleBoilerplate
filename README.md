# Module Boilerplate

Module boilerplate is our starting point for building [Orchard Core](https://orchardcore.readthedocs.io/en/latest/) modules.

## Build Status

[![NuGet](https://img.shields.io/nuget/v/Etch.OrchardCore.ModuleBoilerplate.svg)](https://www.nuget.org/packages/Etch.OrchardCore.ModuleBoilerplate)

## Getting Started

To create a new module using the boilerplate it's quickest to use the `dotnet new` command. First you'll need to install the template, which is hosted on NuGet.

    dotnet new install Etch.OrchardCore.ModuleBoilerplate --nuget-source https://api.nuget.org/v3/index.json

Once installed successfully, run the command below, which demonstrates all the possible parameters that are available.

    dotnet new orchardcore-moduleboilerplate -n Example.OrchardCore.Module -o Example.OrchardCore.Module -au "Your Company Ltd." --description "Description for your module" -m "Your Module Name" -w "https://yourwebsite.co.uk" -c "Content"

### Parameters

Below are the different parameters that can be included in the `dotnet new` command. The majority of the parameters will be used in the `package.json`, `.csproj` (to describe author of NuGet package) and the module manifest. `-n` & `-o` are parameters required by `dotnet new`.

#### -au/--author

Author of the module.

#### -c/--category

Category for the module.

#### --description

Short description of the module.

#### -m/--moduleName

Name of your module.

#### -w/--website

URL for your website.

## Packaging Template

This template has been made available on NuGet. To create the `.nupkg` file that can be published to NuGet, run the command shown below.

    nuget pack ./Etch.OrchardCore.ModuleBoilerplate.nuspec
