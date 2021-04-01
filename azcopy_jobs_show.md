## azcopy jobs show

Show detailed information for the given job ID

### Synopsis


If you provide only a job ID, and not a flag, then this command returns the progress summary only.
The byte counts and percent complete that appears when you run this command reflect only files that are completed in the job. They don't reflect partially completed files.
If you set the with-status flag, then only the list of transfers associated with the given status appear.

```
azcopy jobs show [jobID] [flags]
```

### Options

```
  -h, --help                 help for show
      --with-status string   Only list the transfers of job with this status, available values: Started, Success, Failed.
```

### Options inherited from parent commands

```
      --cap-mbps float                      Caps the transfer rate, in megabits per second. Moment-by-moment throughput might vary slightly from the cap. If this option is set to zero, or it is omitted, the throughput isn't capped.
      --output-type string                  Format of the command's output. The choices include: text, json. The default value is 'text'. (default "text")
      --trusted-microsoft-suffixes string   Specifies additional domain suffixes where Azure Active Directory login tokens may be sent.  The default is '*.core.windows.net;*.core.chinacloudapi.cn;*.core.cloudapi.de;*.core.usgovcloudapi.net'. Any listed here are added to the default. For security, you should only put Microsoft Azure domains here. Separate multiple entries with semi-colons.
```

### SEE ALSO

* [azcopy jobs](azcopy_jobs.md)	 - Sub-commands related to managing jobs

###### Auto generated by spf13/cobra on 31-Mar-2021