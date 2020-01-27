---
title: Reikningsstjórnunarsíður og -einingar
description: Þetta efni fjallar um reikningsstjórnunarsíður og -einingar í Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: f9fc3731cd9d21294b0161e1d419f255096d7790
ms.sourcegitcommit: 96bfc20eb748f4090a2b5e1ff9f54997d5a5d359
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/04/2019
ms.locfileid: "2885810"
---
# <a name="account-management-pages-and-modules"></a>Reikningsstjórnunarsíður og -einingar

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Þetta efni fjallar um reikningsstjórnunarsíður og -einingar í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Með stjórnun reikninga er átt við hóp síðna sem notaðar eru til að stjórna upplýsingum sem tengjast notendareikningi í Dynamics 365 Commerce. Reikningsstjórnunarsíður innihalda lendingasíðu reikningsstjórnunar, notandaforstillingasíðu, notendasíðu, síðu pöntunarferils, pöntunarupplýsingasíðu, vildarsíðu og óskalistasíðu.

### <a name="account-management-landing-page"></a>Lendingasíða fyrir stjórnun reikninga

Lendingasíða reikningsstjórnunar notar eftirfarandi einingar:

- **Staðsetning efnis** - Þessi eining er gámaeining sem geymir allar einingar á lendingasíðu reikningsstjórnunar.
- **Móttökuskilaboð reiknings** - Þessi eining er notuð til að veita móttökuskilaboð á reikningssíðu. Hún felur í sér eiginleika fyrir fyrirsögnina og reitastærðina. Eiginleikinn **Reitastærð** skilgreinir breidd einingarinnar í staðsetningareiningu efnis. Gildin eru frá **1** til **12**, þar sem **12** táknar alla breidd staðsetningargáms efnisins.
- **Staðsetningarliður reikningspöntunar** - Þessi eining er notuð til að gefa yfirlit yfir fjölda pantana sem hafa verið gerðar af notendareikningnum. Hún felur í sér eiginleika fyrir fyrirsögnina, reitastærðina og tengilinn „Skoða upplýsingar“. Stilla ætti tengilinn „skoða upplýsingar“ til að framsenda á pöntunarferilsíðuna.
- **Staðsetningarliður reikningsforstillinga** - Þessi eining er notuð til að gefa yfirlit yfir notandaforstillingarnar. Hún felur í sér eiginleika fyrir fyrirsögnina, reitastærðina og tengilinn „Skoða upplýsingar“. Stilla ætti tengilinn „skoða upplýsingar“ til að framsenda á notandaforstillingasíðuna.
- **Óskalistaliður reiknings** - Þessi eining er notuð til að gefa yfirlit yfir hluti á óskalista viðskiptavinar. Til dæmis gæti hann fullyrt: „Þú ert með 10 atriði á óskalistanum þínum.“ Hún felur í sér eiginleika fyrir fyrirsögnina, reitastærðina og tengilinn „Skoða upplýsingar“. Stilla ætti tengilinn „skoða upplýsingar“ til að framsenda á óskalistasíðuna.
- **Netfangaliður reiknings** - Þessi eining er notuð til að gefa yfirlit yfir netföng notandans. Til dæmis gæti hún fullyrt: „Þú ert með 2 netföng bætt við reikninginn þinn.“ Hún felur í sér eiginleika fyrir fyrirsögnina, reitastærðina og tengilinn „Skoða upplýsingar“. Stilla ætti tengilinn „skoða upplýsingar“ til að framsenda á notandanetfangasíðuna.
- **Vildaratriði reiknings** - Þessi eining er notuð til að sýna og tengjast upplýsingum um vildarkerfi. Hún felur í sér eiginleika fyrir fyrirsögnina, reitastærðina, tengilinn „Skoða upplýsingar“ og tengilinn „Gerast meðlimur“. Stilla ætti tengilinn „skoða upplýsingar“ til að framsenda á vildarkerfissíðuna. Stilla ætti tengilinn „gerast meðlimur“ til að framsenda á síðu þar sem notendur geta tekið þátt í vildarkerfinu.

### <a name="order-history-page"></a>Pöntunarferilssíða

Pöntunarferilsíðan notar pöntunarferilseininguna til að sýna allar nýlegar pantanir sem notandinn hefur sett inn.

### <a name="order-details-page"></a>Upplýsingasíða pöntunar

Pöntunarupplýsingasíðan veitir ítarlegar upplýsingar um hverja pöntun og má nálgast af pöntunarferilssíðunni. Það notar pöntunarupplýsingaeininguna, sem krefst sölukennis eða færslukennis til að sækja pöntunarupplýsingarnar.

### <a name="user-profile-page"></a>Notandaforstillingasíða

Notandaforstillingasíðan sýnir upplýsingar um notandareikning, svo sem nafn notanda og netfang. Hún notar notandaforstillingaeininguna. Þrátt fyrir að ekki sé hægt að fjarlægja netfangið er hægt að breyta því. Notandasniðssíðan sýnir einnig óskir notenda sem gera notanda kleift að velja eða afþakka ákveðna eiginleika eins og að sérsníða meðmælalista. 

### <a name="user-address-page"></a>Netfangssíða notanda

Netfangasíða notanda sýnir lista yfir netföng sem tengjast notendareikningnum. Notandinn gaf þessi netföng annaðhvort upp í greiðsluferlinu eða bætti þeim beint við á þessari síðu. Notendanetfangareiningin er notuð til að bæta við og breyta netföngum, stilla aðalnetfangið og láta núverandi netföng birtast á síðunni.

### <a name="wish-list-page"></a>Óskalistasíða

Óskalistasíðan sýnir atriðin sem hefur verið bætt við óskalista viðskiptavinar. Hún notar óskalistaeininguna til að birta atriði óskalista.

### <a name="loyalty-page"></a>Síða vildarkerfis

Vildarkerfissíðan gerir viðskiptavinum kleift að ganga í vildarkerfi eða, ef þeir eru nú þegar meðlimir í vildarkerfi, skoða upplýsingar um kerfið«». Þeir geta einnig skoðað stigin sem þeir hafa unnið og innleyst í nýlegum færslum.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit byrjendaeiningar](starter-kit-overview.md)

[Hólfeining](add-container-module.md)

[Kaupkassaeining](add-buy-box.md)

[Körfueining](add-cart-module.md)

[Greiðsluferliseining](add-checkout-module.md)

[Pöntunarstaðfestingareining](order-confirmation-module.md)

[Fyrirsagnareining](author-header-module.md)

[Neðanmálseining](author-footer-module.md)
