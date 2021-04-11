# Installing-NGINX-on-Ubuntu-20.04

## What is Nginx?

Nginx is a Fast, Open Source, a high-performance web server that commands a huge market share in production environments. Nginx is one of the most popular web servers in the world and hosts some of the largest and highest-traffic sites on the internet. Nginx provides a content management cache, and a reverse proxy feature for HTTP and non-HTTP servers.

In this we will show you how to install, Services Manage, and Adjust Firewall.

### 1. Prerequisites

   * The operating system running Ubuntu 20.04 Linux
   * A root or non-root user with sudo privileges
   * A stable internet connection
   * Make sure Apache or any other processes are not running on port 80 or 443
   * Terminal window / Command line

### 2. Update Software Repositories

Updating the local package with apt command. Open a terminal window and run the following command:

    sudo apt update


Upgrading the local package with apt command. Open a terminal window and run the following command:

    sudo apt upgrade


### 3. Installing Nginx

Nginx is available in the Ubuntu 20.04 default repositories. Run the following command and install Nginx:

    sudo apt install nginx


### 4. Verify Installation

When Nginx installed correctly, checking by the software version.

    nginx -v


### 5. Managing the Nginx Process

Now that you have your web server up and running, let's go over basic management commands.

To stop your web server, run this command:

    sudo systemctl stop nginx 

To start your web server, run this command:

    sudo systemctl start nginx

To reload your web server, run this command:

    sudo systemctl reload nginx

To disable your web server, run this command:

    sudo systemctl disable nginx

To enable your web server, run this command:

    sudo systemctl enable nginx

To status your web server, run this command:

    sudo systemctl status nginx

### 6. Nginx Adjusting Firewall

Check the available ufw application profiles:

    sudo ufw app list

Let’s enable the most restrictive profile that will still allow the traffic you’ve configured, permitting traffic on port 80:

    sudo ufw allow 'Nginx Full'

Verify the change:

    sudo ufw status

If you have other applications or services to allow, make sure you configure your firewall to allow traffic.

For example, using the sudo ufw allow 'OpenSSH' the command will enable secure, encrypted logins over the network.

### 7. Test

For Verify it installed correctly Nginx, open a web browser and type in the address bar http://server_ip_address

After opening this URL, you can see the Nginx default page as in the image below:
