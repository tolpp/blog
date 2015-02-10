---
layout: post
title:  İşletim Sistemi Ne Yapar?
date:   2012-01-25 14:31:00
tags: Application Programs, Control Program <!--"Application Programs","Control Program", "Resource Allocator", "System Programs", "System View", "User View" -->
categories: Operating Systems
---

Bir bilgisayar sistemi donanım (hardware), işletim sistemi (operating system), uygulama programları (application programs) ve kullanıcılar (users) olmak üzere 4 bölümde incelenebilir.

Hardware sistem için temel kaynakları sağlar.  İşlemci (CPU), bellek, Girdi/Çıktı cihazları (I/O devices) gibi.

Application programs kullanıcıların problemlerini çözmek için donanım kaynaklarını kullanan yazılımlardır. Spreadsheet, Web tarayıcıları, derleyiciler gibi.

Operating system ise hardware, application programs ve users arasında köprü görevi görür. Hardware'ı kontrol eder ve birçok user'ın birçok application programda çalışmasına izin verir.

### User View

Bir bilgisayarı kullanan kişinin (kullanıcı/user) görüşü kullanılan arayüz'e göre değişir.

Birçok kullanıcı monitör, klavye, fare ve sistem parçalarından oluşan bilgisayarları kullanır. Bu tür bilgisayarlara kişisel bilgisayar(PC/Personal Computer) diyoruz. Bu tür sistemler bir kullanıcının tüm kaynakları tekeline alması için tasarlanmıştır. Burada amaç kullanıcının yapacağı işin performansını en üst seviyeye çıkarmaktır. Bu tür bilgisayarlarda kullanılan işletim sistemi kolay kullanım sağlar. İşletim sisteminin asıl amacı performanstır ve kaynak kullanımını (resource utilization) çok kullanıcıya dağıtma amacı gütmez.

Diğer tür bilgisayarlar kullanıcıların terminalleri kullandıklarıdır. Burada, merkezde çalışan bir mainframe veya minicomputer vardır. Tüm kullanıcılar terminaller vasıtasıyla bu ana bilgisayara bağlanır. Bu tür bilgisayarlarda kullanılan işletim sisteminin asıl amacı kaynak kullanımını (resource utilization) en üst seviyeye çekmektir.

Üçüncü tür bilgisayarlar, kişilerin workstation kullandıklarıdır. Bir workstation diğer workstationlara ve serverlara bağlıdır. Kullanıcıların kendilerine ait kaynakları (resources) vardır fakat aynı zamanda network üzerinde paylaşılan kaynakları da kullanırlar. (dosya saklama, hesaplama yapma, çıktı alma gibi). Bu tür bilgisayarlarda kullanılan işletim sistemi kullanılabilirlik (usability) ve kaynak kullanımını (resource utilization) orantılı şekilde yüksek tutmalıdır.

Dördüncü tür bilgisayarları el bilgisayarları, tabletler, akıllı telefonlar olarak düşünebiliriz. Bu tür cihazların azı artık bağımsız olarak çalışmaktadır. Çoğu kablosuz olarak bir ağa dahildir. Bu tür cihazlar fazla güç harcamamaları için çok hızlı değildir. Bu yüzden de arayüzleri limitlidir. Bu tür bilgisayarlarda bulunan işletim sistemi, bireysel kullanımı kolaylaştırmayı hedefler. Ancak pil ömrü diye bir problem olduğundan olabildiğince az güç tüketmeye çabalar.

Bazı bilgisayarlar ise user view çok az olabilir veya hiç olmayabilir. Evdeki bazı embedded cihazlar, otomobillerdeki bazı embedded bilgisayarlar. Bu tür bilgisayarlar için tasarlanan işletim sistemleri daha çok kullanıcı müdahalesi olmadan çalışabilmesi için tasarlanır.

### System View

*Resource Allocator :* İşletim sistemi bir kaynak ayırıcısıdır. Bir bilgisayar sisteminde birçok kaynak vardır ve bunlar CPU Time, memory space, file-storage space problemlerinin çözümünü gerektirir. OS, bu kaynakların hangi programlar tarafından nasıl kullanacağını belirler. Resource allocation, özellikle çok kullanıcılı bilgisayarlarda hayati önem taşır.

*Control program :* İşletim sistemi bir kontrol programıdır. Control program user programlarının çalışmasını yönetir. Hatalardan korur ve yanlış kullanımı önler. Ayrıca I/O cihazlarıyla da control program ilgilenir.

###İşletim Sisteminin Tanımı

İşletim sistemi için tam bir tanım yapmak mümkün değildir. İşletim sistemleri vardır çünkü kullanılabilir bilgisayar sistemleri kullanılarak problem çözümünde makul çözüm yolları sunarlar.

Bilgisayar sisteminin temel görevi kullanıcı programlarını çalıştırmak ve kullanıcı problemini kolaylıkla çözmektir. Bu amaçla ilk olarak bilgisayar donanımı geliştirildi. Donanımın kendi başına kullanımının zor olduğu anlaşıldığındaysa application programlar geliştirildi. Bu application programların birleştirilip tek bir noktadan çalıştırılan halin işletim sistemi (operating system) diyebiliriz.

İşletim sistemini hangi parçaların oluşturduğu da kesin değildir. Ancak bir işletim sistemini kernel, system programs ve application programs olarak incelemek mümkündür.

*Kernel :* İşletim sistemi çalıştığı süre boyunca çalışan program. İşletim sisteminin çekirdeği. Bilgisayar açılır açılmaz memorye yüklenen program.

*System Programs :* Kernel parçası olmayan, ancak bilgisayarın çalışmasını etkileyen, düzenleyen programlar. Sürücüler (drivers) bu gruba alınabilir

*Application Programs :* İşletim sistemiyle doğrudan ilişkili olmayan programlardır. Daha çok kullanıcıların işlerini halletmeye yöneliktir.

<address>Kaynak : Operating System Concepts ~ Eight Edition (s3,s4,s5,s6)</address>