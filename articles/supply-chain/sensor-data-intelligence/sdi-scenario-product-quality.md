---
title: Atburðarás vörugæða
description: Þessi grein veitir upplýsingar um atburðarás vörugæða. Þessi atburðarás notar skynjara til að mæla gæði vörulotu og myndar viðvörun ef mæling fellur utan skilgreinds þröskulds.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreNotification, IoTIntMfgResourceStatusConfiguration, IoTIntMfgResourceStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 8c4808ea3a0389c2a8699f0e11ea154705a6916d
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/08/2022
ms.locfileid: "9429001"
---
# <a name="the-product-quality-scenario"></a>Atburðarás vörugæða

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Í *vörugæði* atburðarás er skynjari settur upp til að mæla gæði vörulotu á verslunargólfinu. Ef mæling fellur utan skilgreinds þröskulds fyrir vöruna birtist tilkynning á mælaborði umsjónarmanns. Til dæmis er skynjari að mæla raka matvöru sem kemur út úr framleiðslulínunni. Ef mælingin er utan leyfilegs lágmarks- eða hámarksgildis fyrir raka fyrir vöruna er tilkynning gefin út.

## <a name="scenario-dependencies"></a>Ósjálfstæði sviðsmynda

The *vörugæði* atburðarás hefur eftirfarandi ósjálfstæði:

- Aðeins er hægt að kveikja á viðvörun ef framleiðslupöntun er í gangi á kortlagðri vél og ef sú vél er að framleiða vöru sem hefur kortlagða runueiginleika.
- Merki sem stendur fyrir runueigindina verður að vera send til IoT-miðstöðvar og einkvæmt heiti eiginleika verður að fylgja.

## <a name="prepare-demo-data-for-the-product-quality-scenario"></a>Undirbúa kynningargögn fyrir atburðarás vörugæða

Ef þú vilt nota kynningarkerfi til að prófa *vörugæði* atburðarás, notaðu kerfi þar sem [kynningargögn](../../fin-ops-core/fin-ops/get-started/demo-data.md) er uppsett skaltu velja *USMF* lögaðila (fyrirtæki), og undirbúa viðbótar kynningargögn eins og lýst er í þessum hluta. Ef þú ert að nota þína eigin skynjara og gögn geturðu sleppt þessum hluta.

Í þessum hluta muntu setja upp kynningargögnin þannig að þú getir notað útgefna vöru *P0111* (*Samsett hulstur*) með *vörugæði* atburðarás. Í þessari atburðarás rekur kerfið hvort gildi runueiginleika sem er mælt með skynjara sé utan skilgreinds þröskulds fyrir runueiginleika sem tengist vörunni.

### <a name="set-up-a-sensor-simulator"></a>Settu upp skynjarahermi

Ef þú vilt prófa þessa atburðarás án þess að nota líkamlegan skynjara geturðu sett upp hermi til að búa til nauðsynleg merki. Fyrir frekari upplýsingar, sjá [Settu upp herma skynjara til að prófa](sdi-set-up-simulated-sensor.md).

### <a name="associate-a-batch-attribute-and-resource-with-product-p0111"></a>Tengja runueiginleika og tilföng við vöru P0111

Fylgdu þessum skrefum til að tengja runueiginleika við vöru *P0111* (*Samsett hulstur*) og staðfestu þá auðlind *3118* (*Froðuskurðarvél*) er notað til þess.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Finndu og veldu vöruna þar sem **Vörunúmer** reiturinn er stilltur á *P0111*.
1. Á aðgerðarrúðunni, á **Stjórna birgðum** flipa, í **Hópeiginleikar** hópur, veldu **Vara sértæk**.
1. Á **Vara sértæk** síðu, veldu **Nýtt** til að búa til vörusértæka runueigind.
1. Á hausnum skaltu stilla eftirfarandi reiti:

    - **Eiginleikakóði** - Veldu umfang eiginda sem þú munt fylgjast með (*Tafla*, *·*, eða *Allt*). Fyrir þessa atburðarás skaltu velja *Tafla*, vegna þess að þú munt alltaf fylgjast með einum eiginleika.
    - **Eiginleikatengsl** - Veldu eigindina sem þú munt nota *vörugæði* atburðarás til að fylgjast með verðmæti. Fyrir þetta dæmi, veldu *Einbeiting*, sem er eiginleiki sem er innifalinn í stöðluðum kynningargögnum.

