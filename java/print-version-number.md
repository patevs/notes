# Print Java Version Number

* [Fetch Java version using single line command](https://stackoverflow.com/questions/7596454/how-to-fetch-java-version-using-single-line-command-in-linux/7596535#7596535)

1. Redirect `stderr` to `stdout`.
2. Get the first line.
3. Filter version number.

```bash
# Note for Windows users: 
#   head and awk are provided by git unix tools located in `$GIT_HOME/usr/bin`.
$ java -version 2>&1 | head -n 1 | awk -F '"' '{print $2}'
```

---
