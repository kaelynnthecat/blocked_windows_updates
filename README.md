# blocked_windows_updates
How to block Windows Updates (AU/AutoWindowsUpdate)

HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\WindowsUpdate\AU

NoAutoUpdate (REG_DWORD):

    0: Automatic Updates is enabled (default).

    1: Automatic Updates is disabled.

AUOptions (REG_DWORD):

    1: Keep my computer up to date is disabled in Automatic Updates.

    2: Notify of download and installation.

    3: Automatically download and notify of installation.

    4: Automatically download and scheduled installation.

    5: Allow local admin to select the configuration mode. This option isn't available for Windows 10 or later versions.

    7: Notify for install and notify for restart. (Windows Server 2016 and later only)

ScheduledInstallEveryWeek (REG_DWORD):

    0: Do not enforce a once-per-week scheduled installation

    1: Enforce automatic installations once a week on the specified day and time. (Requires ScheduledInstallDay and ScheduledInstallTime to be set.)

ScheduledInstallDay (REG_DWORD):

    0: Every day.

    1 through 7: The days of the week from Sunday (1) to Saturday (7).

ScheduledInstallTime (REG_DWORD):

    n, where n equals the time of day in a 24-hour format (0-23).

UseWUServer (REG_DWORD):

    Set this value to 1 to configure Automatic Updates to use a server that is running Software Update Services instead of Windows Update.

RescheduleWaitTime (REG_DWORD):

    m, where m equals the time period to wait between the time Automatic Updates starts and the time that it begins installations where the scheduled times have passed. The time is set in minutes from 1 to 60, representing 1 minute to 60 minutes)

    This setting only affects client behavior after the clients have updated to the SUS SP1 client version or later versions.

NoAutoRebootWithLoggedOnUsers (REG_DWORD):
