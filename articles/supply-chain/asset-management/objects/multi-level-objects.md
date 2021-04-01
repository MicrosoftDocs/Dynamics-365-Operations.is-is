---
title: Stigskiptar eignir
description: Þetta efni útskýrir hvernig á að búa til og eyða eignum í mörgum stigum.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a69fd8b7d81700a62ae96d679372b1d6c8a70bbf
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253207"
---
# <a name="multi-level-assets"></a>Stigskiptar eignir

[!include [banner](../../includes/banner.md)]

 

Þetta efni útskýrir hvernig á að búa til og eyða eignum í mörgum stigum. Þú getur búið til eignir og tengdar undireignir í stigskiptri trjábyggingu. Á þennan hátt geturðu sýnt sambönd og ósjálfstæði meðal eigna. Viðhaldsstörf geta tengst öllum stigum trébyggingarinnar. Einnig er hægt að búa til tölfræði fyrir einstaklingstig eða sem summa af öllum undireignarstigum.

Á listasíðunni **Allar eignir** (**Eignastýring** \> **Sameiginlegt** \> **Eignir** \> **Allar eignir**), sýnir dálkurinn **Eignir** eignir í stigveldi. Dálkurinn **Yfireining** sýnar tengdar yfireiningar. Að auki, ef eignir og undireignir hafa þegar verið stofnaðar sýnir hlutinn **Eignatré** í glugganum **Tengdar upplýsingar** eignirnar í trjábyggingu.

Nánari upplýsingar um hvernig stofna eigi eign, sjá [Stofna eign](../objects/create-an-object.md). Til að búa til undireign skal velja yfireignina í reitnum **Yfireining** á flýtiflipanum **Almennt**.

## <a name="copy-an-asset-or-asset-structure"></a>Afritaðu eign eða uppbyggingu eigna

Ef fyrirtæki þitt hefur nokkra svipaða eignaskipulag geturðu notað afritunaraðgerðina í eignastjórnun til að búa þau fljótt til.

1. Veldu **Eignastýring** \> **Sameiginlegt** \> **Eignir** \> **Allar eignir**.
2. Á listasíðunni **Allar eignir**, veldu eignina sem á að afrita. Til dæmis, ef þú vilt afrita alla eignaskipulagið, þar á meðal undireignir, skaltu velja yfireign.
3. Veldu **Afrita eign**. Í hlutanum **Afrita frá** er reiturinn **Eignir** stilltur á eignina sem þú valdir á listasíðunni.
4. Í hlutanum **Afrita í** í reitnum **Eignir** slærðu inn nafn nýju eignarinnar.
5. Ef eignin sem þú ert að búa til ætti að vera hluti af núverandi eignaskipan, skaltu velja fyrirkenni í hlutanum **Yfireign** í retinum **Eignir**.
6. Veljið **Í lagi**. Nýja eignaskipan er sýnd á **Allar eignir** listasíðu. Allir eignareiginleikar, viðhaldsáætlanir og viðhaldsumferðir sem tengjast eigninni sem þú afritaðir eru fluttar yfir í nýju eignina eða eignaskipan.

Þegar þú afritar eignaskipulag hafa undireignirnar í nýju skipulaginu sama nafn og undireignirnar sem þú afritaðir. Eftir að afritunarferlinu er lokið geturðu auðveldlega breytt nafni og öðrum stillingum fyrir eign. Veldu eignina á listasíðunni **Allar eignir** og veldu síðan hnappinn **Breyta**.

> [!NOTE]
> Þegar þú afritar eign eða eignaskipulag er líftíma hinna nýju eigna endurstillt í það ástand sem þú skilgreindir sem upphafsástand lífsins fyrir eignir. Virka staðsetningin er núllstillt á sjálfgefna virka staðsetningu.

## <a name="delete-an-asset-or-asset-structure"></a>Eyða eign eða uppbyggingu eigna

Ef eign hefur tengdar undireignir geturðu eingöngu eytt henni ef engar viðhaldsbeiðnir, verkbeiðnastörf, bilunarskráningar eða ástandsmat eru skráð á einhverja af eignunum.

1. Á listasíðunni **Allar eignir**, veldu eignina sem á að eyða.
2. Veljið **Eyða**.

> [!NOTE]
> Ef þú getur ekki eytt eign með því að nota þessa aðferð, er önnur leið til að takast á við eyðingu að setja upp eignatíma í þessu skyni. Til dæmis er hægt að setja upp líftímastöðuna **Hent** eða **Eytt** á síðunni **Líftímastaða eigna**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]