Fatal errors can be frustrating, but they can be resolvable with some troubleshooting. This guide will help you identify and address common causes of fatal errors in BeyondATC.

## What is a Fatal Error?
A fatal error is a critical issue that stops BeyondATC from running as expected. These errors can have various causes, so it's essential to review the logs to pinpoint the exact issue.

## Steps to Troubleshoot Fatal Errors

### 1. Common scenarios and solutions

#### **Fatal errors before starting a flight or accessing settings**
- **Solution:** Delete the `config.json` file located at:
  ```
  %userprofile%\appdata\locallow\Skirmish Mode Games, Inc\BeyondATC
  ```
  This will reset your settings and may resolve the issue.

#### **Fatal errors related to traffic**
- **Solution:** Disable traffic temporarily to see if the error persists. This can help isolate whether traffic settings are the root cause.

#### **Fatal error when updating BeyondATC**
- **Solution:** Check your antivirus or Windows Security software. It's likely that a security program is blocking the update process. Add an exclusion for BeyondATC to resolve this issue.

### 2. Share your logs
If the above steps do not resolve your issue, please share your `player.log` file in our Discord support channel. This file contains critical information that helps us understand and address the error.

- **Log location:**
  ```
  %userprofile%\appdata\locallow\Skirmish Mode Games, Inc\BeyondATC
  ```
- **Support Channel:** [Discord Support](https://discord.com/channels/1082413096045391915/1316525717881880597)

We appreciate your patience while we work to resolve the issue!