---
layout: post
title:  "Solr “Undefined field text” hatası"
date:   2012-07-26 01:55:00
tags: Solr, Apache
categories: Science
mathjax: false
---

org.apache.solr.common.SolrException: undefined field text şeklinde bir hata alıyorsanız muhtemelen schema.xml içerisinde tanımlanmamış bir “text” fieldını solrconfig.xml içerisinde kullanmanızdan kaynaklanıyordur.

Yeni başlayan çoğu insan gibi ben de Solr ile beraber gelen example üzerinden gitmiştim. Kendi yapıma uygun şekilde schema.xml dosyası içerisinde tüm değişiklikleri tamamladım.”text” isimli bir field’a ihtiyacım olmadığından da schema.xml içerisinden kaldırdım.  Ancak solrconfig.xml içerisinde default search field olarak text atandığından bulunamayan “text ” field’ı için exception yemeye başladım.

Siz de example üzerinde değişiklik yapmşsanız soruna şu iki şey sebebiyet veriyor olabilir :

1. solrconfig.xml içerisinde<str name=”qf”> vb.  tagler içerisinde value olarak text kullanılması.
2. schema.xml içerisinde copyField vb. olarak text kullanılması.
Yani işin özü yaratmamış olduğunuz text field’ını herhangi bir yerde kullanmamanız gerekiyor.