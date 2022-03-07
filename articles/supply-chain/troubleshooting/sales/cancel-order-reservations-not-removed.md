---
title: Ekki er hægt að fjarlægja frátekningar þegar hætt er við pöntun
description: Ekki er hægt að hætta við sölupöntun fyrr en hætt er við vinnuna sem tengist pöntuninni hún bakfærð. Það er gert með því að fylgja þessum þremur skrefum.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a8d947e64568246dba5eff3c21fd3920b6494b73
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476671"
---
# <a name="reservations-cannot-be-removed-when-canceling-an-order"></a>Ekki er hægt að fjarlægja frátekningar þegar hætt er við pöntun

## <a name="symptoms"></a>Einkenni

Ef vinna tengist sölupöntun og þú reynir að hætta við pöntunina færðu eftirfarandi villuboð:

> Ekki er hægt að fjarlægja frátekningar vegna þess að búið er að stofna vinnu sem byggir á frátekningunum.

Ekki er hægt að hætta við sölupöntunina fyrr en hætt er við vinnuna og hún bakfærð. Þessi krafa gildir jafnvel þótt vinnan sem tengist sölupöntuninni sé lokuð.

## <a name="resolution"></a>Lausn

Til að laga þetta vandamál skal fylgja þessum skrefum:

1. Hættið við verkið og setjið birgðir aftur á æskilega staðsetningu. Farið á viðeigandi farm sölupöntunarinnar og veljið annaðhvort **Minnka tiltektarmagn** í farmlínunni eða **Bakfæra vinnu** á aðgerðasvæðinu.

    Verkið er nú með stöðuna *Hætt við* og ný birgðahreyfingarvinna er sjálfkrafa stofnuð og unnið úr til að setja birgðir aftur í staðsetninguna sem var lýst þegar bakfærslan var gerð.

2. Eyðið farminum. Sendingunni er einnig eytt.

3. Nú ætti að vera hægt að fara í sölupöntunina og hætta við hana.
