## azcopy make

Create a container or file share.

### Synopsis

Create a container or file share represented by the given resource URL.

```
azcopy make [resourceURL] [flags]
```

### Examples

```

  - azcopy make "https://[account-name].[blob,file,dfs].core.windows.net/[top-level-resource-name]"

```

### Options

```
  -h, --help              help for make
      --quota-gb uint32   Specifies the maximum size of the share in gigabytes (GiB), 0 means you accept the file service's default quota.
```

### Options inherited from parent commands

```
      --cap-mbps float                      Caps the transfer rate, in megabits per second. Moment-by-moment throughput might vary slightly from the cap. If this option is set to zero, or it is omitted, the throughput isn't capped.
      --output-type string                  Format of the command's output. The choices include: text, json. The default value is 'text'. (default "text")
      --trusted-microsoft-suffixes string   Specifies additional domain suffixes where Azure Active Directory login tokens may be sent.  The default is '*.core.windows.net;*.core.chinacloudapi.cn;*.core.cloudapi.de;*.core.usgovcloudapi.net'. Any listed here are added to the default. For security, you should only put Microsoft Azure domains here. Separate multiple entries with semi-colons.
```

### SEE ALSO

* [azcopy](azcopy.md)	 - AzCopy is a command line tool that moves data into and out of Azure Storage.

###### Auto generated by spf13/cobra on 31-Mar-2021
