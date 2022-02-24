---
title: Fyrirspurnir og skýrslur um hættuleg efni
description: Þetta efnisatriði útskýrir hvernig á að vinna með ýmsar skýrslur sem tengjast hættulegum efnum. Margar þessara skýrslna eru nauðsynlegar svo að þú fylgir ýmsum reglugerðum varðandi hættuleg efni við sendingu og geymslu.
author: dasani-madipalli
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 188c339ddf5f5c2488133924e9a0288f218f495c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430369"
---
# <a name="hazardous-materials-inquiries-and-reports"></a>Fyrirspurnir og skýrslur um hættuleg efni

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Microsoft Dynamics 365 Supply Chain Management býður upp á ýmsar skýrslur sem tengjast hættulegum efnum. Margar þessara skýrslna eru nauðsynlegar svo að þú fylgir ýmsum reglugerðum varðandi hættuleg efni við sendingu og geymslu.

Allar þessar skýrslur, nema skýrslan **Fjölþættur hættulegur varningur**, nota afhendingarmátann sem er skilgreindur fyrir sendinguna til að finna reglugerðina sem á að nota til að prenta texta fyrir sendingu fyrir vörur. Flutningsmátinn tengist farmflytjanda og flutningsþjónustunni. Þess vegna þarf að setja upp farmflytjanda og flutningsþjónustu og tengja þá við afhendingarmáta. Afhendingarmáti tengist reglugerðinni um hættuleg efni.

Eftirfarandi mynd sýnir röð verkþátta sem eiga sér stað þegar kerfið myndar skýrslur fyrir hættuleg efni.

![Röð verkþátta fyrir skýrslur fyrir hættuleg efni](media/hazmat-report-sequence.png "Röð verkþátta fyrir skýrslur fyrir hættuleg efni")

## <a name="set-up-hazardous-materials-reporting"></a><a name="set-up"></a>Setja upp skýrslur fyrir hættuleg efni

Oftast, ef vörur eru sendar sem innihalda hættuleg efni, þarf að mynda sérstakar skýrslur til að hjálpa til við að varðveita öryggi og fara eftir reglum um hættuleg efni. Til að setja upp skýrslurnar skal fylgja þessum skrefum.

1. Farðu í **vöruhúsakerfi \> Uppsetning \> Færibreytur vöruhúsakerfis**.
2. Opnið flipann **Skýrslur**. Í flipanum **Skýrslufæribreyta hættulegra efna** skal stilla eftirfarandi reiti.

    | Kafli | Svæði | lýsing |
    |---|---|---|
    | Fjölþættur hættulegur varningur | Reglugerðarkóði | Velja skal reglugerðina sem á að nota þegar **Fjölþættur hættulegur varningur** skýrsla er búin til. |
    | Birgðamörk hættulegra efna | Reglugerðarkóði | Velja skal reglugerðirnar sem á að nota þegar birgðamörk eru metin. |
    | Flutningur varnings á vegum | CMR-flokksafurð | CMR stendur fyrir „krabbameinsvaldandi, stökkbreytandi og æxlunarskaðandi efni“. Stillið þennan valkost á **Já** til að grunnstilla kerfið þannig að það prenti tilteknar viðvaranir og skilaboð sem tengjast meðhöndlun þessara efna. |
    | Flutningur varnings á vegum | Lýsing á flokki hættulegra efna | Sláið inn texta sértækra viðvörunar sem tengjast CMR og flutningi varnings á vegum. Þessi texti verður tekinn með í skýrslunni. |
    | Farmsendingarskýrsla | Viðvörun | Færa skal inn texta viðvörunarskilaboða sem á að prenta á yfirlýsingu flutningsaðila (til dæmis „Viðvörun: hættulegur varningur, eldfimur“). |
    | Farmsendingarskýrsla | Yfirlýsing á fæti | Færa skal inn texta skilaboða sem prenta á neðst á skjal fyrir sendingaryfirlýsingu. |
    | Tungumál skýrslu fyrir hættulegan varning | Tungumál innlendrar skýrslu fyrir hættulegan varning | Veljið sjálfgefið tungumál fyrir skýrslur fyrir hættuleg efni sem tengjast sendingum innanlands. |
    | Tungumál skýrslu fyrir hættulegan varning | Tungumál útflutningsskýrslu fyrir hættulegan varning | Veljið sjálfgefið tungumál fyrir skýrslur fyrir hættuleg efni sem tengjast alþjóðlegum sendingum. |

