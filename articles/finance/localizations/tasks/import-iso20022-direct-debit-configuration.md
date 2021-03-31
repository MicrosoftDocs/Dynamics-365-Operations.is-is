---
title: Flytja inn ISO20022-beingreiðsluskilgreiningu
description: Þessi verklýsing sýnir hvernig á að flytja inn skilgreiningu rafrænnar skýrslugerðar fyrir greiðslu viðskiptavinar.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 964f396625340d593a2fe3dd5be5a1b7da795e9a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218759"
---
# <a name="import-iso20022-direct-debit-configuration"></a>Flytja inn ISO20022-beingreiðsluskilgreiningu

[!include [banner](../../includes/banner.md)]

Þessi verklýsing sýnir hvernig á að flytja inn skilgreiningu rafrænnar skýrslugerðar fyrir greiðslu viðskiptavinar. Þessi aðferð notar snið ISO-20022 beingreiðslu sem dæmi. 



Þetta ferli var stofnuð með því að nota sýnigögn fyrirtækisins DEMF en hægt er að nota hvaða sýnigögn fyrirtækis í þessum tilgangi.



Þetta er fyrsta af fimm ferlum sem lýsa greiðsluferlinu viðskiptavinar með grunnstillingar fyrir rafræna skýrslugerð.

1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.
2. Í lista yfir tiltæka veitandi skilgreininga, veljið Microsoft.
3. Smellt á Stilla sem virkt.
4. Smella á Geymslur.
5. Smellt er á Opin.
6. Smellt er á Sýna síur.
7. Notið eftirfarandi síur: færðu inn síugildi "ISO20022 beingreiðsla (DE)" á reitnum "heiti skilgreiningar" með því að nota síuvirknitáknið "byrjar á".
    * Einnig má finna skilgreiningu á listanum, veljið það og sleppið þessu skrefi.  
8. Smelltu á Flytja inn.
    * Ef hnappurinn Innflutningur er ekki tiltækur, merkir það að þessi skilgreining hefur þegar verið flutt inn.  
9. Smella á Já.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]