# hisco-to-hisclass

This Python script facilitates the automatic conversion of HISCO-codes to their corresponding HISCLASS-categories. It leverages a CSV file containing predefined mappings and applies these to an existing dataset of occupational codes.

## 1. Prerequisites
- Python 3.6 or higher
- pandas library
- openpyxl library



## 2. Before use
Before you can use the convertor, you need an (excel) database of professions linked to their HISCO-code. For example:

|profession|hisco|
|---|---|
| baker|77610|
| doctor      |06105|
| factory worker|99930|
| policeman|58220        |
| blacksmith|   883190           |

I've built a fuzzy matcher for Dutch-language professions, see: 

For other languages you can make use of the [HISCO database](https://historyofwork.iisg.amsterdam/index.php).

## 3. Usage
- Make sure the hisco codes in your excel database are in a column named 'hisco'.
- Download the jupyter notebook (the actual convertor) and the csv file (the hisco-hisclass mappings).
- Change the filename in the notebook to the filename of the hisco-database you want to convert.
- Run the code!



## 4. Example of result

Below you can see an example of professions linked to their respective HISCO- and HISCLASS-codes after running the convertor.

|profession|hisco|hisclass|
|---|---|---|
| baker|77610|7|
| doctor      |06105|2|
| factory worker|99930|11|
| policeman|58220        |4|
| blacksmith|   883190           |9|

## 5. Legend of hisclass codes

| Number | Occupation Category                  |
|--------|--------------------------------------|
| 1      | Higher managers                      |
| 2      | Higher professionals                 |
| 3      | Lower managers                       |
| 4      | Lower prof and clerical, sales       |
| 5      | Lower clerical and sales             |
| 6      | Foremen                              |
| 7      | Skilled workers                      |
| 8      | Farmers                              |
| 9      | Lower skilled workers                |
| 10     | Lower skilled farm workers           |
| 11     | Unskilled workers                    |
| 12     | Unskilled farm workers               |


## 6. Credit
- [HISCO](https://historyofwork.iisg.amsterdam/index.php) (Historical International Standard Classification of Occupations) was developed by Marco H.D. van Leeuwen, Ineke Maas and Andrew Miles (Leuven 2002). 

- [HISCLASS](https://lup.be/products/100004) (Historical International Social Class Scheme) was developed by Marco H.D. van Leeuwen and Ineke Maas (Leuven 2011).  
