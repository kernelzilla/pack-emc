pack-emc
========

Shinken configuration pack for EMC² Clariion, VNX and VNX2 Block arrays.

This pack requires a version of Navisphere Secure CLI that matches the block
operating environment version of your array.

For RedHat Enterprise Linux, Oracle Linux and SuSE Enterprise Linux:

https://support.emc.com/downloads/5890_Navisphere-Agents-CLI---Linux

For Debian and Ubuntu Linux:
https://github.com/emc-openstack/naviseccli

You will need to change the credential variables in etc/resource.d/emc.cfg:

$NAVISECCLIUSER$=admin

$NAVISECCLIPASSWORD$=admin


This pack assumes the default NaviCLI install location of /opt/Navisphere.
If you have installed the package to a different directory change the following
variables in libexec/check_emc_clariion.pl:

$NAVICLI = '/opt/Navisphere/bin/navicli';

$NAVISECCLI = '/opt/Navisphere/bin/naviseccli';


Report any issues or feature requests via the GitHub Issues Tracker:

https://github.com/shinken-monitoring/pack-emc/issues
