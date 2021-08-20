---
title: Umframtiltekt fyrir sölupantanir og flutningspantanir
description: Í þessu efnisatriði er útskýrt hvernig á að virkja umframtiltekt fyrir sölupantanir og flutningspantanir.
author: GalynaFedorova
ms.date: 07/06/2021
ms.topic: article
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-06
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 3c6f9d386f79754edce38e4e2cf4c9bfefbce69bdb252e8754f39d909827fa02
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722152"
---
# <a name="over-picking-for-sales-orders-and-transfer-orders"></a>Umframtiltekt fyrir sölupantanir og flutningspantanir

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði eru aðstæður sem sýna hvernig á að virkja annaðhvort ákveðinn starfsmann eða alla starfsmenn til að gera umframtiltekt. Ferli umframtiltektar leyfir stýrða umframtiltekt í tiltektinni.

Hugmyndin á bak við umframtiltekt vöruhúss er einföld. Kerfið gerir starfsmönnum kleift að velja fleiri hluti en eru tilgreindir fyrir pöntun. Enn er þó tekið tillit til mörk umframtiltektar sem eru stillt á línustigi fyrir flutningspöntun eða sölupöntun. Ef farið er yfir þau mörk tilkynnir forrit Warehouse Management starfsmanninum að hann sé að fara yfir mörk umframtiltektar.

Eiginleiki umframtiltektar hjálpar til við að lágmarka viðhald og auðveldar einnig uppsetningunni að vera áfram sveigjanleg. Hægt er að skilgreina eitt eða fleiri atriði í valmynd fartækis og virkja umframtiltekt fyrir aðeins nokkur þeirra. Þú getur einnig komið í veg fyrir að útvaldir starfsmenn geri umframtiltekt á sölupöntunum og/eða flutningspöntunum án þess að þurfa að breyta valmyndaratriðunum. Þess í stað er hægt að slökkva á öðrum eða báðum möguleikunum í viðeigandi uppsetningum starfsmanna.

Eiginleiki umframtiltektar getur sparað starfsmönnum tíma og orku þegar þeir tína og senda vörur. Til dæmis gerir eiginleikinn starfsmönnum kleift að vinna þessi verk:

- Bæta fyrir rýrnun við tínslu eða sendingu.
- Forðastu að þurfa að opna umbúðir meðan á tiltektarferlinu stendur.
- Bæta tjón á hlut við flutning.
- Sendu frávik magns eða mælieiningar.
- Lágmarkaðu skiptingu á magni á númeraplötum.
- Forðastu efnissóun og skort á dýrum efnum.
- Mældu tiltektarmagnið eftir tínslu (til dæmis með vigtun á flutningabifreið).

> [!IMPORTANT]
> Eiginleiki umframtiltektar gildir aðeins um tiltekt og úrvinnslu sölupöntunar og flutningspöntunar. Áfylling styður ekki umframtiltekt. Þegar áfyllingarvinnan er keyrð leyfir kerfið notendum ekki að tína of mikið.

Þessar aðstæður í þessu efnisatriði sýna hvernig á að setja upp og nota eiginleika umframtiltektar.

## <a name="scenario-prerequisite-make-demo-data-available"></a>Skilyrði fyrir aðstæðurnar: Bjóða upp á sýnigögn

Aðstæður í þessu efnisatriði vísa í gildi og færslur sem eru innifaldar í stöðluðum sýnigögnum fyrir Microsoft Dynamics 365 Supply Chain Management. Ef nota á gildin sem er boðið upp á hér eins og í æfingunum skal gæta þess að vinna í umhverfi þar sem sýnigögnin eru uppsett og stilla lögaðilann á *USMF* áður en hafist er handa.

## <a name="scenario-setup"></a>Uppsetning sviðsmyndar

Áður en unnið er í gegnum sýnidæmið þarf að virkja umframtiltekt fyrir bæði viðeigandi starfsmann og viðeigandi valmyndaratriði.

### <a name="set-up-a-worker-to-allow-for-over-picking"></a>Setja upp starfsmann til að leyfa umframtiltekt

