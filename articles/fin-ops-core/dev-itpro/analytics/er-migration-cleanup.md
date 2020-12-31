---
title: Hreinsun flutnings rafrænnar skýrslugerðar
description: Í þessu efnisatriði er útskýrt hvernig hægt er að nota hreinsunaraðgerð fyrir flutning rafrænnar skýrslugerðar til að leysa úr málum er varða sniðmát rafrænnar skýrslugerðar.
author: NickSelin
manager: AnnBe
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, ERParameters, ERMigrationCleanup
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: edb60f247b2bd6cc4ecd514e3e85bafbb681788d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686369"
---
# <a name="er-migration-cleanup"></a>Hreinsun flutnings rafrænnar skýrslugerðar 

[!include[banner](../includes/banner.md)]

Þegar þú stjórnar fjármálatilvikum þínum gætir þú ákveðið að flytja núverandi tilvik á aðra staðsetningu. Til dæmis gætirðu flutt framleiðslutilvikið í nýtt sandkassaumhverfi. Ef þú hefur skilgreint ramma rafrænnar skýrslugerðar til að geyma sniðmát í Microsoft Azure Blog-geymslu vísar taflan **DocuValue** í nýja sandkassaumhverfinu í tilvikið af Blog-geymslu í framleiðsluumhverfinu. Hins vegar er ekki hægt að opna þetta tilvik í sandkassaumhverfinu vegna þess að flutningsferlið styður ekki flutning gervinga í Blog-geymslu. Frekar er búist við því að í nýja sandkassaumhverfinu sé vísað í tilvik Blob-geymslunnar í sandkassaumhverfinu sem sækir ekki enn sniðmát rafrænnar skýrslugerðar.

Ef reynt er að keyra snið rafrænnar skýrslugerðar sem notar sniðmát til að búa til viðskiptaskjöl á sér stað undantekning og tilkynnt er um sniðmátið sem vantar. Þér er einnig bent á að nota hreinsunarvalkost fyrir flutning rafrænnar skýrslugerðar til að eyða og síðan flytja aftur inn skilgreiningu á sniði rafrænnar skýrslugerðar sem inniheldur sniðmátið.

[![Keyrir snið rafrænnar skýrslugerðar](./media/er-migration-cleanup-run.png)](./media/er-migration-cleanup-run.png)

Þú færð svipaða villu ef þú ferð yfir á síðuna **Skilgreiningar** (**Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**) og í skilgreiningartrénu skaltu reyna að eyða skilgreiningu á sniði rafrænnar skýrslugerðar sem notar sniðmát.

[![Eyðing á sniði rafrænnar skýrslugerðar](./media/er-migration-cleanup-delete.png)](./media/er-migration-cleanup-delete.png)

Ljúkið eftirfarandi skrefum til að leysa úr vandamálum með sniðmát rafrænnar skýrslugerðar sem ekki er hægt að opna.

1.  Farið á síðuna **Fyrirtækisstjórnun** \> **Reglubundið** \> **Hreinsun flutnings**.
2.  Veljið skilgreiningu rafrænnar skýrslugerðar sem ekki er hægt að keyra eða eyða.
3.  Veljið **Eyða**.
4.  Staðfestið eyðingu á valdri skilgreiningu á sniði rafrænnar skýrslugerðar.
5.  [Flytja inn](download-electronic-reporting-configuration-lcs.md) eydda skilgreiningu á sniði rafrænnar skýrslugerðar í núverandi fjármálatilvik.

## <a name="applicability"></a>Gildissvið

> [Mikilvægt] Valkosturinn **Hreinsun flutnings** miðast eingöngu við skilgreiningar á sniði rafrænnar skýrslugerðar sem innihalda sniðmát rafrænnar skýrslugerðar sem ekki er hægt að opna. Þegar skilgreiningu á sniði rafrænnar skýrslugerðar er eytt með því að nota valkostinn **Hreinsun flutnings** eyðir rafræn skýrslugerð sniðmátunum sem tengjast gervingum skilgreiningarinnar í eingöngu gagnagrunni forrits. Tilvist viðeigandi efnislegra skráa í Blob-geymslu er ekki staðfest. Þess í stað er gert ráð fyrir að þær séu ekki til. Þess vegna skal ekki nota valkostinn **Hreinsun flutnings** sem aðra leið í stað þess að eyða skilgreiningu rafrænnar skýrslugerðar á síðunni **Skilgreiningar**. Aðeins skal nota valkostinn **Hreinsun flutnings** þegar eyðing á skilgreiningu rafrænnar skýrslugerðar á síðunni **Skilgreiningar** tókst ekki.
>
> Ef valkosturinn **Hreinsun flutnings** er notaður til að eyða skilgreiningu á sniði rafrænnar skýrslugerðar þegar sniðmátið sem vísað er í er tiltækt í Blob-geymslunni, er aðeins hægt að eyða tengdum gervingum skilgreiningar í gagnagrunni forritsins. Efnislega skráin í sniðmátinu í Blob-geymslunni verður þar áfram. Ekki er lengur leyfilegt að skrifa yfir skrár í Blog-geymslunni. Nánari upplýsingar eru í [KB4557217](https://fix.lcs.dynamics.com/Issue/Details?kb=4557217). Þar að auki er ekki lengur hægt að flytja aftur inn eyddar skilgreiningar með því að nota hreinsun flutnings í þessu umhverfi. Til að leysa þetta vandamál þarf að finna samsvarandi skrá í Blob-geymslu og eyða henni handvirkt.

[![Flytja inn snið rafrænnar skýrslugerðar](./media/er-migration-cleanup-import.png)](./media/er-migration-cleanup-import.png)

Svipað vandamál getur komið upp ef forritstilvikið er flutt á aðra staðsetningu sem hefur verið notuð sem flutningsmarkmið oftar en einu sinni og þar sem Blob-geymslan inniheldur nú þegar sniðmátsskrár rafrænnar skýrslugerðar.

Fyrst að hægt er að hafa margar skilgreiningar á sniði rafrænnar skýrslugerðar getur þetta ferli verið tímafrekt. Þar af leiðandi er æskilegt að nota eiginleikann [Öryggisafrit sniðmáta rafrænnar skýrslugerðar](er-backup-storage-templates.md) til að endurheimta sjálfkrafa sniðmát með gölluðum tilvísunum.
