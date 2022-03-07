---
title: Algengar spurningar um afbrigðalíkan afurðar
description: Þetta efnisatriði lýsir útreikningum fyrir afbrigðalíkönum afurðar og útskýrir hvernig á að nota útreikninga með skorðum.
author: t-benebo
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PCConstraintEditor, PCProductConfigurationModelDetails, PCRuntimeConfigurator
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19191
ms.assetid: 8993f9a1-d1c0-49f5-afd3-5e1077ded0fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9463fac363f6bb25c1bd2afebe5737e47aa8b3cf
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570802"
---
# <a name="calculations-for-product-configuration-models-faq"></a>Algengar spurningar um afbrigðalíkan afurðar

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir útreikningum fyrir afbrigðalíkönum afurðar og útskýrir hvernig á að nota útreikninga með skorðum.

Hægt er að nota útreikninga fyrir útreiknings eða rökaðgerðir. Þeir bæta segðaskorður í afbrigðalíkönum afurðar Hægt er að skilgreina útreikninga á **afbrigðalíkan afurðar sem byggist á skorðum** skjámyndinni og síðan byggja segðir fyrir útreikninga í segðaritlinum. Nánari upplýsingar sjá stofna útreikninga.

## <a name="what-is-a-calculation"></a>Hvað er útreikningur?
Útreikningur er einingu sem hægt er að nota í afbrigðalíkani afurðar. Útreikningar eru viðbót við skorður með því að leyfa þér að nota tugabrotum til að reikna gildi þegar afurð er skilgreind. Enn fremur hafa útreikningar stærri safn virknitákna tiltækt en skorður hafa.  

Eins og skorða tengist útreikningur tilteknum íhlut í afbrigðalíkani afurðar og hann er ekki hægt að endurnýta af eða deila með öðrum hluti. Er ein mikilvæg mismunur milli útreikninga og skorður er að útreikningar eru óskilyrtir (einstefnu), en skorður eru yfirlýsingar (tvístefnu). Sjá frekari upplýsingar um skorður í [segðaskorður og töfluskorður í afbrigðalíkönum afurða](expression-constraints-table-constraints-product-configuration-models.md).  

Útreikningur samanstendur af markmiðseigind og útreikningssegð.

## <a name="what-is-a-target-attribute"></a>Hvað er í markmiðseigind?
Markeigind er eigind sem tekur við niðurstöðu útreikningsinssegðar.  

Í eftirfarandi segð er markmiðseigind mælieining fyrir borðdúk:  

**Segð:** If\[decimalAttribute1 &lt;= decimalAttribute2, True, False\]  

**DecimalAttribute1** er borðlengdin og **decimalAttribute2** er lengd borðdúksins. Þessi segð skilar gildi **"Rétt"** á markmiðseigindin ef **decimalAttribute2** er hærra en eða jafnt og **decimalAttribute1**. Annars skilar segðin **"Rangt".** Til að mæling borðdúks sé ásættanleg ef lengd borðdúks er jöfn eða meiri en lengd borðsins.

## <a name="what-attribute-types-can-be-set-to-target-attributes"></a>Hvaða gerðir má stilla mark eigindir eigind?
Allar gerðir eiginda sem eru studd fyrir afurðarafbrigðastillir er hægt að stilla á markeigindir, nema fyrir texta án fasts lista.

## <a name="can-the-value-of-a-target-attribute-restrict-the-values-of-the-input-attributes-in-a-calculation"></a>Getur gildi fyrir markeigindi takmarkað gildi fyrir inntaks eigindir í útreikninga?
Nei, gildi fyrir markeigindi getur ekki takmarkað gildi fyrir inntaks eigindir af því útreikningar eru einstefnu? Þess vegna er gildi mareigindar stillt á grunni breytinga í gildi inntakseigindar, en breytingin í gildi marksins hefur ekki áhrif á gildi inntakseigindarinnar. Þessi hegðun er frábrugðið hegðun skorða. Skorður á sér stað í báðar áttir.

### <a name="example"></a>Dæmi

Í eftirfarandi segð er markið fyrir útreikninginn lengd rafmagnsleiðslu og inntaksgildið er litur:  

**Segð:** \[If Litur == "Grænt", 1,5, 1,0\]  

Þegar vara er skilgreind er lengd rafmagnssnúru stillt á **1,5** ef **Grænt** er tilgreint sem litareigindi. Ef annar litur er er tilgreindur, er lengdin stillt á **1,0**. Hins vegar, þar sem útreikningar eru einstefnumiðaðir eru útreikning ekki með gildi stillt á eigindarlit **Grænt** þegar tilgreind er lengd **1,5**.

