---
title: Viðteknar reglur
description: Þessi grein lýsir því hvernig á að setja upp venjur til að ákvarða hvernig kostnað ætti að færa í alþjóðlegt birgðabókhald.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f148d4c6ece543c8a11eee3e6dcdff47b3767936
ms.sourcegitcommit: 6b209919de39c15e0ebe4abc9cbcd30618f2af0b
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/11/2022
ms.locfileid: "9135501"
---
# <a name="conventions"></a>Viðteknar reglur

[!include [banner](../includes/banner.md)]

Viðtekin regla er gámur fyrir safn af reglum sem hafa áhrif á hegðun kerfisins. Eftir því hverjar viðskiptaþarfirnar eru þarf að skilgreina viðteknar reglur með því að nota samsetningu af ýmsum stefnum sem segja til um hvernig gerð er grein fyrir kostnaði í altæku birgðabókhaldi. Hægt er að tengja sérhverja viðtekna reglu við einn fjárhag eða fleiri til að tryggja samræmi í bókhaldsreglum sem eru notaðar í öllum fjárhagsbókum.

Til að setja upp viðteknar reglur skal fara í **Altækt birgðabókhald \> Uppsetning \> Viðteknar reglur**. Fyrir hverja viðtekna reglu skal stilla eftirfarandi reiti:

- **Heiti** - Færið inn heiti viðtekinnar reglu.
- **Lýsing** - Færið inn lýsingu á viðtekinni reglu.
- **Stefna kostnaðarhlutar** – Veljið stefnu kostnaðarhlutar. Þessar stefnur skera úr um hversu mikla nákvæmni kerfið setur í að reikna og vinna með birgðavirði. Völ er á þessum fyrirfram ákveðnu kostum:

    - Afurð
    - Afurð – Svæði
    - Afurð – Svæði – Vöruhús

    Til dæmis, ef valið er *Afurð – Svæði*, fyrir hverja birgðahreyfingu (á inn- og útleið) reiknar kerfið út og vinnur með birgðakostnað hverrar afurðar á stigi svæðis. Þess vegna hafa birgðahreyfingar á lægri stigum, eins og vöruhúsastiginu, ekki áhrif á birgðavirðið. (Dæmi um flutning á vöruhúsastigi er flutningur vöru á milli vöruhúsa á einu svæði.) Að sama skapi er ekki hægt að skoða birgðakostnaðinn á lægra stigi, t.d. vöruhúsastiginu.

- **Regla um grunnmælingu inntaks** – Veljið reglu um grunnmælingu inntaks. Þessar reglur ákvarða kostnaðinn sem á að renna inn á birgðareikninginn og kostnaðinn sem á að innheimta. Eftirfarandi valkostir eiga við fyrir viðskiptafyrirtæki:

    - **Eðlilegur eldri kostnaður** – Allir kostnaðarhlutir renna inn á birgðareikninginn.
    - **Staðlaður kostnaður** – Staðlaður kostnaður rennur inn birgðareikninginn og mismunurinn milli notaðs kostnaðar og raunverulegs kostnaðar er skuldfærður á fráviksreikninga. Ef þú vilt búa til *Staðlaða* reglu um grunnmælingu inntaks þarf fyrst að búa til verðlista þar sem reglan getur flett upp á staðalkostnaði vörunnar.
    - **Verðlistar** – Altækt birgðabókhald styður að sækja vöruverð frá mörgum lögaðilum. Hægt er að skilgreina verðlista sem regla um grunnmælingu inntaks mun notar. Þannig veit kerfið hvar á að fletta upp á vöruverðinu. Fylgið þessum skrefum til að setja upp verðlista:

        1. Færið inn lýsandi nafn í reitinn **Heiti**.
        1. Í reitnum **Lýsing** skal færa inn lýsingu.
        1. Í reitnum **Gerð kostnaðarútreiknings** skal velja gerð kostnaðarútreiknings (*Staðlaður kostnaður* eða *Áætlaður kostnaður*).
        1. Í reitnum **Gerð verðs** skal velja gerð verðs (*Kostnaður*, *Innkaup* eða *Söluverð*).
        1. Bæta við kostnaðarútgáfu.
        1. Á aðgerðasvæðinu skal velja **Verð** til að staðfesta vöruverðin í verðlistanum.

- **Áætlunarregla kostnaðarflæðis** – Veljið áætlunarreglu kostnaðarflæðis. Þessar reglur ákvarða hvernig kostnaður er fjarlægður úr birgðum og tilkynntur sem kostnaður seldra vara. Völ er á þessum fyrirfram ákveðnu kostum:

    - Meðaltal
    - Tiltekin – Runa

    > [!NOTE]
    > Altækt birgðabókhald er varanlegt birgðakerfi. Kerfið rekur því birgðavirði fyrir hverja færslu fyrir sig.

- **Reglur um kostnaðareiningu** – Hægt er að skilgreina reglur um kostnaðareiningu og tengja þær við þennan reit. *Kostnaðareining* er kostnaður tilfangs sem tilvik notar. Hægt er að nota kostnaðareiningu til að rekja og flokka kostnað. Til að búa til reglur um kostnaðareiningu skal færa upplýsingar inn á eftirfarandi staði:

    - **Heitis** svæði
    - **Lýsing** svæði
    - **Kostnaðareining** listi
    - Hnitanetið **Reglur**

    Ef ætlunin er ekki að sundurliða birgðavirði neitt frekar þarf samt sem áður að stofna kostnaðareiningalista sem er með eina kostnaðareiningu. Síðan þarf að stofna reglu um kostnaðareiningu til að varpa öllum viðeigandi gerðum mælingar (kostnaðarhlutum) í þá kostnaðareiningu.
