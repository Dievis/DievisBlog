---
title: Làm việc với DOM trong JavaScript
date: 2024-12-15
author: Đạt TP
description: Hướng dẫn về DOM trong JavaScript
tags:
  - JavaScript
  - DOM Manipulation
---

# **Làm việc với DOM trong JavaScript**

## **1. Chọn phần tử DOM**
```javascript
let element = document.getElementById('demo');
```

## **2. Thay đổi nội dung**
```javascript
element.innerHTML = 'Hello DOM!';
```

## **3. Tạo phần tử mới**
```javascript
let newElement = document.createElement('p');
newElement.textContent = 'Thêm đoạn văn mới';
document.body.appendChild(newElement);
```

## **4. Kết luận**
DOM là công cụ mạnh mẽ để thao tác và tương tác với trang web.
