# Linux commands...

## scp
```
scp -i ~/.ssh/credentials.pem ./data.tgz  user@server:../folder
```


## tar

### tar a folder
```
tar -cfz targetfile.tgz sourcefolder
```


### untar a file
```
tar -xfz sourcefile.tgz
```
## redirect output
```
ls importscript.sh asdf 1>output.txt 2>error.txt
```

## Processes
### Execute long running process in background
```
nohup ./importscript.sh -u admin -p xxx -r https://server.com/  1>output.txt 2>error.txt &
```
