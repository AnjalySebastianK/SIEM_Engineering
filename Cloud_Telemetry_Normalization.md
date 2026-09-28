# Cloud Telemetry Normalization

## Understanding Cloud Telemetry Normalization
Cloud telemetry normalization is the process of converting raw alerts and logs from cloud platforms into a consistent, structured format that can be analyzed by SIEM systems. Since cloud providers like AWS and Azure generate logs in different formats, normalization ensures that these diverse data streams can be integrated, correlated, and searched effectively.

---

## Structural Integration
Structural integration refers to the way SIEM platforms connect with native cloud services to ingest telemetry.  
- Cloud providers expose APIs and logging services such as AWS CloudTrail, AWS GuardDuty, and Azure Activity Logs.  
- SIEM systems integrate with these services to pull alerts and events in real time.  
- Integration ensures that cloud‑specific events, such as IAM policy changes or suspicious network activity, are captured alongside traditional on‑premises logs.  
- This step provides a unified view of both cloud and enterprise environments.  

---

## Field Mapping
Field mapping is the process of aligning cloud‑specific fields with a standardized schema.  
- For example, AWS CloudTrail may record `userIdentity` while Azure Activity Logs may record `caller`.  
- Normalization maps both fields to a common attribute such as `user.name`.  
- GuardDuty findings may include fields like `resourceType` or `threatName`, which are mapped to standardized categories such as `event.type` or `threat.indicator`.  
- Field mapping ensures that queries and correlation rules can operate across multiple cloud providers without confusion.  

---

## Native Cloud Infrastructure Alerts
Cloud platforms generate alerts that reflect changes in infrastructure and security posture.  
- **AWS IAM Policy Modifications**: These alerts indicate changes to identity and access management policies, which could signal privilege escalation or misconfiguration.  
- **AWS GuardDuty Threat Findings**: These alerts highlight suspicious activity such as anomalous API calls, communication with known malicious IPs, or compromised credentials.  
- **Azure Activity Logs**: These alerts capture management operations such as resource creation, deletion, or role assignment changes.  

Normalization ensures that these alerts are translated into a consistent format so they can be correlated with other enterprise events.  

---

## Benefits of Normalization
- **Consistency**: Analysts can query logs using standardized field names across AWS, Azure, and other platforms.  
- **Correlation**: Normalized data allows detection of multi‑cloud attack patterns, such as simultaneous IAM changes in AWS and Azure.  
- **Searchability**: Structured and normalized data is easier to search, filter, and visualize.  
- **Compliance**: Normalization supports audit requirements by ensuring logs are categorized and retained in a consistent manner.  

---

## Key Takeaway
Cloud telemetry normalization transforms diverse cloud alerts into a unified schema through structural integration and field mapping. By normalizing events such as AWS IAM policy modifications and GuardDuty threat findings, organizations gain consistent visibility, enabling effective correlation, investigation, and compliance across multi‑cloud environments.
