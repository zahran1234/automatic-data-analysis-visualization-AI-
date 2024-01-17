# use case data copilot 
### work steps 
#### 1.chat with your csv file using openai 
```
not accepted results in general 
all you need in the and chat_with_cvs_file and section1 in comparison file 

```
#### prompt templet 
```
1.columns descration 
2.dataset subset 
3.content 
______________
columns_des_t  = PromptTemplate.from_template(
    "the columns describtion   {column}."
)
dataset_subset_t = PromptTemplate.from_template(
    "this is a subset from the dataset frist 2 samples not all data   \n {data}"
)
content_t=   PromptTemplate.from_template(

    "your task is to generate the correct Python code ready for running on Python that  matches user requirements , the output sholud be charts with numbers if avaliable    \n the path of data determined by 3  quotes  ```/content/Month_Value_1.csv ``` \n  , {columns_des} {data_subset}"
)


```


### english verstion  secation2  in comparsion file 


#### concoluation in the in english veration the results of month dataset perfect  using autogen(user proxy and assistand ) 

#### arabic verstion secation 3 in comparsion file 

