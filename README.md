# dbexport 

A simple database reader and transformer for `Product` and `Rating` databases

## Usage

Use it to fetch a database from the cloud:
``` bash
$ export DB_URL="postgresql://username:password@IP:PORT/reviews"
$ PYTHONPATH=. python
>>> from dbexport.config import Session
>>> db_session = Session()
>>> ...
```

Export data to csv in the `product_ratings.csv` file in this format:
``` csv
name,level,published,created_on,review_count,avg_rating
Product 1,1,True,2019-07-10,10,4.3
```

Heres how you'd do it:
``` bash
$ export DB_URL="postgresql://username:password@IP:PORT/reviews"
$ product_csv.py
```

You can also export to a JSON file called `product_ratings.csv` in this format:
``` JSON
[
    {
        "name": "Product1",
        "level": "1",
        "published": true,
        "created_on": "2019-07-10",
        "review_count": 10,
        "avg_rating": 4.3
    },
    {
        "name": "Product2",
        "level": "2",
        "published": true,
        "created_on": "2019-07-10",
        "review_count": 3,
        "avg_rating": 4.5

    }
]
```





