---
layout: post
title:  "System Calls (Sistem Çağrıları)"
date:   2012-03-31 02:51:00
tags: 
categories: Operating Systems
mathjax: false
---
Sistem çağrıları  OS tarafından servisler için sağlanan arayüzdür.  Doğrudan donanıma erişenler gibi düşük seviye görevler (tasks) assembly dilinde instructionlar içerdiği halde genellikle C, C++ dilleriyle yazılmışlardır. System call'lar sayesinde yazılımcı doğrudan donanıma müdahale etmez. Donanım üzerinde gerçekleştireceği işlemi system call kullanarak gerçekleştirir. Bu sayede olası sistem haatalarından kaçınılmış olur.

System call'ların da, sistemden sisteme değişiyor olması yazılımcının işini zorlaştırır. Bu değişiklik, bir OS için yazılan programın başka bir OS üzerinde çalışamamasına sebep olur. Bu yüzden programcılar, doğrudan sistem call'lar yerine application program interface(API) kullanmayı tercih ederler.

<strong>Neden API kullanılır?</strong>
<ul>
	<li>API'ler programın her sistem üzerinde çalışabilmesini sağlar.</li>
	<li>API kullanımı, her sistemin system call'larını ezbere bilmeyi gerektirmez.</li>
	<li>Birden fazla sistem işlemini kısa fonksiyonlarla yapabilmeyi sağlar. Programcı API fonksiyonunun içeriğiyle ilgilenmez. Fonksiyonun parametrelerini ve dönüş değerini bilmesi yeterlidir.</li>
</ul>
API'lerin programlamayı oldukça kolaylaştırdığı doğrudur. Ancak daha spesifik işlemler için system call'ları kullanmak gerekebilir.
<h3>System Call Tipleri</h3>
<ul>
	<li>Process Control (Süreç Kontrolü)</li>
<ul>
	<li>bitirme, iptal etme</li>
	<li>yükleme, çalıştırma</li>
	<li>create process(süreç yaratma), terminate process(süreç sonlandırma)</li>
	<li>process attributelerini getirme, process'e attribute atama</li>
	<li>belli bir süre bekleme</li>
	<li>bekleme event'ı, sinyal event'ı</li>
	<li>memory bölgesini allocate, free işlemleri</li>
</ul>
	<li>File Management (Dosya Yönetimi)</li>
<ul>
	<li>dosya yaratma, dosya silme</li>
	<li>açma, kapama</li>
	<li>okuma, yazma, konumunu değiştirme(reposition)</li>
	<li>dosya attributelerini getirme, atama</li>
</ul>
	<li>Device Management (Aygıt Yönetimi)</li>
<ul>
	<li>request device, release device</li>
	<li>okuma, yazma, reposition</li>
	<li>device attributelerini getirme, atama</li>
	<li>mantıksal olarak aygıtları ilişkilendirmek, ayırmak</li>
</ul>
	<li>Information Maintenance (Bilgilendirme Hizmeti)</li>
<ul>
	<li>zamanı veya tarihi getirme, atama</li>
	<li>sistem verisini getirme, atama</li>
	<li>process, dosya veya device attributelerinin getirilmesi, atanması</li>
</ul>
	<li>Communications (İletişim)</li>
<ul>
	<li>iletişim bağlantısının yaratılması, silinmesi</li>
	<li>mesaj alma, gönderme</li>
	<li>durum bilgisinin transferi</li>
</ul>
	<li>Protection (Koruma)</li>
<ul>
	<li>dosyaların yazma, okuma, çalıştırma izinleri</li>
	<li>kullanıcıların system call'lar üzerindeki yetkileri</li>
</ul>
</ul>
<em>Kaynak : Operating System Concepts ~ Eight Edition (s55-s60)</em>