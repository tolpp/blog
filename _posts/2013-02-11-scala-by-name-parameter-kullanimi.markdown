---
layout: post
title:  "Scala “By-Name Parameter”(=>) kullanımı"
date:   2013-02-11 07:06:00
tags: [scala]
categories: [Scala]
---
Scala'da foksiyon içerisinde fonksiyon yaratılabiliyor, bu fonksiyonlar bir referansa atanabiliyor ve parametre olarak başka bir fonksiyona gönderilebiliyor. Bu işlemi kitaplarda "function values" ya da "pass-by-name" olarak bulmanız mümkün.

Bu da kod içerisindeki metodun farklı şekillerde kullanılabilmesini sağlıyor. Örneğin verilen bir liste üzerinde toplama işlemi yapan bir metod kolay bir şekilde tek sayılar üzerinde toplama işlemi yapan hale getirilebiliyor.

Bir örnekle :
<script src="https://gist.github.com/tolpp/6d2913979650da688359.js"></script>
Peki, yukarıda ne oldu?

* sumList(myList:List[Int], realVal:Int => Int)metodu birinci parametre olarak toplanacak sayıların tutulduğu integer listesini aldı. İkinci parametre olaraksa realVal ismindeki, dışarıdan tek parametreli Int değeri alan ve geriye Int değer döndüren bir kod bloğu verildi. Bu sayede realVal'ı bundan sonra realVal(a) şeklinde kullanabiliyor olduk.
* Eğer parametre realVal : (Int,Int)  => String olarak tanımlanmış olsaydı, vereceğimiz kod bloğu iki parametre alan ve String döndüren bir kod bloğu olmalıydı.
* 7\. ve 9. satırlarda doğrudan çağırıldığı yere kod bloğu yerleştirildi.
* 8\. ve 10. satırlarda ise, aynı görevi yapacak fonksiyonlar doğrudan parametre olarak yollandı.
* 11\. satır hatalıdır. Çünkü çağırılacak fonksiyonun ismi bekleniyor.

Yukarıdaki kodun konsol çıktısı aşağıdaki gibi olur :
<script src="https://gist.github.com/tolpp/da8cafcdbcf96b022682.js"></script>

Bu sayede, tek bir toplama metodu ile birden fazla işi yapan toplama metoduna sahip olmuş olduk. Scala'nın sahip olduğu metodları incelerseniz, dışarıdan kod bloğu verebildiğiniz pek çok metod olduğunu görebilirsiniz.