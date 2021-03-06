Collection level buffer cache reporting for MongoDB
===================================================

##### Collstat:

 Reports buffer cache usage at a collection level, along with all indexes associated with it. It has the functionality to
 automatically discovers and report on replica set members. 
 

  ```python
python collstats.py -host 192.0.0.1 -port 40000 -db test -coll foo -discover
```

![alt tag](screenshots/mongoCollstat.JPG)
 
* name = db.collection_name or index name (if indented)
* used = bytes currently in the cache
* dirty = tracked dirty bytes in the cache
* pri = pages read into cache
* pwf = pages written from cache
* prq = pages requested from the cache
* ops = number of operations that has used the index

```python 
optional arguments:
  -h         Show this help message and exit
  -host      Hostname
  -port      Port number
  -db        Database_name
  -coll        Collection name
  -discover  Discover repset members
```
    
### Required packages

```python
pip install pymongo

pip install argparse
```  
### Requirments

 Mongodb running wired tiger storage engine
 



