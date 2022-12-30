---
title: Nýjungar eða breytingar í Dynamics 365 Supply Chain Management 10.0.27 (júlí 2022)
description: Þessi grein lýsir nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Supply Chain Management 10.0.27.
author: kamaybac
ms.date: 04/22/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 3ce3b2f3524dbeb043717ed9ef5429ea0eea4b8a
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427801"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10027-july-2022"></a>Nýjungar eða breytingar í Dynamics 365 Supply Chain Management 10.0.27 (júlí 2022)

[!include [banner](../includes/banner.md)]

Í þessari grein er að finna eiginleika sem eru annaðhvort nýir eða breyttir í Microsoft Dynamics 365 Supply Chain Management útgáfu 10.0.27. Þessi útgáfa er með smíðarnúmer 10.0.1227 og er í boði á eftirfarandi áætlun:

- **Forskoðun útgáfu:** Apríl 2022
- **Almennt framboð losunar (handvirk uppfærsla):** Júní 2022
- **Almennt framboð losunar (sjálfvirk uppfærsla):** Júlí 2022

## <a name="features-included-in-this-release"></a>Eiginleikar innifaldir í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikana sem eru í þessari útgáfu. Við gætum uppfært þessa grein til að hafa með eiginleika sem var bætt við smíðina eftir að þessi grein var upphaflega birt.

| Eiginleikasvæði | Eiginleiki | Meiri upplýsingar | Virkjað af   |
|---|---|---|---|
| Birgða- og vörustjórnun | [Birgðaúthlutun fyrir innbót birgðasýnileika](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/inventory-allocation-inventory-visibility-add-in) | [Inventory Visibility birgðaúthlutun](../inventory/inventory-visibility-allocation.md) | Virkja að sjálfgefnu |
| Framleiðsla | Yfirlitið „Dagurinn minn“ fyrir keyrsluviðmót framleiðslugólfs | [Hvernig starfsfólk notar keyrsluviðmót framleiðslugólfs](../production-control/production-floor-execution-use.md) og [Sýna stöðu frídaga í keyrsluviðmóti framleiðslugólfs](../production-control/production-floor-execution-payroll-stats.md) | Stjórnun eiginleika:<br>*Yfirlitið „Dagurinn minn“ fyrir keyrsluviðmót framleiðslugólfs* |
| Áætlun | [Stuðningur við fínstillingu áætlanagerðar fyrir úthýsingu](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-subcontracting) | [Stjórnun úthýsingarvinnu í framleiðslu](../production-control/manage-subcontract-work-production.md) | Virkja að sjálfgefnu |

## <a name="feature-enhancements-included-in-this-release"></a>Eiginleikaviðbætur í þessari útgáfu

Í eftirfarandi töflu er listi yfir eiginleikaviðbætur sem eru í þessari útgáfu. Hver þessara endurbóta býður upp á stigvaxandi viðbót á fyrirliggjandi eiginleika. Þær eru aðeins viðbætur og eru því ekki skráðar í [útgáfuáætluninni](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). En til að tryggja að þessar viðbætur stangist ekki á við núverandi sérstillingar eða kjörstillingar er sjálfgefið slökkt á þeim öllum (nema annað sé tekið fram).

