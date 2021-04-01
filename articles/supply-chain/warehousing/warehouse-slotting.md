---
title: Hólfaskipting vöruhúss
description: Þetta efni inniheldur upplýsingar um hólfaskiptingu vöruhúss. Hólfaskipting vöruhúss gerir þér kleift að sameina eftirspurn eftir vöru og mælieiningu frá pöntunum með stöðuna Pöntuð, Frátekin eða Sleppt. Slíkt aðstoðar stjórnendur vöruhúsa að skipuleggja betur tiltektarstaðsetningar áður en þeir sleppa pöntunum til vöruhússins og búa til tiltektarvinnu.
author: mirzaab
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 0851af976dd73b7f13372880587187f546091bec
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248596"
---
# <a name="warehouse-slotting"></a>Hólfaskipting vöruhúss

[!include [banner](../includes/banner.md)]

Ýmsir eiginleikar fyrir hólfaskiptingu vöruhúss eru í boði til að aðstoða stjórnendur vöruhúsa að skipuleggja betur tiltektarstaðsetningar áður en þeir sleppa pöntunum til vöruhússins og búa til tiltektarvinnu.

Eiginleikinn *Hólfaskipting vöruhúss* gerir þér kleift að sameina eftirspurn eftir vöru og mælieiningu frá pöntunum með stöðuna *Pöntuð*, *Frátekin* eða *Sleppt*. Tilbúna eftirspurn er síðan hægt að nota á staðsetningar sem verða notaðar fyrir tiltekt miðað við magn, einingu, efnislegar víddir, fastar staðsetningar o.s.frv. Þegar áætlunin um hólfaskiptingu er tilbúin er hægt að stofna áfyllingarvinnu til að færa rétt magn birgða í hverja staðsetningu.

Eiginleikinn *Vöruhúsahólf fyrir flutningspantanir* heimilar stjórnendum vöruhúss að fylla á tiltektarstaðsetningar samkvæmt eftirspurn flutningspantana sem ekki er enn búið að losa úr vöruhúsinu. Slíkt tryggir að í tiltektarstaðsetningunum verði allar vörurnar sem þarf fyrir flutningspantanir þegar þær eru losaðar í vöruhús. Þessi eiginleiki krefst þess að eiginleikinn *Hólfaskipting vöruhúss* sé einnig virkjaður.

Eiginleikinn *Endurbætur á úthlutun hólfaskiptingar í vöruhúsi* bætir við valkosti fyrir sniðmátslínur sem eru notaðar af eiginleikanum *Hólfaskipting vöruhúss*. Valkosturinn gerir kerfinu kleift að íhuga fyrirliggjandi lagerbirgðir á viðtökustað. Þar af leiðandi kunna færri áfyllingar að vera búnar til fyrir hólf. Eiginleikinn *Endurbætur á úthlutun hólfaskiptingar í vöruhúsi* krefst þess að eiginleikinn *Hólfaskipting vöruhúss* sé einnig virkjaður. Einnig er hægt að nota hann ásamt eiginleikanum *Vöruhúsahólf fyrir flutningspantanir*.

## <a name="turn-on-the-warehouse-slotting-features"></a>Kveikja á eiginleikum fyrir hólfaskiptingu vöruhúss

