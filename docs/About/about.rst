About
=====


CLI vs. Portal
--------------

A common question is why use PowerZure or command line at all when you
can just login to the Azure web portal?

This is a fair question and to be honest, you can accomplish 90% of the
functionality in PowerZure through clicking around in the portal,
however by using the Azure PowerShell modules, you can perform tasks
programmatically that are tedious in the portal. E.g, listing the groups
a user belongs to. In addition, the ability to programmatically upload
exploits instead of tinkering around with the messy web UI. Finally, if
you compromise a user who has used the PowerShell module for Azure
before and are able to steal the accesstoken.json file, you can
impersonate that user which effectively bypasses multi-factor
authentication.

Why PowerShell?
---------------

While the offensive security industry has seen a decline in PowerShell
usage due to the advancements of defensive products and solutions, this
project does not contain any malicious code. PowerZure does not exploit
bugs within Azure, it exploits misconfigurations.

C# was also explored for creating this project but there were two main
problems:

1. There were at least four different APIs being used for the project.
   MSOL, Azure REST, Azure SDK, and Graph.

2. The documentation for these APIs simply was too poor to continue.
   Entire methods missing, namespaces typo’d, and other problems begged
   the question of what advantage did C# give over PowerShell (Answer:
   none)

Realistically, there is zero reason to ever run PowerZure on a victim’s
machine. Authentication is done by using an existing accesstoken.json
file or by logging in via prompt when logging into Azure CLI.

Author & License
----------------

Author: Ryan Hausknecht (@haus3c)

License: BSD-3