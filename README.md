# getting-started-python

Some suggested resources for learning Python

::: {.cell .markdown colab_type="text" id="view-in-github"}
`<a href="https://colab.research.google.com/github/Mjboothaus/getting-started-python/blob/main/GettingStartedPythonAnalytics.ipynb" target="_parent">`{=html}`<img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>`{=html}`</a>`{=html}
:::

::: {.cell .markdown id="6cb6gTaBtIEd"}
# Some resources for getting started with Python and analytics

## `TL;DR`

*Choose one of the options below and have a go!*

**Note: At the end of this notebook is some code to demonstrate pulling
data from the web and doing introductory exploration.**

## Introduction

This short document provides a few recommendations for getting started
with the Python language and data analytics. I learnt Python when I was
45 (although I have also programmed in Basic, Fortran, C/C++/C#, VBA,
Matlab, R). I think Python is a very accessible language and it has a
very large package ecosystem to expand on its base functionality
(standard libraries).

There is **no unique path** to follow - we all learn differently -
although I think it is true that most of us learn best by doing i.e.
experimenting with code and solving small problems as we go along. Few
of us \"get the textbook\" and work systematically through it!

Unless otherwise indicated, these resources are available for free (or
the courses can be taken for free in \"audit\" mode).

There are many other quality free and paid resources available online,
however, these are very good starting places.

**Happy problem solving and coding - Enjoy!**
:::

::: {.cell .markdown id="9qkH2hiox4cK"}
### Author

    Dr. Michael J. Booth
    Founder, DataBooth
    michael@databooth.com.au
:::

::: {.cell .markdown id="DiTBx6ToP_cf"}
## Git a Repository

If you\'re going to write some code, setup a free-tier `git` based
respository to track your work. e.g. [GitHub.com](https://github.com),
[GitLab.com](https://gitlab.com) or
[BitBucket.org](https://bitbucket.org).
:::

::: {.cell .markdown id="9loTU1vl0kWs"}
## Options

So, in no particular order\...
:::

::: {.cell .markdown id="4-KeXxXE_F6n"}
## Google Colaboratory (hosted Jupyter notebooks)

That\'s the platform that this document (notebook) is built with/hosted
on. [Jupyter](https://jupyter.org) notebooks are a great/interactive way
to learn. Google has plenty of resources to help you learn about using
their complimentary, computational notebooks (their version of Jupyter
notebooks).

See their excellent introductory overview notebook
[here](https://colab.research.google.com/notebooks/intro.ipynb).
:::

::: {.cell .markdown id="sZXaLcBhvYsq"}
## Replit.com (Game-ified approach) {#replitcom-game-ified-approach}

Replit provides a free, on-demand, collaborative, in-browser IDE to code
in over 50 languages including Python. Consquently it does not require
any explicit setup to get going which makes it a great platform for
newbies with a gamified look and feel :)

Create an account here [Replit.com](https://replit.com) and choose a
Python project to get going.

There are some Python specfic tutorials embedded within the learning
materials on the platform.
:::

::: {.cell .markdown id="bDp3dFaktVmm"}
## IBM courses on Coursera

[Python for Data Science, AI &
Development](https://www.coursera.org/learn/python-for-applied-data-science-ai)
this course can be done as part of a number of specialities - the
following two courses look most relevant:

-   [Data Science Fundamentals with Python and SQL
    Specialization](https://www.coursera.org/specializations/data-science-fundamentals-python-sql)
-   [Data Engineering Foundations
    Specialization](https://www.coursera.org/specializations/data-engineering-foundations)

If I\'m being completely frank, it seems to me that *Data Engineering*
skills are likely to be in greater demand that *Data Science* skills
moving forward (as tools are attempting to commoditise much of the lower
value data \"science\" work) - although there can be significant overlap
between the two areas.
:::

::: {.cell .markdown id="IAlmJaMAtweo"}
## Jose Portilla Udemy Courses - Two (low cost) paid options

-   [2022 Complete Python Bootcamp From Zero to Hero in
    Python](https://www.udemy.com/course/complete-python-bootcamp/)
-   [Python for Data Science and Machine Learning
    Bootcamp](https://www.udemy.com/course/python-for-data-science-and-machine-learning-bootcamp/)

I learnt Python from the first of these two courses. Typically you can
purchase them on Udemy at significant discount for around AUD \$20.
:::

::: {.cell .markdown id="OWb5PQS0ya1c"}
## Tinkerstellar and Juno (options for iOS devices)

If you own an iPad there are a couple of interesting learning resources.
From my testing [Tinkerstellar](https://tinkerstellar.com) and companion
app [Juno](https://juno.sh) feel very solid and are elegant - glossy
magazine style notebooks.

Tinkerstellar is an app that helps you learn coding and data science
with interactive tutorials (or labs), where you can edit and run code
examples straight away --- no need to configure environments, download
datasets or rely on networking connection to execute code. Just download
a lab, and you're ready to play around and experiment with code solving
real-world problems of computational science 🚀.
:::

::: {.cell .markdown id="gipbTOrlICSx"}
## Articles

### [Towards Data Science](https://towardsdatascience.com/about)

-   [9 Free Quality Resources to Learn and Expand Your Python Skills -
    Learn Python regardless of your technical
    background](https://towardsdatascience.com/9-free-quality-resources-to-learn-and-expand-your-python-skills-44e0fe920cf4)

### [Medium](https://medium.com)

-   TODO: Add more references.
:::

::: {.cell .markdown id="U5eG4iL-zr72"}
*p.s. any suggestions, improvements, errors or typos please email me.*
:::

::: {.cell .markdown id="uDUhvNEKAjhP"}

------------------------------------------------------------------------

## Now for a simple example of loading, previewing and profiling data

Some Python code to load some sample data from [NSW Open
Data](https://www.data.nsw.gov.au).
:::

::: {.cell .code execution_count="1" id="9hQ8rUrkNJwP"}
``` python
# Sometimes needed to update the pre-installed version of pandas-profiling (uncomment and run if needed)
#
#pip install -U pandas-profiling
```
:::

::: {.cell .code execution_count="2" id="cdVVDR99AiuT"}
``` python
import pandas as pd  # Pandas is the usual library for doing structured data analysis
from pandas_profiling import ProfileReport
```
:::

::: {.cell .markdown id="p7HJVoXMBSMG"}
### Example **PUBLIC** data set

[COVID-19 cases by notification date and postcode, local health
district, and local government area.csv
(Discontinued)](https://data.nsw.gov.au/search/dataset/ds-nsw-ckan-aefcde60-3b0c-4bc0-9af1-6fe652944ec2/distribution/dist-nsw-ckan-21304414-1ff1-4243-a5d2-f52778048b29/details?q=)

`TIP:` As far as possible, as good practice, keep real data out of your
repository (especially any data with private information).
:::

::: {.cell .code execution_count="3" id="TbRmjG3YBEC1"}
``` python
data_URL = "https://data.nsw.gov.au/data/dataset/aefcde60-3b0c-4bc0-9af1-6fe652944ec2/resource/21304414-1ff1-4243-a5d2-f52778048b29/download/confirmed_cases_table1_location.csv"
```
:::

::: {.cell .code execution_count="4" colab="{\"base_uri\":\"https://localhost:8080/\"}" id="Xnc_UsP6Kj8y" outputId="d831ac2f-3c9b-4945-fb62-0c1ab280e9c9"}
``` python
# Look at first 5 lines of .csv data file
# Example of using Unix command line from within notebook (note the use of '!' before the actual command)

!curl -s $data_URL | head -n 5
```

::: {.output .stream .stdout}
    notification_date,postcode,lhd_2010_code,lhd_2010_name,lga_code19,lga_name19
    2020-01-25,2134,X700,Sydney,11300,Burwood (A)
    2020-01-25,2121,X760,Northern Sydney,16260,Parramatta (C)
    2020-01-25,2071,X760,Northern Sydney,14500,Ku-ring-gai (A)
    2020-01-27,2033,X720,South Eastern Sydney,16550,Randwick (C)
:::
:::

::: {.cell .code execution_count="5" id="8GRAWbqdBcxS"}
``` python
# Load data into a pandas dataframe

data_df = pd.read_csv(data_URL)
```
:::

::: {.cell .code execution_count="6" colab="{\"base_uri\":\"https://localhost:8080/\"}" id="bDOyvmvtL0ez" outputId="b63196b2-c75b-4cfb-d700-9ad9eb8239ad"}
``` python
data_df.columns.to_list()
```

::: {.output .execute_result execution_count="6"}
    ['notification_date',
     'postcode',
     'lhd_2010_code',
     'lhd_2010_name',
     'lga_code19',
     'lga_name19']
:::
:::

::: {.cell .code execution_count="7" colab="{\"height\":204,\"base_uri\":\"https://localhost:8080/\"}" id="808dayNXBjQs" outputId="7c2aeed7-2eb4-4568-f066-8c5fba2b2892"}
``` python
data_df.head()
```

::: {.output .execute_result execution_count="7"}
```{=html}

  <div id="df-505193c4-aff1-45b8-b0ab-3c6d218d0425">
    <div class="colab-df-container">
      <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>notification_date</th>
      <th>postcode</th>
      <th>lhd_2010_code</th>
      <th>lhd_2010_name</th>
      <th>lga_code19</th>
      <th>lga_name19</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2020-01-25</td>
      <td>2134</td>
      <td>X700</td>
      <td>Sydney</td>
      <td>11300</td>
      <td>Burwood (A)</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2020-01-25</td>
      <td>2121</td>
      <td>X760</td>
      <td>Northern Sydney</td>
      <td>16260</td>
      <td>Parramatta (C)</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2020-01-25</td>
      <td>2071</td>
      <td>X760</td>
      <td>Northern Sydney</td>
      <td>14500</td>
      <td>Ku-ring-gai (A)</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2020-01-27</td>
      <td>2033</td>
      <td>X720</td>
      <td>South Eastern Sydney</td>
      <td>16550</td>
      <td>Randwick (C)</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2020-03-01</td>
      <td>2077</td>
      <td>X760</td>
      <td>Northern Sydney</td>
      <td>14000</td>
      <td>Hornsby (A)</td>
    </tr>
  </tbody>
</table>
</div>
      <button class="colab-df-convert" onclick="convertToInteractive('df-505193c4-aff1-45b8-b0ab-3c6d218d0425')"
              title="Convert this dataframe to an interactive table."
              style="display:none;">
        
  <svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
       width="24px">
    <path d="M0 0h24v24H0V0z" fill="none"/>
    <path d="M18.56 5.44l.94 2.06.94-2.06 2.06-.94-2.06-.94-.94-2.06-.94 2.06-2.06.94zm-11 1L8.5 8.5l.94-2.06 2.06-.94-2.06-.94L8.5 2.5l-.94 2.06-2.06.94zm10 10l.94 2.06.94-2.06 2.06-.94-2.06-.94-.94-2.06-.94 2.06-2.06.94z"/><path d="M17.41 7.96l-1.37-1.37c-.4-.4-.92-.59-1.43-.59-.52 0-1.04.2-1.43.59L10.3 9.45l-7.72 7.72c-.78.78-.78 2.05 0 2.83L4 21.41c.39.39.9.59 1.41.59.51 0 1.02-.2 1.41-.59l7.78-7.78 2.81-2.81c.8-.78.8-2.07 0-2.86zM5.41 20L4 18.59l7.72-7.72 1.47 1.35L5.41 20z"/>
  </svg>
      </button>
      
  <style>
    .colab-df-container {
      display:flex;
      flex-wrap:wrap;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

      <script>
        const buttonEl =
          document.querySelector('#df-505193c4-aff1-45b8-b0ab-3c6d218d0425 button.colab-df-convert');
        buttonEl.style.display =
          google.colab.kernel.accessAllowed ? 'block' : 'none';

        async function convertToInteractive(key) {
          const element = document.querySelector('#df-505193c4-aff1-45b8-b0ab-3c6d218d0425');
          const dataTable =
            await google.colab.kernel.invokeFunction('convertToInteractive',
                                                     [key], {});
          if (!dataTable) return;

          const docLinkHtml = 'Like what you see? Visit the ' +
            '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
            + ' to learn more about interactive tables.';
          element.innerHTML = '';
          dataTable['output_type'] = 'display_data';
          await google.colab.output.renderOutput(dataTable, element);
          const docLink = document.createElement('div');
          docLink.innerHTML = docLinkHtml;
          element.appendChild(docLink);
        }
      </script>
    </div>
  </div>
  
```
:::
:::

::: {.cell .code execution_count="8" colab="{\"base_uri\":\"https://localhost:8080/\"}" id="27mqtsgTBmB8" outputId="b9889b97-a7ac-4014-d0cb-b6cabd8fccfc"}
``` python
data_df['postcode'].nunique()
```

::: {.output .execute_result execution_count="8"}
    765
:::
:::

::: {.cell .code execution_count="9" colab="{\"height\":173,\"base_uri\":\"https://localhost:8080/\"}" id="jxFP6no_CMGM" outputId="9dbc4db7-b50f-4623-94e8-0d881a953bc4"}
``` python
data_df.describe()
```

::: {.output .execute_result execution_count="9"}
```{=html}

  <div id="df-da30980a-58b5-487b-b52c-80a5eeffbfa6">
    <div class="colab-df-container">
      <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>notification_date</th>
      <th>postcode</th>
      <th>lhd_2010_code</th>
      <th>lhd_2010_name</th>
      <th>lga_code19</th>
      <th>lga_name19</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>973412</td>
      <td>973412</td>
      <td>959365</td>
      <td>959365</td>
      <td>959279</td>
      <td>959279</td>
    </tr>
    <tr>
      <th>unique</th>
      <td>686</td>
      <td>765</td>
      <td>17</td>
      <td>17</td>
      <td>130</td>
      <td>130</td>
    </tr>
    <tr>
      <th>top</th>
      <td>2022-01-06</td>
      <td>2170</td>
      <td>X710</td>
      <td>South Western Sydney</td>
      <td>11570</td>
      <td>Canterbury-Bankstown (A)</td>
    </tr>
    <tr>
      <th>freq</th>
      <td>41338</td>
      <td>19158</td>
      <td>167966</td>
      <td>167966</td>
      <td>68654</td>
      <td>68654</td>
    </tr>
  </tbody>
</table>
</div>
      <button class="colab-df-convert" onclick="convertToInteractive('df-da30980a-58b5-487b-b52c-80a5eeffbfa6')"
              title="Convert this dataframe to an interactive table."
              style="display:none;">
        
  <svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
       width="24px">
    <path d="M0 0h24v24H0V0z" fill="none"/>
    <path d="M18.56 5.44l.94 2.06.94-2.06 2.06-.94-2.06-.94-.94-2.06-.94 2.06-2.06.94zm-11 1L8.5 8.5l.94-2.06 2.06-.94-2.06-.94L8.5 2.5l-.94 2.06-2.06.94zm10 10l.94 2.06.94-2.06 2.06-.94-2.06-.94-.94-2.06-.94 2.06-2.06.94z"/><path d="M17.41 7.96l-1.37-1.37c-.4-.4-.92-.59-1.43-.59-.52 0-1.04.2-1.43.59L10.3 9.45l-7.72 7.72c-.78.78-.78 2.05 0 2.83L4 21.41c.39.39.9.59 1.41.59.51 0 1.02-.2 1.41-.59l7.78-7.78 2.81-2.81c.8-.78.8-2.07 0-2.86zM5.41 20L4 18.59l7.72-7.72 1.47 1.35L5.41 20z"/>
  </svg>
      </button>
      
  <style>
    .colab-df-container {
      display:flex;
      flex-wrap:wrap;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

      <script>
        const buttonEl =
          document.querySelector('#df-da30980a-58b5-487b-b52c-80a5eeffbfa6 button.colab-df-convert');
        buttonEl.style.display =
          google.colab.kernel.accessAllowed ? 'block' : 'none';

        async function convertToInteractive(key) {
          const element = document.querySelector('#df-da30980a-58b5-487b-b52c-80a5eeffbfa6');
          const dataTable =
            await google.colab.kernel.invokeFunction('convertToInteractive',
                                                     [key], {});
          if (!dataTable) return;

          const docLinkHtml = 'Like what you see? Visit the ' +
            '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
            + ' to learn more about interactive tables.';
          element.innerHTML = '';
          dataTable['output_type'] = 'display_data';
          await google.colab.output.renderOutput(dataTable, element);
          const docLink = document.createElement('div');
          docLink.innerHTML = docLinkHtml;
          element.appendChild(docLink);
        }
      </script>
    </div>
  </div>
  
```
:::
:::

::: {.cell .code execution_count="10" colab="{\"height\":204,\"base_uri\":\"https://localhost:8080/\"}" id="V--URny8CTor" outputId="28f6e7eb-46ac-4fba-b081-ba64dec264a5"}
``` python
data_df.tail(5)
```

::: {.output .execute_result execution_count="10"}
```{=html}

  <div id="df-bd6cf97c-63c2-4c2e-874f-f6c45b1b0d7d">
    <div class="colab-df-container">
      <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>notification_date</th>
      <th>postcode</th>
      <th>lhd_2010_code</th>
      <th>lhd_2010_name</th>
      <th>lga_code19</th>
      <th>lga_name19</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>973407</th>
      <td>2022-02-07</td>
      <td>2283</td>
      <td>X800</td>
      <td>Hunter New England</td>
      <td>14650</td>
      <td>Lake Macquarie (C)</td>
    </tr>
    <tr>
      <th>973408</th>
      <td>2022-02-07</td>
      <td>2019</td>
      <td>X720</td>
      <td>South Eastern Sydney</td>
      <td>10500</td>
      <td>Bayside (A)</td>
    </tr>
    <tr>
      <th>973409</th>
      <td>2022-02-07</td>
      <td>2076</td>
      <td>X760</td>
      <td>Northern Sydney</td>
      <td>14500</td>
      <td>Ku-ring-gai (A)</td>
    </tr>
    <tr>
      <th>973410</th>
      <td>2022-02-07</td>
      <td>2760</td>
      <td>X750</td>
      <td>Nepean Blue Mountains</td>
      <td>16350</td>
      <td>Penrith (C)</td>
    </tr>
    <tr>
      <th>973411</th>
      <td>2022-02-07</td>
      <td>2066</td>
      <td>X760</td>
      <td>Northern Sydney</td>
      <td>14700</td>
      <td>Lane Cove (A)</td>
    </tr>
  </tbody>
</table>
</div>
      <button class="colab-df-convert" onclick="convertToInteractive('df-bd6cf97c-63c2-4c2e-874f-f6c45b1b0d7d')"
              title="Convert this dataframe to an interactive table."
              style="display:none;">
        
  <svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
       width="24px">
    <path d="M0 0h24v24H0V0z" fill="none"/>
    <path d="M18.56 5.44l.94 2.06.94-2.06 2.06-.94-2.06-.94-.94-2.06-.94 2.06-2.06.94zm-11 1L8.5 8.5l.94-2.06 2.06-.94-2.06-.94L8.5 2.5l-.94 2.06-2.06.94zm10 10l.94 2.06.94-2.06 2.06-.94-2.06-.94-.94-2.06-.94 2.06-2.06.94z"/><path d="M17.41 7.96l-1.37-1.37c-.4-.4-.92-.59-1.43-.59-.52 0-1.04.2-1.43.59L10.3 9.45l-7.72 7.72c-.78.78-.78 2.05 0 2.83L4 21.41c.39.39.9.59 1.41.59.51 0 1.02-.2 1.41-.59l7.78-7.78 2.81-2.81c.8-.78.8-2.07 0-2.86zM5.41 20L4 18.59l7.72-7.72 1.47 1.35L5.41 20z"/>
  </svg>
      </button>
      
  <style>
    .colab-df-container {
      display:flex;
      flex-wrap:wrap;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

      <script>
        const buttonEl =
          document.querySelector('#df-bd6cf97c-63c2-4c2e-874f-f6c45b1b0d7d button.colab-df-convert');
        buttonEl.style.display =
          google.colab.kernel.accessAllowed ? 'block' : 'none';

        async function convertToInteractive(key) {
          const element = document.querySelector('#df-bd6cf97c-63c2-4c2e-874f-f6c45b1b0d7d');
          const dataTable =
            await google.colab.kernel.invokeFunction('convertToInteractive',
                                                     [key], {});
          if (!dataTable) return;

          const docLinkHtml = 'Like what you see? Visit the ' +
            '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
            + ' to learn more about interactive tables.';
          element.innerHTML = '';
          dataTable['output_type'] = 'display_data';
          await google.colab.output.renderOutput(dataTable, element);
          const docLink = document.createElement('div');
          docLink.innerHTML = docLinkHtml;
          element.appendChild(docLink);
        }
      </script>
    </div>
  </div>
  
```
:::
:::

::: {.cell .code execution_count="11" colab="{\"base_uri\":\"https://localhost:8080/\"}" id="LFTADMaACZ38" outputId="3fcdd9ec-adf1-420d-a216-89aa9010c320"}
``` python
data_df.dtypes
```

::: {.output .execute_result execution_count="11"}
    notification_date    object
    postcode             object
    lhd_2010_code        object
    lhd_2010_name        object
    lga_code19           object
    lga_name19           object
    dtype: object
:::
:::

::: {.cell .markdown id="zuq0_tUUMQay"}
### Pandas Data Profiling Report

[Pandas
Profiling](https://pandas-profiling.ydata.ai/docs/master/index.html) is
a handy library for doing initial exploratory data analysis (EDA) on
data in a [pandas
dataframe](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.html).

*Uncomment the following line to execute it. It takes \~15-20 seconds to
run on this size dataset (progress bars show where the analysis is up
to).*
:::

::: {.cell .code execution_count="12" id="NT9wBzigKeSA"}
``` python
# ProfileReport(data_df, title="Demo: NSW COVID data", correlations=None).to_notebook_iframe();
```
:::

