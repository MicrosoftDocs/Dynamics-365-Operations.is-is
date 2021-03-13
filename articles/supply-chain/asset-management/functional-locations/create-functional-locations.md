---
title: Stofna virkar staðsetningar
description: Þetta efni útskýrir hvernig á að stofna virka staðsetningu í eignastjórnun.
author: josaw1
manager: tfehr
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationCopyStructure, EntAssetFunctionalLocationCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 81b5b81d7c318ba0a195dbc6324d700ccb8d39bf
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018222"
---
# <a name="create-functional-locations"></a>Stofna virkar staðsetningar

[!include [banner](../../includes/banner.md)]

 

Þetta efni útskýrir hvernig á að stofna virka staðsetningu í eignastjórnun.

Þegar þú býrð til virkt staðsetningarskipulag þarftu að hafa í huga að þegar þú hefur búið til virka staðsetningu getur þú ekki fært hana af upprunalegum stað. Það þýðir að þú ættir að huga vel að uppbyggingu virkra staðsetninga áður en þú byrjar að stofna þær í eignastjórnun. Ef þú sérð eftir virkri staðsetningu geturðu eytt henni að því tilskildu að hún hafi ekki enn verið tekið í notkun.

Til að geta unnið með virkar staðsetningar byrjarðu með því að búa til tvo „flokka“ virkra staðsetninga:

- Stofnaðu *eina* sjálfgefna virka staðsetningu án undirstaðsetninga. Þessi virka staðsetning er aðeins notuð sem staðsetning fyrir eignir þegar þú stofnar nýjar eignir.  
- Stofnaðu uppbyggingu virkrar staðsetningar sem þarf til að stjórna viðhaldsverkum í fyrirtækinu þínu.

## <a name="create-a-default-functional-location"></a>Stofna sjálfgefna virka staðsetningu

Þegar þú notar virkar staðsetningar skaltu byrja með því að stofna eina sjálfgefna staðsetningu til að nota við stofnun nýrra eigna. Þessi virka staðsetning er sú sem var valin í tenglinum **Eignastýring** > **Uppsetning** > **Færibreytur eignastýringar** > **Eignir** > reitnum **Sjálfgefin virk staðsetning**. Hægt er að nota sjálfgefna virka staðsetningu við stofnun nýrra eigna og þegar þú hefur ekki enn sett upp skipulag virkrar staðsetningar fyrir þessar eignir.

1. Veldu **Eignastýring** > **Sameiginlegt** > **Virkar staðsetningar** > **Allar virkar staðsetningar**.  
2. Í **Allar virkar staðsetningar** velurðu **Nýtt**.
3. Settu inn auðkenni í retinum **Virk staðsetning**, til dæmis „0000“ eða „Sjálfgefið“, til að gefa til kynna að þetta sé sérstök virk staðsetning.
4. Í reitnum **Heiti** slærðu inn heiti fyrir sjálfgefna virka staðsetningu.
5. Veldu *ekki* yfireiningu í reitnum **Yfireining** - láttu þennan reit vera auðan.
6. Í reitnum **Gerð virkrar staðsetningar** velurðu þá gerð virkrar staðsetningar sem á að nota fyrir sjálfgefna virka staðsetningu. Sjá [Gerðir virkra staðsetninga](../setup-for-functional-locations/functional-location-types.md) fyrir frekari upplýsingar um hvernig á að setja upp gerðir virkra staðsetninga.
7. Veljið **Í lagi**. Þú ættir ekki að bæta frekari gögnum við þessa virku staðsetningu þar sem þau eru aðeins notuð sem tímabundin staðsetning fyrir nýjar eignir þar til þú setur upp eignirnar á virkum stöðum sem fyrirtækið þitt notar.

## <a name="create-functional-locations"></a>Stofna virkar staðsetningar

Eftirfarandi ferli lýsir því hvernig þú stofnar virkar staðsetningar sem þarf til viðhaldsstjórnunar hjá fyrirtækinu þínu.

1. Veldu **Eignastýring** > **Sameiginlegt** > **Virkar staðsetningar** > **Allar virkar staðsetningar**. Þú getur stofnað virka staðsetningu úr töfluskoðun eða smáatriðum.
2. Veldu hnappinn **Nýtt**.
3. Settu inn auðkenni í reitnum **Virk staðsetning**.
4. Í reitnum **Heiti** slærðu inn heiti fyrir virka staðsetningu.
5. Ef virka staðsetningin er undirstaðsetning í skipulagi skaltu velja yfirstaðsetningu í reitnum **Yfireining**.
6. Veldu tegund í reitnum **Gerð virkrar staðsetningar**.
7. Veljið **Í lagi**.
8. Veldu virka staðsetningu og smelltu á **Breyta** til að bæta við frekari upplýsingum.

