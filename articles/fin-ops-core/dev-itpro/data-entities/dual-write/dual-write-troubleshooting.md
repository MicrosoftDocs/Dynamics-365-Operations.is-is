---
title: Almenn úrræðaleit
description: Þetta efnisatriði veitir almennar upplýsingar um úrræðaleit fyrir tvískrifa samþættingu milli Finance and Operations forrita og Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f6f5b9f26990e2f4db9bf69040a6c4be31400b40
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062339"
---
# <a name="general-troubleshooting"></a>Almenn úrræðaleit

[!include [banner](../../includes/banner.md)]



Þetta efnisatriði veitir almennar upplýsingar um úrræðaleit fyrir tvískrifa samþættingu milli Finance and Operations forrita og Dataverse.

> [!IMPORTANT]
> Nokkur þeirra atriða sem þetta efni fjallar um geta krafist annað hvort kerfisstjórans eða Microsoft Azure Active Directory (Azure AD) Leyfisupplýsingar leigjanda. Hlutinn fyrir hvert vandamál útskýrir hvort krafist sé sérstaks hlutverks eða skilríkja.

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>Virkið og skoðið rakningarkladda viðbóta í Dataverse til að skoða upplýsingar um villu

**Nauðsynlegt hlutverk til að kveikja á rakningarkladda og skoða villur:** Kerfisstjóri

Fylgdu þessum skrefum til að kveikja á rakningarkladda.

1. Skráðu þig inn í forrit viðskiptavinar, opnaðu síðuna **Stillingar** og undir **Kerfi** velurðu **Stjórnun**.
2. Á síðunni **Stjórnun** skal velja **Kerfisstillingar**.
3. Á flipanum **Sérsnið**, í dálkinum **Viðbót og sérsniðnar rakningaraðgerðir verkflæðis**, velurðu **Allt** til að virkja rakningarkladda viðbótar. Ef þú vilt skrá rakningarkladda aðeins þegar undantekningar eiga sér stað, geturðu valið **Undantekning** í staðinn.


Fylgdu þessum skrefum til að skoða rakningarkladdann.

1. Skráðu þig inn í forrit viðskiptavinar, opnaðu síðuna **Stillingar** og undir **Sérstilling** velurðu **Viðbót rakningarkladda**.
2. Findu rakningarkladda þar sem dálkurinn **Heiti gerðar** er stilltur á **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.
3. Tvísmelltu á hlut til að skoða alla skrána og síðan á flýtiflipanum **Framkvæmd**, skoðarðu textann **Skilaboðablokk**.

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>Virkjaðu villuleitarstillingu til að leysa vandamál í beinni samstillingu í Finance and Operations forritum

**Nauðsynlegt hlutverk til að skoða villurnar:** Kerfisstjóri

Tvöfalt skrif villur sem eiga uppruna sinn í Dataverse getur birst í Finance and Operations appinu. Til að virkja fjölorða skráningu fyrir villurnar skal fylgja þessum skrefum:

1. Fyrir allar verkefnastillingar í Finance and Operations appinu er fáni **IsDebugMode** á **DualWriteProjectConfiguration** borð.
2. Opnaðu **DualWriteProjectConfiguration** með Excel-innbótinni. Til að nota viðbótina skaltu virkja hönnunarham í Finance and Operations Excel viðbótinni og bæta við **DualWriteProjectConfiguration** að blaðinu. Frekari upplýsingar er að finna í [Skoða og uppfæra einingagögn með Excel](../../office-integration/use-excel-add-in.md).
3. Stilltu **IsDebugMode** á **Já** í verkinu.
4. Keyrðu atburðarásina sem er að búa til villur.
5. Fjölorða kladdar eru geymdir í töflunni **DualWriteErrorLog**.
6. Til að fletta upp gögnum á töfluvafra skal nota eftirfarandi tengil: `https://999aos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`, sem kemur í staðinn fyrir `999` eftir þörfum.
7. Uppfærðu aftur eftir [KB 4595434](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=98e5dc124ac125c57ad633d885ac612aea3ddb8f4abf9d71ab3aa354f2e06cbe) sem er í boði fyrir uppfærslur á verkvangi 37 og síðar. Ef þú ert með þessa lagfæringu uppsetta þá sækir kembistillingin fleiri kladda.  

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Athugaðu samstillingarvillur á sýndarvélinni fyrir Finance and Operations appið

