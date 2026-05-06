# Capstone Assessment: Prioritized Risk Analysis for "ConnectSphere"

---

## Deliverable 1: Cybersecurity Governance Review Card

### Risk Analysis Table

| Section | Issue / Definition | Impact | Suggested Fix / Mitigation |
|---------|-------------------|--------|---------------------------|
| **1. Confidentiality Risk** | PII transmitted over unencrypted channels (violates CIA Triad – Confidentiality) | Exposure of sensitive user data (names, emails, company info) to attackers | Enforce HTTPS/TLS encryption for all data in transit; implement secure API communication |
| **2. Integrity Risk** | Lack of input validation (violates Secure SDLC & Input Validation principles) | Risk of injection attacks (SQL, XSS) leading to data corruption or manipulation | Implement strict input validation and sanitization; use parameterized queries and validation libraries |
| **3. Availability Risk** | No logging or incident response mechanisms (violates CIA Triad – Availability) | Delayed detection of attacks leading to prolonged downtime or service disruption | Implement centralized logging, monitoring tools, and an incident response plan |

### Monitoring / Reporting Recommendation

- **Metric to Monitor:** Failed Login Attempt Rate
- **Definition:** Number of failed login attempts per minute/hour across the platform
- **Visualization Type:** Line Chart
- **Why It Matters:** Helps detect brute-force attacks early and supports proactive security response

---

## Deliverable 2: Corrected Architecture Diagram (Annotations)

**1. Implement HTTPS/TLS Encryption**
- *Change:* All communication between client and server secured using HTTPS
- *Why:* Protects PII in transit and ensures confidentiality

**2. Enforce API Access Control (RBAC + PoLP)**
- *Change:* Introduce Role-Based Access Control and restrict endpoints based on user roles
- *Why:* Prevents unauthorized data access and reduces risk of privilege escalation

**3. Add Input Validation & Sanitization Layer**
- *Change:* Validate all incoming data at API gateway and backend
- *Why:* Prevents injection attacks and protects system integrity

**4. Secure Session Management**
- *Change:* Use secure cookies, session expiration, and token-based authentication (JWT/OAuth2)
- *Why:* Prevents session hijacking and unauthorized access

**5. Enable Logging & Incident Response System**
- *Change:* Integrate logging tools (e.g., audit logs, SIEM systems)
- *Why:* Ensures traceability, supports incident detection and response

---

## Deliverable 3: Summary of Review Process

The review process for ConnectSphere was conducted using established cybersecurity governance principles, including the CIA Triad, Principle of Least Privilege (PoLP), and Secure Software Development Lifecycle (SSDLC). First, the system architecture and project brief were analyzed to identify weaknesses in data handling, access control, and system resilience. Risks were then categorized into confidentiality, integrity, and availability to ensure a structured and comprehensive evaluation.

Confidentiality risks were identified in the lack of encryption for data in transit, exposing sensitive personal and professional information. Integrity issues were found in the absence of input validation, making the system vulnerable to injection attacks that could compromise data accuracy and trust. Availability concerns stemmed from missing logging and incident response mechanisms, limiting the system's ability to detect and recover from attacks efficiently.

Applying PoLP helped highlight overly permissive API access, leading to recommendations for role-based access control. SSDLC principles guided the inclusion of secure coding practices such as input validation and continuous testing. These improvements strengthen compliance with regulations like GDPR and CCPA by enhancing data protection, user privacy, and accountability.

The recommended monitoring metric, failed login attempt rate, supports ethical and transparent governance by enabling early detection of suspicious behavior such as brute-force attacks. This ensures proactive security management while maintaining system availability and user trust.

Overall, the proposed mitigations improve ConnectSphere's security posture, ensure regulatory alignment, and support sustainable, secure platform growth.