Áður en hægt er að nota slíka eiginleika verður að vera kveikt á þeim í kerfinu. Stjórnendur geta notað stillingar [eiginleikastjórnunar](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikanna og kveikja á þeim ef þörf krefur. Kveikja skal á eftirfarandi eiginleikum eftir því sem þörf krefur:

- Hólfaröðunareiginleiki vöruhúss
- Vöruhúsahólf fyrir flutningspantanir

    > [!IMPORTANT]
    > Kveikja verður á eiginleikanum *Vöruhúsahólf fyrir flutningspantanir* áður en kveikt er á þessum eiginleika.

- Endurbætur á úthlutun hólfaskiptingar í vöruhúsi

    > [!IMPORTANT]
    > Kveikja verður á eiginleikanum *Vöruhúsahólf fyrir flutningspantanir* áður en kveikt er á þessum eiginleika.

## <a name="set-up-warehouse-slotting"></a>Setja upp hólfaskiptingu vöruhúss

Þú verður að setja upp eftirfarandi eiginleika í kerfinu til að hægt sé að nota hólfaskiptingu vöruhúss:

- Mælieiningarlög hólfaskiptingar
- Leiðbeiningarkóðar
- Hólfaskiptingarsniðmát
- Staðsetningarleiðbeiningar

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a>Búa til mælieiningarlag fyrir hólfaskiptingu

Mælieiningarlög gera kleift að flokka margar mælieiningar saman í þeim tilgangi að skipta niður í hólf. Til dæmis, ef kassar í mörgum stærðum eru teknir af sama tiltektarsvæði kassa, er hægt að búa til eitt lag fyrir allar stærðirnar. **Búa verður til línu fyrir hverja mælieiningu sem ætti að vera hluti af stiginu.**

1. Opnaðu **Vöruhúsakerfi \> Uppsetning \> Áfylling \> Hólfaskiptieining fyrir mælieiningarlög**.
1. Veljið **Nýtt**.
1. Stilla eftirfarandi gildi í hausnum:

    - **Mælieiningarlag:** *EaBoxPl*
    - **Lýsing:** *Hvert vörubretti með kössum*

1. Veljið **Vista**.
1. Á flýtiflipanum **Mælieiningar** velur þú **Ný** til að bæta línu við hnitanetið.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **Eining:** *Kassi*
    - **Lýsing:** Hafðu svæðið autt. Þetta svæði er sjálfkrafa fyllt út um leið og breytingarnar eru vistaðar.
    - **Einingarflokkur:** *Magn*

1. Veldu **Ný** til að bæta annarri línu við hnitanetið.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **Prófhópur:** *ea*
    - **Lýsing:** Hafðu svæðið autt. Þetta svæði er sjálfkrafa fyllt út um leið og breytingarnar eru vistaðar.
    - **Einingarflokkur:** *Magn*

1. Veldu **Ný** til að bæta þriðju línunni við hnitanetið.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **Eining:** *VÖRUBRETTI*
    - **Lýsing:** Hafðu svæðið autt. Þetta svæði er sjálfkrafa fyllt út um leið og breytingarnar eru vistaðar.
    - **Einingarflokkur:** *Magn*

1. Veljið **Vista** til að vista lagið.

### <a name="create-a-directive-code-for-slotting"></a>Búa til leiðbeiningarkóða fyrir hólfaskiptingu

Þú verður að velja leiðbeiningarkóða sem ætti að tengjast sniðmáti.

1. Opnaðu **Vöruhúsakerfi \> Uppsetning \> Leiðbeiningarkóðar**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Í svæðinu **Leiðbeiningarkóði** skaltu slá inn *Hólfaskipting*.
1. Í svæðinu **Lýsing leiðbeiningar** skaltu slá inn *Hólfaskipting*.

### <a name="set-up-slotting-templates"></a>Setja upp hólfaskiptingarsniðmát

Hvert hólfaskiptingarsniðmát stjórnar því hvernig birgðum er úthlutað á staðsetningar í tilteknu vöruhúsi. Hvert sniðmát verður að innihalda línu fyrir hverja forskrift hólfaskiptingar. Notaðu ferlin í þessum hluta til að setja upp hólfaskiptingarsniðmát.

1. Opnaðu **Vöruhúsakerfi \> Uppsetning \> Áfylling \> Hólfaskiptingarsniðmát**.
1. Veldu **Nýtt** til að búa til sniðmát.

Því næst verður þú að setja upp sniðmáthaus, forskriftir hólfaskiptingar og staðsetningarleiðbeiningar, eins og útskýrt er í eftirfarandi undirköflum. Uppsetning fyrir flutningspantanir líkist uppsetningu fyrir sölupantanir, en svæðið **Gerð eftirspurnar** er stillt á *Flutningspantanir* í staðinn fyrir *Sölupantanir*.

#### <a name="set-up-the-header-for-a-sales-order-slotting-template"></a>Setja upp haus fyrir hólfasniðmát sölupöntunar

1. Stilltu eftirfarandi gildi í sniðmátshausnum:

    - **Hólfaskiptingarsniðmát:** _61_
    - **Lýsing:** _61_
    - **Gerð eftirspurnar:** *Sölupöntun*

        > [!NOTE]
        > Eins og stendur eru *Sölupantanir* og *Flutningspantanir* einu gerðir eftirspurnar sem eru studdar. Þú getur einungis valið *Flutningspantanir* ef kveikt er á eiginleikanum *Vöruhúsahólf fyrir flutningspantanir*.

    - **Eftirspurnarstefna:** _Pöntuð_

        Eftirtalin gildi eru tiltæk á þessu svæði:

        - **Pantað** – Allt pantað magn á sölupöntuninni skal telja sem eftirspurn.
        - **Frátekið** – Aðeins magn af sölupöntunarlínu sem er frátekið (efnislega og pantað) ætti að teljast sem eftirspurn.
        - **Losað** – Losað magn skal flokka sem eftirspurn.

    - **Vöruhús:** _61_
    - **Leyfa bylgjueftirspurn að nota magn sem ekki er frátekið:** _Já_

Þú getur einnig tilgreint fyrirspurn til að þrengja umfang eftirspurnar sem er metin.

#### <a name="set-up-slotting-specifications-for-each-template"></a>Settu upp forskriftir hólfaskiptingar fyrir hvert sniðmát

Fylgdu þessum skrefum fyrir hvert pöntunarsniðmát sem þú býrð til að bæta við línu fyrir hverja forskrift hólfaskiptingar.

1. Á flýtiflipanum **Upplýsingar um hólfaskiptingarsniðmát** velur þú **Nýtt** til að búa til nýja sniðmátslínu.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **Röð:** _1_
    - **Lýsing:** _Föst staðsetning_
    - **Lágmarksmagn:** _1_

        Þetta svæði skilgreinir áskilið lágmarksmagn eftirspurnar fyrir línuna.

    - **Hámarksmagn:** _1000000_

        Þetta svæði skilgreinir áskilið hámarksmagn eftirspurnar sem er gilt fyrir línuna.

    - **Eining:** Hafðu þetta svæði autt.

        Þetta svæði skilgreinir mælieininguna sem lágmarks- og hámarksmagnið vísa til.

    - **Mælieiningarlag:** _EaBoxPl_

        Þetta svæði skilgreinir mælieiningar eftirspurnar sem gilda fyrir línuna. (Frekari upplýsingar er að finna í hlutanum [Uppsetning á mælieiningarlögum fyrir hólfaskiptingu](#unit-tiers) fyrr í þessu efnisatriði).

    - **Skilyrði úthlutunar hólfa:** _Taka mið af magni_

        Eftirtalin gildi eru tiltæk á þessu svæði:

        - **Gera ráð fyrir að staðsetning sé tóm** – Þetta kerfi ætti að gera ráð fyrir að allar staðsetningar á tiltektarsvæðinu séu tómar og ætti ekki að athuga áðurnefndar staðsetningar fyrir birgðir.
        - **Gera ráð fyrir magni á staðsetningu** – Kerfið ætti að athuga staðsetningu á tiltektarsvæðinu fyrir birgðir og ætti að sleppa öllum staðsetningum sem eru ekki tómar.
        - **Íhuga magn í birgðum** – kerfið ætti að athuga hvort einhver viðtökustaður innihaldi magn sem er ekki frátekið fyrir vöruna í eftirspurnarlínunni. Þegar magnið er nægilega mikið til að uppfylla að minnsta kosti eina einingu eftirspurnarlínunnar, er færsla áætlunar fyrir hólfaskiptingu færð niður í tiltækt magn. Þegar eftirspurn er t.d. 10 tilvik og eitt tilvik er á lager verður fundin eftirspurn í níu tilvikum. Þegar eftirspurn er 10 tilvik og hvert þeirra er á lager verður fundin eftirspurn í 10 tilvikum. Þetta gildi er aðeins tiltækt þegar kveikt er á eiginleikanum *Endurbætur á úthlutun hólfaskiptingar í vöruhúsi*.

    - **Leiðbeiningarkóði:** _Hólfaskipting_

        Þetta svæði skilgreinir staðsetningarleiðbeiningarnar sem eru notaðar til að finna tiltektarstaðsetningu áfyllingarvinnunnar.

    - **Yfirflæði á staðsetningu:** Hafðu þetta svæði autt.

        Þetta svæði skilgreinir staðsetningu sem birgðir eru settar ef staðsetning finnst ekki fyrir magnið við vinnslu línunnar.

    - **Leyfa stöðvun:** _já_

        Þegar þessi valkostur er stilltur á *Já*, ef ekki er hægt að skipta einhverri eftirspurn í hólf, verður búin til birgðahreyfing til að taka birgðum úr staðsetningum þar sem engar birgðir eru, en engu var skipt niður í hólf. Sniðmátið er síðan keyrt aftur. Í þetta sinn hunsar það birgðir í staðsetningum. Þessi eiginleiki virkar best þegar svæðið **Úthluta skilyrðum fyrir hólf** er stillt á _Taka mið af magni_.

    - **Notkun fastrar staðsetningar:** _Aðeins fastar staðsetningar fyrir afurðina_

        Eftirtalin gildi eru tiltæk á þessu svæði:

        - **Fastar og lausar staðsetningar** – Ekki ætti að takmarka kerfið við að nota aðeins fastar staðsetningar.
        - **Aðeins fastar staðsetningar fyrir afurðina** – Kerfið ætti aðeins að skipta niður í hólf á staðsetningar sem eru fastar staðsetningar fyrir afurðina.
        - **Aðeins fastar staðsetningar fyrir afurðarafbrigðið** – Kerfið ætti aðeins að skipta niður í hólf á staðsetningar sem eru fastar staðsetningar fyrir afurðarafbrigðið.

> [!NOTE]
> Ef hólfasniðmátið inniheldur að minnsta kosti eina línu þar sem svæðið **Úthluta skilyrðum fyrir hólf** er stillt á *Íhuga magn í birgðum* er yfirflæði ekki lengur leyft fyrir neina línu í sniðmátinu.

1. Veljið **Vista**.
1. Veldu **Ný** til að búa til aðra sniðmátslínu.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **Röð:** _2_
    - **Lýsing:** _Annað_
    - **Lágmarksmagn:** _1_
    - **Hámarksmagn:** _1000000_
    - **Eining:** Hafðu þetta svæði autt.
    - **Mælieiningarlag:** _EaBoxPl_
    - **Skilyrði úthlutunar hólfa:** _Taka mið af magni_
    - **Leiðbeiningarkóði:** _Hólfaskipting_
    - **Yfirflæði á staðsetningu:** Hafðu þetta svæði autt.
    - **Leyfa stöðvun:** _já_
    - **Nota fastar staðsetningar:** _Fastar og lausar staðsetningar_

    Í fyrirspurninni fyrir aðra línuna tilgreinir þú skilyrðin sem eru notuð til að ákvarða hvaða staðsetningar eftirspurnar fyrir umrædda línu er hægt að skipa í hólf.

1. Veldu línuna þar sem svæðið **Runa** er stillt á *2*.
1. Veldu **Breyta fyrirspurn**.
1. Á flipanum **Svið** velur þú **Bæta við** til að bæta línu við hnitanetið.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **Tafla:** *Staðir*
    - **Afleidd tafla:** *Staðsetningar*
    - **Reitur:** *Auðkenni forstillingar staðsetningar*
    - **Skilyrði:** *Tiltekt-06* (Veldu tvöfalt plúsmerki \[**++**\] á svæðinu til að stækka listann, og veldu síðan *Tiltekt-06* - *Tiltektarsvæði 6*.)

1. Veljið **Í lagi**.

#### <a name="set-up-location-directives"></a>Setja upp staðsetningarleiðbeiningar

Setja þarf upp að minnsta kosti eina staðsetningarleiðbeiningar til að styðja tiltekt við hólfaskiptingu. Notaðu verklagsreglurnar í þessum kafla til að setja upp nýjar *staðsetningarleiðbeiningar fyrir áfyllingu* fyrir tiltekt við hólfaskiptingu.

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar**.
1. Í svæðinu **Gerð verkbeiðni** í vinstri glugganum velur þú *Áfylling*.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Í haus nýju staðsetningarleiðbeininganna á svæðinu **Heiti** slærðu inn *61 Tiltekt við hólfaskiptingu*.
1. Samþykktu sjálfgildið í svæðinu **Raðnúmer**.

##### <a name="configure-the-location-directives-fasttab"></a>Grunnstilling flýtiflipans Staðsetningarleiðbeiningar

1. Stilltu eftirfarandi gildi á flýtiflipanum **staðsetningarleiðbeiningar**. Samþykktu sjálfgildin fyrir öll önnur svæði.

    - **Tegund vinnu:** _Tínsla_
    - **Svæði:** _6_
    - **Vöruhús:** _61_
    - **Leiðbeiningarkóði:** _Hólfaskipting_

1. Veldu **Vista** til að gera flýtiflipann **Línur** tiltækan.

##### <a name="configure-the-lines-fasttab"></a>Grunnstilling flýtiflipans Línur

1. Á flýtiflipanum **Línur** velur þú **Ný** til að búa til línu.
1. Stilltu eftirfarandi gildi á nýju línunni.

    - **Frá-magn:** _0_
    - **Til magn:** _1000000_

1. Samþykkið sjálfgefin gildi fyrir reitina sem eftir eru.
1. Veldu **Vista** til að gera flýtiflipann **Aðgerðir í staðsetningarleiðbeiningum** tiltækan.

##### <a name="configure-the-location-directive-actions-fasttab"></a>Grunnstilling flýtiflipans Aðgerðir í staðsetningarleiðbeiningum

1. Á flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** velur þú **Ný** til að búa til línu.
1. Stilltu eftirfarandi gildi á nýju línunni. Samþykktu sjálfgildin fyrir öll önnur svæði.

    - **Raðnúmer:** Samþykkja sjálfgildið.
    - **Heiti:** _Magn_
    - **Áætlun:** _Engin_

1. Samþykkið sjálfgefin gildi fyrir reitina sem eftir eru.
1. Veldu **Vista** til að gera hnappinn **Breyta fyrirspurn** tiltækan.

##### <a name="edit-the-query"></a>Breyta fyrirspurn

1. Í flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** skal velja **Breyta fyrirspurn**.
1. Á flipanum **Svið** velur þú **Bæta við** til að bæta línu við hnitanetið.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **Tafla:** *Staðir*
    - **Afleidd tafla:** *Staðsetningar*
    - **Reitur::** *Auðkenni svæðis*
    - **Skilyrði:** *Magn* (Veldu tvöfalt plúsmerki \[**++**\] á svæðinu til að stækka listann, og veldu síðan *Magn*).

1. Veljið **Í lagi**.

## <a name="scenario"></a>Aðstæður

### <a name="set-up-the-scenario"></a>Setja upp aðstæður

Notaðu innbyggðu sýnigögnin fyrir þessar aðstæður og búðu til skrárnar sem lýst er í þessum hluta.

#### <a name="use-the-usmf-sample-data"></a>Nota USMF-sýnigögn

Til að vinna í gegnum þessar aðstæður með því að nota sýnigögnin og gildin sem eru tilgreind hér verður þú að vera á kerfi þar sem venjuleg [sýnigögn](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er sett upp. Þar að auki verður þú að velja **USMF**-lögaðila áður en þú byrjar.

#### <a name="create-demand"></a>Búa til eftirspurn

Fylgdu eftirfarandi skrefum til að búa til eftirspurn sem verður notuð við hólfaskiptingu.

1. Opnið **Sala og markaðssetning \> Sölupantanir \> Allar sölupantanir**.
1. Smellið á **Nýtt** til að stofna nýja sölupöntun.
1. IÍ svarglugganum **Búa til sölupöntun** í svæðinu **Viðskiptavinalykill** skaltu velja _US-007_.
1. Í reitnum **Vöruhús** skal velja _61_.
1. Veljið **Í lagi**.
1. Ný sölupöntun opnast. Hún inniheldur tóma línu á flýtiflipanum **Sölupöntunarlína**. Stilltu eftirfarandi gildi á þessari línu:

    - **Vara:** _L0101_
    - **Magn:** _20_

1. Veldu **Bæta við línu** til að bæta við nýrri línu og stilltu eftirfarandi gildi:

    - **Vara:** _T0100_
    - **Magn:** _8_

1. Veljið **Vista**.
1. Veldu **Nýtt** til að búa til aðra sölupöntun.
1. IÍ svarglugganum **Búa til sölupöntun** í svæðinu **Viðskiptavinalykill** skaltu velja _US-008_.
1. Í reitnum **Vöruhús** skal velja _61_.
1. Ný sölupöntun opnast. Hún inniheldur tóma línu á flýtiflipanum **Sölupöntunarlína**. Stilltu eftirfarandi gildi á þessari línu:

    - **Vara:** _T0100_
    - **Magn:** _1_

1. Veljið **Vista**.

### <a name="walk-through-a-typical-slotting-scenario"></a>Handleiðsla í gegnum hefðbundnar aðstæður við hólfaskiptingu

Þegar öll skilyrði eru uppfyllt, eins og lýst er í fyrri hlutanum, ertu tilbúinn að prófa eiginleikann með því að vinna í gegnum hverja æfingu í þessum kafla.

#### <a name="generate-demand"></a>Búa til eftirspurn

1. Opnaðu **Vöruhúsakerfi \> Uppsetning \> Áfylling \> Hólfaskiptingarsniðmát** og veldu hólfaskiptingarsniðmátið sem þú bjóst til áður.
1. Á aðgerðasvæðinu skal velja **Búa til eftirspurn**. Þessi skipun metur alla eftirspurn sem er í kerfinu og samsvarar fyrirspurninni um hólfaskiptingarsniðmátið. Heildareftirspurn yfir allar pantanir er síðan sameinaður í eina línu fyrir hvert magn/mælieining. Upplýsingaboð birtast þegar ferlið er fullklárað.

#### <a name="slotting-demand"></a>Eftirspurn eftir hólfaskiptingu

*Eftirspurn eftir hólfaskiptingu* sýnir niðurstöður myndunar eftirspurnar miðað við uppsetningu hólfaskiptingarsniðmátsins.

- Á aðgerðarsvæðinu velur þú **Eftirspurn eftir hólfaskiptingu** til að skoða niðurstöður skipunarinnar **Búa til eftirspurn**. Hægt er að breyta línunum í eftirspurn eftir hólfaskiptingu. Þú getur eytt línu, bætt við nýrri línu eða breytt upplýsingum um línuna.

> [!NOTE]
> Þú getur breytt eftirspurn handvirkt, eða þú getur flutt hana inn frá utanaðkomandi kerfi með gagnastjórnun. Allt efni í eftirspurn eftir hólfaskiptingu er notað í næsta skrefi, óháð því hvaðan hún kom.

#### <a name="locate-demand"></a>Finna eftirspurn

Eftir að eftirspurn hefur verið mynduð verður þú að nota skipunina **Finna eftirspurn** til að búa til *áætlunina um hólfaskiptingu*.

- Á aðgerðasvæðinu skal velja **Finna eftirspurn**. Hólfaskiptingarferlið er keyrt. Upplýsingaboð birtast þegar ferlið er fullklárað.

#### <a name="slotting-plan"></a>Hólfaskiptingaráætlun

Áætlunin fyrir hólfaskiptingu sýnir staðsetningu sem hverri vöru/magni var úthlutað, hvort yfirflæði var notað, hvort vinnustöðvun var búin til og sniðmátalínan sem var notuð. *Eftirspurn sem ekki var hægt að skipa í hólf er auðkennd með rauðu.*

- Á aðgerðarsvæðinu velur þú **Áætlun fyrir hólfaskiptingu** til að skoða niðurstöðurnar.

> [!NOTE]
> - Ferlin **Búa til eftirspurn**, **Finna eftirspurn** og **Keyra áfyllingu** ferli eru nú keyrð í sandkassa. (Þessir ferlar eru tiltækir á aðgerðasvæðinu á síðunni **Hólfasniðmát**.)
> - Ferlin **Búa til eftirspurn**, **Finna eftirspurn** og **Keyra áfyllingu** ferli eru læst til að tryggja að ekki sé hægt að virkja þau samtímis. Að öðrum kosti kann gögnunum sem eru notuð að vera eytt.
> - Ferlin **Búa til eftirspurn** og **Finna eftirspurn** sýna viðvörun ef keyrslan myndar ekki færslur eða ef upplýsingar vantar um færslurnar.
> - Þegar þú velur **Hólfaáætlun** birtast hnapparnir **Nýtt**, **Breyta** eða **Eyða** á aðgerðasvæðinu vegna þess að ekki er hægt að gera breytingar á gagnagjafanum.
> - Þegar þú smellir á **Keyra áfyllingu** villuleitar kerfið í völdum hólfasniðmátum og ferlum.

#### <a name="create-replenishment"></a>Stofna áfyllingu

Þegar áætlun fyrir hólfaskiptingu hefur verið búin til verður þú að búa til *áfyllingarvinnu* miðað við áætlunina.

- Á aðgerðasvæðinu skal velja **Keyra áfyllingu**. Upplýsingaboð birtast þegar ferlið er fullklárað. Þessi skilaboð gefa til kynna fjölda hausa sem voru búnir til fyrir smíðakenni vinnu.

Staðsetningarleiðbeiningar sem notaðar verða eru auðkenndar út frá leiðbeiningarkóðanum sem er tilgreindur á hverri sniðmátslínu.

## <a name="tips"></a>Ábendingar

### <a name="set-up-automatic-slotting"></a>Setja upp sjálfvirka hólfaskiptingu

Eftir að allir nauðsynlegir þættir eru til staðar geturðu sett upp hólfaskiptingu til að keyra sjálfkrafa með því að fylgja þessum skrefum.

1. Opnaðu **Vöruhúsakerfi \> Áfylling \> Keyra hólfaskiptingu**.
1. Tilgreindu skref hólfaskiptingar sem á að keyra. Veldu eitt eða fleiri af eftirfarandi skrefum hólfaskiptingar:

    - Búa til eftirspurn
    - Finna eftirspurn
    - Stofna áfyllingarvinnu

    > [!NOTE]
    > Skrefin við hólfaskiptingu eru samfelld. Ef þú vilt velja *Finna eftirspurn* verður þú fyrst að velja *Búa til eftirspurn*.

1. Tilgreindu hólfaskiptingarsniðmátið sem á að nota.
1. Stilltu endurtekninguna til að keyra sjálfkrafa ef þú vilt.

Þegar aðstæður eru æfðar skal **ekki** setja upp sjálfvirka hólfaskiptingu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]