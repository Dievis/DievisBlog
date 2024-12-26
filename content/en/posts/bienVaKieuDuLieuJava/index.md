---
title: Biến và Kiểu dữ liệu trong Java
date: 2024-12-10
author: Đạt TP
description: Biến và Kiểu dữ liệu trong Java
tags:
  - Java
  - Lập Trình
  - Hướng Dẫn
---

# **Chuyên Sâu Về Biến và Kiểu Dữ Liệu Trong Java**
## **1. Biến Trong Java**
- Biến là tên đại diện cho một vùng nhớ được sử dụng để lưu trữ dữ liệu trong chương trình.

### **1.1. Các loại biến trong Java**
**Biến cục bộ (Local Variables):**
- Khai báo bên trong một phương thức, khối lệnh hoặc constructor.
- Chỉ có hiệu lực trong phạm vi khai báo.
- Không có giá trị mặc định, nên phải khởi tạo trước khi sử dụng.

```java
public class Example {
    void method() {
        int a = 10; // Biến cục bộ
        System.out.println(a);
    }
}
```

**Biến thành viên (Instance Variables):**
- Khai báo bên trong lớp nhưng ngoài các phương thức.
- Thuộc về một đối tượng cụ thể và có thể được truy cập qua đối tượng đó.
- Có giá trị mặc định dựa trên kiểu dữ liệu.

```java
class Student {
    String name; // Biến thành viên
    int age;     // Biến thành viên
}
```

**Biến tĩnh (Static Variables):**
- Khai báo với từ khóa static.
- Chia sẻ chung giữa tất cả các đối tượng của lớp.
- Tồn tại trong bộ nhớ heap.

```java
class Counter {
    static int count = 0; // Biến tĩnh
    Counter() {
        count++;
    }
}
```

## **2. Kiểu Dữ Liệu Trong Java**
### **2.1. Kiểu dữ liệu nguyên thủy (Primitive)**

  Kiểu	  | Kích thước | Giá trị mặc định   | Mô tả
----------|------------|--------------------|-------------------------------------------
  byte	  | 1 byte	   | 0	                | Số nguyên nhỏ (từ -128 đến 127).
  short	  | 2 bytes	   | 0	                | Số nguyên trung bình (-32,768 đến 32,767).
  int	  | 4 bytes	   | 0	                | Số nguyên lớn (-2^31 đến 2^31-1).
  long	  | 8 bytes	   | 0L	                | Số nguyên rất lớn (-2^63 đến 2^63-1).
  float	  | 4 bytes	   | 0.0f	            | Số thực dấu chấm động chính xác đơn.
  double  | 8 bytes	   | 0.0d	            | Số thực dấu chấm động chính xác kép.
  char	  | 2 bytes	   | 'abcd'	            | Ký tự Unicode.
  boolean | 1 bit	   | false	            | Giá trị logic (true hoặc false).


- Ví dụ:

```java
int age = 25;
double height = 5.9;
char grade = 'A';
boolean isPassed = true;
```

### **2.2. Kiểu dữ liệu tham chiếu (Reference)**
- Được sử dụng để lưu trữ địa chỉ của các đối tượng hoặc mảng.

- Ví dụ:

    - Chuỗi (String): Đại diện cho chuỗi ký tự.
    - Mảng (Array): Danh sách các phần tử cùng kiểu.
    - Lớp (Class): Tạo đối tượng tùy chỉnh.
    - Interface.


- Ví dụ:

```java
String name = "Java";
int[] numbers = {1, 2, 3, 4};
```

## **3. Ép Kiểu Dữ Liệu (Type Casting)**
### **3.1. Ép kiểu tường minh (Explicit Casting)**
- Chuyển từ kiểu dữ liệu lớn hơn về nhỏ hơn.

```java
double num = 10.5;
int value = (int) num; // Ép về int
```

### **3.2. Ép kiểu ngầm định (Implicit Casting)**
- Chuyển từ kiểu nhỏ hơn sang lớn hơn mà không cần chỉ định rõ ràng.

```java
int num = 10;
double value = num; // Tự động chuyển thành double
```

## **4. Hằng Số (Constants)**
- Hằng số là giá trị không thể thay đổi sau khi đã gán.
- Khai báo bằng từ khóa final.

```java
final double PI = 3.14159;
```

## **5. Lưu Trữ Bộ Nhớ Của Biến**
 Loại biến	           |   Bộ nhớ sử dụng	| Phạm vi truy cập
 ----------------------|--------------------|---------------------------
 Cục bộ (Local)	       | Stack	            | Chỉ trong phương thức hoặc khối lệnh.
 Thành viên (Instance) | Heap	            | Gắn với đối tượng của lớp.
 Tĩnh (Static)	       | Metaspace	        | Chia sẻ giữa các đối tượng.

## **6. Kết Luận**
- Biến và kiểu dữ liệu là nền tảng của lập trình Java. Việc hiểu sâu về chúng giúp lập trình viên viết mã hiệu quả, tránh lỗi và tối ưu hóa bộ nhớ. Java cung cấp nhiều tùy chọn linh hoạt từ kiểu nguyên thủy đến kiểu tham chiếu và hỗ trợ ép kiểu để chuyển đổi dữ liệu dễ dàng.