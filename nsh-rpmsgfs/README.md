
Previously we can mount rpmsgfs and launch NSH from it upon remote node booting
time. However it breaks recently.  Here are some logs and related nuttx ELF.

The logs are collected with INFO level for MM, FS, SCHED etc

- `rptun` set shows AppBringUp crashed in `rptun_init`.
- `nsh`set shows AppBringUp crashed in creating nsh process.

All crashes happened due to heap corruption, though different log options lead to different crash point.