1. Á **Gildi** Flýtiflipi, í **Lágmark** og **Hámark** reiti, skilgreina svið ásættanlegra gilda sem eigindin verður að tilkynna til að standast gæðaeftirlitið. Ef skynjarinn tilkynnir um gildi utan þessa sviðs mun kerfið bera kennsl á það sem gæðabrot. Hinir reitirnir á þessum flýtiflipanum eiga ekki við um *vörugæði* atburðarás. Sjálfgefin gildi sem þú sérð núna koma frá kynningargögnunum. Þess vegna skaltu skilja þau eftir eins og þau eru og loka **Vara sértæk** síðu til að fara aftur á **Gefnar út upplýsingar um vöru** síðu fyrir hlut *P0111*.
1. Á aðgerðarrúðunni, á **Verkfræðingur** flipa, í **Útsýni** hópur, veldu **Leið**.
1. Á **Leið** síðu, á **Yfirlit** flipann neðst á síðunni, veldu línuna þar sem **Óper. Nei.** Reiturinn er stilltur á *30*.
1. Á **Auðlindaþörf** flipann neðst á síðunni, vertu viss um að tilföngin *3118* (*Froðuskurðarvél*) tengist aðgerðinni.

### <a name="create-and-release-a-production-order-for-product-p0111"></a>Stofna og gefa út framleiðslupöntun fyrir vöru P0111

Fylgdu þessum skrefum til að stofna og gefa út framleiðslupöntun fyrir vöru *P0111*.

1. Fara í **Framleiðslustýringar \> Framleiðslupantanir \> Allar framleiðslupantanir**.
1. Á **Allar framleiðslupantanir** síðu, á aðgerðarrúðunni, veldu **Ný lotupöntun**.
1. Í **Búðu til lotu** valmynd, stilltu eftirfarandi gildi:

    - **Vörunúmer:** *P0111*
    - **Magn:** *10*

1. Veldu **Búa til** til að búa til pöntunina og fara aftur í **Allar framleiðslupantanir** síðu.
1. Nota **Sía** reit til að leita að framleiðslupöntunum þar sem **Vörunúmer** reiturinn er stilltur á *P0111*. Finndu síðan og veldu framleiðslupöntunina sem þú varst að búa til.
1. Á aðgerðasvæðinu, í flipanum **Framleiðslupöntun**, í flokknum **Uppsetning**, skal velja **Áætla**.
1. Í **Áætlun** valmynd, veldu **Allt í lagi** til að keyra matið.
1. Á aðgerðarrúðunni, á **Framleiðslupöntun** flipa, í **Ferli** hópur, veldu **Gefa út**.
1. Í **Gefa út** í glugganum skaltu skrifa niður númer lotupöntunarinnar sem þú bjóst til.
1. Veldu **Allt í lagi** að gefa út pöntunina.

### <a name="configure-the-production-floor-execution-interface"></a>Grunnstilla viðmót fyrir framkvæmd á framleiðslugólfi

Ef þú hefur ekki þegar gert það skaltu stilla framkvæmdarviðmót framleiðslugólfs til að sýna verk sem eru úthlutað til tilföngs *3118* (*Froðuskurðarvél*). Fyrir leiðbeiningar, sjá eftirfarandi kafla:

