---
title: Ákvæði Microsoft Teams frá Dynamics 365 Commerce
description: Þessi grein lýsir því hvernig á að útvega Microsoft Teams með því að nota skipulagsgögn frá Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 56d7cb6da5c359d3e93553adbdc70a4786c42648
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268974"
---
# <a name="provision-microsoft-teams-from-dynamics-365-commerce"></a>Ákvæði Microsoft Teams frá Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að útvega Microsoft Teams með því að nota skipulagsgögn frá Dynamics 365 Commerce.

Dynamics 365 Commerce býður upp á einfalda leið til að úthluta Teams ef ekki er enn búið að setja upp teymi fyrir smásöluverslanir. Með því að nýta sér vel skilgreindar upplýsingar úr Commerce sem ætlunin er að nota í Teams er hægt að aðstoða starfsfólk verslunar að koma sér af stað í Teams. Þessar upplýsingar fela í sér stigveldi fyrirtækis, heiti verslana, upplýsingar um starfsfólk og Azure Active Directory (Azure AD) reikninga. 

Ferlið við að úthluta Teams felur í sér tvö meginskref:

1. Í Teams skal stofna teymi fyrir hverja smásöluverslun og bæta starfsfólki verslunar við sem meðlimum í viðeigandi teymi. Ef starfsmaður tengist fleiri en einni smásöluverslun mun teymisaðild sýna þá staðreynd. Samskiptateymi sem inniheldur svæðisstjóra sem meðlimi verður stofnað til að stuðla að útgáfu verka úr Teams.
1. Hlaðið upp stigveldi fyrirtækis úr Commerce yfir í Teams.

## <a name="provision-teams-in-commerce-headquarters"></a>Ráðstafa Teams í Commerce Headquarters

Áður en Microsoft Teams er úthlutað skal ljúka þessum verkum:

- Gangið úr skugga um að allir svæðisstjórar hafi verið gerðir að samskiptastjórum.
- Staðfestið að Azure-reikningur allra verslunarstjóra og starfsfólks hafi verið tengdur við starfsmannaskrá yfirmanns eða starfsmanns í Commerce Headquarters.

Til að úthluta Teams í Commerce Headquarters skal fylgja þessum skrefum.

1. Opnið **Smásala og viðskipti \> Uppsetning rásar \> Microsoft Teams Samþættingarskilgreining**.
1. Á aðgerðasvæðinu skal velja **Úthluta teymum**. Runuvinnsla sem kallast **Úthlutun Teams** er stofnuð.
1. Farið í **Kerfisstjórnun \> Fyrirspurnir \> Runuvinnslur** og finnið nýlegustu vinnuna sem er með lýsinguna **Úthlutun Teams**. Bíðið þar til verkið hefur verið keyrt.

> [!TIP]
> Ef engum svæðisstjóra, verslunarstjóra eða starfsmanni verslunar hefur verið tengdur við Teams-leyfi gæti komið upp eftirfarandi villuboð: „Ekki tókst að sækja viðeigandi Sku-flokk fyrir notanda.“ Til að lagfæra vandamálið skal velja **Samstilla teymi og meðlimi** á aðgerðasvæðinu.

<!-- ![Dynamics 365 Commerce - Teams integration configuration.](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)-->

## <a name="validate-teams-provisioning-in-the-teams-admin-center"></a>Staðfesta úthlutun Teams í stjórnendamiðstöð Teams

Til að staðfesta úthlutun Microsoft Teams í stjórnendamiðstöð Microsoft Teams skal fylgja þessum skrefum.
    
1. Farið í [Stjórnendamiðstöð Teams](https://admin.teams.microsoft.com/) og skráið ykkur inn sem stjórnandi leigjanda rafrænna viðskipta.
1. Á svæðinu vinstra megin skal velja **Teymi** til að stækka það og velja því næst **Stjórna teymum**.
1. Staðfestið að eitt teymi hafi verið stofnað fyrir hverja smásöluverslun Commerce.
1. Veljið teymi og staðfestið að starfsmönnum verslunar hafi verið bætt við sem meðlimum.
1. Á svæðinu vinstra megin skal velja **Notendur** og staðfesta að öllum starfsmönnum verslunar í öllum verslunum hafi verið bætt við sem notendum.

Eftirfarandi mynd sýnir dæmi um síðuna **Stjórna teymum** í stjórnendamiðstöð Teams.

![Dæmi um síðuna Stjórna teymum í stjórnendamiðstöð Teams.](media/Teams-FLW-Admin-Teams.png)

## <a name="upload-a-commerce-organizational-hierarchy-to-teams"></a>Hlaða upp fyrirtækisstigveldi Commerce í Teams
    
Hægt er að nota fyrirtækisstigveldi Commerce í Microsoft Teams til að gefa verk út til allra eða valdra verslana sem nota sama fyrirtækisstigveldið.

Til að hlaða upp fyrirtækisstigveldi Commerce í Teams skal fylgja þessum skrefum.
    
1. Í Commerce Headquarters skal fara í **Smásala og viðskipti \> Uppsetning rásar \> Microsoft Teams Samþættingarskilgreining**.
1. Veljið **Sækja markstigveldi** og veljið því næst **Smásöluverslanir eftir svæði** til að sækja CSV-skrá með gildum sem eru aðskilin með kommu fyrir stigveldi fyrirtækisins.
1. Setjið upp einingu Microsoft Teams PowerShell með því að fylgja skrefunum í [Setja upp Microsoft Teams PowerShell](/microsoftteams/teams-powershell-install).
1. Þegar beðið er um það í glugga Teams PowerShell skal skrá sig inn í gegnum stjórnendareikninginn fyrir leigjanda Azure AD.
1. Fylgið skrefunum í [Setja upp markstigveldi teymisins](/microsoftteams/set-up-your-team-hierarchy) til að hlaða upp CSV-skránni fyrir markstigveldið.

## <a name="verify-that-the-organizational-hierarchy-was-uploaded-to-teams"></a>Staðfesta að stigveldi fyrirtækisins hafi verið hlaðið upp í Teams

Til að staðfesta að stigveldi fyrirtækisins hafi verið hlaðið upp í Microsoft Teams skal fylgja þessum skrefum.

1. Skráðu þig inn á Teams sem samskiptastjóra.
1. Á yfirlitssvæðinu vinstra megin skal velja **Verk eftir Planner**.
1. Í flipanum **Útgefnir listar** skal búa til nýjan lista sem er með prufuverk.
1. Velja **Birta**. Stigveldi fyrirtækisins ætti að birtast í svarglugganum **Velja hverjum á að birta** eins og sýnt er í dæminu í eftirfarandi skýringarmynd.

![Dæmi um stigveldi fyrirtækis í svarglugganum Velja hverjum á að birta.](media/Microsoft-teams-verify-org-hierarchy.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Dynamics 365 Commerce og Microsoft Teams samþættingaryfirlit](commerce-teams-integration.md)

[Gera Dynamics 365 Commerce og Microsoft Teams samþættingu virka](enable-teams-integration.md)

[Samstilla verkstjórnun á milli Microsoft Teams og Dynamics 365 Commerce sölustaðar](synchronize-tasks-teams-pos.md)

[Stjórna notandahlutverkum í Microsoft Teams](manage-user-roles-teams.md)

[Varpa verslunum og teymum ef fyrirliggjandi teymi eru í Microsoft Teams](map-stores-existing-teams.md)

[Algengar spurningar um samþættingu Dynamics 365 Commerce og Microsoft Teams](teams-integration-faq.md)
