---
title: Algengar spurningar um afurðartengdar þýðingar
description: Þetta efnisatriði lýsir því hvernig stjórna þýðingar fyrir afurðir afurðarvíddargildi og afurðaeigindir.
author: t-benebo
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysTranslationDetail, SysTranslationLanguage, SysTranslationList, EcoResProductListPage, EcoResProductVariants, EcoResProductDetailsExtended, EcoResProductCreate, EcoResProductDetails, RetailSizeGroupTable, RetailStyleGroupTable, RetailColorGroupTable, PCTranslationLanguageLookup, EcoResProductCategory
audience: Application User
ms.reviewer: kamaybac
ms.custom: 201853
ms.assetid: c0286bba-f54b-42de-904c-81fd796bdd1d
ms.search.region: global
ms.search.industry: Product information
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 24a341973b8648b1a697c8c07b6ecbc808e0e504
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570492"
---
# <a name="product-related-translations-faq"></a>Algengar spurningar um afurðartengdar þýðingar

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig stjórna þýðingar fyrir afurðir afurðarvíddargildi og afurðaeigindir. 

## <a name="what-product-related-data-can-be-translated"></a>Hægt er að þýða yfir hvaða tengjast gögn?

Hægt er að stofna þýðingar fyrir eftirfarandi afurðatengdar upplýsingar:
-   Nöfn og lýsingar á afurðum.
-   Lýsingar, nöfnum og hjálpartexta á gildi afurðareiginda.
-   Heiti og lýsing afurðavíddargilda.

Hægt er að þýða upplýsingar tengdar afurðum í hvaða tungumál sem er tiltækt úr skjámyndinni **Textaþýðing**. Frekari upplýsingar má finna í **Hvernig á að stofna þýðingar fyrir afurðatengdar upplýsingar**.

## <a name="where-can-i-view-the-translated-information"></a>Hvar get ég skoðað þýddar upplýsingar?
Hægt er að skoða þýðingar upplýsingar sem tengjast hvaða ytri uppruna skjals, eins og reikning, sem notar tungumál þýðingar sem tiltæk.

## <a name="how-do-i-create-translations-for-product-related-information"></a>Hvernig get ég stofnað þýðingar fyrir upplýsingar sem tengjast vöru?
Til að stofna þýðingar afurðar, skal fylgja þessum skrefum:
1.  Smellið á **Upplýsingastjórnun afurða** &gt; **Algent** &gt; **Losaðar afurðir**.
2.  Velja afurð, og á Aðgerðarúðu í flokknum **Tungumál** er smellt á **Þýðingar**.
3.  Á síðunni **Textaþýðing** á svæðinu **Tungumál** skal velja tungumál. Til að bæta við fleiri tungumálum skal útvíkka svæðið **Tungumál** og smella síðan á **Í lagi**.
4.  Í hópnum **Þýddur texti** skal slá inn þýðingar í svæðunum **Lýsing** og **Afurðaheiti**.

Til að stofna þýðingar fyrir afurðareigindir, skal fylgja þessum skrefum:
1.  Smellið á **Upplýsingastjórnun afurða** &gt; **Algent** &gt; **Losaðar afurðir**.
2.  Undir **Uppsetning**, smellið á **Eigindir**, og smellið síðan á **Eigindir**.
3.  Á síðunni **Eigindir**, smellið á **Þýða**.
4.  Á síðunni **Textaþýðing** á svæðinu **Tungumál** skal velja tungumál. Til að bæta við fleiri tungumálum skal útvíkka svæðið **Tungumál** og smella síðan á **Í lagi**.
5.  Í hópnum **Þýddur texti** skal slá þýðingar inn í svæðin **Lýsing**, **Stutt heiti** og **Hjálpartexti**.

Fylgið eftirfarandi skrefum til að stofna víddargildi þýðingar afurðar:
1.  Smellið á **Upplýsingastjórnun afurða** &gt; **Algent** &gt; **Losaðar afurðir**.
2.  Veljið afurð og smellið síðan á **Afurðarvíddir**.
3.  Veljið einn af tenglunum fyrir afurðavíddir: **Stillingar**, **Stærðir**, **Litir**, eða **Stíll**.
4.  Veljið víddargildi og smellið síðan á **Þýða**.
5.  Á síðunni **Textaþýðing** á svæðinu **Tungumál** skal velja tungumál. Til að bæta við fleiri tungumálum skal útvíkka svæðið **Tungumál** og smella síðan á **Í lagi**.
6.  Í hópnum **Þýddur texti** skal slá inn þýðingar á svæðunum **Heiti** og **Lýsing**.

## <a name="can-the-names-of-product-variants-be-translated"></a>Er hægt að þýða heiti afurðarafbrigði
Afurðarafbrigði eru byggðar á víddum fyrir losaða afurð. Heiti afurðarafbrigða byggjast á samsetningu víddargilda. Þegar víddargildin sem tengjast afurðarafbrigði eru þýða heiti afurðarafbrigðis birtist í þýdd útgáfu.  

