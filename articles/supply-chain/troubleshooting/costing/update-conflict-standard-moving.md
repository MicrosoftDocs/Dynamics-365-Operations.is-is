---
title: Árekstur við uppfærslu þegar aðferð birgðamats er staðalkostnaður eða hlaupandi meðaltal
description: Árekstur við uppfærslu gerist þegar aðferð birgðamats er annaðhvort staðalkostnaður eða hlaupandi meðaltal
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 920d20d19843ce0cac678c5426c00ec99aa61c61
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476690"
---
# <a name="an-update-conflict-occurs-when-the-inventory-valuation-method-is-either-standard-cost-or-moving-average"></a>Árekstur við uppfærslu gerist þegar aðferð birgðamats er annaðhvort staðalkostnaður eða hlaupandi meðaltal

## <a name="symptoms"></a>Einkenni

Þegar bókuð eru skjöl á borð við birgðabækur, innkaupapöntunarreikningar eða sölupöntunarreikningar samhliða fyrir sveigjanleika og afköst, gætu komið upp villuboð um árekstur við uppfærslu og sum skjalanna verða hugsanlega ekki bókuð. Þetta vandamál getur komið upp þegar aðferð birgðamats er annaðhvort *Staðalkostnaður* eða *Hlaupandi meðaltal*. Báðar þessar aðferðir eru varanlegar kostnaaðaraðferðir. Með öðrum orðum er endanlegur kostnaður ákvarðaður á þeim tíma sem bókað er.

Ef verið er að nota aðferðina *Hlaupandi meðaltal* líkjast villuboðin þessu dæmi:

> Ekki er búist við birgðavirði xx.xx eftir hlutfallslegan kostnaðarútreikning

Ef verið er að nota aðferðina *Staðlaður kostnaður* kostnaðaraðferð líkjast villuboðin þessu dæmi:

> Staðalkostnaður stemmir ekki við gildi fjárhagslegra birgða eftir uppfærsluna. Gildi = xx.xx, magn = yy.yy, staðalkostnaður = zz.zz

## <a name="workaround"></a>Hjáleið

Þar til Microsoft gefur út lausn til að laga vandamálið er mögulegt að nota eftirfarandi hjáleið til að forðast eða draga úr þessum villum:

- Endurbókið skjölin sem mistókust.
- Stofna skjöl sem eru með færri línum.
- Forðast skal tugabrot í staðalkostnaði. Reynið að skilgreina staðalkostnaðinn þannig að reiturinn **Magn í verði** sé stilltur á *1*. Ef tilgreina þarf gildi fyrir **Magn í verði** sem er meira en *1* skal reyna að lágmarka fjölda aukastafa í staðalkostnaði einingarinnar. (Helst ættu að vera færri en tveir aukastafir.) Til dæmis skal forðast að skilgreina stillingar staðalkostnaðar á borð við **Verð** = *10* og **Magn í verði** = *3* vegna þess að þær munu leiða til staðalkostnaðar á einingu sem er 3,333333 (þar sem gildi aukastafs endurtekur sig).
- Í flestum skjölum skal forðast að hafa margar línur sem geyma sömu samsetningu afurðar- og fjárhagsbirgðavídda.
- Dragið úr fjölda á samhliða vinnslum. (Í þessu tilviki gæti kerfið orðið fljótara þar sem færri árekstrar við uppfærslu og endurtekningar koma upp.)
