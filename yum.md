# YUM COMMAND CHEAT SHEET for Red Hat Enterprise Linux  

### YUM QUERIES  

<table>
  <tr><th>GROUP</th><th>COMMAND</th><th>DESCRIPTIONS AND TASKS</th></tr>  
  <tr><th colspan = 3; align = "left"> help - Display yum commands and options</tr></tr>
  <tr><td></td><td><b>yum help</b></td><td>Show yum subcommands and options</td></tr>
  <tr><td colspan = 3>Individual packages</td></tr>
  <tr><th colspan = 3; align = "left"> list - List package names from repositories</tr></tr>
  <tr><td></td><td><b>yum list available</b></td><td>List all available packages</td></tr>
  <tr><td></td><td><b>yum list installed</b></td><td>List all installed packagess</td></tr>
  <tr><td></td><td><b>yum list all</b></td><td>List installed and available packages</td></tr>
  <tr><td></td><td><b>yum list kernel</b></td><td>List installed and available kernel packages</td></tr>
  <tr><th colspan = 3; align = "left"> info - Display information about a package</tr></tr>	
  <tr><td></td><td><b>yum info vsftpd</b></td><td>List info about vsftpd package</td></tr>
  <tr><th colspan = 3; align = "left"> deplist - Display dependencies for a package</tr></tr>	
  <tr><td></td><td><b>yum deplist nfs-utils</b></td><td>List dependencies and packages providing them</td></tr>
  <tr><th colspan = 3; align = "left"> provides - Find packages that provide the queried file</tr></tr>	
  <tr><td></td><td><b>yum provides "*bin/top"</b></td><td>Show package that contains top command</td></tr>
  <tr><td></td><td><b>yum provides "*/README.top"</b></td><td>Show package containing README.top file</td></tr>
  <tr><th colspan = 3; align = "left"> search - Search package names and descriptions for a term</tr></tr>	
  <tr><td></td><td><b>yum search samba</b></td><td>Find packages with samba in name or description</td></tr>
  <tr><th colspan = 3; align = "left"> updateinfo - Get information about available package updates</tr></tr>	
  <tr><td></td><td><b>yum updateinfo security</b></td><td>Get info on available security updates</td></tr>
  <tr><td colspan = 3>Groups of packages</td></tr>
  <tr><td></td><td><b>yum grouplist</b></td><td>List names of installed and available package groups</td></tr>	
  <tr><th colspan = 3; align = "left"> groupinfo - Display description and contents of a package group</tr></tr>	
  <tr><td></td><td><b>yum groupinfo "Web Server"</b></td><td>See packages in Web Server group</td></tr> 
  <tr><td></td><td><b>yum check-update</b></td><td>Query repositories for available package updates</td></tr>
</table>

### MANAGE YUM REPOSITORIES

<table>
  <tr><th>GROUP</th><th>COMMAND</th><th>DESCRIPTIONS AND TASKS</th></tr>  
  <tr><th colspan = 3; align = "left"> repolist - Display enabled software repositories</tr></tr>
  <tr><th colspan = 3; align = "left"> repoinfo - Display information about enabled yum repositories</tr></tr>
  <tr><td></td><td><b>yum repoinfo rhel-7-server-rpms</b></td><td>See info on rhel-7-server-rpms repo</td></tr>
	
  <tr><th colspan = 3; align = "left"> repo-pkgs - Work with packages in a particular repository</tr></tr>
  <tr><td></td><td><b>yum repo-pkgs my-rpms list</b></td><td>List packages from my-rpms repo</td></tr>
  <tr><td></td><td><b>yum repo-pkgs my-rpms install</b></td><td>Install all packages from my-rpms repo</td></tr>
  <tr><td></td><td><b>yum repo-pkgs my-rpms remove</b></td><td>Remove all packages from my-rpms repo</td></tr>
  <tr><th colspan = 3; align = "left"> makecache - Download yum repository data to cache</tr></tr>
</table>

  
  <tr><td></td><td><b>yum list kernel</b></td><td>List installed and available kernel packages</td></tr>
  <tr><th colspan = 3; align = "left"> info - Display information about a package</tr></tr>	
  <tr><td></td><td><b>yum info vsftpd</b></td><td>List info about vsftpd package</td></tr>
  <tr><th colspan = 3; align = "left"> deplist - Display dependencies for a package</tr></tr>	
  <tr><td></td><td><b>yum deplist nfs-utils</b></td><td>List dependencies and packages providing them</td></tr>
  <tr><th colspan = 3; align = "left"> provides - Find packages that provide the queried file</tr></tr>	
  <tr><td></td><td><b>yum provides "*bin/top"</b></td><td>Show package that contains top command</td></tr>
  <tr><td></td><td><b>yum provides "*/README.top"</b></td><td>Show package containing README.top file</td></tr>
  <tr><th colspan = 3; align = "left"> search - Search package names and descriptions for a term</tr></tr>	
  <tr><td></td><td><b>yum search samba</b></td><td>Find packages with samba in name or description</td></tr>
  <tr><th colspan = 3; align = "left"> updateinfo - Get information about available package updates</tr></tr>	
  <tr><td></td><td><b>yum updateinfo security</b></td><td>Get info on available security updates</td></tr>
  <tr><td colspan = 3>Groups of packages</td></tr>
  <tr><td></td><td><b>yum grouplist</b></td><td>List names of installed and available package groups</td></tr>	
  <tr><th colspan = 3; align = "left"> groupinfo - Display description and contents of a package group</tr></tr>	
  <tr><td></td><td><b>yum groupinfo "Web Server"</b></td><td>See packages in Web Server group</td></tr> 
  <tr><td></td><td><b>yum check-update</b></td><td>Query repositories for available package updates</td></tr>
 

 
  
 
  
 
