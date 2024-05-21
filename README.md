# :warning: :exclamation: **For Educational Purposes Only** :exclamation::warning:

Disclaimer :
1. For educational purposes only.
2. Don't use them for illegal activities.
3. You alone are responsible for your actions :exclamation:

:see_no_evil: :hear_no_evil: :speak_no_evil: 
----------------------------------------------------------------------------------------------------------------------------
**TTL (Time To Live)**
<p align="justify">
Pernahkah anda menggunakan paket internet seluler unlimited ?, pasti beberapa dari anda pernah dengar dan membelinya. Provider internet seluler sering menggunakan konfigurasi pembatasan TTL yang bertujuan agar penggunanya tidak bisa melakukan pembagian akses internet ke perangkat lain. 
TTL merupakan sebuah nilai (8-bit) di header Internet Protocol (IP) oleh host pengirim yang nilainya akan selalu berkurang ketika router forwarding paket IP, range TTL dari 255 sampai 0. Jika paket ttl mencapai 0 maka kegiatan transfer paket dihentikan dan router mengirimkan pesan ICMP "time exceed message" ke pengirim awal. Sehingga menghentikan transfer paket pada  sebuah jaringan setelah beberapa waktu tertentu, hal ini dapat mengantisipasi terjadinya transfer paket data berulang terus menerus. 
</p>

**Check current TTL**
------------------------------------------------------------------------------------------------------------------------------

Windows - ping 127.0.0.1        or      ping IP address
  
macOS  - ping localhost

Linux - sysctl net.ipv4.ip_default_ttl

------------------------------------------------------------------------------------------------------------------------------
**Change TTL IPv4**
<ol>
  <li> Windows - run command shell on terminal as admin
    
    netsh int ipv4 set glob defaultcurhoplimit=65 
    
  </li>
  <li> Linux - execute this command in the console as temporary setting
  
    sudo sysctl -w net.ipv4.ip_default_ttl=65
                    or
    sudo bash -c 'echo 65 > /proc/sys/net/ipv4/ip_default_ttl'
            
  </li>
  
</ol>


------------------------------------------------------------------------------------------------------------------------------
**Default TTL** and **Hop Limit** values differ across various operating systems. Here are the defaults for a few:
<ol>
  <li>Linux: 64 for TCP, UDP, and ICMP</li>
  <li>Windows: 128 for TCP, UDP, and ICMP</li>
  <li>MacOS: 64 for TCP, UDP, and ICMP</li>


</ol>

Work in Progress........
