### Compress a directory in linux using Parallel Implementation of GZip i.e., `pigz`. 
```
apt install pigz
apt install pv # For measuring progress of the zipping/unzipping operation
```
### Pigz compression flags
- 9 for best compression
- 1 for fast compression
- 0 for no compression
- 6 for default compression
```
tar cf - <dir_name> | pigz -9 > <archive_name>.tar.gz 
```
- If you want to see progress during the compression add `pv` command
```
tar cf - <dir_name> | pv | pigz -9 > <archive_name>.tar.gz 
```


### Uncompress a directory in linux using `pigz`
```
pigz -d <archive_name>.tar.gz | tar xf -
```

- If you want to see progress of the decompression
```
pv <archive_name>.tar.gz | pigz -d | tar xf -
```
