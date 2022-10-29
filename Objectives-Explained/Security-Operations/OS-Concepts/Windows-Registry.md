# Windows Registry

## Explanation

The Windows Registry is a database of settings, information, configurations, and options for the Windows operating system, some applications also use the registry.  The registry is made up of keys and values, keys are like directories and values are like files (but not exactly).

- Hives = main branches of the registry; 5 most common are as follows:
    1. HKEY_CLASSES_ROOT (HKCR) = default file associations; which app opens/reads what file type
    2. HKEY_CURRENT_USER (HKCU) = user-specific settings
    3. HKEY_LOCAL_MACHINE (HKLM) = passwords, boot files, software installations, security settings; most critical
    4. HKEY_USERS (HKU)= similar to current_user hive, but for accomodating multiple users at once
    5. HKEY_CURRENT_CONFIG (HKCC) = real-time hardware monitoring; key values aren't saved permanently in this hive

The registry was created to replace and centralize the contents of individual config files.  These configurations were usually in .ini files, which are still used, but less heavily.

## Importance

Every setting on your system needs to be tracked and stored with persistence, the registry is how Windows accomplishes that.  The registry can be edited to help improve performance or remove unwanted programs.

## Demonstration

To access the registry, click the Windows menu icon in the bottom left of your screen (*Win Key*), type *regedit* and *Enter*, allow regedit to make changes.  The regedit application should open on your device if you have admin privileges.  Regedit is used to make changes to the registry; feel free to look through the branches, but don't change anything unless you know what you're doing and have made a backup of your registry.

To back up your registry, simply open regedit, select File from the menu at the top of the window, click export, and provide a name and save location.

## Additional Resources

- [Computer Hope](https://www.computerhope.com/jargon/r/registry.htm)
- [Avast](https://www.avast.com/c-windows-registry)
- [Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-server/performance/windows-registry-advanced-users)
