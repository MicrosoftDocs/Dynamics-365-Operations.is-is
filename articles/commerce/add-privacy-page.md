---
title: Bæt við síðu persónuverndarstefnu
description: Þetta efni lýsir því hvernig á að bæta síðu persónuverndarstefnu við á vefsvæði í Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ee9a68f46c91299065732e5f65479906f9e06079
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001324"
---
# <a name="add-a-privacy-policy-page"></a>Bæt við síðu persónuverndarstefnu


[!include [banner](includes/banner.md)]

Þetta efni lýsir því hvernig á að bæta síðu persónuverndarstefnu við á vefsvæði í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Fylgni við friðhelgi einkalífsins felur í sér skipulagsaðgerðir sem upplýsa notendur vefsins um hvernig gögnum þeirra er safnað og meðhöndlað. Notendur geta síðan ákveðið hvernig þeir vilja að farið verði með persónuupplýsingar sínar og gripið til viðeigandi ráðstafana.

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a>Lestu yfirlýsingu Microsoft um persónuvernd í Dynamics 365 Commerce

Til að fara yfir persónuverndaryfirlýsingu Microsoft meðan þú ert innskráð/ur í Dynamics 365 Commerce höfundatól, veldu hnappinn **Hjálp** (**?**) efst í hægra horninu og veldu síðan **Persónuvernd og kökur**. Nýr flipi er opnaður sem hefur tengil á [Persónuverndaryfirlýsingu Microsoft](https://privacy.microsoft.com/privacystatement).

## <a name="build-a-privacy-policy-page-for-your-site"></a>Búðu til síðu með persónuverndarstefnu fyrir síðuna þína

Í Dynamics 365 Commerce eru nokkrar leiðir til að veita notendum vefsvæðisins aðgang að persónuverndarstefnu þinni. Þessi hluti sýnir hvernig á að byggja upp persónuverndarstefnusíðu og vísa síðan á síðuna með því að nota síðufótarbrot.

Leiðbeiningarnar sem fylgja eru dæmi sem sýnir hvernig á að smíða almenna persónuverndarstefnusíðu fyrir viðskiptasíðu. Þú berð ábyrgð á því að hanna og útfæra lausn á persónuverndarstefnu sem best uppfyllir lagalegar kröfur fyrirtækisins.

Til að hefjast handa skaltu í höfundatækjunum fara á síðuna sem þú vilt byggja upp persónuverndarstefnusíðu fyrir.

### <a name="create-a-template"></a>Búa til sniðmát

> [!NOTE]
> Ef sniðmát sem hægt er að nota fyrir persónuverndarstefnusíðuna hefur þegar verið stofnað skaltu fara beint áfram í kaflann [Búa til síðu með persónuverndarstefnu](#build-a-privacy-policy-page).

Fylgið eftirfarandi skrefum til að stofna sniðmát.

1. Farðu í **Sniðmát \> Nýtt sniðmát**.
1. Sláðu inn heiti sniðmáts og veldu síðan **Í lagi**.
1. Í sniðmátinu skaltu bæta við þeim einingum sem þarf í þar til gerð hólf á síðunni. Til leiðbeiningar skaltu halda músabendlinum yfir rauðu upphrópunarmerkjunum.

    Til dæmis kann hólfið **HTML-haus** að krefjast einingarinnar **Sjálfvirk ytri forskrift**.

1. Í hólfinu **Meginmál** bætirðu við einingunni **Sjálfgefin síða**.
1. Í einingunni **Sjálfgefin síða**, í hólfinu **Aðal**, skaltu bæta við einingunni **Bálkur með fjölbreyttu efni**.
1. Í einingunni **Bálkur með fjölbreyttu efni** skaltu bæta við einingunni **Bálkaliður með fjölbreyttu efni**.
1. Skráðu sniðmátið inn og birtu það.

### <a name="build-a-privacy-policy-page"></a>Byggja upp síðu persónuverndarstefnu

Fylgdu þessum skrefum til að byggja upp persónuverndarstefnusíðu.

1. Farðu á **Síður \> Ný síða**.
1. Veldu sniðmát fyrir persónuverndarstefnusíðuna.
1. Sláðu inn heiti og slóð síðu og veldu síðan **Í lagi**. 
1. Í hólfinu **Aðal** á síðunni bætirðu við einingunni **Bálkur með fjölbreyttu efni**.
1. Í einingunni **Bálkur með fjölbreyttu efni** skaltu bæta við einingunni **Bálkaliður með fjölbreyttu efni**.
1. Í eiginleikaglugganum fyrir eininguna **Bálkur með fjölbreyttu efni** velurðu **Bæta við gagnagjafa** og velur síðan **RTF-efni**.
1. Sláðu inn innihaldið fyrir persónuverndarstefnusíðuna í RTF-ritlinum. Stækkaðu textaritilinn í fulla skjástillingu eftir þörfum.
1. Þegar þú hefur lokið við að slá inn efni skaltu velja **Forskoðun** til að forskoða síðuna í vafranum.
1. Ljúktu öllu eftirstandandi viðbætum við síðuna og einingareiginleikana.
1. Skráðu persónuverndarsíðuna inn og birtu hana.

Til að birta slóðina fyrir persónuverndarstefnusíðuna skaltu fylgja þessum skrefum.

1. Farðu á **Vefslóðir** og veldu slóðina fyrir persónuverndarstefnusíðuna.
1. Birtu valda slóð.

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a>Búðu til tengil á persónuverndarstefnusíðu í síðufæti

Þú getur bætt krækju á persónuverndarstefnusíðuna við brot. Á þennan hátt er hægt að deila hlekknum og uppfæra hann á mörgum vefsíðum með því að vísa í brotið. Þetta dæmi sýnir hvernig á að bæta við tengli á persónuverndarstefnusíðuna við síðufótarbrot.

Til að bæta tengli við síðufótarbrot skaltu fylgja þessum skrefum.

1. Farðu í **Síðubrot \> Ný síðubrot**.
1. Veldu eininguna **Síðufótur** og sláðu síðan inn heiti í reitinn **Heiti blaðbrots**.
1. Í hólfinu **Síðufótaflokkur** bætirði við einingunni **Neðanmálsatriði**.
1. Í eiginleikaglugganum til hægri velurðu **Tengja texta**.
1. Í glugganum **Tengja texta** skal slá inn tenglatextinn og tengja mark persónuverndarstefnunnar og smella síðan á **Í lagi**.

    Til að fá slóðina á persónuverndarstefnusíðuna ferðu á **Síður**, farðu svo á persónuverndarstefnusíðuna og afritaðu slóðina úr eignarrúðunni.

1. Vistaðu brotið, skráðu það inn og gefðu það út.
1. Forskoðaðu brotið og prófaðu hlekkinn á persónuverndarstefnusíðuna.

Nú er hægt að vísa í brotið í sniðmátinu fyrir aðrar vefsíður. Þegar vísað er í þetta brot í einingunni **Síðufótur** í sniðmáti mun tilvísun tengilsins birtast á öllum síðum sem eru smíðaðar með því sniðmáti.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir samræmi](compliance-overview.md)

[Aðgengiseiginleikar og -geta](accessibility.md)

[Kökusamræmi](cookie-compliance.md)
