---
title: Samstilla uppsetningu skatta úr skattaútreikningsþjónustunni í Dynamics 365 Finance
description: Þessi grein útskýrir hvernig á að samstilla gögn um skattauppsetningu úr Skattaútreikningsþjónustunni við Microsoft Dynamics 365 Finance.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283854"
---
# <a name="sync-the-tax-setup-from-the-tax-calculation-service-to-dynamics-365-finance"></a>Samstilla uppsetningu skatta úr skattaútreikningsþjónustunni í Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að samstilla gögn um skattauppsetningu úr Skattaútreikningsþjónustunni við Microsoft Dynamics 365 Finance.

Eftir að nauðsynlegum uppsetningarskrefum er lokið í [Hafist handa með skattaútreikning](global-get-started-with-tax-calculation-service.md) eru eftirfarandi uppsetningargögn skatta sjálfkrafa samstillt frá Skattaútreikningsþjónustu í Finance.

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
| Ófrádráttarbær upphæð     | Ófrádráttarbær prósenta |

## <a name="tax-limits"></a>Skattmörk

| Skattaútreikningsþjónusta | Finance           |
| ----------------------- | ----------------- |
| Frá-færsludagsetning   | Frá dags.         |
| Til-færsludagsetning     | Til dagsetningar           |
| Lágmarksupphæð skatts      | Lágmark VSK |
| Hámarksupphæð skatts      | Hámark VSK |

## <a name="sales-tax-group"></a>VSK-flokkur

| Skattaútreikningsþjónusta                         | Finance                                    |
| ----------------------------------------------- | ------------------------------------------ |
| Skattflokkur                                       | VSK-flokkur                            |
| Skattkóðar í þessum skattflokki                  | VSK-kóðar undir þessum söluskattsflokki |
| Skattkóðinn er merktur sem **Er undanþeginn**         | Undanþága                                     |
| Skattkóðinn er merktur sem **Er undanþeginn**         | Undanþágukóði                                |
| Skattkóðinn er merktur sem **Er bakfært gjald** | Bakfært gjald                             |
| Skattkóðinn er merktur sem **Er notkunarskattur**        | Neysluskattur                                    |

## <a name="item-sales-tax-group"></a>VSK-flokkur vöru

| Skattaútreikningsþjónusta             | Finance                                         |
| ----------------------------------- | ----------------------------------------------- |
| VSK-flokkur                      | VSK-flokkur vöru                            |
| Skattkóðar í þessum skattflokki vöru | VSK-kóðar undir þessum söluskattsflokki vöru |

Eftir að samstillingu er lokið skal halda áfram að viðhalda þeim breytum sem eftir eru í Finance til bókunar og skýrslugerðar.

> [!NOTE]
> Samstilling skattauppsetningarinnar frá Finance til Skattaútreikningsþjónustunnar er ekki studd. Fyrir fyrirliggjandi Finance umhverfi skaltu fyrst búa til skattauppsetningu í Skattaútreikningsþjónustunni. Samstilltu síðan uppsetningargögnin aftur við Finance umhverfið.
