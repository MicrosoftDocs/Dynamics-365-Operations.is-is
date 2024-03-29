---
title: Skilgreina reiti fyrir farsímaforrit Warehouse Management
description: Þessi grein lýsir því hvernig á að skilgreina og grunnstilla heiti og forgangsröð reita sem sýndir eru í farsímaforrit vöruhúsakerfis.
author: Mirzaab
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 00a20faaa05a9d0891ee202951b1ca50d0176c83
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065959"
---
# <a name="configure-fields-for-the-warehouse-management-mobile-app"></a>Skilgreina reiti fyrir farsímaforrit Warehouse Management

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig á að skilgreina og grunnstilla heiti og forgangsröð reita sem sýndir eru í farsímaforrit vöruhúsakerfis.

> [!NOTE]
> Þessi grein á við aðgerðir í vöruhúsakerfi. Það á ekki við um aðgerðir í birgðastjórnun. Farsímaforrit vöruhúsakerfis er forrit sem hægt er að nota í framkvæmd vöruhúsaverkefna. Hægt er að skilgreina og grunnstilla reitarheiti sem eru notuð í forritinu, ásamt því að grunnstilla forgang sem reitarheitum ætti að vera úthlutað eftir. Þessi grein útskýrir því hvernig á að skilgreina og grunnstilla svæðaheiti og forgang farsímaforrit vöruhúsakerfis og hvernig þau eru notuð í Warehousing.

## <a name="configure-warehouse-app-field-names"></a>Grunnstilla reitarheiti vöruhúsaforrits

Þegar þú notar Warehousing í fartækinu geturðu skilgreint hvernig lýsigögn skulu birt í tækinu á síðunni **Reitarheiti vöruhúsaforrits**. Í nýju fyrirtæki skal velja **Stofna sjálfgefna uppsetningu** til að mynda öll reitaheiti sem verða notuð í verkflæðum vöruhússfartækja og svo úthluta æskilegan ílagsham og ílagsgerð á þau. Eftir að þú hefur myndað öll reitarheiti, geturðu valið eftirfarandi ílagsvalkosti.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valkostur</th>
<th>lýsing</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Æskilegur ílagshamur</td>
<td>Þessi valkostur skilgreinir hvort sýna eigi skönnunarreit eða ílagsreit fyrir handvirka færslu fyrir valið heiti reitar. Þetta er gagnlegt til að aðgreina reiti eftir því hvort strikamerki eru notuð fyrir reitinn. <strong>Athugasemd:</strong> Fyrir reitarheiti með æskilega innsláttarstillingu stillta á <strong>Skönnun</strong> er hægt að færa inn upplýsingar handvirkt ef strikamerki er ólæsilegt eða skemmt.</td>
</tr>
<tr class="even">
<td>Inntaksgerð</td>
<td>Þessi valkostur skilgreinir hvaða innsláttargerð ætti að vera notuð fyrir valið reitarheiti. Fjórir valkostir eru í boði.
<ul>
<li><strong>Val</strong> - Inniheldur lista yfir tiltæka valkosti til að velja úr. Reitaheitum með þennan valkostur er ekki hægt að breyta.</li>
<li><strong>Dagsetning</strong> - Reitaheiti sem eru skilgreind sem dagsetning munu sýna dagsetningarsnið með merkinu. Þetta hjálpar starfsmanni í vöruhúsi að sjá á hvaða sniði eigi að færa inn dagsetningu. Reitaheitum með þennan valkostur er ekki hægt að breyta.</li>
<li><strong>Stafir</strong> - Ef valið verður lyklaborð tækisins notað þegar upplýsingar eru færðar handvirkt í forritið. Hægt er að breyta lyklaborðsupplifun eftir því hvaða tæki er notað.</li>
<li><strong>Tölustafir</strong> - Fyrir reitaheiti sem nota aðeins tölustafi sem ílag geturðu valið þennan valkost til að birta sérsniðið talnalyklaborð með ílagssvæðinu í stað lyklaborðs tækis.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a>Grunnstilla reitaforgang vöruhúsaforrits

Á síðunni **Svæðisforgangur vöruhúsaforrits** síða, geturðu sett reitarheiti inn í mismunandi forgangsflokka. Þetta gerir kleift að ákveða hvaða upplýsingar ætti að birta á aðalverkefnasíðunni þegar starfsmaður í vöruhúsi framkvæmir verkefni með notkun forritsins. Ef smellt er á **Stofna sjálfgefna uppsetningu**, verður sjálfgefinn hópur forgangsflokks myndaður. Hægt er að stofna eins marga forgangsflokka og þörf er á, en aðeins þrír forgangsflokkar verða sýndir á verkefnasíðunni. Þegar kerfið sendir lýsigögn í forritið mun það úthluta hverju svæði hlutfallslegum forgangi eftir forgangsflokki og forritið mun birta fyrstu þrjá forgangsflokkana sem eru birtir í lýsigögnunum á verkefnasíðu. Afgangurinn af yfirfylltum lýsigögnum verða birt á síðu með aukaupplýsingum. Eftirfarandi tafla sýnir dæmi um fimm forgangsflokka.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Forgangsflokkur</th>
<th>Úthlutuð svæði</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> Forgangur 10</td>
<td><ul>
<li>vara</li>
<li>Magn</li>
<li>Mælieining</li>
</ul></td>
</tr>
<tr class="even">
<td> Forgangur 20</td>
<td><ul>
<li>Staðsetning klasa:</li>
<li>Klasi</li>
</ul></td>
</tr>
<tr class="odd">
<td> Forgangur 30</td>
<td><ul>
<li>Vörulýsing</li>
</ul></td>
</tr>
<tr class="even">
<td> Forgangur 40</td>
<td><ul>
<li>Grunnstilling</li>
<li>Litur</li>
<li>Stærð</li>
<li>Stíll</li>
</ul></td>
</tr>
<tr class="odd">
<td> Forgangur 50</td>
<td><ul>
<li>Staður</li>
<li>Númeraplata</li>
</ul></td>
</tr>
</tbody>
</table>

Til dæmis þegar starfsmaður í vöruhúsi framkvæmir verk á fartæki, ef lýsigögnin sem verða birt í forritinu samanstanda af eftirfarandi svæði:

-   vara
-   Magn
-   Mælieining
-   Vörulýsing
-   Stærð og staðsetning

Á grunni reitaforgangs í vöruhúsaforritinu sem var settur upp í töflunni hér að ofan, verða eftirfarandi 3 línur upplýsinga birtar á verkefnasíðunni:

-   Lína 1: Vara, Magn, Mælieining
-   Lína 2: Vörulýsing
-   Lína 3: Stærð

Eftirstandandi lýsigögn, til dæmis, Staðsetning, verða ekki birt á verkefnasíðunni heldur verða þau birt á upplýsingasíða. Frekari upplýsingar um þetta og dæmi um notandaviðmót má sjá í bloggfærslunni [Announcing Dynamics 365 Supply Chain Management - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).

## <a name="additional-resources"></a>Frekari upplýsingar

[Setja upp og tengja farsímaforrit vöruhúsakerfis](../warehousing/install-configure-warehouse-management-app.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
