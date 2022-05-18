---
title: Forritið „Human Resources“ í Teams
description: Þetta efnisatriði kynnir Microsoft Dynamics 365 Human Resources forritið í Microsoft Teams.
author: twheeloc
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: debb18ab85e5b9011166a73571533a84d3f53512
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/05/2022
ms.locfileid: "8717084"
---
# <a name="human-resources-app-in-teams"></a>Forritið „Human Resources“ í Teams


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources app í Microsoft Teams skulum starfsmenn biðja fljótt um frí og skoða upplýsingar um frístöðu sína í Microsoft Teams. Starsmenn geta haft samband við þjarka til að óska eftir upplýsingum. Finna má ítarlegri upplýsingar á flipanum **Frí**. Að auki er hægt að senda fólki upplýsingar um væntanlegan frítíma í hópum og spjalli utan Human Resources.

![Human Resources Teams þjarkaforrit fyrir leyfi.](./media/hr-teams-leave-app-bot.png)

![Fríflipi fyrir frítímaforrit Human Resources Teams.](./media/hr-teams-leave-app-timeoff-tab.png)

![Leyfisbeiðnispjald Human Resources.](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a>Setja upp

Hægt er að finna Dynamics 365 Human Resources forritið í Teams versluninni. Frekari upplýsingar um uppsetningu á Teams-forritinu má finna í [Stjórna leyfisbeiðnum í Teams](hr-teams-leave-app.md).

Frekari upplýsingar um stjórnun forritsheimilda í Teams er að finna í [Stjórna reglum forritaheimilda í Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).

Ef notendur eiga að skoða Leyfis- og fjarvistadagatal í forritinu þarf að virkja **Leyfis- og fjarvistadagatal í Teams** í eiginleikastjórnun. Frekari upplýsingar um virkjun eiginleika er að finna í [Vinna með eiginleika](hr-admin-manage-features.md).

## <a name="update-app"></a>Uppfærðu app
>[!NOTE]
> Frá og með 20. desember 2021 verður þjónusta mannauðsapps sem hýst er hjá Microsoft leigjanda tekin úr notkun. Það mun engin áhrif hafa fyrir uppfærða viðbót (útgáfa 1.1.5) sem er tiltæk til uppsetningar. Helstu áhrifin verða á gamaldags framlengingu (útgáfa 1.1.4). Spjallbotninn í þessari útgáfu mun hætta að virka. The **Frí** flipinn mun halda áfram að virka í báðum viðbótunum.

Fyrir útgáfu 1.1.4 mun spjallbotninn hætta að svara öllum skilaboðum. Til dæmis, **skrá inn**, **stöður**, og **Sjá frí**. Forritið verður að vera handvirkt uppfært í nýjustu útgáfuna. Fyrir frekari upplýsingar, sjá [Uppfærðu öpp í Microsoft Teams](/MicrosoftTeams/apps-update-experience).

Til að uppfæra í útgáfu 1.1.5 skaltu ljúka þessum skrefum:
1. Í Microsoft Teams, fara til **Forrit**.
2. Finndu **Mannauður** app.
3. Veldu **Uppfærsla**.

Þú getur athugað útgáfuna af Human Resources appinu með því annað hvort að fara í **Um** flipann eða með því að fara í **Persónulegt app** kafla. 

![Mannauður **Um** flipinn.](./media/HR-teams-about.png)

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a>Kveikja á tilkynningum fyrir forritið „Human Resources“ í Teams

Ef notendur eiga að fá tilkynningar vegna leyfisbeiðna í Teams-forritinu verður að virkja tilkynningar í Dynamics 365 Human Resources.

>[!NOTE]
>Aðeins notendur sem eru skráðir inn í Teams og nota Dynamics 365 Human Resources Teams-forritið fá tilkynningar.

1. Veldu í Human Resources **Kerfisstjórnun**.

2. Veljið **Tenglar**.

3. Undir **Uppsetning**, skal velja **Kerfisfæribreytur**.

4. Á flipanum **Almennt** skal stilla **Kveikja á tilkynningum fyrir Teams-forritið** á **Já**.

   ![Kveikja á tilkynningum fyrir Teams-forrit í kerfisfæribreytum.](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. Til að kveikja á tilkynningum Teams fyrir alla notendur skal velja **Já** þegar spurt er um það.

   ![Virkja Teams-tilkynningar fyrir alla notendur.](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a>Kveikja eða slökkva á hóptilkynningum fyrir einstaka notendur

Þegar búið er að virkja tilkynningar fyrir Dynamics 365 Human Resources Teams forritið er hægt að kveikja eða slökkva á tilkynningum fyrir einstaka notendur.

1. Veldu í Human Resources **Kerfisstjórnun**.

2. Veljið **Tenglar**.

3. Undir **Notendur** skal velja **Notandavalkostir**.

4. Veldu flipann **Verkflæði**.

5. Stillið **Kveikja á tilkynningum fyrir Teams-forritið** á **Já** til að virkja tilkynningar fyrir notandann eða **Nei** til að gera tilkynningar óvirkar fyrir notandann.

   ![Kveikja á tilkynningum Teams-forrits á verkflæðisflipanum Valkostir notanda.](./media/hr-admin-teams-leave-app-notifications.png)

6. Veldu **Vista**.

## <a name="supported-languages"></a>Studd tungumál

Forritið Dynamics 365 Human Resources í Teams styður eftirfarandi tungumál:

| Landstaðalskenni | Tungumál |
| --- | --- |
| de-DE | Þýska (Þýskaland) |
| es-ES | Spænska (Spánn) |
| es-MX | Spænska (Mexíkó) |
| fr-CA | franska (Kanada) |
| fr-FR | Franska (Frakkland) |
| it-IT | Ítalska (Ítalía) |
| nl-NL | Hollenska (Holland) |
| pt-BR | Portúgalska (Brasilía) |
| tr-TR | Tyrkneska (Tyrkland) |
| zh-CN | kínverska (einfölduð) |

## <a name="notes"></a>Athugasemdir

Eftirfarandi vinnuliðir eru áætlaðir í síðari útgáfum:

| Vinnuliður | Staða |
| --- | --- |
| Staðan er röng þegar sendur er frítími fyrir dagsetningu í framtíðinni. | Spár eru ekki enn til staðar. Staðan birtist fyrir núverandi dagsetningu. |
| Ekki er hægt að hætta við beiðni með stöðuna **Í yfirferð**. | Þessi eiginleiki er ekki studdur eins og er og honum verður bætt við í síðari tíma útgáfum. |
| Upplýsingar um stöðu eru reiknaðar frá og með deginum í dag. | Kerfið sýnir ekki stöður eins og er á uppsöfnunartímabilinu, jafnvel þótt það sé stillt á **Orlofs- og fjarvistarfæribreytur** síðu. |

## <a name="troubleshooting"></a>Úrræðaleit

Ef notandi á í vandræðum með að skrá sig inn í eða nota forritið Human Resources Teams skal reyna að fylgja þessum leiðbeiningum úrræðaleitar. Ef þú átt enn í vandræðum eftir úrræðaleit skaltu hafa samband við notendaþjónustu. Frekari upplýsingar er að finna í [Fá stuðning](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

### <a name="ensure-the-teams-human-resources-application-is-up-to-date"></a>Gakktu úr skugga um að Teams Human Resources umsóknin sé uppfærð
Ef þú lendir í vandræðum með Teams Human Resources appið þarftu að staðfesta að þú sért að keyra nýjustu útgáfuna. Lágmarks studd útgáfa er 1.1.5. Fyrir leiðbeiningar um hvernig á að uppfæra Teams forrit, sjá [skjöl liðanna](/MicrosoftTeams/apps-update-experience).

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>Ekki er hægta að skrá inn í forritið „Human Resources“ í Teams

Ef notandi hefur samband við þig vegna þess að hann vill skrá sig inn í forritið, skaltu sannprófa að hann sé með tengda starfsmannafærslu í Human Resources.

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>Villa þegar leyfisbeiðnir eru samþykktar í forriti Human Resources í Teams

Ef notandi fær villu á meðan hann er að reyna að samþykkja leyfisbeiðnir í Teams appinu skaltu prófa eftirfarandi úrræðaleitarskref:

1. Gangið úr skugga um að Teams-reikningurinn sé sá sami og hann notar til að fá aðgang að Human Resources.

2. Gangið úr skugga um að hann sé gildur samþykktaraðili fyrir beiðnina með því að athuga stillingar verkflæðis fyrir samþykkt leyfis. Frekari upplýsingar um verkflæði leyfisbeiðna er að finna í [Búa til verkflæði leyfisbeiðni](hr-leave-and-absence-workflow.md).

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a>Samþykkisaðilar leyfis fá ekki spjallskilaboð úr Teams til að samþykkja leyfisbeiðnir

1. Gangið úr skugga um að tilkynningar séu virkar fyrir umhverfið og notandann. Frekari upplýsingar er að finna í [Virkja tilkynningar fyrir Human Resources-forritið í Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) og [Kveikja eða slökkva á tilkynningum Teams fyrir einstaka notendur](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).

2. Gangið úr skugga um að notendur séu skráði inn í flipann **Spjall** með sömu innskráningarupplýsingunum og þeir nota til að samþykkja leyfisbeiðnir. Notið skilaboðin „skrá út“ og síðan „skrá inn“ til að skrá inn með réttum innskráningarupplýsingum.

3. Ef vandamálið er viðvarandi skaltu athuga stöðuna á **Viðskiptaviðburðakerfi** hópvinna sem kerfisstjóri. Ef það er í a **Að bíða** eða **Framkvæmd** stigi, athugaðu aftur eftir nokkrar mínútur. Ef staðan helst óbreytt, skráðu þig stuðningsmiða svo að teymið okkar geti hjálpað til við að laga málið.

## <a name="privacy-notice"></a>Tilkynning um persónuvernd

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft Language Understanding Intelligent Service (LUIS)

Með Dynamics 365 Human Resources bot í Microsoft Teams, eru textainntak notandans greind til að skilja undirliggjandi fyrirspurn/tilgang. Inntak notandans eins og „Search account Contoso“ er beint til einnar af vitsmunaþjónustu Microsoft sem kallast Language Understanding Intelligent Service (LUIS). Lesa meira um LUIS  [hér](https://www.luis.ai/). LUIS-þjónustan ræður úr eða skilur ásetning notanda (í þessu tilviki er ætlunin að finna upplýsingar) og markeiningu (í þessu tilviki er tilgreinda einingin reikningur sem heitir Contoso). Þessar upplýsingar eru síðan sendar til Microsoft [Azure bot ramma](https://azure.microsoft.com/services/bot-service/), sem hefur samskipti við gögn frá Dynamics 365 Human Resources og sækir þær upplýsingar sem óskað er eftir fyrir notandafyrirspurnina.

Með því að setja upp og leyfa aðgang að þjarkanum samþykkir þú að leyfa LUIS-þjónustunni og Azure þjarkaramma að vinna úr ásetningi á bak við fyrirspurn, sem leiðir til betri notandaupplifunar. LUIS-þjónustan og Azure þjarkaramminn kunna að hafa mismikið samræmi samanborið við Dynamics 365 Human Resources. Þó að LUIS þjónustan hafi aðeins aðgang að notendafyrirspurnum og sé ekki hönnuð til að vera tengd við notandann Dynamics 365 Human Resources gögnum eða reikningi, notandi á Dynamics 365 Human Resources láni gæti sjálfviljugur slegið inn fyrirspurn sem inniheldur viðskiptavinagögn, persónuupplýsingar eða önnur gögn og slíkt fyrirspurnarefni gæti verið sent til LUIS þjónustunnar og Azure bot ramma. 

Innihald fyrirspurna og skilaboða notenda er varðveitt í LUIS kerfinu í að hámarki 30 daga, er dulkóðað í hvíld og er ekki notað til þjálfunar eða endurbóta á þjónustu. Lestu meira um Cognitive Services  [hér](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Til að stjórna stjórnandastillingum fyrir forrit í Microsoft Teams er farið í [Microsoft Teams stjórnendamiðstöð](https://admin.teams.microsoft.com/).

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>Microsoft Teams, hnitanet Azure-tilviks og Azure Cosmos DB

Þegar þú notar Dynamics 365 Human Resources app í Microsoft Teams, tiltekin gögn viðskiptavina gætu streymt út fyrir landfræðilega svæði þar sem starfsmannaþjónusta leigjanda þíns er notuð.

Dynamics 365 Human Resources sendir leyfisbeiðni starfsmanns og upplýsingar um verkflæðisverk til Microsoft Azure Viðburðarnet og Microsoft Teams. Þessi gögn má geyma í Microsoft Azure Event Grid í allt að sólarhring og verða unnin í Bandaríkjunum, þau er dulkóðuð í flutningi og í hvíld, og eru ekki notuð af Microsoft eða meðhöndlunaraðilum fyrir þjálfun eða þjónustuúrbætur. Til að skilja hvar gögnin þín eru geymd í Teams skaltu skoða: [Staðsetning gagna í Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).

Í samskiptum við spjallarann í forriti Human Resources, er hægt að geyma innihald samtalsins í Azure Cosmos DB og flytja það yfir í Microsoft Teams. Þessi gögn má geyma í Azure Cosmos DB í allt að sólarhring og kunna að vera meðhöndluð utan staðsetningarinnar þar sem Human Resources-þjónusta leigjandans er uppsett, þau er dulkóðuð í flutningi og í hvíld, og eru ekki notuð af Microsoft eða meðhöndlunaraðilum fyrir þjálfun eða þjónustuúrbætur. Til að skilja hvar gögnin þín eru geymd í Teams skaltu skoða: [Staðsetning gagna í Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).
 
Til að takmarka aðgang að Human Resources í Microsoft Teams fyrir fyrirtækið þitt eða notendur innan fyrirtækisins skal skoða [Stjórna reglum um forritsheimildir í Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).

## <a name="see-also"></a>Sjá einnig 

[Sækja og setja upp Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams hjálparmiðstöð](https://support.office.com/teams)</br>
[Stjórna leyfisbeiðnum í Teams](hr-teams-leave-app.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
