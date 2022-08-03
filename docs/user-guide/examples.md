There are a few examples listed below on running the AsBuiltReport script against a FortiGate. Refer to the README.md file in the main AsBuiltReport project repository for more examples.

```powershell
# Generate a Fortinet FortiGate As Built Report for FortiGate fortigate.fortidemo.com using specified credentials. Export report to HTML & DOCX formats. Use default report style. Append timestamp to report filename. Save reports to 'C:\Users\PowerFGT\Documents'
New-AsBuiltReport -Report Fortinet.FortiGate -Target fortigate.fortidemo.com -Username demo -Password demo -Format Html,Word -OutputFolderPath 'C:\Users\PowerFGT\Documents' -Timestamp

# Generate a Fortinet FortiGate As Built Report for FortiGate fortigate.fortidemo.com using specified credentials and report configuration file. Export report to Text, HTML & DOCX formats. Use default report style. Save reports to 'C:\Users\PowerFGT\Documents'. Display verbose messages to the console.
New-AsBuiltReport -Report Fortinet.FortiGate -Target fortigate.fortidemo.com -Username demo -Password 'demo' -Format Text,Html,Word -OutputFolderPath 'C:\Users\PowerFGT\Documents' -ReportConfigFilePath 'C:\Users\Jon\AsBuiltReport\AsBuiltReport.Fortinet.FortiGate.json' -Verbose

# Generate a Fortinet FortiGate As Built Report for FortiGate fortigate.fortidemo.com using stored credentials. Export report to HTML & Text formats. Use default report style. Highlight environment issues within the report. Save reports to 'C:\Users\PowerFGT\Documents'.
$Creds = Get-Credential
New-AsBuiltReport -Report Fortinet.FortiGate -Target fortigate.fortidemo.com -Credential $Creds -Format Html,Text -OutputFolderPath 'C:\Users\PowerFGT\Documents' -EnableHealthCheck

# Generate a Fortinet FortiGate As Built Report for FortiGate fortigate.fortidemo.com using stored credentials. Export report to HTML & DOCX formats. Use default report style. Reports are saved to the user profile folder by default. Attach and send reports via e-mail.
New-AsBuiltReport -Report Fortinet.FortiGate -Target fortigate.fortidemo.com-Username demo -Password 'demo' -Format Html,Word -OutputFolderPath 'C:\Users\PowerFGT\Documents' -SendEmail
```