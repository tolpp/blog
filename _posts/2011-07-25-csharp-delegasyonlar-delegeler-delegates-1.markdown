---
layout: post
title:  "C# - CSharp delegasyonlar (delegeler [delegates]) - 1"
date:   2011-07-25 19:40:00
tags: [csharp, .net]
categories: [.Net]
---

**Delegeler**, birçok programlama dilindeki function pointer'ların C# karşılığı olarak düşünülebilir. Bu pointerlar vasıtasıyla, istediğimiz bir değişkene fonksiyonun geri döndürdüğü değeri değil, fonksiyonun kendisi (aslında fonksiyonun belekteki yeri) atanmış olur. Event mekanizmaları tasarlanırken sıkça kullanılan function pointer, typesafe olmadığından birçok problemlere yol açabilir. C# içindeki delegeler ise typesafetir.

Madem temelde sıradan metodlar gibi,  peki neden delegate kullanılır?

* Delegeler ile birden fazla metodu aynı anda kullanabiliriz.
* Anonim metodlar ile  daha kısa kodlar yazarız.
* Async Delegate kullaranarak, metodların asenkron olarak çalışmasını sağlayabiliriz.
* Delegeleri dizi şeklinde tutarak, metodların döngülerle çağırılmasını sağlayabiliriz.

Örnek bir delege kullanımı :

<script src="https://gist.github.com/tolpp/4edb610618743eeef039.js"></script>

Delegeler hakkında bir sonraki yazı : [CSharp delegates - 2]({{site.baseurl}}/c-csharp-delegasyonlar-delegeler-delegates-2/) 