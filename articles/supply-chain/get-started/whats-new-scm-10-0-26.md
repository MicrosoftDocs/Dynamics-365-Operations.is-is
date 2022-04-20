---
title: Forskoðun Dynamics 365 Supply Chain Management 10.0.26 (maí 2022)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Supply Chain Management 10.0.26.
author: kamaybac
ms.date: 03/01/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 996988b1a4d59ae9ad7b4031e492824c0a6abc95
ms.sourcegitcommit: d475dea4cf13eae2f0ce517542c5173bb9d52c1c
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 04/05/2022
ms.locfileid: "8547874"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10026-may-2022"></a>Forskoðun Dynamics 365 Supply Chain Management 10.0.26 (maí 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Þetta efni sýnir eiginleika sem eru annað hvort nýir eða breyttir í Microsoft Dynamics 365 Supply Chain Management forskoðunarútgáfa 10.0.26. Þessi útgáfa er með byggingarnúmer 10.0.1192 og er fáanlegt á eftirfarandi hátt:

- **Forskoðun á útgáfu:** mars 2022
- **Almennt framboð losunar (sjálfvirk uppfærsla):** Apríl 2022
- **Almennt framboð losunar (sjálfvirk uppfærsla):** Maí 2022

## <a name="features-included-in-this-release"></a>Eiginleikar innifaldir í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikana sem eru í þessari útgáfu. Við gætum uppfært þetta efnisatriði til að hafa með eiginleika sem voru hafðir í smíðinni eftir að þetta efnisatriði var gefið út upphaflega.

| Eiginleikasvæði | Eiginleiki | Meiri upplýsingar | Virkjað af   |
|---|---|---|---|
| Birgða- og vörustjórnun | [Fyrirspurn um birgðasýnileika til að styðja við háþróaða vöruhússtjórnunarhluti](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/inventory-visibility-support-advanced-warehouse-management) | [Stuðningur við birgðasýnileika fyrir WHS hluti](../inventory/inventory-visibility-whs-support.md) | Eiginleikastjórnun:<br>*Virkja vörur vöruhúss í birgðasýnileika* |
| Birgða- og vörustjórnun | [Hægt að lofa fyrir birgðasýnileikaviðbótina](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/available-to-promise-inventory-visibility-add-in) | [Birgðasýnileiki fyrirliggjandi breytingaráætlanir og hægt að lofa](../inventory/inventory-visibility-available-to-promise.md) | Virkt með þjónustustillingu |
| Framleiðsla | [Fáðu þyngdarhluti fyrir framkvæmdarviðmót framleiðslugólfs](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/catch-weight-items-production-floor-execution-interface) | [Hvernig starfsfólk notar viðmót fyrir framkvæmd á framleiðslugólfi](../production-control/production-floor-execution-use.md) | Eiginleikastjórnun:<br>*(Forskoðun) Skýrsla um vörur með framleiðsluþyngd úr keyrsluviðmóti framleiðslugólfs* |
| Framleiðsla | Flipinn „Verkin mín“ í keyrsluviðmóti framleiðslugólfs <!-- KFM: Add link to release plan when available --> | [Hvernig starfsfólk notar viðmót fyrir framkvæmd á framleiðslugólfi](../production-control/production-floor-execution-use.md) | Eiginleikastjórnun:<br>*Flipinn „Verkin mín“ í keyrsluviðmóti framleiðslugólfs* |

## <a name="feature-enhancements-included-in-this-release"></a>Eiginleikaviðbætur í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikaviðbætur sem eru í þessari útgáfu. Hver þessara endurbóta býður upp á stigvaxandi viðbót á fyrirliggjandi eiginleika. Þær eru aðeins viðbætur og eru því ekki skráðar í [útgáfuáætluninni](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). En til að tryggja að þessar viðbætur stangist ekki á við núverandi sérstillingar eða kjörstillingar er sjálfgefið slökkt á þeim öllum (nema annað sé tekið fram).

