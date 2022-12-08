---
title: Uppfærsluferli
description: Microsoft Dynamics 365 Human Resources er sannur hugbúnaður sem þjónusta (SaaS) sem veitir stöðugar, snertilausar þjónustuuppfærslur fyrir breytingar á forriti og verkvangi.
author: twheeloc
ms.date: 12/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 197b3c5717494ab3c80a57cda337a9021293bf73
ms.sourcegitcommit: 68efa7b89273d04484566cbe14d3533a8fd4ee53
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 12/02/2022
ms.locfileid: "9819297"
---
# <a name="update-process"></a>Uppfærsluferli

_**Gildir um:** Mannauð á sjálfstæðum innviðum_ 

> [!NOTE]
> Frá og með júlí 2022 er ekki hægt að útvega nýtt mannauðsumhverfi á sjálfstæðum mannauðsinnviðum og ekki er hægt að búa til ný Microsoft Dynamics Lifecycle Services (LCS) verkefni á því. Viðskiptavinir geta innleitt mannauðsumhverfi á fjármála- og rekstrarinnviðum. Sjá nánar [Útvega mannauðs í innviðum fjármála og rekstrar](hr-admin-setup-provision-fo.md).

> [!IMPORTANT]
> Uppfærslu- og flýtileiðréttingarferlið á innviðum fjármála- og rekstrarforrita er frábrugðið sjálfstætt uppfærslu- og flýtileiðréttingarferli mannauðs. Frekari upplýsingar um uppfærsluferlið er að finna í [Ferli til að fara yfir í nýjustu uppfærslu á fjármálum og rekstri](../fin-ops-core/dev-itpro/migration-upgrade/upgrade-latest-update.md). Fyrir frekari upplýsingar um flýtileiðréttingar, sjá [Hlaða niður uppfærslum frá Lifecycle Services (LCS)](/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs.md). 

Microsoft Dynamics 365 Human Resources er sannur hugbúnaður sem þjónusta (SaaS) sem veitir stöðugar, snertilausar þjónustuuppfærslur. Þessar uppfærslur innihalda bæði forrits- og vettvangsbreytingar sem oft veita mikilvægar endurbætur á þjónustunni, þ.mt uppfærslur á reglugerðum.

## <a name="update-policy"></a>Uppfæra stefnu

Uppfærslur eru gefnar út með reglubundnum hætti fyrir öll umhverfi. Human Resources er stutt samkvæmt [Microsoft Lifecycle policy](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy) sem býður upp á stöðugar og einfaldar leiðbeiningar fyrir tiltækileika stuðnings við vöru.

## <a name="release-cadence"></a>Losunartaktur 

Uppfærslum á Human Resources er beitt sjálfkrafa í öll umhverfi. Human Resources veitir tvenns konar útgáfur:

- **Þjónustuuppfærslur**: Þjónustuuppfærslur innihalda viðeigandi vettvangsuppfærslur þegar þær eru gefnar út. Til viðbótar við uppfærslur sem byggjast á undantekningum, eiga sér stað reglulegar þjónustuuppfærslur í kjölfar uppfærslna á Dynamics 365 Finance vettvangsuppfærslum fyrir almennt aðgengi (GA). Fyrir frekari upplýsingar um útgáfur palla, sjá [Hvað er nýtt eða breytt í pallauppfærslum](../fin-ops-core/dev-itpro/get-started/whats-new-home-page.md). Uppfærslur eru með stigaðri útfærslu á heimsvísu á milli svæða. Fyrir frekari upplýsingar um uppfærslur, sjá [Hvað er nýtt eða breytt í Dynamics 365 Human Resources](hr-admin-whats-new.md).

- **Dataverse lausnir uppfærslur**: Þessar uppfærslur eiga sér stað um það bil á sex vikna fresti eftir þörfum. Þau fela í sér nýja aðila og breytingar á núverandi aðilum í Dataverse. Þessar uppfærslur eru gefnar út á sömu svæðum og tveggja vikna uppfærslur og það tekur um sex vikur að endurtaka þær í gegnum allar gagnaver. Lausn uppfærslna kann eða er ekki í samræmi við þjónustuuppfærslur á tveggja vikna fresti.

> [!NOTE]
> Lausnaruppfærslur eru fáanlegar á öllum gagnaverum þegar þeim er sleppt. Ef þú vilt ekki bíða eftir að uppfærslurnar endurtaki sig sjálfkrafa geturðu beitt þessum uppfærslum handvirkt á hvaða umhverfi sem er í hvaða gagnaveri sem er.

