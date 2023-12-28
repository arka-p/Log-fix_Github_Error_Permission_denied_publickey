# Mengatasi Error / fix Github Error: Permission denied (publickey)

⛔ Tidak bisa push / clone dari local ke github

## How to Fix?

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

## Lanjutkan Untuk mendapatkan SSH
<pre>
  <code class="language-java">
    ssh-keygen
  </code>
</pre>

## Terminal akan menampilkan lokasi keygen yang akan di generate
```
Generating public/private rsa key pair.
Enter file in which to save the key (/home/user/.ssh/id_rsa): 
```
(/home/user/.ssh/id_rsa): Merupakan Lokasi key yang akan kita pakai dikemudian

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
id_rsa.pub Merupakan File yang akan kita buka melalui Powershell Windos
