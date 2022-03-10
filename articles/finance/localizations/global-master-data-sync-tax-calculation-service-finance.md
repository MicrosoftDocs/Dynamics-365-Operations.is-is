---
title: Samstilltu skattuppsetninguna frá Skattreikningsþjónustunni við Dynamics 365 Finance
description: Þetta efnisatriði útskýrir hvernig á að samstilla aðalgögn skattuppsetningar frá skattaútreikningsþjónustunni við Microsoft Dynamics 365 Finance.
author: wangchen
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegration, TaxServiceParameters
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: d5d994934014a146f825431cb53dfbef8fe20bc8
ms.sourcegitcommit: 27475081f3d2d96cf655b6afdc97be9fb719c04d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/12/2022
ms.locfileid: "7965108"
---
# <a name="sync-the-tax-setup-from-the-tax-calculation-service-to-dynamics-365-finance"></a>Samstilltu skattuppsetninguna frá Skattreikningsþjónustunni við Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að samstilla aðalgögn skattuppsetningar frá skattaútreikningsþjónustunni við Microsoft Dynamics 365 Finance.

Eftir að þú hefur lokið nauðsynlegum uppsetningarskrefum inn [Byrjaðu á skattaútreikningi](global-get-started-with-tax-calculation-service.md), eru eftirfarandi skattuppsetningargögn sjálfkrafa samstillt frá skattreikningsþjónustunni við fjármál.

## <a name="sales-tax-code"></a>VSK-kóði

| Skattaútreikningsþjónusta           | Finance                             |
| --------------------------------- | ----------------------------------- |
| Skattkóði                          | VSK-kóði                      |
| Lýsing                       | Heiti                                |
| Ílag notanda                        | Jöfnunartímabil                   |
| Ílag notanda                        | Fjárhagsbókunarflokkur                |
| Ílag notanda                        | Gjaldmiðill virðisaukaskatts                  |
| Neikvætt skatthlutfall er stillt | Leyfa neikvæða virðisaukaprósentu |

## <a name="tax-value"></a>Virði skatts

| Skattaútreikningsþjónusta | Finance                   |
| ----------------------- | ------------------------- |
| Frá-færsludagsetning   | Frá degi                 |
| Til-færsludagsetning     | Til dagsetning                   |
| Lágmarksupphæð          | Neðri mörk             |
| Hámarksupphæð          | Hámarksgildi             |
| Skatthlutfall                | Gildi                     |
| Ófrádráttarbært hlutfall     | Ófrádráttarbær prósenta |

## <a name="tax-limits"></a>Skattamörk

| Skattaútreikningsþjónusta | Finance           |
| ----------------------- | ----------------- |
| Frá-færsludagsetning   | Frá degi         |
| Til-færsludagsetning     | Til dagsetning           |
| Lágmarksskattupphæð      | Lágmark VSK |
| Hámarksskattsupphæð      | Hámark VSK |

## <a name="sales-tax-group"></a>VSK-flokkur

| Skattaútreikningsþjónusta                         | Finance                                    |
| ----------------------------------------------- | ------------------------------------------ |
| Skattflokkur                                       | VSK-flokkur                            |
| Skattkóðar undir þessum skattflokki                  | Vsk-kóðar undir þessum vsk-flokki |
| Skattnúmerið er merkt sem **Er undanþegin**         | Undanþága                                     |
| Skattnúmerið er merkt sem **Er undanþegin**         | Undanþágukóði                                |
| Skattnúmerið er merkt sem **Er Reverse Charge** | Bakfært gjald                             |
| Skattnúmerið er merkt sem **Er Notkunarskattur**        | Neysluskattur                                    |

## <a name="item-sales-tax-group"></a>VSK-flokkur vöru

| Skattaútreikningsþjónusta             | Finance                                         |
| ----------------------------------- | ----------------------------------------------- |
| VSK-flokkur                      | VSK-flokkur vöru                            |
| Skattkóðar undir þessum lið skattflokkur | Vsk-kóðar undir þessum lið Vsk-flokkur |

Eftir að samstillingunni er lokið skaltu halda áfram að viðhalda þeim færibreytum sem eftir eru í Finance í færslu- og skýrsluskyni.

> [!NOTE]
> Samstilling skattauppsetningar frá Finance við skattútreikningsþjónustuna er ekki studd. Fyrir núverandi fjármálaumhverfi, stofnaðu fyrst skattuppsetninguna í skattaútreikningsþjónustunni. Samstilltu síðan uppsetningargögnin aftur við fjármálaumhverfið.