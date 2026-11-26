
# AWS Application Load Balancing

## 1. Project Overview and Objectives

This project focused on deploying an Application Load Balancer (ALB) to distribute incoming HTTP traffic across two EC2 instances in a custom VPC.

The objective was to understand how an ALB receives application requests, forwards traffic to registered targets, monitors target health, and maintains application availability when a target becomes unavailable.

## 2. Architecture and Resource Design

The architecture used an internet-facing Application Load Balancer connected to two EC2 instances deployed across two Availability Zones.

**Traffic flow:**

`Client → Application Load Balancer → Target Group → EC2 Instances`

Both EC2 instances hosted Nginx and returned a custom web page when accessed through the load balancer.

The ALB was deployed across two public subnets, while the EC2 instances were registered as targets in the target group.

## 3. AWS Services and Configurations

- **Application Load Balancer:** Created `CloudSecurity-ALB-Lab` as an internet-facing, IPv4 load balancer in the custom VPC.

  ![Created Application Load Balancer](screenshots/Created%20Application%20Load%20Balancer.png)

- **Network Mapping:** Selected two public subnets across two Availability Zones to provide the ALB with network connectivity across both zones.

  ![Configured ALB Network Mapping](screenshots/Configured%20ALB%20Network%20Mapping.png)

- **ALB Security Group:** Configured an inbound rule allowing HTTP traffic on TCP port 80 from `0.0.0.0/0`.

  ![Configured ALB Security Group](screenshots/Configured%20ALB%20Security%20Group.png)

- **Listener:** Configured an HTTP listener on port 80 to forward incoming requests to the target group.

  ![Configured ALB Listener](screenshots/Configured%20ALB%20Listener.png)

- **Target Group:** Created `CloudSecurity-ALB-TG` with instance targets, HTTP on port 80, and `/` as the health check path.

  ![Created Target Group](screenshots/Created%20Target%20Group.png)

- **EC2 Instances:** Registered two Ubuntu EC2 instances running Nginx as targets in the target group.

- **Target Health:** Verified that both registered EC2 instances passed their health checks.

  ![Verified Healthy EC2 Targets](screenshots/Verified%20Healthy%20EC2%20Targets.png)

## 4. Implementation and Key Decisions

The ALB was configured to receive incoming HTTP requests through its listener on port 80 and forward them to the registered EC2 instances through the target group.

The security groups were configured to control traffic between the load balancer and the EC2 instances:

- The ALB security group allowed inbound HTTP traffic on TCP port 80.
- The EC2 security group allowed HTTP traffic on TCP port 80 from the ALB security group.
- SSH access to the EC2 instances remained restricted to my IP address.

Both EC2 instances had Nginx installed and were configured to serve a custom application response.

The target group's default routing algorithm, round robin, was retained after exploring other routing algorithm options.

## 5. Security Considerations

- Used separate security groups for the ALB and EC2 instances.
- Allowed HTTP traffic to the EC2 instances only from the ALB security group.
- Restricted SSH access to my IP address.
- Deployed the ALB across two Availability Zones.
- Used target health checks to determine which registered instances were healthy and eligible to receive traffic.

## 6. Testing and Validation

I tested the ALB using its DNS name in a web browser.

The application returned the custom response:

`Hello from AWS EC2! My Application Load Balancer practical is working.`

![Verified ALB Application in Browser](screenshots/Verified%20ALB%20Application%20in%20Browser.png)

I also verified that both EC2 instances were registered and healthy in the target group.

**Target availability test:**

To test how the ALB handled an unavailable target, I stopped the second EC2 instance.

The stopped instance was no longer available to serve application traffic, and the ALB routed requests to the remaining healthy instance.

After the test, I restarted the second instance.

## 7. Troubleshooting and Findings

The target health status helped me understand how the ALB monitors registered EC2 instances before forwarding application traffic.

During the availability test, stopping one EC2 instance changed its target status to `Unused`. The ALB continued forwarding requests to the remaining healthy target.

This demonstrated the importance of health checks and having multiple registered targets across Availability Zones.

## 8. Lessons Learned

This project gave me practical experience configuring an Application Load Balancer, creating a target group, setting up listeners and health checks, and connecting multiple EC2 instances.

I also learned how security groups control traffic between the load balancer and its targets, and how the ALB responds when one registered instance becomes unavailable.

The exercise helped me understand how load balancing supports application availability and distributes incoming traffic across healthy targets.
