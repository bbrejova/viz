---
title: Test syllabus
---

## General test rules

* Bring your pens /pencils etc and ISIC
* Not allowed: any papers, electronic devices, communications with other people except instructors
* Write to the space allocated for each question, ask for additional paper if necessary
* Write legibly, illegible answers will get 0 points
* Duration of the test 60-90 minutes (will be announced at the start of the test)
* You need to get at least 50% of the grade on the test to pass the course
* Below you have a list of terms you should know (definition if given, intuitive meaning, advantages/disadvantages etc.)
* Also there is a list of pandas/matplotlib/seaborn commands and their parameters you should know
* If other commands from these libraries appear, they will be explained in the text
* Typical types of questions
  * simple knowledge / understanding questions (as many quiz questions)
  * what would this code do on this input?
  * how to complete the code so that it does xyz? (adding a single command or choosing from options)
  * discuss a plot with respect to some aspects covered in class

## L01b Matplotlib

* `figure,axes = plt.subplots(rows, columns, sharex, sharey)`
* `axes.plot(x,y,fmt,label)` (`fmt` options `'.'`, `'-'`, `'.-'`)

## L02 Pandas

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

## L03 Plot types, matplotlib, seaborn

* Types of variables: categorical / qualitative vs numerical / quantitative; nominal, ordinal, discrete, continuous, ratio, interval
* Different plot types (what types variables to use it for, advantages, disadvantages)
  * scatterplot, additional variable as color, size, shape, log axes
  * line graph
  * area graph
  * small multiples
  * bar graph, horizontal/vertical, additional variable as color, stacked
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

## L04 Summary statistic

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

## L05 Pandas 2

* `pd.merge(df1, df2, on)`
* split-apply-combine strategy, apply as aggregation, transformation, filtering
* `df.groupby(column)[column_selection].aggregation_function()` with aggregation functions `size()`, `count()`, `sum()`, `mean()`, `median()`, `min()`, `max()`, `describe()`
* `df.groupby(column)[column_selection].transform(function)`
* `df.groupby(column)[column_selection].filter(function)`
* Missing values as `np.nan`

## L06 Maps, graphs, time series

* Map projections: conformal / equal-area / orthographic
* Thematic maps
* Data as points or lines in a map
* Isarithmic maps / isoline maps / heatmaps
* Choropleth maps, spatially extensive/intensive variables
* Graph terminology (vertices, edges, tree), basics of graph drawing
* Time series: smoothing with aggregation and sliding window, overlapping timescales, uncertainty and missing values

## L07 More statistics

* Histograms: properties of data shown, choice of bins, comparing several distributions
* `sns.histplot(data, x, bins, hue, multiple, common_norm)` (for `multiple` option `"stack"`)
* Probability density function, relation to histogram
* Kernel density estimation (how is it constructed, how is it used, bandwidth)
* Violin plots
* Two-diensional histograms / KDE
* Cumulative distribution function (definition, properties)
* Empirical cumulative distribution function (definition, properties, use for visualization)
* Clustering (meaning, use for improving heatmaps)
* Dimensionality reduction (meaning, use for visualizing high-dimensional data)

## L08 Visual perception and colors

* Light as a mixture of wavelengths
* Human eye: retina, photorecpetors, cones and rods, cones with three wavelengths
* Foveal vs peripheral vision
* Metamers, LMS color space
* Additive color models, RGB, HSL, HSV
* Subtractive color models, CMY(K)
* Color wheel, RYB model, primary and secondary colors, complementary color scheme
* Issues to consider in visualization (color blindess, technical limitations, use for highlihting)
* Palettes in visualization: qualitative, quantitative sequential, quantitative diverging
* Raster vs vector image formats
* Data analysis project phases, exploratory vs explanatory visualization

## L09 Text, Visual perception (2)

* Text visualization: word clouds vs other techniques for showing word frequencies
* Pre-attentive attributes and their use in visualization
* Hierarchy of graph elements for quantitative reasoning
* Gestalt principles of proximity, similarity, connection, enclosure, closure, continuity and their use in visualization
* Illusions
* Working memory
* Chart junk

## L10 Presentation of results

* Context of a presentation
* Storytelling in a presentation
* Cognitive biases, patternicity bias, storytelling bias, conformation bias
* Aspects of visualization: basic setup, data transformations and other settings, focus and explatation
* Table vs plot
* Infographics vs data visualization

## L11 Interactivity, other types of plots

* Interactivity, which aspects of a plot can be interactive
* Dashboard (what it is)
* Other types of graphs: waterfall chart, funnel charts, Gannt chart, candlestick chart
