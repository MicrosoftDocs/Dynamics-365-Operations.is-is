---
title: Setja upp greiðsluþóknanir fyrir TDS-greiðslur til yfirvalda
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp greiðsluþóknanir sem eru innheimtar fyrir TDS-greiðslur til yfirvalda.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: b52331bb1c7a1bc2c764008112f3df9cc0385995
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023343"
---
# <a name="set-up-payment-fees-for-tds-authority-payments"></a>Setja upp greiðsluþóknanir fyrir TDS-greiðslur til yfirvalda

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er útskýrt hvernig á að setja upp greiðsluþóknanir sem eru innheimtar fyrir TDS-greiðslur til yfirvalda.

1. Farið í **Viðskiptaskuldir \> Greiðsluuppsetning \> Greiðsluþóknun**.

    [![Síða greiðsluþóknunar](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)

2. Veljið **Ný** til að stofna nýja greiðsluþóknun og færið inn nauðsynlegar upplýsingar.
3. Í reitnum **Gerð þóknunar** skal velja gerð greiðsluþóknunar:

    - **Engum**
    - **Vextir** – Vextir eru innheimtir á síðbúnum greiðslum sem eru greiddar lánardrottnayfirvaldi TDS.
    - **Önnur** – Önnur gjöld eru innheimt á síðbúnum greiðslum sem eru greiddar lánardrottnayfirvaldi TDS.

    Ef **Vextir** eða **Önnur** er valið verður reiturinn **Gjöld** sjálfkrafa stilltur á **Fjárhagur**.

4. Ef valið var **Vextir** eða **Önnur** í reitnum **Reitargerð**, í reitnum **Aðallykill**, skal velja fjárhagslykilinn til að bóka vextina eða önnur gjöld á.
5. Færið inn aðrar áskildar upplýsingar.
6. Á aðgerðasvæðinu skal velja **Uppsetning greiðsluþóknunar** til að opna síðuna **Uppsetning greiðsluþóknunar** þar sem hægt er að setja upp greiðsluþóknanir fyrir ýmsar samsetningar banka, greiðslumáta, greiðsluupplýsinga, gjaldmiðla og dagsetningarbila.

    [![Uppsetningarsíða greiðsluþóknunar](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)

7. Í flipanum **Yfirlit**, í reitnum **Flokkanir**, skal tilgreina hvaða banka er verið að setja upp greiðsluþóknun fyrir:

    - **Tafla** – Þóknunin er gild fyrir tiltekinn bankareikning.
    - **Flokkur** – Þóknunin er gild fyrir tiltekinn bankaflokk.
    - **Allir** – Þóknunin er gild fyrir alla bankareikninga.

8. Ef **Tafla** eða **Flokkur** var valið í reitnum **Flokkanir**, í reitnum **Bankavensl**, skal velja tiltekinn bankareikning eða bankaflokk sem verið er að setja upp greiðsluþóknun fyrir.
9. Í reitnum **Greiðslumáti** skal velja greiðsluaðferðina fyrir greiðsluþóknanir.
10. Í reitnum **Greiðsluupplýsingar** skal velja eða færa inn kóða greiðsluupplýsinga sem var búinn til á síðunni **Greiðsluupplýsingar**.
    - Greiðsluupplýsingar er notaður við rafræna sjóður greiðsluhættir flutning.
12. Í reitnum **Greiðslugjaldmiðill** skal velja gjaldmiðilinn sem virkjar þóknunina. Einungis færslur sem nota valinn gjaldmiðil geta virkjað þóknunina. Ef þessi reitur er skilinn eftir auður virkja allir gjaldmiðlar þóknunina.
13. Í reitnum **Prósenta/upphæð** skal velja útreikningsaðferðina. Valkostirnir eru **Upphæð**, **Prósenta** og **Tímabil**.
14. Í reitnum **Upphæð þóknunar** skal tilgreina upphæð þóknunar sem annaðhvort prósentu af greiðslu eða upphæð fyrir eina greiðslu.
15. Í reitnum **Gjaldmiðill þóknunar** skal tilgreina gjaldmiðilskóðann fyrir þóknunina.
16. Veljið flipann **Almennt** til að skoða eða breyta upplýsingunum fyrir valinn bankareikning.

    [![Almennt](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)

16. Í reitnum **Lágmark** skal færa inn lágmarksupphæð færslu sem virkjar þóknunina.
17. Í reitnum **Hámark** skal færa inn hámarksupphæð færslu sem virkjar þóknunina.
18. Í reitunum **Frá dagsetningu** og **Til dagsetningar** skal skilgreina dagsetningabil fyrir útreikning á þóknunum.
19. Í reitnum **Lágmarksþóknun** skal tilgreina upphæð þóknunar sem annaðhvort prósentu af greiðslu eða upphæð fyrir eina greiðslu.
20. Í reitnum **VSK-flokkur** skal velja VSK-flokkinn sem nota á við útreikning á virðisaukaskatti fyrir upphæð þóknunar.
21. Í reitnum **VSK-flokkur vöru** skal velja VSK-flokk vöru sem nota á við útreikning á virðisaukaskatti vöru fyrir upphæð þóknunar.
22. Veljið flipann **Tímabil**. 

    [![Tímabilsflipi](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)

23. Í reitnum **Dagar** skal færa inn fjölda daga á milli bókunardagsetningu (afsláttardagsetningu) greiðslunnar og gjalddaga eigin víxla.
24. Í reitnum **Prósenta/upphæð** skal velja hvort hafi verið tilgreint prósenta eða ákveðin upphæð.
25. Í reitnum **Upphæð þóknunar** skal færa inn upphæð þóknunar sem annaðhvort prósentu af greiðslu eða upphæð fyrir eina greiðslu.
26. Lokið síðunni **Uppsetning greiðsluþóknunar**.
27. Lokið síðunni **Greiðsluþóknun**.
