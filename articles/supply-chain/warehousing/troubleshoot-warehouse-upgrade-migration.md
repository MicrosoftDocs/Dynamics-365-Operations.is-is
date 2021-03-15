---
title: Úrræðaleit fyrir uppfærslu og flutning yfir í ítarlega vöruhúsastjórnun
description: Þetta efnisatriði lýsir því hvernig á að laga almenn vandamál sem kunna að koma upp við uppfærslu og flutning í ítarlega vöruhúsastjórnun.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: dc1c487a608c2e165f5f12aed344cb89fe8d41e1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993883"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a>Úrræðaleit fyrir uppfærslu og flutning yfir í ítarlega vöruhúsastjórnun

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að laga almenn vandamál sem kunna að koma upp við uppfærslu og flutning í ítarlega vöruhúsastjórnun.

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a>Ég fæ eftirfarandi villuboð: "java.security.cert.certPathValidatorException: Traustakkeri fyrir slóð vottorðs finnst ekki."

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þessi villuboð birtast í vöruhúsaforriti vegna þess að sjálfsafgreiddum skírteinum er ekki treyst á Android 8 + í innanhússumhverfi.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Nota ytri (opinberan) útgefanda vottorðs (CA). Lausn fyrir þetta vandamál er í boði í útgáfu 1.9.0.0 af vöruhúsaforritinu. Frekari upplýsingar um þetta vandamál og hvernig á að laga það er að finna á [Úrræðaleit vegna vandamála með tengingu í vöruhúsaforriti](troubleshoot-warehouse-app-connection.md).

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a>Hvert er samþykkt ferli fyrir flutning úr grunnvöruhús í ítarlegt vöruhús?

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Verið er að keyra lager-/birgðastjórnun og nota grunnstillingu lagers og færa á ítarlegt vöruhús til að nýta fartæki, bylgjur og vinnu. Hins vegar kemur upp vandamál þegar reynt er að færa þetta. Til dæmis er ekki hægt að breyta afurðum þannig að þær noti geymsluvíddir (svæði, vöruhús og staðsetning) vegna þess að afurðirnar eru með færslur á móti þeim. Þess vegna þarf að læra samþykkt ferli fyrir flutning frá grunnvöruhúsi í ítarlegt vöruhús.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Frekari upplýsingar um ferlið fyrir flutning frá grunnvöruhúsi í ítarlegt vöruhús er að finna í eftirfarandi bloggfærslum og fylgiskjölum:

- [Virkja ferli vöruhúsastjórnunar fyrir fyrirliggjandi vörur og vöruhús](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [Flutningur á Microsoft Dynamics AX WMS í ný R3 vöruhús og flutningsvirkni](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [WMSI/WMS2 atriðaflutningur](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [Uppfæra vöruhúsastjórnunarferli úr Microsoft Dynamics AX 2012 í Supply Chain Management](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/upgrade-migration-warehouse-management-processes)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]