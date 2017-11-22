# Teleport
Wrapper around teleport proxy to grab dumps

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

Please, make sure that ```tsh``` from that [source](https://github.com/gravitational/teleport/releases/tag/v1.3.2), is installed on your host. The following command should show you current version of ```tsh``` installed on your host.
```
$ tsh version
```

### Installing
Clone or download script from https://github.com/magento-sparta/teleport
```
git clone https://github.com/magento-sparta/teleport
ln -s /usr/local/bin/cloud-teleport /path/to/teleport/repository/cloud-teleport
```
or download file directly from master branch to the /usr/local/bin directory
```
curl -o /usr/local/bin/cloud-teleport https://raw.githubusercontent.com/magento-sparta/teleport/master/cloud-teleport
```

### Usage
Usage : $(basename "$0") PROJECT_ID [ssh|dump] [-d|--dump=(code|db|scp file_path)] [-u|--user=(teleport username)] [-s|--server=(1|2|3)]
Options:
 - PROJECT_ID - required argument, cloud project ID
 - ssh - Make SSH connection to remote cloud server
 - dump - Create and download code and database dumps
 - scp - Download file from remote cloud server
 - -d|--dump code|db - make only a code or db dump
 - -u|--user username - if you want to specify different username for cloud, current user by default
 - -s|--server 1,2 or 3 - open ssh connection to a specified server

### Examples:
How to download dumps into current directory?
```
$ cloud-teleport projectId dump
```
How to connect by SSH to remote cloud server?
```
$ cloud-teleport projectId
```
How to generate and download only code dump?
```
$ cloud-teleport projectId -d code
```
How to connect by ssh on a second server node?
```
$ cloud-teleport projectId -s 2
```

###### If your username differs from cloud account username
```
$ export TELEPORT_USER=username
```
```
$ cloud-teleport projectId -u username
```


