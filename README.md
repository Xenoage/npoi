## About this fork of NPOI

This experimental update of the [NPOI](https://github.com/nissl-lab/npoi) library removes all `System.Drawing` (GDI+) dependencies and replaces them by [`SixLabors.ImageSharp`](https://github.com/SixLabors/ImageSharp) dependencies. It was started because `System.Drawing` is deprecated starting from .NET 6 on non-Windows platforms, see [this issue](https://github.com/nissl-lab/npoi/issues/656).

For measuring text, also `System.Drawing` was used. This is not supported by `SixLabors.ImageSharp` and all those method bodies were commented out. Thus, calling methods like `ISheet.AutoSizeColumn` have no effect. These features could be added by using libraries like `SixLabors.Fonts`.

See the [NPOI](https://github.com/nissl-lab/npoi) project for further information.
