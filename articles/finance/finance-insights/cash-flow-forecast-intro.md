---
title: Sjóðstreymispá (forútgáfa)
description: Þetta efnisatriði lýsir eiginleika sjóðsstreymisspár.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f4b48122ea54c201888d71afb5fb731ebcab230d
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638777"
---
# <a name="cash-flow-forecast-preview"></a>Sjóðstreymispá (forútgáfa)

[!include [banner](../includes/banner.md)]

Sjóðstreymi er nauðsynlegt fyrir öll fyrirtæki. Jafnvel arðbær fyrirtæki geta staðið frammi fyrir gjaldþroti ef þau hafa ekki nægt sjóðstreymi. Sjóðstreymisspáreiginleikinn í fjármálainnsýn getur auðveldað fyrirtækjum að fylgjast með og stjórna sjóðsstöðu með árangursríkum hætti. Þessi eiginleiki notar vélnám til að hjálpa fyrirtækjum að spá fyrir um sjóðstreymi sem eru nákvæmari en þau hafa áður verið. Það getur einnig hjálpað stjórnendum að taka ákvarðanir sem hámarka tækifæri eftir núverandi reiðufjárstöðu þeirra. 

Í flestum fyrirtækjum er stjórnun sjóðstreymis og keyrsla sjóðstreymisspár leiðinlegt og endurtekningarsamt handvirkt ferli. Flest fyrirtæki reiða sig á Microsoft Excel-lausnir sem eru með mismikið flækjustig. Áskoranir um nákvæmar spár fyrir sjóðstreymi eru eftirfarandi:

- Gögn eru ekki tiltæk fyrir ákvarðanatöku vegna þess að þau eru dreifð á mörgum stöðum, þar á meðal: 
  - Áætlanakerfi fyrir bókhalds- eða fyrirtækistilfang
  - Hugbúnaður fjárhagsáætlanagerðar
  - Excel
  - Fleiri hugbúnaðarforrit 
- Spár byggjast á innri þekkingu sem staðsett er í sílóum innan hvers léns eða deildar.
- Mæling á nákvæmni sjóðstreymisspár eftir að fjárhagstölur eru komnar óvisst og erfitt ferli.
    
## <a name="details-of-the-cash-flow-forecasts-capability"></a>Upplýsingar um getu sjóðstreymisspárinnar
Eiginleiki sjóðstreymisspár inniheldur eftirfarandi virkni. 

- Auðveldar samþættingu sjóðsstreymisgagna úr ytri kerfum í Dynamics 365 Finance. Sjóðsstreymisspár geta einnig notað inn-útflutningsramma gagna. Þessi rammi auðveldar samþættingu við Excel OData. Einnig er hægt að sameina gögn af ólíkum uppruna til að stofna heildstæða sjóðsstreymislausn. 

- Kynnir til sögunnar snjalla reiðufjárstöðu. Staða reiðufjár er stofnuð á grundvelli greiðsluhegðunar viðskiptavinar til að spá fyrir um hvenær fyrirtæki getur búist við því að fá greitt reiðufé á reikninga sína. Þar er einnig hægt að greina söguleg mynstur greiðslna til lánardrottna til að spá fyrir um hvenær reikningar og pantanir eru líklegar til greiðslu. 

- Kynnir hugvitsamlega sjóðsstreymisspá fyrir langtímaspá með því að nota tímaraðaspár í gegnum sjálfvirka samþættingu við AI Builder.

- Býður upp á möguleikann á að vista tiltekna sjóðsstreymisstöðu eða spár, breyta þeim, bera þær saman og mæla frammistöðu spánna við rauntölur.

- Virkjar hvað-ef-greiningu í gegnum samanburð skyndimynda. Til dæmis er hægt að búa til margar skyndimyndir sem tákna bjartsýna, svartsýna og raunhæfa sýn á sjóðstreymi notanda og síðan bera saman og skoða mismuninn.

- Býður upp á möguleika á því að skoða sjóðsstreymisspá í mörgum gjaldmiðlum, þvert á lögaðila, og sía og skoða sjóðstreymi sem tengist bankareikningi. 

- Gerir notendum kleift að sía og skoða bankareikninga sem tengjast fjárhagsvíddum.

Sjóðstreymisspáin í Dynamics 365 Finance mun gera fyrirtækinu kleift að umbreyta leiðinlegri, flókinni, en endurtekningarsamri vörpun sjóðstreymis í einfalt, sjálfvirkt ferli. Með því að gera leiðinlegustu þætti sjóðstreymisspár sjálfvirka er hægt að leggja áherslu á mikilvæga ákvörðunartöku til að ná æskilegri rekstrarniðurstöðu.

## <a name="setting-up-dimensions-for-cash-flow-forecasting"></a>Setja upp vídd fyrir sjóðsstreymisspá
Nýr flipi á síðunni **Uppsetning sjóðstreymisspár** gerir notendum kleift að hafa stjórn á því hvaða fjárhagsvíddir eru notaðar fyrir síun í vinnusvæðinu **Sjóðsstreymisspá**. Þessi flipi mun aðeins birtast þegar eiginleiki sjóðstreymisspár er virkur. 

Á flipanum **Víddir** skal velja víddir af listanum sem á að nota fyrir síun og nota örvalyklana til að fara þá í dálkinn til hægri. Aðeins er hægt að velja tvær víddir til að sía spárgögn sjóðstreymisspár. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
