# GettingAndCleaningDataProject
Project for the Getting And Cleaning Data course, week 3.

## How to use the script
This section describes the steps to follow in order to execute the __run\_analysis.R__ script.  
1. Clone the Git repository (_git clone https://github.com/virtualramblas/GettingAndCleaningDataProject.git_). It contains the Samsung raw test data (folder __UCI HAR Dataset__ and its subfolders) as well.  
2. Open the R console.  
3. Set your working directory to the root folder of the cloned repository.  
4. Execute the script (_source("run\_analysis.R")_).  
  
At the end of the script execution a text file named _tidyDataset.txt_ containing the tidy data would be generated in the working directory.
## How the script works
This section describes the steps that the script follows during its execution.  
* It loads the required packages (_data.table_ and _reshape2_).  
* Reads the raw test data from the files in the __UCI HAR Dataset__ subfolder.  
* Concatenates the data tables, merges their columns and sets the key.  
* Reads the __features.txt__ file in order to subset only measurements for the mean and standard deviation.  
* Converts the column numbers to a vector of variable names matching columns in the data set and then subsets these variables using variable names.  
* Reads the __activity_labels.txt__ file to add descriptive names to the activities.  
* Labels the data set with descriptive variables names.  
* Creates a tidy data set.  
* Saves the tidy data set to a file named  __tidyDataset.txt__
