---
title: Tilvísunarkóðar fyrir villur greiðsluferilseininga
description: Þessi grein lýsir villutilvísunarkóðum fyrir greiðslueininguna sem eru sýndir í villuskilaboðum sem snúa að notendum í Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 10/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-09-20
ms.openlocfilehash: 952cb932522b4e0bb91be985e4f8974cb6cd8bc0
ms.sourcegitcommit: 435e69160dbd7f9c61b37ac4440285a5df144622
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728246"
---
# <a name="checkout-module-error-reference-codes"></a>Tilvísunarkóðar fyrir villur greiðsluferilseininga

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Þessi grein lýsir villukóðum afgreiðslueiningarinnar sem eru sýndir í villuskilaboðum sem snúa að notendum í Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce hefur innleitt staðlaðar villutilvísanir sem hægt er að taka með í stöðvunarvillum á netinu sem eru kynntar viðskiptavinum á netinu. Í Commerce útgáfu 10.0.31 og síðar innihalda villuboð í afgreiðslueiningunni villukóða og sýna ekki óþarfa upplýsingar til netviðskiptavinarins. Villukóðarnir vísa til villna sem lýst er í þessari grein.

Það fer eftir villunni sem kemur upp, taflan í þessari grein inniheldur eftirfarandi upplýsingar:

- Lýsing á ástandinu sem olli villunni, eða frekari upplýsingar
- Upplýsingar til athugunar í umhverfinu eða stillingum greiðslutengja
- Upplýsingar sem hægt er að vísa til í stuðningsmáli ef þörf er á frekari aðstoð

## <a name="prerequisites"></a>Forkröfur

Til að virkja villutilvísunarkóða fyrir greiðslueininguna sem taldir eru upp hér að neðan, í vefsvæðisgerð fyrir síðuna þína, farðu á **Vefstillingar \> Framlengingar**, og í **Körfu og kassa** kafla, veldu **Virkjaðu endurbætt netrásarvilluskjáskilaboð**. 

## <a name="checkout-module-error-reference-codes"></a>Tilvísunarkóðar fyrir villur greiðsluferilseininga

Notaðu eftirfarandi töflu til að fá frekari upplýsingar um tilvísanir í villukóða sem eru veittar af viðskiptavinum eða reynslu í netversluninni. Skrunaðu til hægri til að skoða **Villulýsing** dálki.

