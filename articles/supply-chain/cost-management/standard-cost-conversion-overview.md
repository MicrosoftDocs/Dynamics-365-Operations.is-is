---
title: Yfirlit yfir staðlaðan kostnaðarumreikning
description: Þessi grein veitir yfirlit yfir vinnslu til að aðstoða við að setja upp og keyra umreikning staðalkostnaðar. Skref sem eru skráð er ætlað að vera lokið eftir að forkröfur fyrir umreikning staðalkostnaðar hafa verið uppfylltar.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: 78212
ms.assetid: d601d9d5-1de3-4868-aff4-534dca01d624
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bcbd8464532722c83f170db6b19cca5dd77846a0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011798"
---
# <a name="standard-cost-conversion-overview"></a>Yfirlit yfir staðlaðan kostnaðarumreikning

[!include [banner](../includes/banner.md)]

Þessi grein veitir yfirlit yfir vinnslu til að aðstoða við að setja upp og keyra umreikning staðalkostnaðar. Skref sem eru skráð er ætlað að vera lokið eftir að forkröfur fyrir umreikning staðalkostnaðar hafa verið uppfylltar. 

Notið síðuna **Staðlaður kostnaðarumreikningur** til þess að umbreyta birgðalíkani fyrir runu af völdum vörum úr raunverulegum kostnaðargrunni í staðlaða kostnaðarnálgun. Umreikningsferlið felur í sér birgðalokun, sem er nauðsynleg forsenda, nokkur skref koma til framkvæmda á breytingatímabili sem er skilgreint með upphafsdagsetningu breytinga og áætlaðri umreikningsdagsetningu og síðan er umreikningur framkvæmdur ásamt tengdri birgðalokun.

-   Birgðalokun fyrir breytingatímabil − Birgðalokun er forkrafa, því hún jafnar opnar færslur vöru samkvæmt eldri birgðamatsaðferð. Hægt er að færa inn og bóka endurdagsettar færslur, eins og reikninga, á breytingatímabilinu svo hægt sé að loka fyrra tímabili. Dagsetning birgðalokunar verður að vera einum degi fyrr en upphafsdagsetning breytinga til þess að tryggja skörp skil gagnvart eldri matsaðferð.
-   Umreikningsskref í breytingatímabili − Notið skjámyndina **Stöðluð kostnaðarumbreyting** til þess að stofna umreikningsfærslu sem einnig inniheldur notendaskilgreint kenni fyrir nýja kostnaðarútgáfu. Notandi skilgreinir þær vörur sem þarfnast umbreytingar og færir inn yfirvofandi staðlaðan kostnað vörunnar innan hinnar nýju kostnaðarútgáfu. Notandi framkvæmir eftirlit með völdum vörum til að bera kennsl á atriði sem gætu hindrað umreikning, leysir úr þeim og framkvæmir svo annað eftirlit. Þegar allar vörur hafa staðist athugun er stöðu umreikningsfærslunnar breytt í **Tilbúið**. Framkvæmið umreikning á áætlaðri umreikningsdagsetningu, með birgðalokun ef vill. Birgðahreyfingar vöru á breytingatímabilinu eru bókaðar og metnar í samræmi við gamla birgðalíkanið. Síðan eru birgðahreyfingar endurmetnar til staðlaðs kostnaðar eftir að umreikningi er lokið.
-   Birgðalokun fyrir umreikning  − Hægt er að hafa birgðalokun sem hluta umreiknings á áætlaðri umreikningsdagsetningu eða framkvæma hana sem sérstakt skref fyrir umreikninginn.

Þegar birgðalokunarferlið hefur tekist verður birgðalíkan hverrar vöru byggt á stöðluðum kostnaði og staðlaður kostnaður er virkjaður fyrir vöruna. Birgðafærslur sem gerðar eru hér eftir verða metnar samkvæmt stöðluðum kostnaði vöru. Þar að auki umreiknar kerfið efnislegar birgðafærslur vöru í inn- og úthreyfingum í staðlaðan kostnað byggt á umreikningsdagsetningu. Kerfið umbreytir jafnframt fjárhagslegum birgðum á lager fyrir vöru í staðlaðan kostnað og bókar gildismismuninn sem endurmatsfrávik. Allar færslur sem eiga sér stað eftir umbreytinguna eru metnar út frá stöðluðum kostnaði. Ekki er hægt að færa bakfærðar færslur fyrir umreikningsdagsetninguna, því þarf að framkvæma birgðalokun einum degi á undan dagsetningu umreiknings. Aðeins er hægt að framkvæma umreikning ef birgðalokun var framkvæmd einum degi fyrr. Ekki er hægt að hætta við þessa birgðalokun.

