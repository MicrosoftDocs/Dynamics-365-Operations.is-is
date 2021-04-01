---
title: Stofna eign
description: Þetta efni lýsir því hvernig á að stofna eign í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectTableCopyStructure, EntAssetObjectTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a01c1fd72b96bd6ff5e6c76e659394e17060c681
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253399"
---
# <a name="create-an-asset"></a>Stofna eign

[!include [banner](../../includes/banner.md)]

 

Þetta efni lýsir því hvernig á að stofna eign í eignastýringu.

1. Smelltu á **Eignastýring** > **Sameiginlegt** > **Eignir** > **Allar eignir** eða **Virkar eignir**.
2. Smellið á hnappinn **Nýtt**.
3. Í svarglugganum **Stofna eignir** seturðu inn gögn varðandi **Eignir** (eignakenni) og eignaheiti. Veldu dagsetningu og -tíma eignar í reitnum **Virkt**. Frá þeim degi geturðu sett eignina upp á virkri staðsetningu sem og flutt og skipt um eignina í eignaskipan.
4. Í reitnum **Eignagerð** velurðu eignagerð fyrir eignina (skyldureitur). Ef með þarf skaltu velja **Eignaframleiðandi** og **Eignalíkan** fyrir eignina. Ef aðeins ein vara hefur verið sett upp er sú vara sjálfkrafa valin í reitnum **Eignaframleiðandi**. Valið sem er í boði í reitunum **Eignaframleiðandi** og **Eignalíkan** er háð uppsetningunni í [Eignaframleiðendur og líkön](../setup-for-objects/product-and-model.md).
5. Í hópnum **Yfireign** er reiturinn **Eignir** sjálfgefið auður. Ef þess er krafist geturðu valið yfireign og þá verða allir reitir í hópnum **Yfireign** sjálfkrafa fylltir út.
    >[!NOTE]  
    >Þegar þú velur yfireign eru tveir eða þrír flipar tiltækir: Flipinn **Mínar eignir** inniheldur eignir sem tengjast virkum staðsetningum sem þú (viðhaldsstarfsmaðurinn sem er skráður inn í kerfið) getur fengið úthlutað. Ef engar virkar staðsetningar eru settar upp á viðhaldsstarfsmanni í forminu [Viðhaldsstarfsmenn og starfsmannahópar](../setup-for-objects/workers-and-worker-groups.md) verður flipinn **Mínar eignir** ekki sýnilegur. Flipinn **Virkar eignir** hefur að geyma lista yfir allar eignir með eignalíftímastöðuna „Virkt“. Flipinn **Eignayfirlit** sýnir trjáyfirlit yfir virkar staðseningar og eignir sem eru settar upp á þessum stöðum.

6. Mælt er með virkri staðsetningu sem þú hefur sett upp fyrir eignina í hópnum **Eignir** > reitnum **Virk staðsetning**. Veldu aðra virka staðsetningu, ef þess er krafist.

    >[!NOTE]
    >Þegar þú hefur stofnað eign geturðu sett hana upp á annarri virkri staðsetningu, ef þess er krafist. Aðeins efstu eignir (eignir án núverandi yfireignar) er hægt að setja upp á virkri staðsetningu. Þetta þýðir að þú setur upp efsta stigið sem og allar undireignir á valinni virkri staðsetningu. Lestu meira um uppsetningu eigna á virkum staðsetningum í [Kynning á virkum staðsetningum](../functional-locations/introduction-to-functional-locations.md).

7. Smellt er á **OK**.
8. Veldu eignina í listanum **Allar eignir** og smelltu á hnappinn **Breyta** til að bæta frekari upplýsingum við eignina.

## <a name="general-information"></a>Almennar upplýsingar

Virka staðsetningin sem eignin tengist er sýnd í reitnum **Virk staðsetning**. Ef eignin er yfireign er fjöldi undireigna sem tengist eigninni sýndur í reitnum **Undirstig**. Ef eignin er undireign fyrirliggjandi eignar er kenni yfireignarinnar sýnt í reitnum **Yfirstig**.

