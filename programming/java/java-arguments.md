# Arguments

How to pass arguments to a Java program.

## Table of Contents

- [Main Method Parameter](#main-method-parameter)
- [Javac](#javac)
- [Maven](#maven)
- [JAR](#jar)

---

## Main Method Parameter

```java
public class Main {
    public static void main(String[] args) {
        for (int i = 0; i < args.length; i++) {
            System.out.println("args " + i + ": " + args[i]);
        }
    }
}
```

- Main method takes String array as arguments.

<p align="center">
  <img src="../../assets/always-have-been.png" alt="always-have-been.png" height="256"/>
</p>

> [!NOTE]
> Unlike **C** it does not require `int argc` parameter.

---

## Javac

More about javac from [javac.md](./javac.md)

Compile:

```sh
javac Main.java
```

- Creates `Main.class` file.

Run it with arguments:

```sh
java Main foo bar 123
```

Output:

```txt
args 0: foo
args 1: bar
args 2: 123
```

> [!NOTE]
> Unlike **C**, 1st argument is not the program's path.

---

## Maven

Run with [exec-maven-plugin](https://mvnrepository.com/artifact/org.codehaus.mojo/exec-maven-plugin):

```sh
mvn compile

mvn exec:java -Dexec.args="foo bar 123"
```

- `-D`: Defines a maven property.

> [!IMPORTANT]
> Path to main class must be specified in `pom.xml`.

---

## JAR

After building JAR:

```sh
mvn package

java -jar target/my-app-1.0.jar foo bar 123
```

- `package` command will output **JAR** file under `target` directory.
