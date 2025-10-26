
**Disk Space Needed for devcontainer:** 25 GB free space

----
**Prepared By:**
#### Ishaan Kathiriya
[Linkedin]((https://www.linkedin.com/in/ishaan-kathiriya)

---

# Windows Users:


## Option 1: Using Dev Container 

**(Recommended for this workshop if you don't have prior Linux experience)**


### **Step 1: Enable WSL2**

1. **Open PowerShell as Administrator:**
    - Click the **Start** button (Windows logo)
    - Type: `PowerShell`
    - **Right-click** on "Windows PowerShell"
    - Click **"Run as administrator"**
    - Click **"Yes"** when asked for permission
2. **Copy and paste this command:**

```powershell
   wsl --install
```

- Press **Enter**
- Wait for it to finish (takes 2-5 minutes)

3. **Restart your computer** when it asks you to
4. **After restart:**
    - Ubuntu will open automatically (black window with text)
    - It will say "Installing, this may take a few minutes..."
    - If ubuntu does not open automatically, search for **ubuntu** through your windows key and proceed further.
    - **Create a username:** Type any username you want (lowercase, no spaces) and press Enter
    - **Create a password:** Type a password and press Enter (you won't see the password as you type - this is normal!)
    - **Retype password:** Type the same password again and press Enter
    - **Remember this password!** You'll need it later
5. **Close the Ubuntu window** - you can click the X


---

### **Step 2: Install Docker Desktop** 

1. **Download Docker Desktop:**
    - Open your web browser
    - Go to: [https://www.docker.com/products/docker-desktop](https://www.docker.com/products/docker-desktop)
    - Click the big **"Download for Windows AMD"** button
    - Wait for download to complete (500-600 MB file)
2. **Install Docker Desktop:**
    - Go to your **Downloads** folder
    - **Double-click** on `Docker Desktop Installer.exe`
    - Check the box: ☑ **"Use WSL 2 instead of Hyper-V"** (Ignore if you don't see this option)
    - Click **"Ok"**
    - Wait for installation (takes 5-10 minutes)
    - Click **"Close and restart"** when done
    - Your computer will restart
3. **After restart, open Docker Desktop:**
    - Click **Start** button
    - Type: `Docker`
    - Click on **"Docker Desktop"**
    - You may see a service agreement - click **"Accept"**
    - You may be asked to sign up - click **"Skip"** or **"Continue without signing in"**
4. **Configure Docker:**
    - In Docker Desktop, click the Settings icon at the top right
    - Click **"Resources"** on the left
    - Click **"WSL Integration"**
    - Turn ON: **"Enable integration with my default WSL distro"** 
    - Make sure the toggle next to **"Ubuntu"** is ON (blue)
    - Click **"Apply & Restart"** at the bottom
    - Wait for Docker to restart (30 seconds)
5. **Verify Docker is working:**
    - In Docker Desktop, look for a **green** icon at the bottom left that says "Engine running"
    - If it's green, you're good! 



---

### **Step 3: Install Visual Studio Code**

1. **Download VS Code:**
    - Go to: [https://code.visualstudio.com/](https://code.visualstudio.com/)
    - Click the big **"Download for Windows"** button
    - Wait for download to complete
2. **Install VS Code:**
    - Go to your **Downloads** folder
    - **Double-click** on the file that starts with `VSCodeUserSetup`
    - Accept the agreement and click **"Next"**
    - Keep clicking **"Next"** (keep all default options)
    - **IMPORTANT:** On the "Select Additional Tasks" page, check ALL the boxes:
        - ☑ Add "Open with Code" action to Windows Explorer file context menu
        - ☑ Add "Open with Code" action to Windows Explorer directory context menu
        - ☑ Register Code as an editor for supported file types
        - ☑ Add to PATH
    - Click **"Next"**, then **"Install"**
    - Wait for installation
    - Click **"Finish"**
3. **Open VS Code:**
    - It should open automatically
    - If not, click **Start** and type `Visual Studio Code`



---

### **Step 4: Install VS Code Extensions**

1. **In VS Code, install WSL extension:**
    - Look at the left sidebar - find the icon that looks like 4 squares (Extensions)
    - Click on it
    - In the search box at the top, type: `WSL`
    - Find **"WSL"** by Microsoft (it will be the first result)
    - Click the blue **"Install"** button
    - Wait for it to install (you'll see "Installing..." then a checkmark)
2. **Install Dev Containers extension:**
    - In the same search box, clear it and type: `Dev Containers`
    - Find **"Dev Containers"** by Microsoft
    - Click the blue **"Install"** button
    - Wait for it to install



---

### **Step 5: Install Git** 

1. **Download Git:**
    - Go to: [https://git-scm.com/download/win](https://git-scm.com/download/win)
    - The download should start automatically (file named like `Git-2.x.x-64-bit.exe`)
2. **Install Git:**
    - Go to your **Downloads** folder
    - **Double-click** on the Git installer
    - Click **"Next"** for all screens (keep all default options)
    - Keep clicking **"Next"** until you see **"Install"**
    - Click **"Install"**
    - Click **"Finish"**
3. **Verify Git is installed:**
    - Click **Start** button
    - Type: `cmd`
    - Press **Enter** (a black window will open)
    - Type: `git --version`
    - Press **Enter**
    - You should see something like "git version 2.x.x"
    - **Close the window**


---


### Step 6: Clone the Workshop Files

#### **Option A: Download from Git Repository** (if instructor provides a Git link)

1. **Open Command Prompt:**
    - Click **Start** button
    - Type: `cmd`
    - Press **Enter**
2. **Navigate to Documents or your preferred folder:**
    - Run this command

```
   cd <your_username>\Documents
   
   example: cd C:\Users\ishaan
```

- Press **Enter**

3. **Clone the repository:**
   
	Repo Link:  [ros2_workshop](https://github.com/ishaankathiriya/ros2_workshop_devcontainer)
	 
	In the command prompt itself, enter the following command to clone the github repo:

```
git clone https://github.com/ishaankathiriya/ros2_workshop_devcontainer.git
```



**Alternate Option:**  Download the Zip file from the github repository by clicking on the 'Code' option and extract it to your desired location.



---
### **Step 7: Open the Workshop Folder in VS Code** 

1. **Open VS Code** 

2. **Open the folder:**
    - Click **"File"** at the top left
    - Click **"Open Folder"**
    - On the left, click the location where you cloned the repository (eg: Documents)
    - **Double-click** on the `ws_ros2_workshop` folder
    - Click **"Select Folder"** 


---
### Step 8: Build the Container

- Open the command pallet using `Ctrl + Shift + P`  and in it, type:
   Dev Containers: Rebuild and Reopen in Container

Now, just wait for the container to build.

**How to know it's done:**

- The bottom left corner will show: **"Dev Container: ROS2 Humble Desktop-Full"** in green
- The terminal will show a prompt like: `vscode@...:/ws_ros2_workshop$`


---



## Option 2: Dual - Boot your system with Ubuntu 22.04

--> Recommended only if you have enough free space (>100 GB)




---




# 2) Linux Users

**Assuming you have Ubuntu 22.04 installed**


### 1) Step 1: Install git

Run the following command:
```bash
sudo apt install git
```

### 2) Step 2: Install ROS2 Humble

1) Open the official documentation of ROS2 Humble and follow the installation steps
    [ROS2 Humble Documentation](https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debs.html)



### 3) Step 3: Clone the 'ubuntu' branch from the github repository

- Don't worry if there doesn't exist a branch named  *ubuntu*  yet. It will be updated soon.





---

# 3) MacOS Users



### **Step 1: Install Docker Desktop** 

1. **Download Docker Desktop:**
    - Open Safari or your browser
    - Go to: [https://www.docker.com/products/docker-desktop](https://www.docker.com/products/docker-desktop)
    - Click **"Download for Mac"**
    - Choose:
        - **"Mac with Intel chip"** if you have an older Mac
        - **"Mac with Apple chip"** if you have M1/M2/M3 Mac
    - Don't know which? Click the (Apple logo) at top left → **"About This Mac"** → Look for "Chip" or "Processor"
    - Wait for download (500-600 MB)
2. **Install Docker Desktop:**
    - Go to your **Downloads** folder
    - **Double-click** on `Docker.dmg`
    - **Drag** the Docker icon to the **Applications** folder
    - Wait for it to copy
    - **Eject** the Docker disk image (click the eject button next to it in Finder)
3. **Open Docker Desktop:**
    - Go to **Applications** folder
    - **Double-click** on **Docker**
    - Click **"Open"** if it asks about an app from the internet
    - Accept the service agreement
    - Enter your Mac password if asked
    - Click **"Skip"** if it asks you to sign in
    - Wait for Docker to start (you'll see "Docker Desktop is starting...")
4. **Configure Docker resources:**
    - In Docker Desktop, click the **⚙️ (Settings)** icon at the top
    - Click **"Resources"**
    - Set:
        - **CPUs:** 4 or more
        - **Memory:** 8 GB or more
    - Click **"Apply & Restart"**
    - Wait for Docker to restart
5. **Verify Docker is running:**
    - Look for the Docker icon in your menu bar (top right) - it should be a whale
    - If it's there, you're good! 



---

### **Step 2: Install Visual Studio Code** 

1. **Download VS Code:**
    - Go to: [https://code.visualstudio.com/](https://code.visualstudio.com/)
    - Click **"Download Mac Universal"**
    - Wait for download
2. **Install VS Code:**
    - Go to your **Downloads** folder
    - **Double-click** on `VSCode-darwin-universal.zip`
    - It will extract automatically
    - **Drag** "Visual Studio Code" to your **Applications** folder
3. **Open VS Code:**
    - Go to **Applications** folder
    - **Double-click** on **Visual Studio Code**
    - Click **"Open"** if it asks about an app from the internet



---

### **Step 3: Install Dev Containers Extension** 

1. **In VS Code:**
    - Look at the left sidebar
    - Click the icon that looks like 4 squares (Extensions)
    - In the search box at the top, type: `Dev Containers`
    - Find **"Dev Containers"** by Microsoft
    - Click the blue **"Install"** button
    - Wait for it to install



---

### **Step 4: Install Git** 
**Git is usually already installed on Mac. 

1. **Open Terminal:**
    - Press **Cmd + Space**
    - Type: `Terminal`
    - Press **Enter**
2. **Check if Git is installed:**
    - Type: `git --version`
    - Press **Enter**
3. **If you see a version number:**
    - You're done! Close Terminal 
4. **If it says "command not found" or prompts to install:**
    - Click **"Install"**
    - Follow the prompts
    - Wait for installation
    - Restart Terminal and verify: `git --version`



---

### **Step 5: Get the Workshop Files** 

**Choose Option A or Option B:**

#### **Option A: Clone from Git Repository**

1. **Open Terminal** (Cmd + Space, type "Terminal")
2. **Navigate to Documents:**

bash

```bash
   cd ~/Documents
```

- Press **Return**

3. **Clone the repository:**
    Repo Link:  [ros2_workshop](https://github.com/ishaankathiriya/ros2_workshop_devcontainer)
	 
	In the command prompt itself, enter the following command to clone the github repo:

```
git clone https://github.com/ishaankathiriya/ros2_workshop_devcontainer.git
```



**Alternate Option:**  Download the Zip file from the github repository by clicking on the 'Code' option and extract it to your desired location.


---

### **Step 6: Open in VS Code** 

1. **Open VS Code** (if not already open)
2. **Open the folder:**
    - Click **"File"** → **"Open Folder"** (or press Cmd + O)
    - Navigate to **Documents**
    - Click on `ws_ros2_workshop`
    - Click **"Open"**


---

### **Step 7: Build the Container** 


- Press **F1** (or Fn + F1)
- Type: `rebuild`
- Select **"Dev Containers: Rebuild and Reopen in Container"**

1. **Wait for build:**
    - Takes 15-25 minutes first time 
    - **Don't close VS Code!**
    - When done, bottom left will show: **"Dev Container: ROS2 Humble Desktop-Full"** in green
