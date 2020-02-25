---
title: Sérstilla yfirlit svæðis
description: Þetta efnisatriði lýsir því hvernig á að búa til sérsniðið yfirlitsstigveldi á netinu til að skipuleggja vörur þínar til að vafra á Microsoft Dynamics 365 Commerce síðunni.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c2235510c7ef386d66fe3b137f8e791d14706379
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001830"
---
# <a name="customize-site-navigation"></a>Sérstilla yfirlit svæðis


[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að búa til sérsniðið yfirlitsstigveldi á netinu til að skipuleggja vörur þínar til að vafra á Microsoft Dynamics 365 Commerce síðunni.

## <a name="overview"></a>Yfirlit

Vefverslanir á netinu láta viðskiptavini gjarnan uppgötva og skoða vörur með því að fletta í gegnum vöruflokka. Þessi geta er yfirleitt til staðar með flipum efst á síðunni eða með stýristiku vinstra megin. Í Dynamics 365 Commerce geturðu stofnað og stjórnað stigveldisskipulagi flokksleiðsagnar þinna og vörunum sem eru í ýmsum flokkum.

## <a name="create-a-channel-navigation-hierarchy"></a>Stofna yfirlitsstigveldi rásar

Fylgdu þessum skrefum til að stofna yfirlitsstigveldi rásar.

1. Farðu í **Retail og Commerce \> Afurðir og tegundir \> Flokka- og afurðastjórnun**.
1. Veldu **Tegundastigveldi** og veldu síðan **Nýtt**.
1. Gefðu stigveldinu heiti.

    > [!NOTE]
    > Efsti flokkurinn sem þú býrð til er hnútur rótarflokksins. Hann verður ekki sýndur á síðunni. Til að búa til flokkunarstigveldi þar sem einn efsti stigs hnút er sýndur á síðunni skaltu stofna og nefna flokkinn sem undirgildi af rótarflokknum.

1. Veldu **Nýr tegundahnútur** og gefðu flokknum heiti.
1. Haltu áfram að stofna systkina- og undirflokka eftir þörfum.

Núna geturðu úthlutað vörum í hvern flokk sem þú bjóst til undir efsta stigs flokknum.

## <a name="customize-the-order-of-categories"></a>Sérsniðið röðun flokka

Sjálfgefið er að flokkarnir sem þú skilgreinir munu birtast í stafrófsröð á síðunni þinni. Hins vegar getur þú einnig sérsniðið birtingarröð flokka.

## <a name="assign-a-category-hierarchy-type"></a>Úthluta gerð tegundastigveldis

1. Farðu í **Retail og Commerce \> Afurðir og tegundir \> Flokka- og afurðastjórnun**.
1. Veldu **Tegundastigveldi**.
1. Í aðgerðarúðunni á flipanum **Tegundastigveldi** í flokknum **Uppsetning** skal velja **Tengja stigveldisgerð**.
1. Veljið **Nýtt**.
1. Í reitnum **Gerð tegundastigveldis** velurðu **Yfirlitsstigveldi rásar**.
1. Í reitnum **Tegundastigveldi** velurðu yfirlitsstigveldi rásarinnar sem þú bjóst til áður.

## <a name="publish-new-or-updated-navigation-hierarchies"></a>Birta ný eða uppfærð yfirlitsstigveldi

Fylgdu þessum skrefum til að gera yfirlitsstigveldið aðgengilegt fyrir netverslunina.

1. Farðu í **Retail og Commerce \> Uppsetning rásar \> Rásarflokkar og afurðareigindir**.
1. Veldu netverslunina þína í trénu til vinstri.
1. Veldu **Birta uppfærslur rásar**.
1. Farðu í **Retail og Commerce \> Upplýsingatækni í Retail og Commerce \> Dreifingaráætlun**.
1. Á listanum finnurðu og velur **Vinnslu 1040**.
1. Veljið **Keyra núna**.
1. Endurtaktu skref 5 og 6 fyrir vinnslur 1070 og 1150.

## <a name="show-categories-on-your-site"></a>Sýna flokka á síðunni þinni

Til að sýna flokkunarveldi í netverslun þinni verður þú að bæta við yfirlitseiningunni á viðeigandi stað í sniðmáti eða broti. Eining yfirlitsvalmyndar mun síðan sýna yfirlitsstigveldi, að því tilskildu að þú hafir birt yfirlitsstigveldi þitt á rásinni sem vefsvæðið er bundið við.

> [!NOTE]
> Eining yfirlitsvalmyndar sem er innifalin í byrjendaeiningu verslunarinnar gerir notendum kleift að vafra aðeins til flokka sem hafa ekki undirflokka. Ef viðskiptavinir þínir ættu að geta farið í flokka sem eru með undirflokka verður þú að sérsníða valmyndareininguna.

## <a name="add-custom-navigation-options"></a>Bæta við sérsniðnum yfirlitsvalkostum

Á yfirlitsvalmyndinni geturðu bætt við yfirlitsvalkostum sem eru ekki hluti af tegundastigveldi afurðar. Til dæmis, í lok lista yfir vöruflokka getur þú bætt við liðnum **Hafa samband** sem bendir á tengiliðasíðu sem þú hefur smíðað fyrir síðuna.

Fylgdu þessum skrefum til að bæta við sérsniðnum yfirlitsvalkostum fyrir yfirlitsvalmynd.

1. Í sniðmátinu eða brotinu sem þú vilt sérsníða velurðu eininguna yfir yfirlitsvalmyndina.
1. Í einingaglugganum, á flipanum **Gögn**, velurðu **Bæta hlut við** til að búa til nýjan yfirlitslið efnisstjórnunarkerfi (CMS).
1. Sláðu inn tenglatexta og slóð.
1. Endurtaktu skref 2 og 3 til að bæta við fleiri sérsniðnum leiðsöguvalkostum.
1. Þegar því er lokið skaltu vista sniðmátið eða brotið og haka við það.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir sniðmát og útlit](templates-layouts-overview.md)

[Vinna með sniðmát](work-with-templates.md)

[Vinna með forstillt útlit](work-with-layouts.md)

[Vinna með brot](work-with-fragments.md)

[Vinna með einingar](work-with-modules.md)

[Búa til síðuvefslóð](create-page-url.md)

[Unnið með birta hópa](publish-groups.md)
