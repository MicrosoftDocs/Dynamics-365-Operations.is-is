---
title: Umbreyta ósamsettum viðskiptavinum í samstillta viðskiptavini
description: Þessi grein útskýrir hvernig á að breyta ósamstilltum viðskiptavinum í samstillta viðskiptavini í Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: b442bfc0685706359771e4d9e2729565d3652a60
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278193"
---
# <a name="convert-asynchronous-customers-to-synchronous-customers"></a>Umbreyta ósamsettum viðskiptavinum í samstillta viðskiptavini

[!include [banner](includes/banner.md)]

Þessi grein útskýrir hvernig á að breyta ósamstilltum viðskiptavinum í samstillta viðskiptavini í Microsoft Dynamics 365 Commerce.

Til að breyta ósamstilltum viðskiptavinum í samstillta viðskiptavini skaltu fylgja þessum skrefum.

1. Í höfuðstöðvum Commerce, keyrðu **P-starf** að senda ósamstilltu viðskiptavinina til höfuðstöðva Commerce.
1. Keyra á **Samstilltu viðskiptavini og viðskiptafélaga úr ósamstilltu stillingu** starf til að búa til auðkenni viðskiptavinareiknings. (Þetta starf hét áður **Samstilltu viðskiptavini og viðskiptafélaga úr ósamstilltu stillingu** .)
1. Keyra á **1010** starf til að samstilla nýju auðkenni viðskiptavinareiknings við rásirnar.

Ef pöntun vísar í ósamstilltan viðskiptavin eða heimilisfang sem hefur ekki enn verið samstillt við höfuðstöðvar Commerce verður viðskiptavinurinn eða heimilisfangið samstillt sem hluti af **Samstilla pantanir** lotuvinna. Ef reiðufé-og-burðarfærsla vísar til ósamstillts viðskiptamanns eða heimilisfangs, verður viðskiptavinurinn eða heimilisfangið samstillt fyrir lok dags (EOD) færslu.

## <a name="additional-resources"></a>Frekari upplýsingar

[Stjórnun viðskiptavina í verslunum](customer-mgmt-stores.md)

[Ósamstillt stilling til að stofna viðskiptavin](async-customer-mode.md)

[Eigindir viðskiptavinar](dev-itpro/customer-attributes.md)

[Útilokun gagna án nettengingar](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
