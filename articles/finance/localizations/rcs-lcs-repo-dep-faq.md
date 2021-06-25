---
title: Regulatory Configuration Service (RCS) - Lifecycle Services (LCS) úrelding á geymslu
description: Í þessu efnisatriði er að finna upplýsingar um úreldingu á Microsoft Dynamics Lifecycle Services (LCS) geymslu sem er hluti af áætlun um uppfærslu á altækri geymslu Regulatory Configuration Service (RCS).
author: JaneA07
ms.date: 05/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, LCS storage, LCS storage deprecation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.19
ms.openlocfilehash: abaeb34db1d209fa8e5cc83a98c333f42e91f2d2
ms.sourcegitcommit: 7cda434becd198c1cd405e001289777ae7a24fe1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/01/2021
ms.locfileid: "6127920"
---
# <a name="regulatory-configuration-service-rcs--lifecycle-services-lcs-storage-deprecation"></a>Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) úrelding á geymslu

[!include [banner](../includes/banner.md)]

Verið er að úrelda notkun Microsoft Dynamics Lifecycle Services (LCS) sem gagnageymslu fyrir skilgreiningar rafrænnar skýrslugerðar. Þessi úrelding felur í sér eftirfarandi breytingar:

- Skilgreiningar frá Microsoft sem eru notaðar í forritum Microsoft Dynamics 365 verða ekki lengur gefnar út í samnýtt eignasafn í LCS. Þess í stað verða þær einungis birtar í gegnum altæka geymslu RCS. Hins vegar verða stillingar fyrir Dynamics AX 2012 áfram birtar í samnýttu eignasafni í LCS þar til stuðningstíma fyrir AX 2012 lýkur.
- Aðgerðin sem gerir kleift að hlaða upp skilgrieiningum í eignasafn verks í LCS úr Finance and Operations forritum og frá RCS verður gerð óvirk. Hins vegar verður áfram hægt að nota vafrann í LCS til að hlaða upp skilgreiningum í eignasafn verks. Þar af leiðandi verður enn hægt að bæta skilgreiningum við LCS þannig að þær geti verið með í lausnapökkunum.
- Innflutningur á skilgreiningum úr LCS mun áfram vera í boði og studdur í Finance and Operations forritum og í RCS að svo stöddu. Hins vegar verður virknin að lokum gerð úreld. (Nákvæmur dagur úreldingar verður tilkynntur síðar.)

## <a name="deprecation-notice"></a>Tilkynning um úreldingu

Úrelding á notkun LCS sem geymslu var komið á framfæri í [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Finance - LCS tilkynningu um úreldingu](../get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release). Fyrirhuguð dagsetning úreldingar er 1. apríl 2022.

## <a name="key-features"></a>Lykileiginleikar

- Hægt er að nota RCS til að stofna og breyta skilgreiningum. Síðan er hægt að þrýsta þessum skilgreiningum beint úr hönnuðinum og yfir í tengd forrit. Þar af leiðandi er hægt að breyta og prófa skilgreiningarnar á fljótlegan hátt.
- Altæka geymslan er miðstýrð geymsla fyrir allar skilgreiningar rafrænnar skýrslugerðar.

## <a name="guidance-for-one-time-and-ongoing-actions"></a>Leiðbeiningar fyrir stakar og áframhaldandi aðgerðir

Í þessum hluta er lýst nokkrum skrefum sem þarf að ljúka einu sinni. Þar er einnig lýst skrefum sem þarf í kjölfarið að ljúka með reglulegu millibili.

### <a name="one-time-action"></a>Stök aðgerð

Flytjið inn allar nauðsynlegar skilgreiningar úr LCS til RCS og birtið þær síðan úr RCS í altæku geymsluna. Ef notuð eru eigasöfn tiltekins verks til að geyma afleiddar skilgreiningar í LCS þarf að ljúka eftirfarandi skrefum á meðan enn er hægt að opna LCS.

