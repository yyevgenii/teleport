# Teleport
Wrapper around teleport proxy to grab dumps

## Before usage
Please, make sure that ```tsh``` from that [source](https://github.com/gravitational/teleport/releases/tag/v1.3.2), is installed on your host. The following command should show you current version of ```tsh``` installed on your host.
```
$ tsh version
```

## Usage
cloud-teleport PROJECT_ID [ssh|dump] [-d|--dump=(code|db)] [-u|--user=(teleport username)] [-s|--server=(1|2|3)]
 - PROJECT_ID - required argument, cloud project ID
 - -d|--dump code|db - make only a code or db dump
 - -u|--user username - if you want to specify different username for cloud, current user by default
 - -s|--server 1,2 or 3 - open ssh connection to a specified server


## Examples:
 - Download dumps into current directory
```
$ cloud-teleport projectId dump
```
- Connect by ssh
```
$ cloud-teleport projectId
```
- Download only code dump
```
$ cloud-teleport projectId -d code
```
- Connect by ssh on a second server
```
$ cloud-teleport projectId -s 2
```

###### If your username differs from cloud account username
```
$ export TELEPORT_USER=username
```
or 
```
$ cloud-teleport projectId -u username
```


