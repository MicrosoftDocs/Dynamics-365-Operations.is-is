---
title: Tilfangageta
description: "Þessi grein gefur upplýsingar um tilfangagetu. Geta er hæfni rekstrartilfanga til að framkvæma tiltekinn verkþátt. Greinin útskýrir hvernig getu og tengdum hugtökum, svo sem Færnistig og forgang, eru notaðar til að velja viðeigandi tilföng fyrir aðgerð."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: f6b4ccf4d7f9727819831b07221d859e3c5cdd39
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="resource-capabilities"></a>Tilfangageta

[!include[banner](../includes/banner.md)]


Þessi grein gefur upplýsingar um tilfangagetu. Geta er hæfni rekstrartilfanga til að framkvæma tiltekinn verkþátt. Greinin útskýrir hvernig getu og tengdum hugtökum, svo sem Færnistig og forgang, eru notaðar til að velja viðeigandi tilföng fyrir aðgerð.

Geta er hæfni rekstrartilfanga til að framkvæma tiltekinn verkþátt. Rekstrartilföng°geta haft fleiri en einni getu úthlutað og getu er hægt að úthluta fleiri en einu tilfangi. Til að úthluta getu rekstrartilföngum fyrir takmarkaðan tíma, þarf að skilgreina upphafs og gildistíma kortsins á úthlutun getunnar. Þegar geta fyrir tilfang rennur út getur tilfanginu ekki verið áætlað á verk eða framleiðslu sem krefst þeirrar getu. Hægt er að endurnýja getu sem er útrunnin. Hægt er að eyða getu, svo lengi sem þær eru í leiðartengslum eða hluti af framleiðsluleið á framleiðslupöntun sem er virk. Almennt séð, skal fara varlega þegar getu er eytt. Í staðinn skal hafa í huga að leiðrétta lokadag á tilföngum sem hafa þá getu. Hægt er að úthluta getu á öllum gerðum tilfanga: Verkfæri, lánardrottinn,vél, staðsetning, aðstaða eða mannauður.

## <a name="level"></a>Stig
Mörg tilföng hafa oft sömu getu til virkni en á mismunandi færnistigum (t.d. styrkleikar, vinnsluhrað eða°nákvæmni). Þess vegna, þegar getu er úthlutað á tilföng, er hægt að tilgreina **Stig** gildi. Stig er einfalt tölugildi. Ef tilgreint er að geta er tilfangakrafa fyrir framleiðsluleið, er einnig hægt að tilgreina gildið°**Lágmarksstig sem þarf** fyrir þá getu. Röðunarvélin velur þá aðeins°tilföng°sem hafa nauðsynlega getu á stigi sem er jafnt eða°meira en lágmarksstig sem tilgreint er í tilfangakröfunni.

## <a name="priority"></a>Forgangur
Rekstrartilföngum sem hafa sömu getu er hægt að úthluta forgangi. Þannig að ef mörg tilföng hafa getu sem uppfylla röðunarkröfur á tilætluðu stigi og hafa frjálsa afkastagetu, getur röðunarvélin valið milli þeirra tilfanga. Ef **Forgangur** er valinn á svæðinu **Aðalval tilfanga** á síðunni **Röðunarfæribreytur** er það tilfang sem hefur mestan forgang (lægsta tölulegt gildi á reitnum **Forgangur**i) valið fyrst við röðun.

## <a name="resource-requirements"></a>Tilfangaþörf
Þegar tilfangaþarfir fyrir framleiðsluleið er skilgreindar er hægt að tilgreina eina eða fleiri getu sem þarfir. Við framleiðsluröðun,er geta sem er skilgreind í tilfangaþarfir í leiðaraðgerð tengd við getu sem eru skilgreind fyrir tilföngin. Tilföng sem hafa getu sem uppfylla skilyrði eru valin. Ef mörg tilföng hafa sömu virknigetu en°mismunandi kosti (t.d. styrkleikar, vinnsluhraða eða nákvæmni) er hægt að skilgreina margar getur eða°nota getustigið til að viðurkenna getu tilfangsins. Eftirfarandi er dæmi:

-   Á leið, er vinnslutími borunar stillur á 10 einingar á klukkustund, en þörf sjálf er skilgreind sem Borun.
-   Þú ert með tvær borvélar, M1 og M2.
-   Borunargetu er úthlutað á bæði tilföng, M1 vélina°og M2 vélina.
-   Vél M1 getur borað tvær einingar á klukkustund og M2 vélin getur borað 11 einingar á klukkustund.

Í þessu dæmi geta báðar vélarnar verið valdar af röðunarvélinni  þar sem báðar uppfylla grunngetukröfur (Borun). Hins vegar getur vél M1 aðeins borað tvær einingar á klukkustund. Þar sem þetta hlutfall er mikið minna en þær 10 einingar á klukkustund sem eru tilgreindar á leiðinni, mun M1 vél valda vandamálum í framleiðslu ef hún er valin. Það eru tvær leiðir til að leysa þetta vandamál og ganga úr skugga um að M2 vélin é valin í staðinn:

-   Stofna°tvær aðskildar getur: Lághraðaborun og Háhraðaborun. Skilgreina Lághraðaborun°sem borun sem hefur vinnslutíma á bilinu ein til níu einingar á klukkustund. Skilgreina Háhraðaborun sem borun sem hefur vinnslutíma á bilinu 10 til 19 einingar á klukkustund. Úthlutið síðan vél M1 Lághraðaborunargetu og úthlutið vél M2 Háhraðaborunargetu. Loks skal breyta tilfangaþörf getu á leiðinni yfir í Háhraðaborun. Röðunarvélin mun velja rétta vél (M2).
-   Notið getustig til að viðurkenna Borunargetu sem er úthlutað til borvélanna. Tilgreina að vél M1 hefur Borunargetu á stigi 2,0 og vél M2 hefur Borunargetugetu á stigi 11,0. Tilgreinið síðan 10,0 sem það lágmarksstig sem krafist er fyrir Borunargetu á leiðinni. Röðunarvélin mun þá ákvarða að aðeins vél M2 uppfylli tilfangaþarfir.

## <a name="competencies-for-human-resources"></a>Hæfni fyrir mannauð
Þegar þú ert með rekstrartilföng af gerðinni **Mannauður** sem eru tengd við starfsmenn í Mannauði, getur þú einnig nýtt hæfni starfsmanna þegar tilfangaþörf fyrir framleiðsluleið er skilgreind. Með öðrum orðum, er einnig hægt að tilgreina þarfir fyrir ákveðna hæfni, námskeið, skírteini eða titla. Áætlunarkerfið getur svo valið tilföng sem eru tengd við starfsmenn og valið mun byggjast á hæfni þeirra starfsmanna. Hæfni er sett upp í Mannauði, ekki á síðunni **Tilfangageta** síðu. Þegar hæfni, námskeið, skírteini eða titla eru skilgreind sem tilfangaþarfir, verður að nota Mannauðseiginleikann og tengja hvert tilfang af gerðinni **Mannauður** við samsvarandi starfsmann. Ef ekki er verið að nota virknina Mannauður er hægt að skilgreina getu á síðunni **Tilfangagetu** sem líkir eftir eða afritar hæfni úr Mannauði. Hins vegar inniheldur síðan **Tilfangageta** ekki virkni sem krafist er til að vinna með hæfni, námskeið, vottanir eða titla.




