---
title: Leggja inn greiðslur viðskiptavina
description: Innborgun á greiðslum viðskiptavina.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7357683e46df04c3dedd7e22607748512c9de94a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220252"
---
# <a name="deposit-customer-payments"></a>Leggja inn greiðslur viðskiptavina

[!include [banner](../../includes/banner.md)]

Innborgun á greiðslum viðskiptavina. Þetta verkefni notar USMF-sýnifyrirtækið.

1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Viðskiptakröfur > Greiðslur > Greiðslubók**.
2. Veljið **Nýtt**.
3. Í reitnum **Heiti** velurðu **CustPay** í fellivalmyndinni.
4. Veldu **Línur**.
5. Í svæðinu **Lykill** velurðu þann viðskiptavin sem verið er að skrá greiðsluna fyrir.
6. Í reitinn **Kredit** skal færa inn upphæð greiðslunnar. Hægt er að velja að hafa upphæð autt, og láta kerfið reikna hann með því að velja þá reikninga sem voru greiddir.  
7. Í reitinn **Greiðslutilvísun** ritarðu gildi. Greiðslutilvísun gætu vero‘ ávísunarnúmer fyrir greiðslu sem eru færðar inn. Greiðslutilvísun er krafist til að taka með greiðslu á innborgunarseðli.  
8. Merkja í reitinn Nota innborgunarseðil. Breyta þessari stillingu á Já ef greiðslan skuli vera með í innborgun.  
9. Veljið **Nýtt**.
10. Í reitinn **Lykill** velurðu viðskiptavin fyrir næstu greiðslu.
11. Í reitinn **Kredit** skal færa inn greiðsluupphæðina.
12. Í reitinn **Greiðslutilvísun** ritarðu gildi.
13. Merktu í reitinn **Nota innborgunarseðil**.
14. Veldu **Bóka**. Verður að bóka greiðslur áður en hægt er að mynda innborgunarseðli. Þetta er til að tryggja að greiðslurnar ekki breytast eftir innborgunarseðils er mynduð.  
15. Veljið **Aðgerðir**.
16. Veldu **Innborgunarseðil**.
17. Veljið **Í lagi**. Fyrsta síða er notuð til að stofna innborgunarseðil.  
18. Veljið **Í lagi**. Önnur skrefið er að prenta innborgunarseðil en þetta skref er ekki nauðsynlegt.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]