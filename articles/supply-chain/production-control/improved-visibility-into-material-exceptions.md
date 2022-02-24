---
title: Innsýn í efnisundantekningar
description: Þetta efni lýsir því hvernig hægt er að fá betri innsýn í hráefnisundantekningar fyrir framleiðslupantanir og runupantanir.
author: johanhoffmann
manager: tfehr
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgShopSupervisorWorkspace, WHSProdWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 0c17997d9dd04559fb7022fe39bb2b961c1cfc4a
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4430680"
---
# <a name="visibility-into-material-exceptions"></a>Innsýn í efnisundantekningar

[!include [banner](../includes/banner.md)]

Á vinnusvæðinu **Stjórnun á framleiðslugólfi**, gefa þrír reitir betri innsýn í hráefnisundantekningar fyrir framleiðslupantanir og runupantanir:

- Óútgefnar efnislínur sem þarf að athuga
- Óunnar bylgjur sem þarf að athuga
- Opin vöruhúsavinna sem þarf að athuga

Fyrir alla þrjá reiti, er hráefnisdagsetning uppskriftarlína (BOM) og formúlulína borinn saman við vinnusvæðisdagsetninguna og einnig við síur fyrir **Framleiðslueining**, **Tilfangaflokkur** og **Tilföng** sem eru stilltar í **Grunnstilla vinnusvæðið mitt** valmynd. Sjálfgefið er að vinnusvæðisdagsetningin sé stillt á núgildandi dagsetningu, en hægt er að leiðrétta það.

Óútgefin uppskriftarlína eða formúlulína krefjast athygli ef hráefni dagsetning línunnar er sú sama eða fyrr en vinnusvæðisdagsetningin, og ef það uppfyllir viðmiðin sem eru skilgreind með síum í vinnusvæðinu.

Í eftirfarandi mynd táknar bláa stöngin framleiðsluverk sem er áætlað á tilfang. Áætlað er að verkið hefjast 1. maí 2017 (2017/05/01). Þessi dagsetning er hráefnisdagsetningin. Með öðrum orðum verður það efni sem eru úthlutað á verkið á uppskriftar- og formúlulínunum að vera tilbúið á þessum degi. Hinn dagsetning í myndinni, 6. maí 2017 (2017/05/06), táknar dagsetningu vinnusvæðisins. Í þessu dæmi er hráefnisdagsetningin fyrr en vinnusvæðisdagsetningin. Þess vegna er dagsetningin þegar notkun hráefnisins átti að hefjast liðin, og uppskriftar- og formúlulínurnar uppfylla viðmiðanirnar sem kalla á athygli.

![Dæmi um framleiðsluverk þar sem dagsetning hráefnisins er fyrr en dagsetning vinnusvæðis](./media/improved-visibility.png)

## <a name="unreleased-material-lines-needing-attention"></a>Óútgefnar efnislínur sem þarf að athuga

Uppskriftar- eða formúlulína er hægt að losa til vöruhússins á þrjá vegu:

- Sem hluti af losun framleiðslupöntunar eða runupöntunar
- Sem handvirk losun
- Sjálfvirkt gegnum runuvinnslu

Frekari upplýsingar, sjá [Losa uppskriftar- og formúlulínur í vöruhúsið](releasing-bom-and-formula-lines-to-warehouse.md). 

Ef uppskriftar- eða formúlulínur hafa ekki verið losaðar eða aðeins losaðar að hluta til, og ef dagsetning og síuskilyrði vinnusvæðisins eru uppfyllt er línan innifalinn í útreikningi á númerinu sem birtist á reitnum **Ólosaðar efnislínur sem þarfnast athygli**.

Þegar þú velur reitinn, er **Losa í vöruhús** síðan opnuð. Þessi síða sýnir fjölda ólosaðar uppskriftar- og formúlulínum sem er uppgefinn með tölunni í reitnum. Þessar ólosuðu línur birtast í efra hnitanetinu. Þetta hnitanet sýnir magnið sem upphaflega var áætlað fyrir línuna, magnið sem þegar hefur verið losað og það magn sem eftir er og verður að losa. Hægt er að bæta við línum úr efra hnitanetinu í það neðra. Úr neðra hnitanetinu er síðan hægt að losa valdar línur í vöruhúsið. Úr neðra hnitanetinu er einnig hægt að stilla magnið til að losa þannig að aðeins hluta magn er sleppt.

## <a name="unprocessed-waves-needing-attention"></a>Óunnar bylgjur sem þarf að athuga

Þegar uppskriftar- eða formúlulína er losuð, er henni bætt við annaðhvort nýja framleiðslubylgju eða fyrirliggjandi opna bylgju, allt eftir stillingu sniðmáts framleiðslubylgjunnar. Með stillingu bylgjusniðmátsins geturðu einnig sett upp bylgju þannig að hún sé sjálfkrafa unnin þegar uppskriftar- eða formúlulína er losuð. Þegar bylgjan er unninn er myndað vöruhúsaverk fyrir tiltekt hráefnis. Ef bylgjusniðmátið er stillt þannig að bylgjur séu ekki unnar þegar losun á sér stað, þá er verður bylgjan áfram í óunnu ástandi. Reiturinn **Óunnar bylgjur sem þarfnast athygli** sýna fjölda uppskriftar- og formúlulína sem hafa verið losaðar í vöruhúsið á óunnum bylgjum, og hafa hráefnisdagsetningu sem er fyrr en eða sú sama og vinnusvæðisdagsetningin. Línurnar verða einnig að vera notaðar af aðgerðartilfangi sem gildir um síu vinnusvæðisins.

Þegar reiturinn er valinn er **Allar framleiðslubylgjur** síðan opnuð. Þessi síða er síuð út frá fjölda opinna bylgja sem innihalda bylgjulínur frá losuðum uppskriftar- og formúlulínum sem uppfylla viðmiðanirnar fyrir reitinn. Frá síðunni **Allar framleiðslubylgjur** geturðu handvirkt unnið bylgjuna.

## <a name="open-warehouse-work-needing-attention"></a>Opin vöruhúsavinna sem þarf að athuga

**Opin vöruhúsaverk sem þarfnast athygli** reiturinn sýnir fjölda uppskrifta- og formúlulína sem hafa verið losaðar í vöruhúsið, sem innihalda óunnin verk, og hafa hráefnisdagsetningu sem er fyrr en eða sú sama og vinnusvæðisdagsetningin. Línurnar verða einnig að vera notaðar af aðgerðartilfangi sem gildir um síu vinnusvæðisins.

Þegar reiturinn er valinn, opnast síðan **Öll verk**. Þessi síða er síuð út frá fjölda opinna vinnuhausa sem innihalda verklínur úr losuðum uppskriftar- og formúlulínum sem uppfylla viðmiðanirnar fyrir reitinn. Frá **Öll verk** síðunni er hægt að vinna verkið handvirkt.
