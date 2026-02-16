# Burp Suite — Web Traffic Analizi Notlarım

## Burp Suite nedir

Burp Suite, web uygulamaları ile tarayıcı arasındaki HTTP trafiğini analiz etmek için kullanılan bir araçtır.

Web penetration testing için çok önemlidir.

---

## Ne için kullanırım

Burp Suite ile şunları yapabilirim:

- HTTP request ve response incelemek
- Web uygulamasının nasıl çalıştığını anlamak
- Login işlemlerini analiz etmek

---

## Temel kullanım

Tarayıcıyı Burp proxy üzerinden geçiririm.

Sonra web sitesine girdiğimde Burp Suite requestleri yakalar.

Örnek:

GET /login HTTP/1.1
Host: target.com

Bu sayede web uygulamasının nasıl çalıştığını analiz edebilirim.

---

## Öğrendiklerim

- Web trafiğini analiz etmeyi
- HTTP request yapısını anlamayı
- Web uygulamasını analiz etmeyi

---

## Not

CTF makinelerinde web enumeration aşamasında kullandım.
