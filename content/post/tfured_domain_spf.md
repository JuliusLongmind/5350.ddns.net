---
title: A tiszafured.hu domain email kommunikációja külső domain -ek felé
author: Julius Longmind
date: '2020-03-09'
lastmod: 2020-03-10T14:30:25+01:00
slug: tfured_domain_spf
show_thumb_in_post: false
thumbnail: "https://33hf181dgl251b9am73x5nbw-wpengine.netdna-ssl.com/wp-content/uploads/2018/03/SPF-1.png"
categories:
  - Domain
  - tiszafured.hu
  - Önkormányzat
tags:
  - Email
draft: yes
---

A 2020. évi költségvetésről tartott testületi ülés meghívóját a testület tagjai közül többen több napos késéssel kapták meg, melyet Tiszafüred helyettes jegyzője az ülés FB -os közvetítése során egy jól ismert, régmúltra visszatekintő problémaként mutatott be.

<!--more-->

Egy "lelkes" civil aktivista szakértő az alábbi hibaüzenetet fedezte az email fejlécében, mely a felületes szemlélőnek eléggé unalmas, de a lényegre rávilágít.

> Received-SPF: neutral (google.com: 80.249.160.197 is neither permitted nor denied by best guess record for domain of non_public_emailaddress@tiszafured.hu) client-ip=80.249.160.197;
> Authentication-Results: mx.google.com;
>       spf=neutral (google.com: 80.249.160.197 is neither permitted nor denied by best guess record for domain of non_public_emailaddress@tiszafured.hu) smtp.mailfrom=non_public_emailaddress@tiszafured.hu

#### A lényeg:

"To make sure gmail will deliver emails from your private servers i.e. on your own domain and not a well known public email domain, you MUST have defined the SPF records correctly for your domain."

"Annak biztosítása érdekében, hogy a gmail e-maileket forgalmazzon egy magánszerverről - azaz a saját domainről, nem pedig egy közismert nyilvános e-mail tartományból, jól KELL meghatároznia az SPF-rekordokat a domainjéhez."

Az SPF -ről bővebben *[itt](http://www.open-spf.org/Introduction)*.

Az alábbi képen a google saját elemző eszközével a következőt sikerült vizuálisan kideríteni. Aki már olvasgatott email fejlécet, az biztosan egyetért velem abban, hogy az alábbi formában sokkal élvezhetőbb és érhetőbb a dolog.

[![Email késleltetése](http://5350.ddns.net//images/3days_delay_email.png) Email késleltetése a 2020 -as évi költségvetés anyagával](http://5350.ddns.net//images/3days_delay_email.png)

Ezek után hellyel-közzel az alábbi szöveget juttatta el az egyik képviselő a helyettes jegyzőhöz:

>Tehát, megvizsgálva a kiküldött meghívó email fejlécét, szakértőnk a következő megállapításra jutott:
>
>A tiszafured.hu domain szolgáltatójánál (a [Silihost](https://www.silihost.hu/)  -nál) technikai probléma van a domain (SPF) rekordok esetében. Az Önkormányzatnak kell a szolgáltatóval javíttatni ezt a hibát!!!
Továbbá, a "Kézbesítési értesítések" bekapcsolásával kell figyelni vagy ellenőrizni a kézbesítést az Önkormányzatnál - a kliens oldalon, mégpedig úgy, hogyha valamelyik címzett esetében nem érkezik meg a visszaigazolás, akkor a szolgáltatónál jelezni kell, hogy elakadt az email szolgáltatás. Erre annak a személynek kell ügyelni, aki az emailt kiküldi, ha már hivatalos emailről van szó (vagy alternatív szolgáltatón, privát emailen keresztül küldeni ki az emailt azoknak, akikről sejthető, hogy nem kapták meg az anyagot a visszaigazolás hiánya alapján).
>
>Egyébiránt ennek a problémának a megoldása nem új email címek kiosztásában keresendő, mert ezzel a tiszafured.hu levelezése továbbra is megbízhatatlan marad, ami további konfliktusok forrása. Szakmai megoldásra van szükség, amely a probléma okánál keresi a megoldást és nem megkerülni akarja.

**Közben eltelt közel 1 hónap.** Hallomásból kapva az információt, ez idő alatt az önkormányzat "szakértő" -je az időzónák közötti eltéréssel, felháborodva utasította el, hogy valami hiba lehet a tiszafured.hu domain -val. Kíváncsiságból felkértük szakértőnket, hogy ellenőrizze 1 hónap alatt, milyen változást sikerült eszközölni, de mint az alábbi ábra mutatja ...

[![SPF rekord a tiszafured.hu domain -hez](http://5350.ddns.net//images/tfured_spf_rec.png) A tiszafured.hu online SPF rekord vizsgálata](http://5350.ddns.net//images/tfured_spf_rec.png)

...SEMMIT!!!  :tired_face: Nem található SPF rekord a tiszafured.hu domain -hez, annak ellenére sem, hogy a megoldás tálcán van kínálva!?  :disappointed:

Ugyanakkor meglepő csend van az ellenzékiek részéről is (és itt szándékosan nem írtam "összefogás" -t) a dologgal kapcsolatban ahhoz képest, hogy mekkora hangsúlyt fektettek a megkésett emailek miatti információhiány kommunikációjára.

#### Nos, ime egy fontos, de semmilyen erőfeszítést nem igénylő problémamegoldásnak a története Tiszafüredről.

UPDATE: 2020.03.10

Az alábbi képen látható problémák merültek még fel a tiszafured.hu domain -val kapcsolatban.

[![A tiszafured.hu domain -val kapcsolatos problémák](http://5350.ddns.net//images/tfured_domain_issue.png) A tiszafured.hu online domain ellenőrzése](http://5350.ddns.net//images/tfured_domain_issue.png)