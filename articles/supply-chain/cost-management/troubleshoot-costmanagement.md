---
title: Úrræðaleit fyrir kostnaðarstjórnun
description: Þetta efnisatriði lýsir því hvernig á að leysa vandamál sem kunna að koma upp á meðan unnið er með kostnaðarstjórnun.
author: AndersGirke
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: fc6a48a44a529c82c2a9ee818af95569d9bcb249
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834290"
---
# <a name="troubleshoot-cost-management"></a>Úrræðaleit fyrir kostnaðarstjórnun

Þetta efnisatriði lýsir því hvernig á að leysa vandamál sem kunna að koma upp á meðan unnið er með kostnaðarstjórnun.

## <a name="functional-gaps-between-the-inventory-valueaging-reports-and-their-storage-versions"></a>Virknigloppur á milli birgðavirðis/aldursgreiningaskýrslna og geymsluútgáfa þeirra

Eiginleikarnir [Skýrsla um aldursgreiningu birgða](inventory-aging-report-storage.md) og [Skýrsla um birgðavirði í geymslu](inventory-value-report-storage.md) gerir Supply Chain Management kleift að birta mikinn fjölda birgðafærslna. Í hverju tilviki fyrir eru niðurstöður skýrslugjafar fyrir leit og útflutning, ólíkt því sem gert er við útgáfur þessara skýrslna sem eru ekki til geymslu. Hins vegar er tiltekin virkni til staðar í útgáfum þessara skýrslna sem eru ekki til geymslu sem eru ekki til staðar í geymsluútgáfunum. Í eftirfarandi undirköflum er fjallað um mismuninn og boðið upp á hjáleið.

### <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>Geymsluskýrslur innihalda ekki millisamtölur, jafnvel þótt þær séu virkar í skýrsluútlitinu

Millisamtölur geta valdið vandamálum þegar niðurstaðan er flutt út, sérstaklega ef notendur breyta færslustöðinni.

