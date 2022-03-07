---
title: Svæðisvalseining
description: Þetta efnisatriði fjallar um svæðisvalseininguna og útskýrir hvernig á að bæta henni við síður á vefsvæði Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: b4e5f715efcac7f883df99508d282db904be0d80
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665224"
---
# <a name="site-selector-module"></a>Svæðisvalseining

[!include [banner](includes/banner.md)]

Þetta efnisatriði fjallar um svæðisvalseininguna og útskýrir hvernig á að bæta henni við síður á vefsvæði Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Þegar fyrirtæki er með ólík svæði á mörkuðum, svæði og staðhætti þurfa notendur svæðis að skipta á milli svæða og velja æskilegt verslunarsvæði á einfaldan hátt. Til að mæta þessari atburðarás gerir svæðarvaleiningin kleift að fletta á mörgum svæðum.

Grunnkerfi svæðisins verður að skilgreina með lista yfir svæði (markaði, svæði eða svæði) sem notendur svæðisins geta flett í.

> [!NOTE]
> Svæðisvalseiningin er tiltæk í Dynamics 365 Commerce útgáfu 10.0.14.

Eftirfarandi mynd sýnir dæmi um færibreytueiningu sem er valin í haus vefsíðu.

![Dæmi um val á svæðiseiningu í haus vefsíðu](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a>Eiginleikar svæðisvalseiningar

| Nafn eiginleika | Virði                 | lýsing |
|---------------|-----------------------|-------------|
| Fyrirsögn       | Texti                  | Fyrirsögn einingarinnar. |
| Vefsvæðakostir  | Nafn, mynd, URL      | Þessi eiginleiki tilgreinir heiti, tengil á heimasíðu svæðisins og valfrjálsa mynd til að sýna fyrir hvert svæði sem er tekið með í einingunni. Myndin getur verið flagg eða einhver framsetning á markaði, svæði eða staðháttum. |

## <a name="add-a-site-selector-module-to-a-page"></a>Bæta svæðisvalseiningu við síðu

Hægt er að bæta við svæðisvalseiningu í [Hauseiningu](author-header-module.md) undir vali á svæði. Eftir að því er bætt við er hægt að skilgreina fyrirsögn einingar og svæði.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Eining síðuhauss](author-header-module.md)

[Brauðmylsnueining](add-breadcrumb.md)

[Eining yfirlitsvalmyndar](nav-menu-module.md)