Þú getur breytt upplýsingum um **Eignaframleiðanda** og **Eignalíkan** um eignina, sem eru notaðar til að stjórna varahlutum, varahlutum og vanskilum í starfi. Vísa til [Eignaframleiðendur og líkön](../setup-for-objects/product-and-model.md) fyrir meiri upplýsingar. Þú getur líka bætt við upplýsingum um **Árgerð** og **Raðnúmer**, ef nauðsyn krefur.

**Núverandi líftímastaða** er notuð til að skilgreina hvort eignin sé virk eða óvirk. Þegar þú stofnar eign er stigið alltaf stillt á fyrsta stigið í eignastigahópnum. Þegar þú ert tilbúin/n til að virkja eign skaltu smella á **Uppfæra eignastöðu** og velja þá líftímastöðu sem þú hefur skilgreint sem „eignavirka“ og smelltu á **Í lagi**.

**Athugasemd:** Þegar eign er stillt á „óvirk“ er ekki lengur hægt að búa til verkbeiðnir fyrir eignina. Þú getur heldur ekki tímasett forvarnarviðhaldsverk fyrir óvirka eign.

Reitirnir **Þjónustustig** og **Gagnrýni** tengjast verkbeiðnum sem eru stofnaðar fyrir eignina. Reitirnir sýna tölurnar **Þjónustustig** og **Markástand** reiknaðar fyrir núverandi uppsetningu eignarinnar. Vísa til [Þjónustustig](../setup-for-objects/object-priorities.md) og [Markástandgerðir eigna](../setup-for-objects/object-criticalities.md) varðandi uppsetningu þessara gilda.

## <a name="asset"></a>Eign

Þú getur valið **Tilföng** fyrir eignina. Tilfangavalið ákvarðar hvaða dagatal er notað við tímasetningu verkbeiðna. Tilfangaval er oft notað fyrir eignir. Tilföng og tilfangahópar sett upp í **Fyrirtækisstjórnun** > **Tilföngum** > **Tilfangahópum** eða **Tilföngum**.

Í reitnum **Fjöldi eigna** er hægt að velja eign sem á að tengjast eigninni. Þetta skiptir máli ef eign þín er tengd fjárfestingarverkefni.

- Ef eignin er tengd fastafjármunum geturðu búið til gerð vinnupöntunar sem á að nota fyrir vinnupantanir sem tengjast fjárfestingarverkefni. 
- Upplýsingar um fastafjármuni fyrir eign eru tengdar einingunni **Fastafjármunir** í Dynamics 365 Supply Chain Management. Þetta þýðir að í **Fastafjármuni** > **Fastafjármunir** > **Fastafjármunir** geturðu fengið yfirlit yfir eignastýringarverkefnin sem kunna að tengjast fastafjármunum með því að velja eignina á listanum og skoða innihaldið á rúðunni **Tengdar upplýsingar** > hlutanum **Tilheyrandi verkefni**.


## <a name="details"></a>Upplýsingar

Í reitnum **Virkt frá** er dagsetningin sem þú uppfærðir líftímastöðu eignarinnar í virkt ástand (sjá [Lífsferilstöður eigna](../setup-for-objects/object-stages.md) varðandi uppsetningu á líftímastöðum eigna) sýnd. Ef eignin er ekki lengur virk og þú hefur uppfært líftímastöðu eignarinnar í óvirkt ástand, birtist dagsetningin sem eignin er óvirk frá í reitnum **Virkt til**. Ef þörf krefur er hægt að breyta þessum dagsetningum handvirkt.

Ef þess er krafist, getur þú sett áætlaðan dag fyrir skipti á eigninni í reitnum **Dagsetning endurnýjunar**. Hægt er að setja áætlað verðmæti til að skipta um eignina í reitinn **Endurnýjunargildi**. Dæmi: Þú getur notað endurnýjunarupplýsingar til að bera þær saman við kostnað við að viðhalda eign og taka ákvörðun í kjölfarið um að kaupa nýja eign ef viðhaldskostnaður á núverandi eign eykst hratt.

