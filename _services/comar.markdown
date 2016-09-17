---
layout: service
title:  "ÇOMAR"
lang: tr
encoding: utf-8
icon: "icofont icofont-architecture-alt"
sequence: 3
description: "Gerektiğinde donanım, açılış, ağ, kullanıcı, zaman, görüntü gibi ayarların mümkün olduğuca kendiliğinden yapılmasını sağlar"
image: "/images/5.re.jpg"
active: services
---

<div class='col-xs-12'>
    <img class='img-border' src="{{ '/images/comar-logo.png' }}" />
</div>
<div class='col-lg-6 col-md-6 col-sm-12 col-xs-12'>
    <div class='form-group'>
        <p>
        ÇOMAR (Açılımı: COnfiguration MAnageR), dizgenin düzgün çalışması için gerekli olan donanım, açılış, ağ, kullanıcı, zaman, görüntü gibi ayarların mümkün olduğu kadar kendiliğinden yapılmasını sağlayan, kullanıcılara bir yetki denetiminde bu ayarları bayağı ve anlaşılır bir biçimde değiştirme olanağı sağlayan bir yazılımdır.
        <h3><p>Giriş</p></h3>
        <p>Bu belge, Ulusal Dağıtım'ın yapılandırma yönetim sistemi olan ÇOMAR'ın, ne amaçla geliştirildiğini, hangi sorunlara çözüm getirdiğini, yapısını ve bileşenlerini anlatır. Hedef kitlesi, ÇOMAR'ı yakından tanımak isteyen kullanıcılar ve sistem yöneticileridir. Bilişim okuryazarı seviyesine göre yazılmış olmakla birlikte, bazı tartışmaları takip edebilmek için, bir işletim sisteminin bileşenleri, ve uygulamaların nasıl ayarlandığı gibi sistem yönetimi konularında bilgi sahibi olmak gerekebilir. </p>
        <h3>Sorun</h3>

        <p>Çeşitli uygulamalar bir sistem içinde bir araya getirildiklerinde, birbirleriyle uyumlu çalışabilmeleri için ayarlanmaları gerekmektedir. Kurulan bir uygulamanın masaüstü menüsüne eklenmesi, açabildiği dosya tiplerini sisteme bildirmesi, yeni kurulan bir spam (istenmeyen eposta) filtreleyicinin mevcut eposta sunucusuna bağlanması gibi çok sayıda entegrasyon işlemi bulunmaktadır. Kullanıcı, bu ayarları yapabilmek için, kendi yapmak istediği işin dışındaki teknik konularda bilgi kazanmak zorunda kalmakta ve zaman kaybetmektedir. 
        <h3><p>Belgeler</p></h3>

        <p>Özgür yazılım camiası, bu işleri kolaylaştırmak için nasıl (ing. howto) belgeleri adıyla çeşitli belgeler hazırlamıştır. Bunlar bir işi yapabilmek için neler yapılması gerektiğini adım adım anlatan kısa belgelerdir. Kullanıcıların belge okumak istememeleri ve belgelerin kısıtlı sayıda senaryoyu kapsaması yüzünden faydalı olamamaktadırlar. 
        Burda aklımıza, madem bir işi adım adım belgeleyebiliyoruz, bunu bir program haline getirip otomatik olarak yapılmasını sağlayamaz mıyız? sorusu gelmektedir. Bu yapılabilirse, kullanıcının zaman tasarrufu yanında, bu belgelerin çeşitli dillere tercüme edilmesi gibi işler de gereksiz hale gelecektir.</p> 
        <h3><p>Diğer Linux Dağıtımları</p></h3>

        Linux dağıtımları gelişme süreçleri içerisinde bu tür entegrasyon problemleri ile karşılaştıkça bunlara ayrı ayrı çözümler üretip kendi sistemlerine (özellikle paket yönetici yazılımlarının içine) dahil etmişlerdir. Bu çözümler, kurulu uygulamalar (menü), fontlar, açılış işlemleri (initscripts) gibi tek tek alt sistemler bazındadır. 
        Genellikle, uygulama paketleri, dosya sistemi üzerinde sabit bir dizine, söz konusu alt sisteme neler sağladıklarını kaydetmekte; bu alt sistemi kullanacak uygulamalar ise, buraya önceden belirlenmiş biçimde kaydedilen dosyaları tarayarak, sağlanan hizmetleri bulmaktadır. Uygulamaların entegrasyonu için, ya uygulamalar buradaki standartları bilecek biçimde değiştirilmekte, ya da gerekli çevrimi yapacak üçüncü bir yönetici uygulama araya sokulmaktadır. Kayıt ve çevrim işlemleri için özel veri biçimleri, kabuk, Perl ya da Python betikleri, bazen de bunların bir karışımı kullanılmaktadır. </p>
        Bir de uygulama kurulur, kaldırılır ve güncellenirken çalışan özel betikler bulunmaktadır. Bunlarla güncelleme sırasında eski ayarların taşınması gibi işler yapılmaktadır. Bazı sistemler (örneğin Debian'ın debconf'u) kurulum anında bu betiklerin kullanıcıya soru sorabilmeleri ve uygulamayı cevaplara göre ayarlamalarını sağlamaktadır. 
        <h3><p>Burda gördüğümüz noksanlıklar:</p> </h3>
        <p>Her sorun için ayrı bir çözüm kullanılması benzer işlerin tekrar tekrar yapılmasına yol açmaktadır. Genel bir ayar profili oluşturmayı ve yönetmeyi zor kılmaktadır. Birbirleriyle ilişkileri eksik kaldığı için yeterli entegrasyonu sağlayamamaktadır.</p>
        Yapılandırma ile paket kurulumu iç içe geçmiştir. Bir paket (özellikle bir sunucu uygulaması) kurulduğunda çalışacak şekilde yapılandırılmasının yanlış olduğunu, uygulamanın ancak kullanıcı bir emir verdiğinde, verilen emre göre yapılandırılmasının anlamlı olduğunu düşünüyoruz. Yapılandırma, kurma ve kaldırma ile ilgisi olmayan ve uygulama sistemde durduğu sürece her an ihtiyaç duyulabilecek bir iştir.
        Bir sürü veri biçimi ve dil kullanılması, öğrenme ve hata düzeltme süreçlerini çok güçleştirmektedir.
        Bir sorun çıktığında sistemi çalışabilir bir konuma getirmek, uygulamalar güncellenirken kullanıcı ayarlarını ve sistemin tutarlılığını korumak çok zor olabilmektedir.
        </p>  				
    </div>
</div>

<div class='col-lg-6 col-md-6 col-sm-12 col-xs-12 service-content'>    
    <div class="form-group">
        <div class='form-group'>
            <h3 class='sub-title'>
                ÖZELLİKLERİ
            </h3>
            <p>
                Bir görevin yerine getirilmesi için kullanıcının değil, bilgisayarın iş yapmasını sağlamak üzere tasarlanmıştır. Normal şartlar altında böyle bir aracın varlığı dahi fark edilmez.
            </p>
            <ul class='list-unstyled list-primary'>
                <li>
                    <i class="fa fa-check" aria-hidden="true"></i> Programlar, donanım ve işletim sistemi arasında çalışarak gerekli ayarları yapar.
                </li>           
            </ul>
        </div>
    </div>
</div>
<div class='col-xs-12'>
    <img class='img-border' src='{{ page.image }}' />
</div>

<div class='clearfix'></div>
