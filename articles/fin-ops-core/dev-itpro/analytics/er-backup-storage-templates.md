---
title: Afritunargeymsla ER-sniðmáta
description: Þetta efni útskýrir hvernig á að nota varabúnaðargeymslu rafrænnar skýrslugerðar (ER) til að endurheimta sniðmát.
author: NickSelin
manager: AnnBe
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-08-13
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 136a81e661590d7af879e816c1142de85fb72e06
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681401"
---
# <a name="backup-storage-of-er-templates"></a>Afritunargeymsla ER-sniðmáta

[!include [banner](../includes/banner.md)]

[Yfirlit rafrænnar skýrslugerðar (ER)](general-electronic-reporting.md) gerir fyrirtækjanotendum kleift að skilgreina snið fyrir skjöl á útleið í samræmi við lagaskilyrði mismunandi landa og svæða. Stillt ER-snið geta notað fyrirfram skilgreind sniðmát til að búa til útgönguskjöl á ýmsum sniðum, svo sem Microsoft Excel vinnubækur, Microsoft Word skjöl, eða PDF-skjöl. Sniðmátin eru fyllt með gögnum sem skilgreint gagnaflæði fyrir mynduð skjöl krefst.

Hægt er að birta hvert skilgreint snið sem hluta af ER-lausn. Hægt er að flytja út hverja lausn rafrænnar skýrslugerðar úr einu tilviki af Finance and Operations og flytja hana inn í annað tilvik.

Rammi rafrænnar skýrslugerðar notar [Stilla skjalastjórnun](../../fin-ops/organization-administration/configure-document-management.md) til að halda nauðsynlegum sniðmátum fyrir núverandi Finance and Operations tilvik. Það fer eftir stillingum ER-ramma, Microsoft Azure Blob-geymslu eða Microsoft SharePoint hvort hægt er að velja möppu sem aðal geymslupláss fyrir sniðmát. (Sjá frekari upplýsingar [Stilla ramma rafrænnar skýrslugerðar (ER)](electronic-reporting-er-configure-parameters.md).) DocuValue taflan hefur einstaka skrá fyrir hvert sniðmát. Í hverri skrá geymir reiturinn **AccessInformation** slóð sniðmátaskrár sem er staðsett á skilgreindum geymslustað.

Þegar þú stjórnar Finance and Operations tilvikum þínum gætir þú ákveðið að flytja núverandi tilvik á aðra staðsetningu. Til dæmis gætirðu flutt framleiðslutilvikið í nýtt sandkassaumhverfi. Ef þú stillir ER-ramma til að geyma sniðmát í Blob-geymslu, vísar DocuValue-taflan í nýja sandkassaumhverfi til tilviks Blob-geymslu í framleiðsluumhverfi. Hins vegar er ekki hægt að fá aðgang að þessu tilviki úr sandkassanumhverfinu, vegna þess að flutningsferlið styður ekki flutning á gripum í Blob-geymslu. Þess vegna, ef þú reynir að keyra ER-snið sem notar sniðmát til að búa til viðskiptaskjöl, kemur undantekning fyrir, og þér er tilkynnt um það sniðmát sem vantar. Þér er einnig leiðbeint um að nota ER-hreinsunartólið til að eyða og flytja síðan aftur upp skilgreiningu ER-sniðsins sem inniheldur sniðmátið. Vegna þess að þú gætir haft nokkrar stillingar á ER-sniði, getur þetta ferli verið tímafrekt.

Afritunargeymsla ER-sniðmátsaðgerðar getur hjálpað þér að búa til sniðmát þannig að þau eru alltaf tiltæk til að búa til viðskiptaskjöl.

> [!NOTE]
> Þessa aðgerð er aðeins hægt að nota þegar Blob geymsla hefur verið valin sem raunverulegt geymslupláss fyrir ER sniðmát.

## <a name="automated-recovery-and-notification"></a>Sjálfvirk endurheimt og tilkynning

Fyrir þennan möguleika er hvert sniðmát nýrrar stillingar ER snið í núverandi umhverfi sjálfkrafa vistað á afritunargeymsluplássi fyrir sniðmát (ERDocuDatabaseStorage gagnagrunnstaflan) þegar eftirfarandi tilvik eiga sér stað:

