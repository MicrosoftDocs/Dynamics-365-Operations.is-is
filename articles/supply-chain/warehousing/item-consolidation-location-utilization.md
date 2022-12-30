---
title: Vörusameining - nýting á staðsetningu
description: Í þessari grein er að finna upplýsingar um virkni sem auðveldar stjórnendum vöruhúss að skoða og sía rúmmálsnýtingu staðsetninga í öllu vöruhúsinu. Stjórnendur geta valið staðsetningar og búið til birgðahreyfingarvinnu beint úr síðu Vörusameiningar til að sameina vörur og þar af leiðandi nýta betur rými vöruhússins.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSPhysDimUOM, WHSMovementType, WHSItemConsolidationForm, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: d0e52769de3f200e2bb3060b3d9cb19dc0847b69
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336424"
---
# <a name="item-consolidation---location-utilization"></a>Vörusameining - nýting á staðsetningu

[!include [banner](../includes/banner.md)]

Í þessari grein er að finna upplýsingar um virkni sem auðveldar stjórnendum vöruhúss að skoða og sía rúmmálsnýtingu staðsetninga í öllu vöruhúsinu. Stjórnendur geta valið staðsetningar og búið til birgðahreyfingarvinnu beint úr síðunni **Vörusameining** til að sameina vörur og þar af leiðandi nýta betur rými vöruhússins.

## <a name="turn-on-the-features"></a>Kveikja á eiginleikum

Áður en hægt er að nota eiginleikana sem lýst er í þessari grein þarf að kveikja á þeim í kerfinu. Stjórnendur geta notað vinnusvæðið [Eiginleikastjórnunar](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu þessara eiginleika og kveikja á þeim ef þörf krefur. Kveikja á báðum eiginleikum, í þeirri röð sem þeir eru sýndir. (Báðir eiginleikarnir eru fyrir eininguna **Vöruhúsastjórnun**.)

1. *Staðsetningarstaða vöruhúss*<br>(Frá og með útgáfu 10.0.29 af Supply Chain Management er hún skylda og ekki er hægt að slökkva á henni.) Frekari upplýsingar er að finna í [Staðsetningarstaða vöruhúss](warehouse-location-status.md).)
2. *Nýting á staðsetningu samstæðuvöru*<br>(Sem hluti af Supply Chain Management, útgáfa 10.0.29, er sjálfgefið kveikt á þessum eiginleika.)

## <a name="warehouse-location-status"></a>Staðsetningarstaða vöruhúss

Eiginleikinn *Staðsetningarstaða vöruhúss* bætir fjórum nýjum reitum við síðuna **Staðsetningar** til að halda utan um viðbótarupplýsingar um núverandi stöðu staðsetningar:

- **Vörunúmer** – Varan sem er núna í staðsetningunni. Ef staðsetningin inniheldur margar vörur er þessi reitur auður.
- **Dagsetning og tími síðustu virkni** – Tímastimpill síðustu færslu vöruhúss sem var framkvæmd á staðsetningunni.
- **Aldursdagsetning** –Dagsetningin sem birgðir í staðsetningu voru færðar inn í vöruhúsið. Þetta gildi er reiknað út frá aldursdagsetningu númeraplötunnar. Þó þessi dagsetning sé nákvæm fyrir staðsetningar sem er raktar með númeraplötu er hugsanlega ekki nákvæmt fyrir staðsetningar ekki raktar með númeraplötu.
- **Staðsetningarstaða** – Staða staðsetningarinnar. Fjögur gildi eru í boði:

    - **Óákveðið** – Staðsetningarforstillingin rekur ekki stöðuna. Þar af leiðandi er núverandi staða óþekkt.
    - **Autt** – Engar birgðir eru á staðsetningunni sem stendur.
    - **Tiltekt** – Færslur á útleið hafa verið framkvæmdar á staðsetningunni eftir að hún var síðast tóm.
    - **Geymsla** – Aðeins færslur á innleið hafa verið framkvæmdar frá því að staðsetningin var síðast tóm.

Þessi svæði gefa stjórnendum vöruhúsa betri yfirsýn yfir stöðu staðsetninganna í vöruhúsinu. Þau bjóða einnig upp á háþróaðri skýrslugerð og síun.

## <a name="set-up-item-consolidation-and-location-utilization"></a>Setja upp vörusameiningu og nýtingu staðsetningar

Þessi hluti lýsir því hvernig á að búa kerfið undir að nota vörusameiningu og nýtingu staðsetningar. Aðferðirnar nota sýnigildi úr stöðluðu sýnigögnunum. Ef ætlunin er að fara í gegnum dæmið sem boðið er upp á síðar í þessari grein, skal velja lögaðilann **USMF** (sem inniheldur stöðluðu sýnigögnin) og búa til hverja færslu sem er lýst í þessari grein. Ef ætlunin er ekki að fara í gegnum dæmið, er hægt að líta á gildin sem boðið er upp á hér sem dæmi um gerð uppsetningar sem þarf að ljúka til að geta notað eiginleikana.

