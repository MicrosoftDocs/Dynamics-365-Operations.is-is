---
title: Reikna vexti
description: Þessi verklýsing sýnir hvernig á að stofna, prenta og bóka vaxtanótur.
author: ShivamPandey-msft
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3b97515e29d04866172216fc29af9a8d992568276c5e01acd67ad9d0028ea0c5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6764360"
---
# <a name="process-interest"></a>Reikna vexti

[!include [banner](../../includes/banner.md)]

Þessi verklýsing sýnir hvernig á að stofna, prenta og bóka vaxtanótur. Þetta verkefni notar USMF-sýnifyrirtækið.


## <a name="set-up-interest-on-the-posting-profile"></a>Setja upp vexti fyrir bókunarregluna
1. Í **Skoðunarrúðu** ferðu í **Kerfiseiningar > Skuldir og innheimta > Uppsetning > Bókunarreglur viðskiptavina**.
2. Smellið á **Breyta**.
3. Í **Setja upp flýtiflipa**, í reitnum **Vaxtakóði** skaltu velja vaxtakóða úr fellivalmyndinni. Ef ekki á að reikna vexti fyrir færslur með þessari bókunarreglu, skilið eftir autt. Flýtiflipinn **Töflutakmarkanir** gerir þér kleift að breyta hvernig vextir eru unnir. Ef þetta svæði er stillt á Já eru vextir reiknast fyrir þessa bókunarreglu.  

## <a name="calculate-interest"></a>Reikna út vexti
1. Í **Skoðunarrúðu** ferðu í **Kerfiseiningar > Skuldir og innheimta > Vextir > Stofna vaxtanótur**.
2. Velja færslugerðir sem verður að reikna út vexti fyrir. Allar opnar færslur fyrir þessar gerðir verða teknar með í útreikningnum.  
3. Ef þú stillir **Vexti** á Já muntu reikna vaxtavexti. Hægt er að athuga lög um útreikningi á vaxtavöxtum áður en þessar færslur eru hafðar með.  
4. Í reitinn **Frá dagsetningu** skal færa inn dagsetningu sem vextirnir verða reiknaðir frá. Ef ekki er tiltekin **Frá dagsetningu** verður hætt við allar óbókaðar vaxtanótur og vextir verða endurreiknaðir frá færsludagsetningu.
5. Í reitinn **Til dagsetningar** skal færa inn dagsetningu sem vextirnir verða reiknaðir til.
6. Í reitnum **Nota virði frá** skal velja valkost. Í boði eru þrír valkostir fyrir bókunarreglu:
    - Reikningur – Nota bókunarreglu sem er úthlutað til reikning viðskiptavinar fyrir hverja vaxtanótu. 
    - Velja – Notið bókunarregluna sem valin var á svæðinu .
    - Færsla – Notið einstaka bókunarreglu úr færslum þar sem vextir eru reiknaðir fyrir hverja vaxtanótu. Færslur sem hafa ekki úthlutaða bókunarreglu nota bókunarreglu sem er tilgreind á svæðinu Fjárhagur og virðisaukaskattur í skjámyndinni Færibreytur viðskiptakrafna.  
7. Útvíkkaðu flýtiflipann **Færslur til að taka með**.
8. Smella á **Sía**.
9. Í svæðinu **Skilyrði** skal færa inn auðkenni viðskiptavinar. Til dæmis, færið inn ‚US-001'.
6. Smellt er á **OK**.
7. Smellt er á **OK**.

## <a name="print-interest-notes"></a>Prenta vaxtanótur
1. Í **Skoðunarrúðu** ferðu í **Kerfiseiningar > Skuldir og innheimta > Vextir > Endurskoða og vinna vaxtanótur**.
2. Í reitnum **Staða** er ‚Stofnað' valið.
3. Í reitnum **Prentað** skal velja 'Ekki prentað'.
4. Smelltu á **Prenta**.
5. Útvíkkaðu flýtiflipann **Færslur til að taka með**.
6. Smellt er á **OK**.
7. Lokið síðunni.

## <a name="post-the-interest-note"></a>Bóka vaxtanótu
1. Velja vaxtanótu sem er að tilbúin til bókunar (staða er stofnuð).
2. Smelltu á **bóka.**
3. Færð er inn bókunardagsetning fyrir vaxtanóta. Skal velja Já í stofna fjárhagsfærsla fyrir hverja vaxtanóta. Ef þú velur ekki já, safnast upp allir vextir á vaxtanóta til viðskiptavinarins og eru bókaðar á fjárhag í einni færslu.  
4. Útvíkkaðu flýtiflipann **Færslur til að taka með**.
5. Smellt er á **OK**.
6. Í reitnum **Staða** er ‚bókað' valið.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]