1. Ef RCS-tilvik er ekki þegar tiltækt skal úthluta einu slíku. Frekari upplýsingar er að finna í [RCS yfirlit](rcs-overview.md).
2. Í úthlutuðu RCS-tilviki, fyrir hvert LCS-verk í eignasafninu sem inniheldur afleiddar skilgreiningar rafrænnar skýrslugerðar, skal skrá tilhlýðilega LCS-geymslu.
3. Flytjið skilgreiningar rafrænnar skýrslugerðar úr LCS-geymslum í RCS. Frekari upplýsingar er að finna í [Flytja inn skilgreiningar úr LCS](../../dev-itpro/analytics/tasks/er-import-configuration-lifecycle-services.md).
4. Ef altæka geymslan er ekki gefin upp sjálfkrafa skal skrá hana í RCS.
5. Hlaðið upp öllum afleiddum skilgreiningum úr núverandi RCS-tilviki í altæku geymsluna. Notið eiginleikann **Skilgreiningapakkar sem gera notanda kleift að hlaða upp öllum skilgreiningum í altæku geymsluna í einni aðgerð** til að hjálpa til við upphleðsluna. Frekari upplýsingar er að finna í [Upphleðsla á altækri geymslu RCS](rcs-global-repo-upload.md).

### <a name="going-forward"></a>Fer áfram

Notið myndræna hönnuði í RCS til að búa til allar nýjar skilgreiningar. Hlaðið síðan upp skilgreiningunum í altæku geymsluna til geymslu. Frekari upplýsingar er að finna í [Stofna skilgreiningu rafrænnar skýrslugerðar í RCS og hlaða upp í altæka geymslu](rcs-global-repo-upload.md).

## <a name="frequently-asked-questions"></a>Algengar spurningar

### <a name="does-this-change-mean-that-lcs-cant-be-used-as-central-storage-for-configurations"></a>Þýðir þessi breyting að ekki sé hægt að nota LCS sem miðlæga geymslu fyrir skilgreiningar?

Já. Aðgerðin sem gerir kleift að hlaða upp skilgrieiningum í eignasafn verks í LCS úr Finance and Operations forritum verður gerð úreld. Hins vegar verður áfram hægt að nota vafrann í LCS til að hlaða upp skilgreiningum í eignasafn verks eftir þörfum.

### <a name="i-thought-that-rcs-was-a-replacement-repository-for-importing-global-template-files-i-didnt-think-that-its-used-to-store-configurations-which-is-correct"></a>Ég hélt að RCS væri varageymsla fyrir innflutning á altækum sniðmátsskrám. Ég hélt að það væri ekki notað til að geyma skilgreiningar. Hvort er rétt?

RCS er hönnunarþjónusta til að búa til og breyta skilgreiningum rafrænnar skýrslugerðar. RCS er með eigin geymslu sem kallast altæka geymslan. Þessi geymsla er notuð til að geyma skilgreiningar sem eru búnar til í RCS. Þegar búið er að úrelda LCS sem geymslu verður altæka geymslan eini upprunastaðurinn fyrir skilgreiningar Microsoft. Ljúka verður stakri aðgerð til að flytja inn allar skilgreiningarnar sem þarf að flytja úr LCS í RCS og síðan birta þær úr RCS í altæku geymslunni.

### <a name="without-lcs-what-is-the-suggested-way-to-store-configurations-so-that-test-and-production-configurations-can-easily-be-managed-and-transferred"></a>Án LCS, hvaða leið er mælt með til að geyma skilgreiningar þannig að auðvelt sé að halda utan um og flytja á milli skilgreiningarnar „próf“ og „framleiðsla“?

RCS notar hugmyndina á bak við *tengt forrit*. Tengt forrit myndar tengingu milli RCS og hvaða tilviks sem er af Finance and Operations forritum. Þar sem hægt er að nota RCS til að breyta skilgreiningum, er hægt að nota tengt forrit til að þrýsta skilgreiningunum beint úr hönnuði og í umhverfi Finance and Operations forrita. Þar af leiðandi er hægt að breyta og prófa skilgreiningarnar á fljótlegan hátt í staðinn fyrir að fara í gegnum geymslu LCS á verkstigi.

### <a name="are-there-any-examples-that-show-the-setup-and-management"></a>Eru einhver dæmi sem sýna uppsetninguna og stjórnunina?

Engin dæmi eru til en hægt er að ljúka skrefunum fyrri í þessu efnisatriði til að flytja skilgreiningarnar í altæka geymslu RCS.
