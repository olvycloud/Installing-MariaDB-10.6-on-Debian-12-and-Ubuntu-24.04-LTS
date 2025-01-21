# Installing MariaDB 10.6 on Debian 12 and Ubuntu 24.04 LTS

This guide provides step-by-step instructions to install MariaDB 10.6 on Debian 12 and Ubuntu 24.04 LTS systems using the Olvy repository.

> **Note:** MariaDB 10.6 is an officially supported long-term release (LTS).  
> This guide ensures compatibility for systems running Debian 12 and Ubuntu 24.04 LTS.  
> For detailed insights, visit the original guide at [Olvy.net](https://olvy.net/blog/how-to-install-mariadb106-on-debian12-and-ubuntu2404/).

## Prerequisites

- **Operating Systems Supported:**
  - Debian 12 "Bookworm"
  - Ubuntu 24.04 LTS "Noble Numbat"

- **Architectures Supported:**
  - x86-64

## Installation Steps

### 1. Add Olvy Repository

Edit the `sources.list` file to include the Olvy repository:

```bash
sudo nano /etc/apt/sources.list
```

Add the appropriate repository line based on your operating system:

- Debian 12 "Bookworm":
  ```
  deb [trusted=yes] https://repo.olvycloud.com/mariadb/10.6/bookworm /
  ```
- Ubuntu 24.04 LTS "Noble Numbat":
  ```
  deb [trusted=yes] https://repo.olvycloud.com/mariadb/10.6/noble /
  ```
Save and exit the editor.

### 2. Update Package Indexes
Refresh the package lists to include the new repository:
  ```bash
  sudo apt update
  ```

### 3. Install MariaDB 10.6
Proceed to install the MariaDB server and client:
  ```bash
  sudo apt install mariadb-server-10.6 mariadb-client-10.6
  ```

## Post-Installation
After installation, verify the MariaDB service status:
  ```bash
  sudo systemctl status mariadb
  ```
Secure your MariaDB installation by running:
```bash
sudo mysql_secure_installation
```

## Important Notes

- *Enhanced Features in MariaDB 10.6:*
MariaDB 10.6 introduces improvements such as an improved InnoDB storage engine, native JSON support, and enhanced replication capabilities.

- *Security Notice:*
While Olvy provides secure and up-to-date repositories, always monitor and apply future MariaDB patches to ensure system security.

- *Migration Assistance:*
If upgrading from an earlier MariaDB version, carefully review the changes in MariaDB 10.6 to ensure compatibility with your applications.

## About Olvy

Olvy is a private and independent Limited Liability Company based in Bratislava, Slovakia, offering innovative and reliable Managed Cloud Hosting services. For more information, visit [Olvy's website](https://olvy.net/).
