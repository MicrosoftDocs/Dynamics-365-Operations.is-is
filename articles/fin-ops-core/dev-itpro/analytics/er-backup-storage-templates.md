---
title: Afritunargeymsla ER-sniðmáta
description: Þetta efni útskýrir hvernig á að nota varabúnaðargeymslu rafrænnar skýrslugerðar (ER) til að endurheimta sniðmát.
author: NickSelin
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 27621
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-08-13
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 932ba44b4223bf9c9d93ffb19e17f6e57bb303b5
ms.sourcegitcommit: bbb64b3475eef155b3f9d1bdc440545da8a7182f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/04/2019
ms.locfileid: "2553092"
---
# <a name="backup-storage-of-er-templates"></a>Afritunargeymsla ER-sniðmáta

[!include [banner](../includes/banner.md)]

[Rammi rafrænnar skýrslugerðar (ER)](general-electronic-reporting.md) gerir fyrirtækjanotendum kleift að skilgreina snið fyrir skjöl á útleið í samræmi við lagaskilyrði mismunandi landa og svæða. Stillt ER-snið geta notað fyrirfram skilgreind sniðmát til að búa til útgönguskjöl á ýmsum sniðum, svo sem Microsoft Excel vinnubækur, Microsoft Word skjöl, eða PDF-skjöl. Sniðmátin eru fyllt með gögnum sem skilgreint gagnaflæði fyrir mynduð skjöl krefst.

Hægt er að birta hvert skilgreint snið sem hluta af ER-lausn. Hægt er að flytja út allar lausnir frá einu tilviki Finance and Operations og flytja inn í annað tilvik.

ER-ramminn notar [Ramma skjalastjórnunar](../../fin-ops/organization-administration/configure-document-management.md) til að geyma nauðsynleg sniðmát fyrir núverandi tilviki Finance and Operations. Það fer eftir stillingum ER-ramma, Microsoft Azure Blob-geymslu eða Microsoft SharePoint hvort hægt er að velja möppu sem aðal geymslupláss fyrir sniðmát. (Sjá frekari upplýsingar [Stilla ER ramma](electronic-reporting-er-configure-parameters.md).) DocuValue taflan hefur einstaka skrá fyrir hvert sniðmát. Í hverri skrá geymir reiturinn **AccessInformation** slóð sniðmátaskrár sem er staðsett á skilgreindum geymslustað.

Þegar þú hefur umsjón með tilvikum Finance and Operations gætirðu ákveðið að flytja núverandi tilvik yfir á annan stað. Til dæmis gætirðu flutt framleiðslutilvikið í nýtt sandkassaumhverfi. Ef þú stillir ER-ramma til að geyma sniðmát í Blob-geymslu, vísar DocuValue-taflan í nýja sandkassaumhverfi til tilviks Blob-geymslu í framleiðsluumhverfi. Hins vegar er ekki hægt að fá aðgang að þessu tilviki úr sandkassanumhverfinu, vegna þess að flutningsferlið styður ekki flutning á gripum í Blob-geymslu. Þess vegna, ef þú reynir að keyra ER-snið sem notar sniðmát til að búa til viðskiptaskjöl, kemur undantekning fyrir, og þér er tilkynnt um það sniðmát sem vantar. Þér er einnig leiðbeint um að nota ER-hreinsunartólið til að eyða og flytja síðan aftur upp skilgreiningu ER-sniðsins sem inniheldur sniðmátið. Vegna þess að þú gætir haft nokkrar stillingar á ER-sniði, getur þetta ferli verið tímafrekt.

Afritunargeymsla ER-sniðmátsaðgerðar getur hjálpað þér að búa til sniðmát þannig að þau eru alltaf tiltæk til að búa til viðskiptaskjöl.

> [!NOTE]
> Þessa aðgerð er aðeins hægt að nota þegar Blob geymsla hefur verið valin sem raunverulegt geymslupláss fyrir ER sniðmát.

Fyrir þennan möguleika er hvert sniðmát nýrrar stillingar ER snið í núverandi umhverfi sjálfkrafa vistað á afritunargeymsluplássi fyrir sniðmát (ERDocuDatabaseStorage gagnagrunnstaflan) þegar eftirfarandi tilvik eiga sér stað:

- Þú flytur inn nýja ER snið stillingu sem inniheldur sniðmát.
- Þú klárar drög að útgáfu ER sniðstillingar sem inniheldur sniðmát.

Afritun af sniðmátum er flutt yfir í nýtt tilvik Finance and Operations sem hluti af gagnagrunninum.

Ef sniðmáts með ER sniði er krafist til að búa til skjöl á útleið, til að vinna úr greiðslum lánardrottins, þ.m.t. myndun greiðsluráðgjafar og eftirlitsskýrslna, til dæmis, en nauðsynleg sniðmát er ekki að finna á aðalgeymslustaðnum, gerast eftirfarandi tilvik:

