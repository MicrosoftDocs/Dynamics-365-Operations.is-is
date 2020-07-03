---
title: Forritið „Human Resources“ í Teams
description: Þetta efnisatriði kynnir Microsoft Dynamics 365 Human Resources forritið í Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 36684710e39c27840cc4aaa259a85579104fd8d6
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431131"
---
# <a name="human-resources-app-in-teams"></a>Forritið „Human Resources“ í Teams

[!include [banner](includes/preview-feature.md)]

Microsoft Dynamics 365 Human Resources forritið í Microsoft Teams gerir starfsmönnum kleift að biðja um frí og skoða upplýsinga um frítíma á fljótlegan hátt í Microsoft Teams. Starsmenn geta haft samband við þjarka til að óska eftir upplýsingum. Finna má ítarlegri upplýsingar á flipanum **Frí**.

![Human Resources Teams þjarkaforrit fyrir leyfi](./media/hr-admin-teams-leave-app-bot.png)

![Fríflipi fyrir fríforrit Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a>Setja upp

Hægt er að finna forritið Human Resources í Teams versluninni. Frekari upplýsingar um uppsetningu á Teams-forritinu má finna í [Stjórna leyfisbeiðnum í Teams](hr-teams-leave-app.md).

Frekari upplýsingar um stjórnun forritsheimilda í Teams er að finna í [Stjórna reglum forritaheimilda í Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).

## <a name="known-issues"></a>Þekkt vandamál

| Úthreyfing | Staða |
| --- | --- |
| Villa: Vandamál kom upp við að finna umhverfi til að tengjast við. | Þessi villa gæti komið upp jafnvel þótt búið sé að staðfesta að notandinn megi fá aðgang að einu eða fleiri mannauðsumhverfum. Að auki er ekki víst að öll umhverfin sjáist eins og vonast var eftir. Þangað til leyst verður úr þessu vandamáli þarf að eyða notandanum og flytja hann síðan inn aftur til að komast hjá þessum vanda. |
| Staðan er röng þegar sendur er frítími fyrir dagsetningu í framtíðinni. | Spár eru ekki enn til staðar. Staðan birtist fyrir núverandi dagsetningu. |
| Þegar tekinn fjöldi stunda er minnkaður í fyrirliggjandi beiðni fer **Eftirstandandi staða** niður í stað þess að fara upp. | Við munum leysa úr þessu vandamáli í framtíðinni. Birting er röng, en réttar upphæðir eru leiðréttar við sendingu. |
| Tvö **Væntanlegt frí** kort birtast fyrir sömu dagsetningar. | Kortin tákna einstakar sendingar. Við munum halda áfram að taka við ábendingum og gera breytingar. |
| Ekki er hægt að hætta við beiðni með stöðuna **Í yfirferð**. | Þessi eiginleiki er ekki studdur eins og er og honum verður bætt við í síðari tíma útgáfum. |
| Upplýsingar um stöðu eru reiknaðar frá og með deginum í dag. | Kerfið sýnir eins og er ekki stöður frá uppsöfnunartímabilinu, jafnvel þótt það sé skilgreint í færibreytum leyfis og fjarvista. |

## <a name="privacy-notice"></a>Tilkynning um persónuvernd

Með Dynamics 365 Human Resources þjarkanum í Microsoft Teams er texti notanda greindur til að skilja undirliggjandi fyrirspurn/ásetning. Inntak notanda á borð við „Leita í contoso reikningi“ er flutt í eina af Cognitive Service hjá Microsoft sem kallast LUIS (Language Understanding Intelligent Service). Lesa meira um LUIS  [hér](https://www.luis.ai/). LUIS-þjónustan ræður úr eða skilur ásetning notanda (í þessu tilviki er ætlunin að finna upplýsingar) og markeiningu (í þessu tilviki er tilgreinda einingin reikningur sem heitir Contoso). Þessar upplýsingar eru svo sendar í Microsoft  [Azure þjarkaramma](https://azure.microsoft.com/services/bot-service/) sem vinnur með gögn úr Dynamics 365 Human Resources og sækir æskilegar upplýsingum fyrir fyrirspurn notanda. 

Með því að setja upp og leyfa aðgang að þjarkanum samþykkir þú að leyfa LUIS-þjónustunni og Azure þjarkaramma að vinna úr ásetningi á bak við fyrirspurn, sem leiðir til betri notandaupplifunar. LUIS-þjónustan og Azure þjarkaramminn kunna að hafa mismikið samræmi samanborið við Dynamics 365 Human Resources. LUIS-þjónustan hefur aðeins aðgang að fyrirspurnum notenda og er ekki hönnuð til að tengjast við Dynamics 365 Human Resources gögn eða reikning. Notandi Dynamics 365 Human Resources þjarkans gæti fært inn fyrirspurn sem inniheldur gögn viðskiptavinar, persónuleg gögn eða önnur gögn og slíkt fyrirspurnarefni gæti verið sent til LUIS-þjónustunnar og Azure þjarkarammans. 

Innihald fyrirspurna og skilaboða notanda er vistað í LUIS-kerfi í að hámarki 30 daga, er dulkóðað þegar ekki í notkun og er ekki notað fyrir þjálfun eða endurbætur á þjónustu. Lestu meira um Cognitive Services  [hér](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Til að stjórna stjórnandastillingum fyrir forrit í Microsoft Teams er farið í [Microsoft Teams stjórnendamiðstöð](https://admin.teams.microsoft.com/). 

## <a name="see-also"></a>Sjá einnig 

[Sækja og setja upp Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams hjálparmiðstöð](https://support.office.com/teams)</br>
[Stjórna leyfisbeiðnum í Teams](hr-teams-leave-app.md)

