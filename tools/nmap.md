# Nmap — Network Enumeration Notlarım

## Nmap nedir

Nmap (Network Mapper), hedef sistemde açık portları, çalışan servisleri ve servis versiyonlarını tespit etmek için kullandığım temel enumeration aracıdır.

Bir makineyi hack etmeye çalışırken ilk yaptığım şeylerden biridir çünkü attack surface'i belirler.

---

## Temel kullanım akışım

Makine çözerken genelde şu adımları izlerim:

### 1. Tüm portları tarama

Varsayılan Nmap sadece ilk 1000 portu tarar. Bu yüzden ihtiyacım olduğunda tüm portları tararım:

nmap -p- <TARGET_IP>

Amaç:

- Gizli servisleri kaçırmamak
- SSH, HTTP, SMB, FTP gibi servisleri tespit etmek

---

### 2. Açık portlar için servis ve versiyon tespiti

Açık portları bulduktan sonra servis versiyonlarını öğrenirim:

nmap -sV -p  <TARGET_IP>

Örnek:
nmap -sV -p 22,80 10.10.10.10

Bu sayede:

- Apache versiyonu
- SSH versiyonu
- FTP versiyonu

gibi bilgiler elde ederim.

Bu bilgiler exploit ararken çok önemlidir.

---

### 3. Daha detaylı analiz

Daha fazla bilgi için:

nmap -A <TARGET_IP>

Bu komut:

- OS detection
- Version detection
- Script scanning
- Traceroute

yapar.

---

## Gerçek kullanım senaryom

Örnek çıktı:

PORT   STATE SERVICE VERSION
22/tcp open  ssh     OpenSSH 7.6p1
80/tcp open  http    Apache httpd 2.4.29

Bu durumda:

- 80 portu açıksa → web enumeration yaparım (Gobuster, source code analysis)
- 22 portu açıksa → brute force veya exploit araştırırım

---

## Öğrendiklerim

- Enumeration en kritik aşamadır
- Açık portlar attack surface'i belirler
- Servis versiyonları exploit bulmak için kullanılır
- Nmap olmadan sistem hakkında bilgi edinmek çok zordur

---




