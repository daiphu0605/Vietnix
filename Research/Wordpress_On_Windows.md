# Cài đặt Wordpress trên Windows Server 2012

## Source Wordpress

[Link tải source wordpress](https://vi.wordpress.org/latest-vi.zip)

## Source PHP74

[Link tải source php 7.4](https://windows.php.net/downloads/releases/php-7.4.33-Win32-vc15-x64.zip)

PHP dành cho Windows có 02 lựa chọn chính là NTS và TS.

* NTS: non-thread-safe chạy đơn luồng.
* TS: thread-safe chạy nhiều luồng.

## Source PHP Manager for IIS

[Link tải phần mở rộng PHP Manager cho IIS](https://objects.githubusercontent.com/github-production-release-asset-2e65be/143063767/a360b6c5-93c8-431a-bde5-f38f30878b04?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=releaseassetproduction%2F20250317%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250317T070557Z&X-Amz-Expires=300&X-Amz-Signature=d83f306ee55d27efdf4d55fc4cb022406b78ff0967765b77a53cbd6d5145bbfa&X-Amz-SignedHeaders=host&response-content-disposition=attachment%3B%20filename%3DPHPManagerForIIS_x64.msi&response-content-type=application%2Foctet-stream)

PHP Manager là phần mở rộng của IIS, cho phép cấu hình PHP, quản lý PHP và chạy PHP.

## Source MariaDB 8.4

[Link tải MariaDB](https://cdn.mysql.com//Downloads/MySQL-8.4/mysql-8.4.4-winx64.zip)

## Source OpenSSL

[Link tải OpenSSL](https://slproweb.com/download/Win64OpenSSL_Light-3_4_1.exe)

Lưu ý: OpenSSL 3.x sử dụng mã hóa AES256 khi chuyển đổi file crt sang pfx nên khi import file pfx trên Windows Server 2012 sẽ luôn báo sai mật khẩu. Để khắc phục lỗi này sẽ phải chạy câu lệnh chuyển đổi file như sau:

```powershell-interactive
openssl pkcs12 -export -cerpbe PBE-SHA1-3DES -keypbe PBE-SHA1-3DES -nomac -out certicate.pfx -inkey private.key -in certicate.crt -certfile -ca_bundle.crt
```
