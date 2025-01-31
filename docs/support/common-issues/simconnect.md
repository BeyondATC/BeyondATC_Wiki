# Troubleshooting connection issues with BeyondATC  

If you're having trouble connecting to BeyondATC or if BeyondATC is unable to connect to your simulator, please follow these steps to diagnose and resolve the issue.  

---

## 1. Check if the services are online  

Visit [BeyondATC Status Page](https://status.beyondatc.app/) to verify that all services are operational.  

---

## 2. DNS Accessibility  

If you **cannot** access [BeyondATC Status Page](https://status.beyondatc.app/), the issue is likely related to your DNS settings or your ISP blocking access to our services. Users from Turkey and Hong Kong have reported similar issues as an example.  

### What to do:  
- Check if any software is blocking BeyondATC (e.g., **Antivirus, Firewall, or third-party software like NextDNS**). Adjust the settings or temporarily disable them to troubleshoot.  
- If the problem persists, try using a **VPN** to rule out ISP-related restrictions.  

---

## 3. Security software  

Ensure that your **antivirus, firewall, or Windows Security** is not blocking BeyondATC from accessing the internet. Additionally, check your **quarantine folder** for any blocked BeyondATC files.  

If a file is quarantined:  
1. Restore the file.  
2. Add an **exception** for the entire BeyondATC folder in your security software.  

---

## 4. Starting BeyondATC correctly  

To ensure proper connection, follow these steps in order:  

1. **Start your simulator** (MSFS should be at least in the main menu, preferably with your aircraft loaded at the departure airport).  
2. **Start BeyondATC**, ensure you have a valid **SimBrief flight plan**, and click **Fly**.  

---

## 5. SimConnect process issue  

Sometimes, lingering processes may interfere with connectivity.  

### Steps to resolve:  
1. **Close** MSFS and BeyondATC.  
2. Open **Task Manager** and check if `simconnect_ws.exe` is still running.  
3. If found, **end the process** manually.  
4. Restart **MSFS and BeyondATC**.  

---

## 6. Running with administrator privileges  

If BeyondATC still fails to connect, try running it with **administrator privileges**:  

1. Right-click the BeyondATC shortcut.  
2. Select **Run as administrator**.  

---

## 7. Restarting your PC  

Some issues are session-specific. A simple **restart** of your PC can sometimes resolve unexpected problems.  

---

## 8. Reinstalling BeyondATC  

If none of the above steps work, try reinstalling BeyondATC:  

1. **Uninstall** BeyondATC.  
2. Manually **delete** the BeyondATC folder located at:  
   `%userprofile%\AppData\LocalLow\Skirmish Mode Games, Inc\`
3. Download the latest version from the [BeyondATC website](https://beyondatc.app/).  
4. **Run the installer as an administrator**.  

---

If you continue to experience issues, feel free to reach out to our **support team** for further assistance on Discord.