### <a name="released-product"></a>Útgefin afurð

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Í svæðið **Vörunúmer** skaltu velja *M9201* og opna upplýsingasíðuna.
1. Á Aðgerðasvæði, á flipanum **Stjórna birgðum**, í flokknum **Vöruhús**, velurðu **Efnislegar víddir**.
1. Á síðunni **Efnisleg vídd**, á aðgerðasvæðinu, skal velja **Nýr**.

    Nýrri línu er bætt við hnitanetið. Reiturinn **Vörunúmeri** er forstilltur.

1. Í reitnum **Eining** skal velja *ea*. Eftirstandandi reitir í línunni eru sjálfkrafa stilltir.
1. Veljið **Vista** og lokið skjámyndinni.

### <a name="location-profile"></a>Forstillingar staðsetningar

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Forstillingar staðsetningar**.
1. Veldu **FLOOR-05** á lista staðsetningarforstillinga.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Í flýtiflipanum **Almennt** skal ganga úr skugga um að báðir eftirfarandi valkostir séu stilltir á *Já*:

    - Virkja vöru á staðsetningu
    - Virkja staðsetningarstöðu

1. Veljið **Vista**.

    > [!IMPORTANT]
    > Ef valkostirnir **Virkja vöru á staðsetningu** og **Virkja staðsetningarstöðu** voru þegar stilltir á *Já* skal hoppa yfir í leiðbeiningarnar um uppsetningu flýtiflipans **Víddir** í skrefi 10. Ef valkostirnir voru ekki þegar stilltir á *Já* þarf að keyra samræmisathugun fyrir eininguna **Vöruhúsastjórnun** þegar búið er að stilla þá handvirkt. Ef þetta er málið skaltu halda áfram í næsta skref.

1. Til að keyra samræmisathugunina skal fara í **Kerfisstjórnun \> Reglubundin verkefni \> Gagnagrunnur \> Samræmisathugun**.
1. Í svarglugganum **Samræmisathugun** skal stilla eftirfarandi gildi:

    - **Eining:** *Vöruhúsakerfi*
    - **Villuleita/laga:** *Villuleita*
    - **Frá dagsetningu:** Hafðu reitinn auðann.
    - **Samræmisathugun fyrir stöðu vöruhúsastaðsetningar:** Veldu þennan gátreit.

1. Veljið **Í lagi**.

    > [!TIP]
    > Þegar samræmisathugun er lokið færðu senda tilkynningu. Opnið [Aðgerðamiðstöð](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications) til að skoða skilaboðin. Smelltu á **Upplýsingar um skilaboð** til að skoða upplýsingarnar.
    >
    > Ef skilaboðin fyrir samræmisathugun segja: „Rangar upplýsingar um stöðu staðsetningar fannst fyrir staðsetningu XXXX í vöruhúsi XX,“ þarf að keyra samræmisathugunina aftur. Að þessu sinni skal stilla reitinn **Athuga/Laga** á *Laga villu*. Skoða skilaboðin til að ganga úr skugga um að engar villur hafi fundist.

1. Nú þarf að ljúka uppsetningu staðsetningarforstillingar. Farið í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Staðsetningarforstillingar**, veljið staðsetningarforstillingu **FLOOR-05** og síðan, á aðgerðasvæðinu, skal velja **Breyta**.
1. Stilltu eftirfarandi gildi á **Víddir** flipanum:

    - **Hlutfallsleg nýting magns:** *100*
    - **Rúmmálsaðferð sem notuð er við birgðastaðsetningu:** *Nota rúmmál staðsetningar*
    - **Raunveruleg hæð staðsetningar:** *10*
    - **Raunveruleg breidd staðsetningar:** *10*
    - **Raunveruleg dýpt staðsetningar:** *10*
    - **Hámarksþyngd:** *100*

1. Veljið **Vista**.

### <a name="mobile-device-menu-items"></a>Valmyndaratriði fartækis

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.
1. Á aðgerðasvæðinu skal velja **Nýtt** til að stofna nýtt valmyndaratriði fyrir flokkun.
1. Stilla eftirfarandi gildi í hausnum:

    - **Nafn valmyndaratriðis:** *Magnleiðréttingar í*
    - **Titill:** *Breyta í*
    - **Máti:** *Vinna*
    - **Nota fyrirliggjandi vinnu:** *Nei*

1. Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:

    - **Ferli verkstofnunar:** *Magnleiðréttingar í*
    - **Gerðir leiðréttinga á birgðaskrá:** *Leiðréttingar í*

1. Veljið **Vista**.

### <a name="mobile-device-menu"></a>Valmynd fartækis

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmynd fartækis**.
1. Veldu **Birgðir** á valmyndinni.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Á listanum **Tiltækar valmyndir og valmyndaratriði** skaltu finna og velja valmyndaratriðið **Leiðréttingar í**.
1. Smellið á hægri örvarhnappinn til að færa **Leiðréttingar í** yfir á listann **Valmyndarskipan**. Á þennan hátt bætirðu nýju valmyndaratriði við valda valmynd.
1. Veljið **Vista**.

