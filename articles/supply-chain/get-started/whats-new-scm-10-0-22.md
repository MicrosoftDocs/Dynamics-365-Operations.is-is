---
title: Forútgáfa af Dynamics 365 Supply Chain Management 10.0.22 (nóvember 2021)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Supply Chain Management 10.0.22.
author: kamaybac
ms.date: 08/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 6fc4b9d0a0f5319c8a75e7d687ee82ea81497844
ms.sourcegitcommit: a21166da59675e37890786ebf7e0f198507f7c9b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/03/2021
ms.locfileid: "7471861"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10022-november-2021"></a>Forútgáfa af Dynamics 365 Supply Chain Management 10.0.22 (nóvember 2021)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Í þessu efnisatriði er að finna eiginleika sem eru annaðhvort nýir eða breyttir í Microsoft Dynamics 365 Supply Chain Management forútgáfu af útgáfu 10.0.22. Þessi útgáfa er með byggingarnúmer 10.0.995 og er fáanlegt á eftirfarandi hátt:

- **Forskoðun útgáfu:** september 2021
- **Almennt framboð útgáfu (sjálfvirk uppfærsla):** Október 2021
- **Almennt framboð útgáfu (sjálfvirk uppfærsla):** Nóvember 2021

## <a name="features-included-in-this-release"></a>Eiginleikar innifaldir í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikana sem eru í þessari útgáfu. Í dálknum *Eiginleikar* eru tenglar í [útgáfuáætlunina](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) þar sem hægt er að skoða opinberar útgáfudagsetningar hvers eiginleika. Í dálknum *Frekari upplýsingar* eru frekari upplýsingar og/eða tenglar á tengd fylgiskjöl. Til að ákvarða hvernig eigi að virkja eiginleikann, sjá dálkinn *Virkjað af*. Nánari upplýsingar um notkun stjórnunar eiginleika er að finna í [Eiginleikastjórnunaryfirlit](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Við gætum uppfært þetta efnisatriði til að hafa með eiginleika sem voru hafðir í smíðinni eftir að þetta efnisatriði var gefið út upphaflega.

| Eiginleikasvæði | Eiginleiki | Meiri upplýsingar | Virkjað af   |
|---|---|---|---|
| Áætlun | [Stuðningur við fínstillingu skipulagningar fyrir úthlutun tilfanga samkvæmt getu](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-capability-based-resource-allocation) | [Röðun með ótakmarkaða getu](../master-planning/planning-optimization/infinite-capacity-planning.md) | Eiginleikastjórnun (*Ótakmörkuð afkastaáætlun fyrir fínstillingu skipulagningar*) |

