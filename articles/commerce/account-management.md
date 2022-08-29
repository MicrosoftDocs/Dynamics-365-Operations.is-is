---
title: Síður og einingar fyrir stjórnun reikninga
description: Þessi grein fjallar um reikningsstjórnunarsíður og einingar í Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 2db9a1218802234297e9d027691e5887d6a5c808
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274456"
---
# <a name="account-management-pages-and-modules"></a>Síður og einingar fyrir stjórnun reikninga

[!include [banner](includes/banner.md)]

Þessi grein fjallar um reikningsstjórnunarsíður og einingar í Microsoft Dynamics 365 Commerce.

Með stjórnun reikninga er átt við hóp síðna sem notaðar eru til að stjórna upplýsingum sem tengjast notendareikningi í Dynamics 365 Commerce. Reikningsstjórnunarsíður innihalda lendingasíðu reikningsstjórnunar, notandaforstillingasíðu, notendasíðu, síðu pöntunarferils, pöntunarupplýsingasíðu, vildarsíðu og óskalistasíðu.

### <a name="account-management-landing-page"></a>Lendingasíða fyrir stjórnun reikninga

Lendingasíða reikningsstjórnunar notar eftirfarandi einingar:

- **Gámur** - Allar lendingarsíðueiningar reikningsstjórnunar skulu settar í gám. 
- **Móttökureitur reiknings** - Þessi eining er notuð til að veita móttökuskilaboð á reikningssíðu. Hann felur í sér eiginleika fyrir fyrirsögnina.
- **Almennir reitir reiknings** - Þessa einingu er hægt að nota til að útvega fyrirsagnir og tengla á reikningastjórnarsíður, svo sem „Pöntunarferill“ eða „Prófíllinn minn“. Hægt er að nota almenna reitaeiningu til að stilla reit fyrir hvaða síðu sem er. Í Fabrikam er þessi eining notuð fyrir tengilinn „Pöntunarferill“ og „Prófíllinn minn“ á lendingasíðu reikningsstjórnunar.
- **Óskalistareitur reiknings** - Þessi eining er notuð til að gefa yfirlit yfir hluti á óskalista viðskiptavinar. Til dæmis gæti hann fullyrt: „Þú ert með 10 atriði á óskalistanum þínum.“ Hún felur í sér eiginleika fyrir fyrirsögnina og tengilinn „Skoða upplýsingar“. Stilla ætti tengilinn „Skoða upplýsingar“ til að framsenda á óskalistasíðuna. 
- **Netfangareitur reiknings** - Þessi eining er notuð til að gefa yfirlit yfir netföng notandans. Til dæmis gæti hún fullyrt: „Þú ert með 2 netföng bætt við reikninginn þinn.“ Hún felur í sér eiginleika fyrir fyrirsögnina og tengilinn „Skoða upplýsingar“. Stilla ætti tengilinn „Skoða upplýsingar“ til að framsenda á notandanetfangasíðuna.
- **Vildarreitur reiknings** - Þessi eining er notuð til að sýna og tengjast upplýsingum um vildarkerfi. Þessi reitur er með tvær stöður: Ein staða sýnir tengla til að taka þátt í vildarkerfi ef notandinn er ekki meðlimur nú þegar. Hin staðan sýnir tengla til að skoða síðu vildarupplyýsinga þegar notandinn er þegar meðlimur. Eiginleikar fela í sér fyrirsögnina, tengilinn „Skráning“ og tengilinn „Skoða hollustu“. Stilla ætti tengilinn „Skoða vildarupplýsingar“ til að framsenda á vildarkerfissíðuna. Stilla ætti tengilinn „Innskráning“ til að framsenda á síðu þar sem notendur geta tekið þátt í vildarkerfinu. 

### <a name="order-history-page"></a>Pöntunarferilssíða

Pöntunarferilsíðan notar pöntunarferilseininguna til að sýna allar nýlegar pantanir sem notandinn hefur sett inn.

### <a name="order-details-page"></a>Upplýsingasíða pöntunar

Pöntunarupplýsingasíðan veitir ítarlegar upplýsingar um hverja pöntun og má nálgast af pöntunarferilssíðunni. Það notar pöntunarupplýsingaeininguna, sem krefst sölukennis eða færslukennis til að sækja pöntunarupplýsingarnar.

### <a name="my-profile-page"></a>Forstillingarsíða mín

Notandasíða mín sýnir upplýsingar um notandasíðu reikningsins þíns með einingu reikningsstillingar. Síðan sýnir netfangið sem er tengt við reikning notanda, auk kjörstillingar sem eru settar upp fyrir reikninginn. Ef sérstilltir eiginleika viðskiptavinar eru settir upp birtir eigindin „Viðbótarupplýsingar“ einnig þessa eiginleika. Notendur geta breytt nafni sínu, kjörstillingum eða viðbótarupplýsingum (ef þær eru til staðar).

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
