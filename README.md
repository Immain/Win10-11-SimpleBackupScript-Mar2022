<img src=https://www.gamerevolution.com/assets/uploads/2021/07/Windows-11-downgrade-to-Windows-10-1280x720.png >

# Win10-11-SimpleBackupScript-Mar2022
Use this ansible script to backup documents and Outlook

# Operating System Requirements
- MacOS
- Linux

# Enable WinRM on the remote machine using this Action Script
```
$url = "https://raw.githubusercontent.com/ansible/ansible/devel/examples/scripts/ConfigureRemotingForAnsible.ps1"
$file = "$env:temp\ConfigureRemotingForAnsible.ps1"
(New-Object -TypeName System.Net.WebClient).DownloadFile($url, $file)
powershell.exe -ExecutionPolicy ByPass -File $file
winrm enumerate winrm/config/Listener
```
# To run the script, use the following command:
```
sudo ansible-playbook backup.yaml -i hosts
```
