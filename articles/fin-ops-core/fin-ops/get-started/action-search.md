---
title: Aðgerðaleit
description: Þessi grein lýsir aðgerðaleit. Aðgerðleit hjálpar þér að finna og keyra aðgerðir á síðu.
author: jasongre
manager: AnnBe
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b5d2e678b01f052db29d5a1c47eae27d27cd04f
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694189"
---
# <a name="action-search"></a>Aðgerðaleit

[!include [banner](../includes/banner.md)]

Þessi grein lýsir aðgerðaleit. Aðgerðleit hjálpar þér að finna og keyra aðgerðir á síðu.

## <a name="introduction"></a>Inngangur

Síður birta fyrst og fremst skipanir í aðgerðarúðum, bæði í staðlaðri aðgerðarúðu sem birtist efst á síðunni og á verkfærastikum sem birtast í ýmsum köflum síðunnar. Í fyrri útgáfum leyfir Lykillábending þér að fá aðgang fljótt á einhvern hnappinn á aðgerðarúðum með því að ýta á Alt-takkann og síðan röð af stöfum.

[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)

Lykilráð eru ekki lengur tiltæk en þeim hefur verið skipt út fyrir aðgerðaleitareiginleikann. Þessi nýi eiginleiki gerir þér kleift að leita fljótt og keyra hnapp af einhverju af sýnilegu aðgerðarúðunum.

## <a name="using-action-search"></a>Notkun Aðgerðaleitar

Til að nota eiginleikann aðgerðaleið, fylgið þessum skrefum.

1. Á Aðgerðasvæðinu skal smella á **aðgerðaleit** svæði. (reiturinn **aðgerðaleit** inniheldur stækkunarglerstákn.)
2. Slá öllum eða hluta af nafni hnapps sem þú vilt keyra. Þú getur einnig leitað með því að nota orð úr leið hnappsins. (Nánari upplýsingar má nálgast í næsta kafla þessarar greinar.) Yfirleitt, hnappur birtist ofarlega á lista yfir niðurstöður þegar búið er að slá inn tvo til fjóra stafi.
3. Finna og keyra hnappurinn í lista yfir niðurstöður (með því að nota músina eða lyklaborð).

Eftir að hnappurinn er keyrður fer áhersla á síðustu stöðu á síðunni, þannig að hægt er að halda áfram að vinna.

[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)

Einnig er hægt að hefja aðgerðaleit með því að ýta á Ctrl +/ eða Alt + Q. Styðjið á flýtilykli aftur til að snúa aftur áherslu að síðasta stað á síðunni.

## <a name="understanding-the-results-list"></a>Skilningur á lista yfir niðurstöður

Oft er nauðsynlegt að vita bæði staðsetningu og efni hnapps til að skilja tilgang þess hnapps til fulls. Þess vegna birtast viðbótarupplýsingar fyrir hvern hlut í listanum, til að hjálpa þér að skilja nákvæmlega hvaða hnappar birtast í listanum. Einkum er "slóð" hnappsins sýnd. Þessa slóð gætu innihaldið merki eftirfarandi eininga notendaviðmóts, eins og:

- Flipinn aðgerðarúða.
- Hnappaflokkur
- Valmyndarhnapp (ef hnappurinn er inní valmyndarhnapp)
- Skiltákn valmyndar (sé hnappurinn innan nefnds flokks innan valmyndarhnapps)
- Flokkur eða flipa á síðu (til dæmis, heiti flýtiflipa)

Til dæmis, var fært inn **tot** í **aðgerðaleit** svæðinu og ert nú að skoða niðurstöður lista. Fyrsta færslan, fyrir hnapp sem er kallast **Samtala**, er upplýst. Hnappaslóðin **Sölupöntun** &gt; **Skoða** er einnig sýnd. Í hlutanum **Sölupöntun** af slóðinni sem samsvarar flipanum **Sölupöntun** í Aðgerðarúðunni, og **Skoða** hluti slóðar samsvarar **Skoða** flokk á þeim flipa. Á svipaðan hátt tilkynnir slóðin fyrir hnappinn **Heildarafsláttur** (**Selja** &gt; **Reikna út**) þér að hnappurinn sé staðsettur í flokknum **Reikna út** á flipanum **Selja** í aðgerðarúðunni. Þess vegna hjálpa þessar upplýsingar til við að skilja nákvæmlega hvaða hnappur verður ræstur af leitaraðgerð (ef valið er sá hnappur í lista yfir niðurstöður).

[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)

Í fyrri dæmi sýna sýndi leitaraðgerð niðurstöðum úr staðlaða Aðgerðarúðu efst síðu. Hins vegar sýnir aðgerðaleit einnig niðurstöður úr sýnilegri verkfæraslám sem eru staðsettir í öðrum hlutum á síðu. Til dæmis er verið að leita að **lagerbirgðir** hnappi sem er staðsettur í **sölupantanalínum** flýtiflipa. Í þessu tilfelli tilkynnir slóð hnappsins í lista yfir niðurstöður (**sölupantanalínur** &gt; **Birgðir** &gt; **Skoða**) að þessi hnappur er staðsettur undir **Skoða** fyrirsögn á **Birgðir** valmyndarhnapp á í **sölupantanalínur** flýtiflipa.

[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)

> [!NOTE]
> Það eru nokkrir hnappar sem birtast ekki í aðgerðaleit. Meðal þeirra eru fellivalmyndarhnappar og hnappar úr undirskjámyndum. 

## <a name="action-search-vs-navigation-search"></a>Aðgerðaleita samanborið við flettingaleit

Aðgerðaleit er ætlað að finna og keyra aðgerðir á síðu, en sérstakt leitarkerfi er til að finna og fletta á síður. Fyrir frekari upplýsingar um þann möguleika, að sjá greinina [Flettingaleit](navigation-search.md).
