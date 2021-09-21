---
title: Skilyrði verkflæðis birgðabókar gilda á færslubókarstigi en ekki á línustigi
description: Skilyrði verkflæðis birgðabókar gilda aðeins á færslubókarstigi, ekki á línustigi.
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
ms.openlocfilehash: 46bdde7f09c639fbefd46162431762b056d521ae
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476659"
---
# <a name="inventory-journal-workflow-conditions-apply-at-the-journal-level-not-line-level"></a>Skilyrði verkflæðis birgðabókar gilda á færslubókarstigi en ekki á línustigi

## <a name="symptoms"></a>Einkenni

Þetta vandamál gæti komið upp ef til dæmis reynt er að setja upp skilyrði fyrir verkflæði birgðabókar í kostnaðarupphæðinni. Skilyrði er sett upp þannig að skref 1 er aðeins keyrt þegar kostnaðarupphæðin er lægri en 100. Síðan er sett upp annað skilyrði þannig að skref 2 er aðeins keyrt þegar kostnaðarupphæðin er hærri en eða jöfn og 100. Því næst, þegar verkflæðið er keyrt, sýnir verkflæðissagan aðeins eina línu og fyrsta skilyrðið er alltaf metið sem *satt* burtséð frá gildinu sem er sent inn.

## <a name="workaround"></a>Hjáleið

Í núverandi útgáfu eiga skilyrði í verkflæði birgðabókar aðeins við á færslubókarstigi, ekki á línustigi. Þessi hegðun er samkvæmt hönnuninni. Mælt er með því að skilyrðið sé aðeins sett á fyrir eigindir á færslubókarstigi.
