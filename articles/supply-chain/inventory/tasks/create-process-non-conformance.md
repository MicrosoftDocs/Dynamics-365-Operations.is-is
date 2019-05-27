---
title: Stofna og vinna úr samræmi
description: Notaðu þetta ferli til að framkvæma stjórnun ósamkvæmis, samkvæmt fyrirliggjandi gæðapöntun.
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16ed11bce92920fe8240fc85f706a2ac6ab0a04b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572812"
---
# <a name="create-and-process-a-conformance"></a>Stofna og vinna úr samræmi

[!include [task guide banner](../../includes/task-guide-banner.md)]

Notaðu þetta ferli til að framkvæma stjórnun ósamkvæmis, samkvæmt fyrirliggjandi gæðapöntun. Hægt er að keyra þessa skráningu í sýnifyrirtækinu USMF og nota ráðlögð gildi. Þetta ferli er yfirleitt framkvæmt af starfsmanni á sviði gæða.  Frumskilyrði er að keyra verkskráninguna ‚Skoða gæði vara‘. Til að keyra samþykki á ósamkvæmi verður notandi sem keyrir verkskráninguna að hafa „Heiti“ úthlutað á síðunni Notendur. Til að nota athugasemdir skjals verður notandinn einnig að hafa skjalaafgreiðslu virkjaða í valkostum notanda.


## <a name="select-a-quality-order"></a>Velja gæðapöntun.
1. Fara á Gæðapantanir.
2. Í listanum skal merkja valda línu.
    * Veldu gæðapöntunina sem var stofnuð úr verkskráningunni „Skoða gæði vara“.  

## <a name="create-a-nonconformance"></a>Stofna ósamkvæmistilvik
1. Smellt er á Fyrirspurnir.
2. Smellt er á Ósamkvæmnistilvik.
3. Smellið á „Nýtt“.
4. Í reitnum Vandamálagerðir skal smella a fellilistahnappinn til að opna leitina.
    * Veldu vandamálið sem fannst við eftirlitsferlið.  
5. Í reitnum Vandamálagerðir skal smella a fellilistahnappinn til að opna leitina.
6. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
7. Í listanum skal smella á tengilinn í valinni línu.
8. Smellið á „Í lagi“.

## <a name="approvereject-a-nonconformance"></a>Samþykkja/hafna ósamkvæmistilviki
1. Smellið á Aðgerðir.
2. Smellt er á Samþykkja ósamkvæmnistilvik.
    * Í þessu dæmi samþykkirðu ósamkvæmina. Hægt er að tengja samþykkta ósamkvæmi tengdri virkni til að skrá vinnu sem er lokið sem hluti af afgreiðslu ósamkvæmi og, eins og í þessari verkskráningu, vinnslu á afgreiðslu leiðréttinga.  
3. Smella á Já.

## <a name="create-a-correction-action"></a>Stofna leiðréttingaraðgerð
1. Smellt er á Leiðréttingar.
2. Smellið á „Nýtt“.
3. Í listanum skal merkja valda línu.
4. Í reitnum Starfsmannanúmer skal smella á fellilistahnappinn til að opna leitina.
5. Í listanum skal smella á tengilinn í valinni línu.
6. Smellið á Velja.
7. Smellt er á Hengja við.
    * Stofna athugasemd um leiðréttinguna. Fyrir þetta dæmi er aðgerð að hafa samband við lánardrottininn til að  ræða ósamkvæmitilvikið.  
8. Smellið á „Nýtt“.
9. Smellt er á Athugasemd.
    * Athugaðu að, eftir því hvernig uppsetning skýrslunnar er, hægt er að prenta mismunandi skjalategundir á skýrslum sem eru tengdar stjórnun á ósamkvæmi.  
10. Sláið inn gildi í reitnum „Lýsing“.
11. Lokið síðunni.

## <a name="maintain-a-correction"></a>Viðhalda leiðréttingu
1. Smellt er á Merkja sem lokið.
2. Smellið á „Í lagi“.
3. Lokið síðunni.

## <a name="close-a-nonconformance"></a>Loka ósamkvæmistilviki
1. Smellið á Aðgerðir.
2. Smellt er á Loka ósamkvæmnistilviki.
3. Smella á Já.
4. Lokið síðunni.
5. Lokið síðunni.
