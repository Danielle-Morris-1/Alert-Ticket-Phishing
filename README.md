# Alert Ticket – Phishing Attempt

**Scope:** This activity involved the initial analysis of a security alert triggered by a user opening a potentially malicious file received via a phishing email. The investigation focused on identifying key indicators within the email and attachment to determine the nature and severity of the threat. 

## 📄 Ticket Summary

| **Ticket ID** | **Alert Message**        | **Severity** | **Status**   |
|---------------|---------------------------|--------------|--------------|
| A-2703        | Phishing attempt – possible download of malware | Medium       | Escalated   |

## Additional Information 

### 🧪 Known Malicious File Hash
```
54e6ea47eb04634d3e87fd7787e2136ccfbcc80ade34f246a12cf93bab527f6b
```

### 📧 Email Snapshot
- **From**: Def Communications `<76tguyhh6tgftrt7tg.su>`  `114.114.114.114`
- **To**: `<hr@inergy.com>`  `176.157.125.93`
- **Sent**: Wednesday, July 20, 2022 – 09:30 AM
- **Subject**: Re: Infrastructure Egnieer role

**Body**:
> Dear HR at Ingergy,
> 
> I am writing for to express my interest in the engineer role posted from the website.
> There is attached my resume and cover letter. For privacy, the file is password protected. Use the password paradise10789 to open. 
>
>  Thank you,
> Clyde West

**Attachment**: `bfsvc.exe` (malicious executable)

---

## 🔍 Ticket Details

An alert was generated after a user opened a malicious file from a **phishing email**. Key indicators included:

1.  **Header Analysis:** I examined the sender's email address (`76tguy6hh6tgftrt7tg.su`) and compared it against the sender name ("Clyde West") and alias ("Def Communications"). The discrepancies I noted were indicative of phishing.
2.  **Content Review:** I analyzed the email body, identifying suspicious elements such as grammatical errors and an unusual subject line ("Infrastructure Engineer role").
3.  **Attachment Scrutiny:** I noted the presence of a password-protected executable attachment (`bfsvc.exe`), recognizing this as a common tactic used to evade initial security scans.
4.  **Threat Intelligence Verification:** I utilized available threat intelligence (implicitly through the alert flagging the file hash) to confirm the malicious nature of the attached file. The file hash's prior identification as malicious strongly suggested a known threat.
5.  **Malware Identification:** Further investigation revealed the file hash was associated with "Flagpro" malware, a tool reportedly used by the advanced persistent threat (APT) group **BlackTech**, indicating a potentially sophisticated attack.

![image](https://github.com/user-attachments/assets/3072669a-ec58-489d-9348-385656d3e230)

---

## 🚨 Actions Taken

- Escalated to a **Level 2 SOC Analyst** for deeper analysis and containment.
- Documented and confirmed malicious behavior using threat intelligence (known hash).
- Alert severity rated as **Medium**, due to confirmed malware interaction.

---
