## CONTRIBUTION TEST

### Membuat 2 remote atau lebih dalam 1 machine

#### 1. Buat SSH Key dan letakkan didalam folder .ssh

ssh-keygen -t rsa -C "gotipes@gmail.com" -f gotipes
ssh-keygen -t rsa -C "andri1.workspace@gmail.com" -f andri1.workspace

#### 2. Buat file config di dalam folder .ssh dan tuliskan

Host gotipes github.com
    HostName github.com
    PreferredAuthentications publickey
    IdentityFile ~/.ssh/gotipes

Host andri1workspace github.com
    HostName github.com
    PreferredAuthentications publickey
    IdentityFile ~/.ssh/andri1workspace

#### 3. Lakukan **remote** atau **clone** di repo yg akan di fork

git clone git@`Hostname`:gotipes/contribution-test.git
git clone git@gotipes:gotipes/contribution-test.git

git remote add origin git@`Hostname`:gotipes/contribution-test.git
git remote add origin git@gotipes:gotipes/contribution-test.git


Jika push rejected buka `Credential Manager > Windows Credentials` kemudian hapus git