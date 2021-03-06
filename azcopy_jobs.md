## azcopy jobs

Sub-commands related to managing jobs

### Synopsis

Sub-commands related to managing jobs.

### Examples

```
azcopy jobs show [jobID]
```

### Options

```
  -h, --help   help for jobs
```

### Options inherited from parent commands

```
      --cap-mbps float                      Caps the transfer rate, in megabits per second. Moment-by-moment throughput might vary slightly from the cap. If this option is set to zero, or it is omitted, the throughput isn't capped.
      --output-type string                  Format of the command's output. The choices include: text, json. The default value is 'text'. (default "text")
      --trusted-microsoft-suffixes string   Specifies additional domain suffixes where Azure Active Directory login tokens may be sent.  The default is '*.core.windows.net;*.core.chinacloudapi.cn;*.core.cloudapi.de;*.core.usgovcloudapi.net'. Any listed here are added to the default. For security, you should only put Microsoft Azure domains here. Separate multiple entries with semi-colons.
```

### SEE ALSO

* [azcopy](azcopy.md)	 - AzCopy is a command line tool that moves data into and out of Azure Storage.
* [azcopy jobs clean](azcopy_jobs_clean.md)	 - Remove all log and plan files for all jobs
* [azcopy jobs list](azcopy_jobs_list.md)	 - Displays information on all jobs
* [azcopy jobs remove](azcopy_jobs_remove.md)	 - Remove all files associated with the given job ID.
* [azcopy jobs resume](azcopy_jobs_resume.md)	 - Resume the existing job with the given job ID.
* [azcopy jobs show](azcopy_jobs_show.md)	 - Show detailed information for the given job ID

###### Auto generated by spf13/cobra on 31-Mar-2021
