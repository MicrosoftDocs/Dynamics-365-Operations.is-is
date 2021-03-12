---
title: Móttaka númeraplötu í gegnum vöruhúsaforritið
description: Þetta efnisatriði útskýrir hvernig á að setja upp vöruhúsaforrit til að styðja notkun móttökuferlis númeraplötu til að taka á móti efnislegum birgðum.
author: perlynne
manager: tfehr
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSParameters, WHSRFMenuItem, WHSLicensePlate, WHSPackingStructure
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 0fe02a83d05e4b86694c1b210906128ac0cf6a84
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998429"
---
# <a name="license-plate-receiving-via-the-warehouse-app"></a>Móttaka númeraplötu í gegnum vöruhúsaforritið

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að setja upp vöruhúsaforrit þannig að það styðji notkun móttökuferlis númeraplötu til að taka á móti efnislegum birgðum.

Þú getur notað þessa aðgerð til að skrá fljótt móttöku á birgðum á innleið sem tengjast tilkynningu um sendingu (ASN). Kerfið stofnar sjálfkrafa ASN þegar ferli vöruhússtjórnunar eru notuð til að senda flutningspöntun. Fyrir innkaupapöntunarferlið er hægt að skrá ASN handvirkt eða flytja það sjálfkrafa inn með því að nota ASN gagnaeiningarferli á innleið.

ASN gögnin eru tengd við farm og sendingar um *pakkaskipan*, þar sem bretti (yfirnúmeraplötur) geta innihaldið mál (faldaðar númeraplötur).

> [!NOTE]
> Til að fækka birgðafærslum þegar pakkaskipan sem hefur faldaðar númeraplötur er notuð skráir kerfið efnislegar lagerbirgðir á yfirnúmeraplötuna. Til að kveikja á hreyfingu efnislegrar lagerbirgða frá yfirnúmeraplötunni yfir á faldaðar númeraplötur, byggðar á pakkaskipunargögnum, verður fartækið að bjóða upp á valmyndaratriði sem er byggt á vinnusköpunarferlinu *Pakka á faldaðar númeraplötur*.

## <a name="warehousing-mobile-device-app-processing"></a>Úrvinnsla fartækjaforrits vöruhúss

Þegar starfsmaður skannar númeraplötukenni á innleið setur kerfið móttökuferli númeraplötu af stað. Á grundvelli þessara upplýsinga verður efni númeraplötunnar (gögn sem koma frá ASN) efnislega skráð á staðsetningu innhliðs. Verkflæðin sem fylgja munu fara eftir þörfum viðskiptaferlisins.

## <a name="work-policies"></a>Vinnureglur

Eins og við um (sem dæmi) vinnslu valmyndaratriði fartækis *Bóka sem tilbúið*, styður móttökuferli númeraplötu ýmis verkflæði samkvæmt skilgreindri uppsetningu.

### <a name="work-policies-with-work-creation"></a>Vinnureglur með stofnun vinnu

Þegar vörur á innleið eru skráðar með því að nota vinnureglu sem stofnar vinnu, býr kerfið til og vistar færslur frágangsvinnu fyrir hverja skráningu. Ef notað er vinnuferlið *Móttaka og frágangur númeraplötu* eru skráning og frágangur meðhöndluð sem ein aðgerð með því að nota eitt valmyndaratriði fartækis. Ef notað er ferlið *Móttaka númeraplötu* eru móttöku- og frágangsferlin meðhöndluð sem tvær mismunandi vöruhúsaaðgerðir, hver með sitt eigið valmyndaratriði fartækis.

### <a name="work-policies-without-work-creation"></a>Vinnureglur án stofnun vinnu

Hægt er að nota móttökuferli númeraplötu án þess að stofna vinnu. Ef vinnureglur eru skilgreindar sem eru með verkbeiðnigerðina *Millifærslumóttaka* og/eða *Innkaupapantanir* og notað er ferlið *Móttaka (og frágangur) númeraplötu*, munu eftirfarandi tvö ferli Warehousing mobile app ekki stofna vinnu. Þess í stað skrá þau aðeins efnislegar birgðir á innleið á númeraplötunni við móttökuhliðið.

- *Móttaka númeraplötu*
- *Móttaka og frágangur númeraplötu*

> [!NOTE]
> - Skilgreina verður að minnsta kosti eina staðsetningu fyrir vinnureglu í hlutanum **Birgðastaðsetningar**. Ekki er hægt að tilgreina sömu staðsetninguna fyrir margar vinnureglur.
> - Valkosturinn **Prenta merki** fyrir valmyndaratriði fartækis vöruhúss prentar ekki númeraplötumerki án stofnunar vinnu.

