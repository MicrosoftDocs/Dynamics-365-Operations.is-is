---
title: Afritið tilvik
description: Þú getur notað Microsoft Dynamics Lifecycle Services (LCS) til að afrita Microsoft Dynamics 365 Human Resources gagnagrunn í sandkassaumhverfi.
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
ms.openlocfilehash: bb363369994d99f358be0c23cdaf1dbc80b644e5
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092293"
---
# <a name="copy-an-instance"></a>Afritið tilvik

Þú getur notað Microsoft Dynamics Lifecycle Services (LCS) til að afrita Microsoft Dynamics 365 Human Resources gagnagrunn í sandkassaumhverfi. Ef þú ert með annað sandkassaumhverfi geturðu einnig afritað gagnagrunninn úr því umhverfi yfir í markviss sandkassaumhverfi.

Til að afrita dæmi verður þú að tryggja eftirfarandi:

- Tilvik Human Resources sem þú vilt skrifa yfir verður að vera sandkassaumhverfi.

- Umhverfið sem þú ert að afrita frá og til verður að vera á sama svæði. Þú getur ekki afritað á milli svæða.

- Þú verður að vera stjórnandi í markumhverfinu svo þú getir skráð þig inn á það eftir að hafa afritað tilvikið.

- Þegar þú afritar gagnagrunn Human Resources, afritar þú ekki þá þætti (forrit eða gögn) sem eru í Microsoft PowerApps-umhverfi. Fyrir upplýsingar um hvernig á að afrita þætti í PowerApps-umhverfi, sjá [Afrita umhverfi](https://docs.microsoft.com/power-platform/admin/copy-environment). PowerApps-umhverfið sem þú vilt skrifa yfir verður að vera sandkassaumhverfi. Þú verður að vera alþjóðlegur leigjandi stjórnandi til að breyta PowerApps-framleiðsluumhverfi í sandkassaumhverfi. Fyrir frekari upplýsingar um að breyta PowerApps-umhverfi, sjáðu [Skiptu um dæmi](https://docs.microsoft.com/dynamics365/admin/switch-instance).

## <a name="effects-of-copying-a-human-resources-database"></a>Áhrif afritunar gagnagrunns Human Resources

Eftirfarandi atburðir eiga sér stað þegar þú afritar gagnagrunn Human Resources:

- Afritunarferlið eyðir núverandi gagnagrunni í markumhverfinu. Eftir að afritunarferlinu er lokið geturðu ekki endurheimt núverandi gagnagrunn.

- Markaumhverfið verður ekki tiltækt fyrr en afritunarferlinu er lokið.

- Skjöl í Microsoft Azure Blob geymsla er ekki afrituð úr einu umhverfi í annað. Þess vegna verða öll skjöl og sniðmát sem fylgja eru ekki afrituð og þau verða áfram í upprunaumhverfinu.

- Allir notendur nema stjórnandi og aðrar notendareikningar innri þjónustu verða gerðir óvirkir. Þess vegna getur stjórnandi notandinn eytt eða skyggt á gögn áður en aðrir notendur eru leyfðir aftur inn í kerfið.

- Stjórnandi notandinn verður að gera nauðsynlegar stillingarbreytingar, svo sem aftur að tengja endapunkta samþættingar við tiltekna þjónustu eða vefslóðir.

## <a name="copy-the-human-resources-database"></a>Afritaðu gagnagrunn Human Resources

Til að ljúka þessu verkefni afritarðu fyrst dæmi og skráir þig síðan inn á Microsoft Power Platform Admin Center til að afrita PowerApps-umhverfi.

> [!WARNING]
> Þegar þú afritar dæmi er gagnagrunninum eytt í markatilvikinu. Markmiðið er ekki tiltækt meðan á þessu ferli stendur.

1. Skráðu þig inn á LCS og veldu LCS verkefnið sem inniheldur dæmið sem þú vilt afrita.

2. Í LCS verkinu skaltu velja **Human Resources Stjórnun Forrits** reitinn.

3. Veldu dæmið sem á að afrita og veldu síðan **Afrita**.

4. Í verkglugganum **Afritaðu dæmi**, veldu dæmið sem á að skrifa yfir og veldu síðan **Afrita**. Bíddu eftir því að gildið í reitnum **Afrita stöðu** sé uppfært í **Lokið**.

   ![[Velja tilvik til að skrifa yfir](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. Veldu **Power Platform** og skráðu þig inn í Admin Center Microsoft Power Platform.

   ![[Veldu Power Platform](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. Veldu PowerApps-umhverfið sem á að afrita og veldu síðan **Afrita**.

7. Þegar afritunarferlinu er lokið, skráðu þig inn á markstaðinn og virkjaðu samþættinguna Common Data Service. Nánari upplýsingar og leiðbeiningar, sjá [Skilgreina samþættingu Common Data Service](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).

## <a name="data-elements-and-statuses"></a>Gagnaþátta og staða

Eftirfarandi gagnaþættir eru ekki afritaðir þegar þú afritar tilvik Human Resources:

- Netföng í töflunni **LogisticsElectronicAddress**

- Runuvinnslusaga í töflunum **BatchJobHistory**, **BatchHistory**, og **BatchConstraintHistory**

- SMTP lykilorð lykilorðsins í töflunni **SysEmailSMTPPassword**

- SMTP gengi miðlarans í töflunni **SysEmailParameters**

- Prentastjórnunarstillingar í töflunum **PrintMgmtSettings** og **PrintMgmtDocInstance**

- Umhverfissértækar skrár í töflunum **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, og **BatchServerGroup**

- Skjal viðhengi í DocuValue-töflunni. Þessi viðhengi innihalda öll Microsoft Office-sniðmát sem skrifað var yfir í heimildarumhverfinu

- Tengingarstrengurinn í töflunni **PersonnelIntegrationConfiguration**

Sumir af þessum þáttum eru ekki afritaðir vegna þess að þeir eru umhverfissértækir. Sem dæmi má nefna skrárnar **BatchServerConfig** og **SysCorpNetPrinters**. Aðrir þættir eru ekki afritaðir vegna magns stuðningsmiða. Til dæmis gætu tvíteknir tölvupóstar verið sendir vegna þess að SMTP er ennþá virkt í umhverfi notendasamþykktarprófunar (sandkassi), ógild samþættingarskilaboð gætu verið send vegna þess að hópastörf eru ennþá virk og notendur gætu verið virkjaðir áður en umsjónarmenn geta framkvæmt hreinsunaraðgerðir eftir endurnýjun.

Að auki breytast eftirfarandi stöðu þegar þú afritar tilvik:

- Allir notendur nema stjórnandi eru stilltir á **Avirkjað**.

- Allar runuvinnslur nema nokkrar kerfisvinnslur eru stilltar á **Halda eftir**.

## <a name="environment-admin"></a>Umhverfisstjóri

Öllum notendum í marksandkassaumhverfinu, þar með talið stjórnendum, er skipt út fyrir stjórnendur í upprunaumhverfinu. Vertu viss um að þú sért stjórnandi í markumhverfinu áður en þú afritar tilvik. Ef þú ert það ekki muntu ekki geta skráð þig inn í sandkassaumhverfið eftir að afritið er lokið.

Allir notendur sem ekki eru kerfisstjórar í markkassasumhverfinu eru óvirkir til að koma í veg fyrir óæskileg innritun í sandkassaumhverfið. Stjórnendur geta endurtekið notendur ef þörf er á.
