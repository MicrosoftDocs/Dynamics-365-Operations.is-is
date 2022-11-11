---
title: Flutningur yfir í fínstillingu skipulagningar fyrir aðaláætlanagerð
description: Þessi grein veitir upplýsingar um nýju aðalskipulagsvélina, Áætlanagerð fínstillingu, og um flutning frá núverandi vél.
author: t-benebo
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: ''
ms.author: benebotg
ms.search.validFrom: 2020-11-05
ms.dyn365.ops.version: ''
ms.openlocfilehash: dbbc58f0dcd833f63e84a73ac68ada60bd0c291d
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739952"
---
# <a name="migration-to-planning-optimization-for-master-planning"></a>Flutningur yfir í fínstillingu skipulagningar fyrir aðaláætlanagerð

[!include [banner](../includes/banner.md)]

Áætlað er að innbyggða aðaláætlunarvélin sé úrelduð (úrelt). Verið er að skipta um viðbót fínstillingar skipulagningar fyrir Microsoft Dynamics 365 Supply Chain Management. Þessi grein veitir upplýsingar um áhrifin á nýja og núverandi uppsetningu. Þar eru upplýsingar um nauðsynlegar aðgerðir.

Fínstilling skipulagningar greiðir fyrir því að útreikningar aðaláætlanagerðar eigi sér stað kleift að eiga sér stað utan Supply Chain Management og Azure SQL gagnagrunns hennar. Kostirnir við fínstillingu áætlanagerðar eru m.a. bætt afkastageta og minni áhrifum á SQL-gagnagrunninn við keyrslur aðaláætlanagerðar. Vegna þess hægt er að keyra hraða áætlanagerð jafnvel á skrifstofutíma geta skipuleggjendur strax brugðist við eftirspurn eða breytingum á færibreytum.

Fyrir frekari upplýsingar um hagræðingu skipulags, sjá [Aðalskipulagskerfisarkitektúr](master-planning-architecture.md).

## <a name="obsolescence-of-the-existing-master-planning-engine"></a>Úrelding núverandi aðaláætlunarvélar

Microsoft er í því ferli að gera úreltu aðalskipulagsvélina úrelta í þágu skipulagsfínstillingar. Þessi breyting hefur áhrif á allt skýjaumhverfi. Hefur ekki áhrif á uppsetningu innanhúss. Í útgáfu 10.0.16 og síðar færðu villuboð ef þú keyrir úrelta aðalskipulagsvél án þess að búa til fyrirhugaðar framleiðslupantanir. Hins vegar verður lokið við keyrslu aðaláætlanagerðar þrátt fyrir villuboðin.

Fyrir frekari upplýsingar um úrelda aðalskipulagsvélina, sjá tilkynningar í [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Supply Chain Management](../get-started/removed-deprecated-features-scm-updates.md).

## <a name="migration-messages-and-exceptions"></a>Flutningur, skilaboð og undantekningar

Eigendur núverandi umhverfis sem keyra úreltu aðalskipulagsvélina án þess að búa til fyrirhugaðar framleiðslupantanir munu fá tölvupóst sem veitir upplýsingar um undantekningarferlið. Við mælum með því að þú vinnir með samstarfsaðila til að meta og leggja drög að flutningnum yfir í Fínstillingu skipulagningar.

Eins og fram hefur komið færðu villuboð í útgáfu 10.0.16 og síðar ef þú keyrir úrelta aðalskipulagsvél án þess að búa til áætlaðar framleiðslupantanir. Þessi villuskilaboð innihalda leiðbeiningar varðandi flutning og leiðbeiningar um hvernig skal biðja um undantekningu.

### <a name="new-deployments"></a>Nýjar uppsetningar