## <a name="1-define-a-standard-cost-conversion-record-and-the-associated-costing-version"></a>1. Skilgreina umreikning staðalkostnaðar og tengda kostnaðarútgáfu
Nota skal síðuna **Umreikningur staðalkostnaðar** til að stofna umreikningsfærslu. Einungis er hægt að stofna nýja umreikningsfærslu ef búið er að ljúka við eldri umreikningsfærslur. Lengd á áætluðu breytingatímabili er skilgreind af upphafsdagsetningu breytinga og áætlaðri umreikningsdagsetningu. Áætlað breytingatímabil getur verið jafn stutt og einn dagur. Áætlað breytingatímabil hjálpar við að tryggja að umreikningsferlið hafi næga tíma til að ljúka við öll skref þess. Birgðalokun verður að vera framkvæmd einum degi fyrir upphafsdagsetningu breytinga, til að hjálpa til við að tryggja að uppgjörum sé lokið áður en umreikningsferli hefst. Til að ganga úr skugga um að upphafsdagsetning breytinga og dagsetning birgðalokunar passi saman er annað hvort hægt að breyta upphafsdagsetningu breytinga í einum degi eftir fyrirliggjandi birgðalokun, eða framkvæma birgðalokun. Þegar umreikningsfærsla er færð inn, þarf líka að færa inn notendaskilgreint kenni fyrir nýja kostnaðarútgáfu sem mun innihalda staðlaðan kostnað fyrir umreiknaða vöru. Kostnaðarútgáfan stofnast sjálfkrafa þegar umreikningsskýrslan er vistuð.

## <a name="2-review-and-change-the-new-costing-version-for-the-conversion-record"></a>2. Fara yfir og breyta nýstofnaðri kostnaðarútgáfu fyrir umreikningsfærsluna
Nýstofnuð kostnaðarútgáfa er sérnýtt fyrir umreikningsfærsluna, eins og sést í kostnaðargerðinni **Umreikningur**. Sérnýtta kostnaðarútgáfan er svipuð kostnaðarútgáfu fyrir staðlaðan kostnað, og mun innihalda vörukostnaðarfærslu fyrir vörur sem eru tengdar umreikningsfærslunni. Sérnýtta kostnaðarútgáfan fyrir umreikningsfærslu hefur eftirfarandi einkenni, sem fara þarf yfir og breyta eftir þörfum í hinum mismunandi flipum:

-   **Kostnaðargerð:** Þetta svæði ætti að vera stillt á **Staðalkostnaður**.
-   **Útgáfa:** − Kennið endurspeglar upplýsingarnar sem eru færðar inn í umreikningsfærsluna fyrir kenni kostnaðarútgáfunnar.
-   **Heiti:** Sem sjálfgefið er þetta svæði autt. Hægt er að færa inn heiti.
-   **Loka:** Þetta svæði ætti að vera stillt á **Nei**. Hægt er að færa inn kostnaðarfærslur í kostnaðarútgáfu þar til stöðu umreikningsfærslu er breytt í **Tilbúið**. Staðan **Tilbúið** merkir að valdar vörur hafa verið merktar og að breytingar á kostnaðarfærslum verði ekki leyfðar.
-   **Loka á virkjun:** Þetta svæði ætti að vera stillt á **Já**. Ekki er hægt að virkja handvirkt kostnaðarfærslu í bið innan sérnýttu kostnaðarútgáfunnar. Virkjun er framkvæmd þegar umbreytingin hefur tekist.
-   **Frá dagsetningu** - Dagsetningin frá endurspeglar áætlaða umreikningsdagsetningu sem er færð inn í umreikningsfærslu.
-   **Svæði:** Skiljið þennan reit eftir auðan, þannig að hægt sé að færa inn kostnaðarfærslur fyrir öll svæði.
-   **Leyfa svæðisflokka verðtegunda:** Þetta svæði ætti að vera stillt á **Já**, þannig að eingöngu sé hægt að færa inn kostnaðarverðsfærslur.
-   **Varaúrræði:** Þetta svæði er stillt á **Ekkert**. Breytið varaúrræðinu í **Virkt** ef þörf er á kostnaðarupplýsingum sem hafa verið virkjaðar í öðrum kostnaðarútgáfum. Til dæmis geta kostnaðarupplýsingar um íhluti, kostnaðartegundir og óbeinan kostnað verið nauðsynlegar til þess að reikna kostnað við framleidda vöru.
-   **Kostnaðarútgáfa til vara:** Skiljið þetta svæði eftir autt.

