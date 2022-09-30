---
title: Stillingar fyrir innsýn í fjármálum
description: Þessi grein útskýrir stillingarskref sem gera kerfinu þínu kleift að nota þá möguleika sem eru tiltækir í Finance Insights.
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
ms.openlocfilehash: 05bf5fe5a5ff86bbf52ed58ee6b1e84c15bf2c1e
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573195"
---
# <a name="configuration-for-finance-insights"></a>Stillingar fyrir innsýn í fjármálum

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Fjármálainnsýn sameinar virkni frá Microsoft Dynamics 365 Fjármál með Dataverse, Azure og AI Builder til að bjóða upp á öflug spáverkfæri fyrir fyrirtæki þitt. Þessi grein útskýrir stillingarskref sem gera kerfinu þínu kleift að nota þá möguleika sem eru tiltækir í Finance Insights. Til að ljúka aðferðunum í þessari grein verður þú að hafa aðgang að kerfisstjóra og kerfissérstillingu í [Power Portal stjórnunarmiðstöð](https://admin.powerplatform.microsoft.com/), Kerfisstjóraaðgangur í Dynamics 365 Finance og aðgangur til að búa til umhverfi í Microsoft Dynamics Lífsferilsþjónusta (LCS).

> [!NOTE]
> Eftirfarandi aðferðir við að setja upp Finance Insights gilda fyrir útgáfur af Dynamics 365 Finance útgáfu 10.0.21 og síðar.

## <a name="deploy-dynamics-365-finance"></a>Settu upp Dynamics 365 Finance

Fylgja skal eftirfarandi skrefum til að setja upp umhverfin.

1. Í LCS skaltu búa til eða uppfæra Dynamics 365 Finance umhverfi. Umhverfið krefst app útgáfu 10.0.21 eða nýrri.

    > [!NOTE]
    > Umhverfið verður að vera háaðgengilegt (HA) umhverfi. (Þessi tegund umhverfis er einnig þekkt sem umhverfi í tveggja laga umhverfi.) Frekari upplýsingar er að finna í [Umhverfisskipulagning](/fin-ops-core/fin-ops/imp-lifecycle/environment-planning).

2. Ef þú ert að stilla Finance Insights í sandkassaumhverfi gætirðu þurft að afrita framleiðslugögn í það umhverfi áður en spár virka. Spálíkanið notar gögn til margra ára til að búa til spár. Contoso kynningargögnin innihalda ekki nógu mörg söguleg gögn til að þjálfa spálíkanið á fullnægjandi hátt. 

## <a name="configure-your-azure-ad-tenant"></a>Stilltu þína Azure AD leigjanda

Azure Active Directory(Azure AD) verður að stilla þannig að hægt sé að nota það með Dataverse og Microsoft Power Platform umsóknir. Þessi uppsetning krefst þess að annað hvort **Verkeigandi** hlutverk eða **Umhverfisstjóri** hlutverki að vera úthlutað til notanda í **Öryggishlutverk verkefnisins** sviði í LCS.

Staðfestu að eftirfarandi uppsetningu sé lokið:

- Þú hefur **Kerfisstjóri** og **Kerfisaðlögun** aðgang í Power Portal stjórnunarmiðstöðinni.
- Dynamics 365 Finance eða sambærilegt leyfi er notað fyrir notandann sem er að setja upp Finance Insights viðbótina.
- Eftirfarandi Azure AD öpp eru skráð í Azure AD.

    |  Forrit                             | Auðkenni forrits                               |
    |------------------------------------------|--------------------------------------|
    | Microsoft Dynamics ERP Microservices CDS | 703e2651-d3fc-48f5-942c-74274233dba8 |

    Til að staðfesta að forritið sé skráð í Azure AD, athugaðu **Allar umsóknir** lista. Fyrir frekari upplýsingar, sjá [Skoða fyrirtækjaforrit](/azure/active-directory/manage-apps/view-applications-portal).
  
    Ef umsóknin er ekki skráð í Azure AD, hafðu samband við þjónustudeild.
  
## <a name="configure-dataverse"></a>Skilgreina Dataverse

Fylgdu eftirfarandi skrefum til að stilla Dataverse fyrir fjármálainnsýn.

- Í LCS skal opna síðu umhverfis og staðfesta að hlutinn **Power Platform samþætting** sé þegar uppsettur.

    - Ef Dataverse hefur þegar verið sett upp, sem Dataverse nafn umhverfis sem er tengt við fjármálaumhverfið ætti að vera skráð.
    - Ef Dataverse hefur ekki enn verið sett upp, veldu **Uppsetning**. Uppsetning á Dataverse umhverfi getur tekið allt að klukkutíma. Þegar uppsetningunni hefur verið lokið, mun Dataverse nafn umhverfis sem er tengt við í fjármálaumhverfinu ætti að vera skráð.
    - Ef þessi samþætting var sett upp með núverandi Microsoft Power Platform umhverfi, hafðu samband við kerfisstjórann þinn til að ganga úr skugga um að tengda umhverfið sé ekki óvirkt.

        Fyrir frekari upplýsingar, sjá [Að virkja Power Platform samþættingu](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md). 

        Til að fá aðgang að Microsoft Power Platform admin síða, farðu á <https://admin.powerplatform.microsoft.com/environments>.

## <a name="configure-the-finance-insights-add-in"></a>Stilla innbót fjármálainnsýnar

Ef þú hefur áður sett upp Finance Insights viðbótina skaltu fjarlægja hana áður en þú lýkur eftirfarandi ferli.

> [!NOTE]
> Ef þú hefur þegar sett upp gagnavatnsaukinn í LCS mun Finance Insights nota hana til að vista gögn sem eru nauðsynleg fyrir spár. Ef þú hefur ekki enn sett upp gagnavatnsaukinn í LCS, mun Finance Insights viðbótin búa til stýrt gagnavatn fyrir þig.

Fylgið þessum skrefum til að setja upp innbót fjármálainnsýnar.

1. Skráðu þig inn á LCS og veldu síðan **Allar upplýsingar**, undir heiti umhverfisins hægra megin á síðunni.
2. Í hlutanum **Innbætur umhverfis** skal velja **Setja upp nýja innbót**.
3. Veljið innbótina **Fjármálainnsýn**.
4. Samþykktu skilmálana og veldu síðan **Settu upp**.

Það gæti tekið nokkrar mínútur að setja innbótina upp.

## <a name="one-last-thing"></a>Eitt að lokum...

Eftir að viðbótin hefur verið sett upp gæti það tekið allt að klukkutíma áður en þú getur virkjað eiginleika Finance Insights í **Eiginleikastjórnun** vinnusvæði í Dynamics 365 Finance. Ef þú vilt ekki bíða svona lengi geturðu keyrt handvirkt **Athugun á stöðu úthlutunar innsýnar** ferli. 

1. Í Dynamics 365 Finance, farðu í **Kerfisstjórnun \> Uppsetning \> Sjálfvirkni ferlisins**.
2. Á **Bakgrunnsferli** flipi, finna **Athugun á stöðu úthlutunar innsýnar**, og veldu **Breyta**.
3. Stilltu **Næsta framkvæmd** reit í 30 mínútur fyrir núverandi tíma.

   Þessi breyting ætti að knýja fram **Athugun á stöðu úthlutunar innsýnar** ferli til að keyra strax.

   Eftir **Athugun á stöðu úthlutunar innsýnar** ferli er keyrt með góðum árangri geturðu virkjað Finance Insights eiginleika í **Eiginleikastjórnun** vinnurými.

> [!NOTE]
> Ef **Athugun á stöðu úthlutunar innsýnar** ferlið keyrir ekki, farðu til **Kerfisstjórnun** > **Fyrirspurnir** > **Lotustörf**. Í **Könnunarkerfi sjálfvirkt ferli** reit, breyttu gildinu í **Bíður** að hefja ferlið. 
> 
## <a name="feedback-and-support"></a>Ábendingar og stuðningur

Ef þú hefur áhuga á að veita endurgjöf, eða ef þú þarft aðstoð, sendu tölvupóst á [Fjármálainnsýn (Forskoðun)](mailto:fiap@microsoft.com).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