## <a name="what-happens-if-a-calculation-has-a-target-attribute-of-the-integer-type-but-a-calculation-generates-a-decimal-number"></a>Hvað gerist ef útreikningur hefur markmiðseigind af gerðinni heiltala og útreikning gefur tala aukastafa?
ef markmiðseigind af gerðinni heiltala og útreikning gefur tala aukastafi, aðeins heiltöluhluti útreiknaðrar niðurstöðu er skilað. Aukastafshluti er fjarlægð og niðurstaðan er ekki sléttuð. Til dæmis er niðurstaða 12.70 sýnd sem 12.

## <a name="when-do-calculations-occur"></a>Hvenær eiga útreikningar sér stað?
Útreikningar á sér stað þegar gildi hefur verið gefin upp fyrir öll eigindi inntaks.

## <a name="can-i-overwrite-the-value-that-is-calculated-for-the-target-attribute"></a>Get ég skrifa yfir gildi sem er reiknuð fyrir markmiðseigindina?
Hægt er að skrifa yfir gildi sem er reiknuð fyrir markmiðseigindina nema ef markmiðseigindin er stillt sem falin eða aðeins til lestrar.

## <a name="how-do-i-set-a-target-attribute-as-hidden-or-read-only"></a>Hvernig get ég sett inn markmiðseigind sem er falin eða aðeins til lestrar?
Til að setja eigind sem falin eða aðeins til lestrar skal fylgja þessum skrefum:

1.  Smellið á **Upplýsingastjórnun afurða** &gt; **Almennt** &gt; **Afbrigðalíkan afurðar**.
2.  Veldu afbrigðalíkan afurðar og smellið síðan á **breyta** á aðgerðarúðu.
3.  Á **upplýsingum afbrigðalíkans afurðar sem byggir á Skorðum** síðunni, veljið eigindina sem nota á sem markeigind.
4.  Á **Eigindir** flýtiflipi, veljið **Falið** eða **skrifvarið**.

## <a name="can-a-calculation-overwrite-the-values-that-i-set"></a>Getur útreikning að skrifa yfir gildi sem ég setja?
Nei. Gildin sem þú setur fram þegar þú stillir vöru eru gildi sem notuð eru. Útreikningurinn á sér stað þegar ílagsgildanna í er breytt er ekki hægt að skrifa yfir gildi sem er tilgreind fyrir tiltekinn eigind.

## <a name="what-happens-if-i-remove-an-input-value-in-a-calculation"></a>Hvað gerist ef ég fjarlægi inntaksvirði í útreikninga?
Ef fjarlægt er innsett gildi í útreikningi, er gildi markmiðseigindin einnig fjarlægð.

## <a name="why-do-i-receive-an-error-message-that-says-that-my-model-is-in-contradiction"></a>Af hverju koma villuskilaboð sem gefur til kynna að líkanið mitt sé í mótsögn?
Þessi boð birtast þegar útreikningur inniheldur villa eða þegar mótsögn er til staðar í einni eða fleiri skorðum. Fyrir frekari upplýsingar um mótsagnir í skorðu skal sjá [segðaskorður og töfluskorður í afbrigðalíkönum afurða](expression-constraints-table-constraints-product-configuration-models.md). Hér eru nokkrar aðstæðum þar sem villur getur átt sér stað í útreikninga:

-   Gildi er deilt með 0 (núlli).
-   Árekstur er á milli þessara tveggja einingar:
    -   Gildin sem eru tiltækar fyrir eigind og eru takmarkaðir við skorðu.
    -   Gildi sem mynduð var með útreikningi.
-   Gildi sem er skilað eftir útreikning eru utan lén eigindar. Dæmi um þetta er heil tala frá \[1..10\] sem er reiknað niður í 0.

## <a name="why-do-i-receive-an-error-message-even-though-i-successfully-validated-my-product-model"></a>Af hverju kemur villuskilaboð jafnvel þótt ég hafi sannreynt framleiðslulíkanið mitt?
Útreikningar eru ekki teknar með í villuleit. Er þarf að prófa afbrigðalíkan afurðar til að finna villur í útreikningum. Til að prufa afbrigðalíkans afurðar skal fylgja þessum skrefum:

1.  Smellið á **Upplýsingastjórnun afurða** &gt; **Almennt** &gt; **Afbrigðalíkan afurðar**.
2.  Veldu afbrigðalíkan afurðar og smellið síðan á Aðgerðasvæðinu skal í **keyrslu** flokkur skal smella á **prófun**.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]