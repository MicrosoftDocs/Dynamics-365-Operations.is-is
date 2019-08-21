---
title: Flytja inn skilgreiningu ISO20022-kreditfærslu
description: Þessi verklýsing sýnir hvernig á að flytja inn skilgreiningu rafrænnar skýrslugerðar fyrir greiðslu lánardrottins.
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee7e69611d31d2577ebafdfc059b0936aef0520b
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848792"
---
# <a name="import-iso20022-credit-transfer-configuration"></a>Flytja inn skilgreiningu ISO20022-kreditfærslu

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

