---
title: Flutningur yfir í fínstillingu skipulagningar fyrir aðaláætlanagerð
description: Í þessu efnisatriði er að finna upplýsingar um nýja aðaláætlunarvélina, fínstillingu skipulagningar og um yfirfærslu úr fyrirliggjandi vél.
author: ChristianRytt
manager: tfehr
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: ''
ms.author: crytt
ms.search.validFrom: 2020-11-05
ms.dyn365.ops.version: ''
ms.openlocfilehash: 94e5668da45c524ed9ab9eef10b40d0fb5336a65
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645997"
---
# <a name="migration-to-planning-optimization-for-master-planning"></a>Flutningur yfir í fínstillingu skipulagningar fyrir aðaláætlanagerð

[!include [banner](../includes/banner.md)]

Áætlað er að innbyggða aðaláætlunarvélin sé úrelduð (úrelt). Verið er að skipta um viðbót fínstillingar skipulagningar fyrir Microsoft Dynamics 365 Supply Chain Management. Í þessu efnisatriði er að finna upplýsingar um áhrif á nýjar og fyrirliggjandi uppsetningar. Þar eru upplýsingar um nauðsynlegar aðgerðir.

Fínstilling skipulagningar greiðir fyrir því að útreikningar aðaláætlanagerðar eigi sér stað kleift að eiga sér stað utan Supply Chain Management og Azure SQL gagnagrunns hennar. Kostirnir við fínstillingu áætlanagerðar eru m.a. bætt afkastageta og minni áhrifum á SQL-gagnagrunninn við keyrslur aðaláætlanagerðar. Vegna þess hægt er að keyra hraða áætlanagerð jafnvel á skrifstofutíma geta skipuleggjendur strax brugðist við eftirspurn eða breytingum á færibreytum.

Frekari upplýsingar um fínstillingu skipulagningar er að finna í [Yfirliti fínstillingar skipulagningar](planning-optimization/planning-optimization-overview.md).

## <a name="obsolescence-of-the-existing-master-planning-engine"></a>Úrelding núverandi aðaláætlunarvélar

Microsoft vinnur við að úrelda innbyggðu aðaláætlunarvélina til að koma að fínstillingu skipulagningar. Þessi breyting hefur áhrif á allt skýjaumhverfi. Hefur ekki áhrif á uppsetningu innanhúss. Í útgáfu 10.0.16 og síðar birtast villuboð ef innbyggð aðaláætlanagerð er keyrð án myndar áætlaðrar framleiðslupantana. Hins vegar verður lokið við keyrslu aðaláætlanagerðar þrátt fyrir villuboðin.

Frekari upplýsingar um úreldingu innbyggðu aðaláætlunarvélarinnar er að finna í tilkynningunum í [Eiginleikar sem hafa verið fjarlægðir eða eru úreltir í Dynamics 365 Supply Chain Management](../get-started/removed-deprecated-features-scm-updates.md).

## <a name="migration-messages-and-exceptions"></a>Flutningur, skilaboð og undantekningar

Eigendur núverandi umhverfa sem keyra innbyggðu aðaláætlunarvélina án þess að búa til áætlaðar framleiðslupantanir, fá tölvupóst með upplýsingum um undantekningarferlið. Við mælum með því að þú vinnir með samstarfsaðila til að meta og leggja drög að flutningnum yfir í Fínstillingu skipulagningar.

Eins og hefur verið getið birtast villuboð í útgáfu 10.0.16 og nýrri útgáfum ef innbyggð aðaláætlanagerð er keyrð án þess að mynda áætlaðar framleiðslupantanir. Þessi villuskilaboð innihalda leiðbeiningar varðandi flutning og leiðbeiningar um hvernig skal biðja um undantekningu.

### <a name="new-deployments"></a>Nýjar uppsetningar

