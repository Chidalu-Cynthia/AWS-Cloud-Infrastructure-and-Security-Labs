
# AWS Content Delivery, DNS & Web Application Security

## 1. Project Overview and Objectives

This project explored AWS services used to deliver web content, manage DNS resolution and protect web applications.

The objective was to understand how Amazon CloudFront, Amazon Route 53 and AWS Web Application Firewall (WAF) work together to support application availability, performance and security.

This project focused on conceptual study because account restrictions prevented the planned practical deployments.

## 2. Architecture and Resource Design

The project covered three services that address different parts of web application delivery and protection.

**Conceptual architecture:**

`User Request → Route 53 DNS Resolution → CloudFront Distribution → Origin Server`

`AWS WAF → Inspects and Filters Web Requests`

- **Route 53:** Resolves domain names and directs users to application endpoints.
- **CloudFront:** Delivers content through a global network of edge locations.
- **AWS WAF:** Inspects web requests and applies rules to allow, block or monitor traffic.

## 3. AWS Services and Configurations

- **Amazon CloudFront:** Studied distributions, origins, cache behaviours, edge locations, caching and HTTPS configuration.
- **Amazon Route 53:** Studied hosted zones, DNS records, domain resolution and routing policies.
- **AWS WAF:** Studied web access control lists (Web ACLs), managed rule groups, custom rules and request filtering.

## 4. Implementation and Key Decisions

The work in this project focused on understanding the configuration and security features of the three services.

**Amazon CloudFront**

I explored the CloudFront distribution setup process but encountered an AWS account verification restriction that prevented deployment.

I submitted an AWS Support case regarding the restriction. Since the issue remained unresolved, I did not proceed with distribution deployment.

**Amazon Route 53**

I studied how Route 53 manages DNS records and hosted zones, and how DNS routing policies direct traffic to application endpoints.

**AWS WAF**

I studied how WAF uses Web ACLs and rule groups to inspect incoming web requests. Account restrictions prevented me from deploying a Web ACL or attaching WAF protection to an application.

No production or active configurations were deployed for these services.

## 5. Security Considerations

The following security concepts were explored:

- **HTTPS:** Encrypts communication between users and web applications.
- **CloudFront access control:** Controls how content is delivered and how origins can be accessed.
- **Origin protection:** Helps prevent unauthorized direct access to application origins.
- **DNS security:** Requires appropriate control over hosted zones and DNS records.
- **AWS WAF managed rules:** Help detect and block common web application attacks.
- **Custom WAF rules:** Allow traffic filtering based on defined conditions such as IP addresses, request patterns and headers.
- **Request monitoring:** Helps identify suspicious traffic and understand web application threats.

## 6. Lessons Learned

This project improved my understanding of how DNS resolution, content delivery and web application security work together in cloud environments.

I learned how Route 53 directs traffic through DNS, how CloudFront improves content delivery through caching and edge locations, and how AWS WAF filters potentially harmful web requests.

Although practical deployments were not completed, the conceptual study provided a foundation for understanding how these services contribute to the security, performance and availability of web applications.
