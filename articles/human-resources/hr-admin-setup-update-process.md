---
title: Uppfærsluferli
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1817e072805bafbf0d5a9eb2698ef75abc75ad68
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/07/2020
ms.locfileid: "3031091"
---
# <a name="update-process"></a>Uppfærsluferli

Microsoft Dynamics 365 Human Resources er sannur hugbúnaður sem þjónusta (SaaS) sem veitir stöðugar, snertilausar þjónustuuppfærslur. Þessar uppfærslur innihalda bæði forrits- og vettvangsbreytingar sem oft veita mikilvægar endurbætur á þjónustunni, þ.mt uppfærslur á reglugerðum.

## <a name="update-policy"></a>Uppfæra stefnu

Uppfærslur eru gefnar út með reglubundnum hætti fyrir öll umhverfi. Human Resources er stutt samkvæmt [Microsoft Lifecycle policy](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy) sem býður upp á stöðugar og einfaldar leiðbeiningar fyrir tiltækileika stuðnings við vöru.

## <a name="release-cadence"></a>Losunartaktur

Uppfærslum á Human Resources er beitt sjálfkrafa í öll umhverfi. Human Resources veitir tvenns konar útgáfur:

- **Þjónustuuppfærslur**: Vikulegar uppfærslur sem innihalda villuleiðréttingar og nýja eiginleika. Þjónustuuppfærslur innihalda einnig viðeigandi uppfærslur á palli þegar þær eru gefnar út. Sjá til að fá hugmynd um hvenær uppfærslur á verkvangi eru gefnar út [Tafla 3: Verkvangsútgáfur](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases). Vikulegar uppfærslur koma venjulega út á miðvikudögum. Nánari upplýsingar um vikulegar uppfærslur eru í [Hvað er nýtt eða breytt í Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365/talent/whats-new).

    Allar studdar gagnaver uppfæra vikulega nema annað sé tekið fram. Vikulegar uppfærslur hefjast venjulega á miðvikudag og lýkur fyrir sunnudag. Bandaríkin, Ástralía, Evrópa, Bretland, Asía og Kanada eru með í vikulegum uppfærslum. 

- **Common Data Service lausnir uppfærslur**: Þessar uppfærslur eiga sér stað um það bil á sex vikna fresti eftir þörfum. Þau fela í sér nýja aðila og breytingar á núverandi aðilum í Common Data Service. Þessar uppfærslur koma út á sömu svæðum og vikulega uppfærslurnar og það tekur um sex vikur að endurtaka í gegnum allar gagnaver. Lausn uppfærslna kann eða er ekki í samræmi við vikulega þjónustuuppfærslur.

Eftirfarandi tafla sýnir sýnishorn áætlun:

| Vika | Uppfærslugerð |
| --- | --- |
| 1 | Uppfærsla á þjónustu (öll svæði) |
| 2 | Þjónustuuppfærsla (öll svæði) + Lausn uppfærsla (vika 1 svæði) |
| 3 | Þjónustuuppfærsla (öll svæði) + Lausn uppfærsla (vika 2 svæði) |
| 4 | Þjónustuuppfærsla (öll svæði) + Lausn uppfærsla (vika 3 svæði) |
| 5 | Þjónustuuppfærsla (öll svæði) + Lausn uppfærsla (vika 4 svæði) |
| 6 | Þjónustuuppfærsla (öll svæði) + Lausn uppfærsla (vika 5 svæði) |
| 7 | Þjónustuuppfærsla (öll svæði) + Lausn uppfærsla (vika 6 svæði) |
| 8 | Uppfærsla á þjónustu (öll svæði) |

> [!NOTE]
> Lausnaruppfærslur eru fáanlegar á öllum gagnaverum þegar þeim er sleppt. Ef þú vilt ekki bíða eftir að uppfærslurnar endurtaki sig sjálfkrafa geturðu beitt þessum uppfærslum handvirkt á hvaða umhverfi sem er í hvaða gagnaveri sem er.

Þegar þörf er á veitir Human Resources einnig eftirfarandi gerðir af lagfæringum:

- **Endurskoðun (leiðrétting)**: villuleiðréttingar sem geta komið fram annað hvort með eða fyrir utan vikulega þjónustuuppfærslu

