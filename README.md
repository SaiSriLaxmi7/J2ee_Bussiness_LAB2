# J2ee_Bussiness_LAB2
The repository to complete a lab 1 for J2EE Bussiness Components

# Distributed Banking Operations Management System

## Summary of Business Case

CanSecure Bank, a multinational financial institution, is enhancing its IT infrastructure to support scalable and secure inter-branch operations. Each branch functions as an independent module communicating with the central banking hub using Enterprise JavaBeans (EJB) and Remote Method Invocation (RMI). The system uses Java Naming and Directory Interface (JNDI) for dynamic service discovery and Contexts and Dependency Injection (CDI) for loose coupling between components.

This project simulates such a system, providing remote and web-based banking services like deposits, withdrawals, and balance inquiries. It features stateless and stateful EJBs, RMI clients, CDI integration, and deployment on WildFly.

## Technology Stack and Setup Instructions

**Technologies used:**

- Java EE (Jakarta EE)  
- EJB (Stateless and Stateful Session Beans)  
- RMI (Remote Method Invocation)  
- JNDI (Java Naming and Directory Interface)  
- CDI (Contexts and Dependency Injection)  
- JSP, Servlet, JSTL for web interface  
- Maven for project management and build  
- WildFly Application Server (v26+)  
- Eclipse IDE or IntelliJ IDEA (recommended)

**Setup Instructions:**

1. Install JDK 11 or higher.  
2. Install Maven 3.6 or higher.  
3. Download and install WildFly Application Server (version 26 or above).  
4. Clone the project repository to your local machine.  
5. Build the project with Maven using the command:  
   `mvn clean install`  
6. The EAR file will be generated in `bank-ear/target/` directory.

## Deployment Steps (WildFly)

1. Start WildFly server using the standalone-full configuration:  
   - On Windows: `standalone.bat -c standalone-full.xml`

2. Access the WildFly Admin Console at [http://localhost:9990](http://localhost:9990) and log in with your management credentials.

3. Deploy the EAR package:

   - Go to the Deployments section.  
   - Upload the EAR file located at `bank-ear/target/bank-enterprise-app.ear`.  
   - Enable the deployment.

4. Access the web application in a browser at:  
   [http://localhost:8080/bank-web](http://localhost:8080/bank-web)

5. Test banking operations (deposit, withdraw, check balance) through the web interface or remote RMI client.