| Villukóði | Dynamics-fylgni villukóði | Villulýsing |
| ---------- | ------------------------------ | ----------------- |
| CCR001     | Microsoft\_ Dynamics\_ Verslun\_ Runtime\_ UnableToAuthorizePaymentCardTypeMissingOrNotSupported | Ekki var hægt að heimila greiðsluna. Kortategund auðkenni í **TokenizedPaymentCard** vantar, eða auðkenni kortategundar sem gefið er upp er ekki stutt. |
| CCR002     | Microsoft\_ Dynamics\_ Verslun\_ Runtime\_ UnableToAuthorizePayment | Afþakkaði. Ekki var hægt að heimila greiðsluna. |
| CCR003     | Microsoft\_ Dynamics\_ Verslun\_ Runtime\_ UnableToAuthorizePaymentCardAdditionalContextRequired | Ekki var hægt að heimila greiðsluna. Viðbótarupplýsingar krafist frá viðskiptavini. |
| CCR004     | Microsoft\_ Dynamics\_ Verslun\_ Runtime\_ UnableToRetrieveCardPaymentAcceptResult | Því miður fór eitthvað úrskeiðis. Við gátum ekki fengið niðurstöðuna fyrir samþykki korta. Reyndu aftur eða hafðu samband við kerfisstjórann þinn. |
| CCR005     | Microsoft\_ Dynamics\_ Verslun\_ Runtime\_ Greiðsla Krefst Merchant Properties | Ekki er hægt að greiða vegna greiðslueiginleika söluaðila. Hafðu samband við kerfisstjórann þinn. |
| CCR006     | Microsoft\_ Dynamics\_ Verslun\_ Runtime\_ Ógild greiðslubeiðni | Ekki tókst að sækja útboðsþjónustu fyrir reksturinn. Athugaðu uppsetningu greiðslumáta fyrir þá útboðstegund sem valin er. |
| CCR007     | Microsoft\_ Dynamics\_ Verslun\_ Runtime\_ Margar viðskiptavinareikningsgreiðslur ekki leyfðar | Þegar hefur verið beitt greiðslu viðskiptavinareiknings og aðeins ein greiðsla er leyfð á hverja færslu. |
| CCR008     | Microsoft\_ Dynamics\_ Verslun\_ Runtime\_ ViðskiptavinareikningstakmörkSign MismunandiFráUpphæð | Takmark viðskiptavinareiknings er frábrugðið upphæðinni sem gjaldfallið er. Prófaðu annan greiðslumáta eða hafðu samband við þjónustuver til að fá aðstoð. |
| CCR009     | Microsoft\_ Dynamics\_ Verslun\_ Runtime\_ Greiðsla viðskiptavinareiknings fer yfir heildarupphæð fyrir að bera út og skila hlutum | Greiðsla viðskiptavinareiknings fer yfir heildargjalddaga fyrir skráða hluti. Reyndu aftur síðar eða hafðu samband við þjónustuver til að fá aðstoð. |
| CCR010     | Microsoft\_ Dynamics\_ Verslun\_ Runtime\_ Greiðsla UsingUautorized Account | Greiðsla viðskiptavinareiknings krefst eigin reiknings eða samsvarandi reikningsreiknings á tilboðslínu. |
| CCR011     | Microsoft\_ Dynamics\_ Verslun\_ Runtime\_ Greiðsla viðskiptavinareiknings fer yfir Gólftakmark viðskiptavinareiknings | Ekki er hægt að vinna úr greiðslu inn á viðskiptavinalykil eins og er – lágmarkinu hefur verið náð. |
| CCR012     | Microsoft\_ Dynamics\_ Verslun\_ Runtime\_ Viðskiptavinareikningur Greiðsla Fyrir Viðskiptavin Án LeyfisÁReikningi | Þessi viðskiptavinur hefur ekki leyfi til að greiða inn á reikning. |
| CCR013     | Microsoft\_ Dynamics\_ Verslun\_ Runtime\_ UnableToCancelPayment | Því miður fór eitthvað úrskeiðis. Ekki var hægt að hætta við greiðsluna. Reyndu aftur. |
| CCR014     | Microsoft\_ Dynamics\_ Verslun\_ Runtime\_ UnableToReadCardTokenInfo | Villa kom upp við vinnslu greiðslunnar. Reyndu aftur seinna. |
| CCR015     | Microsoft\_ Dynamics\_ Verslun\_ Runtime\_ NotEnoughRewardPoints | Upphæð vildargreiðslu er hærri en leyfilegt er fyrir vildarkortið sem notað er í þessari færslu. |
| CCR016     | Microsoft\_ Dynamics\_ Verslun\_ Runtime\_ EndurgreiðslaMeiraEn Leyfð | Upphæð vildarendurgreiðslu er hærri en leyfilegt er fyrir vildarkortið sem notað er í þessum viðskiptum. |
| CCR017     | Microsoft\_ Dynamics\_ Verslun\_ Runtime\_ Ógilt LoyaltyCardNumber | Vildarkortsnúmer fannst ekki. Annað hvort virkjaðu vildarkortanúmerið eða sláðu inn annað kortanúmer og reyndu svo aftur. |
| CCR018     | Microsoft\_ Dynamics\_ Verslun\_ Runtime\_ Lokað Loyalty Card | Vildarkortanúmerið er ekki tiltækt. Sláðu inn annað kortanúmer og reyndu svo aftur. |
| CCR019     | Microsoft\_ Dynamics\_ Verslun\_ Runtime\_ NoTenderLoyaltyCard | Þetta vildarkort er ekki gjaldgengt til að innleysa vildarpunkta fyrir þessa færslu. |
| CCR020     | Microsoft\_ Dynamics\_ Verslun\_ Runtime\_ GiftCardCurrency Mismatch | Villa kom upp í gjafakortsnúmerinu. Prófaðu annað gjafakort eða hafðu samband við þjónustuver til að fá aðstoð. |
| CCR021     | Microsoft\_ Dynamics\_ Verslun\_ Runtime\_ PaymentAmountExceedsGiftBalance | Upphæðin fer yfir stöðuna á gjafakortinu. Sláðu inn aðra upphæð og reyndu svo aftur. |
| CCR022     | Microsoft\_ Dynamics\_ Verslun\_ Runtime\_ NoMoreThanOneLoyaltyTender | Færslan getur ekki innihaldið fleiri en eina vildargreiðslulínu. |
| CCR023     | Microsoft\_ Dynamics\_ Verslun\_ Runtime\_ Greiðsla þegar ógild | Greiðsluupplýsingarnar vantar ýmist upplýsingar eða eru rangar. Staðfestu greiðsluupplýsingarnar og reyndu svo aftur. |
| CCR024     | Microsoft\_ Dynamics\_ Verslun\_ Runtime\_ Svikahætta | Ekki er hægt að vinna úr pöntuninni að svo stöddu. Reyndu aftur seinna. |
| CCR025     | Front End Timeout fyrir Checkout API | Aðgerð framenda hefur runnið út. Staðfestu hvort pöntunin hafi verið afgreidd í Dynamics 365 Commerce höfuðstöðvar. |
| CCR026     | Upprunalega heimildarupphæð breytt | Pöntunarupphæðin hefur breyst frá upphaflegri heimildarupphæð sem unnin var með greiðslugáttinni. Þetta kann að vera vegna tímasetts útrunnar afsláttarmiða, kynningar eða sölu. |
| CCR027     | Microsoft\_ Dynamics\_ Verslun\_ Runtime\_ InvalidCartVersion | Villa kom upp við vinnslu greiðslu. Tilvísunin sem gefin er upp í körfu-API hefur aðra tilvísun en búist var við (tekið eftir hugsanlegu ósamræmi við greiðsluferlið). |
| CCR028     | Microsoft\_ Dynamics\_ Verslun\_ Runtime\_ MissingRequiredCartTenderLines | Villa kom upp við greiðslumátann sem reynt var. Hafðu samband við þjónustudeild til að fara yfir reikningsstillingarnar þínar eða reyndu aftur með öðrum greiðslumáta. |

## <a name="additional-resources"></a>Frekari upplýsingar

[Algengar spurningar um greiðslur](dev-itpro/payments-retail.md)

[Greiðsluferliseining](add-checkout-module.md)

[Greiðslueining](payment-module.md)
