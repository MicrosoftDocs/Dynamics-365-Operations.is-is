---
title: Stjórna leyfisbeiðnum í Teams
description: Þessi grein sýnir hvernig á að biðja um frí í Dynamics 365 Human Resources appinu í Microsoft Teams.
author: twheeloc
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 84f1190301e67b49535530f85784561b2e51a2df
ms.sourcegitcommit: 3aa3dedc3123cb079614762e2718841c2f7d7d35
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/30/2022
ms.locfileid: "9812161"
---
# <a name="manage-leave-requests-in-teams"></a>Stjórna leyfisbeiðnum í Teams

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources -forritið í Microsoft Teams gerir þér kleift að biðja um frí og skoða upplýsingar um stöðu frítíma í Microsoft Teams. Hægt er að eiga samskipti við þjarka til að óska eftir upplýsingum og byrja leyfisbeiðni. Finna má ítarlegri upplýsingar á flipanum **Frí**. Einnig er hægt að senda fólki upplýsingar um væntanlegan frítíma í hópum og spjalli utan Human Resources.

## <a name="install-the-app"></a>Setja upp forritið

Hægt er að finna Dynamics 365 Human Resources forritið í Teams versluninni.

1. Í Microsoft Teams skal fara á lista yfir forrit.
 
2. Leitið að Dynamics 365 Human Resources og veljið síðan reitinn **Human Resources**.

> [!NOTE]
> Frá og með 20. desember 2021 verður þjónusta mannauðsappabotna (útgáfa 1.1.4) sem hýst er hjá Microsoft leigjanda tekin úr notkun. Nýjustu viðbótin (útgáfa 1.1.5) er fáanleg til uppsetningar. Fyrir frekari upplýsingar, sjá [Stjórna leyfisbeiðnum í Teams](hr-admin-teams-leave-app.md#update-app).

3. Veljið hnappinn **Bæta við** til að setja upp forritið.

Ef forritið skráir þig ekki sjálfkrafa inn skaltu velja flipann **Stillingar** til að skrá þig inn.

> [!NOTE]
> Ef þú sérð ekki innskráningarglugga skaltu uppfæra stillingar vafrans til að leyfa sprettiglugga. 

Ef þú hefur aðgang að fleiri en einu tilviki af Human Resources er hægt að velja hvaða umhverfi á að tengja við á flipanum **Stillingar**.

> [!NOTE]
> Forritið styður nú öryggishlutverk kerfisstjóra.
 
## <a name="use-the-bot"></a>Nota þjarkann

Þegar forritið hefur verið sett upp birtast boð með upplýsingar um þær aðgerðir sem þjarkinn getur gripið til.

> [!NOTE]
> Þegar þú hefur fyrst samskipti við vélmanninn gætirðu þurft að skrá þig inn. Ef þú sérð ekki innskráningarglugga skaltu uppfæra stillingar vafrans til að leyfa sprettiglugga.

Hægt er að spyrja þjarkann um að:

- Skoða núgildandi leyfisstöðu þína. Til dæmis er hægt að senda skilaboð sem segja „Skoða leyfisstöður“.

- Hefja leyfisbeiðni fyrir notanda. Sendu til dæmis skilaboð sem segja: „Taktu frí“ eða „Ég vil taka frí næsta fimmtudag og föstudag“ til að vera nákvæmari fyrir beiðni um leyfi fyrir orlofstegundina. 

  ![Hefja beiðni um leyfi í Teams-spjalli.](./media/hr-teams-leave-app-initiate.png)

- Spjallarinn mun fylla út leyfibeiðni fyrir þig. Veljið **Biðja um frí** til að biðja um og breyta upplýsingum um beiðnina.

   Ef óskað er eftir að senda inn leyfisbeiðnir fyrir margar leyfisgerðir fyrir sömu dagsetninguna skal velja valkostinn **Degi skipt með** í valmyndinni **Fleiri valkostir**. 

   Ef þú velur leyfi í hálfan dag þegar eining leyfisbeiðni er í dögum er hægt að tilgreina hvort beðið sé um frí fyrri hluta dags eða þann seinni með því að velja valkostinn **Skilgreining á hálfum degi** í valmyndinni **Fleiri valkostir**.
   
   ![Skilgreiningar hálfs dags.](./media/HalfDayDefinitions.png)

- Þegar búið er að breyta upplýsingunum um leyfisbeiðni skal velja **Senda** til að senda þær til samþykkis.

  ![Senda inn leyfisbeiðni.](./media/hr-teams-leave-app-submit.png)

## <a name="manage-your-leave-in-teams"></a>Stjórna leyfi í Teams

Flipinn **Frí** býður upp á skoðun: 

- Stöðuupplýsingar fyrir hverjar leyfisgerðir sem þú ert skráð(ur) í

- Næstu leyfisbeiðnir

- Beiðnir um frítíma

- Drög að leyfisbeiðnum
 
### <a name="create-a-new-request"></a>Búa til nýja beiðni

1. Til að stofna nýja leyfisbeiðni skal velja **Ný beiðni**.

2. Sláðu inn daginn eða dagana þar sem þú vilt taka frí og veldu svo **Bæta við**.

   ![Bæta við fríi Human Resources Teams-forriti fyrir leyfi.](./media/TimeOffHours.png)

3. Slá inn ástæðukóða, ef við á. Einnig skal færa inn athugasemdir og bæta við viðhengjum.

4. Veljið valkostinn **Degi skipt með** úr valmyndinni **Fleiri valkostir** ef ætlunin er að senda inn margar færslur leyfisbeiðni fyrir sama daginn fyrir mismunandi leyfisgerðir.

5. Veljið valkostinn **Skilgreining á hálfum degi** til að tilgreina hvort ætlunin sé að biðja um frí fyrri hluta dags eða seinni hluta dags. Þessi valkostur er í boði þegar eining leyfisbeiðni er í dögum og upphæðin sem beðið er um er 0,5 dagar.

6. Þegar upplýsingar hafa verið færðar inn skal ýta á **Senda inn** til að senda þetta inn til samþykktar. Einnig er hægt að færa inn **Vista sem drög** til að koma aftur síðar.

### <a name="manage-draft-requests"></a>Stjórna dragabeiðnum

1. Veljið flipann **Drög**.

2. Veldu blýantinn til að breyta beiðninni eða ruslið til að eyða henni.

3. Gerið nauðsynlegar breytingar. Þegar búið er að færa inn upplýsingar skal slá inn **Senda** til að senda hana til samþykkis. Einnig er hægt að velja **Vista sem drög** til að gera þetta síðar.
   
### <a name="respond-to-teams-notifications"></a>Bregðast við tilkynningum Teams

Þegar þú eða starfsmaður sem þú ert samþykkjandi fyrir sendir inn orlofsbeiðni færðu tilkynningu í Human Resources appinu í Teams. Þú getur valið tilkynninguna til að skoða leyfisbeiðnina. Tilkynningar birtast einnig á svæðinu **Spjall**.

Ef notandi er samþykkjandi er hægt að velja **Samþykkja** eða **Neita** í tilkynningunni. Einnig er hægt að búa til valfrjáls skilaboð.

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a>Sendu upplýsingar um komandi frí til vinnufélaga þinna

Eftir að Human Resources er sett upp fyrir Teams er auðveldlega hægt að senda upplýsingar um væntanlegt frí til samstarfsfólks í hópum og spjalli.

1. Í hópi eða spjalli í Teams skal velja hnapp Human Resources fyrir neðan spjallgluggann.

   ![Hnappur Human Resources fyrir neðan spjallglugga.](./media/hr-teams-leave-app-chat-button.png)

2. Veljið leyfisbeiðnina sem á að deila. Ef óskað er eftir að deila drögum að leyfisbeiðni skal byrja á því að velja **Drög**.

Leyfisbeiðnin mun birtast í spjallinu.

Ef drög að beiðni var deilt mun þau birtast sem drög.

## <a name="view-your-teams-leave-calendar"></a>Skoða frídagatal teymisins

Ef þú ert yfirmaður með beina undirmenn getur þú skoðað samþykkt frí hópsins þíns og frí í bið.

1. Í forritinu „Human Resources“ í Teams skal velja **Frí**.

2. Veldu **Team dagatal**. Dagatalið birtir samþykkt frí og frí í bið fyrir beina undirmenn þína.

   > [!NOTE]
   > Ef ekki er hægt að sjá hópdagatalið skal biðja kerfisstjóra um að virkja það. Frekari upplýsingar eru í [Setja upp](hr-admin-teams-leave-app.md#install-and-setup).

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
| tr-TR | Tyrkneska (Türkiye) |
| zh-CN | kínverska (einfölduð) |

## <a name="troubleshooting"></a>Úrræðaleit

Ef þú átt í vandræðum með að skrá þig inn í eða nota forritið Human Dynamics 365 Human Resources skaltu reyna að fylgja þessum leiðbeiningum úrræðaleitar. Ef þú átt enn í vandræðum eftir úrræðaleit skaltu hafa samband við notendaþjónustu. Frekari upplýsingar er að finna í [Fá stuðning](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>Ekki er hægta að skrá inn í forritið „Human Resources“ í Teams

Ef þú getur ekki skráð þig inn í forritið er hugsanlegt að reikningurinn sem þú notar til að skrá þig inn í Microsoft Teams sé ekki tengdur við starfsmannafærslu í Dynamics 365 Human Resources. Hafa skal samskipti við kerfisstjóra til að tryggja að starfsmannafærslan sé rétt tengd.

### <a name="cant-find-the-dynamics-365-human-resources-environment-in-settings"></a>Finn ekki Dynamics 365 Human Resources umhverfið í stillingum

Ef þú getur ekki valið rétt Dynamics 365 umhverfi gæti verið að notandafærslan hafi ekki verið rétt samstillt. Hafa skal samband við kerfisstjóra til að stofna notandafærsluna aftur og tengja hana við innskráningarupplýsingar notanda. Reyndu svo að skrá þig inn forrit Human Resources fyrir Microsoft Teams nokkrum mínútum síðar.

### <a name="translations-dont-display-correctly"></a>Þýðingar birtast ekki rétt

Ef þýðingar birtast ekki eins og búist er við skal ganga úr skugga um tungumálið sem var valið í Teams passi við valið tungumál í **Valkostum notanda** í Human Resources.

Í Teams skal skoða **Tungumál forrits** í **Stillingum**.

![Teams-stillingar.](./media/hr-teams-leave-app-settings.png)

Í Human Resources skal velja **Stillingar** og síðan velja **Valkostir notanda**. Gangið úr skugga um að reiturinn **Tungumál** samsvari reitnum **Tungumál forrits** í Teams.

![Valkostir notanda í Human Resources.](./media/hr-teams-leave-app-user-options.png)

Láttu okkur vita ef vandamál vegna þýðinga er enn til staðar. Fyrir upplýsingar, sjá [Fáðu stuðning fyrir fjármála- og rekstraröpp eða Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>Villa þegar leyfisbeiðnir eru samþykktar í forriti Human Resources í Teams

Ef villa kemur upp þegar verið er að reyna að samþykkja leyfisbeiðnir í Teams, skal prófa að fara í gegnum eftirfarandi villuleitarskref:

1. Gangið úr skugga um að reikningurinn sem er notaður til að skrá sig inn í Microsoft Teams sé sá sami og notaður er til að fá aðgang að Dynamics 365 Human Resources.

2. Vertu viss um að þú sért gildur samþykktaraðili fyrir beiðnina með því að athuga stillingar verkflæðis fyrir samþykkt leyfis. Frekari upplýsingar um verkflæði leyfisbeiðna er að finna í [Búa til verkflæði leyfisbeiðni](hr-leave-and-absence-workflow.md).

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a>Samþykkisaðilar leyfis fá ekki spjallskilaboð úr Teams til að samþykkja leyfisbeiðnir

1. Gangið úr skugga um að tilkynningar séu virkar fyrir umhverfið og notandann. Frekari upplýsingar er að finna í [Virkja tilkynningar fyrir Human Resources-forritið í Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) og [Kveikja eða slökkva á tilkynningum Teams fyrir einstaka notendur](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).

2. Gangið úr skugga um að notendur séu skráði inn í flipann **Spjall** með sömu innskráningarupplýsingunum og þeir nota til að samþykkja leyfisbeiðnir. Notið skilaboðin „skrá út“ og síðan „skrá inn“ til að skrá inn með réttum innskráningarupplýsingum.

3. Ef vandamálið er viðvarandi skaltu athuga stöðu **Business Events kerfisins** runuvinnslunnar sem kerfisstjóri. Ef það er í **Bið** eða **Í keyrslu** stigi skaltu athuga aftur eftir nokkrar mínútur. Ef staðan helst óbreytt, skráðu þig stuðningsmiða svo að teymið okkar geti hjálpað til við að laga málið.

## <a name="known-accessibility-issues"></a>Þekkta aðgengisvandamál

Human Resources-forritið í Teams er með eftirfarandi aðgengisvandamál sem við vinnum að lagfæringum á í síðari útgáfum.

| Úthreyfing | Hjáleið eða skýring |
| --- | --- |
| Ef 400% aðdráttur er notaður á skjáborði eru sumir aðgerðahnappar ekki sýnilegir. | Mælt er með því að notað sé stækkunargler þar til við styðjum þennan aðdrátt. |
| Á flipanum **Tímafrí** tilkynnir talsetning hnappaaðgerð á meðan hún les hausinn fyrir frítímanetið. | Hausinn og þættirnir í hnitanetinu eru flokkaðir eftir árum og þeir eru hægt að fella saman. Voiceover túlkar þessa kynningu sem verklegt atriði, en það er það ekki. |
| Á flipanum **Frí** er aukaleg strokhreyfing þegar verið er að fletta að **Ástæðukóði** í nýrri beiðni. | Engin falin stjórnun er til staðar sem storkufletting er að reyna að ná til. |
| Á flipanum **Frí**, ef strokið á meðan dagatalið er opið, er endað utan stýringar í stað upphafs nýrrar beiðni eða þegar beiðni er breytt. | Þegar komið er að **Fara á daginn í dag** er það síðasti hlutinn og strokið er í öfuga átt til að komast aftur efst. |
| Á flipanum **Spjall** er farið aftur á toppinn þegar dagsetningin er slegin inn á meðan verið er að nota hjálpartækið eða lyklaborðið. | Flipi þar til þú nærð innsláttarsvæðinu aftur. |

## <a name="privacy-notice"></a>Tilkynning um persónuvernd

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft Language Understanding Intelligent Service (LUIS)

Með Dynamics 365 Human Resources þjarkanum í Microsoft Teams, eru textainnsláttur notandans greindur til að skilja undirliggjandi fyrirspurn/tilgang. Inntak notandans eins og „Search account Contoso“ er beint til einnar af hugrænu þjónustu Microsoft sem kallast Language Understanding Intelligent Service (LUIS). Lesa meira um LUIS  [hér](https://www.luis.ai/). LUIS-þjónustan ræður úr eða skilur ásetning notanda (í þessu tilviki er ætlunin að finna upplýsingar) og markeiningu (í þessu tilviki er tilgreinda einingin reikningur sem heitir Contoso). Þessar upplýsingar eru síðan sendar til Microsoft Teams Azure bot framework [frá Microsoft, sem hefur samskipti við gögn frá](https://azure.microsoft.com/services/bot-service/) og sækir þær upplýsingar sem óskað er eftir fyrir notendafyrirspurnina. 

Með því að setja upp og leyfa aðgang að þjarkanum samþykkir þú að leyfa LUIS-þjónustunni og Azure þjarkaramma að vinna úr ásetningi á bak við fyrirspurn, sem leiðir til betri notandaupplifunar. LUIS-þjónustan og Azure þjarkaramminn kunna að hafa mismikið samræmi samanborið við Dynamics 365 Human Resources. Þó að LUIS þjónustan hafi aðeins aðgang að notendafyrirspurnunum og sé ekki hönnuð til að vera tengd við Dynamics 365 Human Resources gögnum eða reikningi notandans, gæti notandi Dynamics 365 Human Resources botans sjálfviljugur slegið inn fyrirspurn sem inniheldur Viðskiptavinagögn, persónuupplýsingar eða önnur gögn og slíkt fyrirspurnarefni gætu verið send til LUIS þjónustunnar og Azure bot ramma. 

Innihald fyrirspurna og skilaboða notanda er varðveitt í LUIS kerfinu í að hámarki 30 daga, er dulkóðað í hvíld og er ekki notað til þjálfunar eða endurbóta á þjónustu. Lestu meira um Cognitive Services  [hér](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Til að stjórna stjórnandastillingum fyrir forrit í Microsoft Teams er farið í [Microsoft Teams stjórnendamiðstöð](https://admin.teams.microsoft.com/).

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>Microsoft Teams, hnitanet Azure-tilviks og Azure Cosmos DB

Þegar  Dynamics 365 Human Resources appið er notað í Dynamics 365 Human Resources  gætu ákveðin viðskiptavinagögn streymt út fyrir landfræðilega svæðið þar sem mannauðsþjónusta leigjanda þíns er notuð.

 Microsoft Teams sendir leyfisbeiðni starfsmanns og upplýsingar um verkflæðisverk til Dynamics 365 Human Resources Event Grid og Microsoft Azure . Þessi gögn má geyma í Microsoft Azure Event Grid í allt að sólarhring og verða unnin í Bandaríkjunum, þau er dulkóðuð í flutningi og í hvíld, og eru ekki notuð af Microsoft eða meðhöndlunaraðilum fyrir þjálfun eða þjónustuúrbætur. Til að skilja hvar gögnin þín eru geymd í Teams skaltu skoða: [Staðsetning gagna í Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).

Í samskiptum við spjallarann í forriti Human Resources, er hægt að geyma innihald samtalsins í Azure Cosmos DB og flytja það yfir í Microsoft Teams. Þessi gögn má geyma í Azure Cosmos DB í allt að sólarhring og kunna að vera meðhöndluð utan staðsetningarinnar þar sem Human Resources-þjónusta leigjandans er uppsett, þau er dulkóðuð í flutningi og í hvíld, og eru ekki notuð af Microsoft eða meðhöndlunaraðilum fyrir þjálfun eða þjónustuúrbætur. Til að skilja hvar gögnin þín eru geymd í Teams skaltu skoða: [Staðsetning gagna í Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).
 
Til að takmarka aðgang að Human Resources í Microsoft Teams fyrir fyrirtækið þitt eða notendur innan fyrirtækisins skal skoða [Stjórna reglum um forritsheimildir í Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).

## <a name="see-also"></a>Sjá einnig

[Sækja og setja upp Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams hjálparmiðstöð](https://support.office.com/teams)</br>
[Forritið „Human Resources“ í Teams](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

