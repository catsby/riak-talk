!SLIDE 
# Using Riak #


!SLIDE smbullets
### Using Riak
## RESTful API

- Uses normal **HTTP Responce codes**
- **Reading**  
  `GET /riak/bucket/key`
- **Create** new object  
  `PUT /riak/bucket/key (user defined key)`  
  `POST /riak/bucket (random key)`
- **Delete**  
  `DELETE /riak/bucket/key`

!SLIDE smbullets
### Using Riak
## Response Codes  

- 200 OK 
- 300 Multiple Choices
- 304 Not Modified

## Typical Error Codes  

- 404 Not Found

!SLIDE commandline smaller
### Using Riak

<pre>
$ curl -v -d 'this is a test' -H "Content-Type: text/plain" \
    http://127.0.0.1:8091/riak/test
</pre>
