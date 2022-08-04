---
title: Vörulistavalseining
description: Þessi grein fjallar um einingar fyrir vörulistaval og lýsir því hvernig á að bæta þeim við Microsoft Dynamics 365 Commerce viðskipti á milli fyrirtækja (B2B) netviðskiptasíður.
author: ashishmsft
ms.date: 07/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-04-21
ms.openlocfilehash: 642319eea7e40415fd32898f6ec07bfc86f3b1b1
ms.sourcegitcommit: d1491362421bf2fcf72a81dc2dc2d13d3b98122b
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/11/2022
ms.locfileid: "9136929"
---
# <a name="catalog-picker-module"></a>Vörulistavalseining

[!include [banner](includes/banner.md)]

Þessi grein fjallar um einingar fyrir vörulistaval og lýsir því hvernig á að bæta þeim við Microsoft Dynamics 365 Commerce viðskipti á milli fyrirtækja (B2B) netviðskiptasíður.

Vörulistavalareining er sérstakur gámur sem er notaður til að skrá alla vörulista sem eru í boði fyrir B2B-síðunotendur til að versla. Margir vörulistar eru sem stendur aðeins studdir fyrir B2B síður.

Eftirfarandi mynd sýnir dæmi um vörulistavalseiningu.

![Dæmi um vörulistavalseiningu sem sýnir þrjá vörulista.](./media/Catalog-picker-sample.png)

## <a name="add-a-catalog-picker-module-to-your-site"></a>Bættu vörulistavalareiningu við síðuna þína

Fylgdu þessum skrefum til að bæta vörulistavalareiningu við síðuna þína í Commerce site builder.

### <a name="create-a-catalog-picker-page"></a>Búðu til vörulistavalssíðu

Fyrst skaltu búa til vörulistavalssíðu.

1. Farðu í **Síður** og veldu **Ný** til að búa til nýja síðu.
1. Í **Búðu til nýja síðu** svargluggi, undir **Nafn síðu**, koma inn **Vörulistavalari**.
1. Undir **Slóð síðu**, sláðu inn vefslóð fyrir síðuna og veldu síðan **Næst**.

    ![Búðu til nýjan síðuglugga.](./media/Create-catalog-picker-page.png)

1. Undir **Veldu sniðmát**, veldu **Almennt efni**, og veldu síðan **Næst**.
1. Undir **Veldu skipulag**, veldu **Sveigjanlegt skipulag**, og veldu síðan **Næst**.
1. Undir **Farið yfir og klárað**, skoðaðu stillingar síðunnar. Ef þú verður að breyta síðuupplýsingunum skaltu velja **Til baka**. Ef síðuupplýsingarnar eru réttar skaltu velja **Búa til síðu**.
1. Undir **Vörulistavalari**, veldu **Aðal rauf**, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.

    ![Einingu bætt við aðalraufina undir vörulistavali.](./media/Author-web-page-catalog-picker-1.png)

1. Í **Veldu einingar** valmynd, veldu **Ílát** mát og veldu síðan **Allt í lagi**.
1. Veldu **Ílát** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Vörulistavalari** mát og veldu síðan **Allt í lagi**.
1. Í **Vörulistavalari** eignarglugga, undir **Fyrirsögn**, veldu **Vörulistar**, og sláðu síðan inn fyrirsögn fyrir vörulistavalssíðuna.
1. Undir **Fyrirsagnarstig**, veldu fyrirsagnarstig og veldu síðan **Allt í lagi**.
1. Undir **Ríkur texti**, sláðu inn texta sem mun birtast efst á vörulistavalssíðunni.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.

### <a name="add-a-link-on-your-account-page"></a>Bættu við tengli á reikningssíðuna þína

Næst skaltu bæta við tilvísun í vörulistavalssíðuna þína á þínu **Minn reikningur** síðu.

1. Fara til **Síður**, finndu og veldu síðuna þína **Minn reikningur** síðu og veldu síðan **Breyta**.
1. Undir **Aðal** rauf síðunnar, veldu **Almenn reikningsflís** rifa. 
1. Í **Almenn reikningsflís** eignarglugga, undir **Tenglar**, veldu **Bæta við aðgerðartengli**, og veldu síðan **Aðgerðartengill**.
1. Í **Aðgerðartengill** svargluggi, undir **Tengill texti**, sláðu inn tenglatexta fyrir tengilinn á vörulistavalssíðuna þína.
1. Undir **Tenglamarkmið**, veldu **Bættu við tengli**.
1. Í **Bættu við tengli** valmynd, veldu **Sérsniðin síða**, og veldu síðan **Næst**.
1. Undir **Nafn**, veldu vörulistavalssíðuna þína, veldu **Sækja um**, og veldu síðan **Allt í lagi**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.

Eftirfarandi mynd sýnir dæmi um reikningssíðu með tilvísun í vörulistasíðuna.

![Reikningssíðan mín með tengli á vörulista.](./media/my-accounts.png)

### <a name="add-a-link-from-the-header"></a>Bættu við tengli úr hausnum

Að lokum skaltu bæta við tengli úr haus síðunnar þinnar í vörulista þína.

1. Fara til **Brot**, finndu og veldu hausbrot vefsvæðisins þíns og veldu síðan **Breyta**.
1. Veldu hólfið **Fyrirsögn**. 
1. Í **Fyrirsögn** eignarglugga, undir **Reikningstenglar mínir**, veldu **Bæta við aðgerðartengli**, og veldu síðan **Aðgerðartengill**.
1. Í **Aðgerðartengill** svargluggi, undir **Tengill texti**, sláðu inn tenglatexta fyrir tengilinn á vörulistavalssíðuna þína.
1. Undir **Tenglamarkmið**, veldu **Bættu við tengli**.
1. Í **Bættu við tengli** valmynd, veldu **Sérsniðin síða**, og veldu síðan **Næst**.
1. Undir **Nafn**, veldu vörulistavalssíðuna þína, veldu **Sækja um**, og veldu síðan **Allt í lagi**.
1. Smelltu á **Vista**, veldu **Ljúka við breytingar** til að athuga hausbrotið og smelltu síðan á **Birta** til að birta það.

Eftirfarandi mynd sýnir dæmi um haus fyrir netverslun með tengil á B2B vörulistann.

![Fyrirsögn vefsvæðis fyrir netverslun með fellilista í verslun.](./media/catalog-in-header.png)


## <a name="additional-resources"></a>Frekari upplýsingar 

[Stofna Commerce-vörulista fyrir B2B-svæði](catalogs-b2b-sites.md)

[Stækkunarhæfniáhrif Commerce-vörulista fyrir B2B-sérstillingar](catalogs-b2b-sites-dev.md)

[Algengar spurningar um Commerce-vörulista fyrir B2B](catalogs-b2b-sites-FAQ.md)

[Síður og einingar fyrir stjórnun reikninga](account-management.md)

[Eining síðuhauss](author-header-module.md)
