# File Management Commands

## List Files

### Detailed listing

```bash
ls -l
```

### Human-readable file sizes

```bash
ls -lh
```

### Show hidden files

```bash
ls -lha
```

---

## Create a Directory

```bash
mkdir projects
```

Create parent directories if needed:

```bash
mkdir -p projects/linux/rhel
```

---

## Create an Empty File

```bash
touch notes.txt
```

---

## Copy a File

```bash
cp notes.txt backup.txt
```

---

## Move or Rename a File

Move:

```bash
mv notes.txt Documents/
```

Rename:

```bash
mv notes.txt lesson6-notes.txt
```

---

## Delete a File

```bash
rm notes.txt
```

---

## Delete a Directory

```bash
rm -r projects
```