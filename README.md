# İzlek

Windows için Jira test inceleme panosu. Atanan test görevinden story'ye, test mühendisinin senaryolarına ve bağlı Confluence analizine gider. Analiz maddeleri ile test adımlarını yan yana inceleyebilir, kapsam yüzdesini görebilir ve seçtiğiniz yorumları düzenleyerek Jira'ya gönderebilirsiniz.

**[Windows x64 için İzlek 0.1b'yı indir](https://github.com/Birkankader/izlek-releases/releases/download/v0.1b/Izlek-0.1b-windows-x64.exe)** · [Tüm sürümler](https://github.com/Birkankader/izlek-releases/releases)

## Başlangıç

1. Windows 10/11 x64 üzerinde EXE dosyasını açın. Uygulama Microsoft Edge WebView2 Runtime kullanır. EXE dijital imzasızdır.
2. İlk ekranda Jira ve Confluence sunucularınızı girin. Kurum bağlantısı olmadan denemek için **Örnek panoyu aç** seçeneğini kullanabilirsiniz.
3. Data Center'da kişisel erişim tokenı, Cloud'da e-posta ve site adresiyle çalışan API tokenı girin. Cloud Confluence adresine `/wiki` yolunu ekleyin. Sunucular farklıysa iki token alanını da doldurun. Tokenlar yalnızca uygulama oturumunda tutulur.
4. **Görev sorgusu ve kurum alanları** altında atanan testlerin JQL sorgusunu, story türünü, ilişki adlarını ve varsa test adımı özel alanlarını ayarlayın. Test adımları yalnız ayrı bir eklenti API'sinden okunabiliyorsa eklentiye özel bir bağlantı gerekir.
5. Bir görev açın. Birden fazla test varsa **Bağlı testler** üzerinden inceleyeceğiniz testi seçin. Uyum yüzdesi, karşılanan analiz maddelerinin toplam madde sayısına oranıdır. İnceleme önerilerini ve yüzdeye esas sınıflandırmayı düzenleyebilirsiniz.
6. **Yorum sepeti** içinde yalnızca seçtiğiniz taslakları önizleyin. Hedef Jira kaydına onayınızla tek bir yorum gönderilir.

Varsayılan metin eşleştirme ek model gerektirmez. İsteğe bağlı anlamsal inceleme için bilgisayarınızda kurulu bir Ollama modeli gerekir. Ayarlar ve taslaklar Windows kullanıcı profilinde saklanır.

Bu depo dağıtım dosyalarına ayrılmıştır. Her sürümde çalıştırılabilir dosya ve SHA-256 özeti bulunur.

## ChatGPT üyeliğiyle inceleme

**Bağlantı ayarları → Karşılaştırma yöntemi → ChatGPT üyeliğim** seçeneğini açın. Mevcut Codex oturumunuz tanınır. Oturumunuz yoksa uygulamadan **ChatGPT ile giriş yap** düğmesine basarak tarayıcıda giriş yapın. Codex kurulu değilse uygulama resmi Windows bileşenini indirip doğrulayabilir. Seçilen analiz ve test içeriği OpenAI'ye gönderilir ve hesabınızın Codex kullanım hakkı kullanılır. API anahtarı gerekmez.

**Eksik kapsam** kartında ilgili adım numarasını, sorunun eylemde mi beklenen sonuçta mı olduğunu, analizle çelişen ifadeyi ve önerilen düzeltmeyi görebilirsiniz. Kaynakta eşleşen adım yoksa kart yeni bir adım önerir. Jira'ya göndermeden önce yorumu düzenleyebilir ve hedef kaydı önizleyebilirsiniz.
