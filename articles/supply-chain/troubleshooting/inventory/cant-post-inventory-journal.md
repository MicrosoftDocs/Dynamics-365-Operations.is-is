---
title: Verkflæði birgðabókar klárast aldrei og ekki er hægt að vinna úr færslubókinni
description: Þegar búið er að senda inn samþykktarverkflæði færslubókar hættir verkflæðisferli að svara og ekki verður hægt að breyta eða vinna úr færslubókunum.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 9430068f9c2d92c894817db04143297de6c6aa6a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476622"
---
# <a name="inventory-journal-workflow-never-completes-and-the-journal-cant-be-processed"></a>Verkflæði birgðabókar klárast aldrei og ekki er hægt að vinna úr færslubókinni

## <a name="symptoms"></a>Einkenni

Þegar búið er að senda inn samþykktarverkflæði færslubókar hættir verkflæðisferli að svara og ekki verður hægt að breyta eða vinna úr færslubókunum.

## <a name="resolution"></a>Lausn

Ýmsar ástæður eru fyrir því að ekki er hægt að ljúka við verkflæðisferli. Kannið eftirfarandi vandamál:

- Opnið **Birgðastjórnun &gt; Uppsetning&gt; Verkflæði birgðastjórnunar**, og farið yfir skilgreininguna á verkflæðinu sem um ræðir. Fyrir frekari upplýsingar sjá [Samþykktarverkflæði birgðabókar](/dynamics365/supply-chain/inventory/inventory-journal-workflow.md).
- Í verkflæðinu gæti hugsanlega hafa komið upp undantekning eða villa. Farið yfir feril vinnuliðar í verkflæðinu sem um ræðir til að sjá hvort í honum sé forritsvilla sem stöðvar verkflæðið.
- Aðeins er hægt að uppfæra birgðabókina eða breyta henni ef hún er samþykkt. Ef afturköllun er virk er hægt að reyna að afturkalla færslubókina. Ekki er hægt að fresta keyrslu á runuvinnslunni af mörgum ástæðum. Sumar af þessum ástæðum gætu stafað af vandamáli varðandi verkflæðisrammann.
