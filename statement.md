# Extract data from an object using peek() and map() methods

Let us start with a simple example


```java runnable
// { autofold
import java.util.stream.Stream;
public class Main {

public static void main(String[] args) {
// }

long count = Stream.of(1, 2, 3, 4, 5).map(i -> i * i).count();
System.out.printf("This stream has %d elements", count);

//{ autofold
}

}
//}
```

# Square each element in the above stream and print

```java runnable
// { autofold
import java.util.stream.Stream;
public class Main {

public static void main(String[] args) {
// }

long count = Stream.of(1, 2, 3, 4, 5)
                    .map(i -> i * i)
                    .peek(i -> System.out.printf("%d ", i))
                    .count();
System.out.printf("%nThe stream has %d elements", count);

//{ autofold
}

}
//}
```

The map() operation in the stream applies the given lambda function(i - > i * i) as an argument on the elements of the stream. 
The count method returns the value 5.
To Print the square value of each value in the stream, we used intermediate method peek().

