---
title: Seinka nákvæmum útreikningi á verði og afslætti til að bæta afköst
description: Þetta efnisatriði lýsir möguleika seinkaðs verðútreiknings sem er í boði í Microsoft Dynamics 365 Commerce sölustað (POS) og símaveri.
author: boycezhu
ms.date: 09/09/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 8c4264c3a4c71e6aab0e1ef8d7d8cfffad065a46
ms.sourcegitcommit: 7a2001e4d01b252f5231d94b50945fd31562b2bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/15/2021
ms.locfileid: "7488364"
---
# <a name="delay-exact-price-and-discount-calculation-for-improved-performance"></a>Seinka nákvæmum útreikningi á verði og afslætti til að bæta afköst

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir möguleika seinkaðs verðútreiknings sem er í boði í Microsoft Dynamics 365 Commerce sölustað (POS) og símaveri.

Dynamics 365 Commerce styður stofnun samvalsafsláttar sem er notaður þegar margar sölulínur sölupöntunar eða sölutilboðs eru sameinaðar. Þessir afslættir fela í sér blöndu og samsvörun, þröskuld og magnafslætti.

Þegar nýrri línu er bætt við pöntun metur verðlagningarkerfi Commerce alla körfuna til að skera úr um hvort hægt sé að nota einhvern þessara samvalsafslátta. Vegna endurútreikningsins getur viðbót nýrra lína haft áhrif á afköst þar sem sölupöntun stækkar.

Hins vegar eru B2B-fyrirtæki og sum B2C-fyrirtæki oft með mikið pöntunarmagn. Því getur reynst tímafrekt að bíða eftir að verðlagningarkerfið geri endurútreikning eftir viðbót hverrar vöru í körfuna. Þegar um stórar pantanir er að ræða er auk þess yfirleitt ekki mjög mikilvægt að nákvæmt verð og afsláttur komi fram í hvert sinn sem hlut er bætt í körfuna. Mikilvægt er að notendur geti bætt vörum við á fljótlegan hátt. Möguleikinn á að fresta nákvæmum verð- og afsláttarútreikningi þar til notandi óskar eftir því eða þegar gengið er frá pöntun getur aukið afköst umtalsvert. Hann getur einnig dregið úr tímanum sem þarf til að leggja fram pöntun.

Möguleikinn á að seinka nákvæmum verð- og afsláttarútreikningi hefur lengi verið í boði á sölustað. Frá og með Commerce-útgáfu 10.0.22 verður hann einnig í boði fyrir símaver.

## <a name="enable-delayed-price-and-discount-calculation-for-pos"></a>Virkja seinkaðan verð- og afsláttarútreikning fyrir sölustað

Til að virkja seinkaðan verð- og afsláttarútreikning fyrir sölustað skal fylgja þessum skrefum.

1. Í Commerce Headquarters skal fara í virkniregluna sem tengist sjálfri versluninni.
1. Í flýtiflipanum **Upphæð** skal virkja skilgreininguna **Reikna handvirkt afslátt af mörgum vörum**.
1. Opnaðu hönnuð skjáútlits fyrir afgreiðslukassana þar sem virkja á seinkaðan útreikning.
1. Bættu hnappi fyrir aðgerðina **Reikna út samtölu** við æskilegt hnappahnit.
1. Keyrðu vinnslurnar **1070** og **1090**.

Þegar vörum er bætt við færslu eru samvalsafslættir ekki reiknaðir nema gjaldkerinn velji hnappinn **Reikna út samtölu**. Eftir að **Reikna út samtölu** er valið fyrir færslu verða samvalsafslættir alltaf reiknaðir fyrir hana. Gjaldkerinn þarf ekki að velja hnappinn aftur, jafnvel þótt fleiri vörum sé bætt við körfuna. Kerfið leyfir gjaldkeranum ekki að taka við greiðslu fyrr en búið er að velja **Reikna út samtölu**.

## <a name="enable-delayed-price-and-discount-calculation-for-call-center"></a>Virkja seinkaðan verð- og afsláttarútreikning fyrir símaver

Til að virkja seinkaðan verð- og afsláttarútreikning fyrir símaver skal fylgja þessum skrefum.

1. Í Commerce Headquarters skal fara í **Vinnusvæði \> Eiginleikastjórnun**.
1. Gerið eiginleikann **Koma í veg fyrir óviljandi verðútreikning á viðskiptapöntun**. Þessi eiginleiki er forsenda þess að hægt sé að gera seinkaðan verð- og afsláttarútreikning.

    > [!NOTE]
    > Fyrir nýjar uppsetningar er eiginleikinn **Koma í veg fyrir óviljandi verðútreikning á viðskiptapöntun** sjálfgefið virkjaður.

1. Farðu í **Færibreytur Commerce \> Verð og afslættir**.
1. Í hlutanum **Ýmislegt** skal virkja skilgreininguna **Reikna verð og afslætti með mörgum línum handvirkt**.

Nú, þegar sölupöntun eða sölutilboð er búið til eða breytt í símaverinu, verður nákvæmum verð- og afsláttarútreikningi seinkað. Verðlagningarkerfið mun aðeins taka til greina sölulínurnar sem verið er að bæta við eða breyta og mun hunsa allar aðrar sölulínur. Nettóupphæðin fyrir vöru felur í sér verðútreikninga og einfalda afslætti (afsláttarprósentu eða upphæð stakrar vöru). Hinsvegar verður blanda og samsvörun, þröskuldur og magnafslættir ekki notaðir. Notendur símavers sem vilja skoða nákvæmt verð, þ.m.t. alla afslætti, geta valið einn af þremur hnöppum: **Endurreikna**, **Samtölur** eða **Ljúka**.

> [!NOTE]
> Fyrir pantanir í símaveri sýnir kerfið viðvörunarboð til að minna notandann á að hann verði að velja hnappinn **Endurreikna**, **Samtölur** eða **Ljúka** svo að nákvæmur verð- og afsláttarútreikningur verði gerður. Fyrir pantanir þar sem hnappurinn **Ljúka** er tiltækur er engin leið fyrir notanda símaversins að sleppa nákvæmum verð- og afsláttarútreikningi því hann verður að velja **Ljúka** til að ljúka við pöntunina. Fyrir pantanir þar sem hnappurinn **Ljúka** er ekki tiltækur er engin aðgerð sem gefur til kynna að pöntun sé lokið. Þess vegna er notandi símaversins ábyrgur fyrir því að velja annaðhvort **Endurreikna** eða **Samtölur** áður en hann lýkur við pöntunina.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
