###Server implemented with golang.
<pre>


                     Internet
                        ^
     +------------------|--------------------------------------------------+
                        |
             +-----+  +-+---+   +-----+
             |Agent|  |Agent|   |Agent|                    +--------------+
             +--+--+  +-----+   +--+--+                    |    REDIS     |
                |                  |                       |--------------|
     +----------|------------------|------------------+--&gt; | ESTATES      |
                |                  |                       | BASIC        |
          +-----v----+      +------v-----+                 | ....         |
          |HUB Server|      |Event Server|                 |              |
          +----------+      +------------+                 +--------------+</pre>

##条件
1. 确保安装好redis
2. 确保config.ini中的redis_xxxx配置正确

##安装
    sh$go get github.com/vmihailenco/redis  
    sh$cd src/scripts;./proto_gen.sh  
    sh$cd ../..;  make

