# Ansible temel elemanları:

* inventory

> Ansible'ın yöneteceği sunucu adları ve ya IP adreslerinin tanımlandığı dosya.

> /etc/ansible/host altında bulunur.

```
#> cat /etc/ansible/host/host.ini

[WEBsunuculari]
dev.sercangezer.com
www.sercangezer.com

[DBsunuculari]
DBdev.sercangezer.com
DBprod.sercangezer.com
```
* module

> Modüller bağımsız komut dosyasıdır.

* fact

> Sistem & Yazılım hakkında hedef bilgilerini almayı sağlar.

* play

> Ansible'da her bir görev `play` olarak adlandırılır.

* playbook

> Tüm görevlerin ve yapılandırmaların tanımlandığı dosyadır.

---
```
ansible all -a  "/sbin/reboot now" -b -K
```
-b  --> --become (Yöneticisi yetkisi al)
-K  --> --ask-become-pass (Yönetici parolasını sor)