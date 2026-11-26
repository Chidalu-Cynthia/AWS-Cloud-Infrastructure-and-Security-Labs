
# AWS Database Services & Security

## 1. Project Overview and Objectives

This project explored AWS database services and the security considerations involved in deploying and managing cloud databases.

The objective was to understand Amazon RDS, Amazon Aurora and Amazon DynamoDB, including database connectivity, access control, encryption, backups and monitoring.

The project included a limited hands-on deployment of an RDS MySQL database and conceptual study of additional database services and security features.

## 2. Architecture and Resource Design

The lab covered three AWS database services:

- **Amazon RDS:** Managed relational database service for engines such as MySQL.
- **Amazon Aurora:** Relational database engine compatible with MySQL and PostgreSQL, using a distributed storage architecture.
- **Amazon DynamoDB:** Managed NoSQL database service based on tables, items and key-value/document data models.

The security design concepts focused on restricting database access to authorized application resources, protecting stored and transmitted data, and maintaining recoverability through backups.

## 3. AWS Services and Configurations

- **Amazon RDS:** Created an RDS MySQL database named `cloudsecurity-rds-mysql`.

  ![Created Amazon RDS MySQL Database](screenshots/Created%20Amazon%20RDS%20MySQL%20Database.png)

- **Amazon Aurora:** Studied its architecture, including writer and reader instances and shared cluster storage.

- **Amazon DynamoDB:** Studied tables, items, partition keys and the NoSQL data model.

- **AWS KMS:** Explored the role of encryption keys in protecting database data at rest.

- **AWS CloudWatch and CloudTrail:** Studied database monitoring and AWS management-event auditing.

## 4. Implementation and Key Decisions

I created an RDS MySQL database through the AWS console.

However, the simplified database creation experience did not expose the networking and security configuration options I needed to complete the intended setup. I therefore deleted the database rather than leave a deployment that did not meet the lab's security requirements.

The remaining work focused on understanding database architecture and security configurations without deploying additional paid resources.

## 5. Security Considerations

The following database security concepts were studied:

- **Network access control:** Restrict database connectivity to authorized application resources, such as allowing MySQL TCP port 3306 only from the EC2 security group.
- **Encryption at rest:** Use AWS KMS to protect stored database data.
- **Encryption in transit:** Use TLS to protect database connections.
- **IAM database authentication:** Use temporary authentication tokens where supported instead of relying only on static database passwords.
- **AWS Secrets Manager:** Securely store and manage database credentials.
- **Backup protection:** Use automated backups, point-in-time recovery and manual snapshots.
- **Deletion protection:** Reduce the risk of accidentally deleting important database instances.
- **Monitoring and auditing:** Use CloudWatch for database metrics and CloudTrail to review AWS management events.

## 6. Testing and Validation

The RDS MySQL database creation was confirmed through the AWS console, which displayed a successful creation message.

The database was subsequently deleted after encountering limitations in the simplified creation wizard.

## 7. Troubleshooting and Findings

During the RDS deployment, I encountered limitations in the simplified creation wizard that prevented me from accessing the networking and security configuration options required for the intended lab.

Rather than proceed with an incomplete configuration, I deleted the database.

## 8. Lessons Learned

This project improved my understanding of AWS database services and the security controls required to protect cloud-hosted databases.

I learned the differences between relational databases, Aurora's cluster architecture and DynamoDB's NoSQL model.

I also explored how network restrictions, IAM authentication, encryption, secrets management, backups and monitoring contribute to database security.

The exercise reinforced the importance of planning database architecture and security requirements before deployment.
