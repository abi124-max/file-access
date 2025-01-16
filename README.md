# file-access
its about network access
**company**:CODTECH IT SOLUTION PVT.LTD
**NAME**:H.Abirami
**INTERN ID**:CT08GNX
**DOMAIN**:JAVA programming
**BATCH DURATION**:25-12-24 to 25-01-25
**MENTOR NAME**:NEELA SANTHOSH
# ENTER THE DESCRIPTION  OF TASK PERFORMED WITHIN 500 WORDS
File access in Java is a fundamental aspect of many applications, allowing programs to read from and write to files on the file system. Java provides several classes and methods to handle file operations efficiently.

Key Classes for File Access
File Class: The File class in the java.io package represents a file or directory path. It provides methods to create, delete, and check the existence of files and directories.

java
import java.io.File;

public class FileExample {
    public static void main(String[] args) {
        File file = new File("example.txt");
        if (file.exists()) {
            System.out.println("File exists");
        } else {
            System.out.println("File does not exist");
        }
    }
}
FileReader and FileWriter: These classes are used for reading from and writing to text files. FileReader reads character streams, while FileWriter writes character streams.
# PROGRAM
java
import java.io.FileReader;
import java.io.FileWriter;
import java.io.IOException;

public class FileReadWriteExample {
    public static void main(String[] args) {
        try (FileWriter writer = new FileWriter("example.txt")) {
            writer.write("Hello, World!");
        } catch (IOException e) {
            e.printStackTrace();
        }

        try (FileReader reader = new FileReader("example.txt")) {
            int character;
            while ((character = reader.read()) != -1) {
                System.out.print((char) character);
            }
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
BufferedReader and BufferedWriter: These classes provide efficient reading and writing of text files by buffering characters. They are often used in conjunction with FileReader and FileWriter.

java
import java.io.BufferedReader;
import java.io.BufferedWriter;
import java.io.FileReader;
import java.io.FileWriter;
import java.io.IOException;

public class BufferedReadWriteExample {
    public static void main(String[] args) {
        try (BufferedWriter writer = new BufferedWriter(new FileWriter("example.txt"))) {
            writer.write("Hello, Buffered World!");
        } catch (IOException e) {
            e.printStackTrace();
        }

        try (BufferedReader reader = new BufferedReader(new FileReader("example.txt"))) {
            String line;
            while ((line = reader.readLine()) != null) {
                System.out.println(line);
            }
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
FileInputStream and FileOutputStream: These classes are used for reading from and writing to binary files. FileInputStream reads byte streams, while FileOutputStream writes byte streams.

java
import java.io.FileInputStream;
import java.io.FileOutputStream;
import java.io.IOException;

public class FileStreamExample {
    public static void main(String[] args) {
        try (FileOutputStream fos = new FileOutputStream("example.bin")) {
            fos.write(new byte[]{1, 2, 3, 4, 5});
        } catch (IOException e) {
            e.printStackTrace();
        }

        try (FileInputStream fis = new FileInputStream("example.bin")) {
            int byteData;
            while ((byteData = fis.read()) != -1) {
                System.out.print(byteData + " ");
            }
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
Conclusion
Java provides a rich set of classes for file access, making it easy to perform various file operations. Whether you're working with text files or binary files, Java's java.io package offers the tools you need to read, write, and manipulate files efficiently. Understanding these classes and their usage is essential for any Java developer working with file I/O.
# OUTPUT
![Image](https://github.com/user-attachments/assets/692e3452-0eb9-4879-a1b2-952d1f4fcc46)





Message Copilot
