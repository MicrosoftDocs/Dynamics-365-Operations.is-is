---
title: Yfirlit yfir skilgreiningu viðskiptaskulda
description: Þessi grein lýsir þeim síðum sem þú notar til að setja upp grundvallaraðgerðir og valfrjálsar aðgerðir fyrir viðskiptaskuldir. Hún lýsir einnig uppsetningarskrefum sem þú verður að ljúka áður en þú byrjar að setja upp viðskiptaskuldir.
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
ms.openlocfilehash: bce5da0c9593bcfcfb9589f8fe7e09b8acd63726
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906533"
---
# <a name="configure-accounts-payable-overview"></a>Yfirlit yfir skilgreiningu viðskiptaskulda

[!include [banner](../includes/banner.md)]

Þessi grein lýsir þeim síðum sem þú notar til að setja upp grundvallaraðgerðir og valfrjálsar aðgerðir fyrir viðskiptaskuldir. Hún lýsir einnig uppsetningarskrefum sem þú verður að ljúka áður en þú byrjar að setja upp viðskiptaskuldir.

## <a name="prerequisites-for-accounts-payable-setup"></a>Skilyrði fyrir uppsetningu viðskiptaskulda

Áður en hægt er að setja upp viðskiptaskuldir, verður að ljúka eftirfarandi uppsetningu:

-   Í fjárhag:
    -   Ef ætlunin er að nota greiðslubók þarf að setja upp greiðslubækur.
    -   Ef ætlunin er að keyra gengisleiðréttingar þarf að setja upp gjaldmiðilskóða í síðuna **Gjaldmiðlum**, setja upp **gerðir gengis** og setja upp gengi gjaldmiðla á síðu **gengi Gjaldmiðils**.
-   Í reiðufjár- og bankastjórnun, eru settir upp bankareikningar til þess að nota með greiðsluháttum.

## <a name="setup-pages-for-accounts-payable"></a>Uppsetningarsíður fyrir viðskiptaskuldir

Notið eftirfarandi síður til þess að setja upp grundvallaraðgerðir viðskiptaskulda fyrir hvert lögaðila. Síðum er raðað í ráðlagðri röð fyrir uppsetningu. Hægt er stofna sniðmát úr fyrstu færslunum sem eru stofnaðar, til þess að einfalda uppsetningarferlið. Í sniðmáti eru yfirleitt færslur færðar inn í mörgum svæðum til að endurspegla aðgerðirnar sem fyrirtækið vill innleiða fyrir tiltekna gerð lánardrottins.
1.  Á síðunni **Greiðsluskilmálar**, Skilgreinið greiðsluskilmála sem er úthlutað á sölupantanir, innkaupapantanir og viðskiptavinur, og lánardrottna, og ákvarða gjalddaga reikninga. Nánari upplýsingar er að finna í [Skilgreina greiðsluþóknanir lánardrottna](tasks/define-vendor-payment-fees.md).
2.  Á síðunni **Greiðslumátar - síða lánardrottins** skal Stofna og viðhalda upplýsingar um hvernig fyrirtækið greiðir lánardrottnum.
3.  Á síðunni **Lánardrottnaflokkar**, stofnið og viðhaldið lánardrottnaflokkum sem deila mikilvægum færibreytum fyrir bókun, greiðslu og jöfnun, skýrslugerð og spár.
4.  Á síðunni **Bókunarreglur lánardrottins** skal skilgreina hvernig lánardrottnafærslur eru bókaðar í fjárhag.
5.  Á síðunni **Færibreytur viðskiptaskulda** skal setja upp sjálfgefnar stillingar sem eru notaðar ef nánari stillingar eru ekki tilgreindar, færibreytur fyrir ýmsar aðgerðir og ýmsar númeraraðir fyrir viðskiptaskuldir.
6.  Á síðunni **Uppsetning eyðublaða** skal skilgreina snið ýmissa skjala sem tengjast lánardrottnum og eru notuð innan fyrirtækisins til þess að rekja móttöku frá lánardrottnum og færa inn ástæður fyrir greiðsluflæði til lánardrottna.
7.  Á síðunni **Lánardrottnar** skal stofna og viðhalda lánardrottnalyklum, og einnig skattyfirvöldum sem fyrirtækið sendir VSK-skýrslur til.

## <a name="optional-setup-pages-for-accounts-payable"></a>Valfrjálsar uppsetningarsíður fyrir viðskiptaskuldir
Auk grunnaðgerðum, hafa viðskiptaskuldir aðrar aðgerðir sem hægt er að setja upp.

Viðbótar uppsetningarsíður eru skipulagðar eftir aðgerðum.

**Reglur**
-   Síðunni **Stefna fyrir reikning lánardrottins** skal setja upp stefna fyrir reikning lánardrottins.

**Reikningsjöfnun**

