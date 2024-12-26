---
title: Emoji Support
date: 2023-02-01
author: Hugo Authors
description: Guide to emoji usage in Hugo
tags:
  - emoji
---

Emoji can be enabled in a Hugo project in a number of ways. 
<!--more-->
The [`emojify`](https://gohugo.io/functions/emojify/) function can be called directly in templates or [Inline Shortcodes](https://gohugo.io/templates/shortcode-templates/#inline-shortcodes). 

To enable emoji globally, set `enableEmoji` to `true` in your site's `hugo.toml`. You can type emoji shorthand codes directly in content files; e.g.

`:see_no_evil:` :see_no_evil: `:hear_no_evil:` :hear_no_evil: `:speak_no_evil:` :speak_no_evil:

I :heart: Hugo! 😁

The [Emoji cheat sheet](http://www.emoji-cheat-sheet.com/) is a useful reference for emoji shorthand codes.

***

**N.B.** The above steps enable Unicode Standard emoji characters and sequences in Hugo, however the rendering of these glyphs depends on the browser and the platform. To style the emoji you can either use a third party emoji font or a font stack; e.g.

{{< highlight css >}}
.emoji {
  font-family: Apple Color Emoji, Segoe UI Emoji, NotoColorEmoji, Segoe UI Symbol, Android Emoji, EmojiSymbols;
}
{{< /highlight >}}

{{< css.inline >}}
<style>
.emojify {
	font-family: Apple Color Emoji, Segoe UI Emoji, NotoColorEmoji, Segoe UI Symbol, Android Emoji, EmojiSymbols;
	font-size: 2rem;
	vertical-align: middle;
}
@media screen and (max-width:650px) {
  .nowrap {
    display: block;
    margin: 25px 0;
  }
}
</style>
{{< /css.inline >}}

# Giới Thiệu về Java  

Java là một ngôn ngữ lập trình mạnh mẽ và đa nền tảng, được phát triển bởi **Sun Microsystems** (hiện nay thuộc sở hữu của Oracle). Với triết lý **"Write Once, Run Anywhere" (WORA)**, Java trở thành lựa chọn phổ biến cho phát triển phần mềm trên mọi nền tảng.

---

## Đặc Điểm Nổi Bật  

### **1. Độc lập nền tảng**  
- Java chạy trên mọi hệ điều hành thông qua **Java Virtual Machine (JVM)**.  
- Không cần biên dịch lại mã nguồn cho các nền tảng khác nhau.

### **2. Hướng đối tượng**  
- Hỗ trợ đầy đủ các tính năng như **kế thừa**, **đa hình**, và **đóng gói**.  
- Giúp tái sử dụng mã và phát triển ứng dụng phức tạp dễ dàng hơn.

### **3. An toàn và bảo mật**  
- Java có một môi trường runtime an toàn.  
- Quản lý bộ nhớ tự động bằng **Garbage Collector**.  

### **4. Hiệu năng cao**  
- Sử dụng cơ chế **Just-In-Time Compilation (JIT)** để tăng tốc độ thực thi.  

### **5. Thư viện phong phú**  
- Hệ sinh thái lớn với hàng ngàn thư viện hỗ trợ từ cộng đồng.  

---

## Ứng Dụng  

Java được sử dụng rộng rãi trong các lĩnh vực như:  

| **Lĩnh vực**       | **Ứng dụng cụ thể**                            |  
|---------------------|-----------------------------------------------|  
| **Web Development** | Xây dựng website và ứng dụng web với Spring, Hibernate. |  
| **Mobile Apps**     | Phát triển ứng dụng Android.                  |  
| **Enterprise**      | Hệ thống lớn với Java EE, Spring Boot.        |  
| **Game Development**| Lập trình game với LibGDX, jMonkeyEngine.     |  

---

## Một Số Mã Nguồn Mẫu  

### **Hello World**  
```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
