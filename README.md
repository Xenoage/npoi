## About this fork of NPOI

This experimental update of the [NPOI](https://github.com/nissl-lab/npoi) library removes all `System.Drawing` (GDI+) dependencies and replaces them by using the [`SixLabors.ImageSharp`](https://github.com/SixLabors/ImageSharp) and [`SixLabors.Fonts`](https://github.com/SixLabors/Fonts) libraries. It was started because `System.Drawing` is deprecated starting from .NET 6 on non-Windows platforms, see [this issue](https://github.com/nissl-lab/npoi/issues/656).

See the [NPOI](https://github.com/nissl-lab/npoi) project for further information.

### NuGet package

We have created an experimental [NuGet package](https://www.nuget.org/packages/Xenoage.Experimental.NPOI.OOXML.Core.WithoutSystemDrawing).