### <a name="movement-types"></a>Hreyfingargerðir

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Birgðir \> Hreyfingagerðir**.
1. Veldu **Nýtt** á aðgerðasvæðinu og stilltu svo eftirfarandi gildi:

    - **Kóði hreyfingargerðar:** *SAMEINA*
    - **Lýsing:** *Sameina staðsetningar*
    - **Auðkenni vinnuklasa:** *InvMov*

1. Veljið **Vista**.

## <a name="example-scenario"></a>Dæmi

Eftirfarandi aðstæður notar farsímaforrit vöruhúsakerfis til að gera *leiðréttingu á* birgðum á tveimur staðsetningum í vöruhúsinu.

### <a name="add-inventory-to-locations"></a>Bæta birgðum við staðsetningar

1. Skráðu þig inn í fartækið sem notandi sem er settur upp fyrir í vöruhús *51*.
1. Farið í **Birgðir \> Leiðrétta á**.

    Nú verður fyrsta leiðrétting staðsetningar færð inn.

1. Í verkinu **Leiðrétting á** skal velja staðsetninguna þar sem gera á birgðaleiðréttinguna. Í reitnum **LOC** skal velja *LP-001*.
1. Staðfesta staðsetninguna.
1. Sláðu inn kenni númeraplötu fyrir vöruna sem verður bætt við staðsetninguna. Í reitinn **LP** skal slá inn *LP00101*.
1. Staðfesta númeraplötu.
1. Sláðu inn magn af vörunni sem verður bætt við númeraplötuna. Í reitinn **ITEM** skal færa inn *M9201*.
1. Staðfesta atriði.
1. Sláðu inn magn af vörunni sem verður bætt við. Í reitinn **Magn** skaltu slá inn *10*.
1. Staðfestu magnið.

    Skilaboðin „Vinnu er lokið“ birtast. Nú verður önnur leiðrétting staðsetningar færð inn.

1. Í verkinu **Leiðrétting á** skal velja staðsetninguna þar sem gera á birgðaleiðréttinguna. Í reitinn **LOC** skal velja *LP-002*.
1. Staðfesta staðsetninguna.
1. Sláðu inn kenni númeraplötu fyrir vöruna sem verður bætt við staðsetninguna. Í reitinn **LP** skal slá inn *LP00201*.
1. Staðfesta númeraplötu.
1. Sláðu inn magn af vörunni sem verður bætt við númeraplötuna. Í reitinn **ITEM** skal færa inn *M9201*.
1. Staðfesta atriði.
1. Sláðu inn magn af vörunni sem verður bætt við. Í reitinn **Magn** skaltu slá inn *15*.
1. Staðfestu magnið.

    Skilaboðin „Vinnu er lokið“ birtast.

1. Veldu valmyndarhnappinn (stundum kallaður hamborgari eða hamborgarahnappur) og veldu síðan **Hætta við** til að loka verkinu **Leiðréttingar í**.

### <a name="consolidate-locations"></a>Sameina staðsetningar

1. Farið í **Vöruhúsakerfi \> Reglubundin verk \> Sameining vöru**.
1. Í hausnum skal velja vöruhús þar sem gera á sameininguna. Í reitinn **Vöruhús** skal slá inn *51*.

    Færsla er sýnd fyrir hverja staðsetningu þar sem vara *M9201* var leiðrétt. Dálkurinn **Nýtingarprósenta** sýnir rúmmálsnýtingu hverrar staðsetningar.

1. Til að sameina birgðir skal velja allar sendingar sem á að sameina og síðan, á aðgerðasvæðinu, velja **Sameina birgðir**.
1. Í svarglugganum **Sameina birgðir** skal tilgreina staðsetninguna og hreyfingargerðina sem nota á til að búa til vinnu fyrir birgðahreyfingu. Stilla eftirfarandi gildi:

    - **Staðsetning:** *LP-001*
    - **Kóði hreyfingargerðar:** *SAMEINA*

1. Veljið **Í lagi**.
1. Þú færð upplýsingaboð sem sýna hreyfingarvinnu sem var búin til. Skráið niður kenni hreyfingarvinnu.

### <a name="view-movement-work"></a>Skoða hreyfingarvinnu

1. Opnaðu **Vöruhúsastjórnun \> Vinna \> Upplýsingar um vinnu**.
1. Skoða vinnuna sem var búin til. Notið vinnukenni hreyfingar úr birgðasameiningunni til að sía eða leita í hnitaneti vinnu.

    Í þessu dæmi var staðsetning sem hafði birgðir notuð sem samstæðustaðsetning birgða. Því er aðeins eitt vinnuauðkennið stofnað.

    > [!NOTE]
   > Kerfið býr til eitt vinnuauðkenni fyrir hvern flutning sem þarf að ljúka. Ef staðsetning sem inniheldur þegar birgðir er tilgreind er aðeins eitt vinnuauðkennið stofnað. Ef ný staðsetning er tilgreind eru tvö vinnuauðkenni stofnuð.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
