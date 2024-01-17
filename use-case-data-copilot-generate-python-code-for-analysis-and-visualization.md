# use-case-data-copilot-generate-python-code-for-analysis-and-visualization
### model gpt3.5 
#### prompt template
```
content_t=   PromptTemplate.from_template(

    "your task is to generate  correct Python code ready for runing on python that  matches user requirements the data you will work on \n {dataset_des} \n , {columns_des} , {data_subset}"
)


```
##### 1-dataset description "the question will be what is the describation of dataset ?"
```
Question-Answering (QA) System:
A QA system is designed to provide answers to questions posed by users.
It typically involves processing the query,
retrieving relevant information, and then generating or extracting an answer.

```

##### 2-columns description
```
column name with datatype 

```
##### 3-dataset subset 
```
take subset from the data 5 samples convert them int string 
```
#### prompt template example 
```
your task is to generate  correct Python code ready for runing on python that  matches user requirements the data you will work on 
the dataset desicraption is   The data provided is from four different dates in 2023. On December 8, 2023 the open was 135.66000366210938, the high was 137.99000549316406, the low was 135.57000732421875, and the close was 136.63999938964844, with a volume of 22990900. On November 8, 2023, the open was 132.36000061035156, the high was 133.5399932861328, the low was 132.16000366210938, and the close was 133.25999450683594, with a volume of 15093600. On December 5, 2023, the open was 130.3699951171875, the high was 133.5399932861328, the low was 129.72999572753906, and the close was 132.38999938964844, with a volume of 19235100. On September 28, 2023, the open was 130.69000244140625, the high was 134.17999267578125, the low was 130.69000244140625, and the close was 133.1300048828125. 
 , the columns describtion     the column name is {Date} the datatype is <class 'str'>
 the column name is {Open} the datatype is <class 'numpy.float64'>
 the column name is {High} the datatype is <class 'numpy.float64'>
 the column name is {Low} the datatype is <class 'numpy.float64'>
 the column name is {Close} the datatype is <class 'numpy.float64'>
 the column name is {Volume} the datatype is <class 'numpy.int64'>
 the column name is {Dividends} the datatype is <class 'numpy.float64'>
 the column name is {Stock Splits} the datatype is <class 'numpy.float64'>
. , this is a subset from the dataset frist 5 samples not all data   
                      Date       Open       High        Low      Close   Volume  Dividends  Stock Splits
2023-09-12 00:00:00-04:00 137.130005 137.639999 135.929993 136.070007 15212900        0.0           0.0
2023-09-13 00:00:00-04:00 135.899994 137.699997 134.929993 137.500000 16394900        0.0           0.0
2023-09-14 00:00:00-04:00 138.389999 139.550003 137.059998 138.990005 19064600        0.0           0.0
2023-09-15 00:00:00-04:00 138.800003 139.360001 137.179993 138.300003 48947600        0.0           0.0
2023-09-18 00:00:00-04:00 137.630005 139.929993 137.630005 138.960007 16233600        0.0           0.0

```

### user input and model respones  
#### 1-input 
```
give me the averge of open 

```
#### 2-respone

```
To calculate the average of the "Open" column in the dataset, you can use the numpy library in Python. Here's the code:

import numpy as np

# Assuming your dataset is stored in a variable called "data"
open_values = data['Open']
average_open = np.mean(open_values)

print("Average Open: ", average_open)

Make sure to replace "data" with the actual name of your dataset variable. This code will calculate the average of the "Open" column and print the result.
```
### in the socend update of prompt template 
```
dataset description canceled over cost 
```


