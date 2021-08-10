# installing pymongo


`pip3 install pymongo`



# Authentication 
 You will get the URI from the mongodb website and press connect on your database , and get the link from the website.

```
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