Til að bjóða upp á þessa virkni í kerfinu verður að kveikja á eiginleikanum *Endurbætur á móttöku númeraplötu* í [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="receive-inventory-on-a-location-that-doesnt-track-license-plates"></a>Taka á móti birgðum á staðsetningu sem heldur ekki utan um númeraplötur

Hægt er að nota vöruhúsastaðsetningu sem er úthlutað á staðsetningarforstillingu jafnvel þegar ekki er kveikt á **Nota rakningu númeraplötu**. Þegar tekið er á móti birgðum er þar af leiðandi hægt skrá lagerbirgðirnar á staðsetningu án þess að stofna vinnu.

## <a name="add-mobile-device-menu-items-for-each-receiving-location-in-a-warehouse"></a>Bæta við valmyndaratriðum fartækis fyrir hverja móttökustaðsetningu í vöruhúsi

Eiginleikinn *Endurbætur á móttöku númeraplötu* gerir kleift að taka á móti á hvaða staðsetningu sem er í vöruhúsi með því að bæta valmyndaratriði staðsetningarmiðaðrar móttöku (og frágangs) númeraplötu við Warehousing mobile app. Áður studdi kerfið að taka aðeins á móti á sjálfgefinni staðsetningu sem er skilgreind fyrir hvert vöruhús. Hins vegar, þegar kveikt er á þessum eiginleika, bjóða valmyndaratriði fyrir móttöku (eða frágang) númeraplötu í fartæki upp á valkostinn **Nota sjálfgefin gögn** sem gerir kleift að velja sérstillta „til“ staðsetningu fyrir hvert valmyndaratriði. (Þessi valkostur var þegar tiltækur fyrir nokkrar aðrar gerðir valmyndaratriða.)

Til að bjóða upp á þessa virkni í kerfinu verður að kveikja á eiginleikanum *Endurbætur á móttöku númeraplötu* í [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="show-or-skip-the-receiving-summary-page"></a>Sýna eða sleppa móttökuyfirlitssíðu

Þú getur notað aðgerðina *Stjórna því hvort sýna skuli móttökuyfirlitssíðu í fartækjum* til að nýta sér viðbótar ítarlegt forritsflæði vöruhúss sem hluta af móttökuferli fyrir númeraplötur.

Þegar kveikt er á þessari aðgerð munu valmyndaratriðin í fartækinu fyrir móttöku númeraplötu eða móttöku og frágang númeraplötu veita stillinguna **Birta yfirlitssíðu móttöku**. Þessi stilling hefur eftirfarandi valkosti:

- **Birta ítarlegt yfirlit** - Við móttöku númeraplötu munu starfsmenn sjá auka síðu sem sýnir allar ASN upplýsingar.
- **Sleppa yfirlitinu** - Starfsmenn sjá ekki allar ASN upplýsingar. Starfsmenn vörugeymsluhússins ekki heldur sett upp ráðstöfunarkóða eða bætt við undantekningum meðan á móttökuferlinu stendur.

Til að bjóða upp á þessa virkni í kerfinu verður að kveikja á eiginleikanum *Stjórna því hvort á að birta yfirlitssíðu móttöku í fartækjum* í [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a>Komdu í veg fyrir að númeraplötur með flutningspöntunum–sent séu notaðar í vöruhúsum öðrum en ákvörðunarvöruhúsinu

Ekki er hægt að nota móttökuferli númeraplötu ef ASN inniheldur númeraplötukenni sem er þegar til og er með gögn efnislegra lagerbirgða á staðsetningu vöruhúss, önnur en staðsetningu vöruhúss þar sem skráning á númeraplötunni fer fram.

Fyrir aðstæður flutningspöntunar þar sem flutningsvöruhúsið rekur ekki númeraplöturnar (og rekur þar af leiðandi ekki heldur efnislegar lagerbirgðir á hverja númeraplötu) er hægt að nota eiginleikann *Koma í veg fyrir að númeraplötur með sendum flutningspöntunum séu notaðar í öðrum vöruhúsum en ákvörðunarvöruhúsinu* til að koma í veg fyrir efnislegar birgðauppfærslur á númeraplötum sem eru í flutningi.

Til að bjóða upp á þessa virkni í kerfinu verður að kveikja á eiginleikanum *Koma í veg fyrir að númeraplötur, sem afgreiddar voru með flutningspöntun, verði notaðar í öðrum vöruhúsum en vöruhúsi áfangastaðar* í [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Fylgdu þessum skrefum til að stjórna virkni þegar þessi eiginleiki er tiltækur.

1. Farðu í **vöruhúsakerfi \> Uppsetning \> Færibreytur vöruhúsakerfis**.
1. Á flipanum **Almennt**, á flýtiflipanum **Númeraplötur**, stillirðu reitinn **Reglur um númeraplötu flutningsvöruhúsa** á eitt af eftirfarandi gildum:

    - **Leyfa endurnotkun á óröktum númeraplötum** - Kerfið virkar á sama hátt og það virkar þegar eiginleikinn *Koma í veg fyrir að númeraplötur með sendum flutningspöntunum séu notaðar í öðrum vöruhúsum en ákvörðunarvöruhúsinu* er ekki í boði. Þetta gildi er sjálfgefin stilling þegar þú virkjar eiginleikann fyrst.
    - **Koma í veg fyrir endurnotkun á óröktum númeraplötum** - Aðeins handvirkar uppfærslur sem tengjast sendum númeraplötum verða leyfðar í ákvörðunarvöruhúsinu þar til flutningspöntunin hefur borist.

## <a name="more-information"></a>Meiri upplýsingar

Nánari upplýsingar um valmyndaratriði fartækja, sjá [Uppsetning fartækja fyrir vöruhúsavinnu](configure-mobile-devices-warehouse.md).

Frekari upplýsingar um framleiðsluaðstæðurnar *Bóka sem tilbúið* er að finna í [Yfirlit yfir vinnureglur vöruhúss](warehouse-work-policies.md).

Frekari upplýsingar um stjórnun á farmi á innleið er að finna í [Meðhöndlun vöruhúss á farmi á innleið fyrir innkaupapantanir](inbound-load-handling.md).
