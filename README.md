Bu proje, çeşitli istatistiksel olasılık teorileri ve olasılık dağılımlarını kullanarak veriler üzerinde analizler yapmayı amaçlamaktadır. Veriler üzerinden yapılan analizlerle popülasyon ve örneklem ilişkileri, güven aralıkları ve farklı olasılık dağılımlarının uygulanabilirliği incelenmiştir. Aşağıda projede kullanılan bazı temel kavramlar ve analiz yöntemleri açıklanmıştır.

İÇERİK:
Örneklem: Veri bilimi çalışmalarında kullanılacak olan popülasyonun bir alt kümesidir. Günümüzde verilerin fazlalığı sebebiyle  örneklemler üzerinden analizler yapılır, modeller kurulur ve popülasyona ait çıkarımlar elde edilir.

Seaborn kütüphanesi içerisinden "tips" veri seti seçilerek describe() fonksiyonu ile istatistiksel sonuçlarını inceledim. Researchpy kütüphanesi kullanarak da kategorik değişkenlerin de analizini yaptım. Toplam bahşişlerle, günlük bahşişler arasındaki ilişkinin sonucunu " df[["tip","total_bill"]].cov()" ile gözlemledim burda cov() coveryansın kısaltması olarak yazılmıştır. İstatistikte veri seti içerisindeki değişkenlerin birbirleriyle ilişkilerindeki oranı vermektedir.df[["tip","total_bill"]].corr() ile de  bu değişkenlerin birbiriyle ilişkisinin gücünü ve yönünün gösteririr. Yani 
1: Tam pozitif doğrusal ilişki
-1: Tam negatif doğrusal ilişki
0: Hiçbir doğrusal ilişki bulunmamaktadır.

Güven aralığı teorisi
Popülasyon parametrelerinde ortalama,oran değerlerinin hangi değerler arasında olacağını belirler.
Fiyatlar adında oluşturduğumuz datamızda fiyatların ortalamasını aldıktan sonra "statsmodels.stats.api" kütüphanesini kullanarak fiyatlar için %95 oranında bir güven aralığını oluşturdum.

Bernoulli Dağılım
Başarılı-Başarısız, olumlu-olumsuz şeklinde iki sonuçlu olaylar ile ilgilenildiğinde kullanılan kesikli dağılımdır.

Büyük Sayılar Yasası (Law of Large Numbers - LLN), istatistikte, bir deneyin tekrar sayısı arttıkça örneklemin ortalamasının gerçek popülasyon ortalamasına daha yakın bir değeri alacağını ifade eden bir temel yasadır.Yeterince büyük bir örneklemde örneklem ortalaması ile gerçek popülasyon ortalaması arasındaki fark giderek azalır. Projemizde yazı tura üzerinde her seferinde daha fazla atış yaparak atış sayısının artmasıyla sonucun %50'ye ne kadar yaklaştığını gözlemlemekteyiz.

Binom dağılımı birbirinden bağımsız n deneme sonucuna göre başarılı olma durumu üzerinde durulur. Projemizde bir web sitesinde reklama tıklama üzerinde bir çalışma yapılmıştır. 500 kullanıcının reklamı gördüklerinde tıklama olasılıkları üzerinde durulmuştur. p değeri sabittir.

Poisson Dağılımı, belirli bir zaman diliminde ya da belirli bir alanda nadiren gerçekleşen olayların sayısını modellemek için kullanılan bir olasılık dağılımıdır. Örneğin 10000 kelimelik bir kitapta hatalı kelime sayısı.
λ (Lambda): Olayların ortalama sayısını temsil eder. Bu, birim zaman veya birim alanda beklenen olay sayısıdır. 

Normal Dağılım, sürekli rassal değişkenlerin olasılık hesaplaması için kullanılır. Örneğin Bir toplantı öncesinde gelecek ay ile ilgili satışların belli değerlerde gerçekleşme olasılığının belirlenmesi isteniyor.Bunun gibi durumları analiz etmek için kullanılır.