Hér er almenna aðferðin við að skilgreina starfsmann til að virkja umframtiltekt fyrir annars vegar sölupantanir og hins vegar flutningspantanir. Þessi skilgreining stýrir því hvaða starfsmaður tiltektar geti gert umframtiltekt og hvort sá starfsmaður geti gert umframtiltekt fyrir bæði flutningspantanir og sölupantanir.

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Starfskraftur**.
1. Á listasvæðinu skal velja **Julia Funderburk**.
1. Í flýtiflipanum **Notendur** skal velja línuna sem er með eftirfarandi gildi. Ef engin núverandi lína hefur þessi gildi skaltu búa hana til.

    - **Notandakenni:** *24*
    - **Notandanafn:** *WH 24*
    - **Sjálfgefið vöruhús:** *24*
    - **Heiti valmyndar:** *Aðalvalmynd*

1. Í flýtiflipanum **Vinna** skal stilla eftirfarandi gildi fyrir notendur *24* ef þau eru ekki þegar stillt:

    - **Leyfa umframtiltekt í sölu:** *Já*
    - **Leyfa umframtiltekt flutningspöntunar:** *Já*

### <a name="set-up-a-mobile-device-menu-item-to-allow-for-over-picking"></a>Setja upp valmyndaratriði fartækis til að leyfa umframtiltekt

Hér er almenna aðferðin við að skilgreina valmyndaratriði fartækis til að virkja umframtiltekt. Það fer eftir viðskiptakröfum þínum fyrir heimildarstig starfsmannsins hver mun nota valmynd fartækisins, sumum færibreytum er hægt að kveikja og slökkva á.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.
1. Á listasvæðinu skal velja færsluna sem heitir *Tiltekt sölu*. Ef engin fyrirliggjandi færsla er með það heiti skal búa hana til. Staðfestið eða stillið eftirfarandi gildi fyrir færsluna:

    - **Heiti valmyndaratriðis:** *Tiltekt sölu*
    - **Tiltekt:** *Tiltekt sölu*
    - **Máti:** *Vinna*
    - **Nota fyrirliggjandi vinnu:** *Já*
    - **Stýrt af:** *Notandastýrt*
    - **Hnekkja yfirnúmeraplötu:** *Já*
    - **Hnekkja númeraplötu við frágang:** *Já*
    - **Láta notanda halda vinnu læstri:** *Já*
    - **Leyfa umframtiltekt:** *Já*

> [!IMPORTANT]
> Eftir að viðeigandi færibreytur fyrir bæði starfsmanninn og valmyndaratriði fartækisins eru virkjaðar er aðeins hægt að vinna úr umframtilekt í gegnum fartækið.

## <a name="example-scenario"></a>Dæmi

Þegar forsendurnar, uppsetning starfsmanna og uppsetning valmyndaratriða eru komnar er allt til reiðu til að vinna með eiginleikann.

### <a name="create-a-sales-order-that-allows-for-overdelivery"></a>Stofna sölupöntun sem leyfir umframtiltekt

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
1. Veldu **Nýr** til að búa til nýja sölupöntun.
1. Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:

    - **Viðskiptavinalykill:** *US-001*
    - **Vöruhús:** *24*

1. Veldu **Í lagi**.
1. Ný sölupöntun opnast. Í flýtiflipanum **Sölupöntunarlínur** skal bæta við línu sem er með eftirfarandi stillingum:

    - **Vörunúmer:** *A0001*
    - **Magn:** *10*

1. Á flýtiflipanum **Línulýsing**, á flipanum **Afhending**, stillirðu reitinn **Ofafhending** á *10*.
1. Í flýtiflipanum **Sölupöntunarlínur** skal velja **Birgðir \> Frátekning**.
1. Á síðunni **Frátekning**, á aðgerðasvæðinu, skal velja **Frátektarlota** til að taka frá birgðir.
1. Lokaðu síðunni **Frátekning**.
1. Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Losa í vöruhús**.

Þegar losuninni er lokið birtast upplýsingaboð sem sýna auðkenni bylgju og sendingar sem voru búin til.

