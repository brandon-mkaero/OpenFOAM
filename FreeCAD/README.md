# ExportSurfacesToFOAM.FCMacro

ExportSurfacesToFOAM.FCMacro is a FreeCAD macro designed to streamline the process of converting and exporting surfaces to mesh files. Based on the well-established "Batch Export Surfaces to Mesh" macro, this version introduces additional functionality to better serve workflows that require ASCII STL exports (.ast) and a consolidated export of all surfaces with patch labels. These enhancements are especially useful for users preparing meshes for computational fluid dynamics (CFD) simulations using tools such as OpenFOAM.

## Overview

The macro automates the process of exporting multiple FreeCAD objects to mesh formats, with support for:

- Standard binary STL and OBJ exports.
- **ASCII STL (.ast) exports** for users needing text-based mesh data.
- Exporting all selected surfaces into a **single mesh file** where each surface is clearly marked with patch labels, allowing for easier post-processing in CFD applications.

## Features

- **Batch Export**: Convert one or several FreeCAD objects into mesh files in one go.
- **Multiple File Formats**: Supports traditional binary STL, ASCII STL (.ast), and Alias mesh (.OBJ) exports.
- **Enhanced .ast Support**:
    - Direct export to the .ast format.
    - Ability to merge individual .ast files into one consolidated file named `domain.stl`, where each mesh is tagged with its corresponding patch label.
- **GUI Integration**: A user-friendly interface within FreeCAD for setting parameters such as surface and angular deviation, file naming options, and saving directories.
- **Preset Management**: Save and load custom presets for different export configurations.
- **Local/Global Coordinates**: Option to export using local or global coordinate systems.

## Requirements

- **FreeCAD**: Tested with FreeCAD version 0.17 and above.
- **Python**: Comes with Python libraries included with FreeCAD.
- **Dependencies**: Standard dependencies include FreeCAD modules, PySide for the GUI, and MeshPart for mesh operations.

## Installation

1. **Download the Macro**: Clone or download the repository to your local machine.
2. **Place the File**: Copy `ExportSurfacesToFOAM.FCMacro` into your FreeCAD macros directory.
3. **Launch FreeCAD**: Open FreeCAD and navigate to the macros menu.
4. **Run the Macro**: Select `ExportSurfacesToFOAM.FCMacro` and click **Execute**.

## Usage

1. **Select Objects**: In your FreeCAD project, select the surfaces or objects you wish to export.
2. **Configure Parameters**:
    - Adjust surface deviation, angular deviation, and choose between relative or absolute deviation.
    - Choose your preferred file format from STL (binary), STL (ASCII Combined), ASCII STL (.ast), or OBJ.
    - Set the output directory and naming options (Label, Project, or Custom).
3. **Execute Export**: Click the “Convert” button to generate meshes and then “Save to file” to export them.
4. **Post-Processing**: For ASCII STL exports, the macro will either output individual .ast files or merge them into a single file with patch labels, making it easier to identify individual surfaces in downstream applications like OpenFOAM.

## Contributing

Contributions, suggestions, and bug reports are welcome! Feel free to open issues or submit pull requests if you have improvements or fixes.

## License

This project is licensed under the [GNU Lesser General Public License (LGPL)](https://www.gnu.org/licenses/lgpl-3.0.html).

## Acknowledgements

- **Original Macro**: This macro is based on the original [Batch Export Surfaces to Mesh](https://github.com/pgilfernandez/FreeCAD_Macro_Batch_Export_To_Mesh) macro developed for FreeCAD.
