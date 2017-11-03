---
title: "aðgerðaleit"
description: "Þessi grein lýsir aðgerðaleit í Microsoft Dynamics 365 for Finance and Operations. Aðgerðleit hjálpar þér að finna og keyra aðgerðir á síðu."
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9b9bb0acc6f0dc1722c916f133eed766ffdd4cc8
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="action-search"></a>aðgerðaleit

[!include[banner](../includes/banner.md)]


Þessi grein lýsir aðgerðaleit í Microsoft Dynamics 365 for Finance and Operations. Aðgerðleit hjálpar þér að finna og keyra aðgerðir á síðu.

<a name="introduction"></a>Inngangur
------------

Síður í Microsoft Dynamics 365 for Finance and Operations birta fyrst og fremst skipanir í aðgerðarúðum, bæði í staðlaðri aðgerðarúðu sem birtist efst á síðunni og á verkfærastikum sem birtast í ýmsum köflum síðunnar. Í fyrri útgáfum leyfir Lykillábending þér að fá aðgang fljótt á einhvern hnappinn á aðgerðarúðum með því að ýta á Alt-takkann og síðan röð af stöfum. 

[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) Hins vegar eru lykilheilræði í gildandi útgáfu Finance and Operations ekki lengur tiltæk, en í þeirra stað kemur aðgerðaleitin. Þessi nýi eiginleiki gerir þér kleift að leita fljótt og keyra hnapp af einhverju af sýnilegu aðgerðarúðunum.

## <a name="using-action-search"></a>Notkun Aðgerðaleitar
Til að nota eiginleikann aðgerðaleið, fylgið þessum skrefum.

1.  Á Aðgerðasvæðinu skal smella á **aðgerðaleit** svæði. (**aðgerðaleit** inniheldur stækkunarglerstákn.)
2.  Slá öllum eða hluta af nafni hnapps sem þú vilt keyra. Þú getur einnig leitað með því að nota orð úr leið hnappsins. (Nánari upplýsingar má nálgast í næsta kafla þessarar greinar.) Yfirleitt, hnappur birtist ofarlega á lista yfir niðurstöður þegar búið er að slá inn tvo til fjóra stafi.
3.  Finna og keyra hnappurinn í lista yfir niðurstöður (með því að nota músina eða lyklaborð).

Eftir að hnappurinn er keyrður fer áhersla á síðustu stöðu á síðunni, þannig að hægt er að halda áfram að vinna. 

[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)

Einnig er hægt að hefja aðgerðaleit með því að ýta á Ctrl +/ eða Alt + Q. Styðjið á flýtilykli aftur til að snúa aftur áherslu að síðasta stað á síðunni.

## <a name="understanding-the-results-list"></a>Skilningur á lista yfir niðurstöður
Í Finance and Operations er oft nauðsynlegt að vita bæði staðsetningu og efni hnapps til að skilja tilgang þess hnapps til fulls. Þess vegna birtast viðbótarupplýsingar fyrir hvern hlut í listanum, til að hjálpa þér að skilja nákvæmlega hvaða hnappar birtast í listanum. Einkum er "slóð" hnappsins sýnd. Þessa slóð gætu innihaldið merki eftirfarandi eininga notendaviðmóts, eins og:

-   Flipinn aðgerðarúða.
-   Hnappaflokkur
-   Valmyndarhnapp (ef hnappurinn er inní valmyndarhnapp)
-   Skiltákn valmyndar (sé hnappurinn innan nefnds flokks innan valmyndarhnapps)
-   Flokkur eða flipa á síðu (til dæmis, heiti flýtiflipa)

Til dæmis, var fært inn **tot** í **aðgerðaleit** svæðinu og ert nú að skoða niðurstöður lista. Fyrsta færslan, fyrir hnapp sem er kallast **Samtala**, er upplýst. Hnappaslóðin **Sölupöntun** &gt; **Skoða** er einnig sýnd. Í hlutanum **Sölupöntun** af slóðinni sem samsvarar flipanum **Sölupöntun** í Aðgerðarúðunni, og **Skoða** hluti slóðar samsvarar **Skoða** flokk á þeim flipa. Á svipaðan hátt tilkynnir slóðin fyrir hnappinn **Heildarafsláttur** (**Selja** &gt; **Reikna út**) þér að hnappurinn sé staðsettur í flokknum **Reikna út** á flipanum **Selja** í aðgerðarúðunni. Þess vegna hjálpa þessar upplýsingar til við að skilja nákvæmlega hvaða hnappur verður ræstur af leitaraðgerð (ef valið er sá hnappur í lista yfir niðurstöður). 

[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png) 

Í fyrri dæmi sýna sýndi leitaraðgerð niðurstöðum úr staðlaða Aðgerðarúðu efst síðu. Hins vegar sýnir aðgerðaleit einnig niðurstöður úr sýnilegri verkfæraslám sem eru staðsettir í öðrum hlutum á síðu. Til dæmis er verið að leita að **lagerbirgðir** hnappi sem er staðsettur í **sölupantanalínum** flýtiflipa. Í þessu tilfelli tilkynnir slóð hnappsins í lista yfir niðurstöður (**sölupantanalínur** &gt; **Birgðir** &gt; **Skoða**) að þessi hnappur er staðsettur undir **Skoða** fyrirsögn á **Birgðir** valmyndarhnapp á í **sölupantanalínur** flýtiflipa. 

[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)

## <a name="action-search-vs-navigation-search"></a>Aðgerðaleita samanborið við flettingaleit
Aðgerðaleit er ætlað að finna og keyra aðgerðir á síðu, en sérstakt leitarkerfi er til að finna og fletta á síður í Finance and Operations. Fyrir frekari upplýsingar um þann möguleika, að sjá greinina [Flettingaleit](navigation-search.md).




