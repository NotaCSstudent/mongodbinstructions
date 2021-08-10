# installing pymongo


`pip3 install pymongo`



# Authentication 
 You will get the URI from the mongodb website and press connect on your database , and get the link from the website.

```py
import pymongo

client = pymongo.MongoClient(Mongo_URI)
```

Next , to connect your database you must do this.

Inside the string, you would add the name of your collection


` data = client.get_database("collection_name")`

to access the contents of the collection, you would do this

`document_data = data['database']`

if you want to see how many items are in your specific data collection

**We dont add anything inside the bracket, to get everything in the database**

`count_data = document_data.count_documents({})`



if you want to add data

`document_data.insert_one({'key':'value'})`


if you want to delete data

`document_data.delete_one({'key':'value'})`


if you want to add multiple data you would use 

`document_data.insert_many({'key':'value'})`


if you want to delete multiple data 
`document_data.delete_many({'key':'value'})`


if you wanna delete everything

`document_data.delete_many({})`

# Full driver code.

```py


import pymongo

client = pymongo.MongoClient(Mongo_URI)
data = client.get_database("collection_name")
document_data = data['database']
count_data = document_data.count_documents({})
document_data.insert_one({'key':'value'})
document_data.delete_one({'key':'value'})
document_data.insert_many({'key':'value'})
document_data.delete_many({'key':'value'})
document_data.delete_many({})





```
