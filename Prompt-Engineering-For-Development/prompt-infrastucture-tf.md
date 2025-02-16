1. **Application Overview**:
   - The Python application is a REST API built with FastAPI. It uses PostgreSQL for the database and Redis for caching.
   - Key components:
     - FastAPI for the web server.
     - PostgreSQL for the database.
     - Redis for session caching.
     - Docker for containerization.

2. **AWS Infrastructure Requirements**:
   - Required AWS resources:
     - ECS (Fargate) for running the FastAPI application.
     - RDS (PostgreSQL) for the database.
     - ElastiCache (Redis) for caching.
     - S3 bucket for storing static files.
     - Application Load Balancer (ALB) for routing traffic.
     - VPC with public and private subnets, NAT gateway, and security groups.
   - Scalability: Auto-scaling for ECS tasks and RDS read replicas.

3. **Terraform Configuration**:
   - Provide a Terraform configuration to provision the above resources.
   - Use variables for inputs like `environment` (dev/staging/prod), `region`, and `instance_type`.
   - Store the Terraform state file in an S3 bucket with DynamoDB for locking.

4. **Terraform Configuration example**:

5. **Output Configuration**:
