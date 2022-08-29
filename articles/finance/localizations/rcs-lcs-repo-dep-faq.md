---
title: Regulatory Configuration Service (RCS) - Lifecycle Services (LCS) úrelding á geymslu
description: Þessi grein veitir upplýsingar um afskrift Microsoft Dynamics Lifecycle Services (LCS) geymsla sem er fyrirhuguð sem hluti af útfærslu á Regulatory Configuration Service (RCS) alþjóðlegu geymslunni.
author: kfend
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.19
ms.custom: 97423
ms.assetid: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, LCS storage, LCS storage deprecation
ms.openlocfilehash: 717a2b9b00e137631a7cb9a188bdcf1b33e6af02
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277215"
---
# <a name="regulatory-configuration-service-rcs--lifecycle-services-lcs-storage-deprecation"></a>Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) úrelding á geymslu

[!include [banner](../includes/banner.md)]

Verið er að úrelda notkun Microsoft Dynamics Lifecycle Services (LCS) sem gagnageymslu fyrir skilgreiningar rafrænnar skýrslugerðar. Þessi úrelding felur í sér eftirfarandi breytingar:

- Skilgreiningar frá Microsoft sem eru notaðar í forritum Microsoft Dynamics 365 verða ekki lengur gefnar út í samnýtt eignasafn í LCS. Þess í stað verða þær einungis birtar í gegnum altæka geymslu RCS. Hins vegar verða stillingar fyrir Dynamics AX 2012 áfram birtar í samnýttu eignasafni í LCS þar til stuðningstíma fyrir AX 2012 lýkur.
- Virknin sem gerir þér kleift að hlaða upp stillingum í Project eignasafnið í LCS frá fjármála- og rekstrarforritum og frá RCS, verður óvirkjuð. Hins vegar verður áfram hægt að nota vafrann í LCS til að hlaða upp skilgreiningum í eignasafn verks. Þar af leiðandi verður enn hægt að bæta skilgreiningum við LCS þannig að þær geti verið með í lausnapökkunum.
- Innflutningur á stillingum frá LCS verður áfram tiltækur og studdur í fjármála- og rekstraröppum, og í RCS, um nokkurt skeið. Hins vegar verður virknin að lokum gerð úreld. (Nákvæmur dagur úreldingar verður tilkynntur síðar.)

## <a name="deprecation-notice"></a>Tilkynning um úreldingu

Frávísun á notkun LCS sem geymslu var tilkynnt í [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Finance - LCS úreldingartilkynning](../get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release). Fyrirhuguð dagsetning úreldingar er 1. apríl 2022.

## <a name="key-features"></a>Lykileiginleikar

- Notaðu RCS til að búa til og breyta ER-skilgreiningum og altækum eiginleikum.
- Ýttu stillingum beint frá RCS hönnuði yfir í tengt forrit, eins og Dynamics 365 Finance umhverfi, svo að þú getir fljótt gert og prófað breytingar á stillingum þínum.
- Geymdu, deildu og hafðu umsjón með stuðningstímanum miðlægt fyrir bæði skilgreiningar rafrænnar skýrslugerðar og altæka eiginleika í gegnum altæka miðlæga geymslu.

## <a name="guidance-for-one-time-and-ongoing-actions"></a>Leiðbeiningar fyrir stakar og áframhaldandi aðgerðir

Í þessum hluta er lýst nokkrum skrefum sem þarf að ljúka einu sinni. Þar er einnig lýst skrefum sem þarf í kjölfarið að ljúka með reglulegu millibili.

### <a name="one-time-action"></a>Stök aðgerð

Flytjið inn allar nauðsynlegar skilgreiningar úr LCS til RCS og birtið þær síðan úr RCS í altæku geymsluna. Ef notuð eru eigasöfn tiltekins verks til að geyma afleiddar skilgreiningar í LCS þarf að ljúka eftirfarandi skrefum á meðan enn er hægt að opna LCS.

1. Ef RCS-tilvik er ekki þegar tiltækt skal úthluta einu slíku. Frekari upplýsingar er að finna í [RCS yfirlit](rcs-overview.md).
2. Í úthlutuðu RCS-tilviki, fyrir hvert LCS-verk í eignasafninu sem inniheldur afleiddar skilgreiningar rafrænnar skýrslugerðar, skal skrá tilhlýðilega LCS-geymslu.
3. Flytjið skilgreiningar rafrænnar skýrslugerðar úr LCS-geymslum í RCS. Frekari upplýsingar er að finna í [Flytja inn skilgreiningar úr LCS](/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-import-configuration-lifecycle-services).
4. Ef altæka geymslan er ekki gefin upp sjálfkrafa skal skrá hana í RCS.
5. Hlaðið upp öllum afleiddum skilgreiningum úr núverandi RCS-tilviki í altæku geymsluna. Notaðu eiginleikann **Skilgreiningapakkar** til að hjálpa til við upphleðsluna. Frekari upplýsingar er að finna í [Upphleðsla á altækri geymslu RCS](rcs-global-repo-upload.md).

### <a name="going-forward"></a>Fer áfram

Notaðu myndræna hönnuði í RCS í eftirfarandi tilgangi:

- Stækkaðu sniðmátin sem Microsoft útvegar.
- Búðu til nýjar skilgreiningar sem fyrirtækið þitt krefst.
- Sérstilltu altæka eiginleika fyrir rafræna reikningsfærslu og skattaútreikningsþjónustu.

