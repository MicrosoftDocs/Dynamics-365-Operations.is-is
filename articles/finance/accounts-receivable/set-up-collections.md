---
title: Setja upp innheimtu
description: Þessi skrá útskýrir hvernig á að setja upp innheimtuvirkni.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustCollectionsActivitiesListPage
audience: Application User
ms.reviewer: kfend
ms.custom: 14031
ms.assetid: dcc6da2f-9af5-4f1d-abaa-b72967b66979
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 49f47c48158f833f3d2cc0cad851860e995d3886
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870337"
---
# <a name="set-up-collections"></a>Setja upp innheimtu

[!include [banner](../includes/banner.md)]

Þessi skrá útskýrir hvernig á að setja upp innheimtuvirkni. Þú verður að ljúka nokkrum uppsetningarskrefum þegar safnhæfileikinn er notaður. Það eru einnig nokkrar valfrjálsar getu, þar á meðal hópar viðskiptavina og söfnun teymi. 

- Skilgreiningar aldurstímabila
- Aldursgreiningarmyndir
- Færslubókanöfn
- Ástæðukóði fyrir afskriftafærslur
- Innheimtufulltrúar
- Afskriftalykill
- Upplýsingar um ónóga inneign
- Stillingar Outlook fyrir þá sem nota síðuna **Innheimtu**
- Netföng

Nánar er fjallað um þessi atriði í allri þessari grein. 

## <a name="set-up-aging-period-definitions"></a>Setja upp skilgreiningar aldurstímabila

Setja upp skilgreiningu aldurstímabils Skilgreining aldurstímabils skilgreinir dálka sem á að birtast í **Aldursgreindar stöður**, **innheimtuverkþætti**, og **innheimtumál** listasíðum. Hann skilgreinir einnig tímabil sem birtast í **innheimtur** síðu. Ef hópur viðskiptamanna er uppsettur, er skilgreining aldurstímabils fyrir hópinn notuð. Ef engir hópar eru settir upp, er sjálfgefin skilgreining aldurstímabils sem er tilgreind í **færibreytur viðskiptakrafa** skjámynd notuð. Ef engin sjálfgefin skilgreining aldurstímabils er tilgreind, er fyrsta skilgreining aldurstímabils í **Skilgreining aldurstímabils** síðu er notað.

## <a name="create-an-aging-snapshot"></a>Stofna aldursgreiningarmynd
Stofna aldursgreiningarmynd færslna fyrir alla viðskiptavini eða fyrir viðskiptavini í viðskiptavinahóp. Upplýsingar um aldursgreiningarmynd birtist á **Aldursgreindar stöður** listasíðu og á **innheimtur** síðu. Það verður að stofna aldursgreiningarmynd áður en hægt er að nota listasíðuna. Listasíðan sýnir upplýsingar aðeins vegna viðskiptavina sem aldursgreiningarmynd hefur verið stofnuð fyrir.

## <a name="optional-set-up-customer-pools"></a>Valfrjálst: Setja upp viðskiptavinaflokka
Hægt er að setja upp viðskiptavinaflokka til að tákna flokka af viðskiptavinum. Hægt er að nota viðskiptavinahópa sem afmarkanir fyrir upplýsingar um viðskiptamann sem birtast í **innheimtur** listasíður á síðunni **innheimtur** eða þegar notandinn stofnar aldursgreiningarmynd.

## <a name="optional-create-a-collections-team"></a>Valfrjálst: Búa til innheimtuhóp
Ef fjöldi einstaklinga í fyrirtækinu sjá um innheimtuvinnu er hægt að setja upp innheimtuhóp. Hægt er að velja hóps á **Færibreytur viðskiptakrafna** síðunni. Ef þú ekki stofna innheimtuhóp, verður ein slík búin til sjálfkrafa þegar notandinn setur upp innheimtufulltrúa í **innheimtufulltrúi** skjámynd.

## <a name="set-up-a-collections-case-category"></a>Setja upp innheimtumálstegund
Ef skipuleggja á innheimtuvinnu með því að nota mál skal setja upp málstegund með gerð flokks **Innheimta**. Þetta er bara nauðsynleg ef á að nota málsvirkni á síðunni **Innheimta**.

## <a name="set-up-journal-names-settlement-writeoff-and-nsf"></a>Setja upp færslubókarnöfn (jöfnun, afskrift, og innistæðulaus sjóður)
Setja upp færslubókarnöfn sem eru notaðar þegar færslur eru unnin á **innheimtur** síðunni. Þetta ferli innifelur jöfnun á færslu, afskrift færslu, og vinnslu á innistæðulaust (NSF).

| Lýsing | Færslubókargerð     |
|-------------|------------------|
| Byggt svæði  | Greiðsla viðskiptavinar |
| Afskrift   | Daglega            |
| Innistæðulaus sjóður         | Greiðsla viðskiptavinar |

## <a name="set-up-a-reason-code-for-writeoff-transactions"></a>Setja upp ástæðukóða fyrir afskriftarfærslur
Setja upp sjálfgefinn ástæðukóða sem er notaður þegar færslur eru afskrifaðar á síðunni **Innheimta**. Hægt er að breyta kóða við afskriftarferli.

