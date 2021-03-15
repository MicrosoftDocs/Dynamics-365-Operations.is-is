---
title: Birta síður hlið við hlið við því að nota Opna í nýjum gluggaeiginleika
description: Þessi grein útskýrir hvernig eigi að birta síður hlið við hlið.
author: aneesmsft
manager: AnnBe
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 35ade352edf31fe895a9b9118a8ad7d5fe6c0bde
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798404"
---
# <a name="show-pages-side-by-side-using-the-open-in-new-window-feature"></a>Birta síður hlið við hlið við því að nota Opna í nýjum gluggaeiginleika

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig eigi að birta síður hlið við hlið.

Þú gætir viljað skoða margar síður hlið við hlið til að ljúka verkefnum hratt. Sem dæmi, gæti verið óskað að villuleita eða færa inn línur í fleiri en einni færslubók. Venjulega til að staðfesta eða slá inn línur í fleiri en eina færslubók þurfti að fara fram og til baka milli síðunnar sem sýnir lista yfir færslubækur og síðuna sem sýnir línur í tiltekna færslubók. Hins vegar **Opna í nýjum glugga** eiginleikinn gerir kleift að sýna þessar síður hlið við hlið þannig að hægt er að framkvæma verkefnunum fljótt.

Haldið er áfram með fyrrgreint dæmi hér fyrir ofan þegar verið er að skoða línurnar með því að smella á **Opna í nýjum glugga** tákn.

[![Smellið á táknið Opna í nýjum glugga.](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)

Smella á **Opna í nýjum glugga** táknið opnar línusíðuna í nýja, vafra sem sprettur upp og flettir síðan í upprunalega vafra til baka í sögunni á síðuna sem birti lista yfir færslubækur. Hægt er að birta síðan báðar síðurnar hlið við hlið. Eftir að færslubók er skoðuð er hægt að breyta valinni færslubók á listasíðu færslubókar, og línusíður í sprettiglugga birta sjálfkrafa línur í nýlega valinnar færslubókar.

[![Hægt er að birta síður hlið við hlið.](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)

Gagnvirk tengingu og endurnýjun gerist vegna vensl sem eru til staðar á milli gagna sem hafa tekið Gert öryggisafrit af þessar síður. Ef kerfið er ekki kunnugt um tengsl milli gagna, sprettiglugga mun ekki endurnýjast sjálfkrafa til að bregðast við breytingum í glugganum sem það er upprunnið frá.

Sumar síður eru með mörgum yfirlitum eins og hnitanetsyfirlit, hausyfirlit og upplýsingayfirlit. **Opna í nýjum glugga** táknið veldur því að öll síðan opnast í nýjan vafraglugga. Þess vegna er hægt að halda tvö yfirlit yfir sömu síðu hlið við hlið með því að nota eiginleika **Opna í nýjum glugga**. Nánast allar slíkar síður hafa flettingarlista sem þú getur notað til að skipta á milli skráa og ná fram svipaðri upplifun.

Áður en aðgerðin **Opna í nýjum glugga** er notuð ætti að skilgreina sprettigluggavörn vafrans til að leyfa sprettiglugga úr slóð svæðisins. Sem dæmi, mætti heimila sprettiglugga úr "\*. dynamics.com".

**Opna í nýjum glugga** eiginleiki er aðeins tiltækur þegar fleiri en einn síða er opna í glugganum. Sprettigluggi lokast einnig sjálfkrafa þegar engar frekari síður eru opnar (þar er, þegar síðustu síðunni í glugganum er lokað). Kerfið lokar einnig opnum síðum þegar farið er í mismunandi svæði í forritinu. Ef sprettugluggar eru opnir og farið er í annað svæði í forritinu, er sprettugluggum sjálfkrafa lokað því kerfið lokaði síðunum í þeim gluggum.

Efsta sláin í sprettiglugga birtir upplýsingar um fyrirtækið sem síðuna var opnuð í og er skrifvarin. Sprettigluggar treysta einnig á aðalvafragluggann. Ef aðalglugginn er lokaður eða endurnýjuð, allar opnar sprettuglugga mun verða eingöngu lesaðgangur. Ef þetta gerist er hægt að skoða upplýsingarnar í þessum gluggum, en er ekki hægt að eiga samskipti við þá.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]