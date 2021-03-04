---
title: Uppfærsluferli
description: Microsoft Dynamics 365 Human Resources er sannur hugbúnaður sem þjónusta (SaaS) sem veitir stöðugar, snertilausar þjónustuuppfærslur fyrir breytingar á forriti og verkvangi.
author: andreabichsel
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d841a026f589d774ec5ada3ac9adcc84dde9aee1
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527809"
---
# <a name="update-process"></a>Uppfærsluferli

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics 365 Human Resources er sannur hugbúnaður sem þjónusta (SaaS) sem veitir stöðugar, snertilausar þjónustuuppfærslur. Þessar uppfærslur innihalda bæði forrits- og vettvangsbreytingar sem oft veita mikilvægar endurbætur á þjónustunni, þ.mt uppfærslur á reglugerðum.

## <a name="update-policy"></a>Uppfæra stefnu

Uppfærslur eru gefnar út með reglubundnum hætti fyrir öll umhverfi. Human Resources er stutt samkvæmt [Microsoft Lifecycle policy](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy) sem býður upp á stöðugar og einfaldar leiðbeiningar fyrir tiltækileika stuðnings við vöru.

## <a name="release-cadence"></a>Losunartaktur 

Uppfærslum á Human Resources er beitt sjálfkrafa í öll umhverfi. Human Resources veitir tvenns konar útgáfur:

- **Þjónustuuppfærslur**: Uppfærslur verða á tveggja vinkna fresti sem innihalda villuleiðréttingar og nýja eiginleika. Þjónustuuppfærslur innihalda einnig viðeigandi uppfærslur á palli þegar þær eru gefnar út. Sjá til að fá hugmynd um hvenær uppfærslur á verkvangi eru gefnar út [Tafla 3: Verkvangsútgáfur](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases). Uppfærslur á tveggja vikna fresti eru settar á svið alþjóðlegt útbreiðsla milli svæða. Nánari upplýsingar um uppfærslur á tveggja vikna fresti eru í [Hvað er nýtt eða breytt í Dynamics 365 Human Resources](hr-admin-whats-new.md).

    Öll studd gagnaver uppfæra á tveggja vikna fresti nema annað sé tekið fram. Bandaríkin, Ástralía, Evrópa, Bretland, Asía og Kanada eru með í uppfærslum á tveggja vikna fresti. 

- **Common Data Service lausnir uppfærslur**: Þessar uppfærslur eiga sér stað um það bil á sex vikna fresti eftir þörfum. Þau fela í sér nýja aðila og breytingar á núverandi aðilum í Common Data Service. Þessar uppfærslur koma út á sömu svæðum og uppfærslur á tveggja vikna fresti og það tekur um sex vikur að endurtaka í gegnum öll gagnaver. Lausn uppfærslna kann eða er ekki í samræmi við þjónustuuppfærslur á tveggja vikna fresti.

> [!NOTE]
> Lausnaruppfærslur eru fáanlegar á öllum gagnaverum þegar þeim er sleppt. Ef þú vilt ekki bíða eftir að uppfærslurnar endurtaki sig sjálfkrafa geturðu beitt þessum uppfærslum handvirkt á hvaða umhverfi sem er í hvaða gagnaveri sem er.

Þegar þörf er á veitir Human Resources einnig eftirfarandi gerðir af lagfæringum:

- **Endurskoðun (leiðrétting)**: villuleiðréttingar sem geta komið fram annaðhvort með eða fyrir utan þjónustuuppfærslu á tveggja vikna fresti

- **Neyðarúrræði**: Fyrirbyggjandi og viðbragðsbráðabirgafærslur sem eru sjálfstætt í eðli sínu, geta innihaldið eingöngu stillingar eða kóðabreytingar til að leysa vandamál á vefnum og geta komið fyrir utan útgáfu þjónustuuppfærslu á tveggja vikna fresti

Útgáfur eru skoðaðar, prófaðar og staðfestar í innra umhverfi. Eftir að búið er að slökkva á smíðum er þeim síðan sent til framleiðslu.

## <a name="release-cadence-exceptions-in-2020"></a>Undantekningar á útgáfutíðni árið 2020

Til að taka með frídaga er úttektaráætlun fyrir nóvember og desember 2020 sem hér segir:

- Nóvemberútgáfa: 2. nóvember til 13. nóvember
- Desemberútgáfa: 30. nóvember til 11. desember
 
Tveggja vikna útgáfa mun halda áfram eins og venjulega þann 11. janúar 2021.

## <a name="communications"></a>Samskipti

Þú getur fundið út hvað er í verkunum fyrir Human Resources og hvað við höfum sent frá okkur á eftirfarandi stöðum:

- [Dynamics 365 Human Resources leiðarvísir](https://dynamics.microsoft.com/roadmap/human-resources/)

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

[Útgáfuáætlanir Dynamics 365 og Power Platform](https://docs.microsoft.com/dynamics365/release-plans)</br>
[Nýjungar eða breytingar í Dynamics 365 Human Resources](hr-admin-whats-new.md)</br>
[Reglur um stuðningstíma hugbúnaðar](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)



[!INCLUDE[footer-include](../includes/footer-banner.md)]