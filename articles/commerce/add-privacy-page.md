---
title: Bæt við síðu persónuverndarstefnu
description: Þetta efnisatriði lýsir því hvernig á að bæta síðu með persónuverndarstefnu við svæði í Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 12cd0358279684ce1d3050348c37209ba3d29140
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797528"
---
# <a name="add-a-privacy-policy-page"></a>Bæta við persónuverndarstefnusíðu

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að bæta síðu með persónuverndarstefnu við svæði í Microsoft Dynamics 365 Commerce.

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

1. Farðu í **Sniðmát** og veldu síðan **Nýtt** til að búa til síðusniðmát.
1. Í svarglugganum **Nýtt sniðmát** undir **Heiti sniðmáts** skaltu slá inn **Sniðmát tilboðsborða** og velja síðan **Í lagi**.
1. Í sniðmátinu skaltu bæta við þeim einingum sem þarf í þar til gerð hólf á síðunni. Til leiðbeiningar skaltu halda músabendlinum yfir rauðu upphrópunarmerkjunum. (Til dæmis gæti hólfið **HTML-haus** þurft eininguna **Sjálfgefin ytri forskrift**.)
1. Í hólfinu **Meginmál** bætirðu við einingunni **Sjálfgefin síða**.
1. Í einingunni **Sjálfgefin síða**, í hólfinu **Aðal**, skaltu bæta við einingunni **Bálkur með fjölbreyttu efni**.
1. Í einingunni **Bálkur með fjölbreyttu efni** skaltu bæta við einingunni **Bálkaliður með fjölbreyttu efni**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það.

### <a name="build-a-privacy-policy-page"></a>Byggja upp síðu persónuverndarstefnu

Fylgdu þessum skrefum til að byggja upp persónuverndarstefnusíðu.

1. Farðu á **Síður** og veldu **Ný** til að búa til síðu.
1. Í svarglugganum **Velja sniðmát** skal velja sniðmátið fyrir síðu persónuverndarstefnu.
1. Sláðu inn síðuheiti og vefslóð síðu og veldu síðan **Í lagi**. 
1. Í hólfinu **Aðal** á síðunni bætirðu við einingunni **Bálkur með fjölbreyttu efni**.
1. Í einingunni **Bálkur með fjölbreyttu efni** skaltu bæta við einingunni **Bálkaliður með fjölbreyttu efni**.
1. Í eiginleikaglugganum fyrir eininguna **Bálkur með fjölbreyttu efni** velurðu **Bæta við gagnagjafa** og velur síðan **RTF-efni**.
1. Sláðu inn innihaldið fyrir persónuverndarstefnusíðuna í RTF-ritlinum. Stækkaðu textaritilinn í fulla skjástillingu eftir þörfum.
1. Þegar þú hefur lokið við að slá inn efni skaltu velja **Forskoðun** til að forskoða síðuna í vafranum.
1. Ljúktu öllu eftirstandandi viðbætum við síðuna og einingareiginleikana.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.

Til að birta slóðina fyrir persónuverndarstefnusíðuna skaltu fylgja þessum skrefum.

1. Farðu á **Vefslóðir** og veldu slóðina fyrir persónuverndarstefnusíðuna.
1. Veldu **Birta** til að birta valda vefslóð.

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a>Búðu til tengil á persónuverndarstefnusíðu í síðufæti

Þú getur bætt krækju á persónuverndarstefnusíðuna við brot. Á þennan hátt er hægt að deila hlekknum og uppfæra hann á mörgum vefsíðum með því að vísa í brotið. Þetta dæmi sýnir hvernig á að bæta við tengli á persónuverndarstefnusíðuna við síðufótarbrot.

Til að bæta tengli við síðufótarbrot skaltu fylgja þessum skrefum.

1. Farðu í **Brot** og veldu síðan **Nýtt** til að búa til síðubrot.
1. Í svarglugganum **Nýtt brot** skal velja eininguna **Síðufótur**.
1. Undir **Heiti brots** skal slá inn heiti brotsins og síðan velja **Í lagi**.
1. Í hólfinu **Síðufótaflokkur** bætirði við einingunni **Neðanmálsatriði**.
1. Í eiginleikaglugganum til hægri velurðu **Tengja texta**.
1. Í glugganum **Tengja texta** skal slá inn tenglatextinn og tengja mark persónuverndarstefnunnar og smella síðan á **Í lagi**.
1. Til að fá slóðina á persónuverndarstefnusíðuna ferðu á **Síður**, farðu svo á persónuverndarstefnusíðuna og afritaðu slóðina úr eignarrúðunni.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila brotinu og veldu síðan **Birta** til að birta það.
1. Forskoðaðu brotið og prófaðu hlekkinn á persónuverndarstefnusíðuna.

Nú er hægt að vísa í brotið í sniðmátinu fyrir aðrar vefsíður. Þegar vísað er í þetta brot í einingunni **Síðufótur** í sniðmáti mun tilvísun tengilsins birtast á öllum síðum sem eru smíðaðar með því sniðmáti.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir samræmi](compliance-overview.md)

[Aðgengiseiginleikar og -geta](accessibility.md)

[Reglufylgni köku](cookie-compliance.md)

[Skipta um notandakenni sem tengjast röktum efnisbreytingum](replace-IDs-tracked-changes.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
