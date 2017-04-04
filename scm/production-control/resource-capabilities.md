---
title: Tilfangageta
description: "Þessi grein gefur upplýsingar um tilfangagetu. Geta er hæfni rekstrartilfanga til að framkvæma tiltekinn verkþátt. Greinin útskýrir hvernig getu og tengdum hugtökum, svo sem Færnistig og forgang, eru notaðar til að velja viðeigandi tilföng fyrir aðgerð."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WrkCtrCapability, WrkCtrTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 29961
ms.assetid: 30e38233-2a64-4070-911f-8ffd78dd8281
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 4463ca8e11115eb83323716faa4ed6b38937a3e4
ms.lasthandoff: 03/31/2017


---

# <a name="resource-capabilities"></a>Tilfangageta

Þessi grein gefur upplýsingar um tilfangagetu. Geta er hæfni rekstrartilfanga til að framkvæma tiltekinn verkþátt. Greinin útskýrir hvernig getu og tengdum hugtökum, svo sem Færnistig og forgang, eru notaðar til að velja viðeigandi tilföng fyrir aðgerð.

Geta er hæfni rekstrartilfanga til að framkvæma tiltekinn verkþátt. Rekstrartilföng°geta haft fleiri en einni getu úthlutað og getu er hægt að úthluta fleiri en einu tilfangi. Til að úthluta getu rekstrartilföngum fyrir takmarkaðan tíma, þarf að skilgreina upphafs og gildistíma kortsins á úthlutun getunnar. Þegar geta fyrir tilfang rennur út getur tilfanginu ekki verið áætlað á verk eða framleiðslu sem krefst þeirrar getu. Hægt er að endurnýja getu sem er útrunnin. Hægt er að eyða getu, svo lengi sem þær eru í leiðartengslum eða hluti af framleiðsluleið á framleiðslupöntun sem er virk. Almennt séð, skal fara varlega þegar getu er eytt. Í staðinn skal hafa í huga að leiðrétta lokadag á tilföngum sem hafa þá getu. Hægt er að úthluta getu á öllum gerðum tilfanga: Verkfæri, lánardrottinn,vél, staðsetning, aðstaða eða mannauður.

## <a name="level"></a>Stig
Mörg tilföng hafa oft sömu getu til virkni en á mismunandi færnistigum (t.d. styrkleikar, vinnsluhrað eða°nákvæmni). Þess vegna, þegar getu er úthlutað á tilföng, er hægt að tilgreina **Stig** gildi. Stig er einfalt tölugildi. Ef tilgreint er að geta er tilfangakrafa fyrir framleiðsluleið, er einnig hægt að tilgreina gildið°**Lágmarksstig sem þarf** fyrir þá getu. Röðunarvélin velur þá aðeins°tilföng°sem hafa nauðsynlega getu á stigi sem er jafnt eða°meira en lágmarksstig sem tilgreint er í tilfangakröfunni.

## <a name="priority"></a>Forgangur
Rekstrartilföngum sem hafa sömu getu er hægt að úthluta forgangi. Svo ef mörg tilföng hafa getu sem uppfylla röðun þarfir stigi áskilinn og hefur ókeypis afkastagetu, röðunarvélin hægt að velja þau tilföng. Ef **Forgang** er valin í á **Aðalval tilfanga** á í **færibreytur Röðunar** síðuna tilfang hefur mestan forgang (lægsta tölulegt gildi í á **Forgang** svæði) er valin fyrsta við röðun.

## <a name="resource-requirements"></a>Tilfangaþörf
Þegar tilfangaþarfir fyrir framleiðsluleið er skilgreindar er hægt að tilgreina eina eða fleiri getu sem þarfir. Við framleiðsluröðun,er geta sem er skilgreind í tilfangaþarfir í leiðaraðgerð tengd við getu sem eru skilgreind fyrir tilföngin. Tilföng sem hafa getu sem uppfylla skilyrði eru valin. Ef mörg tilföng hafa sömu virknigetu en°mismunandi kosti (t.d. styrkleikar, vinnsluhraða eða nákvæmni) er hægt að skilgreina margar getur eða°nota getustigið til að viðurkenna getu tilfangsins. Eftirfarandi er dæmi:

-   Á leið, er vinnslutími borunar stillur á 10 einingar á klukkustund, en þörf sjálf er skilgreind sem Borun.
-   Þú ert með tvær borvélar, M1 og M2.
-   Borunargetu er úthlutað á bæði tilföng, M1 vélina°og M2 vélina.
-   Vél M1 getur borað tvær einingar á klukkustund og M2 vélin getur borað 11 einingar á klukkustund.

Í þessu dæmi geta báðar vélarnar verið valdar af röðunarvélinni  þar sem báðar uppfylla grunngetukröfur (Borun). Hins vegar getur vél M1 aðeins borað tvær einingar á klukkustund. Þar sem þetta hlutfall er mikið minna en þær 10 einingar á klukkustund sem eru tilgreindar á leiðinni, mun M1 vél valda vandamálum í framleiðslu ef hún er valin. Það eru tvær leiðir til að leysa þetta vandamál og ganga úr skugga um að M2 vélin é valin í staðinn:

-   Stofna°tvær aðskildar getur: Lághraðaborun og Háhraðaborun. Skilgreina Lághraðaborun°sem borun sem hefur vinnslutíma á bilinu ein til níu einingar á klukkustund. Skilgreina Háhraðaborun sem borun sem hefur vinnslutíma á bilinu 10 til 19 einingar á klukkustund. Síðan úthluta vél M1 Lágri hraða drilling getu og úthluta vél M2 High-speed drilling getu. Loks breyta tilfangaþörf getu á leiðinni High-speed bakköfun. Röðunarvélin mun velja rétta vél (M2).
-   Notið getustig til að viðurkenna Borunargetu sem er úthlutað til borvélanna. Tilgreina vél M1 hefur Þetta getu á stigi 2.0 og M2 vél hefur Þetta getu á stigi 11.0. Tilgreinið 10.0 er lágmarksstig sem krafist er fyrir Þetta getuþörf á leiðinni. Röðunarvélin mun þá ákvarða að aðeins vél M2 uppfylli tilfangaþarfir.

## <a name="competencies-for-human-resources"></a>Hæfni fyrir mannauð
Þegar þú ert með rekstrartilföng af gerðinni **Mannauður** sem eru tengd við starfsmenn í Mannauði, getur þú einnig nýtt hæfni starfsmanna þegar tilfangaþörf fyrir framleiðsluleið er skilgreind. Með öðrum orðum, er einnig hægt að tilgreina þarfir fyrir ákveðna hæfni, námskeið, skírteini eða titla. Áætlunarkerfið getur svo valið tilföng sem eru tengd við starfsmenn og valið mun byggjast á hæfni þeirra starfsmanna. Hæfni er sett upp í Mannauði, ekki á síðunni **Tilfangageta** síðu. Þegar um er að skilgreina hæfni, námskeið, skírteini og titla sem tilfangaþarfir, verður á mannauðseiginleikann og tengja hvern tilföng í **mannauður** gerð samsvarandi starfsmann. Ef ekki eru kostnaðarjafnaðar er að nota mannauð aðgerðum er hægt að skilgreina getu á er **tilfangagetu** síðu sem resemble tvítekin hæfni úr mannauðs. Hins vegar inniheldur síðan **Tilfangageta** ekki virkni sem krafist er til að vinna með hæfni, námskeið, vottanir eða titla.


