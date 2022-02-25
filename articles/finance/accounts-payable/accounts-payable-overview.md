---
title: Yfirlit yfir skilgreiningu viðskiptaskulda
description: Þetta efnisatriði lýsir síðunum sem þú notar til að setja upp grunn- og valfrjálsa virkni fyrir viðskiptaskuldir. Hún lýsir einnig uppsetningarskrefum sem þú verður að ljúka áður en þú byrjar að setja upp viðskiptaskuldir.
author: abruer
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable, DeliveryReason, DeliveryTerms, DestinationCode
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "24671"
- intro-internal
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6cbc800d7ae4d566fddb111b7ee9d67234e3cf8c
ms.sourcegitcommit: 43d0555c17a0643c9e5ba3bc2da3ce5f80754642
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/18/2022
ms.locfileid: "8325995"
---
# <a name="configure-accounts-payable-overview"></a>Yfirlit yfir skilgreiningu viðskiptaskulda

[!include [banner](../includes/banner.md)]

Þessi grein lýsir þeim síðum sem þú notar til að setja upp grundvallaraðgerðir og valfrjálsar aðgerðir fyrir viðskiptaskuldir. Hún lýsir einnig uppsetningarskrefum sem þú verður að ljúka áður en þú byrjar að setja upp viðskiptaskuldir.

## <a name="prerequisites-for-accounts-payable-setup"></a>Skilyrði fyrir uppsetningu viðskiptaskulda

Áður en hægt er að setja upp viðskiptaskuldir, verður að ljúka eftirfarandi uppsetningu:

-   Í Fjárhag
    -   Ef ætlunin er að nota greiðslubók þarf að setja upp greiðslubækur.
    -   Ef þú ætlar að keyra gengisbreytingar skaltu setja upp gjaldeyriskóða á **Gjaldmiðlar** síðu, setja upp gengistegundir á **Gengistegundir** síðu og settu upp gengi gjaldmiðla á **Gengi gjaldmiðla** síðu.
-   Í reiðufjár- og bankastjórnun, eru settir upp bankareikningar til þess að nota með greiðsluháttum.

## <a name="setup-pages-for-accounts-payable"></a>Uppsetningarsíður fyrir viðskiptaskuldir

Notið eftirfarandi síður til þess að setja upp grundvallaraðgerðir viðskiptaskulda fyrir hvert lögaðila. Síðum er raðað í ráðlagðri röð fyrir uppsetningu. Hægt er stofna sniðmát úr fyrstu færslunum sem eru stofnaðar, til þess að einfalda uppsetningarferlið. Í sniðmáti eru yfirleitt færslur færðar inn í mörgum svæðum til að endurspegla aðgerðirnar sem fyrirtækið vill innleiða fyrir tiltekna gerð lánardrottins.
1.  Á **Greiðsluskilmálar** síðu, skilgreina greiðsluskilmála sem þú úthlutar sölupantanir, innkaupapantanir, viðskiptavini og lánardrottna og sem ákvarða gjalddaga reikninga. Nánari upplýsingar er að finna í [Skilgreina greiðsluþóknanir lánardrottna](tasks/define-vendor-payment-fees.md).
2.  Á **Greiðslumáti - söluaðilar** síðu, búa til og viðhalda upplýsingum um hvernig fyrirtækið greiðir söluaðilum sínum.
3.  Á **Seljendahópar** síðu, búa til og viðhalda hópum lánardrottna sem deila mikilvægum færibreytum fyrir bókun, uppgjör og greiðslu, skýrslugerð og spá.
4.  Á **Birtingasnið söluaðila** síðu, skilgreina hvernig lánardrottnafærslur eru bókaðar í fjárhag.
5.  Á **Færibreytur viðskiptaskulda** síðu, setja upp sjálfgefnar stillingar sem eru notaðar ef ekki er tilgreind nákvæmari stilling, færibreytur fyrir ýmiss konar virkni og hinar ýmsu númeraraðir fyrir viðskiptaskuldir.
6.  Á **Uppsetning eyðublaðs** síðu, skilgreina snið ýmissa skjala sem tengjast lánardrottnum og sem fyrirtækið notar til að halda utan um kvittanir frá lánardrottnum og færa inn ástæður fyrir flæði greiðslna til lánardrottna.
7.  Á **Söluaðilar** síðu, stofna og viðhalda lánardrottinsreikningum og einnig skattyfirvöldum sem fyrirtæki þitt tilkynnir söluskatta til.

## <a name="optional-setup-pages-for-accounts-payable"></a>Valfrjálsar uppsetningarsíður fyrir viðskiptaskuldir
Auk grunnaðgerðum, hafa viðskiptaskuldir aðrar aðgerðir sem hægt er að setja upp.

Viðbótar uppsetningarsíður eru skipulagðar eftir aðgerðum.

**Reglur**
-   Á **Reikningsstefna söluaðila** síðu, settu upp reikningsreglur lánardrottins.

**Reikningsjöfnun**

-   Á **Heildarvikmörk reikninga** síðu, setja upp vikmörk fyrir heildartölur reikninga.
-   Á **Samsvörunarstefna** síðu, settu upp tvíhliða og þríhliða samsvörunarreglur.
-   Á **Verðvikmörk** síðu, setja upp vikmörk fyrir einingaverð.
-   Á **Vöruþolsflokkar** síðu, setja upp vikmörk fyrir vöruverð.
-   Á **Verðþolshópar söluaðila** síðu, setja upp vikmörk fyrir verð lánardrottna.
-   Á **Hleðsluvikmörk** síðu, setja upp vikmörk fyrir gjöld.

**Verkflæði**

-   Á **Verkflæði viðskiptaskulda** síðu, setja upp verkflæðisstillingar fyrir færslubókarsamþykki og innkaupabeiðnir.

**Ástæður**

-   Á **Ástæður söluaðila** síðu, settu upp ástæðukóða.

**Gjöld**

-   Á **Gjaldkóði** síðu, setja upp kóða fyrir gjöldin sem eru notuð í innkaupapöntunum.
-   Á **Seljandi gjöld hópur** síðu, búa til og viðhalda gjaldahópum fyrir söluaðila.
-   Á **Hlutagjaldaflokkar** síðu, búa til og viðhalda gjaldahópum fyrir hluti.
-   Á **Sjálfvirk gjöld** síðu, skilgreinið gjöldin sem eru sjálfkrafa úthlutað á pantanir.

**Fylgivörur**

-   Á **Viðbótarvöruflokkar - Seljandi** síðu, búa til og viðhalda viðbótarvöruflokkum fyrir lánardrottna.
-   Á **Viðbótarvöruflokkar - Birgðir** síðu, búa til og viðhalda viðbótarvöruflokkum fyrir vörur.

**Arðgreiðsla**

-   Á **Skilmálar afhendingar** síðu, búa til og viðhalda skilyrðum fyrir flutningi hlutar frá seljanda til kaupanda.
-   Á **Afhendingarmátar** síðu, búa til og viðhalda þeim flutningsaðferðum sem notaðar eru þegar pöntun er afhent frá seljanda til kaupanda.
-   Á **Áfangastaðakóðar** síðu, búa til og viðhalda auðkennum og lýsingum fyrir áfangastaði fyrir afhendingu.

**Skjámyndir**

-   Á **Form athugasemdir** síðu, búðu til staðlaðan texta sem birtist á ýmsum síðum.
-   Á **Formflokkunarfæribreytur** síðu, setja upp flokkunarröð fyrir beiðnir, kvittunarlista, fylgiseðla og reikninga.
-   Á **Uppsetning prentstjórnunar** síðu, setja upp prentstjórnunarupplýsingar fyrir frumrit og afrit af síðum.

**Greiðslur**

-   Á **Staðgreiðsluafsláttur** síðu, setja upp og hafa umsjón með skilmálum til að fá staðgreiðsluafslátt. Staðgreiðsluafsláttarkóðar eru tengdir lánardrottnum og notaðir í innkaupapöntunum.
-   Á **Greiðsluáætlanir** síðu, setja upp greiðsluáætlanir sem eru notaðar til að stjórna raðgreiðslum til lánardrottna.
-   Á **Greiðsludagar** síðu, skilgreinið greiðsludaga sem eru notaðir til að reikna út gjalddaga og tilgreinið greiðsludaga fyrir tiltekinn vikudag eða mánuð.
-   Á **Greiðslugjald** síðu, stofna og viðhalda greiðslugjöldum sem tengjast söluaðilum.
-   Á **Greiðsluleiðbeiningar** síðu, búa til og viðhalda greiðsluleiðbeiningum.

**Upplýsingar**

-   Á **Skilgreiningar á öldrunartímabili** síðu, setja upp notendaskilgreint bil sem eru notuð til að greina gjalddagadreifingu lánardrottnareikninga.
-   Á **Viðskiptagrein** síðu, búðu til viðskiptagreinakóða (LOB) sem eru úthlutaðir til lánardrottna.

**skattur 1099**

-   Á síðunni **1099-svæðin** staðfesta og uppfæra lágmarksupphæðir sem verður að skrá í skattstofa (IRS), samkvæmt nýjustu kröfum skattayfirvalda Bandaríkjanna.

## <a name="optional-setup-for-other-modules"></a>**Valfrjáls uppsetning fyrir aðrar kerfiseiningar**
**Fyrirtækisstjórnun**

-   Á **Númeraraðir** síðu, setja upp númeraraðarhópa fyrir reikningsnúmer.
-   Á eftirfarandi síðum skal setja upp upplýsingar um aðsetur:
    -   **Uppsetning aðseturs**
    -   **NAF-kóðar**
    -   **Flytja inn póstnúmer**

**Fjárhagur**

-   Á **Fjárhagsstærðir** síðu, setja upp fjárhagsvíddir.
-   Á eftirfarandi síðum skal setja upp skattaupplýsingar:
    -   **VSK-kóðar**
    -   **VSK-flokkar**
    -   **VSK-flokkar vöru**
    -   **Lykilflokkur**
    -   **Undanþágukóðar VSK**
    -   **Skattaumdæmi**
    -   **Skattayfirvöld**
    -   **Virðisaukaskatttímabil**

**Reiðufjár- og bankastjórnun**

-   Á **Tilgangskóðar greiðslu** síðu, settu upp **tilgangskóði Seðlabankans**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
