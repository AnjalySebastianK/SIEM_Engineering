# SIEM Components

## Understanding SIEM Components
A SIEM platform is built on several core components that work together to collect, process, and analyze security data. Each component plays a specific role in ensuring that logs and events are captured, standardized, and stored for monitoring and investigation. Below is a detailed explanation of these components.

---

## Log Collection
Log collection is the process of gathering raw event data from multiple sources across the enterprise.  
- These sources include servers, firewalls, intrusion detection systems, cloud applications, and endpoints.  
- Collection can be done using agents installed on devices or through agentless methods such as syslog.  
- The goal of log collection is to ensure that no critical security event goes unnoticed, providing a complete picture of activity across the environment.  

---

## Data Ingestion
Data ingestion refers to the way SIEM systems bring collected logs into the platform for processing.  
- It involves transferring logs from source systems into the SIEM in real time or batch mode.  
- Ingestion pipelines handle large volumes of data, ensuring scalability and reliability.  
- This step is critical because it determines how quickly and efficiently the SIEM can process incoming information.  

---

## Parsing
Parsing is the process of breaking down raw log data into structured fields that the SIEM can understand.  
- For example, a firewall log might contain an IP address, timestamp, and action taken.  
- Parsing extracts these elements and labels them clearly so they can be analyzed.  
- Without parsing, logs remain unstructured text, making it difficult to search or apply detection rules.  

---

## Normalization
Normalization ensures that data from different sources is converted into a consistent format.  
- Different systems may use different field names (e.g., `src_ip`, `SourceAddress`, `client_ip`).  
- Normalization translates these into a standard schema such as `source.ip`.  
- This consistency allows analysts to run queries, build dashboards, and apply correlation rules across all data sources without confusion.  

---

## Storage
Storage is the component that retains logs and events for future analysis and compliance.  
- SIEM systems store data in databases or indexed repositories that support fast searching.  
- Storage must balance performance with retention requirements, since compliance standards often require logs to be kept for months or years.  
- Proper storage ensures that analysts can perform forensic investigations and generate historical reports when needed.  

---

## Key Takeaway
Together, these components — log collection, data ingestion, parsing, normalization, and storage — form the backbone of a SIEM system. They ensure that raw security data is captured, transformed into usable information, and retained for monitoring, detection, and compliance purposes.
