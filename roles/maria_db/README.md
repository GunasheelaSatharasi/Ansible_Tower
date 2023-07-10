## Task for Installing and Configuring MariaDB

- This Ansible Role installs and configures MariaDB on Linux servers. It supports different distributions including Ubuntu, SUSE, and Red Hat.

The Role performs the following tasks:

1. Installs MariaDB packages based on the distribution:

   - For Ubuntu: `mariadb-server`
   - For SUSE: `mariadb`
   - For Red Hat: `mariadb-server`

2. Creates the MySQL data directory at `/var/lib/mysql` with the following properties:

   - Directory mode: `0755`
   - Owner: `root`
   - Group: `root`

3. Gives full permissions (`0777`) to the MySQL data directory recursively.

4. Copies the MariaDB installation script (`mysql_secure_installation.sh`) from the local system to the remote server at `/var/lib/mysql/mysql_secure_installation.sh` with the following properties:

   - File mode: `0755`

5. Starts the MariaDB service on the target server.

6. Runs the secure installation script (`mysql_secure_installation.sh`) with the specified MariaDB root password. The output of the script is captured in the `out` variable.

7. Displays the `stdout_lines` of the `out` variable using the `debug` module.