with open('lecz-urban-rural-population-land-area-estimates-v2-csv/lecz-urban-rural-population-land-area-estimates_continent-90m.csv','rU') as inputFile:
    header = next(inputFile)                        #remove the header and assign it to a variable
    for line in inputFile:                          #for each line in the inputfile
        line = line.rstrip().split(',')             #rstrip() removes any trailing or leading spaces & split () performs a text to columns delimit split to create multiple columns
        line[5] = int(line[5])                      #changed the population in line 5 from a string to a number
        if line[1] == 'Total National Population':  #there is overlap in the data. I just want to calculate total population
            population_dict[line[0]] += line[5]     #create a dict with continent as key and population as value and add the populations of rural and urban

import pandas as pd  #panel data 

# Reading in the CSV we used
input_dataframe = pd.read_csv('lecz-urban-rural-population-land-area-estimates-v2-csv/lecz-urban-rural-population-land-area-estimates_continent-90m.csv')
input_dataframe['Continent']  # reference a column by name
input_dataframe[0:10]  # reference 10 rows of data

cls = clear powershell screen




