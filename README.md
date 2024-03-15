#Learning Docker
 - Delve into docker images and containers using multiple languages.
 - Setting up prerequisites for Windows 10
    - Ensure that your system has WSL 2 or a higher version.
    - Verify that Virtualization Technology (VTx) is enabled on your PC or laptop. To check if it's enabled, open your PC's Task Manager, navigate to the Performance tab, and check under the CPU section for virtualization.
    - If VTx is not enabled, restart your computer and immediately press F10 to enter BIOS. Navigate to the Security tab, select USB Security, and press Enter. Choose Virtualization Technology (VTx), and toggle between Enabled or Disabled using the left and right arrows.
 - Once the above setup is completed, you can proceed to download and install Docker.

# Create Docker file in docker
  - To create this you can use commant in you project directory - touch dockerfile or you can simply create the file with name dockerfile in the project directory. Please take a note here this file doesn't have any extention.
  - After creation of this file if you are using IDE visual code it provide suggestion to install docker extention so it will help you write docker file so its on up to you if you need you can install it.
  - After creation of dockerfile you need to write the required commands in the the to create your project image
    - FROM php:8.3 or latest -> here you need to tell to docker what is the base image for this docker image
    - COPY source destination -> in copy command you need to tell where is you project and in which folder structure want to create if it execute
    - RUN composer install -> If you project need any external package or library from composer
    - EXPOSE port -> on which port you want to run you project
    - CMD ["command if any"] 
    - WORKDIR /the/workdir/path -> if you want you image execute in the subdirectory not root
  - After write image in dockerfile run the command `docker build -t image-name destination`
    - `-t -> tag for the image`
    - `image-ange -> anything you want`
    - `destination -> where you want create the docker image`