**Nauðsynlegt hlutverk til að skoða villurnar:** Kerfisstjóri

1. Skráðu þig inn í Microsoft Dynamics Lifecycle Services (LCS).
2. Opnaðu LCS-verkið sem þú valdir til að gera tvískriftaprófun fyrir.
3. Veldu reitinn **Umhverfi í skýi**.
4. Notaðu Remote Desktop til að skrá þig inn á sýndarvélina (VM) fyrir Finance and Operations appið. Notaðu staðbundna reikninginn sem er sýndur í LCS.
5. Opnaðu tilvikayfirlit.
6. Veldu **Forrit og þjónustukladdar \> Microsoft \> Dynamics \> AX -DualWriteSync \> Virkt**.
7. Farðu yfir listann yfir nýlegar villur.

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a>Aftengdu og tengdu annað Dataverse umhverfi frá Finance and Operations app

**Áskilið hlutverk til að aftengja umhverfið:** Kerfisstjóri fyrir annað hvort Finance and Operations app eða Dataverse.

1. Skráðu þig inn á Finance and Operations appið.
2. Farðu í **Vinnusvæði \> Gagnastjórnun** og veldu reitinn **Tvöfalt skrif**.
3. Veldu allar keyrandi kortlagningar og veldu síðan **Hætta**.
4. Veldu **Aftengja umhverfi**.
5. Veldu **Já** til að staðfesta aðgerðina.

Þú getur nú tengt nýtt umhverfi.

## <a name="unable-to-view-the-sales-order-line-information-form"></a>Ekki er hægt að skoða Upplýsingar sölupöntunarlínu 

Þegar búin er til sölupöntun í Dynamics 365 Sales og smellt er á **+ Bæta við afurðum** kanntu að fara á eyðublað Dynamics 365 Project Operations pöntunarlínu. Ekki er hægt að skoða **Upplýsingar** sölupöntunarlínu úr þeirri skjámynd. Valkosturinn fyrir **Upplýsingar** birtist ekki í fellivalmyndinni fyrir neðan **Ný pöntunarlína**. Þetta gerist vegna þess að Project Operations hefur verið sett upp í umhverfi þínu.

Fylgdu þessum skrefum til að gera virkja valkostinn **Upplýsingar** aftur:

1. Fara í töfluna **Pöntunarlína**.
2. Finndu **Upplýsingar** undir skjámyndum.
3. Veldu **Upplýsingar** og smelltu á **Virkja öryggishlutverk**.
4. Breyttu öryggisstillingunni í **Sýna öllum**.

## <a name="how-to-enable-and-save-network-trace-so-that-traces-can-be-attached-to-support-tickets"></a>Hvernig á að virkja og vista netrakningu þannig að hægt verði að hengja rakningar við þjónustubeiðni

Þjónustudeildin gæti þurft að fara yfir netrakningar til að  úrræðaleita sum vandamál. Til að búa til netrakningu skal fylgja þessum skrefum:

### <a name="chrome"></a>Chrome

1. Í opna flipanum skal ýta á **F12** eða velja **Verkfæri þróunaraðila** til að opna verkfæri þróunaraðila.
2. Opnaðu flipann **Netkerfi** og sláðu inn **integ** í textasíureitinn.
3. Keyrðu aðstæðurnar og fylgstu með beiðnunum sem eru skráðar inn.
4. Hægrismelltu á færslurnar og veldu **Vista allt sem HAR með efni**.

### <a name="microsoft-edge"></a>Microsoft Edge

1. Í opna flipanum skal ýta á **F12** eða velja **Verkfæri þróunaraðila** til að opna verkfæri þróunaraðila.
2. Opnaðu flipann **Netkerfi**.
3. Keyrðu aðstæðurnar.
4. Veldu **vista** til að flytja út niðurstöður sem HAR.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
