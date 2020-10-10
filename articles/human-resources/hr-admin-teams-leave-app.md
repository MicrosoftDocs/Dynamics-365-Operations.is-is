---
title: Forritið „Human Resources“ í Teams
description: Þetta efnisatriði kynnir Microsoft Dynamics 365 Human Resources forritið í Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 09/01/2020
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
ms.openlocfilehash: 33322b9b553076125695f257b201463e9d8275c6
ms.sourcegitcommit: e27510ba52623c801353eed4853f8c0aeea3bb2d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/22/2020
ms.locfileid: "3828915"
---
# <a name="human-resources-app-in-teams"></a>Forritið „Human Resources“ í Teams

[!include [banner](includes/preview-feature.md)]

Microsoft Dynamics 365 Human Resources forritið í Microsoft Teams gerir starfsmönnum kleift að biðja um frí og skoða upplýsinga um frítíma á fljótlegan hátt í Microsoft Teams. Starsmenn geta haft samband við þjarka til að óska eftir upplýsingum. Flipinn **Frí** veitir ítarlegri upplýsingar. Að auki geta þeir sent fólki upplýsingar um frítíma framundan í hópum og spjalli utan forrits Human Resources.

![Human Resources Teams þjarkaforrit fyrir leyfi](./media/hr-admin-teams-leave-app-bot.png)

