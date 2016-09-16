---
layout: post
title: Project Shield ve DDoS?
---


İlk olarak Google Project Shield’ın ne olduğu ile başlayalım. Google Ideas tarafından ilk olarak ortaya çıkan bu proje bağımsız internet haber sitelerini, sivil toplum kuruluşlarının sayfalarını ve seçim sonuçlarını paylaşan web sayfaları gibi kritik olan mecraları DDoS ataklarından korumayı amaçlıyor. Peki bunu nasıl yapıyor?
TrendMicro araştırmalarına göre internetin karanlık tarafından tam bir hafta sürecek bir DDoS saldırısına sadece 150 dolara almak mümkün. Eğer paylaşımlı bir hosting kullanıyorsanız çok hafif bir DDoS saldırısında sitenizin erişiminin kesilmesi içten bile değil. DDoS hakkında detaylıca bahsetmeyeceğim, fakat yüzeysel olarak buradan önemli bilgiler öğrenmek mümkün.

Google Project Shield’ı kendi web sayfam olan inceleme.co’da yaklaşık 1 haftadır deneyimliyorum ve paylaşımlı hosting kullanmamama rağmen bazen sebepsiz yere azda olsa bu tip saldırılara maruz kalıyordum, her ne kadar siteye erişim kesilmesede ilerleyen zamanlarda trafiğim arttıkça, sitede anlık olan ziyaretçi sayısıda artacağından bu servisin bana fayda sağlayacağını biliyorum.
Şu anda sadece başvuru toplayan Project Shield tamamen ücretsiz, başvurularınızı ise bu linkten yapabilirsiniz. Başvurunuzdan 1–2 hafta sonra onay e-postası geliyor ve gerekli ayarlamaları yapıyorsunuz. Eğer bare domain, yani alan adınızın başında www. kullanmıyorsanız CNAME kaydının yanı sıra A adres kaydınızı da Google’ın IP’si ile değiştirmelisiniz.

Project Shield, web sayfanızda bulunan 64 MB’tan küçük dosyalarınızın tamamını önbellekleyerek kullanıcıların ve saldırıların Google’ın altyapısında bulunan sunuculara yönlenmesini sağlıyor. Daha önce Google’ın DDoS saldırıları yüzünden erişime kapanmadığını söylemeliyim. :)
Aynı zamanda bu servisi kullandığınız zaman gerçek IP adresinizde saklanmış oluyor. Şu anda inceleme.co’nun IP adresi Google tarafında gözüküyor ki bu da direkt olarak sunucuza yapılacak saldırılara önlem anlamına geliyor. Eğer siteniz Project Shield’e seçilmez ise CloudFlare’ı sadece bu IP gizleme olayı yüzünden bile kullanmanızı tavsiye ediyorum. CloudFlare + Project Shield’ı ücretsiz CloufFlare hesabında kullanamıyorsunuz, bunu da belirtmeliyim.

Project Shield kullanıcı paneli oldukça sadece ve kullanımı kolay olan bu ekran üzerinden sitenize saniyede kaç istek yapıldığını görebiliyorsunuz, zaten başka da bir bölüm bulunmuyor. Açıkçası bu istatislikleri belirli gün ve ay olarak görmek isterdim, fakat şu anda sadece son 1 saat ve 30 gün aralığını görebiliyoruz.

Ve gelelim gerçekten işe yarayıp yaramadığına. Loader.io’nun ücretsiz testiyle saniyede 10.000 kullanıcının istek gönderdiği ve bir dakika süren test sonuçlarına aşağıdan ulaşabilirsiniz. Bu sırada sunucumun nload komutunun ekran görüntüsünü de ekliyorum. Ekran görüntüsü sizi şaşırtmasın. :)

Loader.io’dan test yaptığım saatin Project Shield’a yansıması.

![_config.yml]({{ site.baseurl }}/images/6.png)

Received by clients: 36.9 GB. Bütün istekler başarılı.
Yorumlarınızı ve benzer deneyimlerinizi merakla bekliyorum. :)
