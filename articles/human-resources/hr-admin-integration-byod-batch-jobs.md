---
title: Fínstilla BYOD-runuvinnslur á áætlun
description: Þetta efnisatriði útskýrir hvernig á að fínstilla frammistöðu þegar þú ert að nota eiginleikann Koma með eigin gagnagrunn (BYOD) með Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-10
ms.dyn365.ops.version: Platform update 36
ms.openlocfilehash: a2f110d105b8c04f07f219f7f11a57d24e00ce4a
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067780"
---
# <a name="optimize-byod-scheduled-batch-jobs"></a>Fínstilla BYOD-runuvinnslur á áætlun


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði útskýrir hvernig á að fínstilla frammistöðu þegar þú ert að nota eiginleikann Koma með eigin gagnagrunn (BYOD). Frekari upplýsingar um BYOD er að finna á [Koma með eigin gagnagrunn (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

## <a name="performance-considerations-for-data-export"></a>Afkastaatriði fyrir gagnaútflutning

Eftir að einingar eru birtar í viðtökugagnagrunni er hægt að nota útflutningseiginleikann á vinnusvæðinu **Gagnastjórnun** til að flytja gögn. Með útflutningseiginleikanum er hægt að skilgreina gagnahreyfingavinnslu sem inniheldur eina eða fleiri einingar. Frekari upplýsingar um gagnaútflutning er að finna í yfirlitinu [Yfirlit yfir inn- og útflutningsvinnslu gagna](../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

Hægt er að nota síðuna **Flytja út** til að flytja út gögn í mismunandi viðtökusniðmáta, svo sem aðskilin gildi fyrir kommu (CSV). Þessi síða styður einnig SQL-gagnagrunna sem annan áfangastað.

Hægt er að stofna gagnaverk sem er með margar einingar og nota runuvinnslu til að stilla keyrslu gagnaverks. Ef valkosturinn **Flytja út í runu** er valinn er hægt að láta gagnaflutningsvinnslu keyra reglulega.

Til að hjálpa til við að varðveita heildaráreiðanleika BYOD-skýrslu verður að gæta varúðar þegar mörgum einingum er bætt við verk sem á að flytja út. Þegar verið er að ákvarða fjölda eininga sem á að bæta við sama verk þarf að hafa eftirfarandi færibreytur í huga:

- Hversu flóknar einingarnar eru
- Væntanlegt gagnamagn á einingu
- Heildartíminn sem er nauðsynlegur til að ljúka við útflutning á verkstigi

Til að fá sem bestan árangur skal forðast að bæta hundruðum eininga við eitt verk. Mælt er með því að stofna margar vinnslur, þar sem hver inniheldur færri einingar.

## <a name="scheduling-byod-batch-jobs"></a>Setja BYOD-runuvinnslur á áætlun

Til að hjálpa til við að draga úr áhrifum á notendur Microsoft Dynamics 365 Human Resources, skal keyra BYOD runuvinnslur á kvöldin eða eftir vinnu. Gætið þess að athuga tímabeltið fyrir endurteknar runuvinnslur. Sumar runuvinnslur nota hugsanlega PST staðaltíma.

Til að koma í veg fyrir frammistöðuvandamál skal huga að eftirfarandi þáttum þegar áætlunartíðnin fyrir BYOD-runuvinnslu er skilgreind:

- Tíminn sem þarf til að ljúka hverri runuvinnslu
- Viðskiptaþörfin fyrir gögnin í BYOD

Stillið tíðni hverrar runuvinnslu á gildi sem tryggir að hægt sé að ljúka vinnslunni vel á undan næsta áætlaða keyrslutíma. Forðist að nota margar vinnslur samhliða, þar sem þessi nálgun getur haft neikvæð áhrif á afköst Human Resources.

Fyrir bestu afköst skal ávallt nota valkostinn **Flytja út í runu** á síðunni **Flytja út** til að áætla BYOD-runuvinnslur. Forðist að áætla endurtekna útflutninga hjá **Stjórna \> Stjórna endurteknum gagnavinnslum**.

## <a name="incremental-export"></a>Stigvaxandi útflutningur

Þegar einingu fyrir gagnaflutning er bætt við er hægt að velja stigvaxandi sendingu (útflutningu) eða fulla sendingu. Full sending eyðir öllum fyrirliggjandi færslum úr einingu í BYOD-gagnagrunninum. Hún setur síðan inn núverandi safn færslna úr mannauðseiningunni.

Til að gera stigvaxandi dreifingu þarf að kveikja á breytingarakningu fyrir hverja einingu á síðunni **Einingar**. Frekari upplýsingar er að finna í [Virkja breytingarakningu fyrir einingar](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

Ef valin er stigvaxandi sending er fyrsta sending alltaf full sending. SQL-rásir breytar frá fyrstu heildarsendingu. Þegar ný færsla er sett inn eða þegar færsla er uppfærð eða henni eytt kemur breytingin fram í viðtökueiningunni.

## <a name="time-outs"></a>Tímamörk

Hér eru sjálfgefin tímamörk fyrir BYOD-útflutning:

- Tíu mínútur fyrir styttingu
- Ein klukkustund fyrir margar innsetningaraðgerðir

Þegar magnið er mikið er hugsanlegt að þessar tímastillingar séu ekki nægilegar. Til að uppfæra þær skal fara í **Gagnastjórnun \> Færibreytur ramma \> Koma með eigin gagnagrunn**. Þessi tímamörk miðast við ákveðið fyrirtæki og þarf að stilla sérstaklega fyrir hvert fyrirtæki.

## <a name="known-limitations"></a>Þekktar takmarkanir

BYDO-eiginleikinn hefur eftirfarandi takmarkanir:

- Ekki ættu að vera neinar virkar læsingar á gagnagrunninum meðan á samstillingu stendur. Virk læsing getur valdið því að skrif verði hæg eða jafnvel að það mistakist að flytja út gögn í Azure SQL-gagnagrunninn.
- Ekki er hægt að flytja samsettar einingar í eigin gagnagrunn. Sem stendur eru samsettar einingar ekki studdar. Þú verður að flytja út einstakar einingar sem mynda samsettu eininguna. Hins vegar er hægt að flytja báðar einingarnar út í sama gagnaverk.
- Ekki er hægt að flytja út einingar sem ekki eru með einstæða lykla með stigvaxandi sendingu. Hugsanlega kemur þessi takmörkun sérstaklega upp þegar reynt er að flytja út færslur úr nokkrum tilbúnum einingum. Vegna þess að einingarnar voru hannaðar fyrir innflutning gagna eru þær ekki með einkvæman lykil.

## <a name="troubleshooting"></a>Úrræðaleit

### <a name="incremental-push-doesnt-work-correctly"></a>Stigvaxandi sending virkar ekki rétt

**Vandamál:** Þegar full seding á sér stað fyrir einingu sést mikið safn færslna í BYOD þegar þú notar **val**. Þegar stigvaxandi sending er notuð sjást hins vegar aðeins nokkrar færslur í BYOD. Það virðist sem stigvaxandi sending hafi eytt öllum færslunum og aðeins bætt við breyttum færslum í BYOD.

**Lausn:** Töflur SQL-breytingarakninga eru hugsanlega ekki í væntanlegri stöðu. Í tilvikum sem þessu er mælt með því að slökkt sé á breytingarakningu fyrir eininguna og kveikja síðan á henni aftur. Frekari upplýsingar er að finna í [Virkja breytingarakningu fyrir einingar](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

### <a name="staging-tables-arent-clearing"></a>Millistigstöflur hreinsast ekki

**Vandamál:** Þegar millistig er notað fyrir verkið hreinsast millistigstöflurnar ekki á réttan hátt. Gögnin í töflunum halda síðan áfram að vaxa, sem leiðir til vandamála með afköst.

**Lausn:** Ferlinum er viðhaldið í sjö daga í millistigstöflunni. Gögn eldri en sjö dagar eru hreinsuð sjálfkrafa úr millistigstöflunni af runuvinnslunni **Hreinsun millistigs innflutnings/útflutnings**. Ef þetta verk festist hreinsast töflurnar ekki á réttan hátt. Ef þessi runuvinnsla er endurræst mun ferlið halda áfram og hreinsa millistigstöfluna sjálfkrafa.

## <a name="see-also"></a>Sjá einnig

[Yfirlit gagnastjórnunar](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[Koma með eigin gagnagrunn (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[Yfirlit yfir inn- og útflutningsvinnslu gagna](../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[Virkja rakningarbreytingu fyrir einingar](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
