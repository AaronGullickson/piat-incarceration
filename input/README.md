# Data Source Description

The data used here is compiled from several different sources:

-   Incarceration rates are based on 2022 data from [The Sentencing Project](https://www.sentencingproject.org/).
-   Data on homelessness comes from the [United States Interagency Council on Homelessness](https://www.usich.gov/tools-for-action/map/#fn%5B%5D=1300&fn%5B%5D=2900&fn%5B%5D=6400&fn%5B%5D=10200&fn%5B%5D=13400).
-   Data on homicide rates comes from the [National Center for Health Statistics](https://www.cdc.gov/nchs/pressroom/sosmap/homicide_mortality/homicide.htm).
-   Urbanization data com from the US Census Bureau.
-   Data on party control by state comes from the [National Conference on State Legislatures](https://www.ncsl.org/research/about-state-legislatures/partisan-composition.aspx).
-   The remaining state level data comes from [American Community Survey](https://www.census.gov/programs-surveys/acs) data pooled from 2016-2020 and extracted from [Social Explorer](<https://socialexplorer.com>).

I have combined this data together to create the analytical dataset that we will use. To load this dataset in R, you just need to run the setup code chunk in the full_report.Rmd R Markdown document. The name of the dataset in R is `full_data`. The variables are:

-   **state**: The name of the state. We will not use this in computations but it may be useful for reference. 
-   **incarceration_rate**: Number of incarcerated persons in the state per 100,000 population. This is the key dependent variable.
-   **homeless_rate**: Number of homeless persons in the state per 100,000 population.
-   **homicide_rate**: Number of homicide deaths in the state per 100,000 population.
-   **pct_black**: Percent of state population that is Black.
-   **unemp_rate**: Percent of the labor force in each state that is unemployed.
-   **pct_college**: Percent of the adult population aged 25 and over in the state that has at least a four year college degree.
-   **poverty_rate**: Percent of the state population that has a household income below the federal poverty line. This is the key independent variable.
-   **gini**: A measure of income inequality in the state. This index ranges from 0 (perfect equality of income) to 100 (one person has all the money).
-   **urbanization**: The percent of the state's population that lives in a metropolitan area.
-   **party_control:** A measure of which party controls the state government. When one party controls both the legislature and the governorship, the result is either "Democrat" or "Republican". If the results are mixed (either due to governor/legislature difference or a split bicameral legislature), then the result is "Split".
