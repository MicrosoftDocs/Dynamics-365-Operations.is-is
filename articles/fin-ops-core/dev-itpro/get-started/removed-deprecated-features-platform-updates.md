---
title: Fjarlægðir eða úreltir eiginleikar verkvangs
description: Þetta efnisatriði lýsir eiginleikum sem hafa verið fjarlægðir eða sem verða fjarlægðir í verkvangsuppfærslum á forritum Finance and Operations.
author: sericks007
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: d394f5ca84efc5beb943d349e45a3d2c9639d83c
ms.sourcegitcommit: 75974ae567bb0eacf0f65cac992b34ce5c680b93
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/03/2020
ms.locfileid: "3095775"
---
# <a name="removed-or-deprecated-platform-features"></a>Fjarlægðir eða úreltir eiginleikar verkvangs

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir eiginleikum sem hafa verið fjarlægðir eða sem verða fjarlægðir í verkvangsuppfærslum á forritum Finance and Operations.

- *Fjarlægður* eiginleiki er ekki lengur tiltækur í vörunni.
- *Úreltur* eiginleiki er ekki í virkri þróun og getur verið fjarlægður úr uppfærslum í framtíðinni.

Þessi listi er ætlað að hjálpa þér að íhuga þessar fjarlægingar og úreldingar fyrir eigin áætlanagerð. 

> [!NOTE]
> Ítarlegar upplýsingar um hluti í forritum Finance and Operations má finna í [Tæknilegum tilvísunarskýrslum](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Hægt er að bera saman mismunandi útgáfur þessara skýrslna til að fá upplýsingar um hluti sem hefur verið breytt eða hafa verið fjarlægðir í hverri útgáfu forrita Finance and Operations.

## <a name="platform-update-32"></a>Update 32 fyrir verkvang

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Gluggi fyrir breytingu á verkflæðisbeiðni inniheldur ekki lengur fellivalmynd fyrir val á notendum
|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þetta var öryggisatriði vegna þess að beiðni um breytingar var hægt að senda í ógáti til notanda. Þetta var einnig nothæfismál vegna þess að það neyddi notandann til að ákvarða hver upphafsmaður verkflæðisins var og velja þá handvirkt.  |
| **Skipt út fyrir aðra eiginleika?**   | Nr |
| **Afurðasvæði sem haft er áhrif á**         | Verkflæði |
| **Dreifingarvalkostur**              | Öll |
| **Staða**                         | Listi notendavalsins var fjarlægður úr valmyndinni um breytingu á beiðni í uppfærslu á verkvangi 32. Beiðnir um breytingu verða sjálfkrafa sendar til höfundar eins og til er ætlast. Fyrir frekari upplýsingar um þessa virkni, sjá [Verkþættir í samþykktarferli verkflæðis](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change). |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a>Innfelldir boratenglar eru ekki lengur studdir í skjöluðum skjölum sem gefin eru af þjónustunni í skýinu 
|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Vefslóðir sem eru felldar inn í skjöl sem þjónustan veitir geta innihaldið viðkvæm viðskiptagögn. Við erum að fjarlægja stuðning við innbyggða boratengla í skjölum sem öryggisráðstöfun til að vernda gögn viðskiptavinarins frekar. Notendur munu einnig njóta góðs af bættum árangri meðan þeir framleiða skjöl gagnvirkt vegna þessarar breytinga.  |
| **Skipt út fyrir aðra eiginleika?**   | Ekkert |
| **Afurðasvæði sem haft er áhrif á**         | Skýrslugerð |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Þessi aðgerð er virkur tekinn úr þjónustunni.<br><br>Nútíma viðskiptavinurinn býður upp á fjölmarga möguleika til að framleiða áhorf sem innihalda tengla sem myndast sjálfkrafa til að aðstoða við siglingar forritsins. Mælt er með pagineruðum gögnum sem þjónustan veitir vegna utanaðkomandi samskipta sem eru send, geymd og geymd og prentuð fyrir viðtakendur. Við höfum bætt reynsluna af því að forskoða skjöl beint í vafranum, sem býður upp á beinan aðgang að prenturum á staðnum. Fyrir frekari upplýsingar, sjá [Forskoða PDF skjöl með innbyggðri skoðun](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/preview-pdf-documents). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Fyrri tilkynningar um eiginleika sem voru fjarlægðir eða úreltir
Til að læra meira um eiginleika sem hafa verið fjarlægðir eða úreltir í fyrri útgáfum, sjá [Fjarlægir eða úreltir eiginleikar í fyrri útgáfum](../migration-upgrade/deprecated-features.md).

