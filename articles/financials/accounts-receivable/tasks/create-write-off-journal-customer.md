---
title: Stofna afskriftabók fyrir viðskiptavin
description: Þessi leiðarvísi fyrir verk sýnir hvernig á að setja upp færibreytur fyrir afskriftir og síðan að afskrifa færslur frá síðu Innheimtu, á listasíðu Opna reikninga viðskiptavina og síðu Viðskiptavinar.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cd576458bab1e4654d21773b581a5b0f726c928
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "339810"
---
# <a name="create-a-write-off-journal-for-a-customer"></a>Stofna afskriftabók fyrir viðskiptavin

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi leiðarvísi fyrir verk sýnir hvernig á að setja upp færibreytur fyrir afskriftir og síðan að afskrifa færslur frá síðu Innheimtu, á listasíðu Opna reikninga viðskiptavina og síðu Viðskiptavinar. Þetta verkefni notar USMF-sýnifyrirtækið.


## <a name="set-up-the-write-off-parameters"></a>Setja upp færibreytur afskriftar
1. Farið í Skuldir og innheimta > Uppsetning > Færibreytur viðskiptakrafna.
2. Smellt er á flipanum innheimta.
3. Stækka eða fella saman afskriftarhlutann.
    * Afskriftabók er almennri færslubók sem mun innihalda afskriftafærslur sem eru stofnaðar.  
    * Hægt er að tengja ástæðukóða við hvert afskrift. Hægt er að hnekkja þessari sjálfgefnu gildi við sjálfa afskriftina.  
    * Setja þetta á Já ef óskað er að aðskilja virðisaukaskatts úr upphaflegu færslunnar í afskriftir.  
4. Lokið síðunni.
5. Farið í Skuldir og innheimta > Uppsetning > Bókunarreglur viðskiptavina.
    * Afskriftalykill verður notað sem kostnaðarlykill eða öfug leiðrétting í almennu færslubókinni   
6. Lokið síðunni.

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a>Afskrifa stöðu viðskiptavina af síðunni aldursgreindar stöður
1. Fara í skuldir og innheimta > Innheimta > Aldursgreindar stöður.
2. Merkja línuna fyrir viðskiptavin sem á að afskrifa. Til dæmis að merkja línuna með Birch Fyrirtækisins á því.
3. Í aðgerðasvæðinu er smellt á innheimta.
4. Smellt er á Afskrifa.
5. Smellið á „Í lagi“.
6. Lokið síðunni.
7. Fara í fjárhag > Færslubókarfærslur > Almennar færslubækur.
8. Veljið rununúmer færslubókar fyrir færslubók sem inniheldur afskrift.
    * Ein lína er stofnuð til að snúa við stöðu viðskiptavinar. Ein eða fleiri línur eru stofnaðar til að bóka afskriftir í afskriftarlykil.  
9. Lokið síðunni.
10. Lokið síðunni.

## <a name="write-off-transactions-from-the-collections-form"></a>Afskrifa færslur úr skjámyndinni innheimta.
1. Fara í skuldir og innheimta > Innheimta > Aldursgreindar stöður.
2. Velja nafn viðskiptavinar sem hefur færslur sem á að afskrifa. Veljið til dæmis Cave Wholesales (U.S.-004).
3. Merkja línuna fyrir fyrstu færsluna.
4. Merkja línu fyrir aðra færslu.
5. Smellt er á Afskrifa.
6. Færðu inn 'Lélegar skuldir' í svæði Ástæðuathugasemd.
7. Smellið á „Í lagi“.
8. Lokið síðunni.
9. Lokið síðunni.
10. Fara í fjárhag > Færslubókarfærslur > Almennar færslubækur.
11. Veljið rununúmer færslubókar fyrir færslubók sem inniheldur afskrift.
    * Ein lína er stofnuð til að snúa við stöðu viðskiptavinar. Ein eða fleiri línur eru stofnaðar til að bóka afskriftir í afskriftarlykil.  
12. Lokið síðunni.
13. Lokið síðunni.

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a>Afskrifa reikning frá síðunni Opna reikninga viðskiptavinir 
1. Farið í Viðskiptakröfur > Reikningar > Opna reikninga viðskiptavina.
2. Merkja línu fyrir reiknings. Til dæmis að merkja línuna fyrir CIV 000667.
3. Smellið á „Reikningur“ á aðgerðarúðunni.
4. Smellt er á Afskrifa.
5. Smellið á „Í lagi“.
6. Lokið síðunni.

## <a name="write-off-a-customer-balance-from-the-customer-page"></a>Afskrifa staða viðskiptavinar á síðu viðskiptavinar
1. Farið í Viðskiptakröfur > Viðskiptavinir > Allir viðskiptavinir.
2. Veljið viðskiptavinalykil. Veljið til dæmis U.S.-001 (Contoso Retail San Diego).
3. Í aðgerðasvæðinu er smellt á innheimta.
4. Smellt er á Afskrifa.
5. Smellið á „Í lagi“.
6. Lokið síðunni.

