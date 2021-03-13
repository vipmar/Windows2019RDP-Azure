

Real Author: NT. Hải

Modified by https://t.me/mmahim

code:

```

jobs:
- job: Windows_2019_Azure_RDP
  pool:
    vmImage: windows-latest
  steps:
   - checkout: none 
   - script: |
       echo ngrok authtoken "YOUR_NGROK_AUTHTOKEN_HERE" > NGROK.bat
       curl -s -O https://raw.githubusercontent.com/docefio/Windows2019RDP-Azure/main/AzureNgrokAutoRegion.bat
       AzureNgrokAutoRegion.bat
     displayName: 'Run RDP on Azure Pipeline'

```
