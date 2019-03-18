# Eclipse IDE

Eclipse is a Java-based IDE.

## Installing

Get the "Eclipse IDE YYYY-MM" from https://www.eclipse.org/downloads/ or
"Eclipse Installer" from  http://eclipse.bluemix.net/packages/


Unpack the installer in $HOME/eclipse/eclipse-installer

  echo 'exec ~/eclipse/eclipse-installer/eclipse-inst $\*' > ~/bin/eclipse-inst
  chmod 755 ~/bin/eclipse-inst

Start eclipse-inst

Hamburger Menu, Enable Bundle Pools, Enable Advanced Mode

Select the IDE you want from Eclipse.org
Select a bundle pool on $HOME/.p2/pool (saves a LOT of space if you have multiple installations)


  echo 'exec ~/eclipse/latest/eclipse/eclipse $\*' > ~/bin/eclipse
  chmod 755 ~/bin/eclipse



## Updating

Make sure that you have (at least) these five repositories.

http://download.eclipse.org/releases/2019-03

http://download.eclipse.org/releases/latest

http://download.eclipse.org/oomph/updates/milestone/latest

http://download.eclipse.org/eclipse/updates/4.11

http://download.eclipse.org/technology/epp/packages/2019-03/

## Cleanup

Release old

 Help -> About Eclipse IDE
   See Version
   Installation Details -> Installation History
     Select previous configurations -> Delete

Remove resources that aren't in use anymore

Window -> Preferences -> Oomph -> Bundle Pools
select the bundle pool you want to Cleanup
Analyze Agent...

If any damaged artifacts, Repair Damaged artifacts

If any unused artifacts, Delete Unused artifacts

Exit Eclipse

If you have an SSD, you should TRIM now.

Linux: fstrim -av
