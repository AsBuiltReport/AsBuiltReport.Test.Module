### VMware vSphere
The VMware vSphere As Built Report supports the following vSphere versions;

* vSphere 6.5
* vSphere 6.7
* vSphere 7.0

#### :warning: End of Support
The following VMware vSphere versions are no longer being tested and/or supported;

* vSphere 5.5
* vSphere 6.0

### :material-console: PowerShell
This report is compatible with the following PowerShell versions;

| Windows PowerShell 5.1 |     PowerShell 7    |
|:----------------------:|:--------------------:|
|   :white_check_mark:   | :white_check_mark: |

### :package: PowerShell Modules

Each of these modules can be easily downloaded and installed via the PowerShell Gallery

- [VMware PowerCLI Module](https://www.powershellgallery.com/packages/VMware.PowerCLI/)
- [AsBuiltReport.VMware.vSphere Module](https://www.powershellgallery.com/packages/AsBuiltReport.VMware.vSphere/)

### :penguin: Linux & macOS
.NET Core is required for cover page image support on Linux and macOS operating systems.

* [Installing .NET Core for macOS](https://docs.microsoft.com/en-us/dotnet/core/install/macos)
* [Installing .NET Core for Linux](https://docs.microsoft.com/en-us/dotnet/core/install/linux)

ℹ️ If you are unable to install .NET Core, you must set `ShowCoverPageImage` to `False` in the [report JSON configuration](../configuration/#report) file.


### :closed_lock_with_key: Required Privileges

A VMware vSphere As Built Report can be generated with read-only privileges, however the following sections will be skipped;

* vSphere licensing information
* VM Storage Policy information
* VMware Update Manager / Lifecycle Manager information

For a complete report, the following role assigned privileges are required;

* Global > Licenses
* Global > Settings
* Host > Configuration > Change Settings
* Profile-driven Storage > Profile-driven storage view
* VMware vSphere Update Manager > View Compliance Status