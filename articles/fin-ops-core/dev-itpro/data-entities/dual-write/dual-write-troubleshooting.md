---
title: Almenn úrræðaleit
description: Þetta efni veitir upplýsingar um almenna úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: c3352afd93dfc7c37a8af9dabaf85b7a1debad30
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997255"
---
# <a name="general-troubleshooting"></a>Almenn úrræðaleit

[!include [banner](../../includes/banner.md)]



Þetta efni veitir upplýsingar um almenna úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Common Data Service.

> [!IMPORTANT]
> Nokkur þeirra atriða sem þetta efni fjallar um geta krafist annað hvort kerfisstjórans eða Microsoft Azure Active Directory (Azure AD) Leyfisupplýsingar leigjanda. Hlutinn fyrir hvert vandamál útskýrir hvort krafist sé sérstaks hlutverks eða skilríkja.

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a>Þegar þú reynir að setja upp pakka fyrir tvöföld skrif með því að nota verkfærið Package Deployer eru engar fáanlegar lausnir sýndar

Sumar útgáfur af verkfærinu Package Deployer eru ósamrýmanlegar með tvískiptu lausnarpakkanum. Til að setja upp pakkann svo vel sé skaltu passa að nota [útgáfu 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) eða nýrri af verkfærinu Package Deployer.

Eftir að þú hefur sett upp verkfærið Package Deployer skaltu setja upp lausnarpakkann með því að fylgja þessum skrefum.

1. Sæktu nýjustu pakkaskrá lausnarinnar af Yammer.com. Eftir að zip-skráin hefur verið sótt skaltu hægrismella á hana og velja **Eiginleikar**. Veldu gátreitinn **Opna fyrir** og veldu síðan **Beita**. Ef þú sérð ekki gátreitinn **Opna fyrir** er zip-skráin þegar aflæst og þú getur sleppt þessu skrefi.

    ![Svargluggi eiginleika](media/unblock_option.png)

2. Opnaðu zip-skrána með pakkanum og afritaðu allar skrárnar í möppuna **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438**.

    ![Innihald möppunnar Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438](media/extract_package.png)

