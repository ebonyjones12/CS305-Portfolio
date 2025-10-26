# CS 305 Software Security Portfolio

## Artemis Financial Secure Software Project

This repository contains my completed **Practices for Secure Software Report** from Project Two, demonstrating my ability to implement enterprise-grade security features and conduct vulnerability assessments.

---

## Client Summary

**Artemis Financial** is a financial consulting company that creates personalized financial plans for customers, including savings, retirement planning, investments, and insurance services. The company wanted to modernize their operations by adding current and effective software security to protect client data and financial information. Specifically, they needed a file verification system using checksums and secure HTTPS communications to ensure data integrity and confidentiality when transmitting sensitive financial information through their web application.

---

## What I Did Well

When assessing Artemis Financial's software security vulnerabilities, I excelled at implementing a **defense-in-depth approach** with multiple layers of security rather than relying on a single security control. I successfully integrated industry-standard cryptographic algorithms (SHA-256), configured SSL/TLS certificates, and implemented automated vulnerability scanning all while maintaining clean, functional code.

**Why secure coding matters:** Secure coding is critical because software vulnerabilities can lead to data breaches, financial losses, legal penalties, and destroyed customer trust. For a financial services company like Artemis Financial, a single security breach could expose sensitive client information like social security numbers, bank accounts, and retirement plans, resulting in millions of dollars in damages and regulatory fines.

**Value to the company:** Software security adds immense value by protecting the company's reputation, ensuring regulatory compliance (GLBA, SEC requirements), reducing cyber insurance costs, preventing costly data breaches (average cost: $4.45 million), and building customer trust. Security-conscious companies have a competitive advantage in the marketplace.

---

## Challenging and Helpful Aspects

The most challenging part of the vulnerability assessment was configuring the OWASP Dependency-Check Maven plugin to work properly. I encountered authentication errors with the NVD API and OSS Index, requiring me to troubleshoot configuration settings and disable external API calls while still generating meaningful security reports.

This challenge was actually very helpful because it taught me that security tools don't always work perfectly out-of-the-box, you need to understand how they work, read documentation carefully, and adapt configurations to your specific environment. This real-world troubleshooting experience will be valuable in future security implementations.

---

## Increasing Layers of Security

I increased security through multiple layers:

1. **Transport Layer Security**: Converted HTTP to HTTPS with SSL/TLS certificate configuration
2. **Cryptographic Data Integrity**: Implemented SHA-256 checksum verification for detecting data tampering
3. **Secure API Design**: Created REST endpoints with proper input validation and error handling
4. **Dependency Monitoring**: Integrated automated vulnerability scanning with OWASP Dependency-Check
5. **Secure Coding Practices**: Applied proper exception handling, used established security libraries, and followed NIST standards

**Future vulnerability assessment tools I would use:**
- OWASP Dependency Check (for third-party library vulnerabilities)
- SonarQube (for code quality and security analysis)
- Burp Suite (for web application security testing)
- OWASP ZAP (for penetration testing)
- Static Application Security Testing (SAST) tools integrated into CI/CD pipelines

**Mitigation decisions:** I would prioritize vulnerabilities based on CVSS scores, exploitability, and business impact. Critical vulnerabilities in internet-facing applications handling sensitive data would be addressed first.

---

## Ensuring Functional and Secure Code

To ensure the code and application were both functional and secure, I followed a comprehensive testing approach:

**Functional Testing:**
- Manually reviewed all code for syntax errors
- Ran the application successfully and verified all features worked
- Tested the checksum endpoint with multiple inputs
- Confirmed HTTPS connections established properly
- Verified SSL certificate loaded correctly

**Security Testing:**
- Ran OWASP Dependency-Check to scan for known vulnerabilities
- Checked that no new security issues were introduced by my refactored code
- Verified proper error handling that doesn't expose sensitive information
- Confirmed encryption was working correctly
- Tested input validation on REST endpoints

**After refactoring:** I specifically ran the dependency-check tool again and compared results to ensure my code additions (SHA-256 implementation, SSL/TLS configuration, REST controller) did not introduce any new vulnerabilities. The scan confirmed that all identified vulnerabilities existed in the original framework dependencies, not in my new code.

---

## Helpful Resources and Tools

**Tools that will be helpful in future work:**
- **OWASP Dependency-Check**: Essential for identifying vulnerable libraries in any Java project
- **Java Keytool**: For certificate generation and management
- **Maven**: For dependency management and build automation
- **Spring Boot Security**: For implementing authentication and authorization
- **Postman**: For testing REST API endpoints

**Coding practices I'll continue using:**
- Always use established cryptographic libraries (like Java's MessageDigest) rather than creating custom encryption
- Implement multiple layers of security (defense in depth)
- Add proper try catch blocks and error handling for security functions
- Follow industry standards (NIST, OWASP) rather than making up security approaches
- Document security decisions and configurations clearly
- Use automated security scanning as part of the development process

**Resources:**
- OWASP Top 10 vulnerabilities guide
- NIST Cryptographic Standards documentation
- Java Security API documentation
- Spring Security reference materials

---

## Demonstrating Skills to Future Employers

From this assignment, I would show future employers:

1. **The Complete Secure Software Report** - Demonstrates my ability to document security implementations professionally and explain technical concepts clearly

2. **Code Implementation** - Shows hands-on ability to:
   - Implement SHA-256 cryptographic hashing
   - Configure SSL/TLS certificates
   - Build secure REST APIs
   - Handle errors securely
   - Follow secure coding best practices

3. **Vulnerability Assessment Results** - Proves I can use industry-standard security tools and interpret their results

4. **Screenshots of Working Application** - Visual proof that I can deliver functional, secure software

5. **Problem-Solving Skills** - The project demonstrates I can troubleshoot complex security issues like Maven dependency conflicts and certificate configuration problems

**Key talking points for interviews:**
- "I implemented enterprise-level security for a financial application, including encryption, SSL/TLS, and vulnerability scanning"
- "I understand the importance of defense-in-depth security strategies"
- "I can use industry standard tools like OWASP Dependency-Check to assess security risks"
- "I follow NIST cryptographic standards and security best practices"
- "I know how to balance security requirements with functional requirements"

This project demonstrates that I don't just write code I write **secure** code that protects sensitive data and meets industry compliance requirements.

---

## Technologies Used

- Java
- Spring Boot
- SHA-256 Cryptography
- SSL/TLS Certificates
- HTTPS Protocol
- Maven
- OWASP Dependency-Check
- REST API Development
- Security Best Practices (NIST, OWASP)

---

## Project Artifacts

- **Practices for Secure Software Report** (included in this repository)
- **Refactored Secure Code** (ssl-server_student project)
- **Dependency Check Reports**
- **SSL Certificate Generation**

---

**Author:** Ebony Jones  
**Course:** CS 305 Software Security  
**Date:** October 2025
