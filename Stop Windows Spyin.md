Execute the 2 script down below With CMD as administrator 

sc config DiagTrack start= disabled

sc config dmwappushservice start= disabled
# Disable DiagTrack service
Set-Service -Name DiagTrack -StartupType Disabled
Stop-Service -Name DiagTrack -Force

# Disable dmwappushservice service
Set-Service -Name dmwappushservice -StartupType Disabled
Stop-Service -Name dmwappushservice -Force
