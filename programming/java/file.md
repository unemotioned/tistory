# File

```java
import java.io.File;
```

## Table of Contents

- [Check](#check)
- [Create File](#create-file)
- [Create Directory](#create-directory)
  - [Directories](#directories)

---

## Check

```java
public void checkFile(String fileName) {
  File file = new File(fileName);

  if (file.isFile()) {
    System.out.println(file + " is a file");
  } else if (file.isDirectory()) {
    System.out.println(file + " is a directory");
  } else if (!file.exists()) {
    System.out.println(file + " doesn't exists");
  }
}
```

---

## Create File

```java
public void createFile(String fileName) {
  File file = new File(fileName);

  try {
    if (file.createNewFile()) {
      System.out.println(fileName + " is created");
    }
  } catch (IOException e) {
    System.out.println(e);
  }
}
```

---

## Create Directory

```java
public void makeDirectory(String dir) {
  File dir = new File(dir);

  if (dir.mkdir()) {
    System.out.println(dir + " created");
  }
}
```

### Directories

create missing parent directories too

```java
public void makeDirectories() {
  String dir = "foo/bar/bazz";
  File dir = new File(dir);

  if (dir.mkdirs()) {
    System.out.println(dir + " created");
  }
}
```

> [!NOTE]
> `try - catch` not necessary.
