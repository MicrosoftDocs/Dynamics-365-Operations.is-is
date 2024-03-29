---
title: Hvað er nýtt eða breytt í Dynamics 365 Supply Chain Management 10.0.26. (maí 2022)
description: Þessi grein lýsir nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Supply Chain Management 10.0.26.
author: kamaybac
ms.date: 03/01/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: db8799aba8095c8144d878c96590e8d90276726b
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428201"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10026-may-2022"></a>Hvað er nýtt eða breytt í Dynamics 365 Supply Chain Management 10.0.26. (maí 2022)

[!include [banner](../includes/banner.md)]

Í þessari grein er að finna eiginleika sem eru annaðhvort nýir eða breyttir í Microsoft Dynamics 365 Supply Chain Management útgáfu 10.0.26. Þessi útgáfa er með byggingarnúmer 10.0.1192 og er fáanlegt á eftirfarandi hátt:

- **Forskoðun á útgáfu:** mars 2022
- **Almennt framboð losunar (sjálfvirk uppfærsla):** Apríl 2022
- **Almennt framboð losunar (sjálfvirk uppfærsla):** Maí 2022

## <a name="features-included-in-this-release"></a>Eiginleikar innifaldir í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikana sem eru í þessari útgáfu. Við gætum uppfært þessa grein til að hafa með eiginleika sem voru hafðir í smíðinni eftir að þessi grein var gefið út upphaflega.

| Eiginleikasvæði | Eiginleiki | Meiri upplýsingar | Virkjað af   |
|---|---|---|---|
| Birgða- og vörustjórnun | [Lagerfyrirspurnin birgðasýnileika til að styðja við vörur í ítarlegu vöruhúsakerfi](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/inventory-visibility-support-advanced-warehouse-management) | [Stuðningur fyrir Inventory Visibility af vörum í vöruhúsakerfi](../inventory/inventory-visibility-whs-support.md) | Stjórnun eiginleika:<br>*Virkja vörur vöruhúss í birgðasýnileika* |
| Birgða- og vörustjórnun | [Tiltækt til loforðs fyrir innbót birgðasýnileika](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/available-to-promise-inventory-visibility-add-in) | [Breytingaáætlun á lager og ATP-afhendingarspá Inventory Visibility](../inventory/inventory-visibility-available-to-promise.md) | Gert virkt með þjónustustillingu |
| Framleiðsla | [Vörur framleiðsluþyngdar fyrir vinnsluviðmót framleiðslugólfs](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/catch-weight-items-production-floor-execution-interface) | [Hvernig starfsfólk notar viðmót fyrir framkvæmd á framleiðslugólfi](../production-control/production-floor-execution-use.md) | Stjórnun eiginleika:<br>*Skýrsla um vörur með framleiðsluþyngd úr keyrsluviðmóti framleiðslugólfs* |
| Framleiðsla | Flipinn „Verkin mín“ í keyrsluviðmóti framleiðslugólfs | [Hvernig starfsfólk notar viðmót fyrir framkvæmd á framleiðslugólfi](../production-control/production-floor-execution-use.md) | Stjórnun eiginleika:<br>*Flipinn „Verkin mín“ í keyrsluviðmóti framleiðslugólfs* |

## <a name="feature-enhancements-included-in-this-release"></a>Eiginleikaviðbætur í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikaviðbætur sem eru í þessari útgáfu. Hver þessara endurbóta býður upp á stigvaxandi viðbót á fyrirliggjandi eiginleika. Þær eru aðeins viðbætur og eru því ekki skráðar í [útgáfuáætluninni](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). En til að tryggja að þessar viðbætur stangist ekki á við núverandi sérstillingar eða kjörstillingar er sjálfgefið slökkt á þeim öllum (nema annað sé tekið fram).

