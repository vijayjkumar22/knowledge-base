---
title: Performance Troubleshooting
parent: Oracle
nav_order: 1
---

# Oracle Performance Troubleshooting

## Scenario
To change the database to noarchivelog mode

## Steps
srvctl status database -d ctrnb
srvctl status database -d ctrnb -v
srvctl stop database -d ctrnb
srvctl start database -d ctrnb -o mount
alter database noarchivelog;
archive log list;
alter database open;
select name,created,log_mode,checkpoint_change#,archive_change# from v$database;
<img width="1172" height="288" alt="image" src="https://github.com/user-attachments/assets/2f15f1b5-2969-4070-ab02-c10976f6acc6" />
