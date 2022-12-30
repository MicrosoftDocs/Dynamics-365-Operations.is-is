---
title: Hanna viðmótið fyrir framkvæmd á framleiðslugólfi
description: Þessi grein lýsir því hvernig á að hanna efni í notandaviðmóti fyrir hverja skilgreiningu.
author: johanhoffmann
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecutionConfiguration, JmgProductionFloorExecutionConfigurationTab
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 66190ab261d19c718e13801c17a34b915ccf158c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852245"
---
# <a name="design-the-production-floor-execution-interface"></a>Hanna viðmótið fyrir framkvæmd á framleiðslugólfi

[!include [banner](../includes/banner.md)]

Hægt er að hanna efni í notandaviðmóti fyrir hverja skilgreiningu sem notendaviðmót framleiðslugólfsins notar. Til dæmis gæti verið að starfskraftar í einum vinnuflokki geti opnað verkleiðbeiningar á framleiðslugólfið, en í öðrum vinnuflokki er ekki þörf á leiðbeiningum. Í því tilviki er hægt að stofna tvær grunnstillingar, eina með hnapp til að opna viðhengi skjala og eitt án þessa hnapps.

## <a name="design-a-tab"></a>Hanna flipa

Á **grunnstillingarsíðu Framleiðslugluggana** er hægt að stofna og grunnstilla flipa með því að velja **Hanna flipa** á aðgerðasvæði.

Hverjum flipa er skipt í fjóra kafla, eins og sýnt er á eftirfarandi mynd.

![Flipaútlit.](media/pfe-tab-layout.png "Flipaútlit")

Eftirfarandi einingar eru sýndar á mynd:

1. Fyrsta tækjastika
1. Önnur tækjastika
1. Aðalyfirlit
1. Ítarlegt yfirlit

Til að stofna og skilgreina nýjan flipa skal fylgja þessum skrefum:

1. Farið í **Framleiðslustýring \> Uppsetning \> Framkvæmd framleiðslu \> Grunnstilla framkvæmd á framleiðslugólfi**.

1. Veljið **Hanna flipa** á aðgerðasvæði til að opna síðuna **Hanna flipa**.

    ![Síða hönnunarflipa.](media/pfe-design-tabs.png "Síðan Hanna flipa")

1. Veljið **Nýtt** á aðgerðasvæðinu.

1. Gerið eftirfarandi stillingar í haus síðunnar:

    - **Heiti flipa** - Tilgreindu heiti fyrir flipann
    - **Aðalyfirlit** – Veldu á meðal fyrirfram skilgreindra verklista (*Virk verk*, *Öll verk*, *Verkin mín* og *Vélin mín*).
    - **Upplýsingayfirlit** -Veldu milli auðra gilda eða **Upplýsingar um starf**. Ef valið er autt gildi verður engin nákvæm skoðun á flipanum. Ef valið er **Upplýsingar um starf** mun Ítarlegt yfirlit innihalda nákvæma lýsingu á vinnslunni sem er valin í verklistanum í aðalyfirlitinu.

1. Í **aðaltækjastikunni** skal velja hvaða hnappar eiga að vera tiltækir í aðaltækjastikunni. Dálkurinn **Tiltækar aðgerðir** sýnir lista yfir alla hnappa sem hægt er að bæta við. Dálkurinn **Valdar aðgerðir** sýnir lista yfir alla hnappa sem eru teknir með í núgildandi skilgreiningu. Notaðu hnappana á milli dálka til að fara valdar vörur á milli dálka eftir þörfum. Notaðu upp- og niðurhnappana við hliðina á **Valdar aðgerðir** til að hafa stjórnina á pöntuninni þar sem hnapparnir eru sýndir í notandaviðmótinu.

1. Í **Auka** tækjastiku er hægt að velja hvaða hnappar eiga að vera tiltækir í aukatækjastikunni. Dálkurinn **Tiltækar aðgerðir** sýnir lista yfir alla hnappa sem hægt er að bæta við. Dálkurinn **Valdar aðgerðir** sýnir lista yfir alla hnappa sem eru teknir með í núgildandi skilgreiningu. Notaðu hnappana á milli dálka til að fara valdar vörur á milli dálka eftir þörfum. Notaðu upp- og niðurhnappana við hliðina á **Valdar aðgerðir** til að hafa stjórnina á pöntuninni þar sem hnapparnir eru sýndir í notandaviðmótinu.

## <a name="associate-a-tab-with-a-configuration"></a>Tengja flipa við skilgreiningu

Eftir að þú hefur hannað alla flipana sem þú þarft er hægt að tengja þá við skilgreiningu.

1. Farið í **Framleiðslustýring \> Uppsetning \> Framkvæmd framleiðslu \> Grunnstilla framkvæmd á framleiðslugólfi**.

    ![Grunnstilla framkvæmd á framleiðslugólfi.](media/pfe-config-prod-floor-execution.png "Grunnstilla framkvæmd á framleiðslugólfi")

1. Í flýtiflipanum **Val á flipa** skal velja **Bæta við**.

1. Nýrri línu er bætt við hnitanetið. Fyrir þessa nýju línu skal velja heiti flipa sem bæta á við skilgreininguna.

1. Halda áfram að bæta við öðrum flipum eftir þörfum.

1. Notið hnappana **Færa upp** og **Færa niður** á tækjastikunni til að raða flipunum eftir þörfum. Fliparnir birtast frá vinstri til hægri í þeirri röð sem sýnd er í ofangreindri skjámynd (flipinn efst er sýndur hér til vinstri).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
