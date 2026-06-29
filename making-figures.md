# Making Figures

A good figure communicates one idea clearly. A bad figure makes the reader work to extract information that should be obvious. This guide covers the principles behind effective research figures and the practical tools to make them.

**Jump to:**
- [The Core Principle: Data-Ink Ratio](#the-core-principle-data-ink-ratio)
- [Choosing the Right Chart Type](#choosing-the-right-chart-type)
- [Chart Junk](#chart-junk)
- [Color](#color)
- [Typography and Labels](#typography-and-labels)
- [Tools](#tools)
- [Figure Checklist](#figure-checklist)
- [Further Reading](#further-reading)

---

## The Core Principle: Data-Ink Ratio

Edward Tufte, the foundational thinker on data visualization, introduced the concept of the **data-ink ratio**: the proportion of a figure's ink that is actually encoding information versus ink that is decorative or redundant.

> "Above all else, show the data." — Edward Tufte

The goal is to maximize the data-ink ratio. Every element of a figure should earn its place by communicating something. If it does not, remove it.

---

## Choosing the Right Chart Type

Before you make a figure, decide what relationship in the data you are trying to show. The chart type follows from the *question*, not the other way around. Most research figures answer one of these:

| You want to show... | Use | Avoid |
|---|---|---|
| How one quantity changes over a continuous variable (time, load, distance) | Line chart | Bar chart for continuous x |
| Comparison of a value across discrete categories | Bar chart (horizontal if labels are long) | Pie chart |
| The relationship between two continuous variables | Scatter plot (add a fit line only if justified) | — |
| The distribution / spread of a single variable | Histogram, box plot, or violin plot | A single mean ± error bar that hides the spread |
| Distribution across groups | Grouped box / violin, or a strip/swarm plot for small n | Bar-of-means ("dynamite plot") — it hides the actual data |
| Parts of a whole | Stacked bar, or just a table | Pie chart (humans compare angles poorly) |
| A value over two dimensions (a field, a matrix) | Heatmap with a perceptually uniform colormap | Rainbow/jet colormap |
| Spatial data | A map (QGIS) | A table of coordinates |

**Two rules that catch most mistakes:**
- **Show the data, not just a summary.** With small sample sizes, plot the individual points (strip/swarm/jitter) rather than only a mean and error bar. A bar of means can hide that your "difference" is two clouds that overlap completely.
- **Match the chart to the variable type.** Continuous x → line or scatter. Categorical x → bar. Mixing these (a bar chart across a continuous axis) misleads the reader about what is and is not measured.

**Decision tools — when you are unsure, use these:**
- **[From Data to Viz](https://www.data-to-viz.com/)** — a decision tree: tell it what kind of data you have, and it shows the appropriate chart types (with code and common caveats for each).
- **[Peer Recognized: Research Data Visualization](https://peerrecognized.com/dataviz/)** — practical chart-selection guidance, color-palette tools, and a **downloadable data visualization cheat sheet** that maps data types to chart types on one page. Keep the cheat sheet handy when you are drafting figures.
- **[Data Visualization Catalogue](https://datavizcatalogue.com/)** — a reference of chart types, each with a description of when (and when not) to use it.

---

## Chart Junk

Chart junk is everything in a figure that does not help the reader understand the data. Common offenders:

**Remove these:**
- 3D effects on 2D data (3D bar charts, pie charts with depth) — they distort perception and add nothing
- Gradient fills and drop shadows on bars or areas
- Heavy grid lines — if you need them, make them light gray
- Borders around the entire figure
- Unnecessary tick marks
- Redundant legends (if you only have one data series, you do not need a legend)
- Decorative background colors or images behind data
- Clip art and icons used as decoration

**Be skeptical of:**
- Pie charts — humans are poor at comparing angles; use a bar chart instead
- Dual y-axes — they are almost always misleading; find another way
- Smoothed lines through noisy data that imply more certainty than exists

---

## Color

Color is one of the most misused elements in scientific figures.

**Use color to encode information, not to decorate.** If changing the color of an element would not change what the figure communicates, the color is probably decorative.

**Colorblind accessibility:** About 8% of men have red-green color blindness. Do not rely on red vs. green to distinguish categories. Use colorblind-friendly palettes — the Viridis, Cividis, and ColorBrewer palettes are designed for this.

**Perceptual uniformity:** In heatmaps and continuous scales, use perceptually uniform colormaps (Viridis, Plasma, Magma) rather than rainbow/jet colormaps. Rainbow colormaps create false visual boundaries and obscure real gradients.

**Print-friendly:** Figures may end up printed in grayscale. Check that your figures are still readable without color.

---

## Typography and Labels

- **Font size:** Axis labels, tick labels, and captions should be readable at the size the figure will appear in the paper. A common mistake is making text too small in a large figure that will be scaled down.
- **Label axes always.** Include units. "Displacement (mm)" not just "Displacement."
- **Captions should be self-contained.** A reader should be able to understand your figure without reading the surrounding text. Define abbreviations and describe what is shown.
- **Significant figures:** Report values to a precision that is meaningful, not just whatever your software outputs.

---

## Tools

### Matplotlib (Python)
The standard for programmatic figure generation in research. Figures made in code are reproducible — if your data changes, you regenerate the figure, you do not redraw it.

```python
import matplotlib.pyplot as plt
import matplotlib as mpl

# Use a clean style
plt.style.use('seaborn-v0_8-whitegrid')

fig, ax = plt.subplots(figsize=(6, 4))
ax.plot(x, y, color='#2563EB', linewidth=1.5, label='Model prediction')
ax.scatter(x_data, y_data, color='#DC2626', s=20, label='Observed')
ax.set_xlabel('Time (s)', fontsize=11)
ax.set_ylabel('Displacement (mm)', fontsize=11)
ax.legend(frameon=False)

# Remove top and right spines (cleaner look)
ax.spines['top'].set_visible(False)
ax.spines['right'].set_visible(False)

plt.tight_layout()
plt.savefig('figure1.pdf', dpi=300, bbox_inches='tight')
```

Save figures as **PDF or SVG** for vector output (infinitely scalable, looks sharp at any size) or **PNG at 300 dpi minimum** for raster output.

### Adobe Illustrator
For figures that require manual layout, diagrams, or polishing of programmatically generated figures. Export from Python as PDF or SVG, open in Illustrator to adjust typography and layout.

### QGIS
For maps and spatial data visualization. Open source and free. Use it to make publication-quality maps from GIS data.

### Inkscape
A free alternative to Illustrator for vector editing. Less powerful but sufficient for most figure cleanup tasks.

---

## Figure Checklist

Before submitting any figure, ask:

- [ ] Does this figure communicate one clear idea?
- [ ] Have I removed everything that does not directly encode information?
- [ ] Are all axes labeled with units?
- [ ] Is the font size readable at the size it will appear in print?
- [ ] Is the color palette colorblind-friendly?
- [ ] Does the caption fully describe what is shown?
- [ ] Is the resolution sufficient (300 dpi minimum for raster)?
- [ ] Would this figure still make sense in grayscale?

---

## Further Reading

- **Edward Tufte, *The Visual Display of Quantitative Information*** — the foundational text; read the first half at minimum
- **Claus Wilke, *Fundamentals of Data Visualization*** — free online at clauswilke.com/dataviz; practical and directly applicable
- **[Peer Recognized: Research Data Visualization Tools](https://peerrecognized.com/dataviz/)** — practical guide to chart selection, color palette tools, and software options; includes a downloadable cheat sheet
- **[Peer Recognized: Research Data Visualization Book](https://peerrecognized.com/visualization/)** — deeper treatment of visualization principles for scientific graphics
- **[From Data to Viz](https://www.data-to-viz.com/)** — decision tree for choosing the right chart type for your data
- **[Data Visualization Catalogue](https://datavizcatalogue.com/)** — reference for chart types with descriptions of when to use each
- **Matplotlib documentation** — matplotlib.org; the gallery is a useful starting point for code examples