>[!NOTE]
>Það fer eftir uppsetningu þinni á líftímastöðum virkra staðsetninga, en þú gætir þurft að stofna allar undirstaðsetningar fyrir virka staðsetningu og síðan breyta líftímastöðu virkrar staðsetningar áður en þú getur byrjað að setja upp eignir. Sjá [Setja upp eignir á virkum staðsetningum](../functional-locations/install-objects-on-functional-locations.md) til að fá frekari upplýsingar um uppsetningu eigna. Sjá [Líftímastöður virkra staðsetninga](../setup-for-functional-locations/functional-location-stages.md) til að læra meira um uppsetningu á líftímastöðum virkra staðsetninga.

Í smáatriðum muntu sjá flýtiflipa þar sem þú getur bætt við og breytt upplýsingum um virka staðsetningu.

## <a name="general-information"></a>Almennar upplýsingar

Þessi hluti veitir yfirlit yfir yfir- og undirupplýsingar í skipulagi virkrar staðsetningar. Í hlutanum **Upplýsingar** er hægt að sjá fjölda eignaeiginda, viðhaldsáætlana og eigna sem tengjast virkri staðsetningu. Í hlutanum **Birgðir** er hægt að velja síðuna og vöruhúsið sem virk staðsetning er tengd við. Vefsvæði og vörugeymsla er notað í tengslum við vöruspár um verkbeiðnir. Þegar þú býrð til vöruspá eru upplýsingar um svæði og vöruhús frá virkni staðsetningu eignarinnar sjálfkrafa notaðar. Í hlutanum **Líftímastaða** birtast upplýsingar um líftímastöðu virkrar staðsetningar.

## <a name="installed-assets"></a>Uppsettar eignir

Sjá [Setja upp eignir á virkum staðsetningum](../functional-locations/install-objects-on-functional-locations.md) til að fá frekari upplýsingar um uppsetningu eigna. Þú getur notað hnappinn **Skoða** á þessum flýtiflipa til að sýna fleiri reiti á flýtiflipa. Hægt er að sýna reitina **Gildir frá** og **Undireign** í töflunni.

## <a name="asset-attribute-requirements"></a>Kröfur eignaeiginda

Á þessum flýtiflipa geturðu bætt við sérstökum eigindakröfum fyrir eignirnar sem þú setur upp á virkri staðsetningu. Þessar kröfur eru eingöngu ætlaðar til upplýsinga. Þær koma ekki í veg fyrir að þú setjir upp eignir með öðrum eigindakröfum. Veldu **Bæta við línu** og veldu eigindagerðina. Síðan seturðu inn viðkomandi **Gildi**, velur þröskuld í reitnum **Skilyrði fyrir þröskuld** og vistar skrána.

## <a name="maintenance-plans-and-maintenance-rounds"></a>Viðhaldsáætlanir og viðhaldsumferðir

Hér getur þú bætt viðhaldsáætlunum og viðhaldsumferðum við virka staðsetningu, þar með talið upphafsdagsetningu. Eignir settar upp á virkri staðsetningu geta verið með aðrar viðhaldsáætlanir settar upp. Hægt er að nota allar viðhaldsáætlanir og viðhaldsumferðir við tímasetningu færslna á dagatali eigna fyrir virka staðsetningu og þegar uppsettar eignir.

>[!NOTE]
>Ef þú uppfærir uppsetningu á eignategundum, eignamerkjum og eignalíkönum í viðhaldsáætlunum í smáatriðunum **Allar virkar staðsetningar** > flýtiflipanum **Viðhaldsáætlanir** eftir að þú hefur skipulagt viðhaldsáætlanir, verður núverandi viðhaldsáætlunargögnum sem tengjast þeirri virku staðsetningu sjálfkrafa eytt. Til að stofna nýjar áætlunarfærslur sem samsvara uppfærðri viðhaldsáætlunaruppsetningu á virkri staðsetningu verður þú að keyra nýja viðhaldsáætlun fyrir þá virku staðsetningu. 

## <a name="address"></a>Aðsetur

Settu aðsetur virkrar staðsetningar á flýtiflipanum **Aðsetur**. Aðsetur á virkum staðsetningum eru erfð, sem þýðir að ef undirstaðsetning hefur ekkert aðsetur skilgreint er aðsetur yfirstaðsetningar notað.

## <a name="workers"></a>Starfskraftar

Á þessum flýtflipa geturðu bætt við starfskröftum sem tengjast virkri staðsetningu og þú getur valið virka staðsetningu aðal fyrir starfskraftinn. 

## <a name="attributes"></a>Eiginleikar

