### Azure Content Delivery Network (CDN) VS Azure Front Door

Guidance:
https://microsoftlearning.github.io/AZ-204-DevelopingSolutionsforMicrosoftAzure/Instructions/Labs/AZ-204_lab_12.html

**Azure Content Delivery Network (CDN)** is a distributed network of servers that efficiently delivers web content to users by caching content at edge servers located in various regions around the world. This helps reduce latency and improve performance by serving content from the nearest edge server to the user.

### Key Features of Azure CDN

1. **Global Reach**: Delivers content quickly and reliably to users worldwide.
2. **Performance Improvement**: Reduces latency and improves load times for websites, mobile apps, and streaming media.
3. **Scalability**: Handles traffic spikes and high loads without additional infrastructure costs.
4. **Security**: Provides features like custom domain HTTPS, DDoS protection, and Web Application Firewall (WAF) to secure content.
5. **Integration**: Seamlessly integrates with other Azure services for easy setup and management.

### How It Works

1. **User Request**: A user requests content using a URL with a special domain name (e.g., `<endpoint name>.azureedge.net`).
2. **DNS Routing**: The DNS system routes the request to the nearest edge server (Point of Presence or POP).
3. **Content Delivery**: If the edge server has the content cached, it delivers it directly to the user. If not, the edge server fetches the content from the origin server, caches it, and then delivers it to the user.
4. **Caching**: The content remains cached on the edge server until the Time to Live (TTL) expires.

### Benefits

- **Enhanced User Experience**: Faster load times and improved performance for end users.
- **Reduced Bandwidth Costs**: Distributes user requests and serves content directly from edge servers, reducing traffic to the origin server.
- **High Availability**: Handles high traffic loads and ensures content is always available.

### Getting Started with Azure CDN

1. **Create a CDN Profile**: Use the Azure portal, CLI, or ARM templates to create a new CDN profile.
2. **Create a CDN Endpoint**: Within the profile, create an endpoint to start delivering content.
3. **Configure Settings**: Set up caching rules, HTTPS, and other configurations as needed.
4. **Monitor and Manage**: Use Azure Monitor and Azure Security Center to track performance and security.

Both **Azure Front Door** and **Azure Content Delivery Network (CDN)** are powerful services offered by Microsoft Azure, but they serve slightly different purposes and have distinct features. Here's a comparison to help you understand the differences:

### Azure Front Door
- **Purpose**: Designed for global load balancing, intelligent routing, and application delivery.
- **Dynamic Content**: Supports dynamic content delivery and can route traffic based on various factors like latency, health probes, and endpoint weighting.
- **Protocol Support**: Supports HTTP, HTTPS, HTTP/2, WebSockets, Server Name Indication (SNI), and WebSocket routing.
- **Security**: Offers enhanced security features including Web Application Firewall (WAF) integration and integrated DDoS protection.
- **Global Load Balancing**: Provides native support for global load balancing across different regions, improving availability and performance.
- **Analytics and Monitoring**: Advanced analytics and monitoring features integrated with Azure Monitor and Azure Log Analytics.

### Azure CDN
- **Purpose**: Focuses on caching and delivering static content like images, CSS, and JavaScript files from edge locations close to the end-user.
- **Static Content**: Primarily used for static content delivery, reducing latency and optimizing performance.
- **Protocol Support**: Supports HTTP, HTTPS, HTTP/2, and WebSocket support.
- **Security**: Provides content protection, token authentication, and SSL/TLS encryption.
- **Global Reach**: Delivers content quickly and reliably to users worldwide but does not provide native global load balancing.
- **Analytics and Monitoring**: Basic analytics and monitoring capabilities through Azure Monitor and Azure CDN Reports.

### Key Differences
- **Content Type**: Azure Front Door is better suited for dynamic content and complex routing scenarios, while Azure CDN is ideal for static content delivery.
- **Security**: Azure Front Door offers more advanced security features compared to Azure CDN.
- **Load Balancing**: Azure Front Door provides native global load balancing, whereas Azure CDN focuses on content caching and delivery.

