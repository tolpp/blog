---
layout: post
title:  "Java Configurations Dosyası ve Properties"
date:   2012-06-21 23:30:00
tags: Java
categories: Java
mathjax: false
---
Konfigurasyon dosyaları, sonradan düzenlenebilir çeşitli ayar verilerine ve pek değişmeyeceği düşünülen bağlantı verilerine sonradan kolayca erişilebilip kod üzerinde oynamaksızın programın işleyişini değiştirmek amacıyla kullanabileceğimiz dosya yapılarıdır. Buradaki verilere java.util.Properties sınıfını kullanarak ulaşılabilir.

Kolay bir örnek dosya aşağıdaki gibidir.
<script src="https://gist.github.com/tolpp/8d1d3548df9f91cbbdbe.js"></script>

İşlem sonrasında config.properties dosyasının içeriği de aşağıdaki gibi olacaktır :
	
	dbpassword=password
	database=default
	dbuser=root