---
title: Umreikningar gjaldmiðils innan samstæðu
description: Þetta efnisatriði útskýrir umreikninga gjaldmiðla fyrir færslur innan samstæðu
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: f0af05c324bb67744ba6650e3d7a4ba8b958040e
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671899"
---
# <a name="intercompany-currency-conversions"></a>Umreikningar gjaldmiðils innan samstæðu

[!include [banner](../../includes/banner.md)]

Þegar gjaldmiðilskóði upprunalegrar sölupöntunar og innkaupapöntunar innan samstæðu er ekki sá sami, er gjaldmiðill umreiknaður fyrir eftirfarandi reiti ef samstilling er virkjuð:

- **Einingarverð**
- **Sölugjöld** eða **Gjöld á innkaupum**
- **Afsláttur**
- **Samvalsafsláttur**

Þessir reitir eru síðan samstilltir við sölupöntunarlínu innan samstæðu.

Hins vegar, þar sem gjaldmiðillinn í samstæðuinnkaupapöntun og samstæðusölupöntun er ávallt samstilltur, eru eftirfarandi reitir samstilltir án þess að nota umreikning gjaldmiðils:

- **Einingarverð**
- **Sölugjöld** eða **Gjöld á innkaupum**
- **Afsláttur**
- **Afsláttarprósenta**
- **Samvalsafsláttur**
- **Samvalsafsláttarprósenta**

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