Ef á að kveikja eða slökkva á einhverjum þessara eiginleika þarf að gera það í [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Eining | Eiginleikaheiti í eiginleikastjórnun | Meiri upplýsingar |
|---|---|---|
| Áætlanagerð | Hugaðu að afhendingartíma birgða þegar áætluð flutningspöntun er stofnuð | Þegar áætluð flutningspöntun er stofnuð veldur þessi eiginleiki því að kerfið tekur tillit til afhendingartíma birgðanna sem tilgreindur er í sjálfgefnum pöntunarstillingum vörunnar þegar móttökudagsetning áætlaðrar flutningspöntunar er reiknuð fyrir uppsetningu á stjórnun afhendingardagsetningar sem *Engin* eða *Afhendingartími sölu*. Þegar afhendingartími flutnings er tilgreindur verður gildi hans notað fyrir útreikning móttökudagsetningar og flutningsdagsetning verður hunsuð. |
| Innkaup og aðföng | Sjálfgefnar skattaupplýsingar um samning miðlara í reikningslínum lánardrottins | Þessi eiginleiki kynnir reglu til að stilla sjálfgefin gildi fyrir reitina **Söluskattur** og **Söluskattur vöru** í reikningslínum lánardrottins í samningi miðlara. Þessi regla er aðeins notuð þegar tegund gjalds í samningslínu miðlara er fjárhagur/fjárhagur. VSK-flokkur vöru mun fá sjálfgefið gildi sitt annað hvort úr innkaupaflokki miðlunar (ef hann er settur upp) eða úr tegund gjalds. VSK-flokkur vöru mun fá sjálfgefið gildi úr lykli lánardrottins. |
| Innkaup og aðföng | Takmarka fjölda innkaupapöntunarlína á hvert runuverk | Þessi eiginleiki hjálpar þér að hámarka afköst kerfisins þegar staðfestingar og innhreyfingarskjöl afurðar eru bókaðar. Hann bætir nýrri stillingu sem heitir **Línur á verk** við flipann **Afhending** á síðunni **Færibreytur innkaupa og aðfanga**. Þessi nýja stilling gerir þér kleift að takmarka fjölda innkaupapöntunarlína sem hvert runuverk vinnur úr. Þar af leiðandi getur hann hjálpað til við að koma í veg fyrir að stór runuverk hægi á kerfinu. |
| Vöruupplýsingastjórnun | Fylla út gildi afurðareiginda | Þessi eiginleiki bætir við reglubundnu verki sem heitir *Fylla út gildi afurðareiginda*. Þetta nýja reglubundna verk býr til færslur afurðareigindagilda sem vantar fyrir eigindir sem tengjast afurðum í gegnum afurðategund. |
| Framleiðslustýring | Viðbótarstillingar á keyrsluviðmóti framleiðslugólfs | <p>Þessi eiginleiki bætir eftirfarandi valkostum við síðuna **Stilla framkvæmd á framleiðslugólfi**:</p><ul><li>**Opna svarglugga upphafs sjálfkrafa þegar leit er lokið** - Þegar þessi valkostur er virkur verður svargluggi **Verkupphaf** sjálfkrafa opnaður þegar starfsmenn nota leitarstikuna til að finna verkið.</li><li>**Opna svarglugga skýrsluframvindu sjálfkrafa þegar leit er lokið** – Þegar þessi valkostur er virkur verður svarglugginn **Skýrsluframvinda** fyrir verkið sjálfkrafa opnaður þegar starfsmenn nota leitarstikuna til að finna verkið.</li><li>**Sjálfgefið eftirstandandi magn í svarglugga skýrsluframvindu** – Þegar þessi valkostur er virkur mun svarglugginn **Skýrsluframvinda** sýna eftirstandandi magn sem á að tilkynna í framleiðsluverki.</li></ul><p>Frekari upplýsingar er að finna í [Skilgreina keyrsluviðmót framleiðslugólfsins](../production-control/production-floor-execution-configure.md).</p> |
| Framleiðslustýring | Framleiðsluteymi í keyrsluviðmóti framleiðslugólfs | <p>Þegar mörgum starfsmönnum er úthlutað á sama framleiðsluverkið geta þeir nú útnefnt einn starfsmenn sem aðalnotanda. Hinir starfsmennirnir verða sjálfkrafa aðstoðarmenn aðalnotandans. Fyrir tilheyrandi teymi þarf aðeins aðalnotandinn að skrá verkstöðuna á meðan tímafærslur eiga við um alla teymismeðlimi. Þessi eiginleiki styður einnig við aðstæður sem kallast *aðstoðarúrræði*. Í þessum aðstæðum getur starfsmaður skráð aðstoðarmann á annan starfsmann sem verður þá aðalnotandinn fyrir nýlega myndaðan hóp.</p><p>Frekari upplýsingar er að finna á [Hvernig starfsfólk notar viðmót fyrir framkvæmd á framleiðslugólfi](../production-control/production-floor-execution-use.md).</p> |
| Framleiðslustýring | Skýrsla um áætlunarvörur í keyrsluviðmóti framleiðslugólfs | Þessi eiginleiki einfaldar ferlið við skýrslugerð runupantana fyrir áætlunarvörur í keyrsluviðmóti framleiðslugólfs. Þegar runupöntun er stofnuð fyrir afurð með framleiðslugerðina *Áætlunarvara* er aðeins hægt að tilkynna sem tilbúið fyrir aukaafurðir og hliðarafurðir fyrir þá runupöntun. Runupantanir fyrir áætlunarvörur eru yfirleitt notaðar til að styðja sundurhlutunarferli þar sem hráefnisafurð er hlutuð niður í margar einkvæmar afurðir. Þegar starfsmaður tilkynnir runupöntun fyrir vöru áætlanagerðar sem lokið mun svarglugginn **Skýrsluframvinda** nú aðeins sýna aukaafurðir og hliðarafurðir. Áður sýndi það einnig vöru á áætlun og þessi hegðun gæti ruglað starfsmenn. |

## <a name="new-and-updated-documentation-resources"></a>Tilföng fyrir ný og uppfærð skjöl

Nýlega hefur eftirfarandi hjálpargreinum verið bætt við eða þau uppfærð. Þessi grein eru ekki endilega tengd við nýja eiginleika sem var bætt við fyrir þessa útgáfu, eins og kemur fram í fyrri hlutum. Þær gætu hins vegar hjálpað þér að fá meira út úr þeim eiginleikum sem eru til staðar.

| Eiginleikasvæði | Nýjar eða uppfærðar greinar |
|---|---|
| Kostnaðarstýring | [Dagsetning vegins meðaltals með efnislegu virði og merkingu](../cost-management/weighted-average-date.md) |
| Dreifð blönduð grannfræði | [Prófaðu kvörðunareiningar í dreifðri blandaðri grannfræði](../cloud-edge/cloud-edge-try-out.md) |
| Tvöföld skrif | [Samstilla eftirspurn við verðlagningarkerfi Supply Chain Management](../../fin-ops-core/dev-itpro/data-entities/dual-write/pricing-engine.md) |
| Vöruhúsakerfi | [Losa í vöruhús](../warehousing/release-to-warehouse-process.md) |

## <a name="additional-resources"></a>Frekari upplýsingar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Verkvangsuppfærslur fyrir fjármála- og rekstrarforrit.

Microsoft Dynamics 365 Supply Chain Management 10.0.27 inniheldur verkvangsuppfærslur. Frekari upplýsingar má finna í [Verkvangsuppfærslur fyrir útgáfu 10.0.27 á fjármála- og rekstrarforritum (október 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-27.md).

### <a name="bug-fixes"></a>Villuleiðréttingar

Til að fá upplýsingar um villuleiðréttingarnar sem fylgja sérhverri uppfærslu sem er hluti af 10.0.27, skráðu þig inn á Lifecycle Services (LCS) og skoðaðu [KB grein](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).

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

