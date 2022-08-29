---
title: Samstilltu skattauppsetninguna frá skattreikningsþjónustunni við Dynamics 365 Finance
description: Þessi grein útskýrir hvernig á að samstilla aðalgögn skattuppsetningar frá skattútreikningsþjónustu við Microsoft Dynamics 365 Fjármál.
author: EricWangChen
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.21
ms.custom: intro-internal
ms.search.form: TaxIntegration, TaxServiceParameters
ms.openlocfilehash: 315f2b27a64906ca0fc404d704d0b170dbfa48c5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283854"
---
# <a name="sync-the-tax-setup-from-the-tax-calculation-service-to-dynamics-365-finance"></a>Samstilltu skattauppsetninguna frá skattreikningsþjónustunni við Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að samstilla aðalgögn skattuppsetningar frá skattútreikningsþjónustu við Microsoft Dynamics 365 Fjármál.

Eftir að þú hefur lokið nauðsynlegum uppsetningarskrefum inn [Byrjaðu á skattaútreikningi](global-get-started-with-tax-calculation-service.md), eru eftirfarandi skattuppsetningargögn samstillt sjálfkrafa frá skattútreikningsþjónustunni við fjármál.

## <a name="sales-tax-code"></a>VSK-kóði

| Skattaútreikningsþjónusta           | Finance                             |
| --------------------------------- | ----------------------------------- |
| Skattkóði                          | VSK-kóði                      |
| Lýsing                       | Nafn                                |
| Ílag notanda                        | Jöfnunartímabil                   |
| Ílag notanda                        | Fjárhagsbókunarflokkur                |
| Ílag notanda                        | Gjaldmiðill virðisaukaskatts                  |
| Neikvætt skatthlutfall er stillt | Leyfa neikvæða virðisaukaprósentu |

## <a name="tax-value"></a>Virði skatts

| Skattaútreikningsþjónusta | Finance                   |
| ----------------------- | ------------------------- |
| Frá-færsludagsetning   | Frá dags.                 |
| Til-færsludagsetning     | Til dagsetningar                   |
| Lágmarksupphæð          | Neðri mörk             |
| Hámarksupphæð          | Hámarksgildi             |
| Skatthlutfall                | Gildi                     |
| Ófrádráttarbært hlutfall     | Ófrádráttarbær prósenta |

## <a name="tax-limits"></a>Skattamörk

| Skattaútreikningsþjónusta | Finance           |
| ----------------------- | ----------------- |
| Frá-færsludagsetning   | Frá dags.         |
| Til-færsludagsetning     | Til dagsetningar           |
| Lágmarksupphæð skatta      | Lágmark VSK |
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

Eftir að samstillingunni er lokið skaltu halda áfram að viðhalda þeim færibreytum sem eftir eru í Finance fyrir bókun og skýrslugjöf.

> [!NOTE]
> Samstilling skattauppsetningar frá Finance við skattútreikningsþjónustuna er ekki studd. Fyrir núverandi fjármálaumhverfi, stofnaðu fyrst skattauppsetninguna í skattútreikningsþjónustunni. Samstilltu síðan uppsetningargögnin aftur við fjármálaumhverfið.
