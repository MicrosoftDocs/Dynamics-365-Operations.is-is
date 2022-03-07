---
title: Vinna ótengdar endurgreiðslur með Dynamics 365 Commerce Payment Connector fyrir Adyen
description: Þetta efnisatriði lýsir hvernig aftengdar endurgreiðslur virka þegar Microsoft Dynamics 365 Payment Connector fyrir Adyen er notaður.
author: BrianShook
ms.date: 10/07/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: BrShoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: c137dcf7d35031a293c88d8c4f5dc1e5f3d9e2f9
ms.sourcegitcommit: a21a664cd35b95c8600c5af0aac588a64e892902
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/11/2021
ms.locfileid: "7623922"
---
# <a name="process-unlinked-refunds-with-the-dynamics-365-commerce-payment-connector-for-adyen"></a>Vinna ótengdar endurgreiðslur með Dynamics 365 Commerce Payment Connector fyrir Adyen

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir hvernig aftengdar endurgreiðslur virka þegar [Microsoft Dynamics 365 Payment Connector fyrir Adyen](adyen-connector.md) er notaður. Það yfirfer einnig getu til að vinna endurgreiðslu gegn nýjum greiðslumátum á sölustað eða í símaveri.

Dynamics 365 Payment Connector fyrir Adyen styður getuna til að vinna endurgreiðslur með því að nota annan greiðslumáta en var notaður fyrir upprunalegu færsluna. Þótt við mælum með að nota [tengdar endurgreiðslur](linked-refunds.md) til að vinna endurgreiðslu gegn upprunalegum greiðslumáta sem var veittur þarf við sumar aðstæður að endurgreiða á annan greiðslumáta. Til dæmis gæti kortið sem var notað fyrir upprunalegu greiðsluna verið útrunnið eða týnt, eða notandi kann að hafa lokað því.

## <a name="prerequisites"></a>Forkröfur

Eftirfarandi skilyrði þarf að ljúka áður en Dynamics 365 Payment Connector fyrir Adyen getur unnið úr ótengdum endurgreiðslum:

- Setja upp [greiðslumáta](../payment-methods.md).
- Setja upp [greiðslur á omni-rás](../omni-channel-payments.md).

## <a name="additional-configuration"></a>Viðbótargrunnstillingar

Dynamics 365 Payment Connector fyrir Adyen býður upp á tilbúna innleiðingu á öllum studdum endurgreiðsluaðstæðum sem lýst er í næsta hluta. Viðskiptavinir sem ekki nota tilbúnu innleiðinguna í Dynamics 365 Payment Connector fyrir Adyen verða að setja tengilinn upp sem styður tákngerð kreditkorta.

## <a name="supported-refund-scenarios"></a>Studdar endurgreiðsluaðstæður

Dynamics 365 Commerce styður endurgreiðslur á færslum sem áður voru samþykktar og staðfestar. Endurgreiðslur geta verið annaðhvort full endurgreiðsla eða endurgreiðsla að hluta til af færslunni. Endurgreiðslur mega ekki vera hærri en sem nemur upphaflegri greiðsluheimild. Ótengdar endurgreiðslur eru aðeins studdar á sölustað og í símaveri.

## <a name="enable-unlinked-refunds-functionality"></a>Virkja virkni ótengdra endurgreiðslna

Fylgja skal eftirfarandi skrefum til að virkja aftengdar endurgreiðslur í Commerce Headquarters.

1. Opnið **Retail og Commerce \> Uppsetning höfuðstöðva \> Færibreytur \> Samnýttar færibreytur Commerce**.
1. Á flipanum **Greiðslur á omni-rás** skal stilla valkostinn **Nota greiðslur á omni-rás** á **Já**.

### <a name="supported-payment-method-variants"></a>Studd afbrigði greiðslumáta

Eftirfarandi afbrigði greiðslumáta styðja ótengdar endurgreiðslur út úr kassanum:

- Kort
- Veski

Ekki öll afbrigði greiðslumáta styðja ótengdar endurgreiðslur. Eftirfarandi tafla veitir lista yfir algenga greiðslumáta og sýnir stuðningsgetu hvers máta fyrir tengdar og ótengdar endurgreiðslur.

| Greiðslumáti        | Tengd endurgreiðsla | Ótengd endurgreiðsla |
|-----------------------|:-------------:|:---------------:|
| amexcommercial        | Já           | Já             |
| amexconsumer          | Já           | Já             |
| amexcorporate         | Já           | Já             |
| amexdebit             | Já           | Já             |
| amexprepaid           | Já           | Já             |
| amexprepaidreloadable | Já           | Já             |
| amexsmallbusiness     | Já           | Já             |
| uppgötvaðu              | Já           | Já             |
| maestro               | Já           | Já             |
| maestrouk             | Já           | Já             |
| mc                    | Já           | Já             |
| mcalphabankbonus      | Já           | Já             |
| mcprepaidanonymous    | Já           | Já             |
| vegabréfsáritun                  | Já           | Já             |
| visaalphabankbonus    | Já           | Já             |
| visacheckout          | Já           | Já             |
| visadankort           | Já           | Já             |
| visahipotecario       | Já           | Já             |
| visasaraivacard       | Já           | Já             |
| vpay                  | Já           | Já             |
| givex                 | **Nei**        | Já             |
| svs                   | **Nei**        | Já             |
| bolli                   | Já           | Já             |
| diners                | Já           | Já             |
| interac               | **Nei**        | Já             |
| jcb                   | Já           | Já             |
| jcb_applepay          | Já           | Já             |
| unionpay              | Já           | Já             |

### <a name="process-an-unlinked-refund-in-pos"></a>Vinna úr ótengdri endurgreiðslu á sölustað

Viðskiptavinur skilar vöru til gjaldkera á sölustað innan leyfilegs tímabils fyrir skil og er með gilda kvittun. Við úrvinnslu skilanna inniheldur svarglugginn **Skilagreiðsla** valkostinn **Velja greiðslumáta**. Gjaldkerinn velur síðan greiðslumáta úr studdum greiðslumátum fyrir endurgreiðslu (kort og veski).

### <a name="process-an-unlinked-refund-in-call-center"></a>Vinna úr ótengdri endurgreiðslu í símaveri

Þegar ótengd endurgreiðsla er unnin gegn pöntun í símaveri velur starfsmaður í símaveri greiðslumáta sem er annar en upprunalegi greiðslumátinn. Starfsmaðurinn er síðan beðinn um að gefa upp PIN-númer fyrir hnekkingu stjórnanda. PIN-númersins er krafist áður en hægt er að vinna annan greiðslumáta fyrir endurgreiðsluna.

#### <a name="set-up-an-administrator-override-pin-for-call-center"></a>Setja upp PIN-númer fyrir hnekkingu stjórnanda fyrir símaver

Til að setja upp PIN-númer fyrir hnekkingu stjórnanda fyrir símaver í Commerce Headquarters skal fylgja þessum skrefum.

1. Farðu í **Smásala og viðskipti \> Uppsetning rásar \> Uppsetning símavers** eða leitaðu að „Hnekkja heimildir“.
1. Veldu hlutverk sem leyfir vinnslu á ótengdum endurgreiðslum.
1. Á flýtiflipanum **Skil** skal stilla valkostinn **Leyfa aðra greiðslu** á **Já**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Dynamics 365 Payment Connector fyrir Adyen](adyen-connector.md)

[Tengdar endurgreiðslur á áður samþykktum og staðfestum færslum](linked-refunds.md)
