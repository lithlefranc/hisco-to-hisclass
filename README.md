# hisco-to-hisclass

This Python script facilitates the automatic conversion of HISCO-codes to their corresponding HISCLASS-categories. It leverages a CSV-file containing predefined mappings (created by Marco H.D. van Leeuwen and Ineke Maas) and applies these to an existing dataset of occupational codes.

## 1. Prerequisites
- Python 3.6 or higher
- pandas library
- openpyxl library

## 2. Before use
Before you can use the convertor, you need an (excel) database of professions linked to their HISCO-code. For example:

|profession|hisco|
|---|---|
| baker|77610|
| doctor|06105|
| factory worker|99930|
| policeman|58220|
| blacksmith|883190|

I have built a fuzzy matcher for Dutch- and French-language professions. For other languages you can make use of the [HISCO database](https://historyofwork.iisg.amsterdam/index.php).

## 3. Usage
- Make sure the HISCO-codes in your excel database are in a column named 'hisco'.
- Download the jupyter notebook (the actual convertor) and the csv-file (the hisco-hisclass mappings).
- Change the filename in the notebook to the filename of the excel database you want to convert.
- Run the code!

## 4. Example of result

Below you can see an example of professions linked to their respective HISCO- and HISCLASS-codes after running the convertor.

|profession|hisco|hisclass|
|---|---|---|
| baker|77610|7|
| doctor|06105|2|
| factory worker|99930|11|
| policeman|58220|4|
| blacksmith|883190|9|

## 5. Legend of HISCLASS-codes

|number|occupation category|
|---|---|
|1|higher managers|
|2|higher professionals|
|3|lower managers|
|4|lower prof and clerical, sales|
|5|lower clerical and sales|
|6|foremen|
|7|skilled workers|
|8|farmers|
|9|lower skilled workers|
|10|lower skilled farm workers|
|11|unskilled workers|
|12|unskilled farm workers|

## 6. Credit
- [HISCO](https://historyofwork.iisg.amsterdam/index.php) (Historical International Standard Classification of Occupations) was developed by Marco H.D. van Leeuwen, Ineke Maas and Andrew Miles (Leuven 2002). 

- [HISCLASS](https://lup.be/products/100004) (Historical International Social Class Scheme) was developed by Marco H.D. van Leeuwen and Ineke Maas (Leuven 2011).  
