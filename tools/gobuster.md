# Gobuster — Web Enumeration Notlarım

## Gobuster nedir

Gobuster, web sunucusunda gizli dizinleri ve sayfaları brute force yöntemiyle bulmak için kullandığım enumeration aracıdır.

Web penetration testing sürecinde attack surface keşfetmek için çok önemlidir.

---

## Ne zaman kullanırım

Nmap sonucunda şu portları görürsem Gobuster kullanırım:

80/tcp open http
443/tcp open https

Çünkü bu bir web uygulaması olduğunu gösterir.

---

## Temel kullanım komutum

gobuster dir -u http://<TARGET_IP> -w <WORD LIST>

Parametre açıklamaları:

- dir → directory brute force mode
- -u → target URL
- -w → wordlist

---

## Gerçek kullanım örneği

gobuster dir -u http://10.10.10.10 -w /usr/share/wordlists/dirb/common.txt

Örnek çıktı:

/admin
/uploads
/login
/backup

---

## Bu dizinleri bulduktan sonra yaptıklarım

Bulduğum dizinleri manuel olarak incelerim:

Örnek:

http://10.10.10.10/admin
http://10.10.10.10/uploads
Şunları kontrol ederim:

- login panel var mı
- file upload var mı
- hassas dosyalar var mı
- admin panel var mı

---

## Gerçek senaryoda nasıl kullandım

CTF makinelerinde Gobuster kullanarak:

- admin panel buldum
- upload panel buldum
- login sayfası buldum

Bu sayfalar üzerinden exploit geliştirme imkanı elde ettim.

---

## Öğrendiklerim

- Web enumeration çok kritiktir
- Gizli dizinler genellikle entry point olur
- Gobuster attack surface keşfetmek için çok etkilidir

---
