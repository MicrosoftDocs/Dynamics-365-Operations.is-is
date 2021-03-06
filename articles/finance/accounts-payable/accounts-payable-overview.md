---
title: Yfirlit yfir skilgreiningu viðskiptaskulda
description: Þessi grein lýsir þeim síðum sem þú notar til að setja upp grundvallaraðgerðir og valfrjálsar aðgerðir fyrir viðskiptaskuldir. Hún lýsir einnig uppsetningarskrefum sem þú verður að ljúka áður en þú byrjar að setja upp viðskiptaskuldir.
author: abruer
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable, DeliveryReason, DeliveryTerms, DestinationCode
audience: Application User
ms.reviewer: roschlom
ms.custom: 24671
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0edc2fcbde536e98fa3ce3567c2c8fdf3fc864ad
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188783"
---
# <a name="configure-accounts-payable-overview"></a>Yfirlit yfir skilgreiningu viðskiptaskulda

[!include [banner](../includes/banner.md)]

Þessi grein lýsir þeim síðum sem þú notar til að setja upp grundvallaraðgerðir og valfrjálsar aðgerðir fyrir viðskiptaskuldir. Hún lýsir einnig uppsetningarskrefum sem þú verður að ljúka áður en þú byrjar að setja upp viðskiptaskuldir.

## <a name="prerequisites-for-accounts-payable-setup"></a>Skilyrði fyrir uppsetningu viðskiptaskulda

Áður en hægt er að setja upp viðskiptaskuldir, verður að ljúka eftirfarandi uppsetningu:

-   Í Fjárhag
    -   Ef ætlunin er að nota greiðslubók þarf að setja upp greiðslubækur.
    -   Ef ætlunin er að keyra gengisleiðréttingar þarf að setja upp gjaldmiðilskóða í síðuna Gjaldmiðlum, setja upp gerðir gengis á síðu gerðir gengis og setja upp gengi gjaldmiðla á síðu gengi Gjaldmiðils.
-   Í reiðufjár- og bankastjórnun, eru settir upp bankareikningar til þess að nota með greiðsluháttum.

## <a name="setup-pages-for-accounts-payable"></a>Uppsetningarsíður fyrir viðskiptaskuldir

Notið eftirfarandi síður til þess að setja upp grundvallaraðgerðir viðskiptaskulda fyrir hvert lögaðila. Síðum er raðað í ráðlagðri röð fyrir uppsetningu. Hægt er stofna sniðmát úr fyrstu færslunum sem eru stofnaðar, til þess að einfalda uppsetningarferlið. Í sniðmáti eru yfirleitt færslur færðar inn í mörgum svæðum til að endurspegla aðgerðirnar sem fyrirtækið vill innleiða fyrir tiltekna gerð lánardrottins.
1.  Á síðunni greiðsluskilmálar, Skilgreinið greiðsluskilmála sem er úthlutað á sölupantanir, innkaupapantanir og viðskiptavinur, og lánardrottna, og ákvarða gjalddaga reikninga. Nánari upplýsingar er að finna í [Skilgreina greiðsluþóknanir lánardrottna](tasks/define-vendor-payment-fees.md).
2.  Á greiðsluaðferðir - lánardrottnar síðu, Stofna og viðhalda upplýsingar um hvernig fyrirtækið greiðir lánardrottnum.
3.  Á síðunni lánardrottnaflokkur, stofnið og viðhaldið lánardrottnaflokkum sem deila mikilvægum færibreytum fyrir bókun, greiðslu og jöfnun, skýrslugerð og spár.
4.  Á bókunarreglu lánardrottins síðu, skal skilgreina hvernig lánardrottnafærslur eru bókaðar í fjárhag.
5.  Á færibreytusíðum viðskiptaskulda skal setja upp sjálfgefnar stillingar sem eru notaðar ef nánari stillingar eru ekki tilgreindar, færibreytur fyrir ýmsar aðgerðir og ýmsar númeraraðir fyrir viðskiptaskuldir.
6.  Á Síðunni uppsetning sniðs, skal Skilgreina snið ýmissa skjala sem tengjast lánardrottnum og eru notuð innan fyrirtækisins til þess að rekja móttöku frá lánardrottnum og færa inn ástæður fyrir greiðsluflæði til lánardrottna.
7.  Á síðunni lánardrottinn, Stofna og viðhalda lánardrottnalyklum, og einnig skattyfirvöldum sem fyrirtækið sendir VSK-skýrslur til.

## <a name="optional-setup-pages-for-accounts-payable"></a>Valfrjálsar uppsetningarsíður fyrir viðskiptaskuldir
Auk grunnaðgerðum, hafa viðskiptaskuldir aðrar aðgerðir sem hægt er að setja upp.

Viðbótar uppsetningarsíður eru skipulagðar eftir aðgerðum.

**Reglur**
-   Síðunni stefna fyrir reikning lánardrottins er að setja upp stefna fyrir reikning lánardrottins.

**Reikningsjöfnun**

-   Á síðunni vikmörk fyrir heildarupphæð reiknings skal setja upp vikmörk fyrir heildarupphæð reiknings.
-   Á síðunni jöfnunarregla skal Setja upp tvíhliða og þríhliða Jöfnunarreglur.
-   Á síðunni vikmörk verðs skal setja upp vikmörk fyrir einingarverð.
-   Á síðunni vikmarkaflokkur vöruverðs skal setja upp vikmarkaflokkur fyrir vöruverð.
-   Á síðunni vikmarkaflokkur lánardrottnaverðs skal setja upp vikmarkaflokkur fyrir lánardrottnaverð.
-   Á síðunni vikmörk fyrir gjald skal setja upp vikmörk fyrir gjöld.

**Verkflæði**

-   Á síðunni Verkflæði viðskiptaskulda skal setja upp verkflæðisskilgreiningar fyrir færslubókarsamþykktir og innkaupabeiðnir.

**Ástæður**

-   Á síðunni ástæður lánardrottins, Setja upp ástæðukóða

**Gjöld**

-   Á síðunni gjaldakóðar, skal Setja upp kóða fyrir gjöld sem eru notaðir í innkaupapöntunum.
-   Á síðunni Gjaldaflokkur lánardrottins stofna og vinna með gjaldaflokka fyrir lánardrottna.
-   Á síðunni Kostnaðaraukaflokki skal stofna og vinna með gjaldaflokka fyrir afurðir.
-   Á sjálfvirk gjöldsíðunni skal Skilgreina gjöld sem eru sjálfvirkt úthlutað á pantanir.

**Fylgivörur**

-   Á við fylgivöruflokkar- Lánardrottins síðu, skal stofna og viðhalda fylgivöruflokkum fyrir lánardrottna.
-   Á við fylgivöruflokkar- birgðirsíðu, skal stofna og viðhalda fylgivöruflokkum fyrir afurðir.

**Arðgreiðsla**

-   Á síðunni Afhendingarskilmálar skal stofna og viðhalda skilmálum fyrir flutning vöru frá seljanda til kaupanda.
-   Á Afhendingarmátum síðu, stofna og vinna með aðferðir við flutning sem er notaður þegar pöntun er afhent frá seljanda til kaupanda.
-   Á áfangastaðakóðasíðu Stofna og viðhalda kennimerki og lýsingum fyrir afhendingaráfangastaði

**Skjámyndir**

-   Á síðunni Athugasemdir eyðublaða skal stofna staðlaðan texta sem birtist á ýmsum síðum.
-   Á síðunni Röðunarfæribreytur skjámyndar skal setja upp röðunarskipan fyrir beiðnir, innhreyfingarlista, fylgiseðla og reikninga.
-   Á uppsetningu prentstýringar síðu, setja upp upplýsingar um prentstýringu fyrir frumrit og afrit af síðum.

**Greiðslur**

-   Á Staðgreiðsluafsláttur síða, setja upp og Stýra skilmála til að fá staðgreiðsluafsláttur. Staðgreiðsluafsláttarkóðar eru tengdir lánardrottnum og notaðir í innkaupapöntunum.
-   Á Greiðsluáætlun síða, setja upp greiðsluáætlun sem eru notaðar til að stjórna afborgunargreiðslum til lánardrottinn.
-   Á síðunni Greiðsludagar skaltu skilgreina greiðsludaga sem eru notaðir til þess að reikna gjalddaga og tilgreina greiðsludaga fyrir tiltekinn dag vikunnar eða mánaðarins.
-   Á Greiðsluþóknun síða, stofna og viðhalda greiðsluþóknun sem tengist lánardrottinn.
-   Á greiðslufyrirmælin síðu, stofna og viðhalda greiðslufyrirmælum.

**Upplýsingar**

-   Á skilgreining aldurstímabilssíðuSetja upp notendaskilgreind bil til þess að greina gjalddagadreifingu fyrir lánardrottinslykla.
-   Á Atvinnugrein síðu, stofnið línu atvinnugreinakóða (LOB) sem eru úthlutað á lánardrottnum.

**skattur 1099**

-   Á síðunni **1099-svæðin** staðfesta og uppfæra lágmarksupphæðir sem verður að skrá í skattstofa (IRS), samkvæmt nýjustu kröfum skattayfirvalda Bandaríkjanna.

## <a name="optional-setup-for-other-modules"></a>**Valfrjáls uppsetning fyrir aðrar kerfiseiningar**
**Fyrirtækisstjórnun**

-   Á númeraraðir síðu, setja upp númeraraðaflokka fyrir reikningsnúmera.
-   Á eftirfarandi síðum skal setja upp upplýsingar um aðsetur:
    -   Uppsetning aðseturs
    -   NAF-kóðar
    -   Flytja inn póstnúmer

**Fjárhagur**

-   Á fjárhagsvíddirsíðu, skal setja upp fjárhagsvíddir.
-   Á eftirfarandi síðum skal setja upp skattaupplýsingar:
    -   VSK-kóðar
    -   VSK-flokkar
    -   VSK-flokkar vöru
    -   Lykilflokkur
    -   Undanþágukóðar VSK
    -   Skattaumdæmi
    -   Skattayfirvöld
    -   Virðisaukaskatttímabil

**Reiðufjár- og bankastjórnun**

-   Á greiðslumálefnakóða síðu, setja upp málefniskóða seðlabanka







[!INCLUDE[footer-include](../../includes/footer-banner.md)]