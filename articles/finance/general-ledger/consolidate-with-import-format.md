---
title: Innflutningssnið fyrir sameiningu
description: Í þessu efnisatriði er að finna ítarlegar upplýsingar um innflutningssniðið sem notað er við sameiningu fjárhagsgagna úr mörgum lögaðilum.
author: jinniew
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 714c34dfcd109a442a4ecd741409dea5c4aade20
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216807"
---
# <a name="import-format-for-consolidation"></a>Innflutningssnið fyrir sameiningu

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er að finna ítarlegar upplýsingar um innflutningssniðið sem notað er við sameiningu fjárhagsgagna úr mörgum lögaðilum. Vista þarf innflutningssniðið sem textaskrá (.txt).

## <a name="import-format"></a>Innflutningssnið

Í eftirfarandi töflu er listi yfir innflutningssniðin sem á að nota þegar gerð er sameining meðan á innflutningi stendur.

| Færslutafla | Snið | Athugasemdir |
|--------------|---------|-------|
| 1            | 170150, viðskiptavild, 4 | <ul><li>Færslutaflan</li><li>Upprunakenni aðallykils</li><li>Lína aðallykilsins</li><li>Gerð aðallykilsins</li></ul> |
| 2            | 110130, 2015/01/01, 1, USD, 0,0,80699.39,0,1 | <ul><li>Kenni aðallykilsins</li><li>Færsludagsetningin</li><li>Gerð fjárhagstímabilsins (**0** = opnun, **1** = í gangi og **2** = lokun)</li><li>Færslugjaldmiðillinn</li><li>Debet eða kredit (**0** = debet og **1** = kredit)</li><li>Bókunarlagið</li><li>Færsluupphæðir</li><li>Magn</li><li>Staðbundið RecId (tvírætt, einkvæmt int64 gildi fyrir færsluna)</li></ul> |
| 3            | USMF0000009, 2017/01/01, FY2017, 1, 2017,01,01, 602200, USD, 6053.6.0 | <ul><li>Færslunúmerið (færslunúmer fjárhagsáætlunarhauss)</li><li>Sjálfgefin dagsetning fjárhagsáætlunarhauss</li><li>Kenni fjárhagsáætlunarlíkansins</li><li>Gerð fjárhagsáætlunar (**1** - Upprunaleg fjárhagsáætlun, **2** - Flutningur, **3** - Endurskoðun, **4** - Fjárúthlutun, **5** - Áætluð fjárúthlutun, **6** - Fjárhagsáætlun frá fyrra tímabili, **7** - Verk, **8** - Eignir, **9** - Eftirspurnarspá, **10** - Birgðaspá, **11** - Skiptingar, **12** - Bráðabirgðafjárhagsáætlun.)</li><li>Dagsetning línunnar</li><li>Kenni aðallykils fyrir línuna</li><li>Gjaldmiðilskóði fyrir línuna</li><li>Upphæð línunnar, í færslugjaldmiðlinum</li><li>Heiltölugildi tölusetningar fyrir fjárhagsáætlunargerð línunnar (kostnaður eða tekjur)</li></ul> |
| 4            | DEMF | RecordCompany er upprunalegur lögaðili. |
| 5            | 110130, 2015/01/01, 1, USD, 0,0,80699.39,0,1 | <ul><li>Kenni aðallykils</li><li>Færsludagsetning</li><li>Gerð fjárhagstímabils (0 Opnun, 1 Rekstur, 2 Lokun)</li><li>Gjaldmiðill færslu</li><li>Debet- eða kredit (0 fyrir debet, 1 fyrir kredit)</li><li>Bókunarlag</li><li>Færsluupphæð</li><li>Magn</li><li>Staðbundið recid (tvírætt, einkvæmt int64 gildi fyrir færsluna)</li></ul>  |
| 6            | BusinessUnit, 1 deild, 2 | Eigindir fjárhagsvíddar sem eru skilgreindar í hlutaröðinni.<p>Hægt er að nota síðuna **Flytja út** til að staðfesta hvernig eigindirnar eru skilgreindar.</p> |
| 7            | 002,1,658 | <ul><li>Fjárhagsvíddargildið</li><li>Fjárhagsvíddin, sem vísirinn sem boðið er upp á í RecordDimensions</li><li>Tvírætt, einkvæmt færslukenni sem tengist einkvæmu færslukenni úr RecordTrans eða RecordTrans2</li></ul> |
| 8            | 002,1,1 | <ul><li>Víddargildi sem tengjast færslunni úr RecordBudget</li><li>Fjárhagsvíddin, sem vísirinn sem boðið er upp á í RecordDimensions</li><li>Tvírætt færslukenni línu sem er stillt upp með pöntun færslulínanna í skránni</li></ul> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
