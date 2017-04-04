---
title: "aðgerðaleit"
description: "Þessi skrá lýsir leitaraðgerðina aðgerðir í Microsoft Dynamics 365 aðgerða. Leit aðgerð auðveldar leit og aðgerðir sem keyra á síðu."
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 689d8f9fb0501c5007db21d41f126737af77b89e
ms.lasthandoff: 03/31/2017


---

# <a name="action-search"></a>aðgerðaleit

Þessi skrá lýsir leitaraðgerðina aðgerðir í Microsoft Dynamics 365 aðgerða. Leit aðgerð auðveldar leit og aðgerðir sem keyra á síðu.

<a name="introduction"></a>Inngangur
------------

Síðurnar í Microsoft Dynamics 365 aðgerða sýna aðallega skipanir á Aðgerð Rúðunum staðlaða Aðgerðarúðuna sem birtist efst á síðu og verkfæraslár sem birtast í mismunandi hluta af síðunni. Í fyrri útgáfum eiginleiki Lykill Ábendingar láta að komast að allar hnappinn á Aðgerðarúðu með því að ýta á Alt lyklinum og síðan röð innheimtubréfa. 

[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) Hins vegar í gildandi útgáfu af Dynamics 365 fyrir Aðgerðir, Lykill Ábendingar eru ekki lengur tiltæk en hafa verið settir í aðgerðinni aðgerð leit. Þessi nýi eiginleiki gerir þér kleift að leita fljótt og keyra hnapp af einhverju af sýnilegu aðgerðarúðunum.

## <a name="using-action-search"></a>Notkun Aðgerðaleitar
Til að nota eiginleikann aðgerðaleið, fylgið þessum skrefum.

1.  Á Aðgerðasvæðinu skal smella á **aðgerðaleit** svæði. (**aðgerðaleit** inniheldur stækkunarglerstákn.)
2.  Gerð alla eða hluta á nafni hnappurinn sem á að keyra. Einnig er hægt að leita með orð úr á hnappinn "slóðina." (Frekari upplýsingar sjá hlutann næsta þessa þekkingarskráar.) Yfirleitt, hnappur birtist ofarlega lista yfir niðurstöður þegar verið er að slá tveggja á fjögurra stafa.
3.  Finna og keyra hnappurinn í lista yfir niðurstöður (með því að nota músina eða lyklaborð).

Eftir að hnappurinn er keyrður fer áhersla á síðustu stöðu á síðunni, þannig að hægt er að halda áfram að vinna. 

[![aðgerð-leit-svæði](./media/action-search-field.png)](./media/action-search-field.png)

Einnig er hægt að hefja aðgerðaleit með því að ýta á Ctrl +/ eða Alt + Q. Styðjið á flýtilykli aftur til að snúa aftur áherslu að síðasta stað á síðunni.

## <a name="understanding-the-results-list"></a>Skilningur á lista yfir niðurstöður
Oft í Dynamics 365 Aðgerðir, verður vitað staðsetningu og samhengi hnappinn skilja að fullu tilgangur sem hnappinn. Þess vegna viðbótarupplýsingar er sýnt fyrir hverja vöru í lista yfir niðurstöður, til að aðstoða við að skilja nákvæmlega hvaða hnappar birtast í listanum. Einkum er "slóð" hnappsins sýnd. Þessa slóð gætu innihaldið merki eftirfarandi eininga notendaviðmóts, eins og:

-   Flipinn aðgerðarúða.
-   Hnappaflokkur
-   Valmyndarhnapp (ef hnappurinn er inní valmyndarhnapp)
-   Skiltákn valmyndar (sé hnappurinn innan nefnds flokks innan valmyndarhnapps)
-   Flokkur eða flipa á síðu (til dæmis, heiti flýtiflipa)

Til dæmis, var fært inn **tot** í **aðgerðaleit** svæðinu og ert nú að skoða niðurstöður lista. Fyrsta færslan fyrir hnapp sem nefnist **Samtölur**, er auðkenndur. Slóð hnappinn **sölupöntun**&gt;**Skoða** er einnig sýnt. Í **sölupöntun** hluti slóð samsvarar á **sölupöntun** flipanum í Aðgerðarúðunni, og **Skoða** hluti slóð samsvarar á **Skoða** flokkinn á flipanum sem. Svipaðan hátt verður slóð á **heildarafslátt** hnappinn (**Selja**&gt;**Reikna**) tilkynnir þessi hnappur er staðsett í á **Reikna** flokkinn á í **Selja** flipanum í aðgerðarúðunni. Þess vegna þessar upplýsingar hjálpar til við að skilja nákvæmlega hvaða hnappinn verður ræst af leit aðgerð (ef valið er að hnappurinn listanum niðurstöður). 

[![leitar-svæði-með-gögn](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png) 

Í fyrri dæmi sýna sýndi leitaraðgerð niðurstöðum úr staðlaða Aðgerðarúðu efst síðu. Hins vegar sýnir aðgerðaleit einnig niðurstöður úr sýnilegri verkfæraslám sem eru staðsettir í öðrum hlutum á síðu. Til dæmis er verið leita í **lagerbirgðir** er staðsett hnappurinn í **sölupantanalínur** FastTab. Í þessu tilfelli er hnappurinn slóðina í lista yfir niðurstöður (**sölupantanalínur**&gt;**Birgðir**&gt;**Skoða**) tilkynnir þessi hnappur er geymd undir á **Skoða** fyrirsögn á í **Birgðir** valmyndarhnapp á í **sölupantanalínur** FastTab. 

[![á--birgðir](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)

## <a name="action-search-vs-navigation-search"></a>Aðgerðaleita samanborið við flettingaleit
Leit aðgerðin er ætluð til að finna og keyra aðgerðir á síðu, það er aðskildar leit ferli til að finna og fletta að síðurnar í Dynamics 365 fyrir Aðgerðir. Nánari upplýsingar um þá aðgerð í á [Yfirlitstegundar leit](navigation-search.md) grein.


