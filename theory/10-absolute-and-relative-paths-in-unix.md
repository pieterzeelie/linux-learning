# Summary: Absolute and Relative Pathnames in UNIX/Linux

---

## 📂 Path Basics

- A **path** specifies the location of a file or directory.
- Two types:
  - **Absolute Path** → starts from root `/`, independent of current directory.
  - **Relative Path** → based on current working directory (`pwd`).

---

## 🔹 Absolute Path

- Always begins with `/`.
- Full address from root to target file/directory.

- Example:
  ```bash
  /home/user/scripts/myscript.sh
  ```

## 🔹 Relative Path

- Does not start with /.
- Depends on current directory.
- Uses shortcuts:
- . → current directory
- .. → parent directory

- Example:

```bash
cd abc     # enter subdirectory
cd ..      # move up one level
cd ../..   # move up two levels
```

🧭 Examples:

- Absolute Path:

```bash
cd /home/user/docs
```

- Relative Path:

```bash
cd docs
```

✅ Key Takeaways

- Absolute paths are precise and consistent.
- Relative paths are shorter and flexible.
- Mastering both improves navigation efficiency and scripting reliability