## <a name="hazardous-materials-report"></a>Skýrsla fyrir hættuleg efni

Skýrslan **Hættuleg efni** sýnir lista yfir allar vörur sem hafa verið settar upp og skilgreindar þannig að þær séu með upplýsingar um hættulegan varning. Hægt er að nota þessa skýrslu til að fylgjast með og yfirfara upplýsingarnar sem þarf að vinna með. Síðan fyrir skýrslu sýnir takmarkað val á reitum úr uppsetningu hættulegs efnis. Hins vegar er hægt að sérsníða hana til að bæta við viðbótarreitum eftir því sem þörf krefur.

Til að skoða þessa skýrslu skal fara á **Afurðarupplýsingastjórnun \> Fyrirspurnir og skýrslur \> Fylgiskjöl sendingar hættulegra efna \> Hættuleg efni**.

## <a name="hazardous-material-stock-limit-report"></a><a name="stock-limit-report"></a>Skýrsla birgðamarka fyrir hættuleg efni

Skýrslan **Birgðamörk hættulegs efnis** gerir kleift að fylgjast með birgðamörkum hættulegra efna í staðsetningum vöruhúss, til að ganga úr skugga um að þau haldist undir öryggismörkum. Þessi takmörk koma frá takmörkum sem eru skilgreind fyrir hverja útgefna afurð.

Til að skoða þessa skýrslu skal fara á **Afurðarupplýsingastjórnun \> Fyrirspurnir og skýrslur \> Fylgiskjöl fyrir sendingu hættulegra efna \> Birgðamörk hættulegra efna**.

