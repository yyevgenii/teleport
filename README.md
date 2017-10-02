# Teleport
Wrapper around teleport proxy to grab dumps

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