Ef á að kveikja eða slökkva á einhverjum þessara eiginleika þarf að gera það í [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Eining | Eiginleikaheiti í eiginleikastjórnun | Meiri upplýsingar |
|---|---|---|
| Innkaup og aðföng | Bóka skráð magn afurða í birgðum og það sem eftir er af afurðum sem ekki eru í birgðum fyrir kvittanir og reikninga lánardrottna | Þessi eiginleiki breytir því hvernig magn af vörum sem ekki eru á lager (eins og þjónusta) er bókað þegar unnið er úr lánardrottnareikningum og sendingum á innleið á móti innkaupapöntunum. Þessi eiginleiki breytir hegðun magnvalkostsins *Skráð magn og þjónustur* fyrir bókun innhreyfinga og lánardrottnareikninga með því að breyta honum til að stemma við hegðun valkostsins *Skráð magn og vörur sem ekki eru á lager* sem er þegar gefinn upp þegar magn fyrir fylgiseðla sölu er bókað.<br><br>Þegar þú bókar innhreyfingarskjal afurðar eða lánardrottnareikning með magnvalkostinum *Skráð magn og þjónustur* bókar kerfið skráð magn af vörum á lager og bókar eftirstandandi magn af vörum sem ekki eru á lager (þ.m.t. bæði þjónustur og ekki þjónustur). Án þessa eiginleika bókar kerfið enn skráð magn af vörum á lager (þ.m.t. þjónustur sem skilgreindar eru sem vörur á lager) en bókar alltaf fullt pöntunarmagnið af þjónustuvörum sem ekki eru á lager (og hunsar vörur sem ekki eru á lager sem ekki eru af gerðinni *Þjónusta*). |
| Innkaup og aðföng | Samstilla rakningarvíddir í sölu- og innkaupapöntunarlínum innan samstæðu | Þessi eiginleiki gerir þér kleift að stjórna því hvort rakningarvíddir rað- og rununúmers eru samstilltar í öllum sölu- og innkaupapöntunarlínum innan samstæðu. Hann bætir nýjum stillingum við bæði flipana **Innkaupapöntunarreglur** og **Sölupöntunarreglur** á uppsetningarsíðunni **Innan samstæðu** fyrir viðskiptavini og lánardrottna. Það uppfærir einnig nöfn nokkurra tengdra, nálægra stillinga til að fá skýrleika.<br><br>Ef vöruhúsastjórnunarferlar eru notaðir (WMS) skaltu hafa í huga að þessi eiginleiki mun aðeins samstilla lotu- og raðnúmer þegar stærðirnar eru yfir staðsetningu í frásetningarstigveldi vöruhúsabókunar. |
| Vöruupplýsingastjórnun | Hreinsa gildi afurðareiginda | Þessi eiginleiki bætir við reglubundnu verki sem kallast **Hreinsa gildi afurðareiginda**, sem hreinsar færslur afurðareigindargilda sem tengjast ekki lengur neinni afurð í gegnum afurðategund. |
| Birgða- og vöruhúsakerfi | (Rússland) Koma í veg fyrir ósamræmi þegar GTD er gefið út fyrir innkaupapantanir sem innihalda vörur úr vöruhúsakerfi | Þessi eiginleiki er aðeins ætlaður fyrir rússneska staðfærslu. Það kemur í veg fyrir misræmi sem á sér stað þegar rússnesk tollskýrslunúmer (GTDs) eru gefin út fyrir innflutnings- og innkaupapantanir sem innihalda hluti sem eru virkjaðir fyrir vöruhúsastjórnunarferli (WMS). Útgáfa GTD breytir sumum birgðavíddargildum á tilheyrandi birgðafærslum fyrir reikninga sem er að finna í tollabókinni, sem leiðir til ósamræmis milli vinnufærslna fyrir innkaupapöntunina og birgðafærslna fyrir innkaupin. Þegar þessi eiginleiki er gerður virkur býr GTD-útgáfuferlið til leiðréttingarvinnu sem eyðir slíku ósamræmi. |
| Vöruhúsakerfi | Bættur þáttari fyrir GS1-strikamerki | Þessi eiginleiki bætir við endurbættum þáttara fyrir gögn GS1-tákns. Nýi þáttarinn útfærir GS1 General Specification reikniritið fyrir þáttun GS1 tákna og veitir sterkari gagnaprófun. Frekari upplýsingar er að finna í [Skönnun GS1-strikamerkis](../warehousing/gs1-barcodes.md). |
| Vöruhúsakerfi | Forrit vöruhúsakerfis - autt GTD | Þessi eiginleiki er aðeins ætlaður fyrir rússneska staðfærslu. Það gerir starfsmönnum sem nota farsímaforrit vöruhúsakerfisins kleift að skilja rússnesk tollskýrslunúmer (GTD) eftir auð þegar þess gerist þörf. Ef GTD rakningarvíddin er sett upp til að leyfa tóm gildi, mun kerfið samþykkja tóm gildi fyrir GTD fyrir birgðaaðgerðir, að því tilskildu að birgðir á hendi séu tiltækar. |

## <a name="new-and-updated-documentation-resources"></a>Tilföng fyrir ný og uppfærð skjöl

Nýlega hefur eftirfarandi hjálpargreinum verið bætt við eða þau uppfærð. Þessi grein eru ekki endilega tengd við nýja eiginleika sem var bætt við fyrir þessa útgáfu, eins og kemur fram í fyrri hlutum. Þær gætu hins vegar hjálpað þér að fá meira út úr þeim eiginleikum sem eru til staðar.

| Eiginleikasvæði | Nýjar eða uppfærðar greinar |
|---|---|
| Kostnaðarstýring | Uppfærðum dæmum og skýringarmyndum var bætt við hverja af eftirfarandi greinum:<ul><li>[Um FIFO með merkingu og efnislegt virði](../cost-management/fifo-physical-value-marking.md)</li><li>[LIFO (síðast inn - fyrst út) með efnislegu virði og marki](../cost-management/lifo-physical-value-marking.md)</li><li>[LIFO dagsetning með efnislegt virði og merkingu](../cost-management/lifo-date-physical-value-marking.md)</li><li>[Um keyrslu á meðalkostnaðarverði](../cost-management/running-average-cost-price.md)</li><li>[Vegið meðaltal með efnislegt virði og merkingu](../cost-management/weighted-average-physical-value-marking.md)</li></ul> |

## <a name="additional-resources"></a>Frekari upplýsingar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Verkvangsuppfærslur fyrir fjármála- og rekstrarforrit.

Microsoft Dynamics 365 Supply Chain Management 10.0.26 inniheldur verkvangsuppfærslur. Frekari upplýsingar má finna í [Verkvangsuppfærslur fyrir útgáfu 10.0.26 á fjármála- og rekstrarforritum (október 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-26.md).

### <a name="bug-fixes"></a>Villuleiðréttingar

Til að fá upplýsingar um villuleiðréttingarnar sem fylgja sérhverri uppfærslu sem er hluti af 10.0.26, skráðu þig inn á Lifecycle Services (LCS) og skoðaðu [KB grein](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 og rekstrarský: 2022 útgáfubylgja 1 áætlun

Ertu að velta fyrir þér væntanlegum og nýlega útgefnum möguleikum í einhverjum af viðskiptaforritum eða verkvangi okkar?

Kíktu á [Dynamics 365 og rekstrarský: 2022 útgáfubylgja 1 áætlun](/dynamics365-release-plan/2022wave1/). Við höfum tekið saman öll smáatriðin í eitt skjal sem hægt er að nota við áætlanagerð.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjarlægðir og úreltir eiginleikar Supply Chain Management

Greinin [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) lýsir eiginleikum sem hafa verið eða á að fjarlægja eða úrelda fyrir Supply Chain Management.

- *Fjarlægður* eiginleiki er ekki lengur tiltækur í vörunni.
- *Úreltur* eiginleiki er ekki í virkri þróun og getur verið fjarlægður úr uppfærslum í framtíðinni.

Áður en einhver eiginleiki er fjarlægður úr vörunni verður tilkynning um afskriftir tilkynnt í greininni [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 mánuðum fyrir fjarlægingu.

Til að brjóta breytingar sem hafa aðeins áhrif á samantektartíma, en eru tvöfaldar samhæfðir við sandkassa og framleiðsluumhverfi, verður afskriftartíminn innan við 12 mánuði. Venjulega eru þetta hagnýtar uppfærslur sem þarf að gera við þýðandann.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

