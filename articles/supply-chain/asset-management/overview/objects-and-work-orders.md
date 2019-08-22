---
title: Eignir og verkbeiðnir
description: Þetta efni lýsir eignum og verkbeiðnum í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5bd55988578be2b0287b399549f17642bfb1693b
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783344"
---
# <a name="assets-and-work-orders"></a>Eignir og verkbeiðnir

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Þetta efni lýsir eignum og verkbeiðnum í eignastýringu. Eignir og verkbeiðnir eru meginhlutir eignastýringar. *Eign* er vél eða vélarhluti sem krefst stöðugs viðhalds og þjónustu. Hægt er að búa til eignir í stigveldisskipulagi og þær geta tengst virkum stöðum. Viðhaldsstörf geta verið áætluð á öllum stigum eignaskipulagsins.

Ýmis gögn, svo sem vöruupplýsingar og eignaskilgreining, og nauðsynlegar viðhaldsáætlanir eru settar upp um hverja eign. Eftirfarandi mynd sýnir yfirlit yfir eignargögn og tengingu eigna við starfstegundir. Rauður texti er notaður fyrir dæmi sem sýna arf og háð.

![Mynd 1](media/05-overview-image.png)

Sérhver verkbeiðni er með gerð af verkbeiðni, svo fyrirbyggjandi viðhald, úrbótaviðhald eða skoðun. Verkbeiðnin inniheldur eitt eða fleiri störf í verkbeiðni. Sérhver starf í verkbeiðni skilgreinir starf sem þarf að framkvæma á eign og tengda starfstegund. Dæmi um skyldar starfstegundir eru 10.000 km, 50.000 km, 1 árs yfirferð og öryggisskoðun. Ein verkpöntun getur tengst mörgum eignum.

Eftirfarandi mynd sýnir yfirlit yfir lykilgögnin í verkbeiðni.

![Mynd 2](media/06-overview-image.png)

Verkbeiðnin getur verið tengt annarri verkbeiðni og starfstegundir geta innihaldið störf sem hafa náð árangri sem skapa verkbeiðni. Almennt eru engin háð á milli verkbeiðna. Þess vegna geta þeir breytt líftímastöðum verkbeiðni og hægt er að skipuleggja þær óháð hvor annarri.

Verkbeiðnir geta verið búnar til á ýmsa vegu sem tengjast lagfærandi, fyrirbyggjandi eða viðbrögðum viðhaldi. Einnig er hægt að stofna verkbeiðnir handvirkt. Eftirfarandi mynd sýnir yfirlit yfir ferlið við sjálfvirka eða handvirka stofnun verkbeiðna.

![Mynd 3](media/07-overview-image.png)

Nokkrum skrefum verður að vera lokið þegar þú vilt skipuleggja og keyra viðhaldsstörf í verkbeiðni. Eftirfarandi mynd sýnir yfirlit yfir vinnslu fyrir verkbeiðni.

![Mynd 4](media/08-overview-image.png)

> [!NOTE]
> Almennt þegar þú vinnur í Microsoft Dynamics 365 for Finance and Operations og einingunni **Eignastýring** velurðu **Nýtt** til að búa til nýja skrá, velur **Breyta** til að uppfæra fyrirliggjandi skrá og þú velur **Vista** til að vista ný eða breytt gögn.