- [Grunnstilla viðmót fyrir framkvæmd á framleiðslugólfi](sdi-scenario-equipment-downtime.md#config-pfe)
- [Virkjaðu leitarmöguleika á framkvæmdarviðmóti framleiðslugólfs](sdi-scenario-equipment-downtime.md#enable-pfe-search)

### <a name="start-the-first-job-in-the-batch-order"></a>Byrjaðu fyrsta verkið í runupöntuninni

Fylgdu þessum skrefum til að hefja fyrsta verkið í runupöntuninni.

1. Farið í **Framleiðslustýring \> Framkvæmd framleiðslu \> Framkvæmd á framleiðslugólfi**.
1. Í **Merki auðkenni** reit, slá inn *123*. Veldu síðan **skrá inn**.
1. Ef þú ert beðinn um fjarvistarástæðu skaltu velja eitt af kortunum fyrir fjarveru og síðan velja **Allt í lagi**.
1. Í **Leita** reit, sláðu inn lotupöntunarnúmerið sem þú skráðir áður. Veldu síðan **Til baka** lykill.
1. Veldu pöntunina og veldu síðan **Byrja starf**.
1. Í **Byrja starf** valmynd, veldu **Byrjaðu**.

## <a name="set-up-the-product-quality-scenario"></a>Settu upp atburðarás vörugæða

Fylgdu þessum skrefum til að setja upp *vörugæði* atburðarás í Supply Chain Management.

1. Fara til **Framleiðslueftirlit \> Uppsetning \> Sensor Data Intelligence \> Sviðsmyndir**.
1. Í **Vörugæði** atburðarás kassi, veldu **Stilla** til að opna uppsetningarhjálpina fyrir þessa atburðarás.
1. Á **Skynjarar** síðu, veldu **Nýtt** til að bæta skynjara við ristina. Stilltu síðan eftirfarandi reiti fyrir það:

    - **Auðkenni skynjara** – Sláðu inn auðkenni skynjarans sem þú ert að nota. (Ef þú ert að nota Raspberry PI Azure IoT Online Simulator og hefur sett hann upp eins og lýst er í [Settu upp herma skynjara til að prófa](sdi-set-up-simulated-sensor.md), koma inn *Gæði* .)
    - **Lýsing á skynjara** – Sláðu inn lýsingu á skynjaranum.

1. Endurtaktu fyrra skref fyrir hvern viðbótarskynjara sem þú vilt bæta við núna. Þú getur komið aftur og bætt við fleiri skynjurum hvenær sem er.
1. Veljið **Næst**.
1. Á **Kortlagning viðskiptaskráa** síðu, í **Skynjarar** kafla, veldu skrána fyrir einn af skynjurunum sem þú varst að bæta við.
1. Í **Kortlagning viðskiptaskráa** kafla, veldu **Nýtt** til að bæta línu við ristina.
1. Á nýju röðinni er **Tegund viðskiptaskrár** reiturinn ætti sjálfkrafa að vera stilltur á *Tilföng (WrkCtrTable)*. Stilltu **Viðskiptaskrá** reitnum við auðlindina sem þú notar valinn skynjara til að fylgjast með. (Ef þú ert að nota kynningargögnin sem þú bjóst til fyrr í þessari grein, stilltu þau á *3118, Froðuskurðarvél* .)
1. Strax eftir að þú hefur valið tegund viðskiptaskrár fyrir línuna sem þú bættir við í fyrra skrefi er annarri línu sjálfkrafa bætt við hnitanetið. Á þessari röð er **Tegund viðskiptaskrár** reit ætti að vera stillt á *Hópeiginleikar (PdsBatchAttrib)*. Stilltu **Viðskiptaskrá** reitnum við lotueiginleikann sem þú notar valinn skynjara til að fylgjast með. (Ef þú ert að nota kynningargögnin sem þú bjóst til fyrr í þessari grein, stilltu þau á *Styrkur, styrkur prósenta* .)
1. Veljið **Næst**.
1. Á **Virkjaðu skynjara** síðu, í hnitanetinu, veldu skynjarann sem þú bættir við og veldu síðan **Virkjaðu**. Fyrir hvern virkan skynjara í ristinni birtist gátmerki í **Virkur** dálki.
1. Veljið **Ljúka**.

## <a name="work-with-the-product-quality-scenario"></a>Vinna með atburðarás vörugæða

### <a name="view-product-quality-data-on-the-resource-status-page"></a>Skoðaðu gögn um gæði vöru á síðunni Tilfangsstaða

Á **Auðlindastaða** síðu geta umsjónarmenn fylgst með tímalínu vörugæðamerkisins sem er móttekið frá skynjurum sem eru kortlagðar á hverja vélaauðlind. Fylgdu þessum skrefum til að stilla tímalínuna.

1. Fara til **Framleiðslueftirlit \> Framleiðsluframkvæmd \> Auðlindastaða**.
1. Í **Stilla** valmynd, stilltu eftirfarandi reiti:

    - **Auðlind** - Veldu úrræði sem þú vilt fylgjast með. (Ef þú ert að vinna með kynningargögnin skaltu velja *3118* .)
    - **Tímaröð 1** – Veldu færsluna (mælingarlykill) sem hefur eftirfarandi snið fyrir nafnið: *Vörugæði:&lt; JobId&gt; :&lt; Eiginleikanafn&gt;*
    - **Birta nafn** - Koma inn *Eiginleikagildi runu*.

Eftirfarandi mynd sýnir dæmi um vörugæðisgögn um **Auðlindastaða** síðu þegar gildið er á bilinu viðunandi gilda.

![Vörugæðagögn á síðunni Tilfangsstaða þegar gildið er innan marka.](media/sdi-product-quality-in-range.png "Vörugæðagögn á síðunni Tilfangsstaða þegar gildið er innan marka")

Eftirfarandi mynd sýnir dæmi um vörugæðagögn þegar gildi utan sviðs er greint.

![Vörugæðagögn á síðunni Tilfangsstaða þegar gildi utan sviðs er greint.](media/sdi-product-quality-out-of-range.png "Vörugæðagögn á síðunni Tilfangsstaða þegar gildi utan sviðs er greint")

### <a name="view-product-quality-data-on-the-notifications-page"></a>Skoðaðu vörugæðagögn á tilkynningasíðunni

Á **Tilkynningar** síðu, umsjónarmenn geta skoðað tilkynninguna sem myndast þegar skynjarinn mælir lotueiginleikagildi sem fellur utan skilgreinds þröskulds fyrir lotueiginleikann. Hver tilkynning veitir yfirlit yfir framleiðsluverkið sem verður fyrir áhrifum af biluninni og gefur möguleika á að endurúthluta viðkomandi verki í annað tilfang.

Til að opna **Tilkynning** síðu, farðu á **Framleiðslueftirlit \> Fyrirspurnir og skýrslur \> Sensor Data Intelligence \> Tilkynningar**.

Eftirfarandi mynd sýnir dæmi um tilkynningu um gæði vöru.

![Dæmi um vörugæðatilkynningu.](media/sdi-product-quality-notification.png "Dæmi um vörugæðatilkynningu")
