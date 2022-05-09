---
title: Forskoðun Dynamics 365 Supply Chain Management 10.0.27 (júlí 2022)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Supply Chain Management 10.0.27.
author: kamaybac
ms.date: 04/22/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: e8ec20c361f76a6012a7c8e1f03296007f5a05aa
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 04/27/2022
ms.locfileid: "8648172"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10027-july-2022"></a>Forskoðun Dynamics 365 Supply Chain Management 10.0.27 (júlí 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Þetta efni sýnir eiginleika sem eru annað hvort nýir eða breyttir í Microsoft Dynamics 365 Supply Chain Management forskoðunarútgáfa 10.0.27. Þessi útgáfa hefur byggingarnúmer 10.0.1227 og er fáanleg samkvæmt eftirfarandi áætlun:

- **Forskoðun útgáfu:** Apríl 2022
- **Almennt framboð losunar (handvirk uppfærsla):** Júní 2022
- **Almennt framboð losunar (sjálfvirk uppfærsla):** Júlí 2022

## <a name="features-included-in-this-release"></a>Eiginleikar innifaldir í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikana sem eru í þessari útgáfu. Við gætum uppfært þetta efni til að innihalda eiginleika sem var bætt við smíðina eftir að þetta efni var upphaflega birt.

| Eiginleikasvæði | Eiginleiki | Meiri upplýsingar | Virkjað af   |
|---|---|---|---|
| Birgða- og vörustjórnun | [Birgðaúthlutun fyrir birgðasýnileikaviðbótina](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/inventory-allocation-inventory-visibility-add-in) | Væntanlegt | Sjálfgefið virkt |
| Framleiðsla | Yfirlitið „Dagurinn minn“ fyrir keyrsluviðmót framleiðslugólfs | [Hvernig starfsmenn nota framkvæmdarviðmót framleiðslugólfs](../production-control/production-floor-execution-use.md) og [Sýna orlofsstöður í framkvæmdarviðmóti framleiðslugólfs](../production-control/production-floor-execution-payroll-stats.md) | Eiginleikastjórnun:<br>*Yfirlitið „Dagurinn minn“ fyrir keyrsluviðmót framleiðslugólfs* |
| Áætlun | [Stuðningur við skipulagningu hagræðingar fyrir undirverktaka](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-subcontracting) | [Stjórnun úthýsingarvinnu í framleiðslu](../production-control/manage-subcontract-work-production.md) | Sjálfgefið virkt |

## <a name="feature-enhancements-included-in-this-release"></a>Eiginleikaviðbætur í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikaviðbætur sem eru í þessari útgáfu. Hver þessara endurbóta býður upp á stigvaxandi viðbót á fyrirliggjandi eiginleika. Þær eru aðeins viðbætur og eru því ekki skráðar í [útgáfuáætluninni](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). En til að tryggja að þessar viðbætur stangist ekki á við núverandi sérstillingar eða kjörstillingar er sjálfgefið slökkt á þeim öllum (nema annað sé tekið fram).

