# Development Environment for Advanced RTOS class at UNC Charlotte.

The build containes an x86 emulator, QEMU, for running a kernel; and a compiler toolchain, including assembler, linker, C compiler, and debugger, for compiling and testing the kernel. 

Steps:
1. Pull the latest image to your machine. 

	``` docker pull dineshauti/rtos ```

2. Map a folder named rtoslabs on your Desktop inside the container. This is where all your labs will reside. So any changes that you make inside this folder will be dynamically reflected inside the container and vise-versa. The container will start and run in the background. Replace the path in double quotes to the path of the folder that you want to map. If you are windows, I have assumed that there is a folder named rtoslabs on the Desktop. Make sure to replace $user with your user name.

	``` docker run -it -d -v "c:/Users/$user/Desktop/rtoslabs":/root/rtoslabs -w /root/rtoslabs --name rtos dineshauti/rtos:dev bash ```

3. Spwan a new bash process inside the already running container and connect to it. You can execute commands in the bash. Type 'exit' to exit the bash process inside the container. Note that the container is still running in the background.

	``` docker exec -it rtos bash ```