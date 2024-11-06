# Introduction

Provides code analysis and .editorconfig for Status projects

The project adds some well-known analyzers for code analysis as well as a standard .editorconfig for 
Status projects.

https://github.com/biggik/Status.CodeFormatting

# How to use

Add a *Directory.Build.props* file next to your Solution file (*.sln)

Add something like the following to the Directory.Build.props file

```
<Project>
  <PropertyGroup>
    <Authors>Status ehf.</Authors>
    <Copyright>Status ehf.</Copyright>
    <EnforceCodeStyleInBuild>true</EnforceCodeStyleInBuild>
    <EnableNETAnalyzers>true</EnableNETAnalyzers>
    <GenerateDocumentationFile>true</GenerateDocumentationFile>
    <TreatWarningsAsErrors>true</TreatWarningsAsErrors>
    <ImplicitUsings>true</ImplicitUsings>
    <LangVersion>latest</LangVersion>
  </PropertyGroup>
  <ItemGroup>
    <PackageReference Include="Status.CodeFormatting" Version="1.0.0">
      <PrivateAssets>all</PrivateAssets>
      <IncludeAssets>runtime; build; native; contentfiles; analyzers; buildtransitive</IncludeAssets>
    </PackageReference>
  </ItemGroup>
</Project>
```

## Code Analyzers that the project adds

This package adds the following analyzers

- [Microsoft.CodeAnalysis.NetAnalyzers](https://github.com/dotnet/roslyn-analyzers)
- [Microsoft.VisualStudio.Threading.Analyzers](https://github.com/Microsoft/vs-threading)
- [AsyncFixer](https://github.com/semihokur/AsyncFixer)
