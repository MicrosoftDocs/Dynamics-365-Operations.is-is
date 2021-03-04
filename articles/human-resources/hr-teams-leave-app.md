---
title: Stjórna leyfisbeiðnum í Teams
description: Þetta efnisatriði sýnir hvernig á að biðja um frí í Dynamics 365 Human Resources forritinu í Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d24c257054578282f1a2eafa050094194a358aa0
ms.sourcegitcommit: 369639cd92e03fe792ed9d61a329d842aafa052f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/29/2020
ms.locfileid: "4419110"
---
# <a name="manage-leave-requests-in-teams"></a>Stjórna leyfisbeiðnum í Teams

[!include [banner](includes/preview-feature.md)]

Microsoft Dynamics 365 Human Resources -forritið í Microsoft Teams gerir þér kleift að biðja um frí og skoða upplýsingar um stöðu frítíma í Microsoft Teams. Hægt er að eiga samskipti við þjarka til að óska eftir upplýsingum og byrja leyfisbeiðni. Finna má ítarlegri upplýsingar á flipanum **Frí**. Einnig er hægt að senda fólki upplýsingar um væntanlegan frítíma í hópum og spjalli utan Human Resources.

## <a name="install-the-app"></a>Setja upp forritið

Hægt er að finna forritið Human Resources í Teams versluninni.

1. Í Microsoft Teams skal velja sporbauginn.

   ![Sporbaugur fyrir Human Resources Teams-forrit fyrir leyfi](./media/hr-teams-leave-app-ellipses.png)
 
2. Leitið að Dynamics 365 Human Resources og veljið síðan reitinn **Human Resources**.

   ![Human Resources-spjald fyrir Human Resources Teams-forrit fyrir leyfi](./media/hr-teams-leave-app-human-resources-tile.png)

3. Veljið hnappinn **Bæta við** til að setja upp forritið.

   ![Uppsetning Human Resources Teams-forrits fyrir leyfi](./media/hr-teams-leave-app-in-store.png)

Ef forritið skráir þig ekki sjálfkrafa inn skaltu velja flipann **Stillingar** til að skrá þig inn.

