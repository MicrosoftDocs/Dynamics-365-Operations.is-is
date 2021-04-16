---
title: Afritið tilvik
description: Þú getur notað Microsoft Dynamics Lifecycle Services (LCS) til að afrita Microsoft Dynamics 365 Human Resources gagnagrunn í sandkassaumhverfi.
author: andreabichsel
ms.date: 07/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6cb8050980b9b54480d09a59379430cd229ff141
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801096"
---
# <a name="copy-an-instance"></a>Afritið tilvik

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Þú getur notað Microsoft Dynamics Lifecycle Services (LCS) til að afrita Microsoft Dynamics 365 Human Resources gagnagrunn í sandkassaumhverfi. Ef þú ert með annað sandkassaumhverfi geturðu einnig afritað gagnagrunninn úr því umhverfi yfir í markviss sandkassaumhverfi.

Til að afrita tilvik skal hafa eftirfarandi í huga:

- Tilvik Human Resources sem þú vilt skrifa yfir verður að vera sandkassaumhverfi.

- Umhverfið sem þú ert að afrita af og til verður að vera á sama svæði. Þú getur ekki afritað á milli svæða.

- Þú verður að vera stjórnandi í markumhverfinu svo þú getir skráð þig inn á það eftir að hafa afritað tilvikið.

