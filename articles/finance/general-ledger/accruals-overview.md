---
title: Yfirlit yfir uppsafnanir
description: Þessi grein lýsir áföllnum gjöldum og veitir upplýsingar um hvernig skuli setja þær upp og stofna færslur.
author: aprilolson
ms.date: 01/11/2018
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAccuralTable
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "14131"
- intro-internal
ms.assetid: 0489b59a-37a7-4a78-87bf-4b597e9efad9
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2e10842929ba58b845a1df949ecb7c776ae077e8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904702"
---
# <a name="accruals-overview"></a>Yfirlit yfir uppsafnanir

[!include [banner](../includes/banner.md)]

Þessi grein lýsir áföllnum gjöldum og veitir upplýsingar um hvernig skuli setja þær upp og stofna færslur.

Uppsafnanir eru notaðar í rekstrarbókhaldi til að rekja tekjur sem eru viðurkenndar á tímabilinu sem þær eru fengnar í, ekki þegar greiðsla er móttekin, og til að rekja útgjöld (kostnað) sem eru viðurkennd þegar þau eiga sér stað, ekki þegar greiðsla er gerð.

## <a name="accrual-schemes"></a>Uppsöfnunarskemu
Uppsöfnunarskemu eru notuð til að setja upp frestaðar tekjur og kostnað, og hægt er að nota sama uppsöfnunarskema fyrir tekjur og kostnað. Fjárhagsuppsafnanir endurdreifa kostnaði eða tekjum í færslubókarlínu svo að kostnaður eða tekjur eru samþykktar á viðeigandi tímabilum. Á síðunni **Uppsöfnunarskema** eru tilgreindir debet- og kreditlyklar sem verða notaðir þegar uppsöfnunarskema er beitt.

-   **Debet** – Aðallykill sem er skilgreindur mun skipta út aðallykli debets í fylgiskjali færslubókarlínu. Þessi lykill verður einnig notaður fyrir bakfærslu á frestun sem byggir á uppsöfnunarfærslum fjárhags.
-   **Kredit** – Aðallykill sem er skilgreindur mun skipta út aðallykli kredits í fylgiskjali færslubókarlínu. Þessi lykill verður einnig notaður fyrir bakfærslu á frestun sem byggir á uppsöfnunarfærslum fjárhags.

Þegar búið er að ákvarða hvaða lykla á að nota, er hægt að tilgreina hvernig fylgiskjalsnúmer er stofnað þegar uppsöfnunarfærslur eru stofnaðar. Einnig er hægt að tilgreina hversu oft færslur eiga sér stað, fjölda skipta sem færslur eru stofnaðar og hvenær færslur eru bókaðar. Eftir að uppsöfnunarskema hefur verið stofnað er hægt að nota það í sumum færslubókum með aðgerðinni Fjárhagsuppsafnanir.

## <a name="ledger-accruals"></a>Fjárhagsuppsafnanir
Þegar færslubók er færð inn er hægt að smella á **Fjárhagsuppsafnanir** í valmyndinni **Aðgerðir**. Síðan þegar uppsöfnunarskema er valið muntu sjá grunnupphæðina úr færslubókinni sem verður dreift yfir tímabilið, eins og ákvarðast af uppsöfnunarskemanu. Til dæmis, ef þú greiðir tryggingu starfsmanns fyrir allt árið í janúar og upphæðin er 12.000, er verður að viðurkenna þann kostnað í hverjum mánuði. Hægt er að velja upphafsdagsetningu. Einnig er hægt að tilgreina hvort upphæðin sem er safnað upp sé byggð á lyklinum eða mótlyklinum. Þegar valið hefur verið gert er smellt á **Færslur** til að skoða allar færslur sem hafa verið stofnaðar samkvæmt uppsöfnunarskemanu. Til dæmis, ef þú dreifir 12.000 af tryggingakostnaði yfir árið sjást 1.000 fyrir hvern mánuð. Þegar færslubókin er bókuð, er hægt að skoða færslurnar með því að nota fyrirspurnarsíðuna **Fylgiskjalsfærslur**. Ef ekki er hægt að nota uppsöfnunarskema (til dæmis, þegar reikningur sölupöntunar eða innkaupareikningur á í hlut) er hægt að kreditfæra fyrirframgreidda upphæð og debetupphæð kostnaðar. Síðan er hægt að velja **Mótfærsla** þegar uppsöfnunarskemanu er beitt.


Nánari upplýsingar, sjá [stofna uppsöfnunarskemu](tasks/create-accrual-schemes.md) og [Stofna uppsöfnunarfærslur fjárhags](tasks/create-ledger-accrual-transactions.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
