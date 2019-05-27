---
title: Stofna innheimtubréfaröð
description: Notið þessa leiðarvísi fyrir verk til að stofna innheimtubréfaröð.
author: mikefalkner
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CollectionLetterCourse
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db5264f6d8d7723ff01d13e99728c2bfebcb4515
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567439"
---
# <a name="create-a-collection-letter-sequence"></a>Stofna innheimtubréfaröð

[!include [task guide banner](../../includes/task-guide-banner.md)]

Notið þessa leiðarvísi fyrir verk til að stofna innheimtubréfaröð. Þetta verkefni notar USMF-sýnifyrirtækið.

1. Fara í Skuldir og innheimta > Uppsetning > Setja upp innheimtubréfaröð.
2. Smellið á „Nýtt“.
3. Í svæðinu Kenni númeraraðarinnar skal færa inn kenni raðar sem mun standa fyrir röðina. Það verður notuð þegar þú setur upp bókunarreglu.
4. Sláið inn gildi í reitnum „Lýsing“.
    * Greiðsluskilmálar eru valfrjálsar. Ef fært er inn hér gildi, reikningur þóknunar innheimtubréfs nota þessar greiðsluskilmála í stað greiðsluskilmálar geymd með viðskiptavini.  
5. Í safn innheimtubréfs svæðinu, skal velja kóða fyrir fyrsta innheimtubréfið sem á að senda.
    * Fyrsta innheimtubréf er stofna samkvæmt gjalddagi á reikningur, gildi sem þú færa inn fyrir biðtími í svæði dagar á þessari línu, og aðrar upplýsingar sem þú færa inn á þessari línu.  
6. Sláið inn gildi í reitnum „Lýsing“.
    * Gjaldmiðill fyrir fyrir þóknun fær sjálfgildi í gjaldmiðli viðskiptavinar. Þessi gjaldmiðilskóði getur verið annað en gjaldmiðli reikningsins.  
7. Smella á bæta Við til að bæta við næsta innheimtubréf sem verða sendar í röðinni
    * Í mörgum tilvikum fyrsta innheimtubréfið er bara viðvörun. Hægt er að bæta þóknun ef þörf krefur.  
8. Í svæðinu kóði innheimtubréfs , veljið næsta innheimtubréf sem verða sendar í röðinni.
9. Í reitinn Lýsing skal slá inn gildi.
10. Velja tekjurreiknings se, verður notaður fyrir þóknanir í svæðinu aðallykill.
11. Færið inn gjöld sem verður krafinn þegar þessu innheimtubréfi er bókuð.
12. Í reitnum VSK-flokkur vöru skal smella á fellilistahnappinn til að opna leitina.
    * Veljið vsk-flokkur vöru ef þarf að reikna út vsk á þóknunina.  
13. Í listanum skal smella á tengilinn í valinni línu.
14. Færðu inn lágmarks gjaldfallna stöðu sem krafist er áður en innheimtubréf er sent.
15. Færið inn fjölda biðdaga sem verður leyft.
    * Þetta er fjöldi daga eftir gjalddag sem hægt er að mynda innheimtubréf. Gjalddagi sem er notað fyrir útreikning fer eftir stöðu innheimtubréfs í innheimtubréfaröðinni: ⦁ Biðtími fyrir innheimtubréf 1 stendur í samhengi við gjalddaga á reikningnum.  ⦁ Biðtími fyrir innheimtubréf 2 og hærri er miðaður við þá dagsetningu sem fyrri innheimtubréfið er bókað eða prentað, eftir því hvað var valið í svæðinu Uppfærslu kóða innheimtubréfs á síðunni Færibreytur viðskiptakrafna.  
16. Smella á bæta Við til að bæta við síðasta innheimtubréfs í röðinni.
    * Hægt er að bæta við allt að fimm kóðum innheimtubréfs fyrir röð innheimtubréfs.  
17. Í svæðinu kóði innheimtubréfs , veljið næsta innheimtubréf sem verða sendar í röðinni.
18. Í reitinn Lýsing skal slá inn gildi.
19. Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.
20. Færið inn tölu í svæðinu Þóknun í gjaldmiðli.
21. Í reitnum VSK-flokkur vöru skal smella á fellilistahnappinn til að opna leitina.
22. Í listanum skal smella á tengilinn í valinni línu.
23. Færið inn tölu í svæðinu Lágmarks gjaldfallna stöðu.
24. Í reitinn dagar skal slá inn númer.
25. Skal velja þennan gátreitur í stöðva viðskiptamaðurinn frá frekari afhendingum og reikningsfærsla.
    * Veljið Nei í Reikningsfærsla og afhending í bið svæðið á síðunni Viðskiptavinir til að opna fyrir lykilinn.  
26. Útvíkka hlutann Athugasemd.
27. Færið inn textann sem birtist innheimtubréfinu fyrir valda innheimtubréfakóða.
    * Hægt er að þýða þennan texta í á mörgum tungumálum með því að nota valmyndina Þýðingar yfir víxilkassanum.  

