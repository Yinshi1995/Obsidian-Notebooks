#### Checking for Updates

- **Check for Updates:**
    
    sqlCopy code
    
    `/system package update check-for-updates`
    
    This command checks for available updates.
    
- **List Available Updates:**
    
    perlCopy code
    
    `/system package update list`
    
    Display a list of available updates.
    

#### Installing Updates

- **Install All Updates:**
    
    perlCopy code
    
    `/system package update install`
    
    Install all available updates.
    
- **Install Specific Package Update:**
    
    perlCopy code
    
    `/system package update install [package-name]`
    
    Install a specific package update.
    

#### Firmware Upgrade

- **Check for Firmware Upgrade:**
    
    bashCopy code
    
    `/system routerboard print`
    
    Verify the current firmware version.
    
- **Upgrade Firmware:**
    
    bashCopy code
    
    `/system routerboard upgrade`
    
    Upgrade the RouterBOARD firmware.
    

#### Scheduled Updates

- **Schedule Automatic Updates:**
    
    csharpCopy code
    
    `/system scheduler add interval=1d on-event="/system package update install"`
    
    Schedule daily automatic updates.

#### Backup Configuration

- **Backup Configuration:**
    
    arduinoCopy code
    
    `/export file=config-backup`
    
    Create a backup of the current configuration.
    
- **Import Configuration:**
    
    arduinoCopy code
    
    `/import file=config-backup`
    
    Restore the configuration after updates.
    

#### Note

- Always check the MikroTik website for the latest stable releases.
- Ensure that RouterOS updates are compatible with your current configuration.
- Schedule updates during maintenance windows to minimize network disruptions.
- Regularly backup configurations before performing updates.

#### Caution

- Carefully review release notes for each update to understand changes and potential impact.
- Consider testing updates in a controlled environment before applying to production.
- Be cautious with major version updates, as they may introduce significant changes.
- Verify that installed packages are compatible with the updated RouterOS version.