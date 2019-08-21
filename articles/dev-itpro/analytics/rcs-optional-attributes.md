---
title: Flytja inn skrár á XML-sniði með valeigindum
description: Þetta umræðuefni veitir upplýsingar um að uppsetningu á ER-sniðum sem tilgreina XML-eiginleika til að þátta komandi rafræn skjöl í XML-sniði.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: eb5d721784f45097ab466f75d43256495aac36ca
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/02/2019
ms.locfileid: "1849996"
---
# <a name="import-files-in-xml-format-with-optional-attributes"></a>Flytja inn skrár á XML-sniði með valeigindum

Hægt er að setja upp snið rafrænnar skýrslugerðar (ER) til að þátta skjöl á innleið í XML-sniði. Hægt er að tilgreina ákveðna eiginleika XML-eininga í uppsettu ER-sniði sem valfrjálsa. Það mun gera þér kleift að meðhöndla skrár á innleið og án slíkra XML-eiginleika rétt. Síðan er hægt að nota efnið úr þessum skrám til að uppfæra hugbúnaðargögn.

Til að fá frekari upplýsingar um þennan eiginleika skaltu ljúka skrefunum í efninu [RCS Flytja inn skrár á XML-sniði með valkvæðum eiginleikum](tasks/import-files-xml-format-optional-attributes.md), sem er hluti af viðskiptaferlinu 7.5.4.3 Acquire/Develop IT þjónusta/lausnarhluti (10677). Hægt er að sækja þessar verkleiðbeiningarnar og tengdar sýnisskrár úr [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).


| Lýsing á efni       | Skrá                                                         |
|---------------------------|--------------------------------------------------------------|
| Sýnisskrá á XML-sniði | IncomingDocumentToLearnHowToHandleOptionalAttributes.xml     |
| verkefnaleiðbeiningar                | RCS Flytja inn skrár á XML-sniði með valkvæðum attributes.axtr |


