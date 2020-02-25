---
title: Tölvupóstur ER-gerð áfangastaðar
description: Þetta efni veitir upplýsingar um hvernig á að stilla tölvpóst áfangastaðar fyrir hvern FOLDER eða FILE hluti á rafrænu skýrslugerðarsniðinu (ER) sem er stillt til að búa til útgönguskjöl.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 086114d6a8d425ca01521d9607e4a70ec5aa766b
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019826"
---
# <a name="EmailDestinationType">Áfangastður tölvupósts</a>

[!include [banner](../includes/banner.md)]

Hægt er að stilla tölvupóst áfangastaðar fyrir hvern FOLDER eða FILE hluti á rafrænu skýrslugerðarsniðinu (ER) sem er stillt til að búa til útgönguskjöl. Byggt á ákvörðunarstað, er myndað skjal afhent sem viðhengi við tölvupost.

Setja **Virkt** til **Já** til að senda frálagsskrá með tölvupósti. Eftir að þessi valkostur er virkjaður er hægt að breyta efni tölvupósts og tilgreina viðtakendur tölvupósts og meginmál tölvupósts. Hægt er að setja upp fastatexta fyrir efni og meginmál tölvupósts eða hægt er að nota ER-[formúlur](er-formula-language.md) til að gagnvirkt stofna texta tölvupósts. 

Hægt er að grunnstilla netföng fyrir rafræn skýrslugerð á tvo vegu. Hægt er að klára stillingarnar á sama hátt og prentstjórnunaraðgerðin lýkur henni, eða þú getur leyst netfang með því að nota bein tilvísun í ER stillingar með formúlu.

[![Virkja áfangastað tölvupósts](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)

## <a name="email-address-types"></a>Gerðir tölvupóstfanga

Þegar þú velur **Breyta** í reitunum **Til** eða **Cc** birtist svarglugginn **Senda tölvupóst til**. Síðan er hægt að velja rétta gerð tölvupóstfangs til að nota. Tölvupósttegundirnar **Skilgreiningartölvupóstur** og **Prentstýring** eru studdar eins og er.

[![Veldu tölvupóstserð](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)

### <a name="print-management"></a>Prentstýring

Ef þú velur tölvupóstgerðina **Prentstýring tölvupóstur** geturðu fært inn fast netfang í reitinn **Til**. 

[![Stilla föst netföng](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)

Til að nota tölvupóstföng sem eru ekki föst, verður að velja upprunagerð tölvupósts fyrir áfangastað skrár. Eftirfarandi virði eru studd: **Viðskiptavinur**, **Lánardrottinn**, **Viðfang**, **Tengiliður**, **Samkeppnisaðili**, **Starfskraftur**, **Umsækjandi**, **Væntanlegur lánardrottinn**, og **Lánardrottinn án leyfis**. Eftir að upprunagerð tölvupósts er valin skal nota næsta hnapp við reitinn **Upprunareikningur tölvupósts** til að opna skjámyndina **Formúluhönnuður**. Þú getur notað þetta form til að festa við formúlu sem skilar sér á keyrslutíma, **aðilalykill** af völdum upprunategundum frá unnu skjali til áfangastaðar tölvupóstsins.

[![Stilla upprunareikning tölvupósts](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)

Formúlur eru við tilgreindar fyrir skilgreiningu rafrænnar skýrslugerðar. Í **formúla**, Færið inn skjalbundna tilvísun í viðskiptavin eða lánardrottinn gerð aðila. Í stað þess að slá inn, hægt að finna gagnaveituhnút sem stendur fyrir lykil viðskiptavinar eða lánardrottins, og velja hnappinn **Bæta við gagnaveitu** til að uppfæra formúluna. Til dæmis, ef þú notar skilgreininguna **ISO 20022 kreditmillifærsla** er hnúturinn sem stendur fyrir lykil lánardrottins er `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.

Ef þú slærð inn strenggildi, svo sem `"DE-001"` og vistar formúlu verður tölvupóstur sendur til tengiliðs seljandans, **DE-001**.


[![Síðan ER-formúluhönnuður](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)

[![Stilla upprunareikning tölvupósts](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)



### <a name="configuration-email"></a>Skilgreiningartölvupóstur

Notaðu þessa gerð tölvupósts ef skilgreiningin sem þú notar er með hnút í gagnaveitum sem skilar **netfangi**. Hægt er að nota gagnaveitur og aðgerðir í formúluhönnuður til að ná rétt sniðnu netfang. Til dæmis, ef þú notar skilgreininguna **ISO 20022 kreditmillifærsla** er hnúturinn sem stendur fyrir netfang tengiliðar lánardrottins `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.

[![Stilla heimilisfangagjafa tölvupósts](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)
- [Áfangastaðir fyrir rafræna skýrslugerð](electronic-reporting-destinations.md)
- [Formúluhönnuður í rafrænni skýrslugerð (ER)](general-electronic-reporting-formula-designer.md)
