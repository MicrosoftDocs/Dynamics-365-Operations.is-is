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
ms.openlocfilehash: 5e8168a20a1fa4f52d28129eebb9931b31157ced
ms.sourcegitcommit: ab690bc897699ff8a4c489e749251fe0367050ca
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/26/2022
ms.locfileid: "8488968"
---
# <a name="inventory-journal-workflow-never-completes-and-the-journal-cant-be-processed"></a>Verkflæði birgðabókar klárast aldrei og ekki er hægt að vinna úr færslubókinni

## <a name="symptoms"></a>Einkenni

Þegar búið er að senda inn samþykktarverkflæði færslubókar hættir verkflæðisferli að svara og ekki verður hægt að breyta eða vinna úr færslubókunum.

## <a name="resolution"></a>Lausn

Ýmsar ástæður eru fyrir því að ekki er hægt að ljúka við verkflæðisferli. Kannið eftirfarandi vandamál:

- Opnið **Birgðastjórnun &gt; Uppsetning&gt; Verkflæði birgðastjórnunar**, og farið yfir skilgreininguna á verkflæðinu sem um ræðir. Fyrir frekari upplýsingar sjá [Samþykktarverkflæði birgðabókar](../../inventory/inventory-journal-workflow.md).
- Í verkflæðinu gæti hugsanlega hafa komið upp undantekning eða villa. Farið yfir feril vinnuliðar í verkflæðinu sem um ræðir til að sjá hvort í honum sé forritsvilla sem stöðvar verkflæðið.
- Aðeins er hægt að uppfæra birgðabókina eða breyta henni ef hún er samþykkt. Ef afturköllun er virk er hægt að reyna að afturkalla færslubókina. Ekki er hægt að fresta keyrslu á runuvinnslunni af mörgum ástæðum. Sumar af þessum ástæðum gætu stafað af vandamáli varðandi verkflæðisrammann.