Ef þú vilt kveikja eða slökkva á einhverjum af þessum eiginleikum verður þú að gera það inn [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Eining | Eiginleikaheiti í eiginleikastjórnun | Meiri upplýsingar |
|---|---|---|
| Áætlanagerð | Hugaðu að afhendingartíma birgða þegar áætluð flutningspöntun er stofnuð | Þegar fyrirhuguð millifærslupöntun er búin til veldur þessi eiginleiki að kerfið lítur á birgðaafgreiðslutímann sem er tilgreindur í sjálfgefnum pöntunarstillingum vörunnar þegar það reiknar út móttökudagsetningu fyrirhugaðrar millifærslupöntunar fyrir uppsetningu afhendingardagsstýringar sem afhendingartíma vörunnar.*Enginn* eða *Sala* gerð. Þegar flutningstími er tilgreindur verður gildi hans notað við útreikning á móttökudagsetningu og flutningsdagar eru virtir að vettugi. |
| Innkaup og aðföng | Sjálfgefnar skattaupplýsingar um samning miðlara í reikningslínum lánardrottins | Þessi eiginleiki kynnir rökfræði til að stilla sjálfgefin gildi fyrir **Söluskattur** og **Vörusöluskattur** reiti á reikningslínum miðlarasamnings seljanda. Þessari rökfræði er aðeins beitt þegar gjaldgerðin á samningslínu miðlara er höfuðbók/bókhald. Vöruskattsflokkurinn mun taka sjálfgefið gildi sitt annaðhvort úr innkaupaflokki verðbréfamiðlunar (ef hann er settur upp) eða frá gjaldategundinni. Vöruskattsflokkurinn mun taka sjálfgefið gildi sitt af lánardrottinsreikningi. |
| Innkaup og aðföng | Takmarka fjölda innkaupapöntunarlína á hvert runuverk | Þessi eiginleiki hjálpar þér að hámarka afköst kerfisins þegar staðfestingar og vörukvittanir eru birtar. Það bætir við nýrri stillingu sem heitir **Línur fyrir hvert verkefni** til **Afhending** flipi á **Innkaupa- og innkaupafæribreytur** síðu. Þessi nýja stilling gerir þér kleift að takmarka fjölda innkaupapöntunarlína sem hvert lotuverkefni vinnur. Þess vegna getur það hjálpað til við að koma í veg fyrir að stór lotuverkefni hægi á kerfinu. |
| Vöruupplýsingastjórnun | Fylla út gildi afurðareiginda | Þessi eiginleiki bætir við reglubundnu verkefni sem er nefnt *Fylltu út gildi vörueiginleika*. Þetta nýja reglubundna verk býr til virðisfærslur vörueiginda sem vantar fyrir eiginleika sem eru tengdar vörum í gegnum vöruflokk. |
| Framleiðslustýring | Viðbótarstillingar á keyrsluviðmóti framleiðslugólfs | <p>Þessi eiginleiki bætir eftirfarandi valkostum við **Stilla framkvæmd framleiðslugólfs** síða:</p><ul><li>**Opna upphafsgluggann sjálfkrafa þegar leit er lokið** – Þegar þessi valkostur er virkur, **Byrja starf** svarglugginn opnast sjálfkrafa þegar starfsmenn nota leitarstikuna til að finna starfið.</li><li>**Opna sjálfkrafa skýrsluframvinduglugga þegar leit er lokið** – Þegar þessi valkostur er virkur, **Tilkynna framvindu** svargluggi fyrir starfið opnast sjálfkrafa þegar starfsmenn nota leitarstikuna til að finna starfið.</li><li>**Sjálfgefið eftirstandandi magn í framvindu skýrslugluggans** – Þegar þessi valkostur er virkur, **Tilkynna framvindu** svarglugginn sýnir eftirstandandi magn til að tilkynna um framleiðsluverk.</li></ul><p>Fyrir frekari upplýsingar, sjá [Stilltu framkvæmdarviðmót framleiðslugólfs](../production-control/production-floor-execution-configure.md).</p> |
| Framleiðslustýring | Framleiðsluteymi í keyrsluviðmóti framleiðslugólfs | <p>Þegar mörgum starfsmönnum er úthlutað í sama framleiðslustarfið geta þeir nú tilnefnt einn starfsmann sem flugmann. Þeir starfsmenn sem eftir eru verða sjálfkrafa aðstoðarmenn þess flugmanns. Fyrir liðið sem myndast þarf aðeins flugmaðurinn að skrá starfsstöðu, en tímaskrár eiga við um alla liðsmenn. Þessi eiginleiki styður einnig atburðarás sem er nefnd *aðstoða úrræði*. Í þessari atburðarás getur starfsmaður skráð sig sem aðstoðarmann annars starfsmanns, sem síðan verður flugmaður fyrir nýstofnaða hópinn.</p><p>Fyrir frekari upplýsingar, sjá [Hvernig starfsmenn nota framkvæmdarviðmót framleiðslugólfs](../production-control/production-floor-execution-use.md).</p> |
| Framleiðslustýring | Skýrsla um áætlunarvörur í keyrsluviðmóti framleiðslugólfs | Þessi eiginleiki einfaldar ferlið við að tilkynna um runupantanir fyrir áætlunarvörur í framkvæmdarviðmóti framleiðslugólfs. Þegar runupöntun er stofnuð fyrir vöru sem hefur framleiðslugerðina *Skipulagsliður*, aðeins er hægt að tilkynna sem fullunnið um aukaafurðir og aukaafurðir fyrir þá lotupöntun. Lotapantanir fyrir skipulagsvörur eru venjulega notaðar til að styðja við sundurliðaferli, þar sem hráefnisvara er tekin í sundur í margar aðskildar vörur. Þegar starfsmaður tilkynnir runupöntun fyrir áætlunarvöru sem lokið, **Tilkynna framvindu** svarglugginn mun nú aðeins sýna aukaafurðirnar og aukaafurðirnar. Áður sýndi það líka skipulagsatriðið og þessi hegðun gæti ruglað starfsmenn. |

## <a name="new-and-updated-documentation-resources"></a>Tilföng fyrir ný og uppfærð skjöl

Við höfum nýlega bætt við eða uppfært umtalsvert eftirfarandi hjálparefni. Þessi efni eru ekki endilega tengd nýjum eiginleikum sem bætt var við fyrir þessa útgáfu, eins og skráð er í fyrri köflum. Hins vegar gætu þeir hjálpað þér að fá meira út úr núverandi eiginleikum.

| Eiginleikasvæði | Nýtt eða uppfært efni |
|---|---|
| Kostnaðarstýring | [Vegin meðaldagsetning með innihalda líkamlegt gildi og merkingu](../cost-management/weighted-average-date.md) |
| Dreifð blönduð grannfræði | [Prófaðu kvörðunareiningar í dreifðri blandaðri grannfræði](../cloud-edge/cloud-edge-try-out.md) |
| Tvöföld skrif | [Samstilla eftirspurn við verðlagningarkerfi Supply Chain Management](../../fin-ops-core/dev-itpro/data-entities/dual-write/pricing-engine.md) |
| Vöruhúsakerfi | [Losa í vöruhús](../warehousing/release-to-warehouse-process.md) |

## <a name="additional-resources"></a>Frekari upplýsingar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Palluppfærslur fyrir Finance and Operations öpp

Microsoft Dynamics 365 Supply Chain Management 10.0.27 inniheldur verkvangsuppfærslur. Til að læra meira, sjá [Palluppfærslur fyrir útgáfu 10.0.27 af Finance and Operations forritum (júní 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-27.md).<!-- KFM Confirm link -->

### <a name="bug-fixes"></a>Villuleiðréttingar

Til að fá upplýsingar um villuleiðréttingarnar sem fylgja sérhverri uppfærslu sem er hluti af 10.0.27, skráðu þig inn á Lifecycle Services (LCS) og skoðaðu [KB grein](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).

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
