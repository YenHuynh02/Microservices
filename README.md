<div style="font-size: 17px">

# 1. What is a Microservice?
<p>
A microservice is a small, indepedently deployable service that performs a specific business function. It communicates with other microservices through APIs, often over HTTP or messaging queues.
</p>

# 2. What are the real benefits of Microservices?
<div>

<table>
    <tr>
        <td>Independent Deployments</td>
        <td>Each service can be deployed separately, reducing risk.</td>
    </tr>
    <tr>
        <td>Scalability</td>
        <td>Only the parts of the system need scaling can be scaled.</td>
    </tr>
    <tr>
        <td>Fault Isolation</td>
        <td>One failing service doesn't crash the entire system.</td>
    </tr>
    <tr>
        <td>Tech Flexibility</td>
        <td>Teams can use different languages or databases for each service.</td>
    </tr>
    <tr>
        <td>Faster Development</td>
        <td>Small teams can work in parallel on different services.</td>
    </tr>
</table>

</div>

# 3. Why do we use Microservices?
<p>
    To build large, complex applications that need to be modular and maintainable. Microservices enable continuous delivery/ deployment and support independent scaling of components.
</p>

# 4. When do we use Microservices?
<p>
    When the application becomes too large for a single team to manage effectively, or when different parts of the system have very different scaling needs. Microservices are also useful when fault tolerance is important.
</p>

# 5. What problems do Microservices solve?
<table>
    <tr>
        <td>Monolith Bottlenecks</td>
        <td>Difficult to scale, updated, or deploy large codebases.</td>
    </tr>
    <tr>
        <td>Team Scaling</td>
        <td>Allows multiple teams to work independently.</td>
    </tr>
    <tr>
        <td>Slow Deployments</td>
        <td>Enables frequent releases without touching the whole app.</td>
    </tr>
    <tr>
        <td>Tech Debt</td>
        <td>Encourages better separation of concerns and modular design.</td>
    </tr>
</table>

# 6. What do we use Microservices for?
<p>
    Microservices are used in various domains such as e-commerce (cart, inventory, payment, user services), media platforms (video encoding, user authentication, analytics), and banking (transaction, fraud detection, account services). They are suitable for any large, modular application where sercices evolve indepedently.
</p>

# 7. When should I be concerned about scalability?
<p>
    Scalibility becomes a concern when users grow rapidly, certain operations spike (e.g., payments during sales), a single component is under heavy load (e.g., search, image processing), or resource usage increases unevenly across components.
</p>

# 8. Given the tech stack you've designed, what component of the system would you scale?
<p>
    For example, if using Node.js for the API gateway and MongoDB for data, and you're facing high API load:
</p>
<ul>
    <li>Scale the API gateway horizontally (more containers).</li>
    <li>Use read replicas or shaded clusters for MongoDB.</li>
    <li>Offload static content to a CDN.</li>
    <li>Introduce asyncronous queues for heavy background tasks.</li>
</ul>

# 9. What are common strategies to scale? Pros and cons
<table>
    <tr>
        <td>Strategy</td>
        <td>Pros</td>
        <td>Cons</td>
    </tr>
    <tr>
        <td>Horizontal Scaling</td>
        <td>Easy to replicate services, load-balanced</td>
        <td>Requires stateless services, infra cost increases</td>
    </tr>
    <tr>
        <td>Vertical Scaling</td>
        <td>Simple to implement</td>
        <td>Hardware limits, single point of failure</td>
    </tr>
    <tr>
        <td>Database Sharding</td>
        <td>Splits data across servers for high thoughput</td>
        <td>Complex to manage, risk of hot partitions</td>
    </tr>
    <tr>
        <td>Caching</td>
        <td>Fast response times, less DB load</td>
        <td>Cache invalidation is hard</td>
    </tr>
    <tr>
        <td>Message Queues (Kalfka)</td>
        <td>Decouples services, async processing</td>
        <td>Adds complexity, harder debugging</td>
    </tr>
    <tr>
        <td>CDNs</td>
        <td>Offloads static content delivery</td>
        <td>Only for static assets</td>
    </tr>
    <tr>
        <td>Function as a Service</td>
        <td>Auto-scaled, no server management</td>
        <td>Cold starts, limited execution time</td>
    </tr>
</table>

</div>

# References:
```
[1] https://www.geeksforgeeks.org/microservices

[2] https://www.geeksforgeeks.org/what-are-the-advantages-and-disadvantages-of-microservices-architecture

[3] https://www.logicmonitor.com/blog/what-are-microservices

[4] https://medium.com/design-microservices-architecture-with-patterns/when-to-use-and-when-not-to-use-microservices-no-silver-bullet-3ae293faf6d

[5]
https://about.gitlab.com/blog/2022/09/29/what-are-the-benefits-of-a-microservices-architecture

https://daedtech.com/what-problems-do-microservices-solve

[6] https://hazelcast.com/foundations/software-architecture/microservices

[7] https://www.linkedin.com/pulse/why-you-should-use-microservice-architecture-lee-atchison-ouxgc

[8] https://www.coredna.com/blogs/microservices-pros-cons

[9] https://medium.com/cloud-native-daily/scaling-microservices-a-comprehensive-guide-200737d75d62

```