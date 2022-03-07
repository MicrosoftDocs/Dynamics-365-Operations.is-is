---
title: Umreikningar gjaldmiðils innan samstæðu
description: Þetta efnisatriði útskýrir umreikninga gjaldmiðla fyrir færslur innan samstæðu
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 540849003d532ef2f0905c18332d9cb82a04cf7c
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548341"
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