Þegar þörf krefur veitir Mannauðurinn eftirfarandi gerðir af lagfæringum:

- **Endurskoðun (leiðrétting)**: villuleiðréttingar sem geta komið fram annaðhvort með eða fyrir utan þjónustuuppfærslu á tveggja vikna fresti

- **Neyðarúrræði**: Fyrirbyggjandi og viðbragðsbráðabirgafærslur sem eru sjálfstætt í eðli sínu, geta innihaldið eingöngu stillingar eða kóðabreytingar til að leysa vandamál á vefnum og geta komið fyrir utan útgáfu þjónustuuppfærslu á tveggja vikna fresti

Útgáfur eru skoðaðar, prófaðar og staðfestar í innra umhverfi. Eftir að búið er að slökkva á smíðum er þeim síðan sent til framleiðslu.

## <a name="communications"></a>Samskipti

Þú getur fundið út hvað er í verkunum fyrir Human Resources og hvað við höfum sent frá okkur á eftirfarandi stöðum:

- [Dynamics 365 Human Resources leiðarvísir](https://dynamics.microsoft.com/roadmap/human-resources/)

- [Útgáfuáætlanir Dynamics 365](/dynamics365/release-plans/)

- [Nýjungar eða breytingar í Dynamics 365 Human Resources](hr-admin-whats-new.md)

- [Vandamálaleit í Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs.md) (aðeins fyrir villur sem tengjast verkvangi)

- [Human Resources-bloggið](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [Human Resources Yammer samfélag](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a>Forskoðaðu aðgerðir í sandkassaumhverfi

Þú getur sannreynt forsýningaraðgerðir í sandkassaumhverfi áður en þú virkjar þá í framleiðsluumhverfi þínu. Nánari upplýsingar um virkjun eiginleika er að finna í [Eiginleikastjórnunaryfirlit](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Allar nýju aðgerðirnar eru áfram í forskoðun í að minnsta kosti 30 daga og venjulega 30-60 daga. Helstu eiginleikar eru venjulega fáanlegir í október og apríl ár hvert í kjölfar forskoðunartímabilsins. Um leið og þú sérð nýja möguleika í vinnusvæðinu **Stjórnun eiginleika** er hægt að kveikja á þeim. Sumar aðgerðir kunna að vera sjálfkrafa á.

Stundum er sambyggður eiginleiki virkur og ekki er hægt að slökkva á honum (til dæmis vinnusvæðinu Stjórnun eiginleika).

Þegar eiginleiki er almennt tiltækur kann að vera kveikt eða slökkt á honum í framleiðsluumhverfi. Vinnusvæðið **Stjórnun eiginleika** gefur til kynna hvenær forsýningareiginleiki verður nauðsynlegur. Þessi dagsetning er venjulega 1. október eða 1. apríl til að samræma hálfsársáætlun um losun. Ekki er hægt að slökkva á skyldueiginleikum. Þar til það verður skylda geturðu kveikt og slökkt á eiginleikum í öllu umhverfi.

Við mælum mjög með því að forskoða aðgerðir í sandkassa eða prufuumhverfi. Best er að búa til afrit af núverandi framleiðsluumhverfi eða gagnagrunni í sandkassaumhverfi svo að þú getir fengið fullkomna reynslu af nýju aðgerðunum með gögnunum þínum.

Nánari upplýsingar um vistun á sandkassaumhverfi, sjá [Veita verk Human Resources](hr-admin-setup-provision.md). Sjá til að fjarlægja prófunarumhverfi [Fjarlægja tilvik](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment). 

## <a name="report-bugs"></a>Tilkynntu villur

Þó að prófa forskoðunareiginleika eða prófa nýja möguleika gætirðu fundið hluti sem virka ekki eins og búist var við. Vinsamlegast tilkynnið allar villur í gegnum [Microsoft Dynamics 365 stuðning](https://dynamics.microsoft.com/support/).

## <a name="see-also"></a>Sjá einnig

[Útgáfuáætlanir Dynamics 365 og Power Platform](/dynamics365/release-plans)</br>
[Nýjungar eða breytingar í Dynamics 365 Human Resources](hr-admin-whats-new.md)</br>
[Reglur um stuðningstíma hugbúnaðar](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