Ef þú vilt kveikja eða slökkva á einhverjum af þessum eiginleikum verður þú að gera það í [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Eining | Eiginleikaheiti í eiginleikastjórnun | Meiri upplýsingar |
|---|---|---|
| Innkaup og aðföng | Bóka skráð magn afurða í birgðum og það sem eftir er af afurðum sem ekki eru í birgðum fyrir kvittanir og reikninga lánardrottna | Þessi eiginleiki breytir því hvernig magn af vörum sem ekki eru á lager (eins og þjónustu) er bókað þegar unnið er með reikninga lánardrottins og sendingar á heimleið gegn innkaupapöntunum. Eiginleikinn breytir hegðun *Skráð magn og þjónusta* magnvalkostur til að bóka kvittanir og reikninga lánardrottins með því að breyta því til að passa við hegðun *Skráð magn og vörur sem ekki eru á lager* valmöguleiki sem þegar er gefinn þegar magn er bókað fyrir sölu fylgiseðla.<br><br>Þegar þú bókar vörukvittun eða reikning lánardrottins með því að nota *Skráð magn og þjónusta* magnvalkostur, kerfið bókar skráð magn af vörum á lager og bókar afganginn af óbirgðum vörum (þar á meðal bæði þjónusta og ekki þjónusta). Án þessa eiginleika birtir kerfið samt skráð magn af vörum sem eru á lager (þar á meðal þjónusta sem er stillt sem birgðavara) en birtir alltaf allt pantað magn af þjónustuvörum sem ekki eru á lager (og hunsar vörur sem ekki eru á lager sem eru ekki af gerðinni *Þjónusta*). |
| Innkaup og aðföng | Samstilla rakningarvíddir í sölu- og innkaupapöntunarlínum innan samstæðu | Þessi eiginleiki gerir þér kleift að stjórna því hvort rað- og rununúmerarakningarvíddir séu samstilltar á milli fyrirtækjasölu- og innkaupapöntunarlína. Það bætir nýjum stillingum við bæði **Innkaupapöntunarreglur** og **Sölupöntunarstefnur** flipa á **Millifyrirtæki** uppsetningarsíða fyrir viðskiptavini og söluaðila. Það uppfærir einnig nöfn nokkurra tengdra nálægra stillinga til skýrleika.<br><br>Ef þú ert að nota háþróaða vöruhúsastjórnun (WMS), þá skaltu hafa í huga að þessi eiginleiki mun aðeins samstilla lotu- og raðnúmer þegar þessar víddir eru fyrir ofan staðsetningu í stigveldi áfangastaðarpöntunar. |
| Vöruupplýsingastjórnun | Hreinsa gildi afurðareiginda | Þessi eiginleiki bætir við reglubundnu verkefni sem kallast **Hreinsaðu upp gildi vörueiginleika**, sem hreinsar upp vörueiginleikagildisskrár sem eru ekki lengur tengdar neinni vöru í gegnum vöruflokk. |
| Birgða- og vöruhúsakerfi | (Rússland) Koma í veg fyrir ósamræmi þegar GTD er gefið út fyrir innkaupapantanir sem innihalda vörur úr vöruhúsakerfi | Þessi eiginleiki er aðeins fyrir rússneska staðfærslu. Það kemur í veg fyrir misræmi sem verður við útgáfu rússneskra tollskýrslunúmera (GTD) fyrir innkaupapantanir sem innihalda vörur sem eru virkjaðar fyrir háþróaða vörugeymsla (WMS). GTD-útgáfuferlið breytir sumum birgðavíddargildum á tengdum birgðafærslum fyrir reikninga sem eru innifalin í sérsniðnu færslubókinni, sem leiðir til misræmis á milli verkskrár fyrir innkaupapöntun og birgðafærslur fyrir innkaupin. Þegar þessi eiginleiki er virkur myndar GTD-útgáfuferlið aðlögunarvinnu sem útilokar slíkt misræmi. |
| Vöruhúsakerfi | Bættur þáttari fyrir GS1-strikamerki | Þessi eiginleiki bætir við endurbættri flokkun fyrir GS1 tákngögn. Nýi þáttarinn útfærir GS1 General Specification reikniritið til að flokka GS1 tákn og veitir sterkari gagnastaðfestingu. Fyrir frekari upplýsingar, sjá [GS1 strikamerkjaskönnun](../warehousing/gs1-barcodes.md). |
| Vöruhúsakerfi | Nýjar síður á vinnubekknum áætlanagerð | Bætir við tveimur nýjum álagsáætlunarvinnubekksíðum: **Vinnubekkur fyrir skipulagningu álags á innleið** og **Áætlunarbekkur á útleið**. |
| Vöruhúsakerfi | Forrit vöruhúsakerfis - autt GTD | Þessi eiginleiki er aðeins fyrir rússneska staðfærslu. Það gerir starfsmönnum sem nota Warehouse Management farsímaforritið kleift að skilja rússnesk tollskýrslunúmer (GTD) eftir auð þegar þörf krefur. Ef GTD rakningarvídd er sett upp til að leyfa auð gildi mun kerfið samþykkja auð gildi fyrir GTD fyrir birgðaaðgerðir að því tilskildu að lagerbirgðir séu tiltækar. |

## <a name="new-and-updated-documentation-resources"></a>Tilföng fyrir ný og uppfærð skjöl

Nýlega hefur eftirfarandi hjálparatriðum verið bætt við eða þau uppfærð. Þessi efni eru ekki endilega tengd nýjum eiginleikum sem bætt var við fyrir þessa útgáfu, eins og skráð er í fyrri köflum. Þær gætu hins vegar hjálpað þér að fá meira út úr þeim eiginleikum sem eru til staðar.

| Eiginleikasvæði | Nýtt eða uppfært efni |
|---|---|
| Kostnaðarstýring | Uppfærðum dæmum og skýringarmyndum var bætt við hvert eftirfarandi efnis:<ul><li>[Um FIFO með merkingu og efnislegt virði](../cost-management/fifo-physical-value-marking.md)</li><li>[LIFO (síðast inn - fyrst út) með efnislegu virði og marki](../cost-management/lifo-physical-value-marking.md)</li><li>[LIFO dagsetning með efnislegt virði og merkingu](../cost-management/lifo-date-physical-value-marking.md)</li><li>[Um keyrslu á meðalkostnaðarverði](../cost-management/running-average-cost-price.md)</li><li>[Vegið meðaltal með efnislegt virði og merkingu](../cost-management/weighted-average-physical-value-marking.md)</li></ul> |
| Innkaup og aðföng | [Misræmi í gögnum innkaupapöntunarlína](../troubleshooting/procurement/purchase-order-line-data-issues.md) |

## <a name="additional-resources"></a>Frekari upplýsingar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Palluppfærslur fyrir Finance and Operations öpp

Microsoft Dynamics 365 Supply Chain Management 10.0.26 inniheldur verkvangsuppfærslur. Til að læra meira, sjá [Palluppfærslur fyrir útgáfu 10.0.26 af Finance and Operations forritum (maí 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-26.md).

### <a name="bug-fixes"></a>Villuleiðréttingar

Til að fá upplýsingar um villuleiðréttingarnar sem fylgja sérhverri uppfærslu sem er hluti af 10.0.26, skráðu þig inn á Lifecycle Services (LCS) og skoðaðu [KB grein](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 og rekstrarský: 2022 útgáfubylgja 1 áætlun

Ertu að velta fyrir þér væntanlegum og nýlega útgefnum möguleikum í einhverjum af viðskiptaforritum eða verkvangi okkar?

Kíktu á [Dynamics 365 og rekstrarský: 2022 útgáfubylgja 1 áætlun](/dynamics365-release-plan/2022wave1/). Við höfum tekið saman öll smáatriðin í eitt skjal sem hægt er að nota við áætlanagerð.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjarlægðir og úreltir eiginleikar Supply Chain Management

Efnið [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) lýsir eiginleikum sem hafa verið eða á að fjarlægja eða úrelda fyrir Supply Chain Management.

- *Fjarlægður* eiginleiki er ekki lengur tiltækur í vörunni.
- *Úreltur* eiginleiki er ekki í virkri þróun og getur verið fjarlægður úr uppfærslum í framtíðinni.

Áður en einhver eiginleiki er fjarlægður úr vörunni verður tilkynning um afskriftir tilkynnt í efninu [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 mánuðum fyrir fjarlægingu.

Til að brjóta breytingar sem hafa aðeins áhrif á samantektartíma, en eru tvöfaldar samhæfðir við sandkassa og framleiðsluumhverfi, verður afskriftartíminn innan við 12 mánuði. Venjulega eru þetta hagnýtar uppfærslur sem þarf að gera við þýðandann.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
