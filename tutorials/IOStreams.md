# IO Streams

## Tutorial
In Java, **IO Streams** (Input/Output Streams) are used to handle input and output operations. These streams can read data from a source (like a file or network) or write data to a destination.

There are two main types of streams:
1. **Byte Streams:** Handle binary data (e.g., images, files).
   - Examples: `FileInputStream`, `FileOutputStream`
2. **Character Streams:** Handle text data.
   - Examples: `FileReader`, `FileWriter`

### Key Classes
- **`InputStream`**: Abstract class for reading byte data.
- **`OutputStream`**: Abstract class for writing byte data.
- **`Reader`**: Abstract class for reading character data.
- **`Writer`**: Abstract class for writing character data.

### Example of Reading a File
To read from a text file, you can use `FileReader`:
```java
import java.io.*;

public class ReadFileExample {
    public static void main(String[] args) {
        try {
            FileReader reader = new FileReader("example.txt");
            int data;
            while ((data = reader.read()) != -1) {
                System.out.print((char) data);
            }
            reader.close();
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
