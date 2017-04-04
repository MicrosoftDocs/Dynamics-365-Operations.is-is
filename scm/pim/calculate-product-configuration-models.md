---
title: "Útreikningur fyrir FAQ afbrigðalíkönum afurðar"
description: "Þessi skrá útreikninga fyrir líkön afurðaskilgreiningar lýsir og útskýrir hvernig á að nota útreikninga með skorður."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PCConstraintEditor, PCProductConfigurationModelDetails, PCRuntimeConfigurator
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19191
ms.assetid: 8993f9a1-d1c0-49f5-afd3-5e1077ded0fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3d02a15387231160f5b8a237aa11008b91ef1223
ms.openlocfilehash: 3a82fdb8532c79e33c167c43554a3de7d3061fcb
ms.lasthandoff: 03/31/2017


---

# <a name="calculations-for-product-configuration-models-faq"></a>Útreikningur fyrir FAQ afbrigðalíkönum afurðar

Þessi skrá útreikninga fyrir líkön afurðaskilgreiningar lýsir og útskýrir hvernig á að nota útreikninga með skorður.

Hægt er að nota útreikninga fyrir útreiknings eða rökaðgerðir. Þeir bæta segðaskorður í afbrigðalíkönum afurðar Hægt er að skilgreina útreikninga á **  afbrigðalíkan afurðar sem byggist á skorðum** skjámyndinni og síðan byggja segðir fyrir útreikninga í segðaritlinum. Nánari upplýsingar sjá stofna útreikninga.

## <a name="what-is-a-calculation"></a>Hvað er útreikningur?
Útreikningur er einingu sem hægt er að nota í afbrigðalíkani afurðar. Útreikningar eru viðbót við skorður með því að leyfa þér að nota tugabrotum til að reikna gildi þegar afurð er skilgreind. Enn fremur hafa útreikningar stærri safn virknitákna tiltækt en skorður hafa.  

Eins og skorða tengist útreikningur tilteknum íhlut í afbrigðalíkani afurðar og hann er ekki hægt að endurnýta af eða deila með öðrum hluti. Er ein mikilvæg mismunur milli útreikninga og skorður er að útreikningar eru óskilyrtir (einstefnu), en skorður eru yfirlýsingar (tvístefnu). Frekari upplýsingar um segðaskorður sjá [segðarskorður og töfluskorður](expression-constraints-table-constraints-product-configuration-models.md).  

Útreikningur samanstendur af markmiðseigind og útreikningssegð.

## <a name="what-is-a-target-attribute"></a>Hvað er í markmiðseigind?
Markeigind er eigind sem tekur við niðurstöðu útreikningsinssegðar.  

Í eftirfarandi segð er markmiðseigind mælieining fyrir borðdúk:  

**Segð:** Ef\[decimalAttribute1 &lt;= decimalAttribute2, True, Ósatt\]  

**DecimalAttribute1** er lengd töflu og **decimalAttribute2** er tablecloth lengd. Þessi segð skilar gildi **"Rétt" ** á markmiðseigindin ef **decimalAttribute2** er hærra en eða jafnt og **decimalAttribute1**. Annars skilar segðin **"Rangt".** Til að mæling borðdúks sé ásættanleg ef lengd borðdúks er jöfn eða meiri en lengd borðsins.

## <a name="what-attribute-types-can-be-set-to-target-attributes"></a>Hvaða gerðir má stilla mark eigindir eigind?
Allar gerðir eiginda sem eru studd fyrir afurðarafbrigðastillir er hægt að stilla á markeigindir, nema fyrir texta án fasts lista.

## <a name="can-the-value-of-a-target-attribute-restrict-the-values-of-the-input-attributes-in-a-calculation"></a>Getur gildi fyrir markeigindi takmarkað gildi fyrir inntaks eigindir í útreikninga?
Nei, gildi fyrir markeigindi getur ekki takmarkað gildi fyrir inntaks eigindir af því útreikningar eru einstefnu? Þess vegna er gildi mareigindar stillt á grunni breytinga í gildi inntakseigindar, en breytingin í gildi marksins hefur ekki áhrif á gildi inntakseigindarinnar. Þessi hegðun er frábrugðið hegðun skorða. Skorður á sér stað í báðar áttir.

### <a name="example"></a>Dæmi

Í eftirfarandi segðina mark fyrir útreikning lengd power cord og inntaks gildi er lit:  

**Segð:**\[Ef Lit == "Grænt", 1,5, 1,0\]  

