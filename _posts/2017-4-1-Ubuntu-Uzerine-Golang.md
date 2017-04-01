---
layout: post
title: Ubuntu üzerine Go 1.8 nasıl kurulur?
---

Ubuntu sunucumuza Go (Golang) kurmamız için öncelikle makinemize ssh bağlantımızın olması gerekiyor. Suncuumuza SSH ile bağlandıktan sonra paketleri ve güvenlik güncellemelerini alarak başlamanızı tavsiye ederim.

```sh
$ sudo apt-get update
$ sudo apt-get -y upgrade
```

Bunu yaptıktan sonra curl komutu ile Golang'ın 1.8 sürümünü sunucumuza alabiliriz. En son sürümleri de buradan kontrol edebilirsiniz: https://golang.org/dl/

```sh
$ sudo curl -O sudo curl -O https://storage.googleapis.com/golang/go1.8.linux-amd64.tar.gz
```
Gördüğünüz gibi indirdiğimiz dosya .tar formatında sıkıştırılmış bir formatta. Aşağıdaki komutlar Tar aracının çalışıp paket adında bir dosya yaratmasına ardından da bu dosyayı /usr/local konumuna taşıyacak.

```sh
$ sudo tar -xvf go1.8.linux-amd64.tar.gz
$ sudo mv go /usr/local
```

# Ve gelelim Go yazılım dilinin path ayarlarını yapmaya.

Aşağıdaki komut Go'nun root değerini belirtleyerek Go'ya dosyalarının yerini belirtecek.

```sh
$ sudo nano ~/.profile
```

Açılan editörde en alt satıra

```sh
export PATH=$PATH:/usr/local/go/bin
```

ekleyerek dosyayı kaydedip kapatabilirsiniz.

Yaptığınız değişikliklerden sonra alttaki konutu çalıştırarak profilleri yenileyebilirsiniz.

```sh
$ source ~/.profile
```

Bu şekilde sunucumuza Go 1.8 sürümünü başarıyla kurmuş ve ayarlarını yapmış bulunuyoruz.