TROUBLESHOOT AND MAINTAIN YUM
SUBCOMMAND	DESCRIPTIONS AND TASKS
 
check Check the local RPM database for problems (runs for a long time)
history	View and use yum transactions
yum history list  
List all yum install, update and erase actions
yum history info 3  
Show details of yum transaction 3
yum history undo 3  
Undo the yum action from transaction 3
yum history redo 3 
Redo the undone yum action from transaction 3
clean Clear out cached package data
yum clean packages 
Delete packages saved in cache
yum clean all 
Clean out all packages and meta data from cache
fssnapshot	List LVM stapshots (helps roll back after package updates)
fs Act on filesystem (prevent doc or language file install on minimal systems)
yum fs filters 
List enabled filesystem filters
yum fs documentation 
Filters all docs from being installed (careful!)
INSTALL, REMOVE AND UPGRADE PACKAGES WITH YUM
SUBCOMMAND	DESCRIPTIONS AND TASKS
 
install Install a package from a repository to your system
yum install vsftpd 
Install the vsftpd package
update	Update one or all packages on your system
yum update 
Update all packages with available updates
yum update httpd 
Update the httpd package (if available)
yum update --security 
Apply security-related package updates
update-to Update one or all packages to a particular version
upgrade	Update packages taking obsoletes into account
localinstall	Install a package from a local file, http, or ftp
yum localinstall abc-1-1.i686.rpm Install abc package from local directory
yum localinstall http://myrepo/abc-1-1.i686.rpm Install abc from FTP site
downgrade	Downgrade a package to an earlier version
yum downgrade abc 
Downgrade the abc package to an earlier version
reinstall	Reinstall the current version of a package
yum reinstall util-linux 
Reinstall util-linux (to replace any deleted files)
swap	Remove one package and install another
yum swap ftp lftp 
Remove ftp package and install lftp package
erase	Erase a package (and possibly dependencies) from your system
yum remove vsftpd 
Remove the vsftpd package and dependencies
remove	Same as erase
autoremove 	Same as erase, plus removes additional unneeded packages *
yum autoremove httpd 
Remove httpd and other unneeded packages
groupinstall 	Install all packages in the selected group
yum groupinstall “Web server” Install Web Server packages
MANAGE LANGUAGE PACKAGES WITH YUM		MORE YUM-RELATED COMMANDS (install the yum-utils package)
	SUBCOMMAND	DESCRIPTIONS AND TASKS
langavailable List all available languages *
langinfo List packages available for a language *
yum langinfo es 
List packages associated with Spanish language
langinstall Install packages associated with a particular 
language *
yum langinstall es 
Install packages associated with Spanish language
langlist List languages that are installed *
langremove Remove installed language packs for a language *
yum langremove es 
Remove packages associated with Spanish language
POPULAR OPTIONS FOR DIFFERENT YUM COMMANDS **
OPTION	DESCRIPTION
-y	Assume yes if prompted
--assumeno 	Assume no if prompted
-q 	Produce no output
-v 	Produce extra debugging output
--noplugins 	Run command without loading any yum plugins
--disableplugin= Disable a particular plugin for single command
yum --disableplugin=langpacks info vsftpd
--enableplugin= Enable a plugin that is installed, but currently disabled
yum --enableplugin=ps ps 
Show packages tied to running processes
--enablerepo= Enable currently disabled repo for a single command (wildcards okay) yum install docker \
  --enablerepo=rhel-7-server-extras-rpm
--disablerepo= Disable currently enabled repo for a single command (wildcards okay)
yum list available --disablerepo=epel
--downloadonly Download to /var/cache/yum/arch/prod/repo/ packages/, but don’t install
yum install --downloadonly vsftpd Download vsftpd package to cache
--filter-???= Replace ??? with vendors, rpm-groups, arches, and others to filter output
--changelog Display changelog information of package
12/14
	COMMAND	DESCRIPTION
 
find-repos-of-install Find which repository a package comes from
needs-restarting	Find processes that have been updated and need to restart
repoclosure Get unmet dependency list from repositories
repoquery	Query remote repos and local RPM database
repoquery --requires --resolve bash 
Show dependent packages
reposync Synchronize yum repositories to a local directory
reposync -r rhel-atomic-host-beta-rpms Get packages from repo
repotrack	Download a package and all its dependencies
show-installed	List installed RPM packages and statistics
verifytree	Check the local yum repository for consistency
yum-complete-transaction	Try to complete yum transactions that didn’t finish
yumdb	Check or change the yum database
yumdownloader Download  a package from a repo to current directory
 
Type man yum for futher details on all yum subcommands and options
* 	New options for RHEL 7
** Some options need yum plugins. Type yum list “yum-plugin*” to see available plugins.

</table>
