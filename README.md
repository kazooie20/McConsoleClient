# McConsoleClient
# Ensure everything is the same as what is written here for your MinecraftClient.ini file. Sometimes you get this error message #'Disconnected from server. Connection Timeout: Null'. Unfortunately this is an issue faced by many and has not been fixed even by the #developer of this console client. Thus it requires manual intervention of typing /reco. What /reco does is essentially restarts the # #minecraft session.

# The Parts that require to change is the AntiAFK Section and AutoRelog. The rest leave it as it is.

# Minecraft Console Client v1.14.4
# Startup Config File

[Main]

# General settings
# Leave blank to prompt user on startup
# Use "-" as password for offline mode

login=
password=
serverip=aztec.manacube.net

# Advanced settings

language=en_GB
consoletitle=%username%@%serverip% - Minecraft Console Client
internalcmdchar=slash              # Use 'none', 'slash' or 'backslash'
splitmessagedelay=2                # Seconds between each part of a long message
botowners=Player1,Player2,Player3  # Use name list or myfile.txt with one name per line
botmessagedelay=2                  # Seconds to delay between message a bot makes to avoid accidental spam
mcversion=1.12.2                     # Use 'auto' or '1.X.X' values
brandinfo=mcc                      # Use 'mcc','vanilla', or 'none'
chatbotlogfile=                    # Leave empty for no logfile
privatemsgscmdname=tell            # Used by RemoteControl bot
showsystemmessages=true            # System messages for server ops
showxpbarmessages=true             # Messages displayed above xp bar
showchatlinks=true                 # Show links embedded in chat messages
terrainandmovements=false          # Uses more ram, cpu, bandwidth
inventoryhandling=false            # Toggle inventory handling
sessioncache=disk                  # How to retain session tokens. Use 'none', 'memory' or 'disk'
resolvesrvrecords=fast             # Use 'false', 'fast' (5s timeout), or 'true'. Required for joining some servers.
accountlist=accounts.txt           # See README > 'Servers and Accounts file' for more info about this file
serverlist=servers.txt             # See README > 'Servers and Accounts file' for more info about this file
playerheadicon=true                # Only works on Windows XP-8 or Windows 10 with old console
exitonfailure=false                # Disable pauses on error, for using MCC in non-interactive scripts
debugmessages=false                # Please enable this before submitting bug reports. Thanks!
scriptcache=true                   # Cache compiled scripts for faster load on low-end devices
timestamps=false                   # Prepend timestamps to chat messages

[AppVars]
# yourvar=yourvalue
# can be used in some other fields as %yourvar%
# %username% and %serverip% are reserved variables.

[Proxy]
enabled=false                      # Use 'false', 'true', or 'login' for login only
type=HTTP                          # Supported types: HTTP, SOCKS4, SOCKS4a, SOCKS5
server=0.0.0.0:0000                # Proxy server must allow HTTPS for login, and non-443 ports for playing
username=                          # Only required for password-protected proxies
password=                          # Only required for password-protected proxies

[ChatFormat]
# Do not forget to uncomment (remove '#') these settings if modifying them
builtins=true                      # MCC built-in support for common message formats
# public=^<([a-zA-Z0-9_]+)> (.+)$
# private=^([a-zA-Z0-9_]+) whispers to you: (.+)$
# tprequest=^([a-zA-Z0-9_]+) has requested (?:to|that you) teleport to (?:you|them)\.$

[MCSettings]
enabled=true                       # If disabled, settings below are not sent to the server
locale=en_US                       # Use any language implemented in Minecraft
renderdistance=medium              # Use tiny, short, medium, far, or chunk amount [0 - 255]
difficulty=normal                  # MC 1.7- difficulty. peaceful, easy, normal, difficult
chatmode=enabled                   # Use 'enabled', 'commands', or 'disabled'. Allows to mute yourself...
chatcolors=true                    # Allows disabling chat colors server-side
main_hand=left                     # MC 1.9+ main hand. left or right
skin_cape=true
skin_hat=true
skin_jacket=false
skin_sleeve_left=false
skin_sleeve_right=false
skin_pants_left=false
skin_pants_right=false
# Bot Settings

[Alerts]
enabled=false
alertsfile=alerts.txt
excludesfile=alerts-exclude.txt
beeponalert=true

[AntiAFK]
enabled=true
delay= 1800 #10 = 1s     #<--- Set Delay to 1800
command=/server aztec    #<---- Set Command = /server aztec Sends /aztec every 3 mins so if u r at hub it will relog u back to aztec 

[AutoRelog]
enabled=true                        #<---- AutoRelog set to true
delay=10
retries=-1 #-1 = unlimited
kickmessagesfile=kickmessages.txt

[ChatLog]
enabled=false
timestamps=true
filter=messages
logfile=chatlog-%username%-%serverip%.txt

[Hangman]
enabled=false
english=true
wordsfile=hangman-en.txt
fichiermots=hangman-fr.txt

[ScriptScheduler]
enabled=false
tasksfile=tasks.ini

[RemoteControl]
enabled=false
autotpaccept=true
tpaccepteveryone=false

[AutoRespond]
enabled=false
matchesfile=matches.ini
