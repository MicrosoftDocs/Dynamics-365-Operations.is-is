---
title: Flytja inn skilgreiningu ISO20022-kreditfærslu
description: Þessi verklýsing sýnir hvernig á að flytja inn skilgreiningu rafrænnar skýrslugerðar fyrir greiðslu lánardrottins.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ffc86ba9dade0ae494ca4ace8d9f562da9c9527a4731493d892b60112293af3f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781137"
---
# <a name="import-iso20022-credit-transfer-configuration"></a>Flytja inn skilgreiningu ISO20022-kreditfærslu

[!include [banner](../../includes/banner.md)]

Þessi verklýsing sýnir hvernig á að flytja inn skilgreiningu rafrænnar skýrslugerðar fyrir greiðslu lánardrottins. Þýska ISO 20022 snið millifærsla fjármuna er notað sem dæmi. Hægt að nota þetta ferli fyrir aðrar tiltækt snið fyrir rafræna skýrslugerð. 

Þetta verkefni var stofnuð með því að nota sýnigögn fyrirtækisins DEMF en hægt er að nota hvaða sýnigögn fyrirtækis til að ljúka þessu verki.

Þetta er fyrsta af fimm verkefnum sem saman lýsa greiðsluferlinu lánardrottins með því að nota grunnstillingar fyrir rafræna skýrslugerð. Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.

1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.
2. Í lista yfir tiltæka veitandi skilgreininga, veljið Microsoft.
3. Smellt á Stilla sem virkt.
4. Smella á Geymslur.
5. Smellt er á Opin.
6. Smellt er á Sýna síur.
7. Notið eftirfarandi síur: færðu inn síugildi "ISO20022 millifærsla fjármuna (DE)" á reitnum "heiti skilgreiningar" með því að nota síuvirknitáknið "byrjar á".
    * Einnig má finna skilgreiningu á listanum, veljið það og flytja í innflutningsverkið.  
8. Smelltu á Flytja inn.
    * Ef hnappurinn Innflutningur er ekki tiltækur, merkir það að þessi skilgreining hefur þegar verið flutt inn.  
9. Smella á Já.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]