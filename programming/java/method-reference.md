# Method Reference

Passing a reference of a method without invoking it.

## Reference

[Geeks for Geeks - Java Method Reference](https://www.geeksforgeeks.org/java/java-method-references/)

---

Pass the method reference to helper method and invoke from lambda function so
you don't have to write helper methods to check duplication of input for each member.

- `Foo::getBar`: Reference the getter method of member variable **bar** inside
  class **Foo** without invoking it.

- `Function<Foo, String> getter`: Parameter definition of function named
  **getter** that takes object **Foo** and return string type.

- `stream()`: Create stream over the list's elements.

- `anyMatch(predicate)`: Return true on first match.

- `entry -> ...`: Parameter of lambda that receives a stream element.

- `getter.apply(entry)`: Invoke the function with the given argument.

```java
import java.util.function.Function; // For Function<T, R>

@AllArgsConstructor
@Getter
public class Foo {
    private String bar;
    private String baz;
}

public class MyController {
    List<Foo> entries;

    public MyController() {
        entries = start.getEntries();
    }

    public void addEntry() {
        // Pass method reference
        String bar = getUniqueMember("Enter bar: ", Foo::getBar);
        if (bar == null) {
            return;
        }

        // Pass method reference
        String baz = getUniqueMember("Enter baz: ", Foo::getBaz);
        if (baz == null) {
            return;
        }

        Foo foo = new Foo(bar, baz);
        myUtil.appendToFile(foo);
    }

    // Parameter that takes the method reference
    private String getUniqueMember(String prompt, Function<Foo, String> getter) {
        while (true) {
            String input = viewer.getMember(prompt);
            if (input == null) {
                return null;
            }

            // Invoke the referenced method from lambda
            boolean isDuplicated = entries.stream().anyMatch(entry -> input.equalsIgnoreCase(getter.apply(entry)));
            if (!isDuplicated) {
                return input;
            }
        }
    }
}
```

---

**Predicate**: Part of a sentence that tells what the subject does. (A function
that tests a condition and returns boolean type)
