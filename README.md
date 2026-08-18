# Privacy Policy for NetProbe: Net Recon & OSINT

**Effective Date:** August 18, 2026  
**Last Updated:** August 18, 2026  

This Privacy Policy governs the data processing practices of **NetProbe: Net Recon & OSINT** (hereinafter referred to as "the Application"). NetProbe is designed as an offline-first network reconnaissance, penetration testing, and Open Source Intelligence (OSINT) automation platform for Android devices.

We highly respect your privacy and are committed to protecting the integrity of your data.

---

## 1. Information Collection and Use

### 1.1 Local Storage and Sandbox Execution
The Application operates entirely within the Android application sandbox. 
* **Zero Server-Side Tracking:** We do not own, operate, or maintain any external servers, backends, or cloud services to track your usage.
* **Local Database:** All gathered intelligence reports, session histories, discovered subdomains, tested web forms, and infrastructure metadata are compiled using an encrypted local SQLite database built inside your device's isolated storage. 

### 1.2 Network Activity and External API Requests
To perform its core utility features (such as GeoIP resolution, DNS-over-HTTPS lookups, Active Directory Busting, and Passive OSINT extraction), the Application initiates direct outbound TCP/UDP socket connections from your device to the target hosts specified manually by you.
* **Third-Party Endpoints:** The Application utilizes public trusted DNS-over-HTTPS endpoints (such as Cloudflare DNS) and passive transparency databases (such as crt.sh). These interactions are direct client-to-server communications. No intermediate middleware tracks or logs these requests on our behalf.
* **Offline Databases:** Geolocation Lookups are performed entirely offline using local target databases compiled within the Application's assets, eliminating external tracking footprints.

---

## 2. Permissions Required and Justification

To provide advanced network testing capabilities under Android 16 (Target SDK 36), the Application requires the following system permissions:

* `android.permission.INTERNET`: Required to initiate network socket handshakes, perform HTTP/HTTPS audits, and execute load resiliency tests (HTTP Flood, Slowloris, RUDY).
* `android.permission.ACCESS_NETWORK_STATE`: Required to monitor real-time cellular/Wi-Fi connection states and prevent connection drops during heavy automation conveyor operations.

---

## 3. Data Retention and Deletion

Because all scan results and configuration preferences are retained locally on your mobile device, **you have complete control over your data:**
* You can erase specific targets and logs directly within the "History" and "Advanced Configurator" tabs of the Application.
* You can instantly wipe the entire database by utilizing the standard Android OS settings: **Settings ➔ Applications ➔ NetProbe ➔ Storage ➔ Clear Data / Clear Cache**.
* Uninstalling the Application will completely and permanently destroy all database records, reports, and exported configurations from the device.

---

## 4. Security

As a platform designed for cybersecurity professionals, security is our top priority. NetProbe uses non-blocking asynchronous `Java NIO Selectors` and safe parsing routines via `Jsoup` to handle web document objects securely without exposing the device to code execution vulnerabilities. However, since data is stored locally, the physical and logical security of the records ultimately relies on your device's operating system lock screen, disk encryption, and security parameters.

---

## 5. Changes to This Privacy Policy

We may update our Privacy Policy from time to time. Any modifications will be committed directly to this GitHub repository file. You are advised to review this page periodically for any changes.

---

## 6. Contact Us

If you have any questions, bug reports, or architectural suggestions regarding this Privacy Policy or the cryptographic implementations of the platform, feel free to open an **Issue** or submit a **Pull Request** directly within this GitHub repository.
