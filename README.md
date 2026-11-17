# İzlek

Windows için Jira test inceleme panosu. Atanan test görevinden story'ye, test mühendisinin senaryolarına ve bağlı Confluence analizine gider. Analiz maddeleri ile test adımlarını yan yana inceleyebilir, kapsam yüzdesini görebilir ve seçtiğiniz yorumları düzenleyerek Jira'ya gönderebilirsiniz.

**[Windows x64 için İzlek 0.1h sürümünü indir](https://github.com/Birkankader/izlek-releases/releases/download/v0.1h/Izlek-0.1h-windows-x64.exe)** · [Tüm sürümler](https://github.com/Birkankader/izlek-releases/releases)

0.1f ve önceki sürümleri kullanıyorsanız güncel EXE dosyasını bir kez elle indirin. İzlek’i yazabildiğiniz bir klasörden çalıştırın. Sonraki sürümler açılışta ve uygulama açıkken altı saatte bir GitHub üzerinden kontrol edilir. İzlek yayıncı imzasını ve dosyanın SHA-256 özetini doğruladıktan sonra güncellemeyi hazırlar. Açık incelemenize devam edebilir, **Şimdi yeniden başlat** düğmesini kullanabilir veya yeni sürüme bir sonraki açılışta geçebilirsiniz.

0.1h sürümünde inceleme panosu uyum yüzdesini, eksik kapsamı, uç durumları ve karşılanan maddeleri bir arada gösterir. Karttaki **Sorun ve çözüm** bölümünden düzeltmeyi okuyabilir, **Yorumu incele** yan panelinde sorunlu test alanını görüp taslağı düzenleyebilirsiniz.

## Başlangıç

1. Windows 10/11 x64 üzerinde EXE dosyasını açın. Uygulama Microsoft Edge WebView2 Runtime kullanır. EXE dijital imzasızdır.
2. İlk ekranda Jira ve Confluence sunucularınızı girin. Kurum bağlantısı olmadan denemek için **Örnek panoyu aç** seçeneğini kullanabilirsiniz.
3. Data Center'da kişisel erişim tokenı, Cloud'da e-posta ve site adresiyle çalışan API tokenı girin. Cloud Confluence adresine `/wiki` yolunu ekleyin. Sunucular farklıysa iki token alanını da doldurun. Başarılı bağlantıdan sonra tokenlar Windows Kimlik Bilgisi Yöneticisi'nde saklanır. 0.1b veya önceki bir sürümden yükseltirken tokenları bir kez girin. Sonraki bağlantılarda kayıtlı alanları boş bırakın.
4. **Görev sorgusu ve kurum alanları** altında atanan testlerin JQL sorgusunu, story türünü, ilişki adlarını ve varsa test adımı özel alanlarını ayarlayın. İzlek bilinen Jira test adımı alanlarını otomatik arar. Data Center'da özel alanlar adım döndürmezse Xray ve Zephyr Squad kaynaklarını kontrol eder. Test metni boş kalırsa **Kaynak metinler → Jira okuma ayrıntıları** altında alanları ve servis yanıtlarını görebilir, başka bir bağlı test seçebilir veya adımları yapıştırabilirsiniz.
5. Bir görev açın. Birden fazla test varsa **Bağlı testler** üzerinden inceleyeceğiniz testi seçin. Uyum yüzdesi, karşılanan analiz maddelerinin toplam madde sayısına oranıdır. İnceleme önerilerini ve yüzdeye esas sınıflandırmayı düzenleyebilirsiniz.
6. **Yorum sepeti** içinde yalnızca seçtiğiniz taslakları önizleyin. Hedef Jira kaydına onayınızla tek bir yorum gönderilir.

**Kaynak metinler** ekranında başlık biçimindeki gereksinimler ve tablo veri satırları karşılaştırılabilir. Gerektiğinde **Başlık ve etiketleri de karşılaştır** seçeneğini kullanın. **Yeniden dene** kutulardaki güncel metni okur.

Varsayılan metin eşleştirme ek model gerektirmez. İsteğe bağlı anlamsal inceleme için bilgisayarınızda kurulu bir Ollama modeli gerekir. Ayarlar ve taslaklar Windows kullanıcı profilinde saklanır.

Bu depo dağıtım dosyalarına ayrılmıştır. Her sürümde çalıştırılabilir dosya ve SHA-256 özeti bulunur.

## ChatGPT üyeliğiyle inceleme

**Bağlantı ayarları → Karşılaştırma yöntemi → ChatGPT üyeliğim** seçeneğini açın. İzlek kurulu Codex bileşenini bulur. ChatGPT oturumunuz açıksa doğrudan kullanır. Oturumunuz yoksa uygulamadan **ChatGPT ile giriş yap** düğmesine basarak tarayıcıda giriş yapın. Pencere görünmezse aynı giriş sayfasını ayarlardan tekrar açabilir veya bağlantıyı kopyalayabilirsiniz. Codex kurulu değilse uygulama resmi Windows bileşenini indirip doğrulayabilir. Seçilen analiz ve test içeriği OpenAI'ye gönderilir ve hesabınızın Codex kullanım hakkı kullanılır. API anahtarı gerekmez.

ChatGPT ve Ollama incelemelerinde kanıt metni ilgili test adımının kaynak alanından alınır. Geçersiz veya eksik maddeler bir kez daha değerlendirilir. Doğrulanan bulgular panoda kalır. Açık maddeleri ve nedenlerini **Doğrulama bekleyen maddeler** altında görebilirsiniz.

**Eksik kapsam** kartında ilgili adım numarasını, sorunun eylemde mi beklenen sonuçta mı olduğunu, analizle çelişen ifadeyi ve önerilen düzeltmeyi görebilirsiniz. Kaynakta eşleşen adım yoksa kart yeni bir adım önerir. Jira'ya göndermeden önce yorumu düzenleyebilir ve hedef kaydı önizleyebilirsiniz.