Upplýsingum um vörukostnað innan sérnýttu kostnaðarútgáfunnar er bara hægt að viðhalda úr síðunni **Umreikningur staðalkostnaðar**. Ekki er hægt að nota síðurnar **Uppsetning kostnaðarútgáfu** eða **Viðhald kostnaðarútgáfu** til að reikna út kostnað fyrir kostnaðarútgáfuna við umbreytingu. Samt sem áður er hægt að nota þessar síður til að viðhalda sérnýttu kostnaðarútgáfunni þegar umreikningur hefur tekist.

## <a name="3-identify-the-items-to-convert-to-standard-cost"></a>3. Auðkenna vörurnar sem á að umreikna í staðlaðan kostnað
Nota skal síðuna **Umreikningur staðalkostnaðar** til að auðkenna vörurnar sem á að umreikna í staðlaðan kostnað. Hægt er að bæta mörgum vörum við með því að nota síðuna **Bæta vörum við umreikning staðalkostnaðar**. Almennt séð er gott að hafa allar framleiddar vörur með í einni einstakri umreikningsfærslu svo kostnaður verði rétt reiknaður.

## <a name="4-enter-or-calculate-the-pending-standard-cost-for-each-item-that-is-being-converted"></a>4. Færa inn eða reikna staðlaðan kostnað í bið fyrir hverja vöru sem á að umreikna
Notið síðuna **Vöruverð** til þess að færa inn staðlaðan kostnað í bið í sérnýttu kostnaðarútgáfunni fyrir keypta vöru og flutningsvöru. Kostnaðarfærslur eru svæðisbundnar og nauðsynlegt er að færa inn kostnað í bið fyrir hvert svæði. Notið síðuna **Vöruverð** til að reikna kostnaðarfærslur í bið fyrir framleiddar vörur. Kostnað í bið fyrir framleidda vöru ætti að reikna fyrir hvert framleiðslusvæði nema ef svæðið stendur fyrir flutningssvæði. Í því tilfelli ætti að færa kostnað í bið inn handvirkt. Sumar vörur hafa hugsanlega vöruvíddir eins og lit, stærð eða skilgreiningu. Á síðunni **Umreikningur staðalkostnaðar** sýnir gátreiturinn **Nota kostnaðarverð eftir afbrigði** staðlaðan kostnað fyrir sérhverja samsetningu afurðarvídda. Þegar þessi gátreitur er hreinsaður þarf einungis að færa inn kostnað í bið fyrir vöruna.

## <a name="5-check-and-resolve-any-issues-for-the-items-that-are-being-converted"></a>5. Fara yfir og leysa vandamál sem geta komið upp varðandi vörur sem verið er að umreikna
Nota skal skýrsluna **Athuganir á umreikningi staðalkostnaðar** til að auðkenna vandamál fyrir vörurnar sem verið er að umbreyta. Ef engin vandamál finnast fyrir vöru er stöðu hennar í umreikningsfærslunni breytt í **Villuleitað**. Ef vandamál finnst þarf fyrst að leysa það og síðan keyra skýrsluna aftur þar til stöðunni er breytt í **Villuleitað**. Ef ekki er hægt að leysa vandamál vöru í tæka tíð má velja að eyða vörunni úr umreikningsfærslunni og umreikna hana síðar.

## <a name="6-change-the-status-of-the-conversion-record-to-ready"></a>6. Breyta stöðu umreikningsfærslu í Tilbúin
Þegar stöðu umreikningsfærslu er breytt í **Tilbúið**, er lokayfirferð keyrð áður en staðlaður kostnaðarumreikningur er keyrður. Staðan mun einungis breytast í **Villuleitað** þegar eftirfarandi skilyrði hafa verið uppfyllt:

-   Hver vara í umreikningsfærslunni er með stöðuna **Villuleitað**.
-   Birgðalokun var framkvæmd á dagsetningu sem er einum degi fyrr en upphafsdagsetning umreiknings. Til að ganga úr skugga um að upphafsdagsetning breytinga og dagsetning birgðalokunar passi saman er annað hvort hægt að breyta upphafsdagsetningu breytinga í einum degi eftir fyrirliggjandi birgðalokun, eða framkvæma birgðalokun.

## <a name="7-back-up-the-database-before-conversion"></a>7. Gerið öryggisafrit af gagnagrunninum fyrir umreikning
Öryggisafritið gerir mögulegt að endurheimta gagnagrunninn ef villur koma upp í umreikningsferlinu.