3. Límdu allar afritaðar skrár í möppuna **Verkfæri** í verkfærinu Package Deployer. 
4. Keyrðu **PackageDeployer.exe** til að velja Common Data Service umhverfið og setja upp lausnirnar.

    ![Innihald möppunnar Verkfæri](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details"></a>Kveiktu á og skoðaðu rakningarkladda viðbótar í Common Data Service til að skoða villuupplýsingar

**Nauðsynlegt hlutverk til að kveikja á rakningarkladda og skoða villur:** Kerfisstjóri

Fylgdu þessum skrefum til að kveikja á rakningarkladda.

1. Skráðu þig inn á líkanadrifna forritið í Dynamics 365, opnaðu síðuna **Stillingar** og undir **Kerfi** veldu **Stjórnun**.
2. Á síðunni **Stjórnun** skal velja **Kerfisstillingar**.
3. Á flipanum **Sérsnið** , í reitnum **Viðbóð og sérsniðnar rakningaraðgerðir verkflæðis** , velurðu **Allt** til að virkja rakningarkladda viðbótar. Ef þú vilt skrá rakningarkladda aðeins þegar undantekningar eiga sér stað, geturðu valið **Undantekning** í staðinn.


Fylgdu þessum skrefum til að skoða rakningarkladdann.

1. Skráðu þig inn á líkanadrifna forritið í Dynamics 365, opnaðu síðuna **Stillingar** og undir **Sérstillingar** veldu **Rakningarkladdi viðbóta**.
2. Findu rakningarkladda þar sem reiturinn **Heiti gerðar** er stilltur á **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.
3. Tvísmelltu á hlut til að skoða alla skrána og síðan á flýtiflipanum **Framkvæmd** , skoðarðu textann **Skilaboðablokk**.

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>Kveiktu á kembiforriti til að leysa vandamál samstillingar í beinni í forritum Finance and Operations

**Nauðsynlegt hlutverk til að skoða villurnar:** Kerfisstjóri Tvíritaðar villur sem eiga uppruna sinn í Common Data Service geta birst í Finance and Operations forritinu. Í sumum tilvikum er allur texti villuboðanna ekki tiltækur vegna þess að skeytið er of langt eða inniheldur persónugreinanlegar upplýsingar (PII). Þú getur kveikt á fjölorðri skráningu á villum með því að fylgja þessum skrefum.

1. Allar verkefnisstillingar í forritum Finance and Operations eru með eiginleikann **IsDebugMode** í eingunni **DualWriteProjectConfiguration**. Opnaðu eininguna **DualWriteProjectConfiguration** með því að nota Excel-viðbótina.

    > [!TIP]
    > Auðveld leið til að opna eininguna er að kveikja á stillingunni **Hönnun** í Excel-viðbótinni og síðan bætt við **DualWriteProjectConfigurationEntity** í vinnublaðið. Nánari upplýsingar eru í [Opna einingagögn í Excel og uppfæra þau með Excel-innbót](../../office-integration/use-excel-add-in.md).

2. Stilltu eiginleikann **IsDebugMode** á **Já** fyrir verkið.
3. Keyrðu atburðarásina sem er að búa til villur.
4. Fjölorðir kladdar eru fáanlegir í töflunni DualWriteErrorLog. Notaðu eftirfarandi slóð til að fletta upp gögnum í vafra töflunnar (skipta út **XXX** eftir atvikum):

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=>DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Athugaðu samstillingarvillur á sýndarvélinni fyrir forritið Finance and Operations

**Nauðsynlegt hlutverk til að skoða villurnar:** Kerfisstjóri

1. Skráðu þig inn í Microsoft Dynamics Lifecycle Services (LCS).
2. Opnaðu LCS-verkið sem þú valdir til að gera tvískriftaprófun fyrir.
3. Veldu reitinn **Umhverfi í skýi**.
4. Notaðu Remote Desktop til að skrá þig inn á sýndarvélina (VM) fyrir forrit Finance and Operations. Notaðu staðbundna reikninginn sem er sýndur í LCS.
5. Opnaðu tilvikayfirlit.
6. Veldu **Forrit og þjónustukladdar \> Microsoft \> Dynamics \> AX -DualWriteSync \> Virkt**.
7. Farðu yfir listann yfir nýlegar villur.

## <a name="unlink-and-link-another-common-data-service-environment-from-a-finance-and-operations-app"></a>Taktu af og tengdu annað Common Data Service umhverfi úr forrit Finance and Operations

**Nauðsynlegt hlutverk til að aftengja umhverfið:** Kerfisstjóri fyrir Finance and Operations forritið eða Common Data Service.

1. Innskráning í forritið Finance and Operations.
2. Farðu í **Vinnusvæði \> Gagnastjórnun** og veldu reitinn **Tvöfalt skrif**.
3. Veldu allar keyrandi kortlagningar og veldu síðan **Hætta**.
4. Veldu **Aftengja umhverfi**.
5. Veldu **Já** til að staðfesta aðgerðina.

Þú getur nú tengt nýtt umhverfi.

## <a name="unable-to-view-the-sales-order-line-information-form"></a>Ekki er hægt að skoða Upplýsingar sölupöntunarlínu 

Þegar þú býrð til sölupöntun í Dynamics 365 Sales og smellir á **+ Bæta við afurðum** kanntu að fara á Dynamics 365 Project Operations pöntunarlínu. Ekki er hægt að skoða **Upplýsingar** sölupöntunarlínu úr þeirri skjámynd. Valkosturinn fyrir **Upplýsingar** birtist ekki í fellivalmyndinni fyrir neðan **Ný pöntunarlína**. Þetta gerist vegna þess að Project Operations hefur verið sett upp í umhverfi þínu.

Fylgdu þessum skrefum til að gera virkja valkostinn **Upplýsingar** aftur:
1. Fara í eigindina **Pöntunarlína**.
2. Finndu **Upplýsingar** undir skjámyndum. 
3. Veldu **Upplýsingar** og smelltu á **Virkja öryggishlutverk**. 
4. Breyttu öryggisstillingunni í **Sýna öllum**.