Á þessum flýtiflipa geturðu stillt gildi fyrir eigindi virkrar staðsetningar. Hægt er að nota þessa eiginleika til að lýsa eiginleikum eða einkennum sem tengjast virkri staðsetningu, til dæmis burðarvirki, byggingartegund, svæðislýsingum eða staðsetningu fyrir ofan eða undir jörðu.

Veldu **Bæta við línu** og veldu eigindagerðina. Settu næst inn **Gildi** tengt eigindagerðinni og vistaðu skrána.

## <a name="financial-dimensions"></a>Fjárhagsvíddir

Þú getur valið fjárhagsvíddir fyrir virka staðsetningu. [Gerðir virkrar staðsetningar](../setup-for-functional-locations/functional-location-types.md) er hægt að setja upp til að gera kleift að gera sjálfvirka uppfærslu á fjárhagsvíddum frá virkum stað. Það þýðir að eignir settar upp á fjárhagslegri vídd fá sjálfkrafa fjárhagsvíddir fyrir virka staðsetningu. Það er gagnlegt ef þú vilt hafa mismunandi kostnaðarmiðstöðvar, allt eftir staðsetningu.

Þegar gögn varðandi **Svæði**, **Vöruhús**, **Heimilisfang** og **Fjárhagslegar víddir** eru uppfærð á virkri yfirstaðsetningu, þá er hægt að uppfæra tengdar undirstaðsetningar í samræmi við það ef þú tekur það val meðan á uppfærslunni stendur. Gluggi opnast og gefur þér uppfærsluvalkostina.

## <a name="copy-a-functional-location-structure"></a>Afritaðu skipulag virkrar staðsetningar

Ef fyrirtæki þitt er með nokkrar virkar staðsetningar með svipað staðsetningarskipulag geturðu notað afritunaraðgerðina í Eignastjórnun til að búa til fljótt fjölda svipaðra staðsetningarstigvelda. Þegar þú afritar tiltekna virka staðsetningu eða heilt skipulag hefur nýja staðsetningin eða uppbyggingin sama nafn og það sem þú afritaðir. Eftir að afritunarferlið er lokið geturðu auðveldlega breytt nafni eða öðrum stillingum á nýju virku staðsetningunni, að því tilskildu að sú líftímastaða virkrar staðsetningar sem var valin fyrir nýju virku staðsetninguna leyfir það.

1. Í **Allar virkar staðsetningar** velurðu virku staðsetninguna sem þú vilt afrita. Til dæmis velurðu efstu staðsetningu (yfireiningu) ef þú vilt afrita allt skipulag virkar staðsetningar ásamt undirstaðsetningum.
2. Veldu hnappinn **Afrita skipulag virkrar staðsetningar**. Staðsetningin sem þú valdir á listasíðunni er sýnd í reitnum **Afrita frá**.
3. Settu nafn nýrrar staðsetningar inn í reitnum **Ný virk staðsetning**.
4. Í reitnum **Yfireining til að líma undir** þá ættir þú aðeins að setja inn yfirauðkenni ef staðsetningin sem þú ert að stofna ætti að vera hluti af fyrirliggjandi skipulagi virkrar staðsetningar.
5. Smellt er á **OK**. Nýtt skipulag virkrar staðsetningar er sýnt í **Allar virkar staðsetningar**.

>[!NOTE]
>Þegar þú afritar skipulag virkrar staðsetningar eru líftímastöður virkrar staðsetningar í nýja skipulaginu stilltar á „fyrsta stöðu“ sem þú hefur stofnað fyrir virkar staðsetningar. Hvort sem þú getur endurnefnt eða eytt virkri staðsetningu með því að nota hnappana **Endurnefna** og **Eyða** í **Allar virkar staðsetningar** fer eftir núverandi líftímastöðu virkrar staðsetningar.

## <a name="delete-a-functional-location"></a>Eyða virkri staðsetningu

Hægt er að eyða virkri staðsetningu með tengdum undirstöðum ef engar eignir hafa verið settar upp á neinum af þeim virku staðsetningum sem þú ert að reyna að eyða og ef núverandi líftímastaða virkrar staðsetningar leyfir það.

1. Í **Allar virkar staðsetningar** velurðu virku staðsetninguna sem þú vilt eyða.
2. Ef þörf krefur skaltu uppfæra virka staðsetningu í líftímastöðu virkrar staðsetningar sem gerir kleift að eyða virkri staðsetningu.
3. Veljið **Eyða**.

>[!NOTE]
>Ef þú getur ekki eytt virkri staðsetningu geturðu í staðinn séð um eyðingu með því að setja upp líftímastöðu virkrar staðsetningar í þessum tilgangi. Til dæmis er hægt að setja upp „rusl“ eða „eytt“, sem ætti ekki að vera virkt stig, í forminu **Líftímastöður virkra staðsetninga**.
