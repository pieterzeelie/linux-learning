# Step 1: Create a file
Run:
```bash
echo "Hello World" > demo.txt
```

# Step 2: Create a hard link
Run:
```bash
ln demo.txt hard_demo.txt
```

# Step 3: Create a soft link
Run:
```bash
ln -s demo.txt soft_demo.txt
```

# Step 4: Check details
Run:
```bash
ls -l
```
Output:
```bash
-rw-r--r-- 2 pieter devops 12 Dec  3 20:10 demo.txt
-rw-r--r-- 2 pieter devops 12 Dec  3 20:10 hard_demo.txt
lrwxrwxrwx 1 pieter devops  8 Dec  3 20:10 soft_demo.txt -> demo.txt
```