## <a name="8-perform-the-conversion-when-the-conversion-record-has-a-ready-status"></a>8. Framkvæma umreikning þegar umreikningsfærsla hefur stöðuna Tilbúið
Umreikningsferlið útheimtir að birgðalokun sé framkvæmd á dagsetningu sem er einum degi á undan dagsetningu fyrirhugaðs umreiknings. Þessi krafa tryggir að ekki sé hægt að færa bakfærðar færslur inn á umreikningstímabilinu. Ef birgðalokun hefur ekki enn farið fram, spyr kerfið hvort eigi að framkvæma hana sem hluta af umreikningsferlinu. Umreikningsferlið annast eina vöru í einu. Það hefst með vöru á lægsta stigi í framleiðsluferlinu, byggt á lágstigskóða vörunnar. Þegar vöru hefur verið breytt, er stöðu hennar í umreikningsfærslunni breytt í **Umbreytt**. Ef umreikningsferlið er truflað munu vörur sem ekki hefur tekist að umreikna halda áfram að hafa stöðuna **Villuleitað**. Ef tekst að ljúka umreikningsferlinu hefur það eftirfarandi áhrif:

-   Staða umreikningsfærslu breytist úr **Tilbúið** í **Lokið**, og staða hverrar valinnar vöru breytist úr **Villuleitað** í **Umbreytt**.
-   Birgðalíkansflokki umbreyttra vara hefur verið breytt þannig að hann endurspegli nýjan flokk með stöðluðu birgðalíkani kostnaðar.
-   Staðlaður kostnaður fyrir umreiknaðar vörur hefur verið virkjaður í sérnýttu kostnaðarútgáfunni.
-   Kostnaðartegund kostnaðarútgáfunnar breytist úr **Umreikningur** í **Staðlaður kostnaður**, og kostnaðarútgáfan hagar sér nú eins og hver önnur kostnaðarútgáfa fyrir staðlaðan kostnað.

## <a name="9-validate-and-reconcile-the-inventory-values-for-the-converted-items"></a>9. Villuleita og afstemma birgðagildi fyrir umreiknaðar vörur
Skýrslan **Yfirlit fráviksgreiningar** gerir það mögulegt að greina frávik á endurmati og skýrslan **Birgðavirði** gerir kleift að skoða birgðagildi á tiltekinni dagsetningu.

-   Greina endurmatsfrávik. Notið skýrsluna **Yfirlit fráviksgreiningar** til þess að skoða endurmatsfrávik birgða fyrir umreiknaðar vörur. Einnig er hægt að nota síðuna **Færslur staðalkostnaðar** til þess að skoða endurmatsfærslur birgða fyrir umreiknaðar vörur sem hafa birgðir.
-   Greina birgðavirði fyrir upphafsdagsetningu breytinga. Notið skýrsluna **Birgðavirði** til þess að skoða birgðavirði fyrir umreiknaðar vörur. Fyrir Til dagsetningar í skýrslunni skal nota dagsetningu sem er einum degi fyrr en upphafsdagsetning breytinga.
-   Greina birgðavirði fyrir upphafsdagsetningu umreiknings. Notið skýrsluna **Birgðavirði** til þess að skoða birgðavirði fyrir umreiknaðar vörur. Fyrir Til dagsetningar í skýrslunni skal nota dagsetningu sem er einum degi fyrr en dagsetning umreiknings.
-   Greina birgðavirði á dagsetningu umreiknings. Notið skýrsluna **Birgðavirði** til þess að skoða birgðavirði frá og með umreikningsdagsetningu. Bæði Frá dagsetningu og  Til dagsetningar í skýrslunni ætti að stemma við umreikningsdagsetningu. Valskilyrði skýrslu eiga að endurspegla umreiknaðar vörur.
-   Greina bakfærðar birgðahreyfingar. Notið skýrsluna **Birgðavirði** til þess að skoða bakfærðar birgðahreyfingar sem voru færðar inn eftir umreikning. Notið skýrsluvalkostinn fyrir Frá og Til dagsetningar, svo þær samsvari upphafsdagsetningu og umreikningsdagsetningu að frádregnum einum degi. Valskilyrði skýrslu eiga að endurspegla umreiknaðar vörur. Skýrslan birtir birgðahreyfingar gerðar með stöðluðum kostnaði þegar umreikningsferlið stóð yfir.


<a name="additional-resources"></a>Frekari upplýsingar
--------

[Forkröfur fyrir umreikning staðalkostnaðar](prerequisites-standard-cost-conversion.md)



