#   Firewall Setup and Rules Management (Windows)

##  Objective

To configure and test basic firewall rules on Windows using **Windows
Defender Firewall with Advanced Security**.

------------------------------------------------------------------------

##  Steps Performed

### 1. Open Firewall

-   Press **Win + R** → type `wf.msc` → Enter.\
-   This opens **Windows Defender Firewall with Advanced Security**.

### 2. View Existing Rules

-   Navigated to **Inbound Rules** and **Outbound Rules** to see current
    configurations.

### 3. Block Telnet (Port 23)

1.  In **Inbound Rules** → Click **New Rule**.\
2.  Select **Port** → Next.\
3.  Choose **TCP**, Specific Local Port: `23`.\
4.  Action: **Block the connection**.\
5.  Applied to **Domain, Private, Public** profiles.\
6.  Named the rule: **Block Telnet (Port 23)**.

 Result: Attempting `telnet localhost 23` failed (as expected).

### 4. Allow SSH (Port 22)

1.  Created a new inbound rule for **TCP Port 22**.\
2.  Action: **Allow the connection**.\
3.  Applied to all profiles.\
4.  Named it: **Allow SSH (Port 22)**.

 Result: SSH traffic allowed (if OpenSSH is installed on Windows).

### 5. Remove Block Rule

-   Located **Block Telnet (Port 23)** in Inbound Rules.\
-   Right-click → **Disable Rule** / **Delete Rule**.\
-   Restored firewall to original state.


------------------------------------------------------------------------

##  Key Learnings

-   **Firewall** filters traffic based on rules (inbound/outbound).\
-   **Blocking unsafe ports** (like Telnet on port 23) improves
    security.\
-   **Allowing only required ports** (e.g., SSH) ensures controlled
    access.\
-   Windows Firewall provides **fine-grained traffic control** for
    applications and ports.

------------------------------------------------------------------------

##  Deliverables

-   Screenshots of firewall rule setup.\
-   This README explaining steps and results.

------------------------------------------------------------------------
