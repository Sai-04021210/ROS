# ROS2 Project Setup Guide

## 📌 1. Connect to Ubuntu via SSH
```bash
ssh ros2_user@192.168.0.8 #replace the username and ip 
2. Create a New User for ROS2 (Optional)
sudo adduser ros2_user
sudo usermod -aG sudo ros2_user
 3. Set Up SSH Authentication
🔹 Generate SSH Key
ssh-keygen -t rsa -b 4096 -C "your-email@example.com"
🔹 Add Key to GitHub
Copy the key:
cat ~/.ssh/id_rsa.pub
Then add it to GitHub → Settings → SSH and GPG Keys.
4. Clone GitHub Repo
git clone git@github.com:Sai-04021210/ROS2_Project.git
cd ROS2_Project
Create Folder Structure
mkdir -p docs src/my_robot/{launch,urdf,scripts,config} simulation tests
6. Track Empty Folders
touch docs/.gitkeep
touch src/my_robot/config/.gitkeep
touch src/my_robot/launch/.gitkeep
touch src/my_robot/scripts/.gitkeep
touch src/my_robot/urdf/.gitkeep
touch tests/.gitkeep
7. Push Everything to GitHub
git add .
git commit -m "Initial project setup"
git push origin main
