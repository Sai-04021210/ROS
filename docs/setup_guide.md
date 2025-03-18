clearStep 1: Create a Dedicated ROS2 User on Ubuntu

To keep ROS2 development isolated, create a new user on Ubuntu:
sudo adduser ros2_user
sudo usermod -aG sudo ros2_user
Set a password when prompted.

Step 2: Access the Ubuntu Machine via SSH
From another system (e.g., your Mac), connect via SSH:
ssh ros2_user@<your-ubuntu-ip>
Replace <your-ubuntu-ip> with the actual IP address of your Ubuntu machine.

Step 3: Clone the GitHub Repository
Once inside ros2_user, navigate to your workspace and clone the project:
cd ~
git clone git@github.com:Sai-04021210/ROS2_Project.git
cd ROS2_Project

Step 4: Set Up SSH Authentication for Git
Generate an SSH key to avoid repeated login prompts:
ssh-keygen -t rsa -b 4096 -C "your-email@example.com"
cat ~/.ssh/id_rsa.pub

Add the key to GitHub → Settings → SSH and GPG Keys.
Test the SSH connection:
ssh -T git@github.com

Step 5: Create the Project Folder Structure
Inside ROS2_Project, create the required directories:
mkdir -p docs src/my_robot/{launch,urdf,scripts,config} simulation tests

Step 6: Track and Push the Folder Structure to GitHub
git add .
git commit -m "Initialized ROS2 project folder structure"
git push origin main
Verify the changes on GitHub → Repository.