- **Neyðarúrræði**: fyrirbyggjandi og viðbrögð hotfixes sem eru sjálfstætt í eðli sínu, geta innihaldið eingöngu stillingar eða kóðabreytingar til að leysa vandamál á vefnum og geta komið fyrir utan vikulega útgáfu þjónustuuppfærslu

Útgáfur eru skoðaðar, prófaðar og staðfestar í innra umhverfi. Eftir að búið er að slökkva á smíðum er þeim síðan sent til framleiðslu.

## <a name="exceptions-in-2019"></a>Undantekningar árið 2019

Eftirfarandi dagsetningar eru undantekningar frá venjulegri útgáfuáætlun:

| Dagsetning | Lýsing |
| --- | --- |
| Vikan 25. nóvember | Engar uppfærslur |
| Vikan 16. desember | Aðeins minni uppfærslur |
| Vikan 23. desember | Engar uppfærslur |
| Vikan 30. desember | Engar uppfærslur |

## <a name="communications"></a>Samskipti

Þú getur fundið út hvað er í verkunum fyrir Human Resources og hvað við höfum sent frá okkur á eftirfarandi stöðum:

- [Dynamics 365 Human Resources leiðarvísir](https://dynamics.microsoft.com/roadmap/talent/)

- [Útgáfuáætlanir Dynamics 365](https://docs.microsoft.com/dynamics365/release-plans/)

- [Nýjungar eða breytingar í Dynamics 365 Human Resources](hr-admin-whats-new.md)

- [Vandamálaleit í Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (aðeins fyrir villur sem tengjast verkvangi)

- [Human Resources-bloggið](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [Human Resources Yammer samfélag](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a>Forskoðaðu aðgerðir í sandkassaumhverfi

Þú getur sannreynt forsýningaraðgerðir í sandkassaumhverfi áður en þú virkjar þá í framleiðsluumhverfi þínu. Nánari upplýsingar um virkjun eiginleika er að finna í [Eiginleikastjórnunaryfirlit](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Allar nýju aðgerðirnar eru áfram í forskoðun í að minnsta kosti 30 daga og venjulega 30-60 daga. Helstu eiginleikar eru venjulega fáanlegir í október og apríl ár hvert í kjölfar forskoðunartímabilsins. Um leið og þú sérð nýja möguleika í vinnusvæðinu Stjórnun eiginleika er hægt að kveikja á þeim. Sumar aðgerðir kunna að vera sjálfkrafa á.

Stundum er sambyggður eiginleiki virkur og ekki er hægt að slökkva á honum (til dæmis vinnusvæðinu Stjórnun eiginleika).

Þegar eiginleiki er almennt tiltækur kann að vera kveikt eða slökkt á honum í framleiðsluumhverfi. Vinnusvæðið Stjórnun eiginleika gefur til kynna hvenær forsýningareiginleiki verður nauðsynlegur. Þessi dagsetning er venjulega 1. október eða 1. apríl til að samræma hálfsársáætlun um losun. Ekki er hægt að slökkva á skyldueiginleikum. Þar til það verður skylda geturðu kveikt og slökkt á eiginleikum í öllu umhverfi.

Við mælum mjög með því að forskoða aðgerðir í sandkassa eða prufuumhverfi. Best er að búa til afrit af núverandi framleiðsluumhverfi eða gagnagrunni í sandkassaumhverfi svo að þú getir fengið fullkomna reynslu af nýju aðgerðunum með gögnunum þínum.

Nánari upplýsingar um vistun á sandkassaumhverfi, sjá [Veita verk Human Resources](hr-admin-setup-provision.md). Sjá til að fjarlægja prófunarumhverfi [Fjarlægja tilvik](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment). 

## <a name="report-bugs"></a>Tilkynntu villur

Þó að prófa forskoðunareiginleika eða prófa nýja möguleika gætirðu fundið hluti sem virka ekki eins og búist var við. Vinsamlegast tilkynnið allar villur í gegnum [Microsoft Dynamics 365 stuðning](https://dynamics.microsoft.com/support/).

## <a name="see-also"></a>Sjá einnig

- [Útgáfuáætlanir Dynamics 365 og Power Platform](https://docs.microsoft.com/dynamics365/release-plans)
- [Nýjungar eða breytingar í Dynamics 365 Human Resources](hr-admin-whats-new.md)
- [Reglur um stuðningstíma hugbúnaðar](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)