Þegar vara er skilgreind lengd power cord er stillt á **1,5** ef **Grænt** sem gildi eigindar lit. Ef annar litur er er tilgreindur, er lengdin stillt á **1,0**. Hins vegar, þar sem útreikningar eru einstefnumiðaðir eru útreikning ekki með gildi stillt á eigindarlit **Grænt **þegar tilgreind er lengd **1,5**.

## <a name="what-happens-if-a-calculation-has-a-target-attribute-of-the-integer-type-but-a-calculation-generates-a-decimal-number"></a>Hvað gerist ef útreikningur hefur markmiðseigind af gerðinni heiltala og útreikning gefur tala aukastafa?
ef markmiðseigind af gerðinni heiltala og útreikning gefur tala aukastafi, aðeins heiltöluhluti útreiknaðrar niðurstöðu er skilað. Aukastafshluti er fjarlægð og niðurstaðan er ekki sléttuð. Til dæmis er niðurstaða 12.70 sýnd sem 12.

## <a name="when-do-calculations-occur"></a>Hvenær eiga útreikningar sér stað?
Útreikningar á sér stað þegar gildi hefur verið gefin upp fyrir öll eigindi inntaks.

## <a name="can-i-overwrite-the-value-that-is-calculated-for-the-target-attribute"></a>Get ég skrifa yfir gildi sem er reiknuð fyrir markmiðseigindina?
Hægt er að skrifa yfir gildi sem er reiknuð fyrir markmiðseigindina nema ef markmiðseigindin er stillt sem falin eða aðeins til lestrar.

## <a name="how-do-i-set-a-target-attribute-as-hidden-or-readonly"></a>Hvernig gera I sett markmiðseigind sem falin eða readonly?
Til að setja eigind sem falin eða aðeins til lestrar skal fylgja þessum skrefum:

1.  Smellið á **upplýsingar afurðastjórnun**&gt;**Algengar**&gt;**afbrigðalíkönum Afurðar**.
2.  Veldu afbrigðalíkan afurðar og smellið síðan á **  breyta** á aðgerðarúðu.
3.  Á **upplýsingum afbrigðalíkans afurðar sem byggir á Skorðum** síðunni, veljið eigindina sem nota á sem markeigind.
4.  Á **Eigindir** flýtiflipi, veljið **Falið** eða **skrifvarið**.

## <a name="can-a-calculation-overwrite-the-values-that-i-set"></a>Getur útreikning að skrifa yfir gildi sem ég setja?
Nei. Gildi sem er sett upp þegar þú samskipa afurð eru gildin sem eru notaðar. Útreikningurinn á sér stað þegar ílagsgildanna í er breytt er ekki hægt að skrifa yfir gildi sem er tilgreind fyrir tiltekinn eigind.

## <a name="what-happens-if-i-remove-an-input-value-in-a-calculation"></a>Hvað gerist ef ég fjarlægi inntaksvirði í útreikninga?
Ef fjarlægt er innsett gildi í útreikningi, er gildi markmiðseigindin einnig fjarlægð.

## <a name="why-do-i-receive-an-error-message-that-says-that-my-model-is-in-contradiction"></a>Af hverju koma villuskilaboð sem gefur til kynna að líkanið mitt sé í mótsögn?
Þessi boð birtast þegar útreikningur inniheldur villa eða þegar mótsögn er til staðar í einni eða fleiri skorðum. Sjá frekari upplýsingar um mótsagnir í skorðum í  [segðaskorður og töfluskorður](expression-constraints-table-constraints-product-configuration-models.md) Hér eru nokkrar aðstæðum þar sem villur getur átt sér stað í útreikninga:

-   Gildi er deilt með 0 (núlli).
-   Árekstur er á milli þessara tveggja einingar:
    -   Gildin sem eru tiltækar fyrir eigind og eru takmarkaðir við skorðu.
    -   Gildi sem mynduð var með útreikningi.
-   Gildi sem er skilað eftir útreikning eru utan lén eigindar. Sem dæmi er heiltala frá \[1..10\] sem reiknaður er á 0.

## <a name="why-do-i-receive-an-error-message-even-though-i-successfully-validated-my-product-model"></a>Af hverju kemur villuskilaboð jafnvel þótt ég hafi sannreynt framleiðslulíkanið mitt?
Útreikningar eru ekki teknar með í villuleit. Er þarf að prófa afbrigðalíkan afurðar til að finna villur í útreikningum. Til að prufa afbrigðalíkans afurðar skal fylgja þessum skrefum:

1.  Smellið á **upplýsingar afurðastjórnun**&gt;**Algengar**&gt;**afbrigðalíkönum Afurðar**.
2.  Veldu afbrigðalíkan afurðar og smellið síðan á Aðgerðasvæðinu skal í **keyrslu** flokkur skal smella á **prófun**.