## <a name="feature-enhancements-included-in-this-release"></a>Eiginleikaviðbætur í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikaviðbætur sem eru í þessari útgáfu. Hver þessara endurbóta býður upp á stigvaxandi viðbót á fyrirliggjandi eiginleika. Þær eru aðeins viðbætur og eru því ekki skráðar í [útgáfuáætluninni](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). En til að tryggja að þessar viðbætur stangist ekki á við núverandi sérstillingar eða kjörstillingar er sjálfgefið slökkt á þeim öllum (nema annað sé tekið fram). Ef nota á einhvern þessara eiginleika þarf að virkja þá sérstaklega í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Eiginleikasvæði | Eiginleikaheiti í eiginleikastjórnun | Meiri upplýsingar |
|---|---|---|
| Kostnaðarstýring | Búa til tengda afsláttarmiða fyrir endurmat á námundun staðalkostnaðar | <p>Þegar birgðafjárhagsbókun (svo sem sölupöntunarreikningur eða birgðafærsla) er gerð veldur þessi eiginleiki því að kerfið býr til sérstakt fylgiskjal fyrir alla tengda hefðbundna endurmatsreikninga vegna rúnnunar kostnaðar og tengir hann við fylgiskjal fjárhagsbókunar sem tengt fylgiskjal.</p><p>Án þessa eiginleika skráir kerfið hefðbundið endurmat á rúnnun staðalkostnaðar á sömu fylgiskjalsbókun. Sú hegðun getur stundum valdið ósamræmi í upplýsingum um dagsetningar, vegna þess að endurmatið notar lotu- eða kerfisdagsetninguna, en fjárhagsfærslur nota bókunardagsetninguna.</p> |
| Dreifð blönduð grannfræði | *(Engin eiginleikastjórnun er nauðsynleg.)* | <p>Þessi útgáfa eykur við farmáætlunargetu fyrir útleið í vinnuálagi vöruhúsakerfis fyrir einingakvarða skýja og jaðra.</p><p>Frekari upplýsingar eru í [Vinnuálag vöruhúsakerfis fyrir einingakvarða skýja og jaðra](../cloud-edge/cloud-edge-workload-warehousing.md).</p> |
| Umsjón hönnunarbreytinga | Afbrigði útbúið fyrir hönnunarafurðir | <p>Þessi eiginleiki gerir þér kleift að búa til ýmis afbrigði fyrir hönnunarafurð út frá lit, stærð, stíl eða skilgreiningarvíddum.</p><p>Frekari upplýsingar er að finna í [Búa til afbrigði fyrir hönnunarafurðir](../engineering-change-management/engineering-variants.md).</p> |
| Birgða- og vöruhúsakerfi | Samþætting birgðasýnileika með mótbókun frátekningar | <p>Aðeins er hægt að virkja þennan eiginleika eftir að eiginleikinn *Samþætting sýnileika birgða* er virkjaður. Þetta býður upp á virkni til að vega upp á móti frátekningum sem eru gerðar á birgðasýnileika.</p><p>Frekari upplýsingar er að finna í [Frátekningar birgðasýnileika](../inventory/inventory-visibility-reservations.md).</p> |
| Sala og markaðsstarf | Takmarka fjölda sölupantana sem hægt er að velja fyrir bókun | <p>Þessi eiginleiki er sjálfkrafa virkjaður. Þetta bætir **Hámarksfjöldi sölupantana fyrir bókun** reit við síðuna **Færibreytur viðskiptakrafna**. Þessi reitur gerir þér kleift að skilgreina hámarksfjölda sölupantana sem hægt er að velja þegar staðfestingar, tiltektarlistar, fylgiseðlar og reikningar á listasíðu sölupantana eru bókuð. Sjálfgildið er *100*.</p><p>Þessi eiginleiki stuðlar að bættum afköstum á listasíðu sölupantana þegar umtalsverður fjöldi sölupantana er valinn. Það hefur engin áhrif á fjölda sölupantana sem hægt er að afgreiða með reglubundnu verkefni.</p> |

## <a name="new-and-updated-documentation-resources"></a>Tilföng fyrir ný og uppfærð skjöl

Nýlega hefur eftirfarandi hjálparatriðum verið bætt við eða þau uppfærð. Þessi efnisatriði eru ekki endilega tengd við nýja eiginleika sem var bætt við fyrir þessa útgáfu, eins og kemur fram í fyrri hluta. Þær gætu hins vegar hjálpað þér að fá meira út úr þeim eiginleikum sem eru til staðar.

| Eiginleikasvæði | Nýtt eða uppfært efni |
|---|---|
| Umsjón hönnunarbreytinga | [Yfirlit yfir umsjón hönnunarbreytinga](../engineering-change-management/product-engineering-overview.md) sýnir nú alla tengda, valfrjálsa eiginleika sem eru í boði í eiginleikastjórnun |
| Áætlanagerð | [Uppsetning eftirspurnarspár](../master-planning/demand-forecasting-setup.md) |
| Áætlanagerð | [Nettóþörf og þarfarakning með fínstillingu áætlanagerðar](../master-planning/planning-optimization/net-requirements.md) |
| Vöruhúsakerfi | [Losa í vöruhús](../warehousing/release-to-warehouse-process.md) gefur ítarlegt yfirlit yfir losun í vöruhús |

## <a name="additional-resources"></a>Frekari upplýsingar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Verkvangsuppfærslur fyrir forrit Finance and Operations

Microsoft Dynamics 365 Supply Chain Management 10.0.22 inniheldur verkvangsuppfærslur. Frekari upplýsingar má finna í [Verkvangsuppfærslur fyrir útgáfu 10.0.22 í Finance and Operations-forritum (nóvember 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-22.md). <!-- KFM: Confirm link -->

### <a name="bug-fixes"></a>Villuleiðréttingar

Til að fá upplýsingar um villuleiðréttingarnar sem fylgja sérhverri uppfærslu sem er hluti af 10.0.22, skráðu þig inn á Lifecycle Services (LCS) og skoðaðu [KB grein](https://fix.lcs.dynamics.com/Issue/Details?bugId=615299).

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
