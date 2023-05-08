# Gediz-Elektrik-POWER-OUTAGE
![image](https://user-images.githubusercontent.com/64266044/212553242-2556ba31-a091-4ea3-9418-8a9885b271a9.png)

Bu Repository Kaggle da girdiğim  `Gediz-Elektrik-POWER-OUTAGE` yarışmadaki çözümümü içermektedir.Problemimiz Gediz Elektriğin hizmet verdiği İzmir ve Manisa bölgelerinde oluşabilecek plansız kesintilerin kaç adet çağrıya neden olabileceğini tahminlemek.Problemimiz Regression problemi. Train verisi '2022-03-24' Tarihine kadar olan kısım kullanildi.

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

* RMSE/MSE

*  Kök Ortalama Kare Hatası (Root Mean Squared Error (RMSE)) / Ortalama Kare Hatası (Mean Squared Error (MSE)) 
* Ortalama Kare Hatası tahmin edilen sonuçlarınızın gerçek sayıdan ne kadar farklı olduğuna dair size mutlak bir sayı verir. Tek bir sonuçtan çok fazla içgörü yorumlayamazsınız, ancak size diğer model sonuçlarıyla karşılaştırmak için gerçek bir sayı verir ve en iyi regresyon modelini seçmenize yardımcı olur. Kök Ortalama Karekök Hatası (RMSE), MSE’nin kareköküdür. MSE’den daha sık kullanılır çünkü bazen MSE değeri kolayca karşılaştırılamayacak kadar büyük olabilir. Bu yüzden MSE hata karesi ile hesaplanır ve böylece yorumlamayı kolaylaştırır. Fakat MSE aykırı değerlere karşı çok duyarlıdır.


![image](https://user-images.githubusercontent.com/64266044/212553538-bbeb1ce0-3516-40a2-a58a-5c32fb836ac2.png)
