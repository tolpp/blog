---
layout: post
title:  "Dynamic Dispatch nedir?"
date:   2011-05-05 13:59:00
tags: [dynamic dispatch, programming languages, programlama dilleri]
categories: [Terimler]
---
Subclass içinde override edilmiş(overload değil!) bir metod çağırıldığında, subclass içindekinin mi yoksa superclass içindekinin mi çağırılacağının run-time sırasında dinamik olarak belirlenmesine Dynamic Dispatch denir.

Hemen bir örnekle :
<script src="https://gist.github.com/tolpp/6d9b02e5ea911fd5daa1.js"></script>
şeklinde iki class'ım olsun. Kopek sınıfımı, Hayvan sınıfımdan türetmiş olayım. Aşağıdaki işlem sırasında;
<script src="https://gist.github.com/tolpp/6154f17f9edbea9ce665.js"></script>
minnos'un çıkaracağı ses bellidir -&gt; "AbidikGubidik"
fino.sesCikar() fonksiyonu çağırıldığındaysa Dynamic Dispatch yapılır. fino'nun referansı hayvan olsa bile, Kopek sınıfıyla initialize edildiğinden fino "BarkHavBarkHav" sesi çıkaracaktır.

**Not :** Java'da override ettiğiniz bir metodun önüne @Override notunu(annotation) yazmasanız da olur. Yazarsanız, compile time errorların azalmasına, compilerın daha kolay işini görmesine yardımcı olursunuz.