---
title: Skilgreina Viðskiptaskuldir
description: Þessi grein lýsir þeim síðum sem þú notar til að setja upp grundvallaraðgerðir og valfrjálsar aðgerðir fyrir viðskiptaskuldir í Microsoft Dynamics 365 for Finance and Operations. Hún lýsir einnig uppsetningarskrefum sem þú verður að ljúka áður en þú byrjar að setja upp viðskiptaskuldir.
author: abruer
manager: AnnBe
ms.date: 08/08/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 24671
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bf3226060eddf01fb218e99cae4097fecfe56e25
ms.sourcegitcommit: dd1e1636d351a15f9c1b6808bea359417a9bd690
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/25/2019
ms.locfileid: "896627"
---
# <a name="configure-accounts-payable"></a>Skilgreina Viðskiptaskuldir

[!include [banner](../includes/banner.md)]

Þessi grein lýsir þeim síðum sem þú notar til að setja upp grundvallaraðgerðir og valfrjálsar aðgerðir fyrir viðskiptaskuldir í Microsoft Dynamics 365 for Finance and Operations. Hún lýsir einnig uppsetningarskrefum sem þú verður að ljúka áður en þú byrjar að setja upp viðskiptaskuldir.

<a name="prerequisites-for-accounts-payable-setup"></a>Skilyrði fyrir uppsetningu viðskiptaskulda
----------------------------------------

Áður en hægt er að setja upp viðskiptaskuldir, verður að ljúka eftirfarandi uppsetningu:

-   Í Fjárhag
    -   Ef ætlunin er að nota greiðslubók þarf að setja upp greiðslubækur 
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

-   Á síðunni verkflæði viðskiptaskulda skal Setja upp verkflæðisskilgreiningar fyrir færslubókarsamþykktir og innkaupabeiðnir 

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

-   Á afhendingarskilmálar  síðu skal Stofna og viðhalda skilmálum fyrir flutning vöru frá seljanda til kaupanda.
-   Á Afhendingarmátum síðu, stofna og vinna með aðferðir við flutning sem er notaður þegar pöntun er afhent frá seljanda til kaupanda.
-   Á áfangastaðakóðasíðu Stofna og viðhalda kennimerki og lýsingum fyrir afhendingaráfangastaði

**Skjámyndir**

-   Á snið athugasemda  síðu Stofna staðlaðan texta sem birtist í ýmsum síðum
-   Á færibreytur sniðröðunar síðu Setja upp röðunarskipan fyrir beiðnir, innhreyfingarlista, fylgiseðla og reikninga 
-   Á uppsetningu prentstýringar síðu, setja upp upplýsingar um prentstýringu fyrir frumrit og afrit af síðum.

**Greiðslur**

-   Á Staðgreiðsluafsláttur síða, setja upp og Stýra skilmála til að fá staðgreiðsluafsláttur. Staðgreiðsluafsláttarkóðar eru tengdir lánardrottnum og notaðir í innkaupapöntunum.
-   Á Greiðsluáætlun síða, setja upp greiðsluáætlun sem eru notaðar til að stjórna afborgunargreiðslum til lánardrottinn.
-   Á greiðsludagar  síðu Skilgreina greiðsludaga sem eru notaðir til þess að reikna gjalddaga og tilgreina greiðsludaga fyrir tiltekinn dag vikunnar eða mánaðarins 
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





