# Present all the Riaks #

# Viewing the slideshow
This is a [ShowOff][3] presentation about [Riak][7] for [CoMO Rich Web's NoSQL Smackdown][8].


**TOC**

1. Intro. 

  - Basho

2. What Riak is

  - Distributed data store, et. al.
  - CAP Theorem

3. How Riak works

  - Buckets/Keys (example output of bucket/key)
  - Links/Metadata
  - Nodes, Vnodes, and Partitions
  - Distribution

4. Using Riak 

  - API: Reading, writing, and MapReduce
  - curl ex.
  
5. New Hotness
  
  - Secondary Indexes
  - Search
  - Pipe

You can view the presentation here: [http://ctshryock.github.com/riak-talk][6]

If you want to view it locally, you need to install Showoff, clone the repo, and then run `serve`:

    $ gem install showoff
    $ git clone git://github.com/ctshryock/riak-talk.git
    $ cd riak-talk
    $ showoff serve

Go to [http://localhost:9090][5] to view the presentation.


[3]: http://github.com/schacon/showoff
[4]: https://github.com/ctshryock/riak-talk
[5]: http://localhost:9090
[6]: http://ctshryock.github.com/riak-talk
[7]: http://www.basho.com/products_riak_overview.php
[8]: http://comorichweb.posterous.com/next-meetup-nosql-smackdown-september-28th