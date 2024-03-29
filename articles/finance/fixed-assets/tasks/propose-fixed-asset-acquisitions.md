---
title: Stinga upp á eignakaupum
description: Þessi grein lýsir hvernig á að kaupa eignir með því að nota kauptillögu í færslubók eigna.
author: moaamer
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 35d2171dc828cb0227f310e81be1d3e3359f41c5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909070"
---
# <a name="propose-fixed-asset-acquisitions"></a>Stinga upp á eignakaupum

[!include [banner](../../includes/banner.md)]

Þessi grein lýsir hvernig á að kaupa eignir með því að nota kauptillögu í færslubók eigna. Það notar Bókari hlutverk og sýnigögn fyrir USMF lögaðila. Til að komast yfir eign í gegnum tillögubók eignar, þarf fyrst að stofna eignafærsluna og síðan skilgreina kaupverð í eignabókinni.

## <a name="create-an-asset-acquisition-proposal"></a>Stofna tillögu að eignakaupum

Ljúkið eftirfarandi skrefum til að búa til eignaskiptatillögu. 

1. Í skoðunarrúðnni ferðu í **Kerfseiningar > Fastafjármunir > Dagbókarfærslur > Dagbók fastafjármuna**.
2. Veljið **Nýtt**.
3. Sláið inn eða veldu gildi í reitnum **Heiti**.
4. Í aðgerðarúðunni velurðu **Línur**.
5. Veldu **Tillögur**.
6. Veldu **Kauptillaga**.
7. Velja **Síu**. Veljið **Endurstilla** til að hreinsa út fyrri gildi.
8. Veljið línuna **Númer eignar**.
9. Í reitinn **Skilyrði** skal slá inn eða velja gildi. Stilla eftirstandandi skilyrði eigna sem óskað er að öðlast með þessari greiðslutillögu.  
10. Veldu **Í lagi** tvisvar til að fara út úr rúðunni.
- Ganga skal úr skugga um að færslulínurnar séu stofnaðar.  
- Aðeins eignir með kaupdag og kaupverðið settar á bókinni verða teknar með í kauptillögu.  
11. Á síðunni velurðu flipann **Bækur**.
12. Veldu **Bóka**.

## <a name="include-default-financial-dimensions-in-an-acquisition-proposal"></a>Hafa sjálfgefnar fjárhagsvídd með í kauptillögu

Hægt er að búa til kaupfærsluna með því að nota Excel-innbætur með því að fara í **Eignir > Bókarfærslur > Eignabók**. Stofnið nýja færslubók og færið í **Línur** hlutann á síðunni og veljið Excel-táknið og síðan eignabókarlínu. Kerfið býr til og opnar Excel-sniðmát sem táknar færslubókarlínur. Hægt er að bæta við gögnum fyrir færslubókarlínurnar sem verið er að bæta við sniðmátið og birta svo upplýsingarnar aftur í kerfið. 

Ef sjálfgefnar víddir hafa verið settar upp fyrir valda eignabók og samsvarandi eignir sem voru færðar inn í Excel-sniðmátið, verða sjálfgefnar fjárhagsvíddir sóttar úr aðalgögnum eignabókar þegar færslubókin er birt úr Excel í kerfið. Til að taka sjálfkrafa með fjárhagsvídd í eignabók við birtingu á færslubók eigna úr Excel-innbótinni verður að setja upp sjálfgefnar víddir fyrirfram.  


[!INCLUDE [footer-include](../../../includes/footer-banner.md)]
