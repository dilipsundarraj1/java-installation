# ☕ Install Java using SDKMAN! on Windows (Step-by-Step Guide)

> ⚠️ **Note:** SDKMAN! doesn't run natively on Windows.  
> It works inside **WSL (Windows Subsystem for Linux)** — a lightweight Linux environment for Windows.

---

## 📑 Table of Contents

- [STEP 1: Open PowerShell as Administrator](#-step-1-open-powershell-as-administrator)
- [STEP 2: Install WSL + Ubuntu](#-step-2-install-wsl--ubuntu)
- [STEP 3: Launch Ubuntu](#-step-3-launch-ubuntu)
- [STEP 4: Prepare Ubuntu](#️-step-4-prepare-ubuntu)
- [STEP 5: Install SDKMAN!](#-step-5-install-sdkman)
- [STEP 6: Install Java via SDKMAN!](#-step-6-install-java-via-sdkman)
- [STEP 7: Verify Installation](#-step-7-verify-installation)
- [STEP 8: (Optional) Install Build Tools](#-step-8-optional-install-build-tools)
- [STEP 9: Use Java in Your IDE](#-step-9-use-java-in-your-ide)

---

## 🪟 STEP 1: Open PowerShell as Administrator

You can do this in any of the following ways:

- **Start Menu:**  
  Click **Start → type "PowerShell" → Right-click → Run as Administrator**

- **Keyboard Shortcut:**  
  Press **Windows + X → Windows PowerShell (Admin)**

- **Run Command:**  
  Press **Windows + R**, type `powershell`, and hit **Enter**

> ✅ Check: The PowerShell title bar should say **“Administrator: Windows PowerShell”**

---

## 🧱 STEP 2: Install WSL + Ubuntu

In **PowerShell (Admin)**, run:

```powershell
wsl --install -d Ubuntu
```

This installs Ubuntu Linux inside Windows.

If WSL is already installed, run:

```powershell
wsl --update
```

After installation, restart your computer when prompted.

---

## 🐧 STEP 3: Launch Ubuntu

Open Ubuntu from the Start menu.

Create a Linux username and password (this is separate from Windows).

You'll now be inside the Linux terminal:

```bash
username@PC:~$
```

---

## ⚙️ STEP 4: Prepare Ubuntu

Run the following commands:

```bash
sudo apt-get update
sudo apt-get install -y curl zip unzip ca-certificates
```

---

## 📦 STEP 5: Install SDKMAN!

Run these commands:

```bash
curl -s "https://get.sdkman.io" | bash
source "$HOME/.sdkman/bin/sdkman-init.sh"
sdk version
```

If you see a version number — SDKMAN! is successfully installed 🎉

---

## ☕ STEP 6: Install Java via SDKMAN!

List all available Java versions:

```bash
sdk list java
```

Choose the desired JDK identifier (e.g., `21.0.4-tem` for Temurin 21 LTS).

Install and set it as default:

```bash
sdk install java 21.0.4-tem
sdk default java 21.0.4-tem
```

---

## 🔍 STEP 7: Verify Installation

Run:

```bash
java -version
echo $JAVA_HOME
```

You should see your Java version and a JAVA_HOME path like:

```
/home/username/.sdkman/candidates/java/current
```

---

## 🧰 STEP 8: (Optional) Install Build Tools

Install Maven or Gradle if needed:

```bash
sdk install maven
sdk install gradle
```

---

## 🧩 STEP 9: Use Java in Your IDE

**VS Code (with WSL Extension):**

It will automatically detect the SDKMAN! Java.

**IntelliJ IDEA (Windows):**

Add a new JDK with the path:

```
\\wsl$\Ubuntu\home\<your-ubuntu-username>\.sdkman\candidates\java\current
```
