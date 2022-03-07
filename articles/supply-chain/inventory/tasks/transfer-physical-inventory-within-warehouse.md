---
title: Flytja efnislegar birgðir innan vöruhúss
description: Þetta ferli fer í gegnum ferlið fyrir stofnun og bókun á birgðaflutningabók til að skrá hreyfingar vöru úr einni staðsetningu í vöruhúsi í annað.
author: yufeihuang
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf5a3711cfcd6e5a2ddce09af8569ea26c3502c8
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580793"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a>Flytja efnislegar birgðir innan vöruhúss

[!include [banner](../../includes/banner.md)]

Þetta ferli fer í gegnum ferlið fyrir stofnun og bókun á birgðaflutningabók til að skrá hreyfingar vöru úr einni staðsetningu í vöruhúsi í annað. Þú þarft að hafa með heiti birgðabókarinnar sett upp fyrir birgðaflutning áður en byrjað er að þetta. Hægt er að fara í gegnum þessu ferli í sýnigögn fyrirtækisins USMF með notkun dæmagilda sem eru sýndar eða með því að nota eigin gögn ef afurðir og staðsetningar eru uppsettar. Þessi verkefni eru venjulega framkvæmd af starfsmanni í vöruhúsi.


## <a name="create-an-inventory-transfer-journal"></a>Stofna færslubóka fyrir birgðaflutning
1. Í **Skoðunarrúðu** ferðu í **Birgðastjórnun > Færslubókarfærslur > Vörur > Flutningur**.
2. Smellt er á **Nýtt**.
3. Sláið inn eða veldu gildi í reitnum **Heiti**.
4. Smellt er á **OK**. Það er að valkostur um að tilgreina 'Frá' og ''til“ vídda fyrir hverja færslubókarlínu. Þetta eru mikilvægar fyrir gerð færslubókar. Hægt er að flytja vörur á staði með mismunandi reglur. Í þessu dæmi munum við flytja vöru innan sama vöruhús, frá númeraplötustýrð staðsetningu á staðsetningu sem ekki er númeraplötustýrð.   

## <a name="create-journal-lines"></a>Stofna færslubókarlínur
1. Í flýtiflipanum **Færslubókarlínur** smellirðu á **Nýtt**.
2. Í reitinn **Vörunúmer** skal slá inn eða velja gildi. Ef verið er að nota USMF er hægt að velja 'A0001'.  
3. Í reitinn **Frá svæði** skal slá inn eða velja gildi. Ef verið er að nota USMF er hægt að velja '2'.  
4. í reitinn **Til svæðis** skal slá inn eða velja gildi. Ef verið er að nota USMF er hægt að velja '2'.  
5. Í reitinn **Úr vöruhúsi** skal slá inn eða velja gildi. Ef verið er að nota USMF er hægt að velja '24'.  
6. Í reitinn **Í vöruhús** skal slá inn eða velja gildi. Ef verið er að nota USMF er hægt að velja '24'.  
7. Í reitinn **Frá staðsetningu** skal slá inn eða velja gildi. Ef verið er að nota USMF er hægt að velja 'FL-001'.  
8. Í reitinn **Til staðsetningar** skaltu færa inn eða velja gildi. Ef verið er að nota USMF er hægt að velja ‚BULK-001'.  
9. Í reitnum **Magn** slærðu inn tölu.
10. Í flýtiflipanum **Línulýsing** smellirðu á flipann **Birgðavíddir**.
11. Í **Frá birgðavíddum**, í reitnum **Númeraplata** skaltu slá inn eða velja gildi. Ef verið er að nota USMF er hægt að velja '24'.  
12. Smellt er á **Vista**.

## <a name="post-the-inventory-transfer-journal"></a>Bóka færslubóka fyrir birgðaflutning
1. Á **aðgerðasvæðinu** er smellt á **Bóka**.
2. Smellt er á **OK**.

## <a name="view-inventory-transactions"></a>Skoða birgðafærslur
1. Smelltu á **Birgðir**.
2. Smelltu á **Færslur**. Hér er hægt að sjá færslurnar sem voru stofnaðar þegar þitt færslubók var bókuð.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]