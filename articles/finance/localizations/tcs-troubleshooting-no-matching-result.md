---
title: Engin samsvarandi niðurstaða fannst
description: Þessi grein útskýrir hvernig á að leysa villuna "Engin samsvarandi niðurstaða fannst" í skattaútreikningsþjónustunni.
author: hangwan
ms.date: 03/25/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 03/23/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: d3bbc76741fdd018d1b2987538b8de7f6d92ee53
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845145"
---
# <a name="no-matching-result-could-be-found"></a>Engin samsvarandi niðurstaða fannst

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir úrræðaleitarskref sem þú getur tekið ef þú færð "Engin samsvarandi niðurstaða fannst" villu í skattaútreikningsþjónustunni.

## <a name="symptom"></a>Einkenni

Þú færð eftirfarandi villuboð: "Höfuð/línur - 1, skattaflokkur, engin samsvarandi niðurstaða fannst."

```json
======================Tax service calculation result JSON:===========================
{
    "taxDocument": {
        "Header": [
            {
                "Lines": [
                    {
                        ...
                        "Errors": [
                            {
                                "Code": "TaxSetup20000",
                                "Message": "Header/Lines - 1, Tax group applicability, no matching result could be found."
                            }
                        ],
                        "Adjustment": null
                    }
                ],
                "Measures": {
                    ...
                },
                ...
            }
        ]
    },
    ...
}
```

## <a name="cause"></a>Orsök

Vandamálið kemur upp þegar eiginleikauppsetningin í Regulatory Configuration Service (RCS) er röng.

## <a name="troubleshoot"></a>Úrræðaleit

1. Sækja skrána fyrir úrræðaleit. Fyrir frekari upplýsingar, sjá [Virkja villuleitarstillingu fyrir bilanaleit](tcs-troubleshooting-enable-debug-mode.md).
2. Berðu saman skattaþjónustuútreikninginn við eiginleikauppsetninguna til að laga uppsetningarvandann.

    Eftirfarandi dæmi sýnir inntak skattaþjónustuútreiknings.

    ```json
    ===============================Tax service calculation input JSON:=====================================
    {
        "TaxableDocument": {
            "Header": [
                {
                    "Lines": [
                        {
                            ...
                        }
                    ],
                    "Business Process": "Sales",
                    "Ship From Zip Code": "30159",
                }
            ]
        },
        "Parameter": {
            ...
        },
        "Adjustment": {
            "Lines": {}
        }
    }
    ```

    Eftirfarandi tafla sýnir gildi skattaflokka í RCS.

    | Header.Viðskiptaferli | Lines.Business Unit | Header.Ship From Póstnúmer | Skattflokkur |
    |-------------------------|---------------------|---------------------------|-----------|
    | Færslubók                 |                     |                           | A hópur   |
    | Sala                   |                     | 30160                     | Flokkur B   |

    Samkvæmt útreikningi skattaþjónustunnar er **Viðskiptaferli** gildi á hausnum er **Sala**, og **Senda frá póstnúmeri** gildi á hausnum er **30159**. Þetta inntak er byggt á uppsetningu gildandi reglna í RCS. Vegna þess að það er engin samsvarandi lína kemur villan upp.

    > [!NOTE]
    > Ef gildið í nothæfisreglunni er autt, gildir reglan um hvaða gildi sem er.

## <a name="mitigation"></a>Mildun

Fylgdu þessum skrefum til að draga úr villunni.

1. Í RCS skal fara í **Altækir eiginleikar** \> **Skattaútreikningur**.
2. Búðu til nýja útgáfu af eiginleikanum.
3. Bættu við línu fyrir samsvarandi upplýsingar.

    | Header.Viðskiptaferli | Lines.Business Unit | Header.Ship From Póstnúmer| Skattflokkur |
    |-------------------------|---------------------|--------------------------|-----------|
    | Færslubók                 |                     |                          | A hópur   |
    | Sala                   |                     | 30160                    | Flokkur B   |
    | Sala                   |                     | 30159                    | Flokkur B   |

4. Birtu útgáfu eiginleika uppsetningar.
5. Í Microsoft Dynamics 365 Fjármál, farðu til **Skattur** \> **Uppsetning** \> **Skattstilling** \> **Skattreikningsbreytur**, og veldu nýju útgáfuna.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