- Þegar þú afritar gagnagrunn Human Resources, afritar þú ekki þá þætti (forrit eða gögn) sem eru í Microsoft Power Apps-umhverfi. Fyrir upplýsingar um hvernig á að afrita þætti í Power Apps-umhverfi, sjá [Afrita umhverfi](https://docs.microsoft.com/power-platform/admin/copy-environment). Power Apps-umhverfið sem þú vilt skrifa yfir verður að vera sandkassaumhverfi. Þú verður að vera alþjóðlegur leigjandi stjórnandi til að breyta Power Apps-framleiðsluumhverfi í sandkassaumhverfi. Fyrir frekari upplýsingar um að breyta Power Apps-umhverfi, sjáðu [Skiptu um dæmi](https://docs.microsoft.com/dynamics365/admin/switch-instance).

- Ef tilvik er afritað inn í sandkassaumhverfi og ætlunin er að samþætta sandkassaumhverfið við Dataverse þarf að endurnota sérstillta reiti í Dataverse töflurnar. Sjá [Nota sérstillta reiti á Dataverse](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).

## <a name="effects-of-copying-a-human-resources-database"></a>Áhrif afritunar gagnagrunns Human Resources

Eftirfarandi atburðir eiga sér stað þegar þú afritar gagnagrunn Human Resources:

- Afritunarferlið eyðir núverandi gagnagrunni í markumhverfinu. Eftir að afritunarferlinu er lokið geturðu ekki endurheimt núverandi gagnagrunn.

- Markaumhverfið verður ekki tiltækt fyrr en afritunarferlinu er lokið.

- Skjöl í Microsoft Azure Blob geymsla er ekki afrituð úr einu umhverfi í annað. Þar af leiðandi verða öll skjöl og sniðmát sem eru hengd við ekki afrituð og verða áfram í upprunaumhverfinu.

- Allir notendur nema stjórnandi og aðrar notendareikningar innri þjónustu verða gerðir óvirkir. Stjórnandi getur eytt eða lokað á gögn áður en aðrir notendur eru leyfðir aftur í kerfinu.

- Stjórnandi notandinn verður að gera nauðsynlegar stillingarbreytingar, svo sem aftur að tengja endapunkta samþættingar við tiltekna þjónustu eða vefslóðir.

## <a name="copy-the-human-resources-database"></a>Afritaðu gagnagrunn Human Resources

Til að ljúka þessu verkefni afritarðu fyrst dæmi og skráir þig síðan inn á Microsoft Power Platform Admin Center til að afrita Power Apps-umhverfi.

> [!WARNING]
> Þegar þú afritar dæmi er gagnagrunninum eytt í markatilvikinu. Markmiðið er ekki tiltækt meðan á þessu ferli stendur.

1. Skráðu þig inn á LCS og veldu LCS verkefnið sem inniheldur dæmið sem þú vilt afrita.

2. Í LCS verkinu skaltu velja **Human Resources Stjórnun Forrits** reitinn.

3. Veldu dæmið sem á að afrita og veldu síðan **Afrita**.

4. Í verkglugganum **Afritaðu dæmi**, veldu dæmið sem á að skrifa yfir og veldu síðan **Afrita**. Bíddu eftir því að gildið í reitnum **Afrita stöðu** sé uppfært í **Lokið**.

   ![[Veldu dæmi til að skrifa yfir](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. Veldu **Power Platform** og skráðu þig inn í Admin Center Microsoft Power Platform.

   ![[Veldu Power Platform](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. Veldu Power Apps-umhverfið sem á að afrita og veldu síðan **Afrita**.

7. Þegar afritunarferlinu er lokið, skráðu þig inn á markstaðinn og virkjaðu samþættinguna Dataverse. Nánari upplýsingar og leiðbeiningar, sjá [Skilgreina samþættingu Dataverse](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).

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

Sumar þessara eininga eru ekki afritaðar vegna þess að þær eru háðar tilteknu umhverfi. Sem dæmi má nefna skrárnar **BatchServerConfig** og **SysCorpNetPrinters**. Aðrir þættir eru ekki afritaðir vegna magns stuðningsmiða. Dæmi:

- Hægt er að senda afrit af tölvupóstum vegna þess að SMTP er enn virkt í samþykkisprófun notanda (sandkassa).

- Ógild samþættingarskilaboð kunna að verða send vegna þess að runuvinnslur eru enn virkar.

- Notendur gætu verið virkir áður en stjórnendur getur framkvæmt hreinsunaraðgerðir eftir uppfærslu.

Einnig breytast eftirfarandi stöður þegar tilvik er afritað:

- Allir notendur nema stjórnandi eru stilltir á **Avirkjað**.

- Allar runuvinnslur nema nokkrar kerfisvinnslur eru stilltar á **Halda eftir**.

## <a name="environment-admin"></a>Umhverfisstjóri

Öllum notendum í marksandkassaumhverfinu, þar með talið stjórnendum, er skipt út fyrir stjórnendur í upprunaumhverfinu. Vertu viss um að þú sér stjórnandi í upprunaumhverfinu áður en þú afritar dæmi. Ef þú ert það ekki geturðu ekki skráp þig inn í sandkassaumhverfi viðtökustaða eftir að afritun er lokið.

Allir notendur sem ekki eru kerfisstjórar í markkassasumhverfinu eru óvirkir til að koma í veg fyrir óæskileg innritun í sandkassaumhverfið. Stjórnendur geta endurtekið notendur ef þörf er á.

## <a name="apply-custom-fields-to-dataverse"></a>Nota sérstillta reiti á Dataverse

Ef tilvik er afritað inn í sandkassaumhverfi og ætlunin er að samþætta sandkassaumhverfið við Dataverse þarf að endurnota sérstillta reiti í Dataverse töflurnar.

Fyrir hvern sérstilltan reit sem birtist í Dataverse-töflum skal fara í gegnum eftirfarandi skref:

1. Farið í sérstillta reitinn og veljið **Breyta völdu**.

2. Afvelja skal reitinn **Virkur** fyrir hverja cdm_* einingu sem sérstillti reiturinn er virkur fyrir.

3. Veljið **Nota breytingar**.

4. Veljið **Breyta** aftur.

5. Velja skal svæðið **Virkt** fyrir hverja cdm_* einingu sem sérstillti reiturinn er virkur fyrir.

6. Veljið **Nota breytingar** aftur.

Ferlið við að afturkalla valið, nota breytingar, endurvelja og endurnota breytingar kalla á uppfærslu skema í Dataverse til að taka með sérstillta reiti.

Frekari upplýsingar um sérsniðna reiti er að finna á [Stofna og vinna með sérstillt svæði](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields).

## <a name="see-also"></a>Sjá einnig

[Ráðstafa Human Resources](hr-admin-setup-provision.md)</br>
[Fjarlægja tilvik](hr-admin-setup-remove-instance.md)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]