Frekari upplýsingar um hvernig á að stilla birgðamörk á útgefna afurð er að finna á [Stilla birgðamörk fyrir hættulegar afurðir](hazmat-items.md#stock-limits).

Reglugerðin sem er notuð fyrir birgðamörk er skilgreind á síðunni **Færibreytur vöruhúsakerfis**. Farið í **Vöruhúsakerfi \> Uppsetning \> Færibreytur vöruhúsastjórnunar** og síðan, í **Skýrslur** , í **Birgðamörk hættulegra efna** skal tilgreina reglukóða. Frekari upplýsingar er að finna í hlutanum [Setja upp skýrslur fyrir hættuleg efni](#set-up) fyrr í þessu efnisatriði.

## <a name="verified-gross-mass-report"></a>Staðfest skýrsla brúttómassa

Skýrslan **Staðfestur brúttómassi** gerir þér kleift að prenta upplýsingar um þyngd sendingar.

Til að mynda og prenta þessa skýrslu skal fara í **Vöruhúsastjórnun \> Sendingar \> Allar sendingar** og opna viðkomandi sendingu. Á aðgerðasvæðinu, í flipanum **Sendingar**, í flokknum **Fylgiskjal yfir hættuleg efni**, skal velja **Staðfestur brúttómassi**.

## <a name="multimodal-dangerous-goods-report"></a>Skýrsla fyrir fjölþættan hættulegan varning

**Fjölþættur hættulegur varningur** er gefin upp fyrir sendingar sem þarf að flytja með samsettum flutningsmáta. Hann er oftast notaður þegar sending er flutt fyrst á vegi og síðar á sjó.

Til að mynda og prenta þessa skýrslu skal fara í **Vöruhúsastjórnun \> Sendingar \> Allar sendingar** og opna viðkomandi sendingu. Á aðgerðasvæðinu, í flipanum **Sendingar**, í flokknum **Fylgiskjal yfir hættuleg efni**, skal velja **Fjölþættur hættulegur varningur**.

Þegar þessi skýrsla er búin til eru upplýsingarnar vistaðar þannig að hægt er að breyta henni og/eða endurprenta skýrslu ef nauðsynlegt er. Til að breyta myndaðri skýrslu skal fara í **Vöruhúsastjórnun \> Fyrirspurnir og skýrslur \> Fylgiskjöl sendingar hættulegra efna \> Fjölþættur hættulegur varningur**, og finna viðeigandi skýrslu á listanum. Þegar búið er að breyta efninu eins og krafist er skal velja **Prenta** á aðgerðasvæði til að prenta út skýrsluna.

## <a name="shippers-declaration-report"></a>Farmsendingarskýrsla

Í **Farmsendingarskýrsla** er hægt að prenta upplýsingar sem tengjast yfirlýsingu um efni sem er tekið með í sendingunni.

Til að mynda og prenta þessa skýrslu skal fara í **Vöruhúsastjórnun \> Sendingar \> Allar sendingar** og opna viðkomandi sendingu. Á aðgerðasvæðinu, í flipanum **Sendingar**, í flokknum **Fylgiskjal yfir hættuleg efni**, skal velja **Farmsendingarskýrsla**.

## <a name="carriage-of-merchandise-by-road-report"></a>Skýrsla fyrir flutning varnings á vegum

Skýrslan **Flutningur varnings á vegum** líkist farmbréfi en er oftast notuð fyrir flutninga á vegum í Evrópu samkvæmt reglum um millilandaflutninga á hættulegum farmi á vegum. Þessi skýrsla notar prenttexta sendingar fyrir vöru nema ef **Lýsing á flokki hættulegra efna** er stillt á síðunni **Færibreytur vöruhúsakerfis**.

Til að mynda og prenta þessa skýrslu skal fara í **Vöruhúsastjórnun \> Sendingar \> Allar sendingar** og opna viðkomandi sendingu. Á aðgerðasvæðinu, í flipanum **Sendingar**, í flokknum **Fylgiskjal yfir hættuleg efni**, skal velja **Flutningur varnings á vegum**.

Þegar þessi skýrsla er búin til eru upplýsingarnar vistaðar þannig að hægt er að breyta henni og/eða endurprenta skýrslu ef nauðsynlegt er. Til að breyta myndaðri skýrslu skal fara í **Vöruhúsastjórnun \> Fyrirspurnir og skýrslur \> Fylgiskjöl sendingar hættulegra efna \> Flutningur varnings á vegum**, og finna viðeigandi skýrslu á listanum. Þegar búið er að breyta efninu eins og krafist er skal velja **Prenta** á aðgerðasvæði til að prenta út skýrsluna.

## <a name="shipment-summary-report"></a>Samantektarskýrsla sendingar

Skýrslan **Samantekt sendingar** veitir upplýsingar sem eru teknar saman af flutningsflokknum sem tengist útgefnum vörum.

Til að mynda og prenta þessa skýrslu skal fara í **Vöruhúsastjórnun \> Sendingar \> Allar sendingar** og opna viðkomandi sendingu. Á aðgerðasvæðinu, í flipanum **Sendingar**, í flokknum **Fylgiskjal yfir hættuleg efni**, skal velja **Samantekt sendingar**.

## <a name="bill-of-lading-report"></a>farmbréfaskýrsla

Þegar kveikt er á eiginleikann fyrir hættuleg efni í kerfinu er **farmbréf** skýrslan með dálkinn **Hættuleg efni** sem gefur til kynna hvort farmur inniheldur hættuleg efni. Þessi skýrsla er í boði á síðunni **Allar hleðslur**, eins og venjulega.

## <a name="packing-list-report"></a>Skýrsla pökkunarskráar

Þegar kveikt er á eiginleikann fyrir hættuleg efni í kerfinu er inniheldur pökkunarlistinn viðbótarupplýsingar sem tengjast prenttexta sendingar fyrir vöru. Þessi skýrsla er í boði á síðunni **Allar hleðslur**, eins og venjulega.
