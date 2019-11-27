# Getting Started with Try Dotnet

> Try .NET provides developers and content authors with tools to create interactive experiences.

---

## Links & Resources

* [`dotnet/try`](https://github.com/dotnet/try)
* [`dotnet/try-samples`](https://github.com/dotnet/try-samples#basics)
* [Try .NET Local Setup](https://github.com/dotnet/try/blob/master/DotNetTryLocal.md)
* [.NET Jupyter Notebooks](https://github.com/dotnet/try/blob/master/NotebooksLocalExperience.md)

---

## Requirements

* [`.NET Core 3.0 SDK`](https://dotnet.microsoft.com/download/dotnet-core/3.0)
* [`.NET Core 2.1 SDK`](https://dotnet.microsoft.com/download/dotnet-core/2.1)
* [`dotnet try`](https://www.nuget.org/packages/dotnet-try/) global tool

---

## Try .Net Installation

To install the tool run the following command:

```powershell
dotnet tool install -g dotnet-try
```

Updating to the latest version of the tool is easy. Run the following command:

```powershell
dotnet tool update -g dotnet-try
```

---

## .Net Notebooks Setup

Install `jupyter`:

`pip install jupyter`

Install the `dotnet interactive` global tool:

`dotnet tool install -g dotnet-interactive`

Install the .NET kernel by running the following:

`dotnet interactive jupyter install`

You can verify the installation by running the following:

`jupyter kernelspec list`

Launch JupyterLab:

`jupyter lab`

---
