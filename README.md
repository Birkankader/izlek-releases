# İzlek

Windows için Jira test inceleme panosu. Reporter’ı olduğunuz Story’lerin Test disiplinindeki görevlerini listeler. Story’ye bağlanan testleri, analiz görevindeki Confluence sayfasıyla karşılaştırır. Analiz maddeleri ile test adımlarını yan yana inceleyebilir, kapsam yüzdesini görebilir ve seçtiğiniz yorumları düzenleyerek Jira'ya gönderebilirsiniz.

**[Windows x64 için İzlek 0.3 sürümünü indir](https://github.com/Birkankader/izlek-releases/releases/download/v0.3/Izlek-0.3-windows-x64.exe)** · [Tüm sürümler](https://github.com/Birkankader/izlek-releases/releases)

0.1f ve önceki sürümleri kullanıyorsanız güncel EXE dosyasını bir kez elle indirin. İzlek’i yazabildiğiniz bir klasörden çalıştırın. Sonraki sürümler açılışta ve uygulama açıkken altı saatte bir GitHub üzerinden kontrol edilir. İzlek yayıncı imzasını ve dosyanın SHA-256 özetini doğruladıktan sonra güncellemeyi hazırlar. Açık incelemenize devam edebilir, **Şimdi yeniden başlat** düğmesini kullanabilir veya yeni sürüme bir sonraki açılışta geçebilirsiniz.

Mor temalı inceleme panosu uyum yüzdesini ve dört ayrı sütunu gösterir. Sütunlar sırasıyla **Eksik kapsam**, **Kısmi kapsam**, **Uç durumlar** ve **Karşılananlar** olarak düzenlenir. Karttaki **Sorun ve çözüm** bölümünden düzeltmeyi okuyabilir, **Yorumu incele** yan panelinde sorunlu test alanını görüp taslağı düzenleyebilirsiniz.

**Bağlantı ayarları → Tema** bölümünden **Açık** veya **Koyu** seçebilirsiniz. Her iki temada da ana renk mordur. İlk açılışta açık tema kullanılır. Seçiminiz anında uygulanır ve sonraki açılışlarda hatırlanır.

## Başlangıç

1. Windows 10/11 x64 üzerinde EXE dosyasını açın. Uygulama Microsoft Edge WebView2 Runtime kullanır. EXE dijital imzasızdır.
2. İlk ekranda Jira ve Confluence sunucularınızı girin. Kurum bağlantısı olmadan denemek için **Örnek panoyu aç** seçeneğini kullanabilirsiniz.
3. Data Center'da kişisel erişim tokenı, Cloud'da e-posta ve site adresiyle çalışan API tokenı girin. Cloud Confluence adresine `/wiki` yolunu ekleyin. Sunucular farklıysa iki token alanını da doldurun. Başarılı bağlantıdan sonra tokenlar Windows Kimlik Bilgisi Yöneticisi'nde saklanır. 0.1b veya önceki bir sürümden yükseltirken tokenları bir kez girin. Güncellemeden sonra ve sonraki açılışlarda görevleriniz kayıtlı hesapla otomatik açılır. Bağlantı kurulamazsa ayarlar hata nedenini gösterir.
4. **Görev sorgusu ve kurum alanları** altında Story sorgusunu, kayıt türlerini, disiplin alanını, ilişki adlarını ve varsa test adımı özel alanlarını ayarlayın. İzlek bilinen Jira test adımı alanlarını otomatik arar. Data Center'da özel alanlar adım döndürmezse Xray ve Zephyr Squad kaynaklarını kontrol eder. Test metni boş kalırsa **Kaynak metinler → Jira okuma ayrıntıları** altında alanları ve servis yanıtlarını görebilir, başka bir bağlı test seçebilir veya adımları yapıştırabilirsiniz.
5. **Test görevleri** bölümünde Story’nin **is parent of** bağlantısındaki Test disiplinli görevi numarası veya adıyla arayın. Karşılaştırma için testler Story’nin **tested by** bağlantısından, Confluence sayfası ise **is child of** bağlantısındaki veya **parent** alanındaki analiz görevinden alınır. İncelemeyi açmak için görevi seçin. Birden fazla test varsa **Bağlı testler** üzerinden inceleyeceğiniz testi seçin. Uyum yüzdesi, karşılanan analiz maddelerinin toplam madde sayısına oranıdır. İnceleme önerilerini ve yüzdeye esas sınıflandırmayı düzenleyebilirsiniz.
6. **Yorum sepeti** içinde yalnızca seçtiğiniz taslakları önizleyin. Hedef Jira kaydına onayınızla tek bir yorum gönderilir.

**Kaynak metinler** ekranında başlık biçimindeki gereksinimler ve tablo veri satırları karşılaştırılabilir. Gerektiğinde **Gereksinim bölümlerindeki başlık ve etiketleri de karşılaştır** seçeneğini kullanın. Giriş, yayın çizelgesi, içerik, tanımlar, ekran kodu, Jira bağlantısı, işin tanımı, gerekçe, sürüm koşulları, versiyonlama, kısaltmalar, use case listesi ve iş akışı inceleme kapsamından çıkarılır. Analizde belirtilen ön koşullar ve aktörler test hazırlığında, adımlarda veya verilerde ayrı ayrı aranır. Analizde açık bir aktör tanımı yoksa testte rol bulunup bulunmadığı ayrıca gösterilir. Bu son kontrol uyum puanını etkilemez. Durum alanı okunan kaynakları, modelin değerlendirdiği kontrol ve test kaydı sayısını ve geçen süreyi gösterir. Aynı oturumda değişmemiş bir incelemeyi açınca sonuç tekrar kullanılır. Elle karşılaştırma yeni bir inceleme başlatır.

Yeni bağlantılarda varsayılan yöntem ChatGPT üyeliğidir. Kayıtlı yöntem tercihi korunur. Yerel metin eşleştirme ek model gerektirmez. İsteğe bağlı anlamsal inceleme için bilgisayarınızda kurulu bir Ollama modeli gerekir. Ayarlar ve taslaklar Windows kullanıcı profilinde saklanır.

Bu depo dağıtım dosyalarına ayrılmıştır. Her sürümde çalıştırılabilir dosya ve SHA-256 özeti bulunur.

## ChatGPT üyeliğiyle inceleme

**Bağlantı ayarları → Karşılaştırma yöntemi → ChatGPT üyeliğim** seçeneğini açın. İzlek kurulu Codex bileşenini bulur. ChatGPT oturumunuz açıksa doğrudan kullanır. Oturumunuz yoksa uygulamadan **ChatGPT ile giriş yap** düğmesine basarak tarayıcıda giriş yapın. Pencere görünmezse aynı giriş sayfasını ayarlardan tekrar açabilir veya bağlantıyı kopyalayabilirsiniz. Codex kurulu değilse uygulama resmi Windows bileşenini indirip doğrulayabilir. Seçilen analiz ve test içeriği OpenAI'ye gönderilir ve hesabınızın Codex kullanım hakkı kullanılır. API anahtarı gerekmez.

ChatGPT ve Ollama incelemelerinde kanıt metni ilgili test adımının kaynak alanından alınır. Geçersiz veya eksik maddeler bir kez daha değerlendirilir. Doğrulanan bulgular panoda kalır. Açık maddeleri ve nedenlerini **Doğrulama bekleyen maddeler** altında görebilirsiniz.

**Eksik kapsam** kartında ilgili adım numarasını, sorunun eylemde mi beklenen sonuçta mı olduğunu, analizle çelişen ifadeyi ve önerilen düzeltmeyi görebilirsiniz. Kaynakta eşleşen adım yoksa kart yeni bir adım önerir. Jira'ya göndermeden önce yorumu düzenleyebilir ve hedef kaydı önizleyebilirsiniz.
