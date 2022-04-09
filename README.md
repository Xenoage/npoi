## About this fork of NPOI

This experimental update of the [NPOI](https://github.com/nissl-lab/npoi) library removes all `System.Drawing` (GDI+) dependencies and replaces them by [`SixLabors.ImageSharp`](https://github.com/SixLabors/ImageSharp) dependencies. It was started because `System.Drawing` is deprecated starting from .NET 6 on non-Windows platforms, see [this issue](https://github.com/nissl-lab/npoi/issues/656).

For measuring text, also `System.Drawing` was used. This is not supported by `SixLabors.ImageSharp` and all those method bodies were commented out (search for `TODO-SixLabors.Fonts`, all affected placed were marked with this comment). Thus, calling methods like `ISheet.AutoSizeColumn` have no effect. These features could be added by using libraries like `SixLabors.Fonts`.

See the [NPOI](https://github.com/nissl-lab/npoi) project for further information.

### NuGet package

We have created an experimental [NuGet package](https://www.nuget.org/packages/Xenoage.Experimental.NPOI.OOXML.Core.WithoutSystemDrawing).
