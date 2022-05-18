---
title: Stjórna B2B-viðskiptafélögum með því að nota stigveldi viðskiptavina
description: Þetta efnisatriði lýsir því hvernig á að nota stigveldi viðskiptavina til að stjórna viðskiptafélögum fyrir Microsoft Dynamics 365 Commerce viðskiptasíður fyrir viðskipti (B2B) rafræn viðskipti.
author: josaw1
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 70acdf469be2fcddd9e2bf755e958c1b20ee2fcf
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686572"
---
# <a name="manage-b2b-business-partners-using-customer-hierarchies"></a>Stjórna B2B-viðskiptafélögum með því að nota stigveldi viðskiptavina

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að nota stigveldi viðskiptavina til að stjórna viðskiptafélögum fyrir Microsoft Dynamics 365 Commerce viðskiptasíður fyrir viðskipti (B2B) rafræn viðskipti.

Í höfuðstöðvum viðskipta, a *stigveldi viðskiptavina* eining er notuð til að tákna viðskiptafélagasamtökin sem munu nota B2B rafræn viðskipti síðuna þína. Áður en þú getur byrjað að nota stigveldi viðskiptavina til að stjórna viðskiptafélögum verður þú að virkja B2B rafræn viðskipti í höfuðstöðvum Commerce og skilgreina síðan númeraröð fyrir stigveldi viðskiptavina.

## <a name="enable-the-b2b-e-commerce-feature-in-commerce-headquarters"></a>Virkjaðu B2B rafræn viðskipti í höfuðstöðvum viðskipta

Til að nota B2B rafræn viðskipti, verður þú fyrst að virkja **Virkjaðu notkun B2B eCommerce getu** þáttur í höfuðstöðvum Commerce.

1. Opna skal **Vinnusvæði \> Eiginleikastjórnun**.
1. Á **Allt** flipann, notaðu síureitinn til að leita að **Eining: Smásala og verslun**.
1. Finndu **Virkjaðu notkun B2B eCommerce getu** eiginleiki, veldu hann og veldu síðan **Virkja núna** í neðra hægra horninu.

## <a name="define-a-number-sequence-for-the-customer-hierarchy"></a>Skilgreindu númeraröð fyrir stigveldi viðskiptavina

Númeraraðir eru notaðar til að mynda lesanleg, einkvæm kennimerki fyrir skýrslur aðalgagna og færslur sem krefjast kennimerkja. Þú verður að skilgreina númeraröð sem verður notuð til að búa til auðkenni fyrir stigveldi viðskiptavina. Nánari upplýsingar um númeraraðir er að finna í [Yfirlit númeraraða](/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview).

Til að skilgreina númeraröð fyrir stigveldi viðskiptavina í höfuðstöðvum Commerce skal fylgja þessum skrefum.

1. Fara til **Verslun og verslun \> Uppsetning höfuðstöðva \> Númeraraðir \> Númeraraðir**.
1. Búðu til nýja númeraröð eða veldu núverandi númeraröð til að endurnýta hana.
1. Opnið **Retail og Commerce \> Uppsetning höfuðstöðva \> Færibreytur \> Samnýttar færibreytur Commerce**.
1. Á **Númeraraðir** flipanum, bættu númeraröðinni sem þú bjóst til eða valdir áðan við **Auðkenni viðskiptavinastigveldis** tilvísun.

![Númeraröð bætt við tilvísun auðkennisstigveldis viðskiptavinar.](../media/NumberSequenceCustHierarchy.png)

## <a name="how-the-approval-process-works"></a>Hvernig samþykkisferlið virkar

Þegar viðskiptafélagi biður um að tengjast B2B rafrænum verslunarsíðu vistar kerfið beiðnina sem a *horfur*. Persóna í höfuðstöðvum viðskipta, eins og rekstrarstjóri smásölu, getur samþykkt eða hafnað beiðnir samstarfsaðila. Fyrir frekari upplýsingar um hvernig á að stjórna beiðnum viðskiptafélaga og samþykki væntanlegra viðskiptavina, sjá [Stjórna notendum viðskiptafélaga á B2B rafrænum viðskiptavefsíðum](manage-b2b-users.md).

Þegar tilvonandi er samþykktur býr kerfið til tvær nýjar viðskiptamannafærslur:

- Einn viðskiptavinur skrár yfir **Skipulag** gerð táknar stofnunina sem biður um að verða viðskiptafélagi.
- Einn viðskiptavinur skrár yfir **Persóna** gerð táknar þann sem lagði fram beiðnina.