Áætlanagerð fínstilling verður að teljast sjálfgefin aðalskipulagsvél fyrir allar nýjar dreifingar í skýinu. Almennt ætti að nota fínstillingu skipulagningar fyrir allar nýjar uppsetningar sem búa ekki til áætlaðar framleiðslupantanir meðan á aðaláætlanagerð stendur. Ef ný uppsetning er háð virkni sem áætlanagerð fínstilling styður ekki eins og er, geturðu beðið um undanþágu svo þú getir haldið áfram að nota úreltu aðalskipulagsvélina.

### <a name="existing-deployments"></a>Fyrirliggjandi uppsetningar

Eigendur núverandi uppsetninga í skýi sem eru háðar aðaláætlanagerð ættu að skipuleggja flutning yfir í fínstillingu skipulagningar. Ef útfærslan þín veltur á virkni sem áætlanagerð fínstilling styður ekki eins og er, geturðu beðið um undantekningu svo þú getir haldið áfram að nota úreltu aðalskipulagsvélina.

Microsoft sendir tölvupóst til stjórnenda umhverfa sem notar aðaláætlanagerð sem verið er að úrelta. Slíkur tölvupóstur inniheldur upplýsingar um áskildar aðgerðir við flutning eða upplýsingar um hvernig beðið er um undantekningu.

## <a name="the-exception-process"></a>Ferli undantekningar

Þú getur beðið um undanþágu ef þú verður að halda áfram að nota úreltu aðalskipulagsvélina vegna þess að viðskiptaferlar þínir eru mjög háðir að minnsta kosti einum eiginleika sem er ekki innleiddur í áætlanagerð fínstillingu. Listi yfir tiltæka eiginleika er að finna í [Samræmisgreining á fínstillingu áætlanagerðar](planning-optimization/planning-optimization-fit-analysis.md).

Eins og er, eru undantekningar fyrir flutning áætlunarfínstillingar aðeins viðeigandi ef aðalskipulagsferlið þitt inniheldur ekki framleiðslu (þ.e. fyrirhugaðar framleiðslupantanir sem eru búnar til með aðalskipulagningu) og þú þarfnast úreldu aðalskipulagsvélarinnar umfram útgáfu 10.0.15.

Um leið og áskildir eiginleikar verða tiltækir veitir Microsoft reynslutíma þar til undantekningin rennur út. Stjórnandi umhverfisins fær upplýsingar um hvenær áskildir eiginleikar eru tiltækir og þegar reynslutíminn hefst.

Eftirfarandi flæðirit tekur saman upplýsingarnar sem gefnar eru upp í þessari grein svo þú getir fljótt komist að því hvort þú ættir að biðja um undanþágu. Ef óska þarf eftir undanþágu skal fylla út og senda inn [Fínstilling áætlanagerðar, yfirfærsla og spurningalisti undantekningar](https://go.microsoft.com/fwlink/?linkid=2144962). Vöruflokkurinn ber ábyrgð á því að meta og samþykkja hverja undantekningarbeiðni, svo vinsamlegast sendu beiðni þína beint til vöruhópsins með því að nota tengilinn sem gefinn er upp og ekki búa til stuðningsmiða fyrir hana. Ef beiðni þinni er hafnað skaltu ekki búa til stuðningsmiða því Microsoft Support getur ekki endurmetið eða veitt undanþágur.

![Flæðirit undantekningar.](media/exception-diagram.png "Flæðirit undantekningar")

> [!NOTE]
> Einungis er hægt að óska eftir undanþágu fyrir leigjendur sem eru með eða munu vera með vinnsluumhverfi, ekki fyrir leigjendur með eingöngu sandkassaumhverfi. Þegar þörf er á að slökkva á undantekningarvillu fínstillingar skipulagningar í innviðum sem þjónusta (IaaS) í sandkassaumhverfi skal keyra SQL-fyrirspurnina sem er til staðar í [Sandkassaumhverfum](#faq-sandbox).

## <a name="frequently-asked-questions"></a>Algengar spurningar

### <a name="sandbox-environments"></a><a name="faq-sandbox"></a>Sandkassaumhverfi

Get ég notað úreltu aðalskipulagsvélina í sandkassaumhverfinu mínu? Þarf ég undantekningu?

**Svar:** Undantekningar eru venjulega ekki viðeigandi fyrir sandkassaumhverfi vegna þess að undantekningarvillan í skipulagsfínstillingu kemur ekki í veg fyrir að úrelta aðalskipulagsvélin gangi vel. Hins vegar þegar villuboðin trufla notanda er hægt að slökkva á boðunum í IaaS-sandkassaumhverfi (ekki Service Fabric) með því að keyra eftirfarandi fyrirspurn í gagnagrunninum:

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

**Svar:** Nei Undantekning er ekki nauðsynleg fyrir umhverfi á staðnum. Þú getur haldið áfram að nota úreltu aðalskipulagsvélina. Stjórnandi umhverfisins fær upplýsingar um ef einhverra aðgerða er þörf.

### <a name="production-scenarios"></a>Framleiðsluaðstæður

Við notum áætlaðar framleiðslupantanir en ég hef áhyggjur af því hvað gerist þegar við uppfærðum í útgáfu 10.0.16. Ætti ég að grípa til aðgerða?

**Svar:** Þú ættir ekki að hafa áhyggjur af þessu. Þú getur haldið áfram að nota úreltu aðalskipulagsvélina í útgáfu 10.0.16. Hins vegar er ráðlegt að meta hvort flutningur yfir í fínstillingu skipulagningar geti hafist með núverandi virkni. Einnig er ráðlegt að kynna sér nýju virknina til hlítar.

### <a name="email-from-microsoft"></a>Tölvupóstur frá Microsoft

Stjórnandi umhverfis okkar fékk tölvupóst frá Microsoft. Í tölvupóstinum segir að yfirfæra ætti í fínstillingu skipulagningar eða biðja um undantekningu. Þarf ég að grípa til aðgerða?

**Svar:** Já Þú verður að fylgja leiðbeiningunum í tölvupóstinum, að öðrum kosti verður umhverfið þitt fyrir áhrifum. Þú getur annað hvort flutt yfir í fínstillingu skipulagningar á tilgreindum degi að beðið um undantekningu með því að nota tengilinn í tölvupóstinum. Þessi tengill opnar spurningalista. Eftir að þú hefur lokið við og sent inn þennan spurningalista muntu fá svar með tölvupósti. Þrátt fyrir að þetta ferli sé handvirkt reynir Microsoft að svara innan viku eftir að spurningalistinn er sendur.

### <a name="error-messages"></a>Villuboð

Ég nota útgáfu 10.0.16 eða nýrri og ég fæ eftirfarandi villuboð þegar aðaláætlanagerð er keyrð. Er aðaláætlanagerð lokuð?

> Þú færð þessi villuboð vegna þess að úrelta aðalskipulagsvélin var notuð fyrir aðstæður sem studdar eru af áætlanagerð fínstillingu. Þú ættir að flytja yfir í áætlanagerð fínstillingu núna, þar sem innbyggða aðalskipulagsvélin hefur verið úrelt. Athugaðu að þessi áætlanakeyrsla var keyrð.
>
> Ef flutningur þinn er mjög háður eiginleikum í bið er hægt að biðja um undantekningu frá áframhaldandi notkun á úreltu aðalskipulagsvélinni.
>
> Ljúktu við eftirfarandi spurningalista til að hefjast handa og, ef svo á við, biddu um undantekningu frá yfirfærslu í fínstillingu skipulagningar.

**Svar:** Nei, Aðaláætlanagerð er ekki læst. Keyrslu aðaláætlanagerðarinnar lauk á réttan hátt og þú getur notað niðurstöðurnar á hefðbundinn hátt. Hins vegar, til að forðast að fá þessi villuboð við síðari aðaláætlunarkeyrslur, verður að flytja yfir í fínstillingu áætlanagerðar strax eða biðja um undantekningu með því að nota tengilinn í villuboðunum.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