## <a name="set-up-a-folder-for-email-attachments-and-create-email-templates"></a>Setja upp möppu fyrir viðhengi í tölvupósti og stofna sniðmát tölvupósts
Ef þú sendir tölvupóst úr á **innheimtur** síðu sem hefur Microsoft Excel viðhengi, er hægt að stofna valfrjáls sniðmát tölvupósts fyrir þessi skilaboð.

## <a name="set-up-accounts-receivable-parameters-for-collections"></a>Setja upp færibreytur fyrir viðskiptakröfur fyrir innheimtu
Setjið upp færibreytur viðskiptakrafna sem birtast í flipanum **innheimtur**

## <a name="optional-set-up-collections-agents"></a>Valfrjálst: Setja upp innheimtufulltrúa
Ef fjöldi einstaklinga í fyrirtækinu sjá um innheimtuvinnu er hægt að setja upp innheimtufulltrúa. Innheimtufulltrúa er starfsmaður sem er settur upp sem notandi í **notendavensl** skjámynd. Hægt er að úthluta viðskiptavinahópum, (sem eru fyrirspurnir viðskiptavinar), á innheimtufulltrúa til að aðstoða fulltrúa við að skipuleggja vinnu sína. Innheimtufulltrúum er bætt við hópinn sem er valinn á síðunni **Færibreytur viðskiptakrafna**. Ef hópur er ekki valinn á þeirri síðu, er nýr hópur með heitinu **Innheimtur** stofnaður sjálfvirkt og innheimtufulltrúa er bætt við þann hóp.

## <a name="set-up-a-writeoff-account"></a>Setja upp afskriftalykil
Setja upp afskriftalykil sem er notaður fyrir afskriftarfærslu fjárhags þegar færsla er afskrifuð. Þessi lykill er geymt í bókunarreglu viðskiptavinar.

## <a name="set-up-nsf-information-for-bank-accounts"></a>Setja upp upplýsingar um Innistæðulausan sjóð fyrir bankareikninga
Uppfæra bankareikningum þannig að þeir hafi rétta færslubók þegar FSF-greiðsla eru auðkenndar á **innheimtur** síðunni. Á við **gjaldmiðilsstjórnun** flipanum, á **nsf-greiðslubók** skal velja greiðslubók.

## <a name="set-up-outlook-settings-for-users-of-the-collections-page"></a>Uppsetning Outlook - stillinga fyrir notendur innheimtusíðunnar
Áður en starfsmenn geta stofna verkþætti eða senda tölvupóstsskilaboð með því að nota síðuna **Innheimtur**, verður að staðfesta að **Microsoft Outlook samstilling** skilgreiningarlykill er valinn og að samstilling Outlook sé sett upp fyrir þessa starfsmenn.

## <a name="set-up-email-and-addresses"></a>Settu upp tölvupóst og netföng
Þú getur notað tölvupóst til að eiga samskipti við bæði viðskiptavini og afgreiðslufólk um málefni safns til að senda tölvupóst frá **Innheimta** síðu. 

### <a name="set-up-email-and-address-settings-for-collections-customer-contacts"></a>Setja upp tölvupóststillingar og aðseturstillingar fyrir tengiliði viðskiptamanna fyrir innheimtu.
Setja upp tölvupóstsaðsetur fyrir tengiliði viðskiptamanna til að senda tölvupóstsskilaboð til þeirra tengiliða úr **Innheimta** síðu. Tengiliður innheimtu er notaður sem sjálfgefinn tengiliður í **Innheimtur** skjámynd. Hægt er að setja upp uppgjörsaðsetur fyrir viðskiptamanns ef uppgjör á að nota aðsetur sem er annað en aðalaðsetri. 

Á **Skulda og Innheimtu** flýtiflipi fyrir viðskiptavin, í **innheimtutengiliður** skal velja einstaklings í fyrirtæki viðskiptavinar sem vinnur með þínum innheimtufulltrúi. Tengiliðurinn er notaður sem sjálfgefinn tengiliður í **Innheimtur** síðu og er notandinn sem tölvupóstsskilaboð eru send til. 

> [!NOTE] 
> Ef innheimtutengiliður fyrir viðskiptamann er ekki tilgreindur er aðaltengiliðar viðskiptamannsins notað. Ef aðaltengiliður er ekki tilgreint, tölvupóstskilaboð verður sent í fyrsta aðsetur sem er skráð í **Tengiliður** síðu.

### <a name="set-up-email-settings-for-salespeople"></a>Setja upp stillingar fyrir tölvupóst sölumanna
Setja upp tölvupóstsaðsetur fyrir sölufólk til að senda tölvupóstsskilaboð til sölufólks úr **innheimta** síðu. Setja upp tölvunetfang fyrir hvern sölufulltrúa í hverjum þóknunarsöluflokki. Sölufulltrúi sem hefur **tengiliður** gátreitinn valinn er sjálfgefinn sölumaður sem tölvupóstsskilaboð eru send til. 

Ef sölufulltrúi er ekki tilgreindur er aðalsölumaður fyrirtækis viðskiptamanns notað. Ef aðalsölumaður er ekki tilgreindur, verða tölvupóstsskilaboð send til fyrsta sölumanns á listanum á síðunni.


Frekari upplýsingar er hægt að finna í eftirfarandi efni:

 - [Stofna innheimtubréfaröð](tasks/create-collection-letter-sequence.md)

 - [Vinna úr innheimtubréfum](tasks/process-collection-letters.md)

 - [Fara yfir innheimtuupplýsingar](tasks/review-collections-information.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
