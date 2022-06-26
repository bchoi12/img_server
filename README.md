# img_server

## Rename all files sequentially

```
# Powershell

$i = 1
Get-ChildItem *.jpg | %{Rename-Item $_ -NewName ("$($i).jpg" -f $i++)}
```

```
# Bash

ls -v | cat -n | while read n f; do mv -n "$f" "$n.jpg"; done 
```