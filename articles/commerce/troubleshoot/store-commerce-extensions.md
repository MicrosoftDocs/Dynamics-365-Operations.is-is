---
title: Leysaðu vandamál með viðbætur við Store Commerce
description: Þessi grein útskýrir hvernig á að leysa vandamál með viðbót í Microsoft Dynamics 365 Commerce Store Commerce app.
author: mugunthanm
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: ff26bb76e04c60a9cb975e106456fd781f9300c4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870519"
---
# <a name="troubleshoot-store-commerce-extension-issues"></a>Leysaðu vandamál með viðbætur við Store Commerce

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Þessi grein útskýrir hvernig á að leysa vandamál með viðbót í Microsoft Dynamics 365 Commerce Store Commerce app.

## <a name="extensions-packages-arent-loaded"></a>Viðbótarpakkar eru ekki hlaðnir

### <a name="extensions-packages-dont-appear-on-the-pos--settings-page"></a>Viðbótarpakkar birtast ekki á POS \> Stillingar síða

Viðskiptatími (CRT) kveikjur gætu ekki hafa verið uppfærðar til að innihalda viðbótarpakkann, eða þeir eru ekki notaðir. Fyrir frekari upplýsingar, sjá [Viðskiptatími (CRT) teygjanleika og kveikjur](../dev-itpro/commerce-runtime-extensibility-trigger.md).

### <a name="extensions-packages-appear-on-the-pos--settings-page-but-the-manifest-isnt-loaded"></a>Viðbótarpakkar birtast á POS \> Stillingasíðu, en upplýsingaskráin er ekki hlaðin

Staðfestu að viðbótarpakkarnir séu til í **C:\\ Forritaskrár\\Microsoft Dynamics 365\\ 10.0\\ Verslun verslun\\ Framlengingar** möppu. Ef pakkarnir eru til ætti að vera a **POS** möppu þar sem inniheldur upplýsingaskrána.

Ef það er nr **POS** möppu, staðfestu að Store Commerce verkefnið vísar rétt til viðbyggingarverkefnis sölustaðar (POS). Staðfestu tilvísunarslóð verksins og vertu viss um að hún sé til. 

Í eftirfarandi sýnishorni er uppsetningarverkefnið í vandræðum með viðbyggingarverkefnið sem vísað er til.

![Verkefnatilvísun Store Commerce uppsetningarforrits er ekki gild.](media/ReferenceNotValid.png)

Ef tilvísuninni fyrir viðbyggingarverkefnið er rétt bætt við mun ekki vera nein viðvörun eða ósjálfstæðisvandamál í uppsetningarverkefninu, eins og sýnt er á eftirfarandi dæmi.

![Verkefnatilvísun Store Commerce uppsetningarforrits er gild.](media/ReferenceValid.png)
