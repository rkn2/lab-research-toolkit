# Making Figures

A good figure communicates one idea clearly. A bad figure makes the reader work to extract information that should be obvious. This guide covers the principles behind effective research figures and the practical tools to make them.

---

## The Core Principle: Data-Ink Ratio

Edward Tufte, the foundational thinker on data visualization, introduced the concept of the **data-ink ratio**: the proportion of a figure's ink that is actually encoding information versus ink that is decorative or redundant.

> "Above all else, show the data." — Edward Tufte

The goal is to maximize the data-ink ratio. Every element of a figure should earn its place by communicating something. If it does not, remove it.

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
- **Matplotlib documentation** — matplotlib.org; the gallery is a useful starting point for code examples
