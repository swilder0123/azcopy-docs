## azcopy load clfs

Transfers local data into a Container and stores it in Microsoft's Avere Cloud FileSystem (CLFS) format

### Synopsis

The load command copies data into Azure Blob Storage Containers and stores it in Microsoft's Avere Cloud FileSystem (CLFS) format. 
The proprietary CLFS format is used by the Azure HPC Cache and Avere vFXT for Azure products.

To leverage this command, please install the necessary extension via: pip3 install clfsload~=1.0.23. Please make sure CLFSLoad.py is 
in your PATH. For more information on this step, please visit https://aka.ms/azcopy/clfs.

This command is a simple option for moving existing data to cloud storage for use with specific Microsoft high-performance computing cache products. 
Because these products use a proprietary cloud filesystem format to manage data, that data cannot be loaded through the native copy command. 
Instead, the data must be loaded through the cache product itself OR via this load command, which uses the correct proprietary format.
This command lets you transfer data without using the cache - for example, 
to pre-populate storage or to add files to a working set without increasing cache load.

The destination is an empty Azure Storage Container. When the transfer is complete, the destination container can be used with an Azure HPC Cache instance or Avere vFXT for Azure cluster.

NOTE: This is a preview release of the load command. Please report any issues on the AzCopy Github repo.


```
azcopy load clfs [local dir] [container URL] [flags]
```

### Examples

```

Load an entire directory with a SAS:
  - azcopy load clfs "/path/to/dir" "https://[account].blob.core.windows.net/[container]?[SAS]" --state-path="/path/to/state/path"

```

### Options

```
      --compression-type string   specify the compression type to use for the transfers. Available values are: DISABLED,LZ4. (default "LZ4")
  -h, --help                      help for clfs
      --log-level string          define the log verbosity for the log file, available levels: DEBUG, INFO, WARNING, ERROR. (default "INFO")
      --max-errors uint32         specify the maximum number of transfer failures to tolerate. If enough errors occur, stop the job immediately.
      --new-session               start a new job rather than continuing an existing one whose tracking information is kept at --state-path. (default true)
      --preserve-hardlinks        preserve hard link relationships.
      --state-path string         required path to a local directory for job state tracking. The path must point to an existing directory in order to resume a job. It must be empty for a new job.
```

### Options inherited from parent commands

```
      --cap-mbps float                      Caps the transfer rate, in megabits per second. Moment-by-moment throughput might vary slightly from the cap. If this option is set to zero, or it is omitted, the throughput isn't capped.
      --output-type string                  Format of the command's output. The choices include: text, json. The default value is 'text'. (default "text")
      --trusted-microsoft-suffixes string   Specifies additional domain suffixes where Azure Active Directory login tokens may be sent.  The default is '*.core.windows.net;*.core.chinacloudapi.cn;*.core.cloudapi.de;*.core.usgovcloudapi.net'. Any listed here are added to the default. For security, you should only put Microsoft Azure domains here. Separate multiple entries with semi-colons.
```

### SEE ALSO

* [azcopy load](azcopy_load.md)	 - Sub-commands related to transferring data in specific formats

###### Auto generated by spf13/cobra on 31-Mar-2021