Eftirfarandi skref útskýra hvernig notandi í hlutverki kerfisstjóra eða þróunaraðila rafrænnar skýrslulausnar getur sett upp ER-skilgreiningarsnið til að flytja inn skrár á XML-sniði sem innihalda valkvæðar eigindir. Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu [Stofna skilgreiningarveitu og merkja hana sem virka](tasks/er-configuration-provider-mark-it-active-2016-11.md). Áður en þú hefst handa skaltu sækja og vista staðbundið skrána IncomingDocumentToLearnHowToHandleOptionalAttributes.xml frá Microsoft Download Center (https://go.microsoft.com/fwlink/?linkid=874684 ).

1. Farðu í **Fyrirtækisstjórnun** > **Vinnusvæði** > **Rafræn skýrslugerð**.
2. Vertu viss um að skilgreiningarveitan fyrir sýnifyrirtækið, Litware, Inc., sé tiltæk og merkt **Virk**. Ef þú sérð skilgreiningarveituna ekki skaltu klára skrefin í efninu [Stofna skilgreiningaveitu og merkja hana sem virka](tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Smellið á **Skilgreiningar skýrslugerðar**.

## <a name="create-a-new-data-model-configuration"></a>Stofna nýjan skilgreiningu gagnalíkans
1. Smellið á **Stofna skilgreiningu** til að opna felligluggann.
2. Í reitnum **Heiti** ritarðu „Líkan til að flytja inn XML-skrá“.
3. Smellið á **Stofna skilgreiningu**.
4. Smellið á **Hönnuður**.
5. Smelltu á **Nýtt** til að opna felligluggann.
6. Í reitnum **Heiti** skaltu færa inn „Rót“.
7. Smelltu á **Bæta við**.
8. Smelltu á **Nýtt** til að opna felligluggann.
9. Í reitnum **Heiti** skaltu færa inn „Listi“.
10. Í reitnum **Gerð vöru** velurðu **Skráalisti**.
11. Smelltu á **Bæta við**.
12. Smelltu á **Nýtt** til að opna felligluggann.
13. Í reitnum **Heiti** skal færa inn „kóða“.
14. Í reitnum **Gerð vöru** velurðu **Strengur**.
15. Smelltu á **Bæta við**.
16. Smellt er á **Vista**.
17. Lokið síðunni.
18. Smelltu á **Breyta stöðu**.
19. Smelltu á **Ljúka**.
20. Smellt er á **OK**.

## <a name="create-a-format-for-data-import"></a>Stofnaðu snið fyrir gagnaflutning
1. Smellið á **Stofna skilgreiningu** til að opna felligluggann.
2. Í reitnum **Nýtt** skaltu færa inn „Snið byggir á gagnalíkani Líkan til að flytja inn xml-skrá“.
3. Í reitnum **Heiti** ritarðu „Sníða til að flytja inn XML-skrá“. 
4. Veldu **Já** í reitnum **Styður gagnainnflutning**.
5. Smellið á **Stofna skilgreiningu**.

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a>Settu upp snið til að þátta komandi skrá í xml-sniði
1. Smellið á **Hönnuður**.
2. Smellið á **Bæta við rót** til að opna felligluggann.
3. Í trénu skal velja **XML/Element**.
4. Í reitnum **Heiti** skaltu færa inn „rót“.
5. Smellt er á **OK**.
6. Smellið á **Bæta við** til að opna felligluggann.
7. Í trénu skal velja **XML/Element**.
8. Í reitnum **Heiti** skaltu færa inn „skjal“.
9. Í reitnum **Margfeldi** skaltu velja **Einn margir**.
10. Smellt er á **OK**.
11. Í trénu velurðu **rót\skjal**.
12. Smellið á **Bæta við** til að opna felligluggann.
13. Í trénu skal velja **XML\Attribute**.
14. Í reitinn **Heiti** ritarðu „kenni“.
15. Smellt er á **OK**.
16. Smellt er á **Vista**.

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a>Settu upp sniðvörpun til að vista þáttaðar upplýsingar í gagnalíkan
1.  Smelltu á **Varpa sniði á líkan**.
2.  Smellt er á **Nýtt**.
3.  Í reitnum **Skilgreining** skaltu slá inn eða velja gildi.
4.  Í reitnum **Heiti** skaltu færa inn „Vörpun“.
5.  Smellt er á **Vista**.
6.  Smellið á **Hönnuður**.
7.  Í trénu skal víkka út **snið**.
8.  Í trénu skal útvíkka **format\root: XML Element(root)**.
9.  Í trénu skal velja **format\root: XML Element(root)\document: XML Element 1..* (fylgiskjal)**.
10. Smelltu á **Binda**.
11. Í trénu skal útvíkka **format\root: XML Element(root)\document: XML Element 1..* (fylgiskjal)**.
12. Í trénu skal velja **format\root: XML Element(root)\document: XML Element 1..* (fylgiskjal)\kenni**.
13. Í trénu skaltu stækka **List = format.root.document**.
14. Í trénu skaltu velja **List = format.root.document\Code**.
15. Smelltu á **Binda**.
16. Smellt er á **Vista**.
17. Lokið síðunni.

## <a name="run-format-mapping"></a>Keyra sniðsvörpun
1. Smelltu á **Keyra**.
2. Smelltu á **Fletta** og veldu skrána **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.
3. Smellt er á **OK**.

> [!NOTE]
> Valin skrá hefur ekki verið flutt inn þar sem sniðhönnunin gerir ráð fyrir að eigindin „kenni“ sé til staðar fyrir eininguna „skjal“, en innflutt skrá inniheldur engar slíkar eigindir.

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a>Breyta sniðsskipulagi til að meðhöndla xml-eigindi sem valfrjáls
1. Lokið síðunni.
2. Í trénu stækkarðu **rót\skjal**.
3. Í trénu velurðu **rót\skjal\kenni**.
4. Í reitnum **Tómur strengur fyrir eigind sem vantar** velurðu **Já**.
5. Smellt er á **Vista**.

## <a name="run-format-mapping-to-test-changes"></a>Keyra sniðvörpun til að prófa breytingar
1. Smelltu á **Varpa sniði á líkan**.
2. Smelltu á **Keyra**.
3. Smelltu á **Fletta** og veldu skrána **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.
4. Smellt er á **OK**.
5. Yfirfara myndaða skrá. Athugaðu að sama skrá hefur verið flutt inn þar sem sniðshönnunin telur nú að eigindin „kenni“ fyrir eininguna „fylgiskjal“ sé valfrjáls.
