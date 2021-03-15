---
title: Stilla mismunandi víddir fyrir pakka og geymslu
description: Þetta efnisatriði sýnir hvernig á að tilgreina hvaða vinnslu (pökkun, geymsla eða földuð pökkun) hver tilgreind vídd er notuð fyrir.
author: mirzaab
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPhysDimUOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 004d9b4522335b481b640ef0fe35f4db66e3c9f5
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/28/2021
ms.locfileid: "5078274"
---
# <a name="set-different-dimensions-for-packing-and-storage"></a>Stilla mismunandi víddir fyrir pakka og geymslu

[!include [banner](../includes/banner.md)]

Sumar vörur eru pakkaðar eða geymdar á þann hátt að nauðsynlegt kann að vera að rekja efnislegar víddir á annan hátt fyrir hvert mismunandi ferli. Eiginleikinn *Afurðarvíddir pökkunar* gerir kleift að setja upp eina eða fleiri gerðir af víddum fyrir hverja afurð. Hver gerð víddar býður upp á efnislegar mælingar (þyngd, breidd, dýpt og hæð) og kemur með ferlið þar sem þessi gildi efnislegra mælinga eiga við. Þegar þessi eiginleiki er virkur styður kerfið eftirfarandi gerðir af víddum:

- *Geymsla* - Geymsluvíddir eru notaðar ásamt rúmmáli staðsetningar til að ákvarða hversu mikið af hverri vöru er hægt að geyma í hinum ýmsu staðsetningum vöruhúss.
- *Pökkun* – Pökkunarvíddir eru notaðar við umbúðahönnun og í handvirku pökkunarferli til að ákvarða hversu mikið af hverri vöru passar í hinar ýmsu umbúðagerðir.
- *Földuð pökkun* – Víddir faldaðrar pökkunar eru notaðar þegar pökkunarferlið inniheldur mörg stig.

*Geymsluvíddir* eru studdar hvort sem eiginleikinn *Afurðarvíddir pökkunar* er virkur eða ekki. Þetta er sett upp með síðunni **Efnisleg vídd** í Supply Chain Management. Þessar stærðir eru í notaðar af öllum ferlum þar sem víddir pökkunar og faldaðrar pökkunar eru ekki tilgreindar.

Víddir *pökkunar* og *faldaðrar pökkunar* eru settar upp á síðunni **Efnislegar afurðarvíddir** sem er bætt við þegar eiginleikinn *Afurðarvíddir pökkunar* er virkjaður.
Í þessu efnisatriði er að finna aðstæður sem lýsa því hvernig á að nota þennan eiginleika.

