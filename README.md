# Baml2Xaml

A C# utility for converting BAML (Binary Application Markup Language) files back into readable XAML format. This tool is particularly useful when decompiling .NET applications to recover the original XAML markup from compiled BAML resources.

## Overview

BAML2XAML reads binary BAML files and reconstructs the original XAML markup, making it easier to:
- Analyze and understand the structure of compiled WPF applications
- Recover original XAML source code from compiled assemblies
- Debug issues in compiled XAML resources
- Improve readability of decompiled WPF applications

## Features

- Converts BAML binary format to human-readable XAML text
- Preserves the original structure and formatting of the XAML
- Handles complex XAML elements including:
  - Element hierarchies
  - Attributes and properties
  - Resource dictionaries
  - Namespaces
  - Type declarations
  - Complex property elements
  - Markup extensions
- Supports standard WPF types and custom assemblies
- Maintains proper indentation in the output XAML

## Usage

1. Build the project or run the compiled executable
2. When prompted, enter the full path to your BAML file
3. The tool will automatically create a new XAML file in the same directory
   - The output file will have the same name as the input file but with a `.xaml` extension
   - For example: `MyWindow.baml` → `MyWindow.xaml`

```bash
Por favor, entradar una linea por el archivo BAML
C:\Path\To\Your\File.baml
```

## Requirements

- .NET Framework (compatible with the version used to compile the BAML)
- Read access to the BAML file
- Write access to the output directory

## Limitations

- Only processes valid BAML files (MSBAML format)
- Requires BAML version compatibility (currently supports version 0x00600000)
- Some complex markup extensions might need manual adjustment
- Custom controls must have their assemblies available for proper type resolution

## Error Handling

The tool includes basic error handling:
- Validates BAML format and version
- Reports conversion errors to the console
- Ensures proper file handling with using statements
- Gracefully handles invalid input files

## Contributing

Feel free to contribute to this project by:
- Reporting issues
- Suggesting improvements
- Submitting pull requests
- Adding support for newer BAML versions
