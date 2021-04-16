---
title: (RCS) Flytja inn skrár á XML-sniði með valkvæmum eigindum
description: Þetta efni veitir upplýsingar um hvernig notandi getur sett upp skilgreiningu ER-sniðs til að flytja inn skrár á XML-sniði sem inniheldur valkvæð eigindi.
author: NickSelin
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 25ced72bc1bb1b18996c8bab986270fde0557ed3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744868"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a>(RCS) Flytja inn skrár á XML-sniði með valkvæmum eigindum

[!include [banner](../../includes/banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki kerfisstjóra eða þróunaraðila rafrænnar skýrslulausnar getur sett upp ER-skilgreiningarsnið til að flytja inn skrár á XML-sniði sem innihalda valkvæðar eigindir. Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu „Stofna skilgreiningarveitu og merkja hana sem virka”. Áður en þú hefst handa skaltu sækja og vista staðbundið skrána IncomingDocumentToLearnHowToHandleOptionalAttributes.xml frá [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).

1.    Farðu í **Öll vinnusvæði** > **Rafræn skýrslugerð**.
2.    Vertu viss um að skilgreiningarveitan fyrir sýnifyrirtækið, Litware, Inc., sé tiltæk og merkt **Virk**. Ef þú sérð skilgreiningarveituna ekki skaltu klára skrefin í ferlinu [Stofna skilgreiningaveitur og merkja þær sem virkar](er-configuration-provider-mark-it-active-2016-11.md).
3.    Smellið á **Skilgreiningar skýrslugerðar**.

## <a name="create-a-new-data-model-configuration"></a>Stofna nýjan skilgreiningu gagnalíkans
1.    Smellið á **Stofna skilgreiningu** til að opna felligluggann.
2.    Í reitnum **Heiti** ritarðu „Líkan til að flytja inn XML-skrá“.
3.    Smellið á **Stofna skilgreiningu**.
4.    Smellið á **Hönnuður**.
5.    Smelltu á **Nýtt** til að opna felligluggann.
6.    Í reitnum **Heiti** skaltu færa inn „Rót“.
7.    Smelltu á **Bæta við**.
8.    Smelltu á **Nýtt** til að opna felligluggann.
9.    Í reitnum **Heiti** skaltu færa inn „Listi“.
10.    Í reitnum **Gerð vöru** velurðu **Skráalisti**.
11.    Smelltu á **Bæta við**.
12.    Smelltu á **Nýtt** til að opna felligluggann.
13.    Í reitnum **Heiti** skal færa inn „kóða“.
14.    Í reitnum **Gerð vöru** velurðu **Strengur**.
15.    Smelltu á **Bæta við**.
16.    Smellt er á **Vista**.
17.    Lokið síðunni.
18.    Smelltu á **Breyta stöðu**.
19.    Smelltu á **Ljúka**.
20.    Smellt er á **OK**.

## <a name="create-a-format-for-data-import"></a>Stofnaðu snið fyrir gagnaflutning
1.    Smellið á **Stofna skilgreiningu** til að opna felligluggann.
2.    Í reitnum **Nýtt** skaltu færa inn „Snið byggir á gagnalíkani Líkan til að flytja inn xml-skrá“.
3.    Í reitnum **Heiti** ritarðu „Sníða til að flytja inn XML-skrá“.
4.    Veldu **Já** í reitnum **Styður gagnainnflutning**.
5.    Smellið á **Stofna skilgreiningu**.

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a>Settu upp snið til að þátta komandi skrá í xml-sniði
1.    Smellið á **Hönnuður**.
2.    Smellið á **Bæta við rót** til að opna felligluggann.
3.    Í trénu skal velja **XML/Element**.
4.    Í reitnum **Heiti** skaltu færa inn „rót“.
5.    Smellt er á **OK**.
6.    Smellið á **Bæta við** til að opna felligluggann.
7.    Í trénu skal velja **XML/Element**.
8.    Í reitnum **Heiti** skaltu færa inn „skjal“.
9.    Í reitnum **Margfeldi** skaltu velja **Einn margir**.
10.    Smellt er á **OK**.
11.    Í trénu velurðu **rót\skjal**.
12.    Smellið á **Bæta við** til að opna felligluggann.
13.    Í trénu skal velja **XML\Attribute**.
14.    Í reitinn **Heiti** ritarðu „Kenni“.
15.    Smellt er á **OK**.
16.    Smellt er á **Vista**.

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a>Settu upp sniðvörpun til að vista þáttaðar upplýsingar í gagnalíkan
1. Smelltu á **Varpa sniði á líkan**.
2. Smellt er á **Nýtt**.
3. Í reitnum **Skilgreining** skaltu slá inn eða velja gildi.
4. Í listanum skal smella á tengilinn í valinni línu.
5. Í reitnum **Heiti** skaltu færa inn „Vörpun“.
6. Smellt er á **Vista**.
7. Smellið á **Hönnuður**.
8. Í trénu skal víkka út **snið**.
9. Í trénu skal útvíkka **format\root: XML Element(root)**.
10.    Í trénu skal velja **format\root: XML Element(root)\document: XML Element 1..* (fylgiskjal)**.
11.    Smelltu á **Binda**.
12.    Í trénu skal útvíkka **format\root: XML Element(root)\document: XML Element 1..* (fylgiskjal)**.
13.    Í trénu skal velja **format\root: XML Element(root)\document: XML Element 1..* (fylgiskjal)\kenni**.
14.    Í trénu skaltu stækka **List = format.root.document**.
15.    Í trénu skaltu velja **List = format.root.document\Code**.
16.    Smelltu á **Binda**.
17.    Smellt er á **Vista**.
18.    Lokið síðunni.
 
## <a name="run-format-mapping"></a>Keyra sniðsvörpun
1. Smelltu á **Keyra**.
2. Smelltu á **Fletta** og veldu **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.
3. Smellt er á **OK**.

> [!NOTE]
> Valin skrá hefur ekki verið flutt inn þar sem sniðhönnunin gerir ráð fyrir að eigindin „kenni“ sé til staðar fyrir eininguna „skjal“, en innflutt skrá inniheldur engar slíkar eigindir.

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a>Breyta sniðsskipulagi til að meðhöndla xml-eigindi sem valfrjáls
1. Lokið síðunni.
2. Í trénu stækkarðu **rót\skjal**.
3. Í trénu velurðu **rót\skjal\kenni**.
4. Veldu **Já** í reitnum **Tómur strengur fyrir eigind sem vantar**.
5. Smellt er á **Vista**.
 
## <a name="run-format-mapping-to-test-changes"></a>Keyra sniðvörpun til að prófa breytingar
1. Smelltu á **Varpa sniði á líkan**.
2. Smelltu á **Keyra**.
3. Smelltu á **Fletta** og veldu skrána **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.
4. Smellt er á **OK**.
5. Yfirfara myndaða skrá. 

> [!NOTE]
> Sama skrá hefur verið flutt inn þar sem sniðshönnunin telur nú að eigindin „kenni“ fyrir eininguna „fylgiskjal“ sé valfrjáls.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]