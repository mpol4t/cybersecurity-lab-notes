# Netcat — Reverse Shell ve Port Bağlantısı Notlarım

## Netcat nedir

Netcat, ağ bağlantısı kurmak ve portlar üzerinden veri gönderip almak için kullanılan bir araçtır.

Penetration testing sırasında en çok reverse shell almak için kullanılır.

---

## Reverse shell almak için listener başlatma

En sık kullandığım komut:

nc -lvnp 4444

Parametreler:

- l → listen mode
- v → verbose
- n → DNS çözümleme yapma
- p → port belirtme

Bu komut hedef makineden gelecek bağlantıyı bekler.

---

## Reverse shell alma süreci

Genelde şu şekilde kullanırım:

1. Önce listener başlatırım:
   
2. Hedef makinede reverse shell çalıştırırım

3. Bağlantı geldiğinde shell elde ederim

Örnek çıktı:

connect to [10.10.10.10] from [10.10.10.20]

Bu, shell aldığımı gösterir.

---

## Öğrendiklerim

- Reverse shell almak için kullanılır
- Hedef makine ile bağlantı kurmamı sağlar
- Penetration testing sürecinde çok önemli bir araçtır

---

## Not

CTF makinelerinde reverse shell almak için kullandım.
