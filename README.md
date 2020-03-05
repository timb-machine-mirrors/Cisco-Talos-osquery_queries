# Cisco Talos Osqueries

**NOTE:** This repository is still under construction and as such, may not contain all files and packs listed.

### About this Repository

This repository contains Osquery packs used to query for malware family IoCs and other high-risk-of-infection indicators.

This project's goal is to provide consistently updated Osquery packs that reflect and monitor the current threat landscape.

### Repository Layout

All packs will reside under the <i>packs</i> folder. Each pack will be an appropriately named .conf file indicating its platform and type of queries contained.
In the parent folder, malware_information.json and high_risk_information.json contain metadata and other information regarding the queries in each file.

**Current packs available:**
  - win_malware.conf
  - osx_malware.conf
  - linux_malware.conf
  - win_high_risk_indicators.conf
  - osx_high_risk_indicators.conf
  - linux_high_risk_indicators.conf


### Using This Repository

It is recommended to run these queries/configurations in an isolated or lab environment before deploying.

**To install**
  - [Install OSQuery](https://osquery.readthedocs.io/en/latest/#getting-started)
  - Copy the packs into your platform's pack directory
    Default values
    - Windows: C:\ProgramData\osquery\packs
    - OSX: /var/osquery/packs
    - Linux: /etc/osquery/packs
  - Update the osquery.conf file to include the new packs
  - Start the osquery daemon

Each query defaults to being run every 24 hours. This value can be modified by changing the "interval" value under each query.