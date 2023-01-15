# Gediz-Elektrik-POWER-OUTAGE
![image](https://user-images.githubusercontent.com/64266044/212553242-2556ba31-a091-4ea3-9418-8a9885b271a9.png)

* Elektrik Dağıtım Sektörünü düzenleyen Enerji Piyasası Düzenleme Kurulu (EPDK)’ca hazırlanan “Elektrik Dağıtım Şirketlerinin Satın alma ve Satış İşlemleri Uygulama Yönetmeliği”nde belirtilen hizmet standartlarına göre Elektrik Dağıtım Şirketleri, elektrik kesintisi olması durumunda hizmetin tekrar sağlanmasından sorumlu olup, kesintinin ilgili limitler dahili dışında devam etmesi halinde cezai yaptırımlarla karşı karşıya kalmaktadır.Bu kapsamda Elektrik Dağıtım Şirketleri, kesintinin anında ve/veya hızlı tespiti için çeşitli prosedürler geliştirmiş ve geliştirmektedir. Kesinti tespiti için kullanılan prosedürlerden bir tanesi de Çağrı Merkezleridir. Çağrı Merkezleri 7/24 üzerinden 3 vardiya olarak kesintisiz hizmet vermektedirler.

* Bu repository, Oluşan plansız kesintinin kaç adet çağrı merkezi çağrısına neden olacağını tahminlemek.Böylelikle kesintilere daha hızlı ve etkili bir şekilde önlem alınabilecek. 

### Data Description

  `KOD_NO(Outage ID)`: CRM - Müşteri/abonenin aramalarını karşılayan sorumlu tarafından alınan çağrıya istinaden TSKS sisteminde açılan kesinti kaydına atanan benzersiz(unique) numaradır.

  `İL`: Kesinti kaydının açıldığı şehri belirtir.

  `İLÇE`: Kesinti kaydının açıldığı ilçeyi belirtir.

  `ŞEBEKE_UNSURU`: Kesinti kaydı açılırken kesintinin olduğu şebeke unsurunu belirtir.

  `ŞEBEKE_UNSURU_KODU`: Kesinti kaydı açılırken kesintinin olduğu şebeke unsuru kodudur.

  `KESİNTİNEDENİNEİLİŞKİN_AÇIKLAMA`: Açılan kesinti kaydında liste içerisinden CRM sorumlusu tarafından seçilen kesinti nedenidir.

  `KAYNAĞA_GÖRE`: Kesintinin yaşandığı hattın tipini belirtir. Dağıtım-OG / Dağıtım-AG / İletim seçenekleri arasından seçilir.

  `SÜREYE_GÖRE`: Belirlenmiş kısıta istinaden, kesinti süresinin uzun/kısa olduğunu belirtir.

  `SEBEBE_GÖRE`: Dışsal / Güvenlik / Şebeke İşletmecisi seçeneklerinden seçilir.

  `BİLDİRİME_GÖRE`: Kesinti kaydının oluşturulurken çağrı ile bildirilerek veya bildirilmeden kaydının açıldığını belirtir.

  `BAŞLAMA_TARİHİ_VE_ZAMANI`: Kesinti kaydının TSKS sisteminde kaydının açıldığı ve kesintinin başladığını belirten tarih/saattir.

  `SONA_ERME_TARİHİ_VE_ZAMANI`: Kesinti kaydı adına açılan iş emrinin INFOR EAM'de atanan saha ekibi tarafından kapatıldığı tarih/saati belirtir.

  `KESİNTİ_SÜRESİ`: Matematiksel olarak "SONA_ERME_TARİHİ_VE_ZAMANI" - "BAŞLAMA_TARİHİ_VE_ZAMANI"'dır. Kesintinin açıldıktan sonra ilgili kesinti adına INFOR EAM'de açılan iş emrinin kapatıldığı an arasında geçen süreyi saat cinsinden belirten değerdir.

  `KENTSEL_OG`:Tüm illerin merkez mahalleleri ile 2020 yılı TÜİK tarafından açıklanan nüfus verilerine göre nüfusu 50 000 (elli bin) ve üzerinde olan ilçelerin merkez mahallelerinin orta gerilim kesinti hat sayısı.

  `KENTSEL_AG`:Tüm illerin merkez mahalleleri ile 2020 yılı TÜİK tarafından açıklanan nüfus verilerine göre nüfusu 50 000 (elli bin) ve üzerinde olan ilçelerin merkez mahallelerinin alçak gerilim kesinti hat sayısı.

  `KENTALTI_OG`:Kentsel olmayan ilçelerin merkez mahallleri ile 2020 yılı TÜİK tarafından açıklanan nüfus verilerine göre nüfusu 2 000 (iki bin) ve üzerinde olan mahallelerinin orta gerilim kesinti hat sayısı.

  `KENTALTI_AG`:Kentsel olmayan ilçelerin merkez mahallleri ile 2020 yılı TÜİK tarafından açıklanan nüfus verilerine göre nüfusu 2 000 (iki bin) ve üzerinde olan mahallelerinin alçak gerilim kesinti hat sayısı.

  `KIRSAL_OG`:Kentsel olmayan ilçelerin merkez mahallleri ile 2020 yılı TÜİK tarafından açıklanan nüfus verilerine göre nüfusu 2 000 (iki bin)in altında olan mahallelerinin orta gerilim hat sayısı.

  `KIRSAL_AG`:Kentsel olmayan ilçelerin merkez mahallleri ile 2020 yılı TÜİK tarafından açıklanan nüfus verilerine göre nüfusu 2 000 (iki bin)in altında olan mahallelerinin alçak gerilim hat sayısı.

  `TOPLAM_KENTSEL_OG`:Birimi saattir.Tüm illerin merkez mahalleleri ile 2020 yılı TÜİK tarafından açıklanan nüfus verilerine göre nüfusu 50 000 (elli bin) ve üzerinde olan ilçelerin merkez mahallelerinin orta gerilim kesinti hatlarındaki toplam kesinti süresi.

  `TOPLAM_KENTSEL_AG`:Birimi saattir.Tüm illerin merkez mahalleleri ile 2020 yılı TÜİK tarafından açıklanan nüfus verilerine göre nüfusu 50 000 (elli bin) ve üzerinde olan ilçelerin merkez mahallelerinin alçak gerilim kesinti hatlarındaki toplam kesinti süresi.

  `TOPLAM_KENTALTI_OG`:Birimi saattir.Kentsel olmayan ilçelerin merkez mahallleri ile 2020 yılı TÜİK tarafından açıklanan nüfus verilerine göre nüfusu 2 000 (iki bin) ve üzerinde olan mahallelerinin orta gerilim kesinti hatlarındaki toplam kesinti süresi.

  `TOPLAM_KENTALTI_AG`:Birimi saattir.Kentsel olmayan ilçelerin merkez mahallleri ile 2020 yılı TÜİK tarafından açıklanan nüfus verilerine göre nüfusu 2 000 (iki bin) ve üzerinde olan mahallelerinin alçak gerilim kesinti hatlarındaki toplam kesinti süresi.

  `TOPLAM_KIRSAL_OG`:Birimi saattir.Kentsel olmayan ilçelerin merkez mahallleri ile 2020 yılı TÜİK tarafından açıklanan nüfus verilerine göre nüfusu 2 000 (iki bin)in altında olan mahallelerinin orta gerilim kesinti hatlarındaki toplam kesinti süresi.

  `TOPLAM_KIRSAL_AG`:Birimi saattir.Kentsel olmayan ilçelerin merkez mahallleri ile 2020 yılı TÜİK tarafından açıklanan nüfus verilerine göre nüfusu 2 000 (iki bin)in altında olan mahallelerinin alçak gerilim kesinti hatlarındaki toplam kesinti süresi.

  `Cagri_Count`: Kesintinin neden olduğu çağrı sayısı




### Dikkate Alınan Değerlendirme Metrigi
** RMSE
![image](https://user-images.githubusercontent.com/64266044/212553191-dc3360f7-c6a4-4fe1-9931-9214a6235664.png)
