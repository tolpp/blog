---
layout: post
title:  "Sieve of Eratosthenes (Eratosthenes'in Eleği)"
date:   2012-09-27 14:31:00
tags: [algoritmalar, algorithm analysis]
categories: [Algoritmalar]
---

Eratosthenes'in Eleği ya da diğer adıyla Eratosthenes'in Kalburu asal sayıların bulunması için kullanılan eski ve temel yöntemlerden biri.

Algoritma gerçekten bir elek mantığıyla çalışıyor. **N** sayısına kadar tüm asalları bulmak istediğimizde, en küçük asaldan başlayarak bu asalların tüm katları **asal değil** olarak işaretleniyor. **N** sayısına kadar tüm dizi dolaşıldığında **asal değil** olarak işaretlenmeyen tüm sayılar da asal oluyor.

Algoritmanın daha iyi anlaşılabilmesi ve görsel için : [ (Vikipedi) Eratosten kalburu](http://tr.wikipedia.org/wiki/Eratosten_kalburu)

**Pseudocode :**
<script src="https://gist.github.com/tolpp/246f9813c71d92bfd124.js"></script>
**Java :**
<script src="https://gist.github.com/tolpp/cef616c3668714091ca2.js"></script>

<!--Bu yazı <a href="https://tolpp.com/ogrenme-notlari/">öğrenme notları</a>‘nın bir parçasıdır. -->