--- 
title: "Stofna rekstrartilföng"
description: "Rekstrartilföng framkvæmir verkþætti verks eða framleiðsluferli."
author: sorenva
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 12e4a93f908c348a848e056df00115bf2dc50635
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="create-an-operations-resource"></a>Stofna rekstrartilföng

[!include[task guide banner](../../includes/task-guide-banner.md)]

Rekstrartilföng framkvæmir verkþætti verks eða framleiðsluferli. Þessi ferli sýnir hvernig á að skilgreina gæðapöntun. Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.

1. Fara á tilföng
2. Smellið á „Nýtt“.
3. Í reitinn Tilfang skal slá inn gildi.
4. Sláið inn gildi í reitnum „Lýsing“.

## <a name="define-capacity-and-consumption-parameters"></a>Skilgreina afkastageta og notkunarfæribreytur
1. Stækka hlutann aðgerð.
2. Færið inn tölu í reitinn úrkastsprósenta.
3. Sláið inn eða veldu gildi í reitnum Setja upp flokkur.
    * Tilgreina kostnaðartegund sem skilgreinir hvernig á að gera grein fyrir kostnað við uppsetningu.  
4. Færa inn eða veljið gildi í reitinn flokkur keyrslutíma
    * Tilgreina kostnaðartegund sem skilgreinir hvernig á að gera grein fyrir kostnað við keyrslutíma.  
5. Sláið inn eða veldu gildi í reitnum magntegund.
    * Tilgreina kostnaðartegund sem skilgreinir hvernig á að gera grein kostnaði vegna tilfanga á grundvelli úttaksmagns.  
6. Í reitnum Eining afkastagetu skal velja valkost.
    * Tilgreinið eininguna til að sýna afkastagetu rekstrartilfanga.  
7. Í reitinn Afkastageta skal slá inn tölu.
8. Færið inn tölu í reitinn Skilvirkniprósenta.
    * Tilgreina skilvirkni sem búist er við frá rekstrartilföng. Skilvirkniprósenta leiðréttir gegnumstreymi rekstrartilfanga og hefur áhrif á tíma sem er frátekin fyrir tilfang.  
9. Færið inn tölu í Aðgerðaröðun prósentusvæðinu.
    * Tilgreinið hámarkshlutfall afkastagetu rekstrartilfanga sem á að nota í aðgerðaröðun.  
10. Veljið Já í svæðinu takmörkuð Afkastageta.
    * Þessi valkostur stilltur á Já ef rekstrartilföng skuli raðað á grundvelli raunverulega afkastagetu sem er tiltækt, og ef taka skal tillit til fyrirliggjandi frátekningar á afkastagetu. Ef þessi valkostur er stilltur á Nei,  er gert ráð fyrir að rekstrartilföng hafa ótakmarkaða afköst, og gæti tilföngin gætu verið yfirbókaður.  
11. Velja skal Já í svæðinu Flöskuhálstilfang.

## <a name="define-working-times"></a>Skilgreina vinnutíma
1. Stækka Dagatals hluta.
2. Smelltu á Bæta við.
3. Sláið inn eða veldu gildi í reitnum dagatal.
    * Tilgreina vinnutímadagatal sem skilgreinir afkastagetu (í klukkustundum) tilfanganna.  
4. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
5. Í listanum skal smella á tengilinn í valinni línu.

## <a name="define-resource-capabilities"></a>Skilgreina möguleika tilfanga
1. Útvíkka hlutann Getu.
2. Smelltu á Bæta við.
    * Geta er hæfni rekstrartilfanga til að framkvæma tiltekinn verkþátt. Röðunarvél úthlutar tilföng með því að láta tilfangaþörfum á hvern verkþátt samsvara getu tiltækar rekstrartilföng.  
3. Í reitinn Geta skal slá inn eða veldu gildi.
4. Í reitinn Stig skal slá inn númer.
    * Tilgreinið þá færni sem vinnur tilfang á getu.  
5. Í reitinn forgangur skal slá inn númer.
    * Tilgreinið forgang rekstrartilföng með tilliti til getu. Þegar er raðað eftir forgangi, rekstrartilföng með mesta forgang (lægsta tölugildi) er valið fyrst.  

## <a name="assign-resource-to-resource-group"></a>Úthluta tilföngum á tilfangaflokk
1. Útvíkka hlutann tilfangaflokkur.
2. Smelltu á Bæta við.
    * Tilfangaflokkurinn skilgreinir svæði, framleiðslueiningu og samhengi vöruhúss fyrir rekstrartilföngum. Aðeins er hægt að raða rekstrartilföng þegar þeim er úthlutað á tilfangaflokk , og aðeins á svæði þar sem tilfangaflokkurinn er staðsettur.  
3. Í reitinn tilfangaflokkur skal slá inn eða velja gildi.
4. Sláðu inn eða veldu gildi Innsláttur reitnum Staðsetning inntaks.
    * Tilgreina staðsetningu vöruhúss þar sem rekstrartilföng er að nota efni.  


