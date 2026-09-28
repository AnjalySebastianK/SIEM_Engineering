# Correlation Rules

## Understanding Correlation Rules
Correlation rules are the backbone of SIEM detection logic. They define how multiple events are linked together to identify suspicious activity, reduce false positives, and provide visibility into potential threats. By applying correlation rules, SOC teams can move beyond isolated alerts and detect complex attack patterns.

---

## Detection Logic
Detection logic refers to the conditions and rules that determine when an alert should be triggered.  
- It translates security knowledge into actionable rules, such as “10 failed logins in 1 minute.”  
- Detection logic can be signature‑based, anomaly‑based, or behavior‑based.  
- Well‑designed logic ensures that alerts are meaningful and reduces unnecessary noise.  
- For example, a rule may detect privilege escalation attempts by monitoring changes in user roles combined with unusual login activity.  

---

## Event Correlation
Event correlation is the process of linking multiple events across different sources to build context.  
- A firewall log showing suspicious outbound traffic may be correlated with endpoint logs showing malware execution.  
- Correlation helps analysts see the bigger picture rather than isolated events.  
- It reduces false positives by validating activity across multiple systems.  
- Event correlation is essential for detecting advanced persistent threats (APTs) and multi‑stage attacks.  

---

## Alert Conditions
Alert conditions define the thresholds or criteria that must be met for an alert to be generated.  
- Conditions may include time windows, frequency of events, or specific combinations of actions.  
- For example, “five failed login attempts followed by a successful login from a new country” could trigger an alert.  
- Alert conditions ensure that alerts are triggered only when suspicious activity is significant enough to warrant investigation.  
- They help prioritize alerts based on severity and relevance.  

---

## Risk‑Based Detections
Risk‑based detections assign a risk score to events and alerts based on their potential impact.  
- Instead of treating all alerts equally, risk scoring highlights the most critical incidents.  
- Factors such as user role, asset importance, and threat intelligence feeds influence the risk score.  
- For example, a failed login attempt on a domain controller may be scored higher than the same attempt on a test server.  
- Risk‑based detections help SOC teams focus on high‑priority threats and allocate resources effectively.  

---

## Threat Visibility
Correlation rules enhance overall threat visibility by connecting clues across the environment.  
- They allow analysts to detect hidden attack chains that span multiple systems.  
- Visibility improves proactive threat hunting, enabling analysts to spot anomalies before they escalate.  
- By enriching alerts with context, correlation rules provide a holistic view of attacker behavior.  
- Threat visibility ensures that organizations can respond quickly and decisively to evolving threats.  

---

## Key Takeaway
Correlation rules transform raw events into actionable intelligence. By combining detection logic, event correlation, alert conditions, and risk‑based detections, SIEM systems provide enhanced threat visibility and empower SOC teams to detect and respond to complex attacks effectively.
