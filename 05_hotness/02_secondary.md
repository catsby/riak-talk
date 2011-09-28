!SLIDE bullets
### New Hotness
## Secondary Indexes

- Representing alternate keys, one-to-many relationships, or many-to-many relationships 
- "Tag" an object with some **Index** metadata
- Retreive objects by that **Index**

!SLIDE code
### New Hotness
## Secondary Indexes

    $ curl -X POST \
      -H 'x-riak-index-twitter_bin: ctshryock' \
      -H 'x-riak-index-email_bin: clint@ctshryock.com' \
      -d '...user data...' \
      http://localhost:8091/buckets/users/keys/ctshryock

!SLIDE code
### New Hotness
## Secondary Indexes

**Query the twitter handle...**
    curl localhost:8091/buckets/users/index/twitter_bin/ctshryock

**Response...**
    {"keys":["ctshryock"]}