Til að skoða millisamtölur er hægt að flytja niðurstöðuna út í Microsoft Excel. Að öðrum kosti ef þú vilt athuga millisamtölur innan Supply Chain Management skaltu nota [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að virkja eiginleikana *Ný hnitanetsstjórnun* og *Hópar í hnitanetum* sem gefa upp mun sveigjanlegri leið til að sjá millisamtölu fyrir alla flokka eftir dálki. Nánari upplýsingar eru að finna í [Möguleikar hnitanets](../../fin-ops-core/fin-ops/get-started/grid-capabilities.md).

### <a name="inventory-value-storage-report-doesnt-support-ledger-account-information"></a>Skýrsla um birgðavirði í geymslu styður ekki upplýsingar um fjárhagslykil

Hægt er að keyra prófjöfnuð til að fá stöðu birgðalykla og bera saman við **Skýrslu um birgðavirði í geymslu** .

## <a name="warnings-or-errors-are-shown-when-changing-a-ledger-period-status-without-closing-inventory"></a>Viðvaranir eða villur birtast þegar skipt er um stöðu fjárhagstímabils án lokunar birgða

Microsoft kynnti eftirfarandi villuleit til að koma í veg fyrir vandamál sem stafa af röngu endaferli tímabils í kostnaðarútreikningi. Þegar einhver af eftirfarandi villuboðum koma upp finnur þú frekari upplýsingar í [KB 4561987](https://fix.lcs.dynamics.com/Issue/Details?kb=4561987&bugId=445351&dbType=3&qc=f514f2adcddcddceec43af58c26ae8a9020effdc7cdfe085d9d0deeb8cc7b6a3) um hvernig eigi að leysa úr þessum vandamálum.

- Þú ert að fara að framkvæma endurútreikning með dagsetningu %1 (02-10-2019). Síðasti skráði endurútreikningur var keyrður á fyrra tímabili með dagsetningu %2 (20-01-2019). Engin keyrsla á birgðalokun með dagsetningu %3 (31-01-2019) sem samsvarar tímabilslokum hefur verið skráð. Mundu að keyra birgðalokun frá %3 (31-01-2019) sem samsvarar lokum tímabilsins. Mat á birgðum, kostnaði seldra vara og frávikum er hugsanlega ekki rétt í undirbók eða fjárhag fyrr en þetta hefur verið keyrt.

- Þú ert að fara að breyta stöðu fjárhagstímabils %1 í %2. Engin lok birgðalokunaráætlunar með dagsetningu %3 samsvarandi tímabils hefur verið skráð. Munið að keyra birgðalokun frá %3 sem samsvarar lokum tímabilsins áður en stöðunni er breytt. Mat á birgðum, kostnaði seldra vara og frávikum er hugsanlega ekki rétt í undirbók eða fjárhag fyrr en þetta hefur verið keyrt. Tilkynnt frá lögaðila %4. Þetta er aðeins til upplýsinga eins og er en þú þarft að framkvæma slíka aðgerð í framtíðinni.

- Lykilskipulaginu %1 hefur verið breytt. Einn eða fleiri aðallyklar %2 eru ekki lengur til. Þessir aðallyklar eru nauðsynlegir af %3 með %4 dagsetningu. Bæta skal þessum aðallyklum við lykilskipulagið %1 áður en hægt er að halda áfram í %3 vinnslunni. Þetta er aðeins til upplýsinga eins og er en þú þarft að framkvæma slíka aðgerð í framtíðinni.

- Þú ert að fara að framkvæma birgðalokun með dagsetningu %1 (31-01-2019). Engin keyrsla á bakfærslukostnaðaraðferð útreiknings með dagsetningu %2 (31-01-2019) sem samsvarar tímabilslokum hefur verið skráð. Munið að keyra bakfærslukostnaðaraðferð með dagsetningu á %3 (31-01-2019) sem samsvarar lokun tímabilsins. Mat á birgðum, kostnaði seldra vara og frávikum er hugsanlega ekki rétt í undirbók eða fjárhag fyrr en þetta hefur verið keyrt.

- Þú ert að fara að framkvæma útreikning bakfærslukostnaðaraðferðar með dagsetningu %1 (28-02-2019). Síðasti skráði útreikningur bakfærslukostnaðaraðferðar var keyrður á fyrra tímabili með dagsetningu %2 (31-01-2019). Engin keyrsla á birgðalokun með dagsetningu %3 (31-01-2019) sem samsvarar lokum tímabils hefur verið skráð.
Munið að keyra birgðalokun frá %3 (31-01-2019) sem samsvarar lokum tímabilsins. Mat á birgðum, kostnaði seldra vara og frávikum er hugsanlega ekki rétt í undirbók eða fjárhag fyrr en birgðalokun hefur verið keyrð.

## <a name="inventory-aging-report-discrepancies"></a>Ósamræmisskýrsla um aldursgreiningu birgða

**Skýrsla um aldursgreiningu birgða** sýnir ólík gildi þegar hún er skoðuð í mismunandi geymsluvíddum (t.d. svæði eða vöruhúsi). Frekari upplýsingar um skýrslurökin er að finna í [Dæmi og rök fyrir aldursgreiningarskýrslu birgða](inventory-aging-report.md).

## <a name="an-update-conflict-occurs-when-the-inventory-valuation-method-is-either-standard-cost-or-moving-average"></a>Árekstur við uppfærslu gerist þegar aðferð birgðamats er annaðhvort staðalkostnaður eða hlaupandi meðaltal

Þegar bókuð eru skjöl á borð við birgðabækur, innkaupapöntunarreikningar eða sölupöntunarreikningar samhliða fyrir sveigjanleika og afköst, gætu komið upp villuboð um árekstur við uppfærslu og sum skjalanna verða hugsanlega ekki bókuð. Þetta vandamál getur komið upp þegar aðferð birgðamats er annaðhvort *Staðalkostnaður* eða *Hlaupandi meðaltal*. Báðar þessar aðferðir eru varanlegar kostnaaðaraðferðir. Með öðrum orðum er endanlegur kostnaður ákvarðaður á þeim tíma sem bókað er.

Ef verið er að nota aðferðina *Hlaupandi meðaltal* líkjast villuboðin þessu dæmi:

> Ekki er búist við birgðavirði xx.xx eftir hlutfallslegan kostnaðarútreikning

Ef verið er að nota aðferðina *Staðlaður kostnaður* kostnaðaraðferð líkjast villuboðin þessu dæmi:

> Staðalkostnaður stemmir ekki við gildi fjárhagslegra birgða eftir uppfærsluna. Gildi = xx.xx, magn = yy.yy, staðalkostnaður = zz.zz

Þar til Microsoft gefur út lausn til að laga vandamálið er mögulegt að nota eftirfarandi hjáleið til að forðast eða draga úr þessum villum:

- Endurbókið skjölin sem mistókust.
- Stofna skjöl sem eru með færri línum.
- Forðast skal tugabrot í staðalkostnaði. Reynið að skilgreina staðalkostnaðinn þannig að reiturinn **Magn í verði** sé stilltur á *1*. Ef tilgreina þarf gildi fyrir **Magn í verði** sem er meira en *1* skal reyna að lágmarka fjölda aukastafa í staðalkostnaði einingarinnar. (Helst ættu að vera færri en tveir aukastafir.) Til dæmis skal forðast að skilgreina stillingar staðalkostnaðar á borð við **Verð** = *10* og **Magn í verði** = *3* vegna þess að þær munu leiða til staðalkostnaðar á einingu sem er 3,333333 (þar sem gildi aukastafs endurtekur sig).
- Í flestum skjölum skal forðast að hafa margar línur sem geyma sömu samsetningu afurðar- og fjárhagsbirgðavídda.
- Dragið úr fjölda á samhliða vinnslum. (Í þessu tilviki gæti kerfið orðið fljótara þar sem færri árekstrar við uppfærslu og endurtekningar koma upp.)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]