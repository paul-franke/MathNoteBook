# Copilot Instructions for Math Repository

## Overview
This repository features a .NET Interactive notebook (`ScottPlot.ipynb`) demonstrating mathematical plotting using ScottPlot, a .NET library for creating high-quality plots.

## Architecture
- **Main Component**: Single Jupyter notebook with polyglot-notebook cells (C# code).
- **Purpose**: Exploratory data visualization for mathematical functions and data series.
- **Data Flow**: Generate data arrays, create Plot objects, add scatter/function plots, display/save results.

## Key Workflows
- **Running Code**: Use VS Code with .NET Interactive extension. Execute cells sequentially to load dependencies and display plots inline.
- **Plotting**: Instantiate `ScottPlot.Plot`, add data via `Add.Scatter()` or `Add.Function()`, customize labels/titles, save as PNG.
- **Dependencies**: Load ScottPlot via `#r "nuget:ScottPlot, 5.0.*"` in the first cell.

## Conventions and Patterns
- **Formatter Registration**: Use `Formatter.Register()` for inline plot display in notebooks (e.g., `((ScottPlot.Plot)p).GetPngHtml(400, 300)`).
- **Data Generation**: Create double arrays for x/y data, often in loops for mathematical series (see Fourier analysis example in `ScottPlot.ipynb` lines 89-135).
- **Plot Customization**: Set axis limits manually for functions (`plt.Axes.SetLimits(-10, 10, -1.5, 1.5)`), add titles/labels.
- **Output**: Display plots directly in cells; save to files like `demo.png` using `SavePng()`.
- **Language**: C# with standard .NET math functions (Math.Sin, Math.Cos).

## Integration Points
- **External Dependencies**: ScottPlot NuGet package (version 5.0.*).
- **No External Services**: Self-contained notebook for local execution.

## Key Files
- `ScottPlot.ipynb`: Primary notebook with examples of scatter plots, function plots, and Fourier series visualization.

Focus on adding new cells for additional mathematical plots or extending existing examples with more complex data.</content>
<parameter name="filePath">d:\repos\Math\.github\copilot-instructions.md