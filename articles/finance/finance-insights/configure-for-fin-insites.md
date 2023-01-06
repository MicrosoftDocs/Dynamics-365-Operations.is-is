---
title: Stillingar fyrir Finance Insights
description: Þessi grein útskýrir grunnstillingarskref sem mun gera kerfinu kleift að nota þá eiginleika sem eru í boði í Finance Insights.
author: ShivamPandey-msft
ms.date: 09/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 07edea234839a477802e5cd875620509c8f92d69
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/12/2022
ms.locfileid: "9644115"
---
# <a name="configuration-for-finance-insights"></a>Stillingar fyrir Finance Insights

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Finance Insights sameinar virkni Microsoft Dynamics 365 Finance við Dataverse, Azure og AI Builder til að bjóða upp á öflug spáverkfæri fyrir fyrirtækið. Þessi grein útskýrir grunnstillingarskref sem mun gera kerfinu kleift að nota þá eiginleika sem eru í boði í Finance Insights. Til að ljúka ferlunum í þessari grein verður þú að hafa aðgang kerfisstjóra og kerfisstillis í [Stjórnendamiðstöð Power Portal](https://admin.powerplatform.microsoft.com/), aðgang kerfisstjóra í Dynamics 365 Finance og aðgang til að búa til umhverfi í Microsoft Dynamics Lifecycle Services (LCS).

> [!NOTE]
> Eftirfarandi ferli til að setja upp Finance Insights eru gild fyrir útgáfur af Dynamics 365 Finance útgáfu 10.0.21 og síðari.

## <a name="deploy-dynamics-365-finance"></a>Nota Dynamics 365 Finance

Fylgja skal eftirfarandi skrefum til að setja upp umhverfin.

1. Í LCS skal búa til eða uppfæra umhverfi Dynamics 365 Finance. Umhverfið krefst forritsútgáfu 10.0.21 eða nýrri.

    > [!NOTE]
    > Umhverfið verður að vera vel tiltækt umhverfi. (Þessi tegund umhverfis er einnig þekkt sem umhverfi í tveggja laga umhverfi.) Frekari upplýsingar er að finna í [Umhverfisskipulagning](/fin-ops-core/fin-ops/imp-lifecycle/environment-planning).

2. Ef þú ert að stilla Finance Insights í sandkassaumhverfi gætirðu þurft að afrita framleiðslugögn í það umhverfi áður en spár munu virka. Spálíkanið notar gögn til margra ára til að búa til spár. Sýnigögn Contoso innihalda ekki næg söguleg gögn til að hægt sé að þjálfa spálíkanið á fullnægjandi hátt. 

## <a name="configure-your-azure-ad-tenant"></a>Skilgreindu Azure AD leigjandann

Azure Active Directory (Azure AD) verður að vera skilgreint þannig að hægt sé að nota það með Dataverse og Microsoft Power Platform forritunum. Þessi skilgreining krefst þess að annaðhvort hlutverkið **Eigandi verks** eða **Stjórnandi umhverfis** sé úthlutað á notandann í reitnum **Öryggishlutverk verks** í LCS.

Staðfestið að eftirfarandi uppsetningu sé lokið:

- Þú hefur aðgang **Kerfisstjóra** og **Kerfisstillis** í stjórnendamiðstöð Power Portal.
- Dynamics 365 Finance eða sambærilegt leyfi er sett á notandann sem er að setja upp innbót Finance Insights.
- Eftirfarandi Azure AD forrit eru skráð á Azure AD.

    |  Forrit                             | Auðkenni forrits                               |
    |------------------------------------------|--------------------------------------|
    | Microsoft Dynamics ERP Microservices CDS | 703e2651-d3fc-48f5-942c-74274233dba8 |

    Til að ganga úr skugga um að forritið sé skráð í Azure AD skal athuga listann **Öll forrit**. Frekari upplýsingar er að finna í [Skoða forrit fyrirtækis](/azure/active-directory/manage-apps/view-applications-portal).
  
    Ef forritið er ekki skráð í Azure AD skal hafa samband við notendaþjónustu.
  
## <a name="configure-dataverse"></a>Skilgreina Dataverse

Fylgdu eftirfarandi skrefum til að stilla Dataverse fyrir fjármálainnsýn.

- Í LCS skal opna síðu umhverfis og staðfesta að hlutinn **Power Platform samþætting** sé þegar uppsettur.

    - Ef Dataverse hefur þegar verið sett upp ætti heiti Dataverse umhverfisins sem tengt er við Finance-umhverfið að vera gefið upp.
    - Ef Dataverse hefur ekki verið sett upp ennþá skal velja **Uppsetning**. Uppsetning Dataverse umhverfisins getur tekið allt að klukkustund. Þegar uppsetningunni er lokið ætti heiti Dataverse umhverfisins sem er tengt við Finance-umhverfið að vera gefið upp.
    - Ef þessi samþætting var sett upp með núverandi Microsoft Power Platform umhverfi skaltu hafa samband við kerfisstjórann til að ganga úr skugga um að tengt umhverfi sé ekki í óvirkri stöðu.

        Frekari upplýsingar er að finna í [Virkja Power Platform samþættinguna](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md). 

        Til að komast inn á Microsoft Power Platform vefsvæði stjórnanda skaltu fara á<https://admin.powerplatform.microsoft.com/environments>.

## <a name="configure-the-finance-insights-add-in"></a>Stilla innbót fjármálainnsýnar

Ef innbót Finance Insights hefur þegar verið sett upp skaltu fjarlægja hana áður en þú klárar eftirfarandi ferli.

> [!NOTE]
> Ef þú hefur þegar sett upp innbót gagnalindar mun Finance Insights nota hana til að vista gögn sem þarf fyrir spár. Ef þú hefur ekki enn sett upp innbót gagnalindar í LCS mun innbót Finance Insights búa til stýrða gagnalind fyrir þig.

Fylgið þessum skrefum til að setja upp innbót fjármálainnsýnar.

1. Skráðu þig inn á LCS og veldu síðan **Allar upplýsingar**, undir heiti umhverfisins hægra megin á síðunni.
2. Í hlutanum **Innbætur umhverfis** skal velja **Setja upp nýja innbót**.
3. Veljið innbótina **Fjármálainnsýn**.
4. Samþykkið skilmálana og skilyrðin og veljið því næst **Setja upp**.

Það gæti tekið nokkrar mínútur að setja innbótina upp.

## <a name="one-last-thing"></a>Eitt að lokum...

Eftir að innbótin hefur verið sett upp gæti tekið allt að klukkustund áður en þú getur virkjað Finance Insights á vinnusvæðinu **Eiginleikastjórnun** í Dynamics 365 Finance. Ef þú vilt ekki bíða svo lengi geturðu keyrt ferlið **Athugun á úthlutunarstöðu innsýnar** á handvirkan hátt. 

1. Í Dynamics 365 Finance skaltu fara í **Kerfisstjórnun \> Uppsetning \> Sjálfvirkni ferlis**.
2. Í flipanum **Bakgrunnsvinnslur** skaltu finna **Athugun á úthlutunarstöðu innsýnar** og velja **Breyta**.
3. Stilltu reitinn **Næsta keyrsla** á 30 mínútum á undan núverandi tíma.

   Þessi breyting ætti að þvinga ferlið **Athugun á úthlutunarstöðu innsýnar** til að keyra strax.

   Þegar ferlið **Athugun á úthlutunarstöðu innsýnar** hefur verið keyrt er hægt að virkja eiginleika Finance insights á vinnusvæðinu **Eiginleikastjórnun**.

> [!NOTE]
> Ef ferlið **Athugun á úthlutunarstöðu innsýnar** keyrir ekki skal fara í **Kerfisstjórnun** > **Fyrirspurnir** > **Runuvinnslur**. Í reitnum **Bókunarvinnsla sjálfvirkniferlis í kerfinu** skal breyta gildinu í **Í bið** til að hefja ferlið. 
> 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
