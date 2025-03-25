#Virtual Machine: Sanal Makine (VM): fiziki bir bilgisayarda çalıştırılmak istenen belirli bir yazılımın çalıştırılabilmesi amacıyla kullanılan bir bilgisayar olarak tanımlanabilir. Zira Sanal Makine, tıpkı fiziksel bir makinede olduğu gibi kendine ait işletim sistemine, depolamaya, ağa, konfigürasyon ayarlarına ve yazılıma sahiptir.
CONTAİNER :Yazılım dünyasında container (kapsayıcı), bir uygulamanın çalışması için gerekli olan tüm bağımlılıkları, kütüphaneleri ve ayarları içeren izole bir çalışma ortamıdır. Sanal makineler gibi çalışır ama daha hafiftir ve sistem kaynaklarını daha verimli kullanır.

##Docker Desktop Nedir? 
Docker Desktop, Windows ve macOS için geliştirilmiş Docker'ı kolayca yönetmek ve çalıştırmak için kullanılan bir uygulamadır. İçinde Docker Engine, Docker CLI, Docker Compose ve bir dizi araç bulunur.
Özellikleri:
 Kullanıcı dostu arayüz: GUI (Grafiksel Arayüz) sayesinde container’ları görsel olarak yönetebilirsin.
 Docker Compose desteği: Çoklu container uygulamalarını yönetmeyi kolaylaştırır.
 Sanal makine desteği: Windows/macOS ortamında Linux tabanlı container’ları çalıştırabilir.
 Kubernetes entegrasyonu: Kubernetes’i kolayca kullanabilirsin.
Docker Desktop, geliştiriciler için Docker kullanımını daha kolay hale getirir. Ancak Linux kullanıcıları genellikle doğrudan Docker CLI kullanır, çünkü Docker Desktop genellikle Windows/macOS ortamları için daha kullanışlıdır.

##Containerd Nedir? 
Containerd, Docker’ın temelinde çalışan düşük seviyeli bir container çalışma zamanıdır (container runtime).
Docker'ın ilk sürümlerinde tüm bileşenler tek bir monolitik yapıdaydı. Daha sonra Docker ekibi, container işlemlerini yöneten bölümü "Containerd" olarak ayırdı. Bu sayede Containerd, Docker’a bağımlı olmadan Kubernetes gibi diğer sistemlerde de kullanılabilir hale geldi.
Containerd’in Görevleri:
 Container başlatma ve durdurma
 Image (görsel) yönetimi (çekme, kaydetme, silme)
 Ağ ve depolama işlemleri
 Container yaşam döngüsünü yönetme
Containerd, Docker'ın bir parçası olmasına rağmen Docker olmadan da Kubernetes gibi sistemlerde çalışabilir.




Kubernetes: (K8s), container'ları otomatik olarak yöneten, ölçeklendiren ve dağıtan bir container orkestrasyon platformudur.
Container teknolojileri (örneğin Docker) tek bir container'ı yönetmek için iyidir. Ancak çok sayıda container çalıştırmak ve bunları verimli şekilde yönetmek gerektiğinde Kubernetes devreye girer.

#Bu teknolojiler nerede kullanılmaktadır?
Bu teknolojiler genellikle bulut bilişim, yazılım geliştirme, mikro servis mimarisi ve büyük ölçekli dağıtık sistemlerde kullanılır.
Virtual Machine (VM - Sanal Makine) 
Kullanım Alanları:
 Bulut Bilişim (AWS, Azure, Google Cloud) → Örneğin, AWS EC2, Azure VM, Google Compute Engine gibi hizmetler sanal makineler sağlar.
 Test ve Geliştirme Ortamları → Geliştiriciler farklı işletim sistemlerini çalıştırmak için VM kullanır.
 Eski Sistemlerin Çalıştırılması → Örneğin, eski Windows/Linux sistemleri modern donanımlarda çalıştırmak için.
 Güvenli Ortamlar (Sandboxing) → Şüpheli yazılımları çalıştırmak için izole bir ortam sağlar.
Özet: VM’ler, tam işletim sistemlerini sanal olarak çalıştıran ağır yapılardır ve fiziksel donanımı taklit eder.

###Container (Kapsayıcı) 
Kullanım Alanları:
 Mikroservis Mimarisi → Büyük uygulamalar, küçük bağımsız servisler halinde container olarak çalıştırılır.
 CI/CD (Sürekli Entegrasyon/Sürekli Dağıtım) → Yazılım geliştirme süreçlerini hızlandırır.
 Bulut Tabanlı Uygulamalar → AWS, Azure, GCP gibi bulut platformlarında taşınabilir uygulamalar çalıştırmak için.
 Hızlı ve Hafif Uygulama Dağıtımı → Uygulamaları her ortamda (yerel, test, prod) aynı şekilde çalıştırmak için.
Özet: Container’lar, sadece uygulama ve bağımlılıklarını içeren hafif sanal ortamlardır.


#Docker Desktop / Containerd 
Kullanım Alanları:
Geliştiriciler için Yerel Test Ortamları → Windows/macOS’ta container’ları kolayca çalıştırmak için.
 Container Yönetimi → Docker komut satırı (CLI) veya GUI üzerinden container’ları kontrol etmek için.
 CI/CD Pipelines → Kod değişikliklerini hızlıca test etmek için kullanılır.
 Hafif Sanal Ortamlar → Fiziksel makineye bağımlı olmadan uygulama geliştirmek ve çalıştırmak için.
Özet: Docker Desktop, özellikle geliştiricilerin container kullanmasını kolaylaştıran bir araçtır.

Kubernetes (K8s) 
Kullanım Alanları:
 Büyük Ölçekli Uygulamalar → Google, Netflix, Spotify gibi büyük şirketler mikroservislerini yönetmek için Kubernetes kullanır.
 Otomatik Ölçeklendirme Gerektiren Sistemler → Kullanıcı trafiğine göre container’ları artırıp azaltmak için.
 Multi-Cloud Çözümleri → AWS, Azure, GCP gibi platformlarda taşınabilir uygulamalar çalıştırmak için.
 DevOps ve CI/CD → Yazılım geliştirme süreçlerini otomatize etmek için.
 Yüksek Erişilebilirlik (High Availability) → Çöken servisleri otomatik yeniden başlatmak için.
Özet: Kubernetes, çok sayıda container’ı otomatik yöneten bir orkestrasyon aracıdır ve genellikle büyük ölçekli sistemlerde kullanılır.
