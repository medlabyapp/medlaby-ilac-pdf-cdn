# Medlaby İlaç Dokümantasyon Servisi (Asset Storage & CDN)

Bu depo, Medlaby sağlık teknolojileri projesinin geliştirme ve test süreçlerinde kullanılmak üzere yapılandırılmış bir statik içerik dağıtım ağı (CDN) ve veri depolama birimidir.

## Proje Tanımı ve Teknik Gereksinim

Bu depo, uygulama geliştirme süreçlerinde karşılaşılan yüksek boyutlu statik dosyaların (PDF) istemci tarafındaki (mobil/web) performans ve depolama sorunlarını optimize etmek amacıyla oluşturulmuştur. Temel işlevi, uygulama içi dosya çekme (fetch) protokollerinin ve dış kaynaklı dosya okuma mimarisinin simülasyonunu sağlamaktır.

Bu depo, son kullanıcıya (hasta, sağlık profesyoneli vb.) doğrudan bir tıbbi bilgi kaynağı sunmak amacıyla tasarlanmamıştır; yalnızca Medlaby yazılım mimarisi için teknik bir altyapı birimi olarak işlev görür.

## Dosya İsimlendirme ve Erişim Protokolü

Sistem, veritabanı entegrasyonu için 13 haneli GTIN (Global Trade Item Number) standardını referans alır.

| Doküman Tipi | İsimlendirme Formatı | Örnek |
| :--- | :--- | :--- |
| Kısa Ürün Bilgisi (KUB) | `{gtin}_kub.pdf` | `8699570150011_kub.pdf` |
| Kullanım Talimatı (KT) | `{gtin}_kt.pdf` | `8699570150011_kt.pdf` |

## HUKUKİ BEYAN VE SORUMLULUK REDDİ

Bu depoda yer alan içeriklere erişen veya bu içerikleri kullanan her kişi, aşağıdaki maddeleri peşinen kabul etmiş sayılır:

1. **Bilgi Kaynağı ve Geçerlilik:** Depoda bulunan KUB ve KT dosyaları, belirli bir tarihte açık kaynaklı verilerden (web scraping/crawling) derlenmiştir. Bu dosyaların güncelliği, eksiksizliği veya yasal geçerliliği hakkında hiçbir taahhüt verilmemektedir. İlaç bilgilerinde meydana gelen güncellemeler, mevzuat değişiklikleri veya toplatma kararları bu depoya anlık olarak yansıtılmayabilir.
2. **Resmi Merci Referansı:** İlaçlara dair en güncel ve yasal dokümanlara erişmek için tek yetkili mercii Türkiye İlaç ve Tıbbi Cihaz Kurumu (TİTCK) resmi internet sitesidir (titck.gov.tr).
3. **Tıbbi Tavsiye Niteliği:** Bu içerikler hiçbir koşulda tıbbi tavsiye, teşhis veya tedavi önerisi teşkil etmez. Herhangi bir tıbbi uygulama veya ilaç kullanımı öncesinde mutlaka uzman bir hekim veya eczacı ile görüşülmelidir.
4. **Mülkiyet Hakları:** Depoda barındırılan `.pdf` dosyalarının içerik, tasarım ve marka hakları ilgili ilaç ruhsat sahiplerine aittir. Bu depo, söz konusu belgeler üzerinde herhangi bir telif veya mülkiyet hakkı iddia etmez.
5. **Sorumluluk Sınırlandırması:** Geliştiriciler, repo sahipleri ve projeye katkıda bulunanlar; verilerin hatalı veya eksik kullanımından, dokümanların içeriğine dayanılarak yapılan işlemlerden doğabilecek doğrudan veya dolaylı hiçbir maddi, manevi, hukuki veya tıbbi zarardan sorumlu tutulamaz.

## Lisans

Repository altyapısı ve dizin kurgusu MIT Lisansı ile sunulmaktadır. İçerik dosyalarının mülkiyet hakları ilgili üçüncü taraf kurum ve kuruluşlara aittir.
