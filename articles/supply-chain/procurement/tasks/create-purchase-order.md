---
title: Stofna innkaupapöntun
description: Þetta efni sýnir hvernig á að stofna innkaupapöntun handvirkt.
author: RichardLuan
manager: tfehr
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventDimParmFixed, InventItemIdLookupPurchase, InventProductDimensionLookup, PurchTotals
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a3da6b70054fac878ba6266017bffe75f634f61
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016629"
---
# <a name="create-a-purchase-order"></a>Stofna innkaupapöntun

[!include [banner](../../includes/banner.md)]

Þetta efni sýnir hvernig á að stofna innkaupapöntun handvirkt. Dæmigerðara er fyrir innkaupapantanir að stofnast sjálfkrafa sem afleiðing af aðaláætlanagerð, beinni afhendingu og öðrum ferlum. Innkaupapöntun eru yfirleitt stofnaðar af innkaupastjórar. Dæmi sýnd hér er hægt að nota í USMF sýnigögn fyrirtækis með gildum sem eru lögð til í athugasemdir fyrir mismunandi skref.


## <a name="create-the-purchase-order-header"></a>Stofna haus innkaupapöntunar
1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Innkaup og aðföng > Innkaupapantanir > Allar innkaupapantanir**.
2. Veljið **Nýtt**.
3. Veldu lánardrottnalykilinn **US-101.** Þegar þú velur lánardrottinn, upplýsingar úr færslu um lánardrottinn eins og aðsetur, reikningslykil, afhendingarskilmála og afhendingarmáta verður afrituð sem sjálfgefin gildi í pöntunarhaus. Hægt er að breyta þessum gildum hvenær sem er.  
4. Víkkaðu út hlutann **Almennt**.

    - Reiturinn **Svæði** ásamt reitnum **Vöruhús** ákvarða hvar innkeyptar vörur eða þjónusta skulu afhent. Sjálfgefið afhendingaraðsetur er svæðið. Bæði svæðin má fylla með gildi sem sett er upp fyrir valinn lánardrottinn, eða hægt að tilgreina þær handvirkt.  
    - Reiturinn **Afhendingardagur** er notaður til að tilgreina þegar afhenda þarf keypta vöru og þjónustu. Hægt er að tilgreina eina afhendingardagsetningu fyrir pöntun eða fyrir einstakar pöntunarlínum má úthluta einkvæmt afhendingardagsetningar. Ef afhendingardagsetningu sem er tilgreint hér ekki er hægt að uppfylla fyrir tilteknar vörur eða þjónustu þar sem þeir hafa lengri afhendingartíma, þá verða þessar línur stofnuð með fjarlægari afhendingardag til að hliðra til fyrir þessu.  

5. Útvíkkaðu kaflann **Stjórnun**. Hægt er að nota svæðið **Pöntunaraðili** til að tilgreina hver er að panta. Það getur verið hentugt að deila þessu með lánardrottins ef þau þurfa að hafa samband við þann einstakling. Reitnum má úthluta gildi sjálfkrafa ef gildandi notandareikningur tengist heiti á síðunni **Notendur**.  
6. Veljið **Í lagi**. Pöntunarhaus hefur nú verið stofnaður. Þegar unnið er með innkaupapöntunarlínur birtist aðeins útdráttur úr upplýsingar úr haus. Ef þú þarft að skoða afganginn af upplýsingunum skaltu velja **Haus**.  

## <a name="add-a-purchase-order-line"></a>Bæta við innkaupapöntunarlína
1. Velja **Innkaupapöntunarlínu**.
2. Veldu **Víddir**. Afurðir mega vera vöruvíddasamsetningar flokkuð eftir víddir, eins og lit, stærð eða stíl. Einnig er hægt að setja afurðir upp til að nota geymsluvíddir eins og svæði og vöruhús. Það eru einnig valfrjálsar rakningarvíddir, eins og runu og raðnúmer. Hægt er að skilvirkni skráning pantana, er hægt að bæta við víddarsvæði sem þú notar oft beint í hnitanet.  
3. Veldu gátreitinn **Litur**. Valfrjálst: Ef þú velur reitinn **Vista uppsetningu** munu víddirnar sem þú valdir einnig birtast á hnitaneti pöntunarlínu næst þegar þú opnar síðuna innkaupapöntun.  
4. Veljið **Í lagi**.
5. Í svæðið **Vörunúmer** veldu **T0004**.

    - Pöntunarlínur eru stofnaðar fyrir vörur og þjónustu með því að tilgreina vörunúmer eða sem útgjöld með því að tilgreina innkaupaflokk. 
    - Flokksreiturinn **Innkaup** er notaður til að bæta línum við þar sem innkeyptar vörur eru gjaldfærðar beint, frekar en að fara inn í birgðir. Það merkir að ef gjaldfæra á innkaup er hægt að gera það með því að stofna innkaupapöntunarlínu sem tilgreinir innkaupategund frekar en að stofna línu með vörunúmeri. Vörur má einnig tengja innkaupaflokki og í því tilfelli er innkaupategund sýnd sem upplýsingar aðeins.  