- Ef sniðmátið er tiltækt á öryggisafritunargeymslunni er það sjálfkrafa tekið af afritunargeymslustaðnum, endurheimt á aðalgeymsluplássið og notað fyrir núverandi framkvæmd.
- Sérhverjum notanda sem er úthlutað á hlutverkið **Þróunaraðili rafrænnar skýrslulausnar** eða **Kerfisstjóri** er tilkynnt um sniðmátið sem vantar í gegnum aðgerðarstöðina. Skilaboðin sem birtast eru háð gildi færibreytunnar **Keyra ferlið sjálfkrafa til að endurheimta brotin sniðmát í runu**:

    - Ef þessi færibreyta er stillt á **Slökkt** mæla skilaboðin með því að þú hefjir runuferlið til að laga sjálfkrafa svipuð vandamál fyrir önnur ER-sniðmát fyrir skilgreiningarsnið. Skilaboðin innihalda tengil sem þú getur notað til að hefja runuferlið.
    - Ef þessi færibreyta er stillt á **Kveikt** tilkynna skilaboðin þér að uppgötvast hafi vandamál vegna sniðmáts sem vantar og að ný runuvinnsla, **Endurheimta biluð sniðmát úr innri afritun gagnagrunnsins**, hefur sjálfkrafa verið áætluð. Þessi runuvinnsla mun sjálfkrafa laga svipuð vandamál fyrir önnur sniðmát.

Til að setja upp færibreytuna **Keyra ferlið sjálfkrafa til að endurheimta brotin sniðmát í runu** skal ljúka eftirfarandi skrefum:

1. Í Finance and Operations skal opna **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Skilgreiningarsíða**.
2. Á síðunni **Skilgreiningar**, í aðgerðarúðunni, í flipanum **Skilgreiningar**, í flokknum **Ítarlegar stillingar**, skal velja **Færibreytur notanda**.
3. Í valmyndinni **Færibreytur notanda** stillirðu nauðsynleg gildi fyrir færibreytuna **Keyra ferlið sjálfkrafa til að endurheimta brotin sniðmát í runu**.

> [!NOTE]
> Þessi færibreyta er skilgreind sem notandi forrita og skráð sem fyrirtækjasértæk.

![Skilgreiningarsíða í ER](./media/GER-BackupTemplates-1.png)

Eftirfarandi mynd sýnir dæmi um skilaboðin sem birtast þegar færibreytan **Keyra ferlið sjálfkrafa til að endurheimta brotin sniðmát í runu** er stillt á **Kveikt**.

![Greiðslubókarsíða lánardrottins](./media/GER-BackupTemplates-2.png)

Eftirfarandi mynd sýnir runuvinnsluna **Endurheimta biluð sniðmát úr innri afritun gagnagrunnsins** á síðunni **Runuvinnsla**.

![Síða runuvinnslu](./media/GER-BackupTemplates-3.png)

Framkvæmdaskrá yfir lokna runuvinnslu **Endurheimta biluð sniðmát úr innri afritun gagnagrunnsins** inniheldur upplýsingar um sniðmát sem hafa verið endurheimt frá varabúnaðargeymslustað yfir á aðalgeymslustað.

![Síða runuvinnslusögu](./media/GER-BackupTemplates-4.png)

Sjálfgefið er að kveikt er á ferlinu við að búa sjálfkrafa til afrit af sniðmátum sem búa í skilgreiningum á ER-sniðmátum. Til að hætta að taka afrit af sniðmátum stillirðu valkostinn **Hætta að gera afrit af sniðmáti** á **Já** á flipanum **Viðhengi** á síðunni **Rafrænar breytur**. Hægt er að opna þessa síðu úr vinnusvæðinu **Rafræn skýrslugerð**.

Ef þú stillir valkostinn **Hætta að búa til afrit af sniðmátum** á **Já** og vilt ekki geyma afrit sem áður voru gerð af sniðmátum skaltu velja **Hreinsa upp afritunargeymslu** á síðunni **Rafrænar skýrslufæribreytur**.

Ef þú uppfærðir umhverfi þitt í Finance and Operations útgáfu 10.0.5 (október 2019) og vilt flytja yfir í nýtt umhverfi sem inniheldur skilgreiningar ER-sniðmáta sem hægt er að keyra skaltu velja **Skrá í afritunargeymslu** á síðunni **Rafrænar skýrslufæribreytur** áður en flutningur á sér stað. Þessi hnappur hefur ferlið við að stofna afrit af öllum tiltækum sniðmátum svo hægt sé að geyma þau í varabúnaðargeymslu ER fyrir sniðmát.

![Síða rafrænna skýrslufæribreyta](./media/GER-BackupTemplates-5.png)

## <a name="supported-deployments"></a>Studdar uppsetninar

Í Finance and Operations útgáfu 10.0.5 er eiginleikinn Afritunargeymsla ER-sniðmáta aðeins tiltækur í skýjadreifingum.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)

[Skilgreina rafrænan skýrslugerðarramma](electronic-reporting-er-configure-parameters.md)
