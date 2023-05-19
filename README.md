#Unit Test
Bir yazılımın ayrı birimlerinin veya bileşenlerinin test edildiği bir yazılım test türüdür
#Unit Test Methods
####Arrange
Test edilecek methodun kullanılacağı kaynakların hazırlandığı bölümlerdir.Değişken tanımlama,nesne oluşturma vs. bu bölümde oluşturulur
####Act
Arrange'de hazırlanan değişken veya nesneler eşliğinde test edilecek olan methodun çalıştırıldığı bölümdür
####Assert
Act aşamasında yapılan testin doğrulama evresidir

###Fonksiyonlar ve Açıklamaları
######Equal/ NotEqual
Gelen sonuç ile beklenen sonucu kıyaslar
######Contain/ DoesNotContain
Gelen sonuç içerisinde bir değerin olup olmamasını kontrol eder
######Match/ DoesNotMatch
Test süresince gelen değerin bildirilmiş Regex ifadesine uyup uymadığını kontrol eder
######StartsWith/ EndsWith
Gelen değerin bildirilmiş olan değer ile başlama ve bitişini kontrol eder
######Empty/ NotEmpty
Boş olup olmama durumunu kuntrol eder
######InRange/ NotInRange
Gelen değerin belirli bir aralıkta olup olmamasını kontrol eder
######Single
Verinin içerisindeki başka verinin varlığını kontrol eder
######IsType/ IsNotType
Gelen değerin türüne göre kontrol sağlar
######IsAssignableFrom
Gelen değerin hangi türden türediğini kontrol eder
######Null/ NotNull
Null olup olmama durumunu kontrol eder yani boş olup olmama durumu

######Not
Test classlarımız için üç farklı seviye vardır(Assembly Level, Test Level, Class Level)
######Not2
En üstte [ClassIntialize] tanımlanır.Eğer tek bir sefer yapılmasını istediğimiz bir işlem veya method varsa.Bütün projede geçerli static tanımlanır. Eğer bir işlem yapılacaksa da [ClassCleanup] methodu kullanılır.

####Assert Medhodları
######AreEqual
İki değer arası eşitliği kontrol eder
######AreSome
İki obje arası referans kontrolü yapar
######IsNull/ IsNotNull
Bir değişkenin null olup olmama durumunu kontrol eder
####CollectionAssert Methodları
######AreEqual
İki collection arasında itemlar aynı olmalı ve aynı sırada da olmalı 
######AreEquivalent
İtemlar aynı olsa yeterli, sıralama önemli değil
######AllItemsAreNotNull
Herhangi bir item null değer barındırdıysa test hata verir
######AllItemsAreUnique
Liste içinde bulunan değerlerin benzersiz olma durumunu kontrol eder
######AllItemsAreInstancesOfType
Liste içinde objelerin tiplerinin aynı olma durumunu kontrol eder
######Contains
Bir elementin listede var olma durumunu kontrol eder
######IsSubsetOf
X listesi Y listesini barındırıyor mu gibi kontrolleri yapar
####StringAssert Methodları
(Contains, Matches/ DoesNotMatch,StartWith/ EndsWith)

[Owner("....")] => testi yazan kişinin adı belirtilir
[TestCategory(".....")] => Kategori belirtilir örneğin Tester Developer
[Priorty(1)] => Öncelik sırası belirtir
[TestProperty("....")] => Testi güncelleyen yeniden yapanın ismi yazılır
[ignore] => Testi yok saymak yani atlamak için kullanılır
[TimeOut] => Verilen sürede bitmez ise zaman aşımı olur
[Description] => Test Methoduna mesaj girmek için kullanılır