## <a name="turn-on-the-packaging-product-dimensions-feature"></a>Kveikja á eiginleika afurðarvíddar pökkunar

Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu. Stjórnendur geta notað vinnusvæði [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur. Þar er eiginleikinn sýndur á eftirfarandi hátt:

- **Eining:** *Vöruhúsakerfi*
- **Heiti eiginleika:** *Afurðarvíddir pökkunar*

## <a name="example-scenario"></a>Dæmi

### <a name="set-up-the-scenario"></a>Setja upp aðstæður

Áður en hægt er að keyra sýnidæmið þarf að undirbúa kerfið eins og lýst er í þessum hluta.

#### <a name="enable-demo-data"></a>Kveikja á sýnigögnum

Til að vinna í gegnum þessar aðstæður með því að nota sýnigögnin og gildin sem eru tilgreind hér verður þú að vera í kerfi þar sem venjuleg [sýnigögn](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) eru sett upp. Þar að auki verður þú að velja *USMF*-lögaðila áður en þú byrjar.

#### <a name="add-a-new-physical-dimension-to-a-product"></a>Bæta nýrri efnislegri vídd við afurð

Bæta við nýrri efnislegri vídd fyrir afurð með því að gera eftirfarandi:

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Veljið afurðina með **Vörunúmer** *A0001*.
1. Á aðgerðasvæðinu skal opna flipann **Stjórna birgðum**, úr flokknum **Vöruhús**, og velja **Efnislegar afurðarvíddir**.
1. Síðan **Efnislegar afurðavíddir** opnast. Á aðgerðasvæðinu skal velja **Ný** til að bæta nýrri vídd við hnitanetið með eftirfarandi stillingum:
    - **Gerð efnislegrar víddar** - *Pökkun*
    - **Efnisleg eining** - *stk*
    - **Þyngd** - *4*
    - **Þyngdareining** - *kg*
    - **Dýpt** - *3*
    - **Hæð** - *4*
    - **Breidd** - *3*
    - **Lengd** - *cm*
    - **Rúmmálseining** - *cm3*

Reiturinn **Rúmmál** er sjálfkrafa reiknaður samkvæmt stillingunum fyrir **Dýpt**, **Hæð** og **Breidd**.

#### <a name="create-a-new-container-type"></a>Stofna nýja umbúðagerð

Farið í **Vöruhúsakerfi \> Uppsetningu \> Umbúðir \> Umbúðagerðir** og stofnið nýja færslu með eftirfarandi stillingum:

- **Kóði umbúðagerðar** - *Lítill kassi*
- **Lýsing** - *Lítill kassi*
- **Hámarksnettóþyngd** - *50*
- **Magn** - *144*
- **Lengd** - *6*
- **Breidd** - *6*
- **Hæð** - *4*

#### <a name="create-a-container-group"></a>Stofna umbúðaflokk

Farið í **Vöruhúsakerfi \> Uppsetningu \> Umbúðir \> Umbúðaflokkar** og stofnið nýja færslu með eftirfarandi stillingum:

- **Auðkenni umbúðaflokks** - *Lítill kassi*
- **Lýsing** - *Lítill kassi*

Bætið nýrri línu við hlutann **Upplýsingar**. Stillið **Umbúðagerðina** á *Lítill kassi*.

#### <a name="set-up-a-container-build-template"></a>Setja upp gámaröðunarsniðmát

Farið í **Vöruhúsakerfi \> Uppsetning \> Umbúðir \> Sniðmát umbúðahönnunar** og veljið **Kassar**. Breytið **Auðkenni umbúðaflokks** í *Lítill kassi*.

### <a name="run-the-scenario"></a>Keyra aðstæður

Þegar kerfið hefur verið undirbúið eins og lýst var í hlutanum hér á undan er hægt að keyra aðstæðurnar eins og lýst er í næsta hluta.

#### <a name="create-a-sales-order-and-create-a-shipment"></a>Stofna sölupöntun og stofna sendingu

Í þessu ferli verður sending stofnuð sem byggir á *pökkunarvíddum* vörunnar þar sem hæðin er minni en 3.

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:

    - **Viðskiptavinalykill:** *US-001*
    - **Vöruhús:** *63*

1. Veljið **Í lagi** til að stofna sölupöntunina og loka svarglugganum.
1. Ný sölupöntun opnast. Hún ætti að innihalda nýja, auða línu í hnitanetinu í flýtiflipanum **Sölupöntunarlínur**. Stilltu eftirfarandi gildi á þessari línu:

    - **Vörunúmer:** *A0001*
    - **Magn:** *5*

1. Í flýtiflipanum **Sölupöntunarlínur** skal velja **Birgðir \> Frátekning**.
1. Á síðunni **Frátekning**, á aðgerðasvæðinu, skal velja **Frátektarlota** til að taka frá birgðir.
1. Lokið síðunni.
1. Á aðgerðasvæðinu skal opna flipann **Vöruhús** og velja **Losa í vöruhús** til að búa til vinnu fyrir vöruhúsið.
1. Í flýtiflipanum **Sölupöntunarlínur** skal velja **Vöruhús \> Upplýsingar sendingar**.
1. Á aðgerðasvæðinu skal opna flipann **Flutningur** og velja **Skoða umbúðir**. Staðfestið að varan hafi verið komið fyrir í tveimur umbúðum af *Litlum kassa*.

#### <a name="place-an-item-into-storage"></a>Setja vöru í geymslu

1. Opnið fartækið, skráið ykkur inn í vöruhús 63 og farið í **Birgðir \> Breyting á**.
1. Sláið inn **Loc** = *SHORT-01*. Búið til nýja númeraplötu með **Vöru** = *A0001* og **Magn** = *1 stk*.
1. Veljið **Í lagi**. Upp kemur villan „Staðsetningin SHORT-01 tókst ekki vegna þess að varan A0001 passar ekki í tilgreindar víddir staðsetningar.“ Þetta er vegna þess að víddir *Geymslutegundar* fyrir afurðina eru stærri en víddirnar sem tilgreindar eru í staðsetningarforstillingunni.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]