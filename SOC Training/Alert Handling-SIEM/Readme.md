Alert Handling – SIEM Investigation

This repository documents my hands-on experience investigating security alerts in a SIEM environment.
In this exercise, I analyzed three different alerts, determined their nature, and provided a final security verdict for each.

The objective of this task was to practice:

Alert analysis

Log investigation

Identifying true vs false positives

Documenting security findings

Alerts Overview
Alert #	Alert Type	Verdict
1	Large Data Transfer to Zoom	False Positive
2	Double-Extension Executable	True Positive
3	GitHub Download	False Positive
Alert 1 – Large Data Transfer to Zoom

Verdict: False Positive

Description

This rule detects 5 GB or more of data sent from a single device to a single destination within a day, which may indicate possible data exfiltration.

Alert Details

Destination: *.zoom.us

Source IP: 192.168.45.66

Source Network: UK04/MEETINGROOM

Sent Data: 5.8 GB

Received Data: 5.2 GB

Analysis

The destination belongs to Zoom, a legitimate video conferencing platform.

The source device is in a meeting room network, which is commonly used for video calls.

High data transfer is expected during long or high-quality meetings.

Conclusion

The activity matches normal Zoom usage and shows no signs of data exfiltration.

Final Verdict: False Positive

Screenshot: Refer to the screenshot for details.

Alert 2 – Double-Extension Executable

Verdict: True Positive

Description

This rule detects files with double extensions such as *.pdf.exe or *.mp4.exe.
Attackers commonly use this technique in phishing attacks to trick users into opening malicious files.

Alert Details

Host: LPT-HR-009

Process Name: chrome.exe

User: S.Conway

Target File:
C:\Users\S.Conway\Downloads\cats2025.mp4.exe

Source URL:
https://freecatvideoshd.monster/cats2025.mp4.exe

File MD5:
14d8486f3f63875ef93cfd240c5dc10b

Analysis

The file uses a double extension to appear as a media file.

The source domain is suspicious and untrusted.

The file was downloaded through a browser, indicating a possible phishing attempt.

Conclusion

This behavior is consistent with malware delivery techniques.

Final Verdict: True Positive

Recommended Actions

Isolate the affected host.

Remove the malicious file.

Perform a full malware scan.

Provide user awareness training.

Screenshot: Refer to the screenshot for details.

Alert 3 – GitHub Download

Verdict: False Positive

Description

This rule detects any download from GitHub.
Although GitHub may host malicious content, it is also widely used for legitimate development activities.

Alert Details

Accessed URL:
https://github.com/facebook/react

Source User: G.Chandler

Source Host: LPT-IT-063

Source Network: VPN/DEVELOPERS

Analysis

The URL points to the official React repository.

The user belongs to the developer network.

Downloading open-source tools is normal developer behavior.

Conclusion

The activity is legitimate and expected for a developer.

Final Verdict: False Positive

Screenshot: Refer to the screenshot for details.

Skills Demonstrated

SIEM alert investigation

Log analysis

Threat identification

Incident response reasoning

Security documentation

Author

Hamza Akram
Cybersecurity Enthusiast | SOC Analyst Path

If you want, I can also:

Add GitHub badges (TryHackMe, certifications, etc.)

Create a professional README template for all your SOC labs

Help you structure your cybersecurity portfolio repository.



