## 1. Change the Owner of a File
Practice changing ownership of a single file.
Scenario
You created a file as root but want a normal user (e.g., pieter) to own it.

### Commands
```bash 
sudo touch report.txt
sudo chown pieter report.txt
ls -l report.txt
```
## 2. Change Only the Group of a File
### Scenario
You want a team group (e.g., devteam) to manage a shared file.
### Commands
```bash
sudo groupadd devteam
sudo chown :devteam report.txt
ls -l report.txt
```

## 3. Change Both Owner and Group
### Scenario
You’re restructuring permissions and want both owner and group updated.
### Commands
```bash
sudo chown pieter:devteam report.txt
ls -l report.txt
```

## 4. Recursively Change Ownership of a Directory
### Scenario
You created a project folder as root and want to hand it over to a user.
### Commands
```bash
sudo mkdir -p /opt/projectA
sudo chown -R pieter:devteam /opt/projectA
ls -l /opt
```

## 5. Change Ownership Only If Current Owner Matches (--from)
### Scenario
You want to update ownership only if the file is currently owned by a specific user.
### Commands
```sudo chown --from=root pieter report.txt```



## 6. Change Group Only If Current Group Matches
### Scenario
You want to update the group only if it currently belongs to devteam.
### Commands
```sudo chown --from=:devteam :admins report.txt```



## 7. Copy Ownership From One File to Another (--reference)
### Scenario
You want two files to always have identical ownership.
### Commands
```bash
sudo touch fileA fileB
sudo chown pieter:devteam fileA
sudo chown --reference=fileA fileB
ls -l fileA fileB
```


## 8. Change Ownership of Multiple Files at Once
### Scenario
Batch‑assign ownership to a set of files.
### Commands
```bash
sudo touch a.txt b.txt c.txt
sudo chown pieter:devteam a.txt b.txt c.txt
ls -l
```

## 9. Change Ownership of a Symlink Itself (-h)
### Scenario
You want to modify the symlink, not the target file.
### Commands
```bash
sudo ln -s report.txt link_report
sudo chown -h pieter link_report
ls -l link_report
```

## 10. Verbose Output to See What Changed (-v)
### Scenario
You want to see exactly what chown is doing.
### Commands
```sudo chown -v pieter report.txt```

## 11. Suppress Errors When Changing Ownership (-f)
### Scenario
You’re running a script and want to avoid noisy errors.
### Commands
```sudo chown -f pieter missingfile.txt```



## 12. Combine Recursive + Symlink Handling (-R -P / -H / -L)
### Scenario
Practice how chown behaves with symlinks during recursion.
### Commands
```bash
sudo mkdir -p testdir/sub
sudo touch testdir/sub/file.txt
sudo ln -s testdir link_testdir
```

```bash
# Do not follow symlinks
sudo chown -RP pieter:devteam testdir
```

```bash
# Follow symlinks on command line only
sudo chown -RH pieter:devteam testdir
```

```bash
# Follow all symlinks
sudo chown -RL pieter:devteam testdir
```











