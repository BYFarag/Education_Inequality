# Education Inequality

# Description : 
The purpose of this project is to addresses inequality of educational opportunity in U.S. high schools. In this project we will focus on average student performance on the ACT or SAT exams that students take as part of the college application process. We will be answering the question "Given socioeconomic factors can we predict an ACT score?"

Software used for both preperation & analysis was google colab notebook

# Data Used: 
Data: The First data set is the EdGap data set from https://www.edgap.org/#4/37.89/-97.00. This data set from 2016 which includes information about average ACT or SAT scores for schools and several socioeconomic characteristics of the school district. The second data set is information about each school from the National Center for Education Statistics. https://nces.ed.gov/ccd/pubschuniv.asp. Dr. Brian Fischer, a professor at Seattle University, had both sets for ready for his students found on his git as well https://github.com/brian-fischer/DATA-3320/tree/main/education


The first data set can be found in the Github repository. Named EdGap_data.xlsx
The second is too large & can be accessed from the dropbox link:
https://www.dropbox.com/s/lkl5nvcdmwyoban/ccd_sch_029_1617_w_1a_11212017.csv?dl=0. 

# Data preparation: 
The file preparing the data is called: Bayan_Farag_DATA_3320_Education_Inequality.ipynb.  The output files are called: clean_train & clean_test

The standard data cleaning process involves several important steps. Firstly, the source of the data must be identified and all necessary links to data sources provided. The contents of each data set should be inspected for issues such as duplicates, missing values, outliers, and data type inconsistencies.

Specfic data types were converted to ensure consistency and avoid errors during analysis. For example We needed to join two DataFrames using the school identity as the key, which is represented by the NCESSCH column. However, the column has different names in the two DataFrames and is stored as an int64 in one DataFrame and a float64 in the other. To merge the two DataFrames, we'll first cast the NCESSCH column in the DataFrame with the float64 datatype to an int64. Before casting, we must drop any rows where the NCESSCH value is NaN.Unnecessary parts of the data set were removed, and relevant columns kept when joining data frames. 

Missing values were imputed or removed as appropriate. Inaddtion to removal columns were renamed according to best practices. Finally, we created 2 CVS files called 
clean_train & clean_test. These two files will be used in the analysis in the project & can be found the the repository

# Analysis: 
The file doing the analysis is called 
"Bayan Farag Analysis - DATA 3320 Education.ipynb" 

In order to analyze the data and create meaningful plots, specific steps were taken, this included: breaking the problems into smaller subproblems, plotting these subproblems, and leveraging ordinary least squares regression to determine the influential independent variables affecting the dependent variable, "average_act". Additionally, we built a model with a regression line to examine specific independent variables and created a Heat Map to gain comprehensive insights from the dataset.

These steps enabled us to uncover compelling findings, facilitating accurate predictions and culminating in well-grounded conclusions.


# Authors & License Note: 

This colab notebook was authored by Bayan Farag, a student at Seattle University, with the valuable oversight and guidance of Dr. Brian Fischer, ensuring the project's successful execution.

The materials in this repository are licensed

This means that you are free to:
- Share: Copy and redistribute the materials in any medium or format.
- Adapt: Remix, transform, and build upon the materials for any purpose, even commercially.

Under the following terms you must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.

