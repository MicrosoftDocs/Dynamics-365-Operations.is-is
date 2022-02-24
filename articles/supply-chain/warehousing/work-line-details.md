---
title: Upplýsingar um vinnulínu
description: Í þessu efnisatriði er að finna upplýsingar um upplýsingasíðu vinnulínu sem sýnir heildstæðan, raðanlegan og síanlegan lista yfir einstakar vinnulínur í kerfinu.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkLocationChange, WHSWorkLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: bcb340b21e06b294a40784bf3a1da71b0daf7655
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4430711"
---
# <a name="work-line-details"></a>Upplýsingar um vinnulínu

[!include [banner](../includes/banner.md)]

Síðan **Upplýsingar um vinnulínu** sýnir heildstæðan, raðanlegan og síanlegan lista yfir einstakar vinnulínur í kerfinu. Hún býður upp á heildaryfirlit yfir vinnu sem er verið að áætla og framkvæma í vöruhúsinu. Auðvelt er að skipta á milli þess að skoða allar vinnulínur og skoða aðeins opnar vinnulínur. Upplýsingar sem eru gefnar upp fyrir hverja línu innihalda verkstöðuna, vörunúmerið, staðsetningu, vinnumagn, farmkenni og sendingarkenni.

## <a name="turn-on-the-work-line-details-feature"></a>Kveikja á eiginleika vinnulínuupplýsinga

Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Vöruhúsakerfi*
- **Heiti eiginleika:** *Upplýsingar um vinnulínu*

## <a name="open-and-use-the-work-line-details-page"></a>Opna og nota upplýsingasíðu vinnulínu

Til að skoða listann yfir upplýsingar um vinnulínur skal opna **Vöruhúsastjórnun \> Vinna \> Upplýsingar um vinnulínu**. Héðan er hægt að framkvæma eftirfarandi aðgerðir:

- Notið reitinn **Sía** til að leita að línum sem eru með tiltekin gildi fyrir einhverja tiltæka færibreytu. (Tiltækar færibreytur fela í sér margar færibreytur sem ekki eru sýndar sem dálkar í hnitanetinu.)
- Notið gátreitinn **Sýna lokaðar** til að sýna eða fela lokaðar línur.
- Veljið **Birta víddir** til að opna svargluggann **Birting vídda** þar sem hægt er að velja að sýna eða fela hina ýmsu dálka vídda í hnitanetinu.
- Veljið einhvern dálkahaus til að opna valmynd þar sem hægt er að velja um að raða eða sía listann eftir gildum í þeim dálki.
- Veljið vinnulínu og veljið svo **Breyta staðsetningu** til að opna svarglugga þar sem hægt er að breyta staðsetningu þeirrar vinnulínu. Staðsetningin sem tilgreind er mun hnekkja uppsetningu staðsetningarleiðbeiningar.
- Veljið vinnulínu og veljið svo **Hætta við vinnulínu** til að opna svarglugga þar sem hægt er að minnka magnið að hluta til eða að fullu fyrir þá vinnulínu.
- Leiðréttið magn.
- Skoðið færslurnar á bak við hvaða vinnulínu sem er.

## <a name="try-out-the-feature"></a>Prófa eiginleikann

Þessi hluti býður upp á sýniútgáfu í þremur hlutum sem sýnir hvernig á að vinna með upplýsingar vinnulínu.

### <a name="make-sample-data-available"></a>Gera sýnigögn tiltæk

Til að vinna í gegnum þessa sýnikennslu með því að nota sýniskrárnar og sýnigildin sem eru kynnt í þessu efnisatriði verður þú að vinna á kerfi þar sem venjulegu [sýnigögnin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) eru sett upp. Þar að auki verður þú að velja **USMF**-lögaðila áður en þú byrjar.

Einnig er hægt að nota þessa sýniútgáfu sem leiðsögn þegar unnið er í framleiðslukerfi. Hinsvegar þarf að skipta út eigin gildum og einhverjar nauðsynlegar færslugerðir gæti vantað sem stöðluðu sýnigögnin bjóða upp á.

### <a name="verify-that-the-scenario-setup-includes-enough-available-inventory"></a>Staðfesta að uppsetning aðstæðna feli í sér nægar birgðir

Ef unnið er með sýnigögnin **USMF** ætti fyrst að ganga úr skugga um að kerfið sé sett upp þannig að nægar birgðir séu tiltækar á öllum viðeigandi tiltektarstaðsetningum. Fyrir þessa sýniútgáfu er væntingin sú að eftirfarandi birgðir séu tiltækar:

- **Atriði M9200:** 45 ea. (eða fleiri)
- **Atriði M9202:** 10 ea. (eða fleiri)

Fylgið þessum skrefum til að staðfesta að nægar birgðir séu til staðar og til að gera nauðsynlegar leiðréttingar.

1. Farið í **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar** og ákveðið hvaða tiltektarstaðsetningar eru notaðar fyrir tiltekt sölupöntunar í vöruhúsi 51. (Frekari upplýsingar er að finna í [Stýra vöruhúsavinnu með vinnusniðmátum og staðsetningarleiðbeiningum](control-warehouse-location-directives.md).)
1. Athugið birgðastöðu á staðsetningum sem eiga við.
1. Leiðréttið birgðir eftir þörfum. Hægt er að búa til handvirkar hreyfingar, nota áfyllingu eða nota hvaða flæði sem er til að leiðrétta birgðirnar.

