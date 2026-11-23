-- ============================================================
-- Week 8 Assignment: MySQL Database Backup and Restore
-- ============================================================

-- ------------------------------------------------------------
-- Question 1: Creating a Complete Database Backup
-- ------------------------------------------------------------

-- Command (run in system terminal / Git Bash):
-- mysqldump -u root -p sales > sales_backup.sql

-- Explanation:
-- 1. What the command does:
--    - `mysqldump`: Invokes MySQL's command-line backup utility.
--    - `-u root`: Specifies 'root' as the MySQL user account.
--    - `-p`: Prompts the user to enter the database password securely.
--    - `sales`: Targets the specific 'sales' database to export both its
--      table structures (DDL) and all table records (DML).
--    - `> sales_backup.sql`: Redirects the output into a file named
--      'sales_backup.sql' in the current directory.
--
-- 2. Why regular database backups are important:
--    - Protects against accidental data deletion, human error, or bad queries.
--    - Enables fast recovery after hardware failures, software bugs, or
--      cyberattacks (such as ransomware).
--    - Provides a safe rollback point before performing major schema changes
--      or system upgrades.


-- ------------------------------------------------------------
-- Question 2: Backing Up All Databases
-- ------------------------------------------------------------

-- Command (run in system terminal / Git Bash):
-- mysqldump -u root -p --all-databases > all_databases_backup.sql

-- Explanation:
-- 1. What the command does:
--    - `--all-databases` (or `-A`): Exports every database hosted on the
--      MySQL server, including 'sales' and system databases (such as 'mysql'),
--      along with CREATE DATABASE statements so they can be restored cleanly.
--    - `> all_databases_backup.sql`: Saves the full server dump into a single
--      file named 'all_databases_backup.sql'.
--
-- 2. Why backing up all databases is important before a server migration:
--    - Prevents data loss if network interruptions, hardware failures, or
--      configuration errors occur during the move.
--    - Preserves all user accounts, privileges, stored routines, and multiple
--      application databases in one consistent snapshot.
--    - Allows you to quickly restore the entire environment on the original
--      server if the migration fails.
# answers.sql8
