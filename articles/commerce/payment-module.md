---
title: Greiðslueining
description: Þetta efnisatriði fjallar um greiðslueininguna og útskýrir hvernig á að skilgreina hana í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 4267391edaf70ec645933b2c5c08a72735f52894
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818327"
---
# <a name="payment-module"></a>Greiðslueining

[!include [banner](includes/banner.md)]

Þetta efnisatriði fjallar um greiðslueininguna og útskýrir hvernig á að skilgreina hana í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Greiðslueiningin gerir viðskiptavinum kleift að greiða pantanir með kredit- eða debetkortum. Greiðslusamþætting fyrir þessa eining er í boði greiðslutengils Dynamics 365 fyrir Adyen. Frekari upplýsingar um hvernig setja á upp og skilgreina greiðslutengil er að finna í [Greiðslutengill Dynamics 365 fyrir Adyen](dev-itpro/adyen-connector.md).

Greiðslueiningin hýsir greiðsluupplýsingar sem er miðlað í gegnum Adyen í innfelldum HTML-ramma (iframe). Greiðslueiningin vinnur með Commerce Scale Unit til að sækja Adyen-greiðsluupplýsingar. Sem hluti af samvinnu Commerce Scale Unit, getur greiðslueiningin leyft upplýsingar um reikningsaðsetur að vera sett fram annaðhvort í iframe eða aðskilinni einingu. Í Fabrikam-þemanu er reikningsaðsetrið sýnt í aðskilinni einingu. Þessi nálgun býður upp á meiri sveigjanleika fyrir sniðmótun, því að hægt er að sýna línur aðsetursins þannig að þær líkist línum afhendingaraðsetursins.

Greiðslueiningin leyfir einnig innskráðum viðskiptavinum að vista greiðsluupplýsingarnar sínar. Greiðsluupplýsingar og reikningsaðsetur eru vistuð og stjórnað í gegnum Adyen-greiðslutengilinn.

Greiðslueiningin nær yfir öll pöntunargjöld sem vildarpunktar eða gjafakort ná ekki þegar yfir. Ef samtala fyrir pöntun er að fullu dekkuð af vildarpunktum eða inneign gjafakorts, verður greiðslueiningin falin, og viðskiptavinurinn mun geta lagt inn pöntunina án hennar.

Adyen-greiðslutengillinn styður einnig öfluga sannvottun viðskiptavinar (SCA). Hluti af greiðsluþjónustutilskipun 2.0 (PSD2.0) Evrópusambandsins krefst þess að kaupendur á netinu verði auðkenndir utan umhverfis netverslunarinnar þegar þeir nota rafrænan greiðslumáta. Meðan á greiðsluferlinu stendur, er viðskiptavinum vísað á bankaþjónustusvæðið þeirra. Eftir sannvottun er þeim beint aftur í greiðsluferli Commerce. Á meðan á þessari framsendingu stendur verða upplýsingar sem viðskiptavinur færði inn í greiðsluferlið (til dæmis sendingaraðsetur, afhendingarvalkostir, upplýsingar um gjafakort og vildarupplýsingar) haldið við. Áður en hægt er að kveikja á þessum eiginleika verður að skilgreina greiðslutengilinn fyrir öfluga sannvottun viðskiptavinar í Commerce Headquarters. Frekari upplýsingar er að finna í [Öflug sannvottun viðskiptavinar með Adyen](adyen_redirect.md).

Eftirfarandi skýringarmynd sýnir dæmi um einingar gjafakorts, vildarpunkta og greiðslu á greiðsluferlissíðu.

![Dæmi um gjafakort, vildarpunkta og greiðslueiningar á greiðsluferlissíðu](./media/ecommerce-payments.PNG)

## <a name="payment-module-properties"></a>Eiginleikar greiðslueiningar

| Nafn eiginleika | Gildi | lýsing |
|---------------|--------|-------------|
| Fyrirsögn | Fyrirsagnartexti | Valfrjáls fyrirsögn fyrir greiðslueininguna. |
| Hæð iFrame | Dílar | Hæð iframe í dílum. Hægt er að stilla hæðina eftir þörfum. |
| Sýna greiðsluaðsetur | **Satt** eða **Ósatt** | Ef þessi eiginleiki er stilltur á **Satt** verður reikningsaðsetrið lagt fram af Adyen innan iframe greiðslueiningarinnar. Ef hann er stilltur á **Ósatt** verður reikningsaðsetrið ekki lagt fram af Adyen og notandi Commerce verður að skilgreina einingu til að sýna reikningsaðsetrið greiðsluferlissíðunni. |
| Hnekkja greiðslustíl | Kóði fyrir stölluð stílblöð (CSS) | Vegna þess að greiðslueiningin er hýst í iframe, er takmarkaður möguleiki á stílmótun. Hægt er að ná einhverri stílmótun með því að nota þennan eiginleika. Til að hnekkja stílbrigðum svæðis þarf að líma CSS-kóðann inn sem gildið fyrir þennan eiginleika. Hnekkingar og stílbrigði CSS-svæðissmiðs eiga ekki við um þessa einingu. |

## <a name="billing-address"></a>Póstfang greiðanda

Greiðslueiningin gerir viðskiptavinum kleift að bjóða upp á reikningsaðsetur vegna greiðsluupplýsinganna. Hún gerir þeim einnig kleift að nota sendingaraðsetur sitt sem reikningsaðsetur, til að gera greiðsluferlið auðveldara og fljótlegra. Ef eiginleikinn **Sýna reikningsaðsetur** er stilltur á **Ósatt** ætti að skilgreina greiðslueininguna á greiðsluferlissíðunni.

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a>Bæta greiðslueiningu við greiðsluferlissíðu og stilla nauðsynlega eiginleika

Aðeins er hægt að bæta greiðslueiningu við greiðsluferliseiningu. Frekari upplýsingar um hvernig á að skilgreina greiðslueiningu fyrir greiðsluferlissíðu er að finna í [Greiðsluferliseining](add-checkout-module.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Körfueining](add-cart-module.md)

[Körfutáknseining](cart-icon-module.md)

[Greiðsluferliseining](add-checkout-module.md)

[Eining sendingaraðseturs](ship-address-module.md)

[Eining afhendingarvalkosta](delivery-options-module.md)

[Pöntunarupplýsingaeining](order-confirmation-module.md)

[Gjafakortseining](add-giftcard.md)

[Dynamics 365-greiðslutengill fyrir Adyen](dev-itpro/adyen-connector.md)

[Öflug sannvottun viðskiptavinar með Adyen](adyen_redirect.md)
