---
layout: post
title:  "C# – CSharp delegasyonlar (delegeler [delegates]) – 2"
date:   2014-09-16 15:55:00
tags: [.net, csharp, delegate]
categories: [.Net]
---

Merhaba,

3 yıl önce delegeler hakkında bir şeyler [yazmıştım]({{site.baseurl}}/csharp-delegasyonlar-delegeler-delegates-1/). X bilişim firması çalışanı bir kişi pek açıklayıcı bulmamış o yazıyı.

Neyse, daha açıklayıcı bir örnekle ve gündelik kullanıma daha yakın şekilde yeniden delegete'lerden bahsedecek olursak ;

Özetle **Delegeler**, belli bir olay sonrasında çalıştırılması gereken metodların olay yeri tarafından bilinmeksizin çalıştırılmasını sağlayan yapılardır. En temel örnek olarak [System.EventHandler](http://msdn.microsoft.com/en-us/library/system.eventhandler) gösterilebilir. Windows Forms içerisinde kullanılan default tüm click, load eventlarının handle edilmesi için bu delegate kullanılır.

Benzeri şekilde kendi delegemizi oluşturacak olursak;
<script src="https://gist.github.com/tolpp/b89aa394a10959ccd366.js"></script>

Yukarıda UserEventHandler isminde, kullanıcı işlemleri için kullanılacak bir delegate yaratılmıştır. Bu tanımlama class seviyesinde, doğrudan namespace içerisinde yapılmıştır.

UserContext içerisinde kullanıcının yaratılma işlemi sırasında sırayla çağrılması gereken metodlar UserCreated isimli UserEventHandler isimli delegate içerisinde atılmıştır. 

Bu sayede, CreateUser metodu içerisinde UserCreated delegate'i bir kez çağrılarak SaveUserToDatabase, SendRegisterationSmsToUser ve NotifyManager metodları da aynı anda çağrılmış olur. Bu durum için delegate kullanımının en büyük artısı, kullanıcı yaratımından sonra hangi işlemlerin yapılacağı kısmı ile CreateUser metodunun ilgilenmemesidir. Delegate sayesinde CreateUser metodu ile diğer işlemleri birbirinden ayırmış olduk (bkz. [loose coupling](http://en.wikipedia.org/wiki/Loose_coupling))