# Title

```bash
LOCK="/var/run/rsync.lock"
 
if [ ! -e $LOCK ]; then
  touch $LOCK
  rsync -av foo bar
  rm $LOCK
else
   echo "It's running"
fi
```
