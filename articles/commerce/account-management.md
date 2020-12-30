---
title: Reikningsstjórnunarsíður og -einingar
description: Þetta efni fjallar um reikningsstjórnunarsíður og -einingar í Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: b0f963bcf65ae622522fe52fd59996c6ec0ecf17
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413079"
---
# <a name="account-management-pages-and-modules"></a>Reikningsstjórnunarsíður og -einingar

[!include [banner](includes/banner.md)]

Þetta efni fjallar um reikningsstjórnunarsíður og -einingar í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Með stjórnun reikninga er átt við hóp síðna sem notaðar eru til að stjórna upplýsingum sem tengjast notendareikningi í Dynamics 365 Commerce. Reikningsstjórnunarsíður innihalda lendingasíðu reikningsstjórnunar, notandaforstillingasíðu, notendasíðu, síðu pöntunarferils, pöntunarupplýsingasíðu, vildarsíðu og óskalistasíðu.

### <a name="account-management-landing-page"></a>Lendingasíða fyrir stjórnun reikninga

Lendingasíða reikningsstjórnunar notar eftirfarandi einingar:

- **Gámur** - Allar lendingarsíðueiningar reikningsstjórnunar skulu settar í gám. 
- **Móttökureitur reiknings** - Þessi eining er notuð til að veita móttökuskilaboð á reikningssíðu. Hann felur í sér eiginleika fyrir fyrirsögnina.
- **Almennir reitir reiknings** - Þessa einingu er hægt að nota til að útvega fyrirsagnir og tengla á reikningastjórnarsíður, svo sem „Pöntunarferill“ eða „Prófíllinn minn“. Hægt er að nota almenna reitaeiningu til að stilla reit fyrir hvaða síðu sem er. Í Fabrikam er þessi eining notuð fyrir tengilinn „Pöntunarferill“ og „Prófíllinn minn“ á lendingasíðu reikningsstjórnunar.
- **Óskalistareitur reiknings** - Þessi eining er notuð til að gefa yfirlit yfir hluti á óskalista viðskiptavinar. Til dæmis gæti hann fullyrt: „Þú ert með 10 atriði á óskalistanum þínum.“ Hún felur í sér eiginleika fyrir fyrirsögnina og tengilinn „Skoða upplýsingar“. Stilla ætti tengilinn „Skoða upplýsingar“ til að framsenda á óskalistasíðuna. 
- **Netfangareitur reiknings** - Þessi eining er notuð til að gefa yfirlit yfir netföng notandans. Til dæmis gæti hún fullyrt: „Þú ert með 2 netföng bætt við reikninginn þinn.“ Hún felur í sér eiginleika fyrir fyrirsögnina og tengilinn „Skoða upplýsingar“. Stilla ætti tengilinn „Skoða upplýsingar“ til að framsenda á notandanetfangasíðuna.
- **Vildarreitur reiknings** - Þessi eining er notuð til að sýna og tengjast upplýsingum um vildarkerfi. Þessir reitir eru með tvær stöður: Ein staða sýnir tengla til að taka þátt í vildarkerfi ef notandinn er ekki meðlimur nú þegar. Hin staðan sýnir tengla til að skoða síðu vildarupplyýsinga þegar notandinn er þegar meðlimur. Eiginleikar fela í sér fyrirsögnina, tengilinn „Skráning“ og tengilinn „Skoða hollustu“. Stilla ætti tengilinn „Skoða vildarupplýsingar“ til að framsenda á vildarkerfissíðuna. Stilla ætti tengilinn „Innskráning“ til að framsenda á síðu þar sem notendur geta tekið þátt í vildarkerfinu. 

### <a name="order-history-page"></a>Pöntunarferilssíða

Pöntunarferilsíðan notar pöntunarferilseininguna til að sýna allar nýlegar pantanir sem notandinn hefur sett inn.

### <a name="order-details-page"></a>Upplýsingasíða pöntunar

Pöntunarupplýsingasíðan veitir ítarlegar upplýsingar um hverja pöntun og má nálgast af pöntunarferilssíðunni. Það notar pöntunarupplýsingaeininguna, sem krefst sölukennis eða færslukennis til að sækja pöntunarupplýsingarnar.

### <a name="user-profile-page"></a>Notandaforstillingasíða

Notandaforstillingasíðan sýnir upplýsingar um notandareikning, svo sem nafn notanda og netfang. Það notar upplýsingar um notandasnið og notendasnið til að breyta. Þrátt fyrir að ekki sé hægt að fjarlægja netfangið er hægt að breyta því. Notandasniðssíðan sýnir einnig óskir notenda sem gera notanda kleift að velja eða afþakka ákveðna eiginleika eins og að sérsníða meðmælalista. 

### <a name="user-address-page"></a>Netfangssíða notanda

Netfangasíða notanda sýnir lista yfir netföng sem tengjast notendareikningnum. Notandinn gaf þessi netföng annaðhvort upp í greiðsluferlinu eða bætti þeim beint við á þessari síðu. Notendanetfangareiningin er notuð til að bæta við og breyta netföngum, stilla aðalnetfangið og láta núverandi netföng birtast á síðunni.

### <a name="wish-list-page"></a>Óskalistasíða

Óskalistasíðan sýnir atriðin sem hefur verið bætt við óskalista viðskiptavinar. Hún notar óskalistaeininguna til að birta atriði óskalista.

### <a name="loyalty-page"></a>Síða vildarkerfis

Vildarkerfissíðan gerir viðskiptavinum kleift að skoða í vildarupplýsingar sínar ef þeir eru nú þegar meðlimir í vildarkerfi. Þeir geta einnig skoðað stigin sem þeir hafa unnið og innleyst í nýlegum færslum. Síðan notar vildarupplýsingareininguna til að sýna upplýsingar um vildarkerfi. 

Til að taka þátt í vildarkerfi er hægt að búa til markaðssíðu með vildarskráningar og einingar fyrir vildarskilmála. Ef notandinn er ekki meðlimur í vildarkerfi munu þessar einingar gera notandanum kleift að skrá sig.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Hólfeining](add-container-module.md)

[Kaupgluggaeining](add-buy-box.md)

[Körfueining](add-cart-module.md)

[Greiðsluferliseining](add-checkout-module.md)

[Pöntunarstaðfestingareining](order-confirmation-module.md)

[Fyrirsagnareining](author-header-module.md)

[Neðanmálseining](author-footer-module.md)
