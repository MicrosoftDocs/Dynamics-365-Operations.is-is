---
title: Hlaða upp myndum
description: Þetta efnisatriði lýsir hvernig á að hlaða upp myndum á Microsoft Dynamics 365 Commerce svæðasmið.
author: psimolin
ms.date: 03/03/2020
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
ms.openlocfilehash: 2a0a2fdb275cbeb65c06c01128e90ba660f98c9b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799230"
---
# <a name="upload-images"></a>Hlaða upp myndum

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir hvernig á að hlaða upp myndum á Microsoft Dynamics 365 Commerce svæðasmið.

Margmiðlunarsafn vefsvæðishönnuðar Commerce gerir þér kleift að hlaða inn myndum, annaðhvort stökum eða mörgum í einu með því að nota möppur. Þú ættir alltaf að hlaða útgáfuna af myndinni með hæstu upplausn og gæðum, vegna þess að hluti myndbotans bætir sjálfkrafa myndina fyrir mismunandi skoðunargáttir og brotamörk þeirra.

### <a name="image-information-specified-during-upload"></a>Upplýsingar um mynd sem tilgreindar voru við upphleðslu

Þegar mynd er hlaðið inn er hægt að tilgreina eftirfarandi upplýsingar.

- **Titill, annar texti, lýsing, lykilorð**: Lýsigögn myndarinnar eða myndanna. Titill og annar texti eru nauðsynleg gildi.
- **Velja tegund**:
    - **Enginn**: Notað fyrir sagnamynd eða myndir í e-verslun.
    - **Afurð, flokkur, viðskiptavinur, starfsmaður, vörulisti**: Notað fyrir Dynamics 365 Commerce alhliða mynd eða myndir.
- **Birta eignir eftir upphleðslu**: Þegar þessi gátreitur er valinn birtast myndin eða myndirnar strax eftir upphleðslu.

> [!NOTE]
> Myndeignir með útlutaðan flokk eru einnig sjálfkrafa merktar með flokknum sem lykilorð til að hjálpa til að leita að eignum í tilteknum flokki.

### <a name="naming-conventions-for-omni-channel-images"></a>Nafngiftavenjur fyrir alhliða myndir 

Ef þú hefur stillt Margmiðlunarsafnið sem alhliða myndabakvinnslu er hægt að nota myndaflokka til að tilgreina hvaða flokk hlaðin mynd tilheyrir. Það er líka til nafngiftarvenja sem ætti að fylgja til að tryggja að myndir séu rétt sóttar af öðrum rásum, svo sem sölustað (POS).

Sjálfgefin nafngiftarvenja er breytileg eftir flokknum:
- Myndir vörulista ættu að heita „**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**”
- Flokkamyndir ættu að heita „**/Categories/\{CategoryName\}.png**”
- Viðskiptavinamyndir ættu að heita „**/Customers/\{CustomerNumber\}.jpg**”
- Starfsmannamyndir ættu að heita „**/Workers/\{WorkerNumber\}.jpg**”
- Afurðamyndir ættu að heita „**/Products/\{ProductNumber\}_000_001.png**”
    - 001 er röð myndarinnar og hún getur verið 001, 002, 003, 004 eða 005
- Afuðaraðbrigðamyndir ættu að heita „**/Products/\{ProductNumber\} \^ \{Style\} \^ \{Size\} \^ \{Color\} \^\_000_001.png**“
    - Til dæmis: 93039 \^ \^ 2 \^ Svart \^_000_001.png

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
