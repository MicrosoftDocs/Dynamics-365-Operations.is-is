---
title: Úrræðaleit fyrir uppfærslu og flutning yfir í ítarlega vöruhúsastjórnun
description: Þetta efnisatriði lýsir því hvernig á að laga almenn vandamál sem kunna að koma upp við uppfærslu og flutning í ítarlega vöruhúsastjórnun.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 12dcadae2a65d71614a2eee9468ec93cac284a7b
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907888"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a>Úrræðaleit fyrir uppfærslu og flutning yfir í ítarlega vöruhúsastjórnun

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að laga almenn vandamál sem kunna að koma upp við uppfærslu og flutning í ítarlega vöruhúsastjórnun.

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a>Ég fæ eftirfarandi villuboð: "java.security.cert.certPathValidatorException: Traustakkeri fyrir slóð vottorðs finnst ekki."

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þessi villuboð birtast í farsímaforriti vöruhúsakerfis vegna þess að sjálfsafgreiddum skírteinum er ekki treyst á Android 8 + í innanhússumhverfi.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Nota ytri (opinberan) útgefanda vottorðs (CA). Lausn fyrir þetta vandamál er í boði í útgáfu 1.9.0.0 af vöruhúsaforritinu. Frekari upplýsingar um þetta vandamál og hvernig á að laga það er að finna á [Úrræðaleit vegna vandamála með tengingu í farsímaforriti vöruhúsakerfis](troubleshoot-warehouse-app-connection.md).

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a>Hvert er samþykkt ferli fyrir flutning úr grunnvöruhús í ítarlegt vöruhús?

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Verið er að keyra lager-/birgðastjórnun og nota grunnstillingu lagers og færa á ítarlegt vöruhús til að nýta fartæki, bylgjur og vinnu. Hins vegar kemur upp vandamál þegar reynt er að færa þetta. Til dæmis er ekki hægt að breyta afurðum þannig að þær noti geymsluvíddir (svæði, vöruhús og staðsetning) vegna þess að afurðirnar eru með færslur á móti þeim. Þess vegna þarf að læra samþykkt ferli fyrir flutning frá grunnvöruhúsi í ítarlegt vöruhús.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Frekari upplýsingar um ferlið fyrir flutning frá grunnvöruhúsi í ítarlegt vöruhús er að finna í eftirfarandi bloggfærslum og fylgiskjölum:

- [Virkja ferli vöruhúsastjórnunar fyrir fyrirliggjandi vörur og vöruhús](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [Flutningur á Microsoft Dynamics AX WMS í ný R3 vöruhús og flutningsvirkni](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [WMSI/WMS2 atriðaflutningur](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [Uppfæra vöruhúsastjórnunarferli úr Microsoft Dynamics AX 2012 í Supply Chain Management](./upgrade-migration-warehouse-management-processes.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]