---
title: Bæta við nýrri síðu á svæði
description: Þetta efnisatriði lýsir því hvernig á að bæta við nýrri svæðssíðu í Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4b031431499eba0e109ac04dc46ec187250eba694284864bf78bb1f90265d788
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725387"
---
# <a name="add-a-new-site-page"></a>Bæta við nýrri síðu á svæði

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að bæta við nýrri svæðssíðu í Microsoft Dynamics 365 Commerce.

Eftir að þú hefur búið til sniðmát og brot fyrir síðuna þína er næsta skref að byrja að búa til síður sem nota þau. Til að byrja verður þú að velja sniðmát eða skipulag, nafn á síðu og slóð síðu.

## <a name="template-or-layout"></a>Sniðmát eða útlit

Þú getur annaðhvort notað sniðmát eða skipulag fyrir nýju síðuna þína. Frekari upplýsingar eru í [Yfirlit yfir sniðmát og skipulag](templates-layouts-overview.md).

## <a name="page-name"></a>Heiti síðu

Síðuheitið verður að vera einkvæmt fyrir síðuna. Það ætti að vera lýsandi, svo að þú getur auðveldlega fundið það og aðrir vita fyrir hvað síðan stendur. Veldu síðuheitið vandlega, því ekki er hægt að breyta því seinna.

## <a name="page-url"></a>Vefslóð síðu

Þú getur haft þann kost að slá inn slóð fyrir nýju síðuna. Þegar þú býrð til síðu geturðu slegið inn streng sem verður notaður til að mynda heila vefslóð. Þessi strengur er þekktur sem hlutfallsleg slóð eða slóðasnigill. Síðan er stofnuð heil vefslóð byggt á slóðarsniglinum og nýju síðunni er úthlutað á hana. Þú getur breytt slóðarsnigli seinna áður en þú birtir síðuna. Nánari upplýsingar sjá [Stofna vefslóð síðu](create-page-URL.md).

> [!NOTE]
> Dynamics 365 Commerce aftengir slóðir og innihald. Með öðrum orðum er hægt að búa til síðu sem er ekki tengd vefslóð og hægt er að búa til slóð sem er ekki tengd síðu. Þess vegna er hægt að skipta um innihald fyrir slóð og engan niðritíma þarf og því er auðveldara að stjórna framsendingum.

## <a name="add-a-new-page"></a>Bæta við nýrri síðu

Fylgdu þessum skrefum til að bæta við nýrri síðu á síðuna þína.

1. Undir **Svæði** velurðu **Fabrikam** (eða heiti svæðisins).
1. Veljið **Ný síða**.
1. Í svarglugganum **Ný síða** skal velja sniðmát og síðan smella á **Í lagi**.
1. Í reitnum **Heiti síðu** slærðu inn heiti síðunnar (til dæmis, **Nýja síða mín**).
1. Í reitinumm **Vefslóð** slærðu inn streng (slóðarsnigil) til að ljúka slóðinni (t.d. **myndsíða**).
1. Veljið **Í lagi**. Síðuritillinn birtist. Taktu eftir að fyrirsögn og undirmálstexta er sjálfkrafa bætt við síðuna, byggt á sniðmátinu sem þú valdir.
1. Í síðuútlínunum velurðu hólfið **Aðal**, velur úrfellingarhnappinn (**...**) og velur síðan **Bæta við einingu**.
1. Veldu **Gámur** og síðan **Í lagi**.
1. Veldu **Vökvagámur**, veldu úrfellingarhnappinn og veldu síðan **Bæta við einingu**.
1. Veldu **Bálkur með fjölbreyttu efni** og veldu síðan **Í lagi**.
1. Veldu **Bálk með fjölbreyttu efni**, veldu úrfellingarhnappinn og veldu síðan **Bæta við einingu**.
1. Veldu **Bálkaliður með fjölbreyttu efni** og veldu síðan **Í lagi**.
1. Í eiginleikaglugganum til hægri velurðu **Málsgrein** og slærð síðan inn í reitinn **Prufuextinn minn**.
1. Veldu **Vista** og síðan **Ljúka við breytingar**.
1. Í reitnum **Athugasemdir** slærðu inn **Bætti við nýrri síðu** og velur síðan **Í lagi**.
1. Veldu **Forskoðun** til að forskoða síðuna. Þegar þú hefur lokið því skaltu loka forskoðunarflipanum til að fara aftur í höfundatólið.
1. Velja **Birta**.
1. Veldu á leiðsöguslóðina (brauðmylsna) **Fabrikam** (eða nafn vefsvæðisins).
1. Í stýriglugganum vinstra megin velurðu **Vefslóðir**.
1. Finndu og veldu slóðina (**mynewpage**) af listanum.
1. Velja **Birta**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Breyta síðu svæðis sem þegar er til](modify-existing-page.md)

[Velja síðuútlit](select-page-layouts.md)

[Stjórna SEO-lýsigögnum](manage-seo-metadata.md)

[Vista, forskoða og birta síðu](save-preview-publish-page.md)

[Bæta vörusíðu](enrich-product-page.md)

[Bæta lendingarsíðu flokks](enrich-category-page.md)

[Staðfesta aðgengi að efni síðu](verify-accessibility.md)

[Búa til gagnvirkar síður fyrir rafræn viðskipti sem byggja á færibreytum vefslóða](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
