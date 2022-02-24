---
title: Vinna með eiginleika
description: Lærðu hvernig á að kveikja og slökkva á nýjum eiginleikum Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9176e9519c3bf65ef7a4f1b5ae43dbeb411750f5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419063"
---
# <a name="manage-features"></a>Vinna með eiginleika

Sem hluti af samfelldri kynningu okkar á nýrri afkastagetu fyrir Microsoft Dynamics 365 Human Resources, viljum við að viðskiptavinir upplifi nýja eiginleika eins fljótt og auðið er. Við veitum forskoðunareiginleika sem eru næstum tilbúnir til almenns framboðs og hafa farið í gegnum víðtækar prófanir. Við erum bara að falast eftir lokaumsögnum viðskiptavina og fullgildingu áður en við gefum þá út fyrir almenning.

Frekari upplýsingar um nýja eiginleika í Human Resources er að finna í [Nýjungar eða breytingar í Human Resources](hr-admin-whats-new.md) og [Dynamics 365 og Power Platform útgáfuupplýsingar](https://docs.microsoft.com/dynamics365/release-plans/#pivot=products&panel=products1).

Vinnusvæðið **Stjórnun eiginleika** býður upp á lista yfir eiginleika sem eru afhentir í hverri útgáfu. Sjálfgefið er að slökkt sé á nýjum eiginleikum. Hægt er að nota vinnusvæðið til að kveikja á þeim og skoða fylgiskjölin fyrir þá. Nánari upplýsingar um stjórnun eiginleika er að finna í [Eiginleikastjórnunaryfirlit](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Allar nýju aðgerðirnar eru áfram í forskoðun í að minnsta kosti 30 daga og venjulega 30-60 daga. Helstu eiginleikar eru venjulega fáanlegir í október og apríl ár hvert í kjölfar forskoðunartímabilsins. Um leið og þú sérð nýja möguleika í vinnusvæðinu **Stjórnun eiginleika** er hægt að kveikja á þeim. Sumar aðgerðir kunna að vera sjálfkrafa á.

Þegar eiginleiki er almennt tiltækur kann að vera kveikt eða slökkt á honum í framleiðsluumhverfi. Vinnusvæðið **Stjórnun eiginleika** gefur til kynna hvenær forsýningareiginleiki verður nauðsynlegur. Þessi dagsetning er venjulega 1. október eða 1. apríl til að samræma hálfsársáætlun um losun. Ekki er hægt að slökkva á skyldueiginleikum. Þar til það verður skylda geturðu kveikt og slökkt á eiginleikum í öllu umhverfi.

## <a name="enable-or-disable-preview-features"></a>Virkja eða slökkva á forskoðunareiginleikum

Til að fá aðgang að forskoðunareiginleikum þarf fyrst að virkja þá í umhverfinu. Að kveikja eða slökkva á forskoðunareiginleikum fer eftir hverju umhverfi fyrir sig.

> [!IMPORTANT]
> Forskoðunareiginleikar eru aðeins í boði í umhverfi **sandkassa**. Þegar kveikt er á stillingunni Forskoðunareiginleikar virkjast hún fyrir alla notendur í fyrirtækinu þínu sem eru í því umhverfi. Þegar slökkt er á forskoðunarstillingunni, gerirðu hana óvirka og óaðgengilega fyrir notendur þína. Forskoðunareiginleikar hafa takmarkaðan stuðning í Human Resources. Þeir gætu notað færri persónuverndar- og öryggisráðstafanir og þær eru ekki innifalin í þjónustustigssamningi Human Resources (SLA). Þú ættir ekki að nota forskoðunareiginleika til að vinna úr persónulegum gögnum (það er, einhverjum upplýsingum sem þú þekkist á) eða að vinna úr öðrum gögnum sem falla undir lögboðnar kröfur eða reglur um samræmi.

1. Veldu í Human Resources **Kerfisstjórnun**.

2. Veldu reitinn **Stjórnun eiginleika**.

3. Til að gera forskoðunareiginleika virkan skaltu velja hann af listanum og velja síðan **Virkja**. Til að gera forskoðunareiginleika óvirkan skaltu velja hann af listanum og velja síðan **Afvirkja**.

## <a name="enable-or-disable-benefits-management"></a>Virkja eða afvirkja fríðindastjórnun

Til að virkja fríðindastjórnun notarðu sama ferli í [Virkja eða afvirkja forskoðunareiginleika](hr-admin-manage-features.md?enable-or-disable-preview-features).

> [!IMPORTANT]
> Ekki er hægt að afvirkja fríðindastjórnun í umhverfi **Framleiðslu** þegar það hefur verið virkjað. Þó er hægt að afvirkja fríðindastjórnun í umhverfinu **Sandkassi**.

Fyrir frekari upplýsingar um stillingar og notkun á yfirliti fríðindastjórnunar, sjá [Yfirlit fríðindastjórnunar](hr-benefits-management-overview.md).

Hagur stjórnun kemur í stað virkni í vinnusvæðinu **Fríðindi**. Þegar þú kveikir á forskoðunareiginleikanum fyrir ávinning stjórnunar geturðu ekki lengur nálgast eftirfarandi form í vinnusvæðinu **Fríðindi**:

- **Fríðindi**
- **Fríðindaeiningar**
- **Hlutfall útreikninga á framlagi**
- **Niðurstöður fríðindaskráningar**
- **Niðurstöður afturköllunar og lengingar fríðinda**
- **Gerðir reglna um hæfni til fríðinda**
- **Stefnur um hæfni til fríðinda**
- **Hæfnistilvik**

Þú getur skoðað upplýsingarnar á þessum formum í skrifvarnarham. Ef þú vilt breyta upplýsingum, verðurðu fyrst að slökkva á fríðindastjónu (á eingöngu við um umhverfi **Sandkassa**).

## <a name="enable-or-disable-leave-and-absence"></a>Virkja eða afvirkja leyfi og fjarvistir

Til að virkja Leyfi og fjarveru notarðu sama ferli í [Virkja eða afvirkja forskoðunareiginleika](hr-admin-manage-features.md?enable-or-disable-preview-features).

> [!IMPORTANT]
> Ekki er hægt að afvirkja eiginleikann **Margar orlofstegundir** í Leyfi og fjarvistum þegar hann hefur verið virkjaður. Þetta á við um bæði umhverfin **Sandkassi** og **Framleiðsla**.

Frekari upplýsingar um forskoðunareiginleika í leyfum og fjarvistum er að finna í [Forskoðunareiginleikar leyfis og fjarvista](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

## <a name="send-us-feedback"></a>Senda okkur endurgjöf

Við viljum heyra um reynslu þína af forskoðunareiginleikum. Við hvetjum þig til að senda reglulega viðbrögð þín á eftirfarandi vefsvæði þegar þú notar þessar eða einhverjar aðrar eiginleika:

- [Samfélag](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – Þessi síða er frábær auðlind þar sem notendur geta rætt um notkunartilfelli, spyrja spurninga og fá samfélagsaðstoð.
- Láttu okkur vita af eiginleikum sem þú vilt sjá í vörunni eða breytingum sem þér finnst eiga að gera á núverandi eiginleikum. Tillaga að vöruhugmyndum í [Hugmyndir Human Resources](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources).
    
Ekki hafa persónuupplýsingar innifaldar (allar upplýsingar sem þú gætir þekkst á) í athugasemdum þínum eða vöruúrskurðum. Samansafnaðar upplýsingar kunna að vera greindar frekar og verða ekki notaðar til að svara beiðnum samkvæmt gildandi lögum um persónuvernd. Persónuleg gögn sem er safnað sérstaklega með þessum forritum er háð [Yfirlýsing Microsoft um persónuvernd](https://privacy.microsoft.com/privacystatement).

## <a name="see-also"></a>Sjá einnig

- [Hvað er nýtt í Human Resources](hr-admin-whats-new.md)
- [Útgáfuáætlanir Dynamics 365 og Power Platform](https://docs.microsoft.com/dynamics365/release-plans/#pivot=products&panel=products1)