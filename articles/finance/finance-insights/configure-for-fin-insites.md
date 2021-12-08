---
title: Stillingar fyrir innsýn í fjármálum
description: Þetta efnisatriði útskýrir grunnstillingarskref sem mun gera kerfinu kleift að nota þá eiginleika sem eru í boði í Fjármálainnsýn.
author: ShivamPandey-msft
ms.date: 11/19/2021
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
ms.openlocfilehash: 6183e8a7500e9deff0ebf6b5dec8842ad4ca94cb
ms.sourcegitcommit: 6a9f068b59b62c95a507d1cc18b23f9fd80a859b
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/20/2021
ms.locfileid: "7827029"
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

## <a name="configure-your-azure-ad-tenant"></a>Stilltu þína Azure AD leigjanda

Azure Active Directory(Azure AD) verður að stilla þannig að hægt sé að nota það með Dataverse og Microsoft Power Platform umsóknir. Þessi uppsetning krefst þess að annað hvort **Verkeigandi** hlutverk eða **Umhverfisstjóri** hlutverki að vera úthlutað til notanda í **Öryggishlutverk verkefnisins** sviði í LCS.

Staðfestu að eftirfarandi uppsetningu sé lokið:

- Þú hefur **Kerfisstjóri** og **Kerfisaðlögun** aðgang í Power Portal stjórnunarmiðstöðinni.
- A Dynamics 365 Finance eða samsvarandi leyfi er beitt fyrir notandann sem er að setja upp Finance Insights viðbótina.

Eftirfarandi Azure AD öpp eru skráð í Azure AD.

|  Forrit                             | Auðkenni forrits                               |
|------------------------------------------|--------------------------------------|
| Microsoft Dynamics ERP Microservices CDS | 703e2651-d3fc-48f5-942c-74274233dba8 |
    
## <a name="configure-dataverse"></a>Skilgreina Dataverse

Fylgdu eftirfarandi skrefum til að stilla Dataverse fyrir fjármálainnsýn.

- Í LCS skal opna síðu umhverfis og staðfesta að hlutinn **Power Platform samþætting** sé þegar uppsettur.

    - Ef Dataverse hefur þegar verið sett upp, sem Dataverse nafn umhverfis sem er tengt við fjármálaumhverfið ætti að vera skráð.
    - Ef Dataverse hefur ekki enn verið sett upp, veldu **Uppsetning**. Uppsetning á Dataverse umhverfi getur tekið allt að klukkutíma. Þegar uppsetningunni hefur verið lokið mun Dataverse nafn umhverfis sem er tengt við í fjármálaumhverfinu ætti að vera skráð.
    - Ef þessi samþætting var sett upp með núverandi Microsoft Power Platform umhverfi skaltu hafa samband við kerfisstjóra til að ganga úr skugga um að tengt umhverfi sé ekki í óvirku ástandi.

        Fyrir frekari upplýsingar, sjá [Að virkja Power Platform sameining](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md). 

        Til að fá aðgang að Microsoft Power Platform admin síða, farðu á <https://admin.powerplatform.microsoft.com/environments>.

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

Ef þú hefur áhuga á að veita endurgjöf, eða ef þú þarft aðstoð, sendu tölvupóst á [Fjármálainnsýn (Preview)](mailto:fiap@microsoft.com).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