### <a name="get-the-work-id-and-license-plate-number-for-the-new-order"></a>Fá vinnukenni og númeraplötunúmer fyrir nýju pöntunina

Þegar þú losaðir sölupöntunina í vöruhúsið ætti kerfið að hafa stofnað nýtt vinnukenni sem er með eina tiltektarlínu. Fylgið eftirfarandi skrefum til að finna vinnukenni og úthlutanir númeraplötu.

1. Opnaðu **Vöruhúsastjórnun \> Vinna \> Upplýsingar um vinnu**.
1. Í hnitanetinu **Yfirlit**, skal leita í dálknum **Pöntunarnúmer** að sölupöntununum sem voru stofnaðar rétt í þessu. Skráið niður vinnuauðkenni þeirrar sölupöntunar.
1. Veljið línuna fyrir nýju sölupöntunina til að sýna tengdar upplýsingar í hnitanetinu **Línur**. Skráið niður staðsetninguna þar sem varan verður tínd úr.
1. Farið í **Birgðastjórnun \> Fyrirspurnir og skýrslur \> Lagerlisti**.
1. Á aðgerðasvæðinu skal velja **Víddir**.
1. Í svarglugganum **Birting víddar** skal ganga úr skugga um að gátreitirnir **Númeraplata**, **Vöruhús** og **Vörunúmer** séu valdir og veldu því næst **Í lagi**.
1. Í glugganum **Sía** skal stilla eftirfarandi síur:

    - **Vörunúmer** – **er eitt af** – *A0001*
    - **Vöruhús** – **hefst á** – *24*

1. Veljið **Bæta við**.
1. Skráið niður gildi **Númeraplötu** sem birtist.

### <a name="over-pick-the-order-by-using-the-warehouse-management-mobile-app"></a>Tína of mikið fyrir pöntunina með því að nota fartækjaforrit Warehouse Management

1. Skráðu þig inn í farsímaforrit vöruhúsakerfis sem notandi í vöruhúsi *24*.
1. Opnaðu **Á útleið \> Sölutiltekt**.
1. Í reitinn **Skanna vinnukenni eða númeraplötu** skal færa inn vinnukennið sem var stofnað fyrir sölupöntunina.
1. Veljið **Í lagi** (gátmerkistákn).
1. Veldu **Umframtiltekt**.
1. Stilltu reitinn **Tiltektarmagn** á *14*.
1. Veljið **Í lagi** (gátmerkistákn).

    Á síðunni **Umframtiltekt** færðu eftirfarandi skilaboð: „Umframtiltekt línu er 40,00 prósent, en leyfð umframtiltekt er aðeins 10,00 prósent.“ Þessi skilaboð gefa til kynna að tiltektarmagnið sem þú slóst inn fari yfir mörk umframtiltektar. Mörk umframtiltektar fyrir sölupöntunarlínuna er 10 prósent. Fyrir tilgreint magn upp á 10 er því eingöngu hægt að velja 1 umfram, sem gerir samtals tiltektarmagn upp á 11.

1. Stilltu reitinn **Tiltektarmagn** á *11*.
1. Veljið **Í lagi** (gátmerkistákn).
1. Í reitinn **Númeraplata** skal færa inn númeraplötuna sem þú skrifaðir niður í hlutanum hér á undan.
1. Í reitinn **Marknúmeraplata** skal færa inn marknúmeraplötu. Taktu eftir því að tiltektarstaðsetningin (*FLOOR-001*), vara (*A0001*) og magn (*11 stk*) eru sýnd.
1. Veljið **Í lagi** (gátmerkistákn).
1. Skoðið upplýsingarnar á síðunni **Sölupantanir: Frágangur**. Reiturinn **Loc** á að sýna að tíndar vörur eru að fara á staðsetninguna *BAYDOOR*.
1. Veljið **Í lagi** (gátmerkistákn).

Á síðunni **Skanna vinnukenni / kenni númeraplötu** birtast skilaboðin „Vinnu lokið“. Skilaboðin gefa til kynna að vinnukenn sölupöntunarinnar sé lokið og að magn umframtiltektar fari ekki yfir mörk umframtiltektar sem nemur 10 prósent.
