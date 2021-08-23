---
title: Leita að upplýsingum með uppflettingum
description: Í þessu efnisatriði muntu læra um uppflettingaraðgerðir og færð nokkur góð ráð til að ná ákjósanlegri notkun úr uppflettingum í kerfinu.
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 269934
ms.assetid: f20cbd2c-14e0-47e7-b351-8e60d3537f96
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 46ae85fc4f4f305d1ff8063b43aeef51d043742f9860940add0e0dbca02413d4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750461"
---
# <a name="find-information-by-using-lookups"></a>Leita að upplýsingum með uppflettingum

[!include [banner](../includes/banner.md)]

Mörg svæði hafa uppflettingar sem getur hjálpað við að finna auðveldlega rétt eða viðeigandi gildi. Nokkrum viðbótum hefur verið bætt við uppflettingar sem gera þessar stýringar nothæfari og auka framleiðni notenda. Í þessu efnisatriði muntu læra um þessar nýju uppflettingaraðgerðir og færð nokkur góð ráð til að ná ákjósanlegri notkun úr uppflettingum í kerfinu.

## <a name="responsive-lookups"></a>Gagnvirkar uppflettingar

Í fyrri útgáfum, þegar samskipti eru höfð við uppflettistýringu myndi notandi verða að nota skýra aðgerð til að opna í fellilista. Þetta gæti hafa verið með því að færa inn stjörnu (\*) í stýringu til að sía uppflettingu samkvæmt núverandi gildi stýringarinnar, því að smella á hnappinn fellilistanum eða með því að nota **Alt**+**Niður ör** flýtilykli. Uppflettistýringum hefur verið breytt á eftirfarandi hátt til að samræmast betur gildandi vefvenjum:

- Fellilistavalmyndir uppflettingar munu nú opnast sjálfkrafa eftir stutt hlé í vélritun, með efni fellilistans fyrir valmyndinni síað eftir gildi uppflettingar fjárhagsáætlunarstýringar.

    Athugið að gömlu hegðun sjálfvirkrar opnunar fellilista eftir ritun stjörnu (\*) hefur verið hætt.

- Eftir að uppfletting fellilista hefur opnað á eftirfarandi sér stað:

    - Bendillinn verður áfram í uppflettistýringu (en ekki fluttur inn í fellilista áherslu) svo að hægt er að halda áfram að gera breytingar á gildi stýringarinnar. Hins vegar getur notandinn enn notað **Upp ör** og **Niður ör** til að breyta línum í fellilista og færa inn til að velja núgildandi línu fyrir fellilista.
    - Innihald í fellilista verður leiðrétta eftir hvaða breytingar eru gerðar í stýringu uppflettingargilda.

Til dæmis, íhugið uppflettisvæðinu sem kallast **Borg**.

Þegar áhersla er á **Borg** er hægt að hefja leit að borg sem óskað er með því að slá nokkrar stafi, eins og "col." Eftir að hætt er að slá inn opnast uppflettingin sjálfkrafa, afmörkuð við þær borgir sem byrja á "col".

[![typeaheadLookupExample.](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png)

Á þessum tímapunkti, er bendillinn enn í uppflettisvæðinu. Ef haldið er áfram því að slá svo gildið "colum" er efni uppflettingar leiðrétt sjálfkrafa til að endurspegla síðasta gildi stýringarinnar.

![updateFilterLookupExample.](./media/updatefilterlookupexample.png)

Jafnvel þótt áhersla sé enn í uppflettistýringu er einnig hægt að nota lyklana **Upp ör** eða **Niður ör** til að merkja línuna sem á að velja. Ef smellt er á **Færið** verður auðkennd lína valin úr leitinni og gildi stýringarinnar verður uppfært.

![changingSelectionLookup.](./media/changingselectionlookup.png)

## <a name="typing-in-more-than-ids"></a>Slegið inn meira en kenni

Við gagnainnfærslu er eðlilegt fyrir notendur að reyna að auðkenna aðila, eins og viðskiptavin eða lánardrottinn með heiti en ekki kenni fyrir eininguna. Margar (en ekki allar) leitir leyfa nú samhengisgögn. Þessi öflugi eiginleiki leyfir notandanum að færa Kenni eða samsvarandi nafn í stýringu uppflettingu.

Til dæmis, íhugið svæðið **viðskiptavinalykil** þegar sölupöntun er stofnuð. Þetta svæði sýnir á **Kenni reiknings** fyrir viðskiptavin, en notandi myndi yfirleitt vilja færa inn **lykilheiti** í stað **Kennis reiknings** fyrir þetta svæði þegar sölupöntun er stofnuð, eins og "Forest Wholesales" en "US-003."

Ef notandinn byrjaði að færa inn **Kenni reiknings** í uppflettistýringu myndi fellilistinn opnast eins og lýst er í fyrri hluta og notandinn myndi sjá uppflettinguna eins og sýnt er hér að neðan.

[![Samhengisháð uppfletting þegar kenni viðskiptavinalykils er fært.](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)

Hins vegar getur notand nú einnig fært inn upphaf í **lykilheiti**. Ef þetta uppgötvast mun notandinn sjá eftirfarandi uppflettingu. Athugaðu hvernig dálkurinn **Heiti** er fluttur til að vera fyrsti dálkur í uppflettingu og hvernig uppfletting raðast og er síuð samkvæmt dálknum **Heiti**.

[![Samhengisháð uppfletting þegar Heiti viðskiptavinar er fært inn.](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)

## <a name="using-grid-column-headers-for-more-advanced-filtering-and-sorting"></a>Notkun dálkahausa hnitanets fyrir ítarlegri afmörkun og röðun

Endurbætur á uppflettingu sem fjallað er um í fyrri tveimur köflum auka getu notanda mjög til að fara í línur í "byrja" leit á grundvelli uppflettingar í **Kenni** eða **Heiti** í uppflettisvæðinu. Hins vegar eru aðstæður þar sem ítarlegri afmörkun (eða röðun) þarf til að finna í réttri röð. Í þessum aðstæðum þarf notandinn að nota valkosti afmörkunar og röðunar í dálkahausum hnitanets í uppflettisvæðinu. Til dæmis, íhugið starfsmanns við sölupöntunarlínu sem þarf að finna rétta „kapalinn“ sem afurðar. Ekki er hjálplegt að slá inn „kapla“ í stýringuna **Vörunúmer**, þar sem engin afurðarheiti hefjast á „köplum.“

![emptyitemlookup.](./media/emptyitemlookup.png)

Þess í stað þarf notandinn að hreinsa gildi uppflettistýringar, opna fellilista uppfletting og sía fellilista með dálkfyrirsögn hnitanets, eins og sýnt er hér að neðan. Notandi músar (eða snertiskjás) getur einfaldlega smellt (eða snert) hvaða dálkhaus sem er til að komast í valkosti síunar og röðunar fyrir þann dálk. Fyrir notanda lyklaborðs þarf notandinn einfaldlega að ýta á **Alt**+**Niður** **ör** aftur til að færa áhersluna inn í fellilista, en eftir það getur notandinn farið í réttan dálk rétt og stutt síðan á **Ctrl**+**G** til að opna fellilista dálkfyrirsagar í hnitanetinu.

[![gridfilteritemlookup.](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png)

Eftir að afmörkun hefur verið beitt (sjá myndina hér fyrir neðan), getur notandinn fundið og valið línuna eins og venjulega.

![filtereditemlookup.](./media/filtereditemlookup.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]