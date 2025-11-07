
# Personal Fail2Ban Configuration

This repository contains a personalised configuration for [Fail2Ban](https://github.com/fail2ban/fail2ban), including custom jails and filters.

## Overview

This setup is tailored for personal server use. It includes a `jail.local` file to define ban policies and a `filter.d` directory for custom log-parsing filters.

## Contents

-   **`jail.local`**: This file overrides the default `jail.conf` settings. It defines which services to monitor (e.g., `sshd`, `nginx-http-auth`), the conditions for banning (e.g., `maxretry`, `findtime`), and the ban duration (`bantime`).
    
-   **`filter.d/`**: This directory contains custom filter definitions. Filters are regex patterns that Fail2Ban uses to identify failed login attempts or other malicious activity in log files.

## Custom Jails/Filters
### apache-too-many-404s
Search Apache access logs for requests resulting in 404s and ban if too frequent.