Að auki er ný stigveldisskrá viðskiptavina stofnuð á **Verslun og verslun \> Viðskiptavinir \> Stigveldi viðskiptavina**. Þessi stigveldisskrá viðskiptavina hefur eftirfarandi eiginleika:

- **Auðkenni viðskiptavinastigveldis** – Einstakt auðkenni viðskiptavinastigveldis. Þetta auðkenni notar númeraröðina sem þú skilgreindir í samnýttum breytum Commerce.
- **Heiti** – Fyrirtækisheiti viðskiptafélagans eins og það er tilgreint í innleiðingarferlinu. Þessi reitur er hægt að breyta.
- **Tilgangur** – Þessi eiginleiki er stilltur á fyrirframskilgreint gildi **B2B-fyrirtæki**.
- **Skipulag** – Auðkenni viðskiptavinar fyrirtækisins.

Sá sem sendi inn beiðni um inngöngu er bætt við á **Stigveldi** flýtiflipann og **Admin** þeim er falið hlutverk. Eftir því sem kerfisstjórinn bætir fleiri notendum við viðskiptafélagasamtökin á B2B síðu, er ný viðskiptavinaskrá búin til fyrir hvern notanda. Viðskiptavinaskránni er einnig bætt við viðkomandi stigveldisskrá viðskiptavinar fyrir viðskiptafélaga og **Notandi** henni er falið hlutverk.

### <a name="examples"></a>Dæmi

Aðili sem heitir Sam J. sendir inn beiðni um inngöngu fyrir hönd Microsoft stofnunarinnar. Eftir að beiðnin hefur verið samþykkt eru tveir nýir viðskiptavinareikningar búnir til: annar af **Persóna** tegund fyrir Sam J. og einn af **Skipulag** gerð fyrir Microsoft.

Eins og dæmið í eftirfarandi mynd sýnir er ný stigveldisskrá viðskiptavina einnig búin til. Þessi skrá hefur sama nafn og stofnunin (**Microsoft**), og **Admin** hlutverki er úthlutað til Sam J. Sem stjórnandi bætir Sam J. öðrum Microsoft notendum B2B síðunnar við þetta stigveldi og úthlutar **Notandi** til þeirra. Í þessu dæmi hefur Sush R. verið bætt við sem notanda.

![Dæmi um stigveldisfærslu viðskiptavina.](../media/CustomerHierarchy2.png)

Til að ákvarða hvort viðskiptavinur sé tengdur við stigveldi viðskiptavina skal opna viðskiptamannafærsluna. Eins og dæmið í eftirfarandi mynd sýnir, er **Auðkenni viðskiptavinastigveldis** sviði í **B2B** kafla um **Smásala** Flýtiflipi sýnir hvort viðskiptavinurinn er hluti af stigveldi viðskiptavina, og **B2B stjórnandi** valkostur gefur til kynna hvort viðskiptavinurinn sé stjórnandi þess stigveldis.

![Dæmi um B2B hlutann á Smásala flýtiflipanum í viðskiptamannafærslu, þar sem viðskiptavinurinn er tengdur stigveldi og tilgreindur sem stjórnandi.](../media/CustomerHierarchyMapping2.png)

Í flestum tilfellum ættu eignagildi allra viðskiptavinaskrár í stigveldi að passa saman. Sem dæmi, þar sem allir notendur viðskiptafélaga eiga að fá svipuð verð fyrir afurðir, ætti verðflokkur þeirra og tengdar skilgreiningar að passa saman. Kerfið framfylgir samt sem áður ekki þessari samsvörun. Þess vegna eru tilheyrandi notendur Commerce Headquarters ábyrgir fyrir því að tryggja að gildi eiginleika og skilgreiningar passi saman fyrir alla viðskiptavini í tilgreindu stigveldi.

Notendur viðskiptahöfuðstöðva geta skoðað eignagildi fyrir allar viðskiptavinaskrár í stigveldi í hlið við hlið. Eins og dæmið í eftirfarandi mynd sýnir geturðu notað **Almennt** valmöguleika í fellilistanum á **Stigveldi** Flýtiflipa og veldu síðan hvaða hluta viðskiptamannafærslunnar sem er til að sýna tengda eiginleika. Notendur geta breytt eignagildum beint í þessu yfirliti. Til að afrita öll gildi úr viðskiptamannaskrá stjórnanda til allra notenda skaltu velja **Hneka** á **Stigveldi** Flýtiflipi.

![Dæmi um stigveldisskrá viðskiptavina, sem sýnir Hneka hnappinn og valmöguleikann í fellilistanum.](../media/HierarchyDetails2.png)

[!include [footer-include](../../includes/footer-banner.md)]