![Fríflipi fyrir fríforrit Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

![Leyfisbeiðnispjald Human Resources](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a>Setja upp

Hægt er að finna forritið Human Resources í Teams versluninni. Frekari upplýsingar um uppsetningu á Teams-forritinu má finna í [Stjórna leyfisbeiðnum í Teams](hr-teams-leave-app.md).

Frekari upplýsingar um stjórnun forritsheimilda í Teams er að finna í [Stjórna reglum forritaheimilda í Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a>Kveikja á tilkynningum fyrir forritið „Human Resources“ í Teams

Ef notendur eiga að fá tilkynningar vegna leyfisbeiðna í Teams-forritinu verður að virkja tilkynningar í Human Resources.

>[!NOTE]
>Aðeins notendur sem eru skráðir inn í Teams og nota Human Resources Teams-forritið fá tilkynningar.

1. Veldu í Human Resources **Kerfisstjórnun**.

2. Veljið **Tenglar**.

3. Undir **Uppsetning**, skal velja **Kerfisfæribreytur**.

4. Á flipanum **Almennt** skal stilla **Kveikja á tilkynningum fyrir Teams-forritið** á **Já**.

   ![Kveikja á tilkynningum fyrir Teams-forrit í kerfisfæribreytum](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. Til að kveikja á tilkynningum Teams fyrir alla notendur skal velja **Já** þegar spurt er um það.

   ![Virkja hóptilkynningar fyrir alla notendur](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a>Kveikja eða slökkva á hóptilkynningum fyrir einstaka notendur

Þegar búið er að virkja tilkynningar fyrir Human Resources Teams forritið er hægt að kveikja eða slökkva á tilkynningum fyrir einstaka notendur.

1. Veldu í Human Resources **Kerfisstjórnun**.

2. Veljið **Tenglar**.

3. Undir **Notendur** skal velja **Notandavalkostir**.

4. Veldu flipann **Verkflæði**.

5. Stillið **Kveikja á tilkynningum fyrir Teams-forritið** á **Já** til að virkja tilkynningar fyrir notandann eða **Nei** til að gera tilkynningar óvirkar fyrir notandann.

   ![Kveikja á tilkynningum Teams-forrits á verkflæðisflipanum Valkostir notanda](./media/hr-admin-teams-leave-app-notifications.png)

6. Veljið **Vista**.

## <a name="known-issues"></a>Þekkt vandamál

| Úthreyfing | Staða |
| --- | --- |
| Lárétt fletting virkar ekki í Android-símum | Lárétt fletting eru ekki vandamál í iOS eða borðtölvum. Unnið er að lagfæringu fyrir Android. |
| Staðan er röng þegar sendur er frítími fyrir dagsetningu í framtíðinni. | Spár eru ekki enn til staðar. Staðan birtist fyrir núverandi dagsetningu. |
| Ekki er hægt að hætta við beiðni með stöðuna **Í yfirferð**. | Þessi eiginleiki er ekki studdur eins og er og honum verður bætt við í síðari tíma útgáfum. |
| Upplýsingar um stöðu eru reiknaðar frá og með deginum í dag. | Kerfið sýnir eins og er ekki stöður frá uppsöfnunartímabilinu, jafnvel þótt það sé skilgreint í færibreytum leyfis og fjarvista. |

## <a name="privacy-notice"></a>Tilkynning um persónuvernd

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft Language Understanding Intelligent Service (LUIS)

Með Dynamics 365 Human Resources þjarkanum í Microsoft Teams er texti notanda greindur til að skilja undirliggjandi fyrirspurn/ásetning. Inntak notanda á borð við „Leita í contoso reikningi“ er flutt í eina af Cognitive Service hjá Microsoft sem kallast LUIS (Language Understanding Intelligent Service). Lesa meira um LUIS  [hér](https://www.luis.ai/). LUIS-þjónustan ræður úr eða skilur ásetning notanda (í þessu tilviki er ætlunin að finna upplýsingar) og markeiningu (í þessu tilviki er tilgreinda einingin reikningur sem heitir Contoso). Þessar upplýsingar eru svo sendar í Microsoft [Azure þjarkaramma](https://azure.microsoft.com/services/bot-service/) sem vinnur með gögn úr Dynamics 365 Human Resources og sækir æskilegar upplýsingum fyrir fyrirspurn notanda. 

Með því að setja upp og leyfa aðgang að þjarkanum samþykkir þú að leyfa LUIS-þjónustunni og Azure þjarkaramma að vinna úr ásetningi á bak við fyrirspurn, sem leiðir til betri notandaupplifunar. LUIS-þjónustan og Azure þjarkaramminn kunna að hafa mismikið samræmi samanborið við Dynamics 365 Human Resources. LUIS-þjónustan hefur aðeins aðgang að fyrirspurnum notenda og er ekki hönnuð til að tengjast við Dynamics 365 Human Resources gögn eða reikning. Notandi Dynamics 365 Human Resources þjarkans gæti fært inn fyrirspurn sem inniheldur gögn viðskiptavinar, persónuleg gögn eða önnur gögn og slíkt fyrirspurnarefni gæti verið sent til LUIS-þjónustunnar og Azure þjarkarammans. 

Innihald fyrirspurna og skilaboða notanda er vistað í LUIS-kerfi í að hámarki 30 daga, er dulkóðað þegar ekki í notkun og er ekki notað fyrir þjálfun eða endurbætur á þjónustu. Lestu meira um Cognitive Services  [hér](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Til að stjórna stjórnandastillingum fyrir forrit í Microsoft Teams er farið í [Microsoft Teams stjórnendamiðstöð](https://admin.teams.microsoft.com/).

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>Microsoft Teams, hnitanet Azure-tilviks og Azure Cosmos DB

Þegar Dynamics 365 Human Resources-forritið er notað í Microsoft Teams geta tiltekin gögn um viðskiptavini flætt út fyrir landsvæðið þar sem biðlari Human Resources þjónustunnar er notaður.

Dynamics 365 Human Resources sendir upplýsingar um leyfisbeiðni og verkflæðisverk til Microsoft Azure tilviks hnitanets og Microsoft Teams. Þessi gögn má geyma í Microsoft Azure Event Grid í allt að sólarhring og verða unnin í Bandaríkjunum, þau er dulkóðuð í flutningi og í hvíld, og eru ekki notuð af Microsoft eða meðhöndlunaraðilum fyrir þjálfun eða þjónustuúrbætur. Til að skilja hvar gögnin þín eru geymd í Teams skaltu skoða: [Staðsetning gagna í Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).

Í samskiptum við spjallarann í forriti Human Resources, er hægt að geyma innihald samtalsins í Azure Cosmos DB og flytja það yfir í Microsoft Teams. Þessi gögn má geyma í Azure Cosmos DB í allt að sólarhring og kunna að vera meðhöndluð utan staðsetningarinnar þar sem Human Resources-þjónusta leigjandans er uppsett, þau er dulkóðuð í flutningi og í hvíld, og eru ekki notuð af Microsoft eða meðhöndlunaraðilum fyrir þjálfun eða þjónustuúrbætur. Til að skilja hvar gögnin þín eru geymd í Teams skaltu skoða: [Staðsetning gagna í Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).
 
Til að takmarka aðgang að Human Resources í Microsoft Teams fyrir fyrirtækið þitt eða notendur innan fyrirtækisins skal skoða [Stjórna reglum um forritsheimildir í Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).

## <a name="see-also"></a>Sjá einnig 

[Sækja og setja upp Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams hjálparmiðstöð](https://support.office.com/teams)</br>
[Stjórna leyfisbeiðnum í Teams](hr-teams-leave-app.md)

