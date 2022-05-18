---
title: Skilgreina númeraraðir flæði vöruhúss
description: Í þessu efnisatriði er að finna yfirlit yfir virknina sem býður upp á viðbætur númeraraðar fyrir auðkenni númeraplatna, auðkenni bylgjumerkja, auðkenni gáma og auðkenni farmbréfa.
author: Mirzaab
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSNumberSequenceExt
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: 20438ed3e34775a6312508595bcd32b16a37a81d
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669556"
---
# <a name="configure-number-sequences-for-warehouse-flows"></a>Skilgreina númeraraðir flæði vöruhúss

[!include [banner](../includes/banner.md)]

*Viðbót númeraraða* bætir við nýrri skilgreiningarsíðu til að setja upp númeraraðir. Það býður upp á sveigjanlega skilgreiningu á GS1-stýrðum auðkennum, þ.m.t. GS1-forskeytum og vartölum (leif 10) og framfylgir lengdartakmörkun á fyrirliggjandi númeraröðum.

Hlutar staðlaðrar númeraraðar eru ekki hentugir fyrir GS1-innleiðingu vegna þess að engin vartala er reiknuð út og GS1-forskeyti fyrirtækisins verður að uppfæra handvirkt.

Þessi eiginleiki bætir við eftirfarandi virkni:

- Hægt er að mynda auðkenni fyrir farmbréf fyrirfram.
- Einkvæma númeraröð er hægt að mynda fyrir raðnúmer vörusendingar (SSCC).
- GS1-fylgin númeraröð er hægt að búa til fyrir númer farmbréfs og SSCC-númer. Þessi eiginleiki bætir við tilbúnum stuðningi fyrir númeraplötukenni, gámakenni, kenni bylgjumerkja og kenni farmbréfa.
- Skilgreining auðkennis númeraplötu er sveigjanleg. Til dæmis er hægt að hafa með eða sleppa kennimerkjum forrits, svo sem núll að framan (00).

Þessi virkni gerir það hagkvæmara að styðja merkingu kassa og að velja ný númer sem búin eru til af kerfinu.

## <a name="turn-on-the-number-sequence-extensions-feature"></a>Kveikja á eiginleika númeraraðar fyrir viðbætur

