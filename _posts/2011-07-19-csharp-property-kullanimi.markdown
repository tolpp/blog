---
layout: post
title:  "C# - CSharp property kullanımı"
date:   2011-07-19 20:11:00
tags: [csharp, .net]
categories: [.Net]
---

Property, C#'ta get ve set metodları kullanmadan private değişkenlere erişimi sağlayan, encapsulation olayını güzelleştirerek OOP'i zevkli hale getiren bir hededir.

bir değişken içindeki veriye ulaşabilmek için 40 takla atmanıza, propertyler sayesinde gerek kalmaz.

Örnek :
<script src="https://gist.github.com/tolpp/cedc4d19a21dcf5d8281.js"></script>
Bu da bize getIsim() setIsim(string isim) gibi fonksiyonlarla uğraşmak yerine, veriye örnekteki gibi kolaylıkla ulaşmamızı sağlar:

Ayrıca, get ve set alanlarının içi istenildiği şekilde değiştirilerek kontroller yapılabilir, istenen değer atanabilir. Veya, get veya set 'lerden istediğimizi yazmayarak, propertinin salt okunur veya salt yazılır olmasını sağlayabiliriz.

Propertylerin diğer bir güzelliği de, metodlara göre daha hızlı çalışmaları. Yazılmış program JIT compiler ile derlenirken, property'ler inline yapılarak intermediate language haline getiriliyormuş*.

*Kaynak : Professional C# 2005 with .NET 3.0 : Nagel, Evjen, Glynn,Watson,Skinner