Notaðu altæka gagnageymslu í eftirfarandi tilgangi:

- Fáðu aðgang að skilgreiningum og altækum eiginleikum framleiddum af Microsoft.
- Hladdu upp skilgreiningum sem þú bjóst til eða stækkaðir í altæku geymsluna til vistunar og deildu þeim í forritsumhverfum Dynamics 365 í fyrirtækinu eða með ytri fyrirtækjum. Frekari upplýsingar er að finna í [Stofna skilgreiningu rafrænnar skýrslugerðar í RCS og hlaða upp í altæka geymslu](rcs-global-repo-upload.md).

## <a name="frequently-asked-questions"></a>Algengar spurningar

### <a name="does-this-change-mean-that-lcs-cant-be-used-as-central-storage-for-configurations"></a>Þýðir þessi breyting að ekki sé hægt að nota LCS sem miðlæga geymslu fyrir skilgreiningar?

Já. Aðgerðin sem gerir þér kleift að hlaða upp stillingum í verkefnasafnið í LCS frá fjármála- og rekstrarforritum verður úrelt. Hins vegar verður áfram hægt að nota vafrann í LCS til að hlaða upp skilgreiningum í eignasafn verks eftir þörfum.

### <a name="i-thought-that-rcs-was-a-replacement-repository-for-importing-global-template-files-i-didnt-think-that-its-used-to-store-configurations-which-is-correct"></a>Ég hélt að RCS væri varageymsla fyrir innflutning á altækum sniðmátsskrám. Ég hélt að það væri ekki notað til að geyma skilgreiningar. Hvort er rétt?

RCS er hönnunarþjónusta til að búa til og breyta skilgreiningum rafrænnar skýrslugerðar. RCS er með eigin geymslu sem kallast altæka geymslan. Þessi geymsla er notuð til að geyma skilgreiningar sem eru búnar til í RCS. Þegar búið er að úrelda LCS sem geymslu verður altæka geymslan eini upprunastaðurinn fyrir skilgreiningar Microsoft. Ljúka verður stakri aðgerð til að flytja inn allar skilgreiningarnar sem þarf að flytja úr LCS í RCS og síðan birta þær úr RCS í altæku geymslunni.

### <a name="without-lcs-what-is-the-suggested-way-to-store-configurations-so-that-test-and-production-configurations-can-easily-be-managed-and-transferred"></a>Án LCS, hvaða leið er mælt með til að geyma skilgreiningar þannig að auðvelt sé að halda utan um og flytja á milli skilgreiningarnar „próf“ og „framleiðsla“?

RCS notar hugmyndina á bak við *tengt forrit*. Tengd umsókn myndar tengingu á milli RCS og hvers kyns tilviks fjármála- og rekstrarappa. Vegna þess að hægt er að nota RCS til að breyta stillingum, er hægt að nota tengda forritið til að ýta stillingunum beint frá hönnuðinum yfir í umhverfi fyrir fjármála- og rekstrarforrit. Þar af leiðandi er hægt að breyta og prófa skilgreiningarnar á fljótlegan hátt í staðinn fyrir að fara í gegnum geymslu LCS á verkstigi.

### <a name="are-there-any-examples-that-show-the-setup-and-management"></a>Eru einhver dæmi sem sýna uppsetninguna og stjórnunina?

Það eru engin dæmi, en þú getur lokið skrefunum fyrr í þessari grein til að flytja stillingarnar þínar yfir í RCS Global geymsluna.

### <a name="is-rcs-a-prerequisite-to-configure-electronic-reporting"></a>Er RCS skilyrði til að stilla rafræna skýrslugerð?

Já. RCS inniheldur möguleika sem styðja við uppsetningu á altækum eiginleikum sem eru notaðir af altækum þjónustum eins og rafrænni reikningsfærslu og skattaútreikningsþjónustu. Þjónustan hefur hinsvegar sömu myndrænu virkni sem gerir þér kleift að stækka eða búa til nýjar skilgreiningar rafrænnar skýrslugerðar. RCS býður einnig upp á umsjón með stuðningstíma fyrir bæði skilgreiningar rafrænnar skýrslugerðar og altæka eiginleika.

### <a name="which-regions-can-rcs-be-deployed-in"></a>Á hvaða svæðum er hægt að nota RCS?

RCS er fáanlegt á eftirfarandi Azure-svæðum:

- Bandaríkin
- Indland
- Frakkland
- Evrópa

Frekari upplýsingar um stuðning við afurð er að finna í [Yfirlit yfir altæka þjónustu Dynamics](globalization-services-overview.md). Upplýsingar um landfræðilegan stuðning er að finna í [Dynamics 365 og Power Platform: Aðgengileiki, staðsetning gagna, tungumál og staðfærsla](https://aka.ms/rcs/D365Productavailabilityguide).

### <a name="whats-the-cost-of-using-rcs"></a>Hvað kostar að nota RCS?

RCS og hnattvæðingargeymslan eru veitt ókeypis sem hluti af núverandi leyfum fyrir fjármála- og rekstrarforrit. Enginn sérstakur kostnaður tengist því að nota þjónustu RCS-hönnunar eða geyma skilgreiningar í altæku geymslunni. Engin takmörk eru á fjölda skilgreininga eða tengdra forrita eins og er.
