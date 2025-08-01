---
title: Splunk Cheat Sheet
nav_order: 3
description: Reference Index - Splunk search queries and usage notes
parent: Cheat Sheets
has_children: false
permalink: /splunk-cheat-sheet/
---

## Splunk Threat Hunting Examples

### Outbound anomalies in traffic
```splunk
index=your_index sourcetype=your_sourcetype 
| stats sum(bytes_out) as total_bytes by src_ip 
| eventstats avg(total_bytes) as avg_bytes 
| where total_bytes > avg_bytes*2
```

---

### Failed, followed by a successful login
```splunk
index=your_index sourcetype=your_sourcetype 
| transaction maxspan=1h startswith="Failed Login" endswith="Successful Login" 
| search Failed AND Successful
```

---

### Rapidly changing firewall rules
```splunk
index=your_index sourcetype=your_sourcetype 
| timechart span=1h count by firewall_rule 
| streamstats window=3 sum(count) as total_count by firewall_rule 
| where total_count > 10
```

---

### Spikes to uncommon ports
```splunk
index=your_index sourcetype=your_sourcetype 
| stats count by dest_port 
| sort -count 
| where count > 100 AND NOT dest_port IN (80, 443, 22)
```

---

### Identify large file downloads
```splunk
index=your_index sourcetype=your_sourcetype 
| rex field=_raw "GET\\s(.*)\\sHTTP/1.1\"\\s\\d+\\s(\\d+)" 
| where tonumber($2) > 1000000
```

---

### Analyze DNS activity on subdomains
```splunk
index=your_index sourcetype=your_sourcetype 
| rex field=query "\\.(?<subdomain>[^.]+)\\." 
| stats count by subdomain 
| sort -count 
| where count > 10
```

---

## Documentation and Community
- [Splunk Documentation](https://docs.splunk.com/)
- [Splunk Community](https://community.splunk.com/)
- [SplunkBase](https://splunkbase.splunk.com/)
