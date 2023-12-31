# Mengatasi Error / fix Github Error: Permission denied (publickey)

⛔ Tidak bisa push / clone dari local ke github dan sebaliknya

⚠️ Kasus ini terjadi pada OS Windows dengan menggunakan WSL



## ▶️ How to Fix?

<pre>
  <code class="language-java">
   git config --global --unset core.excludesfile
  </code>
</pre>

<pre>
  <code class="language-java">
    git config --global --unset user.name
  </code>
</pre>

<pre>
  <code class="language-java">
    git config --global --unset user.email
  </code>
</pre>

<pre>
  <code class="language-java">
    git config --global user.name "USER KAMU"
  </code>
</pre>

<pre>
  <code class="language-java">
    git config --global user.email "emailkamu@gmail.com"
  </code>
</pre>



## ▶️ Get SSH-KEYGEN
<pre>
  <code class="language-java">
    ssh-keygen
  </code>
</pre>



## ▶️ Terminal akan menampilkan lokasi keygen yang akan di generate
```
Generating public/private rsa key pair.
Enter file in which to save the key (/home/user/.ssh/id_rsa): 
```
<code>(/home/user/.ssh/id_rsa)</code> Merupakan Lokasi key yang akan kita pakai dikemudian

Terminal akan berlanjut menampilkan:
```
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
```
Kosongkan saja atau tekan enter

```
Your identification has been saved in /home/user/.ssh/id_rsa
Your public key has been saved in /home/user/.ssh/id_rsa.pub
```
<code>id_rsa.pub</code> Merupakan File yang akan kita buka melalui Powershell Windows



## ▶️ Buka Powershell Windows
pindah ke direktori lokasi keygen, pada kasus ini ubuntu kami menggunakan WSL
```
cd  \\wsl.localhost\Ubuntu\home\user\.ssh
```
Lanjutkan Perintah
```
Get-Content id_rsa.pub | Set-Clipboard
```
Keygen akan tersimpan pada Clipboard anda, silahkan anda paste di Notepad anda

## Lanjut Buka Github
Buka Settings > SSH & GPG Keys

![App Screenshot](https://github.com/arka-p/errorlog/blob/main/Image01)

Isikan Judul dan masukan keygen yang telah di dapat

kemudian coba kembali push / clone dari local ke github dan sebaliknya
