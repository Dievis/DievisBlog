---
title: Giới Thiệu Về Java - Từ Cơ Bản Đến Nâng Cao
date: 2024-12-25
author: Đạt TP
description: Hướng dẫn toàn diện về lập trình Java từ cơ bản đến nâng cao
tags:
  - Java
  - Lập Trình
  - Hướng Dẫn
---

## **Giới Thiệu Về Java**  
Java là một trong những ngôn ngữ lập trình phổ biến nhất hiện nay. Được phát triển bởi **Sun Microsystems** (hiện thuộc **Oracle**), Java nổi bật nhờ tính đa nền tảng, an toàn và hiệu suất cao.  

---

## **1. Java Là Gì?**  
Java là ngôn ngữ lập trình **hướng đối tượng (OOP)** và **đa mục đích**. Một trong những đặc điểm nổi bật của Java là khả năng **viết một lần, chạy mọi nơi** (*Write Once, Run Anywhere - WORA*). 

---

## **2. Cài Đặt Java**  
### **Bước 1: Cài đặt JDK (Java Development Kit)**  
- Tải JDK mới nhất từ [Oracle](https://www.oracle.com/java/) hoặc [OpenJDK](https://openjdk.org/).  

### **Bước 2: Thiết lập biến môi trường**  
```bash
export JAVA_HOME=/path/to/jdk
export PATH=$JAVA_HOME/bin:$PATH
```
---

## **3. Chương Trình "Hello World" Đầu Tiên**
```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```
### **Cách chạy chương trình**
- javac HelloWorld.java   # Biên dịch
- java HelloWorld         # Chạy chương trình

---

## **4. Các Thành Phần Chính Trong Java**
### **4.1. Biến và Kiểu Dữ Liệu**
- Nguyên thủy: int, float, char, boolean, ...
- Tham chiếu: Class, Object, Array.
```java
int age = 25;              // Số nguyên
double price = 10.5;       // Số thực
char grade = 'A';          // Ký tự
boolean isJavaFun = true;  // Boolean
```

### **4.2. Toán tử**
```java
int sum = 10 + 20;         // Toán tử cộng
int mod = 10 % 3;          // Toán tử chia lấy dư
boolean isEqual = (10 == 20); // So sánh
```

### **4.3 Cấu Trúc Điều Kiện**
```java
Copy code
if (age > 18) {
    System.out.println("Đủ tuổi.");
} else {
    System.out.println("Chưa đủ tuổi.");
}
```

### **4.4 Vòng Lặp**
```java
for (int i = 0; i < 5; i++) {
    System.out.println(i);
}

int i = 0;
while (i < 5) {
    System.out.println(i);
    i++;
}
```

## **5. Lập Trình Hướng Đối Tượng (OOP)**
### **5.1 Lớp Và Đối Tượng**
```java
class Animal {
    String name;
    int age;

    void speak() {
        System.out.println(name + " đang kêu.");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal cat = new Animal();
        cat.name = "Mèo";
        cat.age = 2;
        cat.speak(); // Mèo đang kêu.
    }
}
```

### **5.2 Tính Kế Thừa**
```java
class Animal {
    void eat() {
        System.out.println("Đang ăn...");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Sủa...");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.eat();  // Đang ăn...
        dog.bark(); // Sủa...
    }
}
```
### **5.3 Tính Đa Hình**
```java
class Animal {
    void speak() {
        System.out.println("Động vật phát ra âm thanh.");
    }
}

class Dog extends Animal {
    @Override
    void speak() {
        System.out.println("Chó sủa.");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal animal = new Dog();
        animal.speak(); // Chó sủa.
    }
}
```

## **6. Các Chủ Đề Nâng Cao Trong Java**
### **6.1 Xử Lý Ngoại Lệ**
```java
try {
    int result = 10 / 0;
} catch (ArithmeticException e) {
    System.out.println("Lỗi chia cho 0: " + e.getMessage());
} finally {
    System.out.println("Khối finally luôn được thực thi.");
}
```

### **6.2 Luồng (Thread)**
```java
class MyThread extends Thread {
    public void run() {
        System.out.println("Luồng đang chạy...");
    }
}

public class Main {
    public static void main(String[] args) {
        MyThread t = new MyThread();
        t.start();
    }
}
```

### **6.3 Stream API**
```java
import java.util.*;
import java.util.stream.*;

public class Main {
    public static void main(String[] args) {
        List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5);
        numbers.stream()
            .filter(n -> n % 2 == 0)
            .forEach(System.out::println);
    }
}
```
## **7. Lời Kết**
- Java là ngôn ngữ mạnh mẽ, phổ biến và dễ học cho cả người mới bắt đầu lẫn lập trình viên chuyên nghiệp. Việc nắm vững các khái niệm từ cơ bản đến nâng cao sẽ giúp bạn phát triển các ứng dụng mạnh mẽ và linh hoạt.