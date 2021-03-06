# The Great Human Experiment by the Numbers

Welcome! This is the private GitHub repository for our course. Over the length
of the course, you will periodically deposit data you collect from the internet
to this repository following the guidelines enumerated below. We will keep this
repository updated and properly annotated such that all members of the course
will have access to the highest quality data to assess the human impact on the
planet. 

This repository *will NOT* contain any grade reports or identifying information
about you or your enrollment in the course. If you do not wish to use GitHub,
please email Griffin `gchure@caltech.edu` to set up an alternative scheme to
access and deposit data. 

## Using The Repository
Being able to use Git and GitHub is vital to keep track of the data. There are 
many tutorials showing how to use both of these efficiently. If you are not
familiar with Git and GitHub, please review the following tutorials:

* [Version Control with
  Git](http://justinbois.github.io/bootcamp/2019/lessons/l12_version_control_with_git.html)
  by [Justin Bois](http://bois.caltech.edu) at Caltech.
* [Tips and Traps with Git and GitHub](http://bebi103.caltech.edu.s3-website-us-east-1.amazonaws.com/2019a/content/recitations/recitation_02/index.html) by Muir Morrison at Caltech.

Note that in using this repository, it is imperative that you give coherent and
meaningful commit messages. 

## Repository Structure

> :warning: An example data file has been added to `flora_fauna/` if you want to
> learn by example how to manage this repository.

The bare bones of the repository is already in place. Within each folder, you
will find a `README.md` file explaining the purpose of the folder and other
information that will help you manage the repository. The structure of this
repository is very much in its infancy and may change! Keep track of this
`README.md` file to see if things are changing. 

If you are confused with the layout of the repository or have comments on how
things could be changed to improve it, please [open an
issue](https://github.com/rpgroup-pboc/aph150_2020/issues) on this
repository.

This repository houses all *raw* data sets collected from the internet. This
repository is broken down into four separate subdirectories. Of course, some
data sets will fall into multiple categories. When adding your data to the
repository, choose what you think is the best match. 
+ **`food`**: All data sets related to food generation and consumption. + **`water`**: All
data sets related to water consumption and usage. 
+ **`air`**: All data sets related to atmospheric impacts. 
+ **`earth`**: All data sets related to land usage. This may include data
  relating to anthropomass, farmland, city sizes, etc. 
+ **`flora_fauna`**: All data sets pertaining to humans impact on the biosphere. 
+ **`other`**: All data sets which do not fit into any of the above categories.

Within each of these subdirectories, there will be yet *another* directory
for a given data set. The naming of this subdirectory is much less clear cut
and will depend on the nature of the data set. That being said, you should
name the folder of your deposited data set in a clear manner. For example,
say you collect a data set which tabulates the global population by country
for the years 1820 - 2020. You would deposit this data set under
`flora_fauna` in another directory titled `world_population_1820-2020`.
Within this folder, you would deposit the data along with a `README.md` file,
as is described in the next section.

## Data Types
Data can be added to these folders in a variety of formats, but they must be
text-based. This means that spreadsheets (`.xslx` or `.numbers`) should be
converted to plain-text data formats (`.txt` or `.csv`) whenever possible.
Large data sets (≥ 100 MB) will need to be added using the [GitHub Large File
Storage](https://git-lfs.github.com/) system. *Email Griffin
(`gchure@caltech.edu`) for guidance on how to deal with this.* Some of the
data you collect in this data set may be a single number or statistic. Even if
this is the case, it should be added to this folder as a text-based file. 

In general, data should be stored in a [longform, tidy
format](https://www.jstatsoft.org/article/view/v059i10). In this format, each
measurement will get one row. Unfortunately, the raw data you get from the
internet will rarely be in this very convenient format meaning that you will
have to reformat your data to be "tidy". 

For example, Consider the world population in our fictional data set described
above. The raw data set may look something like the following:

| country | 1820 | 1821 | 1822 | ...|
|:--|:--|:--|:--|:--|
| Afghanistan | 3290000 | 3300000| 3310000| ... |
| Albania | 437000| 439000 | 441000| ... |
| ... | ...| ... |... |...| 


This is **not** in tidy format. Rather than having each year as a column, each
year would be a row. Transforming the data into tidy format would make it look
like the following:

| country | year | population |
|:--|:--|:--|
|Afghanistan| 1820 | 32900000|
|Afghanistan| 1821 | 3300000 |
|Afghanistan| 1822 | 3310000 |
| ... | ... | ... |
|Albania | 1820 | 437000 |
|Albania | 1821 | 439000 | 
|Albania | 1822 | 441000 |
| ... | ... |...| 

To ensure that things are properly transformed, you should include the raw data
and the tidy data in the repository.  The original data for our hypothetical
example would be saved as 

```
world_population_1820-2020_raw.csv
```

with the tidy format being renamed to 

```
world_population_1820-2020_tidy.csv
```

For large data sets, this is impossible to do manually and this may require some
computational cleaning of data. 

## Annotation
Every data set you add to this repository *MUST* be accompanied by `README.md`
file describing several features of the data set. This is not optional and
*MUST* follow a particular structure outlined in `README_TEMPLATE.md`. 

The data set readme file has several fields which you will need to populate when
you add your data set. This will make curating the data sets much more manageable
and human readable. Please see the `README_TEMPLATE.md` file for more
information about what to include. 

## Software
During the course, you may want to computationally explore some of the data sets
and make visualizations. Great! We want you to do this and have fun with it.
There is no expectation of a specific programming language and you are free to
use what you see fit. However, you must have your code properly commented and
annotated such that other members of the repository can reproduce your work in
another programming language. 

Any code you write to analyze a data set must be housed within a `code`
subdirectory in your deposited data folder. Consider our example of a
hypothetical data set containing the global population from the years
1820-2020 by country. Say that you wanted to generate a plot of the
population of Brazil over these years using python. The script you use to
generate the plot (`brazil_population.py`)  and the generated plot itself 
(`brazil_population.pdf`) would be housed in the associated folders as
follows. 

```
flora_fauna /
|
|--> world_population_1820-2020/
     |
     | --> world_population_1820-2020_raw.csv
     | --> world_population_1820-2020_tidy.csv
     | --> code/
           |
           |--> brazil_population.py
     | --> media/
           |
           |--> brazil_population.pdf
```

Please see the  data set already present in this directory for a complete example.

## Academic Integrity and Honesty
By using this repository, you are expected to abide by the [Caltech Honor
Code](https://deans.caltech.edu/HonorCode). If you are using this repository and
are *not* enrolled or employed by Caltech, you are still considered a member of
the Caltech community and must abide by the Honor Code.  The Caltech honor code
is simple:

> No member of the Caltech community shall take unfair advantage of any other member of the Caltech community.

## License
All software within this repository that originates from the class should be
licensed under the standard MIT license as is given below. All creative work
originating from this course (e.g. writing and graphics) is similarly
licensed under a [Creative Commons CC-BY
4.0](https://creativecommons.org/licenses/by/4.0/) permissive license. All
data, creative works, and software *not* originating from this course carry
the original license and copyright as is present in the source material.

```
Copyright 2020 The Authors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```