Fínstilling áætlanagerðar ætti að nota sem sjálfgefna aðaláætlunarvél fyrir allar nýjar uppsetningar í skýinu. Almennt ætti að nota fínstillingu skipulagningar fyrir allar nýjar uppsetningar sem búa ekki til áætlaðar framleiðslupantanir meðan á aðaláætlanagerð stendur. Þegar ný uppsetning er háð virkni fínstilling skipulagningar styður ekki eins og stendur, er hægt að biðja um undantekningu þannig að hægt sé að halda áfram að nota innbyggðu aðaláætlunarvélina áfram.

### <a name="existing-deployments"></a>Fyrirliggjandi uppsetningar

Eigendur núverandi uppsetninga í skýi sem eru háðar aðaláætlanagerð ættu að skipuleggja flutning yfir í fínstillingu skipulagningar. Þegar innleiðingin þín er háð virkni sem fínstilling skipulagningar styður ekki eins og er, er hægt að biðja um undantekningu svo hægt sé að halda áfram að nota innbyggðu aðaláætlunarvélina.

Microsoft sendir tölvupóst til stjórnenda umhverfa sem notar aðaláætlanagerð sem verið er að úrelta. Slíkur tölvupóstur inniheldur upplýsingar um áskildar aðgerðir við flutning eða upplýsingar um hvernig beðið er um undantekningu.

## <a name="the-exception-process"></a>Ferli undantekningar

Hægt er að biðja um undantekningu ef nauðsynlegt er að halda þarf áfram að nota innbyggðu aðaláætlunarvélina vegna þess að viðskiptaferli eru afar háð a.m.k. einum eiginleika sem er ekki virkjaður í fínstillingu áætlanagerðar eins og er. Listi yfir tiltæka eiginleika er að finna í [Samræmisgreining á fínstillingu áætlanagerðar](planning-optimization/planning-optimization-fit-analysis.md).

Í augnablikinu eiga undantekningar frá flutningi fínstillingar áætlanagerðar einungis við ef aðaláætlunarferlið inniheldur ekki framleiðslu (þ.e. áætlaðar framleiðslupantanir sem eru myndaðar af aðaláætlanagerð) og þörf er á að nota innbyggðu aðaláætlunarvélina fram yfir útgáfu 10.0.15.

Um leið og áskildir eiginleikar verða tiltækir veitir Microsoft reynslutíma þar til undantekningin rennur út. Stjórnandi umhverfisins fær upplýsingar um hvenær áskildir eiginleikar eru tiltækir og þegar reynslutíminn hefst.

> [!NOTE]
> Aðeins er hægt að biðja um undantekningu fyrir vinnsluumhverfi, ekki fyrir sandkassaumhverfi. Þegar þörf er á að slökkva á undantekningarvillu fínstillingar skipulagningar í innviðum sem þjónusta (IaaS) í sandkassaumhverfi skal keyra SQL-fyrirspurnina sem er til staðar í [Sandkassaumhverfum](#faq-sandbox).

## <a name="frequently-asked-questions"></a>Algengar spurningar

### <a name="sandbox-environments"></a><a name="faq-sandbox"></a>Sandkassaumhverfi

Get ég notað innbyggðan aðaláætlanagerð í sandkassaumhverfinu mínu? Þarf ég undantekningu?

**Svar:** Undantekningar eiga yfirleitt ekki við um sandkassaumhverfi vegna þess að undantekningarvilla fínstillingar skipulagningar kemur ekki í veg fyrir að innbyggða aðaláætlunarvélin keyri á réttan hátt. Hins vegar þegar villuboðin trufla notanda er hægt að slökkva á boðunum í IaaS-sandkassaumhverfi (ekki Service Fabric) með því að keyra eftirfarandi fyrirspurn í gagnagrunninum:

```sql
-- Insert or update an enabled flight:
DECLARE @flightName NVARCHAR(100) = 'ReqPlanningOptimizationExceptionToggle';
IF NOT EXISTS (SELECT TOP 1 1 FROM SysFlighting WHERE flightName = @flightName)
    INSERT INTO SYSFLIGHTING(FLIGHTNAME,ENABLED, FLIGHTSERVICEID,PARTITION)
    SELECT @flightName, 1, 12719367,RECID FROM DBO.[PARTITIONS];
ELSE
    UPDATE SysFlighting SET enabled = 1, flightServiceId = 12719367 WHERE flightName = @flightName;
```

### <a name="on-premises-environments"></a>Umhverfi á staðnum

Umhverfið mitt er á staðnum. Þarf ég undantekningu?

**Svar:** Nei Undantekning er ekki nauðsynleg fyrir umhverfi á staðnum. Þú getur haldið áfram að nota innbyggðu aðaláætlanagerðina. Stjórnandi umhverfisins fær upplýsingar um ef einhverra aðgerða er þörf.

### <a name="production-scenarios"></a>Framleiðsluaðstæður

Við notum áætlaðar framleiðslupantanir en ég hef áhyggjur af því hvað gerist þegar við uppfærðum í útgáfu 10.0.16. Ætti ég að grípa til aðgerða?

**Svar:** Þú ættir ekki að hafa áhyggjur af þessu. Hægt er að halda áfram að nota innbyggða aðaláætlanagerð í útgáfu 10.0.16. Hins vegar er ráðlegt að meta hvort flutningur yfir í fínstillingu skipulagningar geti hafist með núverandi virkni. Einnig er ráðlegt að kynna sér nýju virknina til hlítar.

### <a name="email-from-microsoft"></a>Tölvupóstur frá Microsoft

Stjórnandi umhverfis okkar fékk tölvupóst frá Microsoft. Í tölvupóstinum segir að yfirfæra ætti í fínstillingu skipulagningar eða biðja um undantekningu. Þarf ég að grípa til aðgerða?

**Svar:** Já Þú verður að fylgja leiðbeiningunum í tölvupóstinum, að öðrum kosti verður umhverfið þitt fyrir áhrifum. Þú getur annað hvort flutt yfir í fínstillingu skipulagningar á tilgreindum degi að beðið um undantekningu með því að nota tengilinn í tölvupóstinum. Þessi tengill opnar spurningalista. Eftir að þú hefur lokið við og sent inn þennan spurningalista muntu fá svar með tölvupósti. Þrátt fyrir að þetta ferli sé handvirkt reynir Microsoft að svara innan viku eftir að spurningalistinn er sendur.

### <a name="error-messages"></a>Villuboð

Ég nota útgáfu 10.0.16 eða nýrri og ég fæ eftirfarandi villuboð þegar aðaláætlanagerð er keyrð. Er aðaláætlanagerð lokuð?

> Þú færð þessi villuskilaboð vegna þess að innbyggð aðaláætlunarvél var notuð fyrir aðstæður sem eru studdar fínstillingu skipulagningar. Þú ættir að flytja þig yfir í fínstillingu skipulagningar núna, þar sem núverandi aðaláætlanagerð verður úrelt. Athugaðu að þessi áætlanakeyrsla var keyrð.
>
> Ef flutningurinn þinn inniheldur sterk tengsl um eiginleika sem bíða er hægt að biðja um undantekningu á áframhaldandi notkun á vél fyrir innbyggðri aðaláætlunarvél.
>
> Ljúktu við eftirfarandi spurningalista til að hefjast handa og, ef svo á við, biddu um undantekningu frá yfirfærslu í fínstillingu skipulagningar.

**Svar:** Nei, Aðaláætlanagerð er ekki læst. Keyrslu aðaláætlanagerðarinnar lauk á réttan hátt og þú getur notað niðurstöðurnar á hefðbundinn hátt. Hins vegar, til að forðast að fá þessi villuboð við síðari aðaláætlunarkeyrslur, verður að flytja yfir í fínstillingu áætlanagerðar strax eða biðja um undantekningu með því að nota tengilinn í villuboðunum.
