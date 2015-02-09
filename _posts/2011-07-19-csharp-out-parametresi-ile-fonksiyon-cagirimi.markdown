---
layout: post
title:  "C# - CSharp out parametresi ile fonksiyon çağırımı"
date:   2011-07-19 17:12:00
tags: CSharp
categories: ".Net"
---

Bir metodu void olarak kullanmamıza rağmen metod içindeki bir veya birden fazla değer almak istiyorsak, out veya ref parametresini kullanabiliriz. ref parametresi dediğim, call-by-referance anlamına geliyor. out parametresi de bu parametreye oldukça benziyor. 

Ancak ref ve out parametresi arasında farklar var. Şöyle ki :

1. out parametresi ile gönderilen bir değişkenin değeri metodun içinde kullanılamaz
2. metod içinde yeni bir değişken yaratılır, fonksiyon sonlanırken referansi metoda gönderilen değişkeninkine atanır
3. metoda out parametresiyle gönderilen bir değişkene ilk değer atanması zorunlu değildir

**Hız? Bellek?**

Tıpkı referans ile veri göndermede olduğu gibi, out parametresiyle gönderilen veri de bellek kullanımını azaltıyor. Ayrıca verinin kopyalanması sırasında harcanan süreden de kurtulmuş oluyoruz. Yani, hem hızlı hem de az bellek kullanımını sağlıyor diyebiliriz. 

Örnek :
<script src="https://gist.github.com/tolpp/a0f2e92149811cde05b7.js"></script>