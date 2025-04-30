---
title: Skúška
---


## Ústna skúška

* **Predbežné riadne termíny v AIS:**
  * Piatok 23.5. 13:00 (miestnosť F2-T3)
  * Pondelok 26.5. 9:00 a 13:00 (miestnosť F1-248 doobeda, I-H3 poobede)
  * Utorok 27.5. 9:00 a 13:00 I-H3 (miestnosť I-H3)
  * Každý poldeň má limit 10 študentov, celkové trvanie cca 2,5 hodiny, bude známy približný časový rozpis
  * Zapíšte sa v AIS od stredy 30.4. 18:00
  * Nejaké vážne konflikty?
* Po príchode do počítačovej miestnosti si projekt vašej skupiny otvorte na školskom počítači (Windows alebo Linux), ubezpečte sa, že ho viete spustiť, spravte si kópiu, ktorú budete modifikovať. Vypnite AI asistentov.
* Porozprávame sa o projekte, dostanete za úlohu niečo doňho dorobiť alebo zmeniť.
* Môžete hľadať v prednáškach a cvičeniach, v online dokumentácii alebo v existujúcich diskusiách na internete, môžete si doniesť aj papierové materiály.
* Zakázané je komunikovať s inými osobami a využívať nástroje umelej inteligencie, ako aj iný hardvér okrem školského počítača (ako zálohu pre prípad veľkých technických problémov však odporúčame priniesť si aj vlastný notebook).
* Využité zdroje nechajte otvorené v prehliadači.
* Môžeme sa spýtať aj niečo k vašim individuálnym či skupinovým úlohám.
* Váha skúška je 15%, treba však získať aspoň polovicu, inak Fx. Na základe ústnej skúšky môžeme zmeniť aj vaše body z projektu/úloh, pokiaľ zistíme, že váš prínos k práci skupiny nebol dostatočný alebo že odovzdanej práci nerozumiete.
* Opravné termíny budú neskôr, po dohode s tými, ktorých sa budú týkať. Budú najviac dva ďalšie termíny.


## Záverečný test

* Riadny termín piatok 30.5. 9:00. Nejaké vážne konflikty?
  * Opravné termíny po dohode s tými, ktorých sa budú týkať. Budú najviac dva ďalšie termíny.
* Prineste si perá/ceruzky a ISIC.
* Nie je povolené: akékoľvek papiere, elektronické zariadenia, komunikácia s inými ľuďmi okrem vyučujúcich
* Píšte do priestoru vyhradeného pre každú otázku, v prípade potreby si vyžiadajte ďalší papier
* Píšte čitateľne, nečitateľné odpovede budú hodnotené 0 bodmi
* Trvanie testu 60-90 minút (bude oznámené na začiatku testu)
* Otázky budú v slovenčine, pre prehľadnosť budú uvedené anglické výrazy
* Na úspešné absolvovanie kurzu musíte získať aspoň 50% bodov z testu
* Nižšie je uvedený zoznam pojmov, ktoré by ste mali poznať (pre každý pojem definícia, ak bola uvedená, intuitívny význam, výhody/nevýhody atď.)
* Taktiež je tu zoznam príkazov z knižníc pandas/matplotlib/seaborn a ich parametre, ktoré by ste mali poznať
* Ak použijeme aj iné príkazy z týchto knižníc, budú vysvetlené v texte otázky
* Typy otázok:
  * jednoduché otázky na vedomosti/pochopenie (podobné niektorým kvízovým otázkam)
  * čo by tento kód urobil s týmto vstupom?
  * ako doplniť kód tak, aby robil xyz? (napríklad pridanie jedného príkazu, nie písanie celého dlhšieho kódu)
  * diskutovať o grafe s ohľadom na niektoré aspekty preberané v kurze
  * navrhnúť, ako by ste znázornili určitý typ údajov
  * prípadne aj iné

## Test syllabus

### L01b Matplotlib

* `figure,axes = plt.subplots(nrows, ncols, sharex, sharey)`
* `axes.plot(x, y, fmt, label)` (`fmt` options `'.'`, `'-'`, `'.-'`)

### L02 Pandas

* `df = pd.DataFrame({'col1_name':col1_data,...})`
* `df.iloc[1,2]`
* `df.iloc[[0, 2, 3], 0:2]`
* `df.iloc[[True, False, True, True], :)`
* `df.sort_values(column, inplace)`
* `df.copy()`
* `df.set_index()`
* `df.reset_index()`
* `df.loc[]`
* `series1 + series2`, `series + number`, similarly `-`, `/`, `*`, `>` etc.
* `df.query(...)`
* wide vs. long table

### L03 Plot types, matplotlib, seaborn

* Types of variables: categorical / qualitative vs numerical / quantitative; nominal, ordinal, discrete, continuous, ratio, interval
* Different plot types (what types variables to use it for, advantages, disadvantages)
  * scatterplot (additional variable as color, size, shape; use of log axes)
  * line graph
  * area graph
  * small multiples
  * bar graph (horizontal/vertical, additional variable as color, stacked)
  * dot plot
  * heatmap
  * pie chart
  * strip plot
  * histogram
  * parallel coordinates
  * parallel categories
  * radar chart
* `sns.scatterplot(data, x, y, hue, size, col)`
* `sns.barplot(data, x, y, hue)`

### L04 Summary statistic

* For each statistic: definition, intuive meaning, properties
* Measures of central tendency: mean, median, mode
* Quantiles, percentiles and quartiles
* Measures of variability minimum, maximum, interquartile range, variance and standard deviation
* Tukey's definition of outliers using IQR
* Boxplot
* Summary statistics under linear transformation of the variable
* Pearson correlation coefficient
* Spearman’s rank correlation coeﬀicient
* Correlation does not imply causation
* Computation in Pandas:
  * `series.mean()`, `series.median()`, `series.mode()`
  * `series.quantile([p0,...,pn])`, linear interpolation
  * `series.min()`, `series.max()`, `series.std()`
  * `sns.boxplot(data, x, y)`
  * `df.describe()`
  * `df.corr()`
  * `sns.pairplot(df)`

### L05 Pandas 2

* `pd.merge(df1, df2, on)`
* split-apply-combine strategy, apply as aggregation, transformation, filtering
* `df.groupby(column)[column_selection].aggregation_function()` with aggregation functions `size()`, `count()`, `sum()`, `mean()`, `median()`, `min()`, `max()`, `describe()`
* `df.groupby(column)[column_selection].transform(function)`
* `df.groupby(column)[column_selection].filter(function)`
* Missing values as `np.nan`

### L06 Maps, graphs, time series

* Map projections: conformal / equal-area / orthographic
* Thematic maps
* Data as points or lines in a map
* Isarithmic maps / isoline maps / heatmaps
* Choropleth maps, spatially extensive/intensive variables
* Graph terminology (vertices, edges, tree), basics of graph drawing
* Time series: smoothing with aggregation and sliding window, overlapping timescales, uncertainty and missing values

### L07 More statistics

* Histograms (which properties of data thet show, choice of bins, comparing several distributions)
* `sns.histplot(data, x, bins, hue, multiple, common_norm)` (for `multiple` option `"stack"`)
* Probability density function (and its relation to histograms)
* Kernel density estimation (how it is constructed, how it is used, bandwidth)
* Violin plot
* Two-dimensional histograms / KDE
* Cumulative distribution function (definition, properties)
* Empirical cumulative distribution function (definition, properties, use for visualization)
* Clustering (intuitive meaning, use for improving heatmaps)
* Dimensionality reduction (intuitive meaning, use for visualizing high-dimensional data)

### L08 Visual perception and colors

* Light as a mixture of wavelengths
* Human eye: retina, photoreceptors, cones and rods, cones with three wavelengths
* Foveal vs peripheral vision
* Metamers, LMS color space
* Additive color models, RGB, HSL, HSV
* Subtractive color models, CMY(K)
* Color wheel, RYB model, primary and secondary colors, complementary color scheme
* Issues to consider in visualization (color blindess, technical limitations, use for highlighting)
* Palettes in visualization: qualitative, quantitative sequential, quantitative diverging
* Raster vs vector image formats
* Data analysis project phases, exploratory vs explanatory visualization

### L09 Text, visual perception (2)

* Text visualization: word clouds vs other techniques for showing word frequencies
* Pre-attentive attributes and their use in visualization
* Hierarchy of graph elements for quantitative reasoning
* Gestalt principles of proximity, similarity, connection, enclosure, closure, continuity and their use in visualization
* Illusions
* Working memory
* Chart junk

### L10 Presentation of results

* Context of a presentation
* Storytelling in a presentation
* Cognitive biases, patternicity bias, storytelling bias, conformation bias
* Aspects of visualization: basic setup, data transformations and other settings, focus and explatation
* Table vs plot
* Infographics vs data visualization

### L11 Interactivity, other types of plots

* Interactivity, which aspects of a plot can be interactive
* Dashboard (what it is)
* Other types of graphs: waterfall chart, funnel chart, Gannt chart, candlestick chart
