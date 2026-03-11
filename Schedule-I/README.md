While initial automated sandboxing (Falcon/Hybrid Analysis) returned a 50/100 Threat Score, manual detonation in a controlled REMnux environment confirms this as a False Positive.

During a 15-minute live capture via Wireshark (with INetSim active), the executable exhibited zero outbound network communication to external WAN IP addresses. All detected traffic was restricted to internal link-local protocols (ARP/IGMP) between the Guest and Host. The 'Malicious' flag in automated scanners is likely a result of the SteamRIP DRM-bypass/Steamless injection method, which mimics suspicious process behavior without actually containing a malicious payload.

## Schedule I - Malware Analysis Report

**Date:** March 10, 2026  
**Verdict:** ✅ VERIFIED SAFE (False Positive)

### Analysis Details
- **Source:** SteamRIP
- **Observed Behavior:** No external network requests during 15-minute detonation.
- **Scanner Conflict:** Hybrid Analysis (Falcon) reported 50/100; VirusTotal reported 0/70.
- **Conclusion:** The malicious flag is due to DRM-bypass/Process Injection methods, not actual malware telemetry.

### Files in this Repository
- `Schedule_I_Clean_Log.pcapng`: Raw Wireshark network capture. 
  *(Download this and open in Wireshark to verify zero outbound WAN traffic.)*