- Þú flytur inn nýja ER snið stillingu sem inniheldur sniðmát.
- Þú klárar drög að útgáfu ER sniðstillingar sem inniheldur sniðmát.

Afrit af sniðmátum eru flutt á nýtt tilvik af Finance and Operations sem hluta af gagnagrunni forritsins.

Ef sniðmáts með ER sniði er krafist til að búa til skjöl á útleið, til að vinna úr greiðslum lánardrottins, þ.m.t. myndun greiðsluráðgjafar og eftirlitsskýrslna, til dæmis, en nauðsynleg sniðmát er ekki að finna á aðalgeymslustaðnum, gerast eftirfarandi tilvik:

- Ef sniðmátið er tiltækt á öryggisafritunargeymslunni er það sjálfkrafa tekið af afritunargeymslustaðnum, endurheimt á aðalgeymsluplássið og notað fyrir núverandi framkvæmd.
- Sérhverjum notanda sem er úthlutað á hlutverkið **Þróunaraðili rafrænnar skýrslulausnar** eða **Kerfisstjóri** er tilkynnt um sniðmátið sem vantar í gegnum aðgerðarstöðina. Skilaboðin sem birtast eru háð gildi færibreytunnar **Keyra ferlið sjálfkrafa til að endurheimta brotin sniðmát í runu**:

    - Ef þessi færibreyta er stillt á **Slökkt** mæla skilaboðin með því að þú hefjir runuferlið til að laga sjálfkrafa svipuð vandamál fyrir önnur ER-sniðmát fyrir skilgreiningarsnið. Skilaboðin innihalda tengil sem þú getur notað til að hefja runuferlið.
    - Ef þessi færibreyta er stillt á **Kveikt** tilkynna skilaboðin þér að uppgötvast hafi vandamál vegna sniðmáts sem vantar og að ný runuvinnsla, **Endurheimta biluð sniðmát úr innri afritun gagnagrunnsins**, hefur sjálfkrafa verið áætluð. Þessi runuvinnsla mun sjálfkrafa laga svipuð vandamál fyrir önnur sniðmát.

Til að setja upp **Keyra sjálfkrafa aðferðina við að endurheimta skemmd sniðmát í runu** færibreytuna skal ljúka eftirfarandi skrefum:

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

Ef umhverfi er uppfært í Finance and Operations útgáfa 10.0.5 (október 2019) og ætlunin er að fara í nýtt umhverfi sem inniheldur skilgreiningar fyrir snið rafrænnar skýrslugerðar sem hægt er að keyra skal velja **Fylla út geymslu öryggisafrita** á síðunni **Rafrænar skýrslugerðarfæribreytur** áður en flutningurinn á sér stað. Þessi hnappur hefur ferlið við að stofna afrit af öllum tiltækum sniðmátum svo hægt sé að geyma þau í varabúnaðargeymslu ER fyrir sniðmát.

![Síða rafrænna skýrslufæribreyta](./media/GER-BackupTemplates-5.png)

## <a name="manual-recovery"></a>Handvirk endurheimt

Farið í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Endurheimta skemmd sniðmát** til að ræsa handvirkt endurhemt sniðmáta rafrænnar skýrslugerðar úr geymslu öryggisafrita á aðalgeymslustað. Áður en þetta ferli er hafið á síðunni **Endurheimta skemmd sniðmát** er hægt að tilgreina hvort það verði framkvæmt gagnvirkt eða hvort runuvinnslan verði tímasett fyrir þetta.

## <a name="supported-deployments"></a>Studdar uppsetninar

Í Finance and Operations útgáfu 10.0.5 er öryggisafritunargeymsla á sniðmátseiginleika rafrænnar skýrslugerðar aðeins tiltæk í skýjauppsetningu.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir rafræna skýrslugerð (ER)](general-electronic-reporting.md)

[Skilgreina rafrænan skýrslugerðarramma (ER)](electronic-reporting-er-configure-parameters.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]