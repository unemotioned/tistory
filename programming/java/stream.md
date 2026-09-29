# Stream

```java
import java.io.BufferedReader;
import java.io.FileReader;
```

---

## Read File

```java
public void readFile(String fileName) {
  try (BufferedReader br = new BufferedReader(new FileReader(fileName))) {
    while ((br.readLine()) != null) {
      System.out.println(br.readLine());
    }
  } catch (FileNotFoundException e) {
    System.out.println(e);
  } catch (IOException e) {
    System.out.println(e);
  }
}
```
