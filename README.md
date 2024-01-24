# practice-AWS-architecture

This repository documents the AWS architecture proposal for optimizing the hosting of the Fastier web application. The process involves understanding the client's challenges, devising a suitable AWS solution, and communicating the proposed architecture to the client, Lilly Sawyer.

## Task Overview

1. **Client Brief:**
   - Fastier, a startup, experiences slow response times, server crashes, downtime during deployments, and lacks a disaster recovery plan.
   - The application is a SPA React App with a Python and Flask backend, utilizing PostgreSQL on a single AWS EC2 instance (t3.medium, 4GB of RAM).

2. **Team Decision:**
   - Recognizing the startup nature, the team can provide a greenfield approach with the flexibility to make changes to the application stack.
   - Considering the ease of data migration into AWS and the tolerance for some downtime during migration and setup.
   - Acknowledging the need to host static content for a mixed API and web app.

3. **Solution Decision:**
   - Elastic Beanstalk is recommended for its support of Python applications, automatic scaling, and Blue/Green deployment features.
   - Services include Route 53, Elastic Load Balancing, Elastic Beanstalk with Autoscaling EC2 Group, RDS, S3, and CodePipeline.
   - An additional availability zone is proposed for redundancy, though not strictly necessary.

4. **Evaluation:**
   - Elastic Beanstalk is chosen based on its suitability for Python applications, scalability, and Blue/Green deployment capabilities.
   - Alternatives like Lambda or Fargate are acknowledged but deemed potentially more complex. Lightsail and EC2 are considered easier but lack automatic scaling.

5. **Architecture Diagram:**
   - An architecture diagram is created to visually represent the proposed solution.

## Email Response to Lilly Sawyer

### Subject: Proposed AWS Hosting Architecture for Fastier Web Application

Dear Lilly,

Congratulations on Fastier's recent success! I've reviewed your concerns and am excited to present an AWS architecture proposal to optimize your web application hosting.

**Challenges Addressed:**
1. Slow response times during peak periods.
2. Server crashes due to memory limitations.
3. Downtime during deployments.
4. Lack of a disaster recovery plan.

**Proposed AWS Solution:**

1. **Elastic Beanstalk with Autoscaling EC2 Group:**
   - **Purpose:** Hosts your Python application, simplifying deployment and scaling. Blue/Green deployment minimizes downtime during updates.
   - **Why Chosen:** Tailored for Python applications, offers automatic scaling, and streamlines deployment processes.

2. **Route 53:**
   - **Purpose:** Ensures seamless domain management for easy application connections.
   - **Why Chosen:** Scalability and easy integration with other AWS services.

3. **Elastic Load Balancing (ELB):**
   - **Purpose:** Distributes incoming traffic, improving availability and fault tolerance.
   - **Why Chosen:** Enhances performance and reliability by balancing the load across instances.

4. **RDS (Relational Database Service):**
   - **Purpose:** Provides a managed, scalable, and reliable PostgreSQL solution.
   - **Why Chosen:** Ensures high availability, easy scalability, and efficient database management.

5. **S3 (Simple Storage Service):**
   - **Purpose:** Hosts static content in a scalable and cost-effective manner.
   - **Why Chosen:** Efficiently handles static content for mixed API and web app requirements.

6. **CodePipeline:**
   - **Purpose:** Facilitates continuous integration and delivery, streamlining development and deployment.
   - **Why Chosen:** Automation aligns with Fastier's need for an efficient development lifecycle.

7. **Additional Availability Zone:**
   - **Purpose:** Enhances redundancy for improved fault tolerance.
   - **Why Proposed:** Adds an extra layer of resilience to the architecture.

**Consideration of Alternatives:**
We acknowledge alternative AWS services and are open to discussing them based on your preferences and application requirements.

**Cost Considerations:**
Our approach balances performance and scalability while optimizing costs. Elastic Beanstalk's autoscaling optimizes costs during lower activity periods.

We look forward to discussing this architecture in more detail during our upcoming meeting. Feel free to share any specific preferences or concerns you may have.

Best regards,
[Your Name]
[Your Position]
[Your Company]

---

## Architecture Diagram

![image](https://github.com/Phatd299/practice-AWS-architecture/assets/110618138/d5ff7cbb-0fc3-49d7-a7c9-e237283ef212)

---

## Showcase My Completion Certificate

<img width="579" alt="image" src="https://github.com/Phatd299/practice-AWS-architecture/assets/110618138/62774835-6053-447d-9edf-2a1cef84fbfa">