## <a name="notes"></a>Athugasemdir

Þú getur bætt við athugasemdum sem tengjast eigninni á flýtiflipanum **Athugasemdir**. Smelltu á hnappinn **Bæta tímastimpli við** áður en þú skrifar minnispunktinn, ef þú vilt bæta notendaupplýsingum og dagsetningu/tímastimpli við athugasemdina.

## <a name="attributes"></a>Eiginleikar

Á þessum flýtiflipa geturðu stillt gildi fyrir eignareigindi. Hægt er að nota þessar eigindir til að lýsa eiginleikum eða eiginleikum sem tengjast eigninni, til dæmis stærð, þyngd eða vélarstillingu.

Smelltu á **Bæta við línu** og veldu eigindagerðina. Settu næst inn **Gildi** tengt eigindagerðinni og vistaðu skrána.

>[!NOTE] 
>Þú getur fengið yfirlit yfir eigindagerðir eigna og tengsl þeirra við eignir í **Eigind eignar** og **Yfirlit yfir eignaeigindir**. Sjá [Yfirlit eignaeiginda](../objects/object-specification-overview.md) fyrir meiri upplýsingar.

## <a name="vendor"></a>Lánardrottinn

Á flýtiflipanum **Lánardrottinn** velurðu lánardrottnalykil fyrir eignina. Einnig, ef ábyrgð lánardrottins hefur verið veitt, geturðu sett inn upplýsingar um ábyrgð hér.

## <a name="address"></a>Aðsetur

Á flýtiflipanum **Aðsetur** geturðu sett inn vistfang búnaðarins. Ef ekkert aðsetur er sett á eignina notar eignin aðsetur yfireignar ef yfireignin hefur aðsetur. Ef ekkert heimilisfang er tengt eigninni eða yfireiningum í eignastigveldinu er heimilt að nota aðsetur virku staðsetningarinnar sem eignin er sett á. Ef þessi virka staðsetning er ekki með aðsetur sem tengist henni er aðsetur yfireiningar virku staðsetningarinnar notað á eigninni.

## <a name="asset-management-plans"></a>Áætlanir eignastýringar

Viðhaldsáætlanir eru notaðar við tímasetningu forvarnarviðhaldsverka með reglulegu millibili á eigninni. Á þessum flýtiflipa geturðu sett upp viðhaldsáætlunarlínur fyrir valda eign. Hægt er að setja upp viðhaldsumferðir fyrir ýmsar eignir, þar sem þú þarft að framkvæma svipað verk með reglulegu millibili. Á flipanum **Viðhaldsáætlanir virkrar staðsetningar** sérðu viðhaldsáætlanir sem tengjast virkri staðsetningu sem eignin er sett upp á.

>[!NOTE]
>Ef þú eyðir viðhaldsáætlunarlínu eða viðhaldsumferð sem tengist eign í **Allar eignit**, eyðirðu einnig sjálfkrafa öllum viðhaldsáætlunum með stöðunni „Stofnað“ sem hafa verið stofnaðar út frá þeirri viðhaldsáætlun eða viðhaldsumferð.

## <a name="functional-location-maintenance-plans"></a>Viðhaldsáætlanir virkra staðsetninga

Á þessum flýtiflipa færðu yfirlit yfir viðhaldsáætlanir sem tengjat virkri staðsetningu sem eignin er sett upp á.

## <a name="maintenance-rounds"></a>Viðhaldslotur

Á þessum flýtifliupa geturðu bætt við eða fjarlægt viðhaldsumferðir sem tengjast eigninni.

## <a name="financial-dimensions"></a>Fjárhagsvíddir

Þú getur valið fjárhagsvíddir fyrir eignina.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]