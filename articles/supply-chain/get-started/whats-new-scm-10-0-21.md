---
title: Forútgáfa af Dynamics 365 Supply Chain Management 10.0.21 (október 2021)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Dynamics 365 Supply Chain Management 10.0.21.
author: kamaybac
ms.date: 08/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 42d296cb0402b5e96f23d628f08a28fb35683d5f
ms.sourcegitcommit: 5a44eb4f555bf5ee0b1293f0ecdc37ee8b53aa24
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/17/2021
ms.locfileid: "7391209"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10021-october-2021"></a>Forútgáfa af Dynamics 365 Supply Chain Management 10.0.21 (október 2021)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Í þessu efnisatriði er að finna eiginleika sem eru annaðhvort nýir eða breyttir í Microsoft Dynamics 365 Supply Chain Management forútgáfu af útgáfu 10.0.21. Þessi útgáfa er með byggingarnúmer 10.0.960 og er fáanlegt á eftirfarandi hátt:

- **Forskoðun á útgáfu:** ágúst 2021
- **Almennt framboð útgáfu (sjálfvirk uppfærsla):** September 2021
- **Almennt framboð útgáfu (sjálfvirk uppfærsla):** Október 2021

## <a name="known-deployment-issue"></a>Þekkt vandamál við innleiðingu

Við uppsetningu útgáfu 10.0.21 á IaaS gætir þú fengið eftirfarandi viðvörun vegna uppsetningar:

**Viðvaranakóði:** 95017

**Viðvörunarboð:** Ekki tókst að keyra forskrift \[SetupDiagnostics\] á móti sýndarvél

Uppsetningin mun virka þrátt fyrir viðvörunina. En eftirfarandi þekkt vandamál geta hinsvegar komið upp í Lifecycle Services (LCS):

- Á síðunni **Eftirlit með umhverfi** mun tengillinn **Skoða ítarlegar upplýsingar um útgáfu** ekki birtast þannig að þú getur ekki séð tilteknar útgáfur af uppsettum einingum í umhverfinu þínu. Án þessara gagna gætu næstu bráðabætur mislukkast vegna þess að ferlið sem setur á bráðabæturnar notar þessi gögn til að staðfesta að skilyrði einingaútgáfunnar séu uppfyllt. Þar sem ekki er hægt að nota PEAP/forútgáfusmíð í framleiðslu eða nota bráðabætur, ættu áhrifin að vera minniháttar.
- Fliparnir **Afkastavísar** og **Yfirlitsgreining** á síðunni **Eftirlit með umhverfi** undir SQL-innsýn munu ekki sýna nein gögn. Allir aðrir eiginleikar **eftirlits með umhverfi** munu virka sem skyldi.
- Ekki verður hægt að fara á síðuna **Full kerfisgreining**. Tilheyrandi gögn um stöðu innheimtukeyrslna að næturlagi og vandamál sem reglur hennar finna munu ekki heldur koma fram.

## <a name="features-included-in-this-release"></a>Eiginleikar innifaldir í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikana sem eru í þessari útgáfu. Í dálknum *Eiginleikar* eru tenglar í [útgáfuáætlunina](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) þar sem hægt er að skoða opinberar útgáfudagsetningar hvers eiginleika. Í dálknum *Frekari upplýsingar* eru frekari upplýsingar og/eða tenglar á tengd fylgiskjöl.

Flestir þessara eiginleika verða að vera virkir með [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) áður en þú getur notað þá. Sumir eiginleikanna sem eru taldir upp eru enn í forútgáfu, á meðan aðrir kunna að vera þegar almennt aðgengilegir.