### <a name="part-1-create-picking-work"></a>Hluti 1: Búa til tiltekt

Áður en hafist er handa við stofnun vinnu skal ganga úr skugga um vöruhúsið sé sett upp til að svara vinnubeiðnum á tilætlaðan hátt.

Fylgið þessum skrefum til að búa til tiltektarvinnu.

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
1. Veljið **Ný** til að opna svargluggann **Stofna sölupöntun**.
1. Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:

    - Á flipanum **Viðskiptavinur** skaltu stilla reitinn **Reikningur viðskiptavinar** á _US-001_.
    - Í flýtiflipanum **Almennt** skal stilla reitinn **Vöruhús** á _51_.

1. Veljið **Í lagi** til að stofna sölupöntunina og loka svarglugganum.
1. Nýja sölupöntunin þín opnast. Hún felur í sér nýja, auða línu í hnitanetinu **Sölupöntunarlínur**. Í þessari pöntunarlínu skal stilla eftirfarandi gildi:

    - **Vörunúmer:** _M9200_
    - **Magn:** _20_
    - **Prófhópur:** _ea_

1. Veljið nýju pöntunarlínuna og síðan í valmyndinni **Birgðir** skal velja **Frátekning** til að opna síðuna **Frátekning**.
1. Á síðunni **Frátekning** skal velja **Frátektarlota** til að taka frá heildarmagn valdrar línu í vöruhúsinu.
1. Lokið síðunni **Frátekning** til að fara aftur í sölupöntunina.
1. Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Losa í vöruhús**. Kerfið stofnar sendingu, bætir henni við nýja hleðslu og stofnar nauðsynlega vinnu.
1. Stofnið aðra sölupöntun fyrir sama viðskiptavinalykil og vöruhús sem notað var fyrir fyrstu pöntunina. Bætið eftirfarandi tveimur pöntunarlínum við þessa pöntun:

    - **Lína 1:** Stillið reitinn **Vörunúmer** á _M9200_, reitinn **Magn** á _25_ og reitinn **Eining** á _ea_.
    - **Lína 2:** Stillið reitinn **Vörunúmer** á _M9202_, reitinn **Magn** á _10_ og reitinn **Eining** á _ea_.

1. Endurtakið skref 6 til 8 til að taka frá birgðir fyrir hverja pöntunarlínu (eina í einu) og endurtakið svo skref 9 til að losa pöntunina í vöruhúsið.

### <a name="part-2-change-the-location-for-a-work-line"></a>Hluti 2: Breyta staðsetningu vinnulínu

1. Opnaðu **Vöruhúsastjórnun \> Vinna \> Upplýsingar um vinnulínu**.
1. Finnið og veljið eina af vinnulínunum sem stofnaðar voru fyrir þessa sýniútgáfu.
1. Veljið **Breyta staðsetningu** til að opna svargluggann **Velja nýja staðsetningu**.
1. Í svarglugganum **Velja nýja staðsetningu**, í reitnum **Staðsetning**, skal velja nýja staðsetningu fyrir vinnulínuna.
1. Velja skal **Í lagi** til að gera breytinguna og loka svarglugganum.

> [!IMPORTANT]
> Aðeins er hægt að senda inn breytingar á staðsetningum ef nýja staðsetningin er með nægar birgðir tiltækar (fyrir tiltekt) eða ef hún kemst í gegnum staðfestingu staðsetningargerðar (fyrir frágang).

### <a name="part-3-change-the-quantity-of-a-work-line-or-cancel-a-work-line"></a>Hluti 3: Breyta magni vinnulínu eða hætta við vinnulínu

1. Opnaðu **Vöruhúsastjórnun \> Vinna \> Upplýsingar um vinnulínu**.
1. Finnið og veljið eina af vinnulínunum sem stofnaðar voru fyrir þessa sýniútgáfu. Athugið að aðeins er hægt að hætta við eða breyta magni fyrir vinnulínur þar sem vinnugerðin er _tiltekt_.
1. Veljið **Hætta við vinnulínu** til að opna svargluggann **Magn sem á að hætta við**.
1. Í svarglugganum **Magn sem á að hætta við** skal breyta gildinu í reitnum **Magn** til að tiltaka magnið sem á að *draga frá* magninu sem tiltekið í línunni eins og er. Sjálfgefið er að reiturinn **Magn** sýni fullt magn.

    - Ef hætt er við fullt magn verður gildinu **Staða verks** breytt í _Hætt við_, en reiturinn **Vinnumagn** sýnir áfram upprunalegt gildi.
    - Ef aðeins er hætt við hluta af magninu verður reiturinn **Vinnumagn** uppfærður til að sýna nýja magnið, en gildið **Staða verks** breytist ekki.

1. Velja skal **Í lagi** til að gera breytinguna og loka svarglugganum.

> [!IMPORTANT]
> Ef aðeins er hætt við hluta af magninu fyrir vinnulínu þarf einnig að fjarlægja úrelt magn úr farmlínunni. Að öðrum kosti, nema undirafhending sé sett upp á réttan hátt, er ekki hægt að staðfesta sendingu á farmlínu.
