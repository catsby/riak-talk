!SLIDE title
# How Riak Works #

!SLIDE smbullets
### How Riak Works
## Basics

* Buckets, Keys, and Objects
* Links and Metadata

!SLIDE smbullets
### How Riak Works
## Buckets, Keys, and Objects

  _oh my_

- **Buckets** act as a namspace/keyspace (think Table of Folder)
- **Keys** are simple binary/string value, unique to **Bucket**
- **Objects** provide the _only_ unit of storage (essentially a struct)

!SLIDE smbullets
### How Riak Works
## Links and Metadata

- **Link**s establish one-way connection between objects  
  `Link: </riak/bucket/key>; riaktag="tag"`  
- You can **walk** them  
  `GET /riak/people/clint/people,friends[,1|0]`  
  `GET /riak/people/clint/people,friends,_/_,friends,1`  
  `GET /riak/people/clint/_,friends,_/_,friends,_/_,friends`