| Eiginleikasvæði | Eiginleiki | Meiri upplýsingar |
|---|---|---|
| Birgða-&nbsp;og&nbsp;vörustjórnun | [Innbót fjárhags altæks birgðabókhalds fyrir Dynamics 365 Supply Chain Management](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/global-inventory-accounting-add-in-dynamics-365-supply-chain-management) | [Altækt birgðabókhald –heimasíða](../global-inventory-accounting/global-inventory-accounting-home.md) |
| Birgða-&nbsp;og&nbsp;vörustjórnun | [Bóka breytingar á lager með kóðum sem eru tengdir við mótlykla](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/post-on-hand-adjustments-using-configurable-reason-codes-connected-offset-accounts) | [Ástæðukóðar fyrir birgðatalningu](../warehousing/reason-codes-for-counting-journals.md) |
| Birgða-&nbsp;og&nbsp;vörustjórnun | [Regla um útflutning gagna sem sölutilboð vísar í](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sales-quotation-referenced-data-export-policy) | Veldu hvort breytingar á gögnum sem tilboð vísa í munu valda því að þessi tilboð (eða línur) verða höfð með í næsta stigvaxandi útflutningi. Stigvaxandi útflutningur þinn mun ganga hraðar fyrir sig ef þú velur að setja ekki inn slík tilboð eða línur.<br><br>Þessi eiginleiki bætir stillingu sem heitir **Sleppa gögnum sem sölutilboð vísar í við breytingarrakningu** við síðuna **Færibreytur viðskiptakrafna**. |
| Birgða-&nbsp;og&nbsp;vörustjórnun | [Skanna strikamerki í vöruhúsinu með GS1-sniðsstöðlum](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) | [GS1-strikamerki og QR-kóðar](../warehousing/gs1-barcodes.md) |
| Birgða-&nbsp;og&nbsp;vörustjórnun | [Mjúk frátekning fyrir innbót birgðasýnileika](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/soft-reservation-inventory-visibility-add-in) | [Frátekningar sýnilegra birgða](../inventory/inventory-visibility-reservations.md) |
| Birgða-&nbsp;og&nbsp;vörustjórnun | [Betrumbætur á frádrætti og framleiðsluþyngd fyrir stjórnun eftirágreidds afsláttar](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/deduction-catch-weight-enhancements-rebate-management) | [Stjórna frádráttum með frádráttarvinnusvæðinu](../rebate-management/deduction-workbench.md )<br><br>[Meðhöndla, yfirfara og bóka eftirágreiddan afslátt](../rebate-management/process-review-post.md)<br><br>[Tilboð fyrir stjórnun eftirágreidds afsláttar](../rebate-management/rebate-management-deals.md) |
| Birgða-&nbsp;og&nbsp;vörustjórnun | [Leiðbeiningar fyrir skref vöruhúsaforrits](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | [Sérsníða þrepatitla og leiðbeiningar fyrir farsímaforrit Warehouse Management](../warehousing/mobile-app-titles-instructions.md) |
| Birgða-&nbsp;og&nbsp;vörustjórnun | [Uppfærslur á vinnuhléi og rakningu fyrir heildarkostnað](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/work-breaks-tracking-updates-landed-cost) | [Uppfæra rakningu fyrir frágang](../landed-cost/update-tracking-putaway.md )<br><br>[Vinnsla á vörum í flutningi](../landed-cost/in-transit-processing.md) |
| Áætlanagerð | [Neikvæðir dagar fyrir fínstillingu skipulagningar](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/negative-days-support-planning-optimization) | [Vikmörk tafar (neikvæður dagafjöldi)](../master-planning/planning-optimization/delay-tolerance.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Eiginleikaviðbætur í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikaviðbætur í þessari útgáfu. Hver þeirra býður upp á stigvaxandi viðbót á fyrirliggjandi eiginleika. Þær eru aðeins viðbætur og eru því ekki skráðar í [útgáfuáætluninni](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). En til að tryggja að þessar viðbætur stangist ekki á við núverandi sérstillingar eða kjörstillingar er sjálfgefið slökkt á þeim öllum (nema annað sé tekið fram). Ef nota á einhvern þessara eiginleika þarf að virkja þá sérstaklega í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Eiginleikasvæði | Eiginleika&nbsp;heiti&nbsp;í eiginleika&nbsp;stjórnun | Meiri upplýsingar |
|---|---|---|
| Kostnaðarstýring | Ítarlegar upplýsingar um ferli birgðalokunar | Þessi forskoðunareiginleiki gerir þér kleift að skoða ferli birgðalokunar á ítarlegan hátt. |
| Innkaup og aðföng | Koma í veg fyrir ofnotkun almennra frátekta fjárhagsáætlunar þegar margar innkaupabeiðnir eru í verkflæði | Þessi forútgáfa af eiginleikanum bætir villuleit þegar notendur senda inn og samþykkja innkaupabeiðnir sem eru umfram stöðu almennrar frátektar fjárhagsáætlunarlínu. Þetta hjálpar til við að koma í veg fyrir ofnotkun almennra frátekta fjárhagsáætlunar þegar margar innkaupabeiðnir eru í verkflæði. |
| Framleiðslustýring | Sýna öll raðnúmer, rununúmer og númeraplötunúmer í keyrsluviðmóti framleiðslugólfsins | Þessi eiginleiki býður upp á bætta upplifun til að skoða lista yfir raðnúmer, runu og númeraplötunúmer í keyrsluviðmóti framleiðslugólfsins. Skjárinn breytist úr spjaldyfirliti með takmörkuðum fjölda stafa í listayfirlit sem hefur nægilegt pláss til að sýna öll gildin. Listinn gefur einnig möguleika á að leita að tilteknum tölum. |
| Sala og markaðsstarf | Takmarka fjölda sölupantana sem hægt er að velja fyrir bókun | Þessi eiginleiki gerir þér kleift að skilgreina hámarksfjölda sölupantana sem hægt er að velja þegar staðfestingar, tiltektarlistar, fylgiseðlar og reikningar á listasíðu sölupantana eru bókuð. Kveikt er á því sjálfkrafa. Eiginleikinn bætir stillingu sem kallast **Hámarksfjöldi sölupantana fyrir bókun** við síðuna **Færibreytur viðskiptakrafna**. Nýja stillingin er sjálfgefið stillt á gildið *100*. Eiginleikinn stuðlar að bættum afköstum á listasíðu sölupantana þegar umtalsverður fjöldi sölupantana er valinn. Það hefur engin áhrif á fjölda sölupantana sem hægt er að afgreiða með reglubundnu verkefni. |
| Vöruhúsakerfi | Aftengja frágangsvinnu frá ASN (tilkynningum um sendingu) | Þessi eiginleiki er áskilinn til að senda og taka við tilkynningum um sendingu þegar þú keyrir vinnuálag vöruhúsakerfis á kvörðunareiningu (sem hluta af blandaðri grannfræðilegri dreifingu). Hann bætir við nýrri töflu gagnagrunns sem geymir upplýsingar um frágangsvinnu. Áður voru þessar upplýsingar geymdar í töflum sem einnig voru notaðar fyrir ASN. |
| Vöruhúsakerfi | Setja blandaðar einingar í hólf | Leyfir kerfinu að raða atriðum í staðsetningar sem innihalda blandaðar einingar (eins og bæði kassa og box). Fyrir hverja línu hólfasniðmátsins gerir þessi eiginleiki þér kleift að velja hvort línan ætti að raða atriðum í staðsetningar með blönduðum einingum eða samskonar einingum. |
| Vöruhúsakerfi | Notaðu hraðvirkara API fyrir lokun/enduropnun gáma í pökkunarstöð | Þegar þessi eiginleiki er virkjaður eru búnar til birgðafærslur sem tengjast gámum með léttvægu ferli sem eykur afköst lokunar eða opnunar gáma við úrvinnslu handvirkra pökkunarstöðva. |

## <a name="new-and-updated-documentation-resources"></a>Tilföng fyrir ný og uppfærð skjöl

Nýlega hefur eftirfarandi hjálparatriðum verið bætt við eða þau uppfærð. Þær eru ekki endilega tengdar við nýja eiginleika sem bætt er við fyrir þessa útgáfu, eins og kemur fram í fyrri hluta, en þær geta hjálpað notendum að fá meira út úr fyrirliggjandi eiginleikum.

| Eiginleikasvæði | Nýtt eða uppfært efni |
|---|---|
| Áætlanagerð | [Birgðaspár](../master-planning/inventory-forecast.md) |
| Áætlanagerð | [Færibreytur ekki notaðar af fínstillingu skipulagningar](../master-planning/planning-optimization/not-used-parameters.md) |
| Áætlanagerð | [Áfyllingaraðferðir og magnbreyting](../master-planning/planning-optimization/replenishment-methods-quantity-modification.md) |
| Áætlanagerð | [Röðun með ótakmarkaða getu](../master-planning/planning-optimization/infinite-capacity-planning.md) |
| Áætlanagerð | [Skoða áætlunarferil og skipulagsannála](../master-planning/planning-optimization/plan-history-logs.md) |
| Vöruhúsakerfi | [Pökkunarstefnur gáms](../warehousing/container-packing-strategy-overview.md) |
| Vöruhúsakerfi | [Dæmi um reglulega talningu](../warehousing/cycle-counting-scenarios.md) |
| Vöruhúsakerfi | [Flytja inn ASN á innleið í gegnum V2 gagnaeininguna](../warehousing/import-asn-v2-data-entity.md) |
| Vöruhúsakerfi | [Umframtiltekt fyrir sölupantanir og flutningspantanir](../warehousing/over-picking-for-sales-and-transfer-orders.md) |
| Vöruhúsakerfi | [Áætla prentun bylgjumerkis í bylgju](../warehousing/configure-task-based-wave-label-printing.md) |
| Vöruhúsakerfi | [Nýjungar eða breytingar í farsímaforriti Warehouse Management](../warehousing/whats-new-wma.md) |

## <a name="additional-resources"></a>Frekari upplýsingar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Verkvangsuppfærslur fyrir forrit Finance and Operations

Microsoft Dynamics 365 Supply Chain Management 10.0.21 inniheldur verkvangsuppfærslur. Frekari upplýsingar má finna í [Verkvangsuppfærslur fyrir útgáfu 10.0.21 á forritum Finance and Operations (október 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21.md).

### <a name="bug-fixes"></a>Villuleiðréttingar

Til að fá upplýsingar um villuleiðréttingarnar sem fylgja sérhverri uppfærslu sem er hluti af 10.0.21, skráðu þig inn á Lifecycle Services (LCS) og skoðaðu [KB grein](https://fix.lcs.dynamics.com/Issue/Details?bugId=605166&dbType=3&qc=4b9449bf0d947113983bd0697140bf4d8727bfafd5566aa682cb38db343374de).

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365 og rekstrarský: 2021 útgáfubylgja 2 áætlun

Ertu að velta fyrir þér væntanlegum og nýlega útgefnum möguleikum í einhverjum af viðskiptaforritum eða verkvangi okkar?

Kíktu á [Dynamics 365 og rekstrarský: 2021 útgáfubylgja 2 áætlun](/dynamics365-release-plan/2021wave2/). Við höfum tekið saman öll smáatriðin í eitt skjal sem hægt er að nota við áætlanagerð.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjarlægðir og úreltir eiginleikar Supply Chain Management

Efnið [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) lýsir eiginleikum sem hafa verið eða á að fjarlægja eða úrelda fyrir Supply Chain Management.

- *Fjarlægður* eiginleiki er ekki lengur tiltækur í vörunni.
- *Úreltur* eiginleiki er ekki í virkri þróun og getur verið fjarlægður úr uppfærslum í framtíðinni.

Áður en einhver eiginleiki er fjarlægður úr vörunni verður tilkynning um afskriftir tilkynnt í efninu [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 mánuðum fyrir fjarlægingu.

Til að brjóta breytingar sem hafa aðeins áhrif á samantektartíma, en eru tvöfaldar samhæfðir við sandkassa og framleiðsluumhverfi, verður afskriftartíminn innan við 12 mánuði. Venjulega eru þetta hagnýtar uppfærslur sem þarf að gera við þýðandann.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