![Stillingaflipi Human Resources Teams-forrits fyrir leyfi](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> Ef þú sérð ekki innskráningarglugga skaltu athuga vafrastillingarnar þínar til að leyfa sprettiglugga. 

Ef þú hefur aðgang að fleiri en einu tilviki af Human Resources er hægt að velja hvaða umhverfi á að tengja við á flipanum **Stillingar**.

> [!NOTE]
> Forritið styður nú öryggishlutverk kerfisstjóra.
 
## <a name="use-the-bot"></a>Nota þjarkann

Þegar forritið hefur verið sett upp birtast boð með upplýsingar um þær aðgerðir sem þjarkinn getur gripið til.

![Opnunarkveðja Human Resources Teams-þjarkaforrits fyrir leyfi](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> Hugsanlega þarf að skrá sig inn við fyrstu samskipti við þjarkann. Ef þú sérð ekki innskráningarglugga skaltu athuga vafrastillingarnar þínar til að leyfa sprettiglugga.

Hægt er að spyrja þjarkann um að:

- Sýna upplýsingar um stöðu frís fyrir hverja leyfisgerð sem notandi ert skráður í.

   ![Sýna stöður Human Resources Teams-forrits fyrir leyfi](./media/hr-teams-leave-app-bot-balances.png)
 
- Sýna frekari upplýsingar um tiltekna leyfisgerð.

   ![Sýna upplýsingar Human Resources Teams -forrits fyrir leyfi](./media/hr-teams-leave-app-bot-details.png)

- Hefja leyfisbeiðni fyrir notanda.

   ![Leyfisbeiðni fyrir Human Resources Teams-forrit fyrir leyfi](./media/hr-teams-leave-app-bot-request.png)
 
Eftir að beiðni um leyfi er hafin er hægt að leiðrétta dagana innan spjaldsins.

![Breytingabeiðni Human Resources Teams-forrits fyrir leyfi](./media/hr-teams-leave-app-bot-edit.png)
 
Þegar búið er að færa inn upplýsingar skal velja **Senda** til að senda þær til samþykkis. Einnig er hægt að velja **Vista sem drög** til að gera þetta síðar.

![Senda beiðni í Human Resources Teams-forriti fyrir leyfi](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a>Stjórna leyfi í Teams

Flipinn **Frí** býður upp á skoðun:

- Stöðuupplýsingar fyrir hverjar leyfisgerðir sem þú ert skráð(ur) í

- Næstu leyfisbeiðnir

- Fríbeiðnir

- Drög að leyfisbeiðnum

![Fríflipi fyrir fríforrit Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a>Búa til nýja beiðni

1. Til að stofna nýja leyfisbeiðni skal velja **Ný beiðni**.

   ![Ný beiðni fyrir Human Resources Teams-forrit fyrir leyfi](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. Sláðu inn daginn eða dagana þar sem þú vilt taka frí og veldu svo **Bæta við**.

   ![Bæta við fríi Human Resources Teams-forriti fyrir leyfi](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. Slá inn ástæðukóða, ef við á. Einnig skal færa inn athugasemdir og bæta við viðhengjum.

4. Þegar búið er að færa inn upplýsingar skal slá inn **Senda** til að senda hana til samþykkis. Einnig er hægt að slá inn **Vista sem drög** til að gera þetta síðar.

### <a name="manage-draft-requests"></a>Stjórna dragabeiðnum

1. Veljið flipann **Drög**.

   ![Dragaflipi í Human Resources Teams-forriti fyrir leyfi](./media/hr-teams-leave-app-drafts-tab.png)

2. Veldu blýantinn til að breyta beiðninni eða ruslið til að eyða henni.

3. Gerið nauðsynlegar breytingar. Þegar búið er að færa inn upplýsingar skal slá inn **Senda** til að senda hana til samþykkis. Einnig er hægt að velja **Vista sem drög** til að gera þetta síðar.

   ![Breyta drögum í Human Resources Teams-forriti fyrir leyfi](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a>Bregðast við tilkynningum Teams

Þegar þú eða starfskraftur sem þú ert samþykktaraðili fyrir sendir beiðni um leyfi fyrir færðu senda tilkynningu í Human Resources forritinu í Teams. Hægt er að velja tilkynninguna til að skoða hana. Tilkynningar birtast einnig á svæðinu **Spjall**.

Ef notandi er samþykkjandi er hægt að velja **Samþykkja** eða **Neita** í tilkynningunni. Einnig er hægt að búa til valfrjáls skilaboð.

![Senda beiðni um tilkynningar í forritinu Human Resources Teams](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a>Senda upplýsingar um væntanlegt frí til samstarfsfólks

Eftir að Human Resources er sett upp fyrir Teams er auðveldlega hægt að senda upplýsingar um væntanlegt frí til samstarfsfólks í hópum og spjalli.

1. Í hópi eða spjalli í Teams skal velja hnapp Human Resources fyrir neðan spjallgluggann.

   ![Hnappur Human Resources fyrir neðan spjallglugga](./media/hr-teams-leave-app-chat-button.png)

2. Veljið leyfisbeiðnina sem á að deila. Ef óskað er eftir að deila drögum að leyfisbeiðni skal byrja á því að velja **Drög**.

   ![Velja beiðni um væntanlegt frí til að deila](./media/hr-teams-leave-app-chat-search.png)

Leyfisbeiðnin mun birtast í spjallinu.

![Leyfisbeiðnispjald Human Resources](./media/hr-teams-leave-app-chat-card.png)

Ef drög að beiðni var deilt mun þau birtast sem drög:

![Drög að leyfisbeiðnispjaldi Human Resources](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a>Skoða frídagatal teymisins

Ef þú ert yfirmaður með beina undirmenn getur þú skoðað samþykkt frí hópsins þíns og frí í bið.

1. Í forritinu „Human Resources“ í Teams skal velja **Frí**.

2. Veldu **Team dagatal**.

   ![Skoða dagatal í Human Resources Teams-forriti](./media/hr-teams-leave-app-view-calendar.png)

Dagatalið birtir samþykkt frí og frí í bið fyrir beina undirmenn þína.

![Frítímadagatal í Human Resources Teams forriti](./media/hr-teams-leave-app-calendar.png)

## <a name="troubleshooting"></a>Úrræðaleit

Ef þú átt í vandræðum með að skrá þig inn í eða nota forritið Human Resources Teams skaltu reyna að fylgja þessum leiðbeiningum úrræðaleitar. Ef þú átt enn í vandræðum eftir úrræðaleit skaltu hafa samband við notendaþjónustu. Frekari upplýsingar er að finna í [Fá stuðning](hr-admin-troubleshooting-support.md).

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>Ekki er hægta að skrá inn í forritið „Human Resources“ í Teams

Ef þú getur ekki skráð þig inn í forritið er hugsanlegt að reikningurinn sem þú notar til að skrá þig inn í Microsoft Teams sé ekki tengdur við starfsmannafærslu í Dynamics 365 Human Resources. Hafa skal samskipti við kerfisstjóra til að tryggja að starfsmannafærslan sé rétt tengd.

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>Villa þegar leyfisbeiðnir eru samþykktar í forriti Human Resources í Teams

Ef villa kemur upp þegar verið er að reyna að samþykkja leyfisbeiðnir í Teams, skal prófa að fara í gegnum eftirfarandi villuleitarskref:

1. Gangið úr skugga um að reikningurinn sem er notaður til að skrá sig inn í Microsoft Teams sé sá sami og notaður er til að fá aðgang að Dynamics 365 Human Resources.

2. Vertu viss um að þú sért gildur samþykktaraðili fyrir beiðnina með því að athuga stillingar verkflæðis fyrir samþykkt leyfis. Frekari upplýsingar um verkflæði leyfisbeiðna er að finna í [Búa til verkflæði leyfisbeiðni](hr-leave-and-absence-workflow.md).

## <a name="known-accessibility-issues"></a>Þekkta aðgengisvandamál

Human Resources-forritið í Teams er með eftirfarandi aðgengisvandamál sem við vinnum að lagfæringum á í síðari útgáfum.

| Úthreyfing | Hjáleið eða skýring |
| --- | --- |
| Ef 400% aðdráttur er notaður á skjáborði eru sumir aðgerðahnappar ekki sýnilegir. | Mælt er með því að notað sé stækkunargler þar til við styðjum þennan aðdrátt. |
| Á flipanum **Frí** tilkynnir upplestur hnappaaðgerð þegar hausinn hnitanetsins er lesinn fyrir fríið. | Haus og einingar innan hnitanetsins eru flokkaðar eftir árum og eru samanfellanlegar. Upplestur skilur þetta sem aðgerðarhlut, sem það er ekki. |
| Ef strokið er þegar sprettigluggi eða valmynd er opin sleppir upplestur því að lesa efni sprettigluggans eða valmyndarinnar. | Skoðaðu efnið með fingraskönnun. |
| Á flipanum **Frí** er aukaleg strokhreyfing þegar verið er að fletta að **Ástæðukóði** í nýrri beiðni. | Engin falin stjórnun er til staðar sem storkufletting er að reyna að ná til. |
| Á flipanum **Frí**, ef strokið á meðan dagatalið er opið, er endað utan stýringar í stað upphafs nýrrar beiðni eða þegar beiðni er breytt. | Þegar komið er að **Fara á daginn í dag** er það síðasti hlutinn og strokið er í öfuga átt til að komast aftur efst. |
| Upplestur les ekki merkin fyrir dagsetningar. | Dagsetningarnar sem eru í pörum eru alltaf **Upphafsdagur** og **Lokadagur**. |
| Á flipanum **Spjall** er farið aftur á toppinn þegar dagsetningin er slegin inn á meðan verið er að nota hjálpartækið eða lyklaborðið. | Flipi þar til þú nærð innsláttarsvæðinu aftur. |

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
[Forritið „Human Resources“ í Teams](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]