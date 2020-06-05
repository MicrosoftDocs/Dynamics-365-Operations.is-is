---
title: Stjórna leyfisbeiðnum í Teams
description: Þetta efnisatriði sýnir hvernig á að biðja um frí í Dynamics 365 Human Resources forritinu í Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 67501a1fa65493a1a23eb6176ece5be98d6e4659
ms.sourcegitcommit: 7fc0726c0a93ce6f4dafaad3232b4687f61cdc88
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/21/2020
ms.locfileid: "3393009"
---
# <a name="manage-leave-requests-in-teams"></a>Stjórna leyfisbeiðnum í Teams

[!include [banner](includes/preview-feature.md)]

Microsoft Dynamics 365 Human Resources -forritið í Microsoft Teams gerir þér kleift að biðja um frí og skoða upplýsingar um stöðu frítíma í Microsoft Teams. Hægt er að hafa samband við þjarka til að óska eftir upplýsingum. Finna má ítarlegri upplýsingar á flipanum **Frí**.

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

> [!WARNING]
> Forritið styður ekki öryggishlutverk kerfisstjóra og sýnir villuboð ef þú skráir þig inn með kerfisstjórareikningi. Þegar skrá á inn með öðrum reikningi skal, á flipanum **Stillingar**, velja hnappinn **Skipta um reikning** og skrá inn með notandareikningi sem er ekki með kerfisstjóraréttindi.
 
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
 
Eftir að beiðni um leyfi er hafin er hægt að leiðrétta dagana innan spjaldsins eða velja **Breyta upplýsingum** til að bæta viðbótarupplýsingum við beiðnina.

![Breytingabeiðni Human Resources Teams-forrits fyrir leyfi](./media/hr-teams-leave-app-bot-edit.png)
 
Þegar búið er að færa inn upplýsingar skal slá inn **Senda** til að senda hana til samþykkis. Einnig er hægt að slá inn **Vista sem drög** til að gera þetta síðar.

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
   
## <a name="privacy-notice"></a>Tilkynning um persónuvernd

Með Dynamics 365 Human Resources þjarkanum í Microsoft Teams er texti notanda greindur til að skilja undirliggjandi fyrirspurn/ásetning. Inntak notanda á borð við „Leita í contoso reikningi“ er flutt í eina af Cognitive Service hjá Microsoft sem kallast LUIS (Language Understanding Intelligent Service). Lesa meira um LUIS  [hér](https://www.luis.ai/). LUIS-þjónustan ræður úr eða skilur ásetning notanda (í þessu tilviki er ætlunin að finna upplýsingar) og markeiningu (í þessu tilviki er tilgreinda einingin reikningur sem heitir Contoso). Þessar upplýsingar eru svo sendar í Microsoft  [Azure þjarkaramma](https://azure.microsoft.com/services/bot-service/) sem vinnur með gögn úr Dynamics 365 Human Resources og sækir æskilegar upplýsingum fyrir fyrirspurn notanda. 

Með því að setja upp og leyfa aðgang að þjarkanum samþykkir þú að leyfa LUIS-þjónustunni og Azure þjarkaramma að vinna úr ásetningi á bak við fyrirspurn, sem leiðir til betri notandaupplifunar. LUIS-þjónustan og Azure þjarkaramminn kunna að hafa mismikið samræmi samanborið við Dynamics 365 Human Resources. LUIS-þjónustan hefur aðeins aðgang að fyrirspurnum notenda og er ekki hönnuð til að tengjast við Dynamics 365 Human Resources gögn eða reikning. Notandi Dynamics 365 Human Resources þjarkans gæti fært inn fyrirspurn sem inniheldur gögn viðskiptavinar, persónuleg gögn eða önnur gögn og slíkt fyrirspurnarefni gæti verið sent til LUIS-þjónustunnar og Azure þjarkarammans. 

Innihald fyrirspurna og skilaboða notanda er vistað í LUIS-kerfi í að hámarki 30 daga, er dulkóðað þegar ekki í notkun og er ekki notað fyrir þjálfun eða endurbætur á þjónustu. Lestu meira um Cognitive Services  [hér](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Til að stjórna stjórnandastillingum fyrir forrit í Microsoft Teams er farið í [Microsoft Teams stjórnendamiðstöð](https://admin.teams.microsoft.com/). 

## <a name="see-also"></a>Sjá einnig

[Sækja og setja upp Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams hjálparmiðstöð](https://support.office.com/teams)</br>
[Forritið „Human Resources“ í Teams](hr-admin-teams-leave-app.md)
