<div align="center">
  <h1>PHANTOMPHP</h1>
  <img src="https://img.shields.io/badge/version-1.0-blue" alt="Version">
  <img src="https://img.shields.io/badge/license-MIT-green" alt="License">
</div>




---

## Table of Contents
- [Overview](#overview)
- [Key Features](#key-features)
- [Installing PhantomPHP](#installing-phantomphp)
  - [Installation Requirements](#installation-requirements)
  - [Installation Steps](#installation-steps)
- [Usage](#usage)
  - [Serving](#serving)
  - [Port Selection](#port-selection)
  - [Port Forwarding](#port-forwarding)
  - [Direct File Running in PHP](#direct-file-running-in-php)
  - [Further Help](#further-help)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

**PhantomPHP** is a PHP web server designed for use with the Termux terminal, enabling you to run and share PHP and MySQL applications directly from your mobile device. It’s built to provide fast performance, high reliability, and seamless integration with MySQL databases, offering a powerful solution for dynamic web development on the go.
## Key Features

- **PHP Serving**: Run PHP files directly from Acode.
- **Port Forwarding**: Share your local server with others securely.
- **Direct PHP File Execution**: Execute files without additional configuration.
- **Seamless Fast Auto Installation Integration**: Quick automatic setup, you don't have to do much.
- **MySQLi and phpMyAdmin Support**: Manage databases with ease.
- **Custom Port Selection**: Choose your preferred port.
- **User-Friendly Interface**: Optimized for ease of use.

---

## Installing PhantomPHP

To install PhantomPHP on your Android device, you’ll need the following prerequisites:

### Installation Requirements

1. **Termux**:  
   A powerful Linux terminal emulator for Android, available on [F-Droid](https://f-droid.org) and [GitHub](https://github.com/termux/termux-app/releases).  
   This will allow you to run a Linux environment on your Android device.


2. **PHP (version 7.4 or above)**:  
   Installable via Termux.  
   PHP is required for running server-side scripts and applications.

3. **Composer**:  
   A PHP package manager used for handling dependencies and libraries in PHP projects.  
   You can install Composer in Termux to manage PHP packages.

4. **MariaDB**:  
   A popular open-source database management system, forked from MySQL.  
   Required for managing databases in your projects.

5. **phpMyAdmin**:  
   A web-based tool for managing MySQL and MariaDB databases.  
   It provides an easy-to-use interface for database administration.

### Installation Steps

1. **Install Termux**:
   - Download and install Termux from [F-Droid](https://f-droid.org) or the [Termux GitHub releases page](https://github.com/termux/termux-app/releases).

## Clone Repository

2. Open Termux and run the following commands to clone the PhantomPHP repository, set the appropriate permissions, and run the installation script:

    ```bash
    git clone https://github.com/codetesla51/phantomphp.git
    cd phantomphp
    chmod +x install
    ./install
    ```
   This will clone the PhantomPHP repository, navigate into the project directory, set execute permissions for the installation script, and run it to complete the setup.


## Verify installation

4. After running the previous step to clone and install PhantomPHP, verify the installation by running the following command:

    ```bash
    phantom -v
    ```

## Access phpMyAdmin

5. Use the `phantom` command to start the PHP server for phpMyAdmin access. Replace `<port>` with the desired port number (e.g., 8080):

    ```bash
    phantom --db <port>
    ```

   Once started, you can access phpMyAdmin in your browser by navigating to:

    ```
    http://localhost:<port>
    ```

   **Default Credentials**:  
   - **Username**: `root`  
   - **Password**: `root`


Now, you should be able to access phpMyAdmin through your browser by navigating to `http://localhost:<port>`.
 
---
### Usage
**Basic Usage Outline for PhantomPHP Server**

### Serving
This is the basic way to serve your PHP project. It will run a local server with the default port 8000.

**example:**
```bash
cd /path/to/your-project-directory
phantom --serve
```
---
### Port Selection
In case the default port 8000 is already in use, you can change the port by using the -p option followed by your desired port number (e.g., 8080).

**example**
```bash
phantom --serve 8080
```
#### This will run the local server on the selected port.
---
### phpMyAdmin Initialization

To start both MySQL and phpMyAdmin for database interaction, you can specify a
custom port with the `--db` flag. In this example, we use port 8880. If the port
is already in use, the server will not run.

**Example**:

```bash
phantom --db 8880
```
This will start the MySQL server and phpMyAdmin on port 8880. If the port is already in use, the server will not run.

You can access phpMyAdmin in your browser by navigating to:
```
http://localhost:8880
```
Default Credentials:
   -  Username: root
   - Password: root
---
### Port Forwarding

Want to share your work with your team or friends? PhantomPHP allows you to forward your local server port and share it with others, including SSL certification for a secure connection. Use the `-f` flag to enable port forwarding.

**Example**:

```bash
phantom -serve 8080
```
This will run the local server on port 8080. After serving, the server will read options. Press F (or f) to enable port forwarding and allow others to access your server.
This will forward the port for others to access your application securely.
### Direct File Running in PHP

To quickly run your PHP file and get immediate output, you can use the following command without needing to add the `.php` extension. Simply provide the filename.

**Usage Example:**
```bash
phantom -run filename
```
#### For instance:
```bash
phantom --run init
```
#### This will run the init.php file.
---
### Need Further Help?

If you're still having trouble, you can contact the repository owner or contributors for assistance. You can also email your issue to:

**Email:** uoladele99@gmail.com, 

For additional command options, you can view the help menu with:
```bash
phantom --help
```
---
## Contributing

We welcome contributions! If you'd like to improve or fix something, please open an issue to start a discussion. Once your idea is approved, feel free to submit a pull request.

## License

<h4>This project is licensed under the **MIT License**, which allows you to
freely use, modify, and distribute the code. See the `LICENSE` file for full
details.</h4>

---
## Leave a Star ⭐

If you find **PhantomPHP Server** useful, please consider leaving a star on the repository! Your support helps others discover the project and motivates us to keep improving it.
