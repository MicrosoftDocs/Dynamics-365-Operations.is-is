---
title: Stillingar fyrir innsýn í fjármálum
description: Þetta efnisatriði útskýrir grunnstillingarskref sem mun gera kerfinu kleift að nota þá eiginleika sem eru í boði í Fjármálainnsýn.
author: ShivamPandey-msft
ms.date: 1/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 5668d3ddff777645b4f1c6608f025d0c5a63208a
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752979"
---
# <a name="configuration-for-finance-insights"></a>Stillingar fyrir innsýn í fjármálum

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Fjármálainnsýn sameinar virkni Microsoft Dynamics 365 Finance við Dataverse, Azure og AI Builder til að bjóða upp á öflug spáverkfæri fyrir fyrirtækið. Þetta efnisatriði útskýrir grunnstillingarskref sem mun gera kerfinu kleift að nota þá eiginleika sem eru í boði í Fjármálainnsýn. Til að ljúka aðferðunum í þessu efni með góðum árangri verður þú að hafa aðgang að kerfisstjóra og kerfissérstillingu í [Power Portal stjórnunarmiðstöð](https://admin.powerplatform.microsoft.com/), Kerfisstjóraaðgangur inn Dynamics 365 Finance, og aðgangur til að búa til umhverfi í Microsoft Dynamics Lífsferilsþjónusta (LCS).

> [!NOTE]
> Eftirfarandi aðferðir við að setja upp innsýn í fjármál gilda fyrir útgáfur af Dynamics 365 Finance útgáfu 10.0.21 og síðar.

## <a name="deploy-dynamics-365-finance"></a>Virkja Dynamics 365 Finance

Fylgja skal eftirfarandi skrefum til að setja upp umhverfin.

1. Í LCS, búðu til eða uppfærðu a Dynamics 365 Finance umhverfi. Umhverfið krefst app útgáfu 10.0.21 eða nýrri.

    > [!NOTE]
    > Umhverfið verður að vera háaðgengilegt (HA) umhverfi. (Þessi tegund umhverfis er einnig þekkt sem umhverfi í tveggja laga umhverfi.) Frekari upplýsingar er að finna í [Umhverfisskipulagning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

2. Ef þú ert að stilla Finance Insights í sandkassaumhverfi gætirðu þurft að afrita framleiðslugögn yfir í það umhverfi áður en spár virka. Spálíkanið notar gögn til margra ára til að búa til spár. Contoso kynningargögnin innihalda ekki nógu mörg söguleg gögn til að þjálfa spálíkanið á fullnægjandi hátt. 

## <a name="configure-dataverse"></a>Skilgreina Dataverse

Fylgdu eftirfarandi skrefum til að stilla Dataverse fyrir fjármálainnsýn.

- Í LCS skal opna síðu umhverfis og staðfesta að hlutinn **Power Platform samþætting** sé þegar uppsettur.

    - Ef hann er þegar uppsettur ætti heiti Dataverse umhverfisins sem tengt er við Finance-umhverfið að vera sýnt.
    - Ef það er ekki ennþá sett upp skaltu velja **Uppsetning**. Uppsetning á Dataverse umhverfið gæti tekið allt að klukkutíma. Þegar uppsetningunni er lokið, er Dataverse nafn umhverfis sem er tengt við fjármálaumhverfið ætti að vera skráð.

## <a name="configure-the-finance-insights-add-in"></a>Stilla innbót fjármálainnsýnar

Ef þú hefur áður sett upp Finance Insights viðbótina skaltu fjarlægja hana áður en þú lýkur eftirfarandi ferli.

> [!NOTE]
> Ef þú hefur þegar sett upp gagnavatnsaukinn í LCS, mun Finance Insights nota hana til að vista gögn sem eru nauðsynleg fyrir spár. Ef þú hefur ekki enn sett upp gagnavatnsaukinn í LCS, mun Finance Insights viðbótin búa til stýrt gagnavatn fyrir þig.

Fylgið þessum skrefum til að setja upp innbót fjármálainnsýnar.

1. Skráðu þig inn á LCS og veldu síðan **Allar upplýsingar**, undir heiti umhverfisins hægra megin á síðunni.
2. Í hlutanum **Innbætur umhverfis** skal velja **Setja upp nýja innbót**.
3. Veljið innbótina **Fjármálainnsýn**.
4. Samþykktu skilmálana og veldu síðan **Settu upp**.

Það gæti tekið nokkrar mínútur að setja innbótina upp.

## <a name="one-last-thing"></a>Eitt að lokum...

Eftir að viðbótin hefur verið sett upp gæti það tekið allt að klukkutíma áður en þú getur virkjað Finance Insights eiginleika í **Eiginleikastjórnun** vinnurými í Dynamics 365 Finance. Ef þú vilt ekki bíða svona lengi geturðu keyrt handvirkt **Athugun á stöðu úthlutunar innsýnar** ferli. 

1. Í Dynamics 365 Finance, fara til **Kerfisstjórnun \> Uppsetning \> Sjálfvirkni ferlisins**.
2. Á **Bakgrunnsferli** flipa, finna **Athugun á stöðu úthlutunar innsýnar**, og veldu **Breyta**.
3. Stilltu **Næsta framkvæmd** reit í 30 mínútur fyrir núverandi tíma.

   Þessi breyting ætti að knýja fram **Athugun á stöðu úthlutunar innsýnar** ferli til að keyra strax.

   Eftir **Athugun á stöðu úthlutunar innsýnar** ferli er keyrt með góðum árangri geturðu virkjað Finance Insights eiginleika í **Eiginleikastjórnun** vinnurými.

## <a name="feedback-and-support"></a>Ábendingar og stuðningur

Ef þú hefur áhuga á að veita endurgjöf, eða ef þú þarft aðstoð, sendu tölvupóst á [Fjármálainnsýn (Forskoðun)](mailto:fiap@microsoft.com).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
