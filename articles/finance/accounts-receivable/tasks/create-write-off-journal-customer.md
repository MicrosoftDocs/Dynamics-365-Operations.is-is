---
title: Stofna afskriftabók fyrir viðskiptavin
description: Þessi leiðarvísi fyrir verk sýnir hvernig á að setja upp færibreytur fyrir afskriftir og síðan að afskrifa færslur frá síðu Innheimtu, á listasíðu Opna reikninga viðskiptavina og síðu Viðskiptavinar.
author: ShivamPandey-msft
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7da01759fe4aaa7beb1719ede51ac0abfc3b404c
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713672"
---
# <a name="create-a-write-off-journal-for-a-customer"></a>Stofna afskriftabók fyrir viðskiptavin

[!include [banner](../../includes/banner.md)]

Þessi leiðarvísi fyrir verk sýnir hvernig á að setja upp færibreytur fyrir afskriftir og síðan að afskrifa færslur frá síðu Innheimtu, á listasíðu Opna reikninga viðskiptavina og síðu Viðskiptavinar. Þetta verkefni notar USMF-sýnifyrirtækið.


## <a name="set-up-the-write-off-parameters"></a>Setja upp færibreytur afskriftar
1. Farðu í **Skoðunarrúða > Kerfi > Skuldir og innheimta > Uppsetning > Færibreytur viðskiptakrafna**.
2. Smelltu á flipann **Innheimta**.
3. Stækka eða fella saman hlutann **afskriftir**.
    - **Afskriftabók** er almenn færslubók sem mun innihalda afskriftafærslur sem eru stofnaðar.  
    - Hægt er að tengja ástæðukóða við hvert afskrift. Hægt er að hnekkja þessari sjálfgefnu gildi við sjálfa afskriftina.  
    - Stilltu **Virðisaukaskattur aðskilinn** á Já ef óskað er að aðskilja virðisaukaskatt úr upphaflegri færslu í afskriftum.  
4. Lokið síðunni.
5. Farið í **Skuldir og innheimta > Uppsetning > Bókunarreglur viðskiptavina**. Afskriftalykill verður notað sem kostnaðarlykill eða öfug leiðrétting í almennu færslubókinni.
6. Lokið síðunni.

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a>Afskrifa stöðu viðskiptavina af síðunni aldursgreindar stöður
1. Fara í **skuldir og innheimta > Innheimta > Aldursgreindar stöður**.
2. Merkja línuna fyrir viðskiptavin sem á að afskrifa. Til dæmis að merkja línuna með Birch Fyrirtækisins á því.
3. Í **aðgerðasvæðinu** er smellt á **Innheimta**.
4. Smellt er á **Afskrifa**.
5. Smellt er á **OK**.
6. Lokið síðunni.
7. Farðu í **skoðunarrúðuna > Kerfiseiningar > Fjárhagur > Bókarfærslur > Almennar færslubækur**.
8. Veljið rununúmer færslubókar fyrir færslubók sem inniheldur afskrift. Ein lína er stofnuð til að snúa við stöðu viðskiptavinar. Ein eða fleiri línur eru stofnaðar til að bóka afskriftir í afskriftarlykil.  
9. Lokið síðunni.
10. Lokið síðunni.

## <a name="write-off-transactions-from-the-collections-form"></a>Afskrifa færslur úr skjámyndinni innheimta.
1. Fara í **skuldir og innheimta > Innheimta > Aldursgreindar stöður**.
2. Velja nafn viðskiptavinar sem hefur færslur sem á að afskrifa. Veljið til dæmis Cave Wholesales (U.S.-004).
3. Merkja línuna fyrir fyrstu færsluna.
4. Merkja línu fyrir aðra færslu.
5. Smellt er á **Afskrifa**.
6. Færðu inn 'Lélegar skuldir' í svæði **Ástæðuathugasemd**.
7. Smellt er á **OK**.
8. Lokið síðunni.
9. Lokið síðunni.
10. Farðu í **Fjárhag > Færslubókarfærslur > Almennar færslubækur**.
11. Veljið rununúmer færslubókar fyrir færslubók sem inniheldur afskrift. Ein lína er stofnuð til að snúa við stöðu viðskiptavinar. Ein eða fleiri línur eru stofnaðar til að bóka afskriftir í afskriftarlykil.  
12. Lokið síðunni.
13. Lokið síðunni.

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a>Afskrifa reikning frá síðunni Opna reikninga viðskiptavinir
1. Farðu í **Skoðunarrúðu > Einingar > Viðskiptakröfur > Reikningar > Opnir reikningar viðskiptavina**.
2. Merkja línu fyrir reiknings. Til dæmis að merkja línuna fyrir CIV 000667.
3. Í **aðgerðasvæðinu** er smellt á **Reikningur**.
4. Smellt er á **Afskrifa**.
5. Smellt er á **OK**.
6. Lokið síðunni.

## <a name="write-off-a-customer-balance-from-the-customer-page"></a>Afskrifa staða viðskiptavinar á síðu viðskiptavinar
1. Farið í **Viðskiptakröfur > Viðskiptavinir > Allir viðskiptavinir**.
2. Veljið viðskiptavinalykil. Veljið til dæmis U.S.-001 (Contoso Retail San Diego).
3. Í **aðgerðasvæðinu** er smellt á **Innheimta**.
4. Smellt er á **Afskrifa**.
5. Smellt er á **OK**.
6. Lokið síðunni.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
