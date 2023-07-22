# ModulCar - CI/CD Süreçleri

Bu dökümanda, ModulCar'nın sürekli entegrasyon (CI) ve sürekli dağıtım (CD) süreçleri hakkında bilgi verilecektir. Uygulamanın kod tabanı GitHub'da barındırılıyor ve CI/CD süreçleri, belirli aşamalarda otomatik olarak çalıştırılarak uygulamanın güvenli ve stabil bir şekilde dağıtılmasını sağlamak amacıyla yapılandırılmıştır.

## CI/CD Platformu ve Aracı

ModulCar için CI/CD süreçlerini yönetmek için [Jenkins](https://www.jenkins.io/) kullanmaktayız. Jenkins, açık kaynaklı ve geniş özelliklere sahip bir CI/CD aracıdır ve projemizin ihtiyaçlarına uygun şekilde özelleştirilebilir.

## CI Süreci

CI süreci, her yeni kod değişikliği yapıldığında otomatik olarak tetiklenir. CI sürecinde şu adımlar gerçekleştirilir:

1. **Kod Derlemesi**: Yeni kod değişiklikleri için otomatik olarak derleme işlemi gerçekleştirilir. Bu, kodun geçerli ve çalışabilir olup olmadığını kontrol etmek için yapılır.

2. **Kod Kalite Kontrolü**: Kod stili, hatalar ve kod kalitesi için otomatik kontroller yapılır. Kodun belirlenen standartlara uygunluğu denetlenir.

3. **Otomatik Testler**: Uygulamanın birim ve entegrasyon testleri otomatik olarak çalıştırılır. Bu adım, yeni değişikliklerin uygulama içindeki diğer bileşenlerle uyumlu olduğundan emin olmak için yapılır.

4. **Raporlama**: CI sürecinin sonuçları raporlanır ve ekibin kontrol edebileceği şekilde sunulur.

## CD Süreci

CD süreci, CI sürecinden geçmiş ve başarılı bulunan her yeni değişiklik için otomatik olarak başlatılır. CD sürecinde şu adımlar gerçekleştirilir:

1. **Staging Ortamı**: Başarılı bir şekilde geçmiş değişiklikler, önceden belirlenmiş bir sahte canlı ortama (staging) otomatik olarak dağıtılır. Bu adım, uygulamanın canlı ortama geçmeden önce test edilmesini sağlar.

2. **Canlı Ortam**: Staging ortamındaki uygulama, son kullanıcılara görünebilir hale gelmeden önce canlı ortama otomatik olarak dağıtılır.

3. **Monitörleme ve Geri Bildirim**: Uygulamanın canlı ortamdaki performansı ve kullanılabilirliği sürekli olarak izlenir. Gerekirse ekibimize geri bildirim gönderilir ve hatalar düzeltilir.

## Manuel Müdahale

Her ne kadar CI/CD süreçleri otomatik ve hatasız çalışmaya yönelik olsa da, bazı durumlarda manuel müdahale gerekebilir. Özellikle canlı ortama geçiş ve özel durumlar için belirli adımlar manuel olarak kontrol edilmelidir.

## Katkı

ModulCar'nın geliştirilmesine katkıda bulunmak istiyorsanız, lütfen yeni bir dal oluşturun ve pull talepleriyle değişikliklerinizi gönderin. Yapıcı eleştiriler ve yeni özellik önerileri her zaman memnuniyetle karşılanır!