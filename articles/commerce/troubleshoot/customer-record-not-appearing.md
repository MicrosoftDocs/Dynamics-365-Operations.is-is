---
title: Færslur viðskiptavinar birtast ekki í Commerce Headquarters
description: Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar færslur viðskiptavinar birtast ekki strax í Commerce Headquarters.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f551f94cec71ba7d740756c383b55741e9f8d42e20e63846ea6242383dc3ba32
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733894"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a>Færslur viðskiptavinar birtast ekki í Commerce Headquarters

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar færslur viðskiptavinar birtast ekki strax í Commerce Headquarters.

## <a name="description"></a>lýsing

Þegar færsla viðskiptavinar er stofnuð með því að nota innskráningarflæðið í netverslun rafrænna viðskipta birtist samsvarandi færsla viðskiptavinar ekki strax í Commerce Headquarters.

## <a name="resolution"></a>Upplausn

### <a name="disable-customer-creation-in-async-mode"></a>Slökkva á stofnun viðskiptavinar í ósamstilltri stillingu

> [!IMPORTANT]
> Ef slökkt er á stofnun ósamstillts viðskiptavinar gætu það haft áhrif á afköst kerfisins vegna þess að stofnun hverrar færslu býr til beiðni í rauntíma í Commerce Headquarters. Auk þess, ef Commerce Headquarters liggur niðri (til dæmis þegar þjónustuflæði er í gangi), mun stofnflæði nýrra viðskiptavina leiða til villu.

Til að slökkva á stofnun viðskiptavinar í ósamstilltri stillingu í Commerce Headquarters skal fylgja þessum skrefum.

1. Farið í **Smásala og viðskipti \> Uppsetning rásar \> Uppsetning netverslunar \> Virknireglur**.
1. Ef ekki er verið að nota virknireglu fyrir netrásina skal stofna slíka.
1. Ganga skal úr skugga um að valkosturinn **Stofna viðskiptavin í ósamstilltri stillingu** sé stilltur á **Nei**.
1. Farið í **Smásala og viðskipti \> Rásir \> Netverslanir**.
1. Veljið netverslunina þar sem á að slökkva á stofnun ósamstillts viðskiptavinar.
1. Í flipanum **Almennt** skal ganga úr skugga um að reiturinn **Virkniregla** sé stilltur á virkniregluna sem verið er að nota fyrir netrásina.

## <a name="additional-resources"></a>Frekari upplýsingar

[Setja upp B2C-leigjanda í Commerce](../set-up-b2c-tenant.md)