6. Í reitinn **Litur** skal færa inn eða velja gildi. Reitirnir **Svæði** og **Vöruhús** eru yfirleitt útfylltir með gildum úr pöntunarhaus, en hægt er að hnekkja reitunum ef sumar línur þarf að afhenda á mismunandi stöðum.  
7. Í reitnum **Magn** slærðu inn tölu.

    - Tilgreinið magnið sem á að kaupa. Reiturinn **Magn** er sjálfkrafa fylltur út með minnsta pöntunarmagn afurðar ef þetta er sett upp, eða með gildinu 1.  
    - Í reitnum **Eining** er gefin til kynna mælieining fyrir pantað magn. Venjulega er einingin er sjálfkrafa gefið úr innkaupaeiningu á afurðarsniðmáti, en hægt er að breyta þessu.  
    - Yfirleitt inniheldur reiturinn **Einingarverð** gildi úr annaðhvort innkaupasamningi eða viðskiptasamningi. Hægt er að breyta einingarverðinu í einstaka pöntunarlínum, til dæmis ef samið er um einkvæmt verð við lánardrottininn.  
    - Reiturinn **Afsláttur** inniheldur afsláttarupphæð á einingu. Þessi afsláttur minnkar því einingarverð samkvæmt afsláttinn. Þennan afslátt er yfirleitt fengið sjálfkrafa frá innkaupasamningum eða viðskiptasamninga en mögulegt er að hnekkja honum í einstökum línum ef einkvæmt afsláttur hefur verið samið við lánardrottininn.  
    - Afsláttarprósenta er hægt að færa inn sem minnkar nettóupphæð línunnar, samkvæmt því. Þessi afsláttarprósenta er oft fengið sjálfkrafa frá innkaupasamningum eða viðskiptasamninga en mögulegt er að hnekkja honum í einstökum línum ef einkvæmt afsláttarprósenta hefur verið samið við lánardrottininn.  
    - Gildið í reitnum **Nettóupphæð** er reiknað úr öðrum reitum í línunni, þar með talið magni, einingarverði, afslætti og afsláttarprósentu. Hægt er að breyta nettóupphæðinni en þá verða reitirnir **Einingaverð**, **Afsláttur** og **Afsláttarprósenta** auðir og þegar bókað er á línuna verður bókuð upphæð í hlutfalli við nettóupphæðina. Yfirleitt er reiturinn **Nettóupphæð** einungis notaður til að birta nettóupphæð línunnar.  

8. Útvíkkaðu hlutann **upplýsingar Línu**.
9. Veldu flipann **Afhending**. Hægt er að úthluta einkvæmri afhendingardagsetningu á hverja pöntunarlínu. Dagsetningin kemur úr svæðinu á haus innkaupapöntunar, en hægt er að breyta þessu.  

## <a name="review-order-totals"></a>Fara yfir samtölu pöntunar
1. Veldu **Samtals**.

    - Ef aðgerðin **Samtölur** sést ekki skal velja **Innkaupapöntun** á aðgerðasvæðinu.  
    - Svarglugginn sýnir samtölur fyrir alla pöntunina.  
    - Reiturinn **Val** gerir þér kleift að breyta grundvellinum sem notaður er til að reikna samtölur. Til dæmis gætirðu valið **Magn á innhreyfingarskjali afurða** til að sýna samtölur sem tengjast fjölda afurða sem hafa verið mótteknar, eða **Pantað magn** til að sýna fjölda pantaðra afurða.  

2. Veljið **Í lagi**.

