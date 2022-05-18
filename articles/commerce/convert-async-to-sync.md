---
title: Umbreyta ósamsettum viðskiptavinum í samstillta viðskiptavini
description: Þetta efnisatriði útskýrir hvernig á að breyta ósamstilltum viðskiptavinum í samstillta viðskiptavini í Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: fc1690ff6068317c748bda0d767a10f306f3debe
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691445"
---
# <a name="convert-asynchronous-customers-to-synchronous-customers"></a>Umbreyta ósamsettum viðskiptavinum í samstillta viðskiptavini

[!include [banner](includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að breyta ósamstilltum viðskiptavinum í samstillta viðskiptavini í Microsoft Dynamics 365 Commerce.

Til að breyta ósamstilltum viðskiptavinum í samstillta viðskiptavini skaltu fylgja þessum skrefum.

1. Í höfuðstöðvum Commerce, keyrðu **P-starf** að senda ósamstilltu viðskiptavinina til höfuðstöðva Commerce.
1. Keyra á **Samstilltu viðskiptavini og viðskiptafélaga úr ósamstilltu stillingu** starf til að búa til auðkenni viðskiptavinareiknings. (Þetta starf hét áður **Samstilltu viðskiptavini og viðskiptafélaga úr ósamstilltu stillingu** .)
1. Keyra á **1010** starf til að samstilla nýju auðkenni viðskiptavinareiknings við rásirnar.

Ef pöntun vísar í ósamstilltan viðskiptavin eða heimilisfang sem hefur ekki enn verið samstillt við höfuðstöðvar Commerce verður viðskiptavinurinn eða heimilisfangið samstillt sem hluti af **Samstilla pantanir** lotuvinna. Ef reiðufé-og-burðarfærsla vísar til ósamstilltans viðskiptamanns eða heimilisfangs, verður viðskiptavinurinn eða heimilisfangið samstillt fyrir lok dags (EOD) færslu.

## <a name="additional-resources"></a>Frekari upplýsingar

[Stjórnun viðskiptavina í verslunum](customer-mgmt-stores.md)

[Ósamstillt stilling til að stofna viðskiptavin](async-customer-mode.md)

[Eigindir viðskiptavinar](dev-itpro/customer-attributes.md)

[Útilokun gagna án nettengingar](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