**Dæmi**  

Því afurðin er T-shirt sem kemur í mismunandi stærðum og liti og vöruvíddasamsetningar nöfn eru byggðar á eftirfarandi upplýsingar:
-   Afurðarnúmer: \#3
-   Víddir: Stærð og lit
-   Víddargildi stærðar: Lítill, miðlungs, stór
-   Litur víddargildi: Rauður, Grænn, Svart

Heiti afurðarafbrigðis sem byggir á víddargildunum Lítið og Rautt er **\#3:Small:Red**.  

Viðskiptavinur vill kaupa litla rauðaskyrtu og nafn á skyrtunni verður birtast á frönsku á reikningnum. Þú þýðir víddargildin Lítið og Rautt, yfir á frönsku og heiti afurðarafbrigðisins er **\#3: Petit: Rouge**.
<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Ábending</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Til að stilla æskilegt tungumál viðskiptavinar, skal fylgja þessum skrefum:
<ol><br/><li>Smellið á <strong>Sala og markaðssetning</strong> &gt; <strong> Almennt</strong> &gt; <strong> Viðskiptavinir</strong> &gt; <strong> Allir</strong><strong>viðskiptavinir</strong>.</li>
<li>Tvísmellið á viðskiptavin til að opna skjámyndina <strong>Viðskiptavinir</strong>. Á flipanum <strong>Almennt</strong>, á svæðinu <strong>Tungumál</strong> skal velja <strong>Tungumál</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="what-happens-if-a-customer-has-a-preferred-language-for-which-no-translations-are-available"></a>Hvað gerist ef viðskiptavinur hefur æskilegt tungumál sem engin þýðingar tiltækar?
Þýðingar eru ekki tiltæk í kjörtungumál viðskiptavinarins heita og lýsinga eru birtar í altæka tungumál hitt fyrirtækið.

## <a name="can-i-manage-translations-for-a-series-of-dimension-values-at-the-same-time"></a>Get ég stjórna þýðingar röð víddargilda á sama tíma?
Víddargildi eru afurðartengt og hægt er að stjórna þýðingar víddargilda fyrir hverja vöru. Hins vegar, ef stofnaður er víddargildaflokkur og þýðingar fyrir gildi í gildisflokknum, er auðveldara að stýra þýðingar.   

**Dæmi**  

Fyrirtæki framleiðir stuttermaboli í mismunandi stílum og allir stílar eru til í stærðunum Lítið, Miðlungs og Stórt. Stærðir sem er safnað í gildi einn víddarflokk. Þegar ný T-shirt stíl er bætt við er hægt að tengja það við flokkur vídda sem notaður er fyrir stærðir, þannig að allar stærðir eru tiltækar fyrir afurðina. Einnig er hægt að bæta við eða breyta þýðingum fyrir stærðir í víddagildaflokknum hvenær sem er.  

Víddargildið sem er tengdt við vöru með víddarafbrigðahóp verður að viðhalda úr afurðaflokki vöruvíddasamsetningar.   
Fylgið eftirfarandi skrefum til að stofna gildi víddarflokks:
1.  Smellið á **Upplýsingastjórnun afurða** &gt; **Uppsetning** &gt; **Afbrigðaflokkar**.
2.  Veljið flokkana **Stærð** **,**, **Litur**, eða **Stíll**.
3.  Smelltu á **Nýtt** og sláið síðan heiti fyrir flokkinn í reitnum **Stærð** **hópnum**, **Litaflokkur** eða **Stílflokkur**. Smellið á **Stærðir**, **Litir** eða **Stílar** til að stofna línur fyrir flokkana.
4.  Í á **Stærð** **flokknum** línunum **Lit** **flokknum** **línur**, eða **Stílflokkur** síðunni er smellt á **Nýtt**, og svo stofnaðar stærðir, litir og stílar fyrir flokka.

Til að stjórna þýðingar fyrir gildi í víddaflokknum gildi skal fylgja þessum skrefum:
1.  Fylgið skrefunum í fyrra ferli fyrir stofnun á gildi víddarflokks til að opna síðuna **Línur Stærðarhóps**, **Línur litahóps**, eða **Línur stílhóps**.
2.  Smellið á **Textaþýðing**. Í skjámyndinni **Textaþýðing** í hópnum **Þýddur texti** skal slá inn þýðingar á svæðunum **Heiti** og **Lýsing**.

## <a name="when-can-translations-of-product-related-information-be-managed"></a>Þegar hægt þýðingar upplýsingar sem tengjast stjórnað?
Þýðingum á upplýsingum sem tengjast vöru sem hægt er að stýra hvenær sem er. Þegar þýðingar eru uppfærðar fyrir víddargildi sem tengjast vöru, eru upplýsingar um vörur uppfærðar, án tillits til þess hvort varan sé með færslu.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]