---
title: Các Thuật Toán Cơ Bản trong Java
date: 2024-12-23
author: Đạt TP
description: Sơ lược về các thuật toán cơ bản trong Java
tags:
  - Java
  - Lập Trình
  - Hướng Dẫn
---

# Tổng quan
- **Java là một ngôn ngữ lập trình mạnh mẽ và phổ biến, cung cấp nhiều công cụ và thư viện hỗ trợ việc xây dựng và triển khai các thuật toán hiệu quả. Dưới đây là một số thuật toán cơ bản thường được sử dụng trong lập trình Java:**

## **1. Thuật Toán Sắp Xếp**
- **Các thuật toán sắp xếp giúp tổ chức dữ liệu theo một thứ tự nhất định (tăng dần hoặc giảm dần). Một số thuật toán phổ biến:**

### **Bubble Sort (Sắp xếp nổi bọt):**

```java
public void bubbleSort(int[] arr) {
    int n = arr.length;
    for (int i = 0; i < n - 1; i++) {
        for (int j = 0; j < n - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                int temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
        }
    }
}
```
### **Quick Sort (Sắp xếp nhanh):**

```java
public void quickSort(int[] arr, int low, int high) {
    if (low < high) {
        int pi = partition(arr, low, high);
        quickSort(arr, low, pi - 1);
        quickSort(arr, pi + 1, high);
    }
}

private int partition(int[] arr, int low, int high) {
    int pivot = arr[high];
    int i = (low - 1);
    for (int j = low; j < high; j++) {
        if (arr[j] <= pivot) {
            i++;
            int temp = arr[i];
            arr[i] = arr[j];
            arr[j] = temp;
        }
    }
    int temp = arr[i + 1];
    arr[i + 1] = arr[high];
    arr[high] = temp;
    return i + 1;
}
```
## **2. Thuật Toán Tìm Kiếm**
- **Giúp tìm kiếm giá trị trong một tập dữ liệu.**

### **Tìm Kiếm Tuyến Tính (Linear Search):**

```java
public int linearSearch(int[] arr, int key) {
    for (int i = 0; i < arr.length; i++) {
        if (arr[i] == key) {
            return i;
        }
    }
    return -1;
}
```

### **Tìm Kiếm Nhị Phân (Binary Search):**

```java
public int binarySearch(int[] arr, int key) {
    int low = 0, high = arr.length - 1;
    while (low <= high) {
        int mid = low + (high - low) / 2;
        if (arr[mid] == key)
            return mid;
        if (arr[mid] < key)
            low = mid + 1;
        else
            high = mid - 1;
    }
    return -1;
}
```
## **3. Thuật Toán Đồ Thị**
- **Java cung cấp các cấu trúc dữ liệu như HashMap và ArrayList để hỗ trợ các thuật toán đồ thị:**

### **Dijkstra (Tìm đường đi ngắn nhất):**
```java
public void dijkstra(int graph[][], int src) {
    int V = graph.length;
    int[] dist = new int[V];
    boolean[] sptSet = new boolean[V];

    for (int i = 0; i < V; i++) {
        dist[i] = Integer.MAX_VALUE;
        sptSet[i] = false;
    }
    dist[src] = 0;

    for (int count = 0; count < V - 1; count++) {
        int u = minDistance(dist, sptSet);
        sptSet[u] = true;

        for (int v = 0; v < V; v++) {
            if (!sptSet[v] && graph[u][v] != 0 &&
                dist[u] != Integer.MAX_VALUE &&
                dist[u] + graph[u][v] < dist[v]) {
                dist[v] = dist[u] + graph[u][v];
            }
        }
    }
    printSolution(dist);
}

private int minDistance(int[] dist, boolean[] sptSet) {
    int min = Integer.MAX_VALUE, minIndex = -1;
    for (int v = 0; v < dist.length; v++) {
        if (!sptSet[v] && dist[v] <= min) {
            min = dist[v];
            minIndex = v;
        }
    }
    return minIndex;
}

private void printSolution(int[] dist) {
    System.out.println("Vertex \t Distance from Source");
    for (int i = 0; i < dist.length; i++)
        System.out.println(i + " \t " + dist[i]);
}
```
## **4. Thuật Toán Đệ Quy**
- **Đệ quy là một phần không thể thiếu trong nhiều bài toán:**

### **Tính Giai Thừa:**
```java
public int factorial(int n) {
    if (n == 0)
        return 1;
    return n * factorial(n - 1);
}
```

### **Dãy Fibonacci:**
```java
public int fibonacci(int n) {
    if (n <= 1)
        return n;
    return fibonacci(n - 1) + fibonacci(n - 2);
}
```
# **Kết Luận**
- **Các thuật toán trên là nền tảng để giải quyết nhiều bài toán từ cơ bản đến nâng cao. Java cung cấp nhiều công cụ và thư viện hỗ trợ, giúp bạn triển khai các thuật toán một cách hiệu quả và dễ dàng hơn. Hãy thực hành để hiểu sâu và làm chủ các thuật toán này!**