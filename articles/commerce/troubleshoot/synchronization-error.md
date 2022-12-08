---
title: Ósamstilltur pöntunarsamstillingarvandamál
description: Þessi grein lýsir algengum ástæðum fyrir bilun í ósamstilltri pöntunargerð í Microsoft Dynamics 365 Commerce og gefur upp úrræðaleitarskref til að hjálpa kerfisnotendum og samstarfsaðilum að skilja hvað fór úrskeiðis.
author: Shajain
ms.date: 11/30/2022
ms.topic: Troubleshooting
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.openlocfilehash: 27bccced3c07149fe1842524660447a49f86f3fc
ms.sourcegitcommit: 2804b05214c87f76457608b5db072582ff339852
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 12/01/2022
ms.locfileid: "9815757"
---
# <a name="asynchronous-order-synchronization-issues"></a>Ósamstilltur pöntunarsamstillingarvandamál

[!include [banner](../../includes/banner.md)]

Þessi grein lýsir algengum ástæðum fyrir bilun í ósamstilltri pöntunargerð í Microsoft Dynamics 365 Commerce og gefur upp úrræðaleitarskref til að hjálpa kerfisnotendum og samstarfsaðilum að skilja hvað fór úrskeiðis.

## <a name="symptom"></a>Einkenni

Ósamstilltar pantanir sem eru búnar til úr Dynamics 365 Commerce rafrænum viðskiptum eða sölustað (POS) endurspeglast ekki í höfuðstöðvum Commerce.

## <a name="troubleshooting"></a>Úrræðaleit

Pöntunargerð getur mistekist í höfuðstöðvum af mismunandi ástæðum, allt eftir því á hvaða stigi pöntunargerðin mistekst. Eftirfarandi bilanaleitarskref fara í gegnum mögulegar rót orsakir.

### <a name="validate-that-the-transaction-related-to-the-asynchronous-order-has-reached-headquarters"></a>Staðfestu að færslan sem tengist ósamstilltu pöntuninni hafi náð til höfuðstöðva

Fyrir pantanir í rafrænum viðskiptum, í höfuðstöðvum, farðu í **Smásölu og verslun \> Fyrirspurnir og skýrslur \> Viðskipti á netinu**. Ef þú ert með staðfestingarnúmer fyrir pöntunina skaltu sía færslurnar með því að slá inn staðfestingarnúmerið í **Rás tilvísunarkenni** reitinn. Ef þú ert ekki með staðfestingarnúmerið skaltu sía færslurnar með því að slá inn reikningsnúmer viðskiptavinarins.

Fyrir POS pantanir, opnaðu **Verslunarfærslur** síðuna og síaðu færslurnar eftir kvittunarnúmeri eða reikningsnúmeri viðskiptavinar. Ef færslan finnst ekki skaltu keyra verkið **P-0001** rásarfærslur, sem samstillir viðskipti frá rásum við höfuðstöðvar. Ef **P-0001** starfið mistekst, opnaðu stuðningsmiða fyrir verkið. Ef **P-0001** starfið tekst, en færslurnar birtast samt ekki í höfuðstöðvum, opnaðu stuðningsmiða sem inniheldur viðeigandi upplýsingar.
 
### <a name="check-the-synchronization-status-if-the-transaction-is-present-in-headquarters-but-isnt-linked-with-a-sales-order"></a>Athugaðu samstillingarstöðu ef færslan er til staðar í höfuðstöðvum en er ekki tengd við sölupöntun

Ef færslan er til staðar í höfuðstöðvum en sölupöntunin hefur ekki verið búin til skaltu opna **Netverslunarfærslur** síðuna og velja **Samstillingu staða** Hraðflipi. Ef verkið **Samstilla pantanir** reyndi að samstilla þessa færslu ætti reiturinn **Staða pöntunar í bið** að sýna stöðuna **Tókst** eða **Tókst ekki**. Ef staðan er **Tókst**, verður sölupöntunarreiturinn að vera til staðar á þessari færslu. Ef staðan er **Mistókst**, geturðu skoðað villuupplýsingarnar í **Pöntunarvilluupplýsingum** reitnum á flipanum **Staða samstillingar**. Ef hvorug þessara staða er sýnd hefur engin tilraun verið gerð til að vinna úr færslunni. Í þessu tilviki geturðu valið **Samstilla röð**  efst á síðunni til að keyra samstillingarvinnuna.

Gakktu úr skugga um að verkið **Samstilla pantanir**  sé áætlað að keyra reglulega, þannig að hægt sé að búa til ósamstilltar færslur sem pantanir í höfuðstöðvum.

Eftirfarandi hlutar veita upplýsingar um nokkrar algengar villur og lagfæringar á þeim.

#### <a name="the-order-error-details-field-shows-the-following-error-message-number-sequence-has-been-exceeded"></a>Reiturinn Upplýsingar um pöntunarvillu sýnir eftirfarandi villuboð: „Farið hefur verið yfir númeraröð“

Númeraraðir eru notaðar til að búa til sölupantanir í höfuðstöðvum. Ef allar tölur sem eru leyfðar fyrir númeraröð eru uppurnar myndar kerfið þessi villuboð. Númeraröðina sem er notuð til að búa til sölupantanir er að finna á **Færibreytur viðskiptakrafna \> Númeraraðir \> Sölupöntun**. Til að laga þessa villu skaltu laga núverandi númeraröð eða skipta um hana fyrir nýja númeraröð.

#### <a name="the-order-error-details-field-shows-the-following-error-message-there-must-be-a-default-payment-service-to-process-credit-card-transactions"></a>Reiturinn Pantunarvilluupplýsingar sýnir eftirfarandi villuboð: "Það verður að vera sjálfgefin greiðsluþjónusta til að vinna úr kreditkortafærslum"

Til að laga þessa villu skaltu staðfesta að sjálfgefna greiðsla sé skilgreind í höfuðstöðvum. Ef engin sjálfgefna greiðsla er skilgreind verður þú að skilgreina eina. Farðu í **Viðskiptakröfur \> Greiðsluuppsetning \> Greiðsluþjónusta**, og gakktu úr skugga um að **Sjálfgefinn örgjörvi fyrir ný kreditkort** valkosturinn sé stilltur á **Já** fyrir eina greiðsluþjónustu.
    
#### <a name="the-order-error-details-field-shows-an-account-structure-error-message"></a>Reiturinn Upplýsingar um pöntunarvillu sýnir villuskilaboð reikningsuppbyggingar

Texti villuskilaboðanna fyrir uppbyggingu reiknings getur verið breytilegur eins og eftirfarandi dæmi sýna. Hins vegar deila villunum sameiginlegri grunnorsök sem tengist uppsetningu reikningsskipulagsins.

- "Bætingarniðurstöður fyrir lotunúmer dagbókar 0009656328 Skírteini ARP-000959899 1.00 fyrir skírteini ARP-000959899 í usrt fyrirtækis verður bókað sem ofgreiðsla eða vangreiðsla"
- "Birtunarniðurstöður fyrir lotunúmer dagbókar 0009656328 Skírteini ARP-000959899 Skírteini ARP-000959901 Reikningsuppbygging, fyrir samsetninguna 618160, er ekki gild fyrir höfuðbók Corporate Main Account Shared"
- "Bæta niðurstöður fyrir lotunúmer dagbókar 0009656328 Skírteini ARP-000959899 Skírteini ARP-000959901 Tilkynnt frá fyrirtækjareikningum usrt"
- "Birtunarniðurstöður fyrir lotunúmer dagbókar 0009656328 Skírteini ARP-000959899 Hætt hefur verið við færslu"
    
Til að laga þessar villur skaltu skoða reikningsuppbygginguna til að fá nákvæmni. Frekari upplýsingar má finna í [Skilgreina lykilskipulög](/dynamics365/finance/general-ledger/configure-account-structures).
    
Eftir að villan hefur verið lagfærð skaltu velja færsluna sem mistókst og síðan **Samstilla pöntun** efst á síðunni til að keyra samstillingarverkið.
    
#### <a name="other-types-of-errors-that-might-require-the-transaction-data-to-be-fixed"></a>Aðrar tegundir villna sem gætu þurft að laga færslugögnin

Til að laga aðrar tegundir villna sem gætu krafist þess að færslugögnin séu lagfærð, geturðu notað „breyta og endurskoða færslur“ möguleikann. Frekari upplýsingar má finna í [Breyta og endurskoða færslur](../edit-order-trans.md).
