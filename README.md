# Teleport
Wrapper around teleport proxy to grab dumps

## Before usage
Please, make sure that ```tsh``` from that [source](https://github.com/gravitational/teleport/releases/tag/v1.3.2), is installed on your host. The following command should show you current version of ```tsh``` installed on your host.
```
$ tsh version
```

## Usage
cloud-teleport PROJECT_ID [ssh|dump] [Teleport Username]

## Examples:
 - Download dumps into current directory
```
$ cloud-teleport projectId dump
```
- Connect by ssh
```
$ cloud-teleport projectId
```

###### If your username differs from cloud account username
```
$ export TELEPORT_USER=username
```
or 
```
$ cloud-teleport projectId dump username
```


