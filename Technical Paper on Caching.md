# Caching

#### Definition 

Caching is a key system design concept that involves storing frequently accessed data in a quick and easily accessible location. Its main purpose is to improve performance by reducing the time it takes to retrieve data that users often request.


## Need of Caching 
  
* In General the web applications stores data in a database.

* Whenever the user request for the data , then it is fetched from the database.

* Every time the user requests for the data this process will be happened.

* Reading the data from the database network calls consumes the lots of time. 

* Cache is a temporary storage location for data that is accessed frequently or recently.
  
* To reduce the number of calls to the database, we can use cache.
  
* by using of the cache, whenever the data is requested the system checks for the data in the cache instead of the main database.
  
* If the required data is not present then it will searches from the main database.
  
* This will significantly reduce the time it takes for accessing the data.

## Different types of caching approaches

### 1. Application-Server Cache

* Here the cache is added along with the application server.
  
* Whenever the user request's the data then it will be stored in the cache and if again the same request arises then it will be returned from the cache.
  
* For a new request, data will be fetched from the database and it will be returned.

* Once the new request will be fetched from the database, then it will be stored in the same cache for the next time request from the user.

* If the number of results that we are working with is really less then the application server cache is the best option.

### 2. Distributed Cache

* In a distributed caching system, the total cache space is divided among multiple nodes. Each node stores a specific portion of the data.

* For example, in a system with 10 nodes and a load balancer, each node holds a small fraction of the overall cache.

* A consistent hashing function is used to efficiently identify which node contains specific cached data.

* The system can also expand its cache capacity by adding new nodes to the pool.

* This scalability enhances cache memory and improves performance as demand increases.

### 3. Client-Side Cache

* Client-side caching involves storing data directly on the client’s device, such as in a web browser. 

* This method is particularly useful for web applications that frequently access static resources like images and JavaScript files.

* By implementing client-side caching, web applications can significantly enhance performance by reducing the number of requests sent to the server. 

* However, one downside is the risk of stale data, where the cached information may not be up-to-date.

* To mitigate this issue, it is essential to establish effective caching policies and set appropriate expiration times.

* This ensures that the data remains current and relevant for users.

### 4. Global Cache 
  
* As the name implies, a global cache consists of a single cache space that all nodes share. Each request is directed to this centralized cache space.

* If a cache request is not found in the global cache, it is the cache's responsibility to retrieve the missing data from the underlying storage (such as a database or disk).
  
* If a request is made and the cache cannot locate the data, the requesting node will communicate directly with the database or server to fetch the requested information.

## References

* [Caching – System Design Concept](https://www.geeksforgeeks.org/caching-system-design-concept-for-beginners/)
* [Cache Strategies](https://medium.com/@mmoshikoo/cache-strategies-996e91c80303)
