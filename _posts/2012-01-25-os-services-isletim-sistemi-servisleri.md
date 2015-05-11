---
layout: post
title:  "OS Services (İşletim Sistemi Servisleri)"
date:   2012-03-31 02:51:00
tags: [os, operating system, işletim sistemi]
categories: [Operating Systems]
mathjax: false
---

Bir OS, programların çalışması için uygun bir çevre sağlar. Bunun için de OS çeşitli servislere ihtiyaç duyar. Bazı özelleşmiş servisler işletim sisteminden işletim sistemine farklılık gösterebilir. Ancak genel hatlarıyla bir işletim sisteminin sağladığı servisler şöyledir :<a href="{{site.baseurl}}/assets/images/2012/01/os-scheme.png" target="_blank"><img class="alignright size-medium wp-image-286" title="os-scheme" src="{{site.baseurl}}/assets/images/2012/01/os-scheme-300x247.png" alt="OS scheme with services" width="300" height="247" /></a>

**User Interface :** Kullanıcıların işletim sistemine ne yapmak istedikleri arayüzdür. Neredeyse tüm işletim sistemleri user interface(UI) içerir. Bazı UI türleri :

1. *Command-line interface (CLI) :* Komutların yazı olarak girildiği UI türüdür. Günümüzde neredeyse tüm işletim sistemleri tarafından kullanılır. Örneğin windows için run -> cmd diyerek ulaşılabilir. Linux'ta terminal veya console olarak görülebilir.
2. *Batch interface :* Yapılacak işlemlerin daha önceden dosyalara kaydedildiği UI türü. İşletim sistemine dışarıdan içi komut dolu dosya verilir ve işletim sistemi bu komutları işler.
3. *Graphical User Interface (GUI) :* En çok kullanılan arayüz şeklidir. Arayüz kullanıcıya pencereler şeklinde gösterilir. Menüleri seçmek, pencerelerde dolaşmak, komutlar vermek için fare gibi nokta belirleyen aygıtlar kullanılır. Klavye ise text girişi vb için kullanılır. Windows, Mac OS X, bazı Linux sürümleri (KDE, Gnome ... kullanan) GUI kullanır.

**Program Execution :** Sistem programları belleğe yükleyebilmeli ve yüklediği bu programları çalıştırabilmelidir. Ayrıca bu programlar normal veya normal olmayan yollardan (ör : Hata vererek) sonlanabilmelidir.

**I/O Operations :** Çalışan bir program bir aygıttan veya bir dosyadan girdi/çıktı yapmak isteyebilir. I/O işleminin etkin ve güvenli bir şekilde yapılabilmesi için işlem doğrudan kullanıcı tarafından yapılmamalıdır. Bu da işletim sistemlerin I/O desteği vermesini gerekli kılar.

**File-System Manupilation :** Bir program dosyaları okumak, yazmak; klasörler içerisinde dolaşmak veya dosyaları, klasörlerı oluşturmak, silmek, adlandırmak, isimlerine göre arama yapmak, bilgileri görüntülemek isteyebilir. Bazı programlar dosyayı sahiplenerek dosya, klasör yönetimi hakkına sahip olabilir. Çoğu OS çeşitli file system sunar. Bu seçim kişinin kişisel seçimine veya bazı özelliklere ve performansa bağlı olarak yapılabilir.

**Communications :** Sistemdeki bir process bir başka process ile iletişime geçmek isteyebilir. Bu iki process aynı bilgisayarda veya ağ üzerindeki farklı bilgisayarlarda olabilir. Processler arasındaki iletişim *shared memory* veya *message passing* yöntemlerinden biri ile gerçekleştirilir.

**Error detection :** OS, oluşabilecek hataların sürekli farkında olmalıdır. Her tür hata için OS doğruluğu ve tutarlılığı sağlamak için uygun işlemi yapmalıdır. Oluşabilecek bazı örnek hatalar :

1. CPU ve Bellek hataları : Belleğe erişememe, gücün kesilmesi...
2. I/O Aygıtı hataları : bellek aygıtı üzerindeki parity hataları, ağ üzerindeki bağlantının kesilmesi, yazıcıya kağıt sıkışması...
3. User Program Hataları : Aritmetik taşmalar, kendine ait olmayan bir bellek bölgesine erişmeye çalışmak, çok fazla CPU kullanımı ...

**Resource Allocation :** Birçok kullanıcı veya birçok görevin (task/job) aynı anda çalıştığı sistemlerde, her biri için kaynaklar ayrılmalıdır.

**Accounting :** Hangi kullanıcının ne kadar kaynak kullandığı, hangi kaynakları kullandığı gibi bilgilerin tutulması işlemidir. Bilgisayarın yeniden konfigüre edilmesi; donanımının, yazılımının güncellenmesi için gerekli olabilir.

**Protection and Security :** Çok sayıda process eş zamanlı işletilirken, bir process'in diğer process işleyişine veya bir process'in işletim sisteminin işleyişine karışamıyor olması gereklidir. Bu yüzden bir process, başka bir process'in bellek bölgesine erişemez.

<address>Kaynak : Operating System Concepts ~ Eigthth Edition (s50,s51)</address>