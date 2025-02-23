# Social Media Microservices Project

### Architecture
- Developed a **microservices-based** social media application featuring the following services:
  - **Identity Service**
  - **Media Service**
  - **Post Service**
  - **Search Service**
- All services run on the **same local host**.

### Service Communication
- Implemented **RabbitMQ** for asynchronous messaging to ensure decoupling and scalability between services.

### Service Ports
- **API Gateway:** 3000
- **Identity Service:** 3001  
  *(Handles Authentication, Authorization, and User Management)*
- **Media Service:** 3002  
  *(Manages Cloudinary-based media storage, upload, and deletion)*
- **Post Service:** 3003  
  *(Manages posts, interactions, and ensures deletion in both MongoDB & Cloudinary)*
- **Search Service:** 3004  
  *(Provides indexing and searching for posts using Redis caching)*

### Performance Optimization
- **Rate Limiting:** Implemented to enhance security and manage traffic control.
- **Redis Caching:** Utilized for fast data retrieval in Media, Post, and Search services.
