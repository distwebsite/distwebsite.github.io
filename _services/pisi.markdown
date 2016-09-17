---
layout: service
title:  "PiSi Paket Yöneticisi"
lang: tr
encoding: utf-8
icon: "icofont icofont-architecture-alt"
sequence: 2
description: "Mevcut paketlerin en son kararlı sürümlerini bulundurur. Kurulumdan sonra ofis yazılımı, İnternet gezgini gibi gerekli bütün programları yükler."
image: "/images/Pisi-re-3.png"
active: services
---

<div class='col-xs-12'>
    <img class='img-border' src="{{ '/images/Pisi-logo.png' }}" />
</div>

<div class='col-lg-6 col-md-6 col-sm-12 col-xs-12'>
    <div class='form-group'>
        <h3 class='sub-title'>
            {{page.title}}
        </h3>
        <p>        
			Pisi (Açılımı: Packages Installed Successfully as Intended), Python dilinde yazılmış bir paket yönetim sistemidir. Bağımlılıklara bakarak paket oluşturma, kurma, kaldırma, yükseltme ve benzeri işlevleri yerine getirir. XML ile tanımlanmış ve oluşturma süreci bir Python betiği ile verilmiş kaynak paketlerden ikili paketler oluşturur ve bunları bağımlılıklarına bakarak kurup kaldırabilir. Kullanıcı dostu bir çizgelik arayüz ve kapsamlı bir komut yatacı arayüzü içerir.
			<h3 class='sub-title'>KUŞBAKIŞI PİSİ KOMUT SATIRI</h3>
			
            <p>SVN tarzı komut satırı işlemcisi 29 komut içerir. Aşağıda komut çeşitlerine göre bir ayrım verilmiştir.</p>

            <p>Bilgi/arama komutları: search, search-file, info, list-available, list-components, list-installed, list-pending, list-repo, list-upgrades, graph</p>

            <p>Depo komutları: index, add-repo, remove-repo, update-repo</p>

            <p>Paket inşası: build, build-until,build-build, build-install, build-package, build-setup, build-unpack</p>

            <p>İkili paket işlemleri: install, remove, upgrade, check, configure-pending</p>

            <p>Yardımcı komutlar: rebuild-db, clean, delete-cache</p>

            <h3 class='sub-title'>GRAFİKSEL ARAYÜZ</h3>
            
            <p>Paket Yöneticisi'nde seçilen programlar yüklenirken
            Qt tabanlı arayüze sahiptir. Sadece Pisi Linux kullanmaktadır . SolusOS, GTK tabanlı bir paket yöneticisi geliştirmektedir, henüz tamamlanmamıştır Kullanımının mümkün olduğu kadar basitleştirildiği düşünülen bir arayüzdür. </p>
            <p>Bütün işlemler için tek bir pencere ve depo ayarları için ayrı bir pencereden oluşur. Paket işlemleri için üç ayrı kip bulunmaktadır (yükseltme, yükleme, kaldırma).</p> 
            <p>Arama fonksiyonu paketlerin üstünde tanıdık bir arama çubuğu ile sağlanır. Paketler bileşenlere ayrılır. Öntanımlı olarak sadece uygulamaları gösterir, bir filtre seçeneği ile bütün uygulamalar seçilebilir. Bütün sistem tek bir tuşla güncellenir.</p>
        </p>
    </div>
</div>

<div class='col-lg-6 col-md-6 col-sm-12 col-xs-12 service-content'>    
    <div class='form-group'>
        <h3 class='sub-title'>
            ÖZELLİKLERİ
        </h3>
        <p>
        </p>
		<ul class='list-unstyled list-primary'>
            <li>
                <i class="fa fa-check" aria-hidden="true"></i> PiSi Python'da yazılmıştır, bu sayede performans kaybetmeden taşınabilirlik ve paketlerin boyutunun küçültülmesi sağlanmıştır. Kaynak paketler basit XML dosyaları ve python programcıklarıyla ifade edilir.
            </li>
            <li>
                <i class="fa fa-check" aria-hidden="true"></i> Paketler kaynak tabanlı paket sistemlerindeki gibi kısa ve anlaşılabilir bir inşa reçetesiyle tanımlarır, bunun için geliştirilmis olan bir API gereken ortak komutları toplar. Yüksek seviyeli ve düşük seviyeli paket yönetim işlevlerini tek bir yazılımda birleştirir. Bağımlılıkları takip etmek ya da depoları yönetmek için ayrı bir yazılıma gereksinim duymaz. Hangi dosyanın hangi pakette olduğu ve bağımlılıklar gibi paket bilgilerinı takip etmek için Berkeley DB'yi kullanır.
            </li>
            <li>
                <i class="fa fa-check" aria-hidden="true"></i> Bağımlılıklar hızlı algoritmalarla hesaplanır. Paketler bileşen ve kategorilerle düzenlenir. İkili paketler PKZIP arşivleridir. Birçok işlemde şeffaf biçimde URL desteği verilir, http ve ftp protokolleri desteklenir. Örneğin sadece bir pspec.xml URL'i verilerek uzaktaki bir kaynak inşa edilebilir. Kaynak arşivini URL ile gösterir, orijinal kaynak code'unu içermez, bu da subversion gibi sürüm sistemleriyle geliştirmeyi kolaylaştırır. Kitaplık yaklaşımıyla tasarlandığı için üzerinde uygulama geliştirmek kolaydır. Program mesajları için özgür yazılımlarda yaygın olarak kullanılan gettext uluslararasılaştırması, xml dosyaları için xml:lang uluslarasılaştırması kullanılmıştır.
            </li>
            <li>
                <i class="fa fa-check" aria-hidden="true"></i> Anahtar sözcük araması (search komutu) özetler ve tanımlar üzerinde çalışır. Hızlı işlem için bir ters indeks (inverted index) kullanır ve çok dilli çalışır. Ayrica search-file komutu dosya adıyla paket bulur.
            </li>
            <li>
                <i class="fa fa-check" aria-hidden="true"></i> Özelleştirilebilir ve esnek olması sebebiyle berkeley veritabanı tercih edilmiştir (örneğin liste saklamak vs. kolaydır). Bütün ara (intermediate) veri XML olarak saklanır. XML yapıları otomatik olarak python nesnelerine aktarılır. Felaket durumunda bütün veritabanı saklanan XML dosyalarından yeniden yaratılabilir (rebuild-db komutu).
            </li>           
		</ul>
    </div>
</div>
<div class='col-xs-12'>
    <img class='img-border' src="{{ '/images/Pisi_Paket-1.png' }}" />
</div>
<div class='clearfix'></div>
