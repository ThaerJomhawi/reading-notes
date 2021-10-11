# Arrays, Loops, Imports

## Packages and Import

- **Package** :

* Java classes can be grouped together in packages.
* A package name is the same as the directory (folder) name which contains the .java files.

**Package declaration :**

- The first statement in a Java source file, must be the package declaration.

- Following the optional package declaration, you can have import statements, which allow you to specify classes from other packages that can be referenced without qualifying them with their package.

**Types of Packages**

- Built-in
- User-defined

**Package declaration syntax:**

The statement order is as follows. Comments can go anywhere.

1- Package statment (optional).

2- Imports (optional).

3- Class or interface definitions.

```
// This source file must be Drawing.java in the illustration directory.

package illustration;

import java.awt.*;

public class Drawing {
    . . .
}
```

**Imports: three options :**

-import javax.swing.;\* : To make all classes visible altho only one is used.

```
import javax.swing.*;  // Make all classes visible altho only one is used.

class ImportTest {
    public static void main(String[] args) {
        JOptionPane.showMessageDialog(null, "Hi");
        System.exit(0);
    }
}
```

-import javax.swing.JOptionPane; : To ake a single class visible.

```
import javax.swing.JOptionPane;  // Make a single class visible.

class ImportTest {
    public static void main(String[] args) {
        JOptionPane.showMessageDialog(null, "Hi");
        System.exit(0);
    }
}
```

-We can the fully qualified class name without an import. :

```
class ImportTest {
    public static void main(String[] args) {
        javax.swing.JOptionPane.showMessageDialog(null, "Hi");
        System.exit(0);
    }
}
```

- **common import:**

* there are 166 packages containing 3279 classes and interfaces in Java 5. However, only a few packages are used in most programming

_example:_

```
import java.awt.*;	Common GUI elements.
import java.awt.event.*;	The most common GUI event listeners.
import javax.swing.*;	More common GUI elements. Note "javax".
import java.util.*;	Data structures (Collections), time, Scanner, etc classes.
import java.io.*;	Input-output classes.
import java.text.*;	Some formatting classes.
import java.util.regex.*;	Regular expression classes.
```

## Different types of loops in Java

### Whats is looping :

- looping is a feature which facilitates the execution of a set of instructions until the controlling Boolean-expression evaluates to false.

### **the types of loops that we can find in Java:**

**Simple for loop**:

```
A for loop is a control structure that allows us to repeat certain operations by incrementing and evaluating a loop counter.
```

**Enhanced for-each loop**

**While loop:**

```
The while loop is Java's most fundamental loop statement. It repeats a statement or a block of statements while its controlling Boolean-expression is true.
```
**Do-While loop:**

```
The do-while loop works just like the while loop except for the fact that the first condition evaluation happens after the first iteration of the loop.

```

