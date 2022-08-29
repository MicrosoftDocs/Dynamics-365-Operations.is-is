---
title: Leysa vandamál með viðbætur við Store Commerce
description: Þessi grein útskýrir hvernig á að leysa vandamál með viðbót í Microsoft Dynamics 365 Commerce Store Commerce app.
author: josaw1
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 1a2d6a68b7556d8b4d05529efd90f9e66f0c5925
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269782"
---
# <a name="troubleshoot-store-commerce-extension-issues"></a>Leysa vandamál með viðbætur við Store Commerce

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að leysa vandamál með viðbót í Microsoft Dynamics 365 Commerce Store Commerce app.

## <a name="extensions-packages-arent-loaded"></a>Viðbótarpakkar eru ekki hlaðnir

### <a name="extensions-packages-dont-appear-on-the-pos--settings-page"></a>Viðbótarpakkar birtast ekki á POS \> Stillingar síða

Viðskiptatími (CRT) kveikjur gætu ekki hafa verið uppfærðar til að innihalda viðbótapakkann, eða þeir eru ekki notaðir. Fyrir frekari upplýsingar, sjá [Viðskiptatími (CRT) teygjanleika og kveikjur](../dev-itpro/commerce-runtime-extensibility-trigger.md).

### <a name="extensions-packages-appear-on-the-pos--settings-page-but-the-manifest-isnt-loaded"></a>Viðbótarpakkar birtast á POS \> Stillingasíðu, en upplýsingaskráin er ekki hlaðin

Staðfestu að viðbótarpakkarnir séu til í **C:\\ Forritaskrár\\Microsoft Dynamics 365\\ 10.0\\ Verslun verslun\\ Framlengingar** möppu. Ef pakkarnir eru til ætti að vera a **POS** möppu þar sem inniheldur upplýsingaskrána.

Ef það er nr **POS** möppu, staðfestu að Store Commerce verkefnið vísar rétt til viðbyggingarverkefnis sölustaðar (POS). Staðfestu verktilvísunarslóðina og vertu viss um að hún sé til. 

Í eftirfarandi dæmimynd er uppsetningarverkefnið í vandræðum með viðbyggingarverkefnið sem vísað er til.

![Verkefnatilvísun Store Commerce uppsetningarforrits er ekki gild.](media/ReferenceNotValid.png)

Ef tilvísuninni fyrir viðbyggingarverkefnið er rétt bætt við, verður engin viðvörun eða ósjálfstæðisvandamál í uppsetningarverkefninu, eins og sýnt er á eftirfarandi dæmi.

![Verkefnatilvísun Store Commerce uppsetningarforrits er gild.](media/ReferenceValid.png)
