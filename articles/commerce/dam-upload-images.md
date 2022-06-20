---
title: Hlaða upp myndum
description: Þessi grein lýsir því hvernig á að hlaða upp myndum inn Microsoft Dynamics 365 Commerce vefsmiður.
author: psimolin
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: e0f5cdd0381932cffc64f1c7e83eecd4662d8c9f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892835"
---
# <a name="upload-images"></a>Hlaða upp myndum

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að hlaða upp myndum inn Microsoft Dynamics 365 Commerce vefsmiður.

Margmiðlunarsafn vefsvæðishönnuðar Commerce gerir þér kleift að hlaða inn myndum, annaðhvort stökum eða mörgum í einu með því að nota möppur. Þú ættir alltaf að hlaða útgáfuna af myndinni með hæstu upplausn og gæðum, vegna þess að hluti myndbotans bætir sjálfkrafa myndina fyrir mismunandi skoðunargáttir og brotamörk þeirra.

### <a name="image-information-specified-during-upload"></a>Upplýsingar um mynd sem tilgreindar voru við upphleðslu

Þegar mynd er hlaðið inn er hægt að tilgreina eftirfarandi upplýsingar.

- **Titill, annar texti, lýsing, lykilorð**: Lýsigögn myndarinnar eða myndanna. Titill og annar texti eru nauðsynleg gildi.
- **Velja tegund**:
    - **Enginn**: Notað fyrir sagnamynd eða myndir í e-verslun.
    - **Afurð, flokkur, viðskiptavinur, starfsmaður, vörulisti**: Notað fyrir Dynamics 365 Commerce alhliða mynd eða myndir.
- **Birta eignir eftir upphleðslu**: Þegar þessi gátreitur er valinn birtast myndin eða myndirnar strax eftir upphleðslu.

> [!NOTE]
> - Myndeignir með útlutaðan flokk eru einnig sjálfkrafa merktar með flokknum sem lykilorð til að hjálpa til að leita að eignum í tilteknum flokki.
> - Vöruupplýsingasíður búa til á kraftmikinn hátt **Alt texti** með því að nota vöruheitið, svo að breyta **Alt texti** fyrir vörumynd mun hafa engin áhrif á prentuðu myndina.

### <a name="naming-conventions-for-omni-channel-images"></a>Nafngiftavenjur fyrir alhliða myndir 

Ef þú hefur stillt Margmiðlunarsafnið sem alhliða myndabakvinnslu er hægt að nota myndaflokka til að tilgreina hvaða flokk hlaðin mynd tilheyrir. Það er líka til nafngiftarvenja sem ætti að fylgja til að tryggja að myndir séu rétt sóttar af öðrum rásum, svo sem sölustað (POS).

Sjálfgefin nafngiftarvenja er breytileg eftir flokknum:
- Myndir vörulista ættu að heita „**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**”
- Flokkamyndir ættu að heita „**/Categories/\{CategoryName\}.png**”
- Viðskiptavinamyndir ættu að heita „**/Customers/\{CustomerNumber\}.jpg**”
- Starfsmannamyndir ættu að heita „**/Workers/\{WorkerNumber\}.jpg**”
- Afurðamyndir ættu að heita "**/Products/\{ProductNumber\}\_000_001.png**"
    - 001 er röð myndarinnar og hún getur verið 001, 002, 003, 004 eða 005
- Afuðaraðbrigðamyndir ættu að heita „**/Products/\{ProductNumber\} \^ \{Style\} \^ \{Size\} \^ \{Color\} \^\_000_001.png**“
    - Til dæmis: 93039 \^ &nbsp;\^ 2 \^ Svart \^\_000_001.png
- Myndir afurðarafbrigðis með skilgreiningarvídd eiga að kallast „**/Products/\{ProductNumber\} \^ \{Skilgreining\}\_000_001.png**“
    - Til dæmis 93039 \^ LB8017_000_001.png

> [!NOTE]
> Fyrir myndir afurðarafbrigðis, ef víddargildið er autt, þurfa að vera tvö bil á milli innskotsmerkjanna í skráarheitinu.

Dæmin að ofan nota sjálfgefna skilgreiningu. Skiltáknið og víddirnar eru stillanleg og nákvæm krafa um nafngift getur verið breytileg eftir uppsetningum. Ein aðferð við að auðkenna nákvæma nafngiftarvenju sem er nauðsynleg er að nota stjórnborð þróunaraðila í vafranum til að skoða beiðni um mynd afurðarafbrigðis á meðan afurðarvíddunum á yfirborði upplýsingasíðu afurðar (PDP) er breytt.

## <a name="upload-an-image"></a>Hlaða upp mynd

Fylgdu þessum skrefum til að hlaða upp mynd í vefsvæðishönnuði.

1. Í vinstri stýriglugganum velurðu **Margmiðlunarsafn**.
1. Veldu á skipanastikunni **Hlaða inn \> Hlaða upp margmiðlun**.
1. Farðu í File Explorer gluggann og flettu að og veldu eina eða fleiri myndskrár sem þú vilt hlaða upp og veldu síðan **Opna**.
1. Í valmyndinni **Hlaða upp margmiðlun** slærðu inn nauðsynlegan titil og annan texta.
1. Sláðu inn valfrjálsa lýsingu og lykilorð og veldu flokk ef þess er óskað. 
1. Ef þú vild birta mynd(ir) beint eftir uppflutning skaltu velja gátreitinn **Birta margmiðlunarefni eftir uppflutning**.
1. Veljið **Í lagi**.

## <a name="upload-a-folder-of-images"></a>Hlaða upp möppu með myndum

Fylgdu þessum skrefum til að hlaða upp fjölda mynda í myndamöppu í vefsvæðishönnuði.

1. Í vinstri stýriglugganum velurðu **Margmiðlunarsafn**.
1. Veldu á skipanastikunni **Hlaða inn \> Hlaða upp möppu**.
1. Farðu í File Explorer gluggann og flettu að og veldu möppu til að hlaða upp og veldu síðan **Opna**.
1. Í valmyndinni **Hlaða upp margmiðlunarefni** slærðu inn valkvæð leitarorð og veldu flokk ef þess er óskað. 
1. Ef þú vild birta myndirnar í möppunni beint eftir uppflutning skaltu velja gátreitinn **Birta margmiðlunarefni eftir uppflutning**.
1. Veljið **Í lagi**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit stafrænnar eignastýringar](dam-overview.md)

[Hlaða upp myndbandi](dam-upload-video.md)

[Hlaða upp skrám](dam-upload-files.md)

[Skera myndir](dam-crop-images.md)

[Sérstilla áherslupunkta myndar](dam-custom-focal-point.md)

[Hlaða upp og þjóna föstum skrám](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
