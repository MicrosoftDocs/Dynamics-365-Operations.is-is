---
title: Skráning móttöku skilaðra vara
description: Þú getur skráð kvittun skilavara með því að nota skjámynd komuyfirlits eða skráningarblaða.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSArrivalOverview, InventTransRegister
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f4942e455350844ac5614e70fef21b37461540a6
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2022
ms.locfileid: "9017290"
---
# <a name="register-the-receipt-of-returned-items"></a>Skráning móttöku skilaðra vara 

[!include [banner](../includes/banner.md)]


Það eru tvær aðferðir til að skrá kvittun skilavara. Fyrri aðferðin er móttökuferli vöruhúss sem notar skjámyndina **Komuyfirlit**. Seinni aðferðin notar skjámyndina **Skráning**.

## <a name="register-the-receipt-of-returned-items-in-the-arrival-overview-form"></a>Skráning móttöku skilaðra vara í skjámyndinni komuyfirlit

Þú getur notað skjámyndina **Komuyfirlit** til að bera kennsl á skilaafhendingu eftir númeri vöruskilaheimildar (RMA-númer). Ef heiti færslubókar er skilgreint á flipanum **Uppsetning** og færslubókarlínur sem samsvara línunum sem eru valdar í skjámyndinni **Komuyfirlit** eru til verður nýr færslubókarhaus stofnaður þegar þú smellir á **Upphafskoma**.

1.  Smelltu á **Birgðastjórnun** \> **Reglubundið** \> **Komuyfirlit**.

2.  Í reitnum **Heiti uppsetningar** skal velja **Skilapöntun** og smella síðan á **Uppfæra**.
    

    > [!TIP]
    > <P>Hægt er að nota reitinn <STRONG>Svið</STRONG> til að þrengja leitarniðurstöðurnar. Þú getur slegið inn eða valið RMA-númerið í reitnum <STRONG>RMA-númer</STRONG> til að fá nákvæma niðurstöðu. Til að skilgreina og vista safn af síum sem takmarkar hvaða komur á innleið eru birtar skal smella á flipann <STRONG>Uppsetning</STRONG>. Tiltækar síur eru gerðir, vöruhús og dreifing.</P>

    

    > [!WARNING]
    > <P>Skilapöntunum er ekki hægt að blanda saman við aðrar komugerðir í skjámyndinni <STRONG>Komuyfirlit</STRONG>. Þess vegna verður tilvísunin alltaf sölupöntun, en ekkert sölupöntunarauðkenni verður tilgreint í færslubókarhausnum.</P>



3.  Í hnitanetinu **Kvittanir** skaltu finna línuna sem passar við vöruna sem er skilað og vellja síðan gátreitinn í dálkinum **Velja fyrir komu**.

4.  Til að útiloka ákveðnar línur frá vöruskilamóttökunni, eins og vörur í upprunalegu pöntuninni sem voru ekki teknar með í skilaafhendingunni, skal hreinsa tengda gátreitinn **Velja fyrir komu** í töflunni **Línur** í neðri hluta skjámyndarinnar.

5.  Smelltu á hnappinn **Upphafskoma** til að búa til komubók.
    

    > [!NOTE]
    > <P>Hægt er að velja margar skilapantanir í einu og hafa þær allar með í einu komuferli. Hver skilapöntunarlína verður afrituð í samsvarandi vörukomubókarlínu.</P>

    

    > [!NOTE]
    > <P>Þú getur einnig handvirkt búið til komubók með skjámyndinni <STRONG>Vörumóttaka</STRONG>. 



6.  Smelltu á **Birgðastjórnun** \> **Færslubækur** \> **Vörumóttaka** \> **Vörumóttaka**.

7.  Veldu komubókina sem þú stofnaðir rétt í þessu og smelltu síðan á **Línur** til að opna skjámyndina **Færslubókarlínur, staðsetningar**.

8.  Á flipanum **Almennt** skal stilla númerið í reitnum **Magn** ef þess er krafist og síðan úthluta ráðstöfunarkóða í reitnum **Ráðstöfunarkóði**.
    
    Að öðrum kosti er hægt að velja gátreitinn **Stjórnun biðgeymslu** til að senda skilavörurnar í skoðunarferli í tengslum við biðgeymslupöntun.
    

    > [!NOTE]
    > <P>Ef sendar eru endursendu vörurnar í gegnum biðgeymslu, er ekki hægt að tilgreina ráðstöfunarkóða.</P>



9.  Smellið á hnappinn **Sannprófa**.

10. Ef engar villur eru í staðfestingarferlinu skaltu smella á **Bóka**.

## <a name="register-the-receipt-of-returned-items-in-the-registration-form"></a>Skrá skal móttökuna á skilavörum á skjámyndinni Skráning

Til viðbótar við að nota skjámyndina **Komuyfirlit** getur þú notað skjámyndina **Skráning** til að skrá komu skilavara.

1.  Smelltu á **Sala og markaðsstarf** \> **Söluvöruskil** \> **Allar skilapantanir**. Stofna nýja skilapöntun eða opna vöruskilapöntunina frá listanum. Á flýtiflipanum **Línur** skal velja skilapöntunarlínuna. Smelltu á **Uppfæra línu** og smelltu síðan á **Skráning**.

2.  Úthlutaðu ráðstöfunarkóða í reitnum **Ráðstöfunarkóði** og smelltu síðan á **Í lagi**.
    

    > [!NOTE]
    > <P>Ekki er hægt að senda vöruna til skoðunar sem biðgeymslupöntun með skjámyndinni <STRONG>Skráning</STRONG>.</P>



3.  Í hnitanetinu **Færsla** skal velja færsluna sem á að skrá.

4.  Í hnitanetinu **Skrá núna** skal smella á **Bæta við**. Endurtaktu fyrri tvö skrefin þar til allar skilavörurnar birtast í hnitanetinu **Skrá núna**.

5.  Smelltu á **Bóka allt**.

## <a name="see-also"></a>Sjá einnig

[Komuyfirlit (skjámynd)](https://technet.microsoft.com/library/hh227654\(v=ax.60\))

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]