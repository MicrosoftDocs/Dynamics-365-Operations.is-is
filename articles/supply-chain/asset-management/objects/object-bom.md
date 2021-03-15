---
title: Eignauppskriftir
description: Þetta efni lýsir eignauppskriftum (BOMs) í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetStandardSparePartsItemGroup, EntAssetObjectBOM
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: baaf516eb386c3cf63d72bf31800b8731121fe26
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019523"
---
# <a name="asset-boms"></a>Eignauppskriftir

[!include [banner](../../includes/banner.md)]

 

Þetta efni lýsir eignauppskriftum (BOMs) í eignastýringu. Síðan **Uppskrift eignar** sýnir lista yfir alla hluti (varahluti og aðra hluti) sem eru notaðir á eign alla sína ævi. Þegar þú býrð til nýja eign, ættir þú að íhuga að setja upp uppskrift eignar sem hluta af uppsetningarferlinu. Á þennan hátt getur þú fylgst með sögu sögu eignarinnar frá stofnunardegi.

Eftir að þú hefur lokið viðhaldsstörfum og neysla á hlutum hefur verið skráð í vinnupöntun geturðu fylgst með neyslu varahluta og annarra hluta sem eru notaðir á eignina. Þessi virkni gerir þér kleift að halda fullkomna neysluskrá hluta fyrir allar eignir þínar. Til dæmis er hægt að nota skrána til að fylgjast með því hvort skipt er um ákveðinn varahlut eða oft til að fylgjast með varahlutunum eða öðrum hlutum sem nú eru notaðir á eign.

> [!NOTE]
> Í verkbeiðni gæti neysla á vöru bæði verið varahlutir og aðrir hlutir til viðbótar, svo sem smurefni, boltar og þéttingar.

Hægt er að uppfæra uppskrift eignar sjálfkrafa út frá uppsetningunni í eignastjórnun. Ef búið er að búa til líftímastöðu verkbeiðni til að meðhöndla fullgerðar eða fullgerðar verkbeiðnir, og ef **Uppfæra uppskrift eignar** valkostur fyrir þá líftímastöðu verkbeiðni er stilltur á **Já** á síðunni **Líftímastöður verkbeiðna** verða allir hlutir sem eru notaðir í vinnupöntuninni sjálfkrafa uppfærðir á **Eignastýringarkerfi** síðu þegar verkbeiðnin er uppfærð í þá líftímastöðu. 


Þú getur einnig uppfært uppskrift eignar handvirkt með því að búa til nýjar vörulínur á **Eignastýringarkerfi** síðu.

Á síðunni **Uppskrift eignar** geturðu fylgst með sögu um varahluti fyrir eignir eftir að neysla hlutar er skráð í verkbeiðni. Til að nota þessa virkni verður þú að velja þá vöruhópa sem nota ætti til varahlutaskráningar á síðunni **Hlutahópar varahluta**.

Til að nota virkni uppskrifta eigna verður þú fyrst að setja upp nauðsynlega hópa varahluta. Síðan, ef þú vilt að uppskrift eigna verði uppfærð sjálfkrafa þegar verkbeiðni er lokið, geturðu sett upp lítímastöðu verkbeiðni til að vinna með þá uppfærslu. 


## <a name="set-up-spare-parts-item-groups"></a>Setja upp vöruflokka varahluta

Uppsetning sögu varahluta er byggð á vöruflokkum sem eru búnir til í einingunni **Birgðir og vöruhúsastjórnun**. Í eignastjórnun seturðu upp vöruflokka þannig að þú getur fylgst með varahlutasögu fyrir hlutina í völdum vöruflokkum.

1. Veldu **Eignastýring** \> **Uppsetning** \> **Eignir** \> **Varahlutir hlutahópar**.
2. Veldu **Nýtt** til að setja upp hlutahóp.
3. Veldu hópinn í reitnum **Vöruhópur**. Nafn hópsins er fært sjálfkrafa inn í reitinn **Heiti**.

## <a name="view-and-update-asset-boms"></a>Skoða og uppfæra uppskriftir eignar

Eftir að þú hefur sent vöruneyslu í verkbeiðni geturðu skoðað skráða neyslu hlutar á síðunni **Uppskrift eignar**.

1. Veldu **Eignastýring** \> **Sameiginlegt** \> **Eignir** \> **Virkar eignir**. Veldu eignina á listanum og veldu síðan **Uppskrift eignar**.

    > [!NOTE]
    > Veldu til að skoða allar neysluvörur skráningar á allar eignir **Eignastýring** \> **Fyrirspurnir** \> **Eignir** \> **Uppskrift eignar**.

2. Veldu **Uppfæra uppskrift eignar**. Þú getur bætt eignum, eignategundum og tilföngum við uppfærsluna eins og þú þarfnast með því að velja **Veldu**. Veldu **Í lagi** til að hefja uppfærsluna. Þú getur einnig sett upp uppfærsluaðgerðina sem runuvinnslu.
3. Ef þú vilt sjá frekari upplýsingar sem tengjast hlutunum geturðu bætt við birgðavíddum. Veldu **Birgðir** \> **Birting vídda** og veldu síðan gátreitina fyrir víddirnar sem þú vilt sjá. Til að halda þessari uppsetningu fyrir allar eignir á síðunni **Uppskrift eignar** stillirðu valkostinn **Vista uppsetningu** á **Já**.
4. Til að fá yfirlit yfir hvar í eignastýringu hluturinn á völdum línum er notaður, í tengslum við eignir, vanskil starfstegunda, varahluti og verkbeiðnir, veldu **Hlutur þar sem hann er notaður**. 
5. Ef þú vilt sjá aðeins virka hlutalínur, veldu **Skoða** \> **Núverandi**. Veldu til að sjá allar vörulínur, þar með talið línur þar sem gildistími er eldri en núverandi dagsetning **Skoða** \> **Allt**.

> [!NOTE]
> Þegar þú hefur lokið verkbeiðni, ef einhverjir hlutir eða varahlutir sem tengjast skyldri eign hafa runnið út eða skipt út fyrir aðra hluti eða varahluti, mælum við með að þú uppfærir uppskrift eignar til samræmis.

## <a name="create-a-new-item-line-in-an-asset-bom"></a>Búðu til nýja hlutalínu í uppskrift eignar

Þú getur búið til hlutalínur handa eignum handvirkt.

1. Á síðunni **Uppskrift eignar** skal velja **Nýr**.
2. Í **Eignir** reitinn, veldu eignina sem á að bæta við hlutalínu fyrir.
3. Í reitinn **Línunúmer** skal slá inn raðlínunúmer.
4. Í reitnum **Árangursrík** slærðu inn upphafsdagsetningu fyrir vöru.
5. Ef hluturinn rennur út, í **Fyrning** reitinn, sláðu inn lokadagsetningu.
6. Veldu vöru í reitnum **Vörunúmer**. Nafn hópsins er fært sjálfkrafa inn í reitinn **Heiti afurðar**.
7. Inn í reitinn **Magn** skal slá inn magnið sem er notað. Reiturinn **Eining** er sjálfkrafa uppfært.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]