-   Á síðunni **Vikmörk samtalna reiknings** skal setja upp vikmörk fyrir heildarupphæð reiknings.
-   Á síðunni **Jöfnunarregla** skal setja upp tvíhliða og þríhliða jöfnunarreglur.
-   Á síðunni **Verðvikmörk** skal setja upp vikmörk fyrir einingarverð.
-   Á síðunni **Vikmarkaflokkar vöruverðs** skal setja upp vikmarkaflokkur fyrir vöruverð.
-   Á síðunni **Vikmarkaflokkar lánardrottnaverðs** skal setja upp vikmarkaflokkur fyrir lánardrottnaverð.
-   Á síðunni **Vikmörk gjalda** skal setja upp vikmörk fyrir gjöld.

**Verkflæði**

-   Á síðunni **Verkflæði viðskiptaskulda** skal setja upp verkflæðisskilgreiningar fyrir færslubókarsamþykktir og innkaupabeiðnir.

**Ástæður**

-   Á síðunni **Ástæður lánardrottins** skal setja upp ástæðukóða

**Gjöld**

-   Á síðunni **Gjaldakóði** skal setja upp kóða fyrir gjöld sem eru notaðir í innkaupapöntunum.
-   Á síðunni **Gjaldaflokkur lánardrottins** skal stofna og vinna með gjaldaflokka fyrir lánardrottna.
-   Á síðunni **Vörugjaldaflokkar** skal stofna og vinna með gjaldaflokka fyrir afurðir.
-   Á síðunni **Sjálfvirk gjöld** skal skilgreina gjöld sem eru sjálfvirkt úthlutað á pantanir.

**Fylgivörur**

-   Á **Fylgivöruflokkar - Lánardrottnar** síðunni, skal stofna og viðhalda fylgivöruflokkum fyrir lánardrottna.
-   Á **Fylgivöruflokkar - Birgðir** síðunni skal stofna og viðhalda fylgivöruflokkum fyrir afurðir.

**Arðgreiðsla**

-   Á síðunni **Afhendingarskilmálar** skal stofna og viðhalda skilmálum fyrir flutning vöru frá seljanda til kaupanda.
-   Á síðunni **Afhendingarmátar** skal stofna og vinna með aðferðir við flutning sem er notaður þegar pöntun er afhent frá seljanda til kaupanda.
-   Á síðunni **Áfangastaðarkóðar** skal stofna og viðhalda kennimerki og lýsingum fyrir afhendingaráfangastaði

**Skjámyndir**

-   Á síðunni **Athugasemdir eyðublaða** skal stofna staðlaðan texta sem birtist á ýmsum síðum.
-   Á síðunni **Röðunarfæribreytur eyðublaða** skal setja upp röðunarskipan fyrir beiðnir, innhreyfingarlista, fylgiseðla og reikninga.
-   Á **Uppsetning á prentstýringu** síðunni skal setja upp upplýsingar um prentstýringu fyrir frumrit og afrit af síðum.

**Greiðslur**

-   Á síðunni **Staðgreiðsluafslættir** skal setja upp og Stýra skilmála til að fá staðgreiðsluafsláttur. Staðgreiðsluafsláttarkóðar eru tengdir lánardrottnum og notaðir í innkaupapöntunum.
-   Á síðunni **Greiðsluáætlanir** skal setja upp greiðsluáætlun sem eru notaðar til að stjórna afborgunargreiðslum til lánardrottinn.
-   Á síðunni **Greiðsludagar** skaltu skilgreina greiðsludaga sem eru notaðir til þess að reikna gjalddaga og tilgreina greiðsludaga fyrir tiltekinn dag vikunnar eða mánaðarins.
-   Á síðunni **Greiðsluþóknun** skal stofna og viðhalda greiðsluþóknun sem tengist lánardrottinn.
-   Á síðunni **Greiðslufyrirmæli** skal stofna og viðhalda greiðslufyrirmælum.

**Upplýsingar**

-   Á síðunni **Skilgreiningar aldurstímabila** skal setja upp notendaskilgreind bil til þess að greina gjalddagadreifingu fyrir lánardrottinslykla.
-   Á síðunni **Atvinnugrein** skal stofna línu atvinnugreinakóða (LOB) sem eru úthlutað á lánardrottnum.

**skattur 1099**

-   Á síðunni **1099-svæðin** staðfesta og uppfæra lágmarksupphæðir sem verður að skrá í skattstofa (IRS), samkvæmt nýjustu kröfum skattayfirvalda Bandaríkjanna.

## <a name="optional-setup-for-other-modules"></a>**Valfrjáls uppsetning fyrir aðrar kerfiseiningar**
**Fyrirtækisstjórnun**

-   Á síðunni **Númeraraðir** skal setja upp númeraraðaflokka fyrir reikningsnúmera.
-   Á eftirfarandi síðum skal setja upp upplýsingar um aðsetur:
    -   **Uppsetning aðseturs**
    -   **NAF-kóðar**
    -   **Flytja inn póstnúmer**

**Fjárhagur**

-   Á síðunni **Fjárhagsvíddir** skal setja upp fjárhagsvíddir.
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

-   Á síðunni **Greiðslumálefnakóðar** síðunni skal setja upp **Málefnakóði seðlabanka**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
