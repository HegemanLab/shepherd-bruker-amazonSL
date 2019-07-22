# Shepherd-bruker-amazonSL
Log parsing and forwarding to an InfluxDB database for logs from [Bruker Amazon SL](https://www.bruker.com/products/mass-spectrometry-and-separations/lc-ms/ion-trap/amazon-sl/overview.html) using Telegraf and Fluent-Bit.
 
## Motivation
The goal is to have real-time and historical monitoring of the Bruker's logbooks so that machine performance and status can be evaluated.

## Screenshots

## Tech used
[Telegraf](https://github.com/influxdata/telegraf)

[Fluent-Bit](https://fluentbit.io/)

## Installation (WIP)
1. Download the [telegraf distribution for windows.](https://dl.influxdata.com/telegraf/releases/telegraf-1.10.4_windows_amd64.zip)

2. Download the Fluent-Bit td-agent, vc_redist.x64.exe, vc_redist.x86.exe, Win32OpenSSL-1_0_2s.exe, nssm-2.24.zip, parsers.conf, and fluent.conf from this repository.

3. Either download the telegraf.conf configuration file from the github repo for the lab system you wish to setup or grab the telegraf.conf file you created in the Config File Setup.

4. Run the Fluent-Bit td-agent, vc_redist.x64.exe, vc_redist.x86.exe, and Win32OpenSSL-1_0_2s.exe files and reboot.

5. Place the fluent.conf and parsers.conf in C:\

7. Create the directory `C:\Program Files\Telegraf`

8. Place both the telegraf.exe that was downloaded in step 1 and the config file downloaded in step 3 into `C:\Program Files\Telegraf`

9. As administrator run powershell and run the command 
```
C:\"Program Files"\Telegraf\telegraf.exe --service install
```

10. Open command prompt and run the following command

11. To start telegraf run the command `net start telegraf`

12. Open up the Windows Services menu and start the created Fluent-Bit service.

## References
- [Running Telegraf as a Windows service](https://github.com/influxdata/docs.influxdata.com/blob/master/content/telegraf/v1.7/administration/windows_service.md) - Official Documentation