Áður en hægt er að nota eiginleikann verður að vera kveikt á honum í kerfinu. Stjórnendur geta notað vinnusvæði [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur. Þar er eiginleikinn sýndur á eftirfarandi hátt:

- **Eining:** *Vöruhúsakerfi*
- **Heiti eiginleika:** *Viðbætur númeraraðar*

## <a name="set-up-the-feature"></a>Setja upp eiginleika

Til að setja upp viðbætur númeraraðar í kerfinu skal fylgja þessum skrefum.

1. Farðu í **vöruhúsakerfi \> Uppsetning \> Færibreytur vöruhúsakerfis**.
1. Í flipanum **Almennt**, í reitinn **GS1-fyrirtækjaforskeyti**, og færa inn GS1-fyrirtækjaforskeyti. Þetta gildi mun hafa áhrif á allar númeraraðir þar sem GS1-forskeytið er tekið með sem hluti.
1. Ef ætlunin er að búa til númer farmbréfa fyrir bylgjumerki, í flipanum **Skýrslur**, skal velja gátreitinn **Búa til númer farmbréfs þegar bylgjumerki eru prentuð**.

    > [!NOTE]
    > Þessi gátreitur er aðeins tiltækur ef kveikt er á virkninni fyrir [prentun bylgjumerkis](configure-wave-label-printing.md).

1. Fara í **Vöruhúsakerfi** \> **Uppsetning** \> **Viðbætur númeraraðar**.
1. Á aðgerðasvæðinu skal velja **Stofna sjálfgefna uppsetningu**: GS1-fylgin númeraröð farmbréfs og þrjár gerðir af SSCC-númeraröðum eru búnar til. Allar þessar númeraraðir taka lengd GS1-forskeytis fyrirtækisins til greina.

    Nánari upplýsingar um hvernig á að sérsníða númeraraðir og/eða bæta nýjum við er að finna í næsta hluta. Einnig er hægt að fjarlægja allar þessar raðir ef ekki er þörf á þeim.

1. Farið aftur í **Vöruhúsakerfi \> Uppsetning \> Færibreytur vöruhúsakerfis**.
1. Í flipanum **Númeraraðir** skal velja viðeigandi viðbót númeraraðar sem nota á til að búa til númer fyrir auðkenni númeraplatna, auðkenni bylgjumerkja, gámakenni (í þessu tilviki skal velja viðeigandi röð **SSCC-18 númers**) og/eða auðkenni farmbréfa (í þessu tilviki skal velja röð **Farmbréfs**). Sjálfgefið er að viðbætur númeraraðar séu aðeins studdar fyrir þessar fjórar gerðir af auðkennum.

Næst þegar nýtt númer er myndað fyrir eina af þessum númeraröðum verða nýju rökin notuð.

> [!NOTE]
> Ef ekki er valin viðbót númeraraðar fyrir kenni númeraplötu verða gildandi reglur um myndun númeraplötukenna notaðar. Annars verður valin númeraröð notuð. Hin auðkennin munu nota venjulega númeraröð þangað til notuð er viðbót númeraraðar fyrir þau.

## <a name="create-and-edit-number-sequences"></a>Stofna og breyta númeraröðum

Í fyrri hlutanum var búið til sjálfgefið safn af númeraröðum. Þessi hluti útskýrir hvernig hver númeraröð er skilgreind. Þar er einnig útskýrt hvernig á að stofna sérstilltar raðir og breyta sjálfgefnum eða sérstilltum röðum.

Til að stofna og breyta númeraröðum skaltu fylgja þessum skrefum.

1. Fara í **Vöruhúsakerfi** \> **Uppsetning** \> **Viðbætur númeraraðar**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Í **Viðbót númeraraðar** reitinn, slá inn heiti fyrir nýju röðina. Í reitnum **Lýsing** skal færa inn lýsingu.
1. Í flýtiflipanum **Hlutar** skal nota hnappana í tækjastikunni til að setja saman númerasniðið með því að bæta við, eyða og raða hlutum. Í reitnum **Hlutur** fyrir hverja línu, skal úthluta gerð hluta til að skilgreina tilgang og efni hlutans. Eftirfarandi tafla lýsir þeim gerðum hluta sem eru í boði.

    | Gerð hluta | lýsing |
    |---|---|
    | Fasti | Þessi hlutagerð bætir við sama fasta texta fyrir hvert myndað númer í röðinni. Sláðu inn nauðsynlegan texta í reitinn **Gildi**. Reiturinn **Lengd** er sjálfkrafa uppfærður í lengd textans sem sleginn var inn í reitinn **Gildi**. |
    | Númeraröð | Í reitinn **Gildi** skal slá inn númeratákni (*\#*) fyrir hvern staf sem á að sýna í mynduðu röðinni. Númeraröðin sjálf gæti myndað lengri tölur, en aðeins stafirnir til hægri eru sýndir. Reiturinn **Lengd** er sjálfkrafa uppfærður í fjölda númeratákna sem sleginn var inn í reitinn **Gildi**.<p>Til að fylgja kröfum GS1 fyrir SSCC-18 númer skal ganga úr skugga um að lengd þessa hluta sé 16 mínus lengdin á GS1-forskeytinu þínu.</p> |
    | GS1-forskeyti | Þessi hlutagerð bætir gildinu sem sett er í reitinn **GS1-fyrirtækjaforskeyti** á síðuna **Færibreytur vöruhúsakerfis**. Reiturinn **Gildi** sýnir gildið sem er stillt á síðunni **Færibreytur vöruhúsakerfis** og reiturinn **Lengd** sýnir þann fjölda stafa sem er í gildinu. Bæði reiturinn **Gildi** og **Lengd** eru skrifvarðir. |
    | Kennimerki forrits | Í reitinn **Gildi** skal slá inn kennimerki forrits eins og er tilgreint af viðeigandi GS1-reglu fyrir þessa gerð af númeraröð. Til dæmis skal slá inn *00* fyrir SSCC eða *420* fyrir aðalfarmbréf. Reiturinn **Lengd** er sjálfkrafa uppfærður í lengd kennimerkisins sem slegið var inn í reitinn **Gildi**. |
    | Pökkunargerð | Fyrir vörur sem auðveldlega er hægt að bera kennsl á, bætir þessi hlutagerð við reitargildi úr viðeigandi röðunarflokki einingar (af síðunni **Röðunarflokkar einingar**). (Þessi hegðun samsvarar fyrirliggjandi rökum fyrir kenni númeraplötu.) Fyrir númeraplötur sem fela í sér margar birgðahaldseiningar (BHE), bætir þessi hlutagerð sjálfgefið við *0* (núll). Fyrir þessa hlutagerð er reiturinn **Gildi** alltaf stilltur á *P* og reiturinn **Lengd** er alltaf stilltur á *1*.|
    | Vartala | Þessi hlutagerð bætir við vartölu, sem er með leifastofn 10 við útreikning. (Þessi hegðun samsvarar fyrirliggjandi rökum fyrir kenni númeraplötu.) Fyrir þessa hlutagerð er reiturinn **Gildi** alltaf stilltur á innskotsmerki (*^*) og reiturinn **Lengd** er alltaf stilltur á *1*. |

1. Til að skoða dæmi um endanlegt númerasnið skal skoða reitinn **Snið** neðst í flýtiflipanum **Hlutar**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]