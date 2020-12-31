---
title: Stofna innheimtubréfaröð
description: Notið þessa leiðarvísi fyrir verk til að stofna innheimtubréfaröð.
author: mikefalkner
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CollectionLetterCourse
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5d8aa4963026ad55ed3dfccb28b6cc68a872f326
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444275"
---
# <a name="create-a-collection-letter-sequence"></a>Stofna innheimtubréfaröð

[!include [banner](../../includes/banner.md)]

Notið þessa leiðarvísi fyrir verk til að stofna innheimtubréfaröð. Þetta verkefni notar USMF-sýnifyrirtækið.

1. Í skoðunarrúðunni ferðu í **Kerfi > Skuldir og innheimta > Uppsetning > Setja upp röð innheimtubréfa**.
2. Smellt er á **Nýtt**.
3. Í reitnum **Röð innheimtubréfa** skal færa inn kenni raðar sem mun standa fyrir röðina. Það verður notuð þegar þú setur upp bókunarreglu.
4. Í reitinn **Lýsing** skal slá inn gildi.  Greiðsluskilmálar eru valfrjálsar. Ef fært er inn hér gildi, reikningur þóknunar innheimtubréfs nota þessar greiðsluskilmála í stað greiðsluskilmálar geymd með viðskiptavini.  
5. Í reitnum **Kóði innheimtubréfas** skal velja kóða fyrir fyrsta innheimtubréfið sem á að senda. Fyrsta innheimtubréf er stofna samkvæmt gjalddagi á reikningur, gildi sem þú færa inn fyrir biðtími í svæði dagar á þessari línu, og aðrar upplýsingar sem þú færa inn á þessari línu.  
6. Í reitinn **Lýsing** skal slá inn gildi. Gjaldmiðill fyrir fyrir þóknun fær sjálfgildi í gjaldmiðli viðskiptavinar. Þessi gjaldmiðilskóði getur verið annað en gjaldmiðli reikningsins.  
7. Smelltu á **Bæta við** til að bæta við næsta innheimtubréf sem verður sent í röðinni. Í mörgum tilvikum fyrsta innheimtubréfið er bara viðvörun. Hægt er að bæta þóknun ef þörf krefur.  
8. Í svæðinu kóði innheimtubréfs , veljið næsta innheimtubréf sem verða sendar í röðinni.
9. Í reitinn **Lýsing** skal slá inn gildi.
10. Í reitnum **Aðallykill** velurðu tekjureikninginn sem verður notaður fyrir þóknanir.
11. Færið inn gjöld sem verður krafinn þegar þessu innheimtubréfi er bókuð.
12. Í reitnum **VSK-flokkur vöru** skal smella á fellilistahnappinn til að opna leitina. Veljið vsk-flokkur vöru ef þarf að reikna út vsk á þóknunina.  
13. Í listanum skal smella á tengilinn í valinni línu.
14. Í reitnum **Lágmarksupphæð vanskila** slærðu inn þá lágmarksupphæð vanskila sem krafist er áður en innheimtubréf er sent.
15. Í reitinn **Dagar** færirðu inn fjölda biðdaga sem verður leyfður. Þetta er fjöldi daga eftir gjalddag sem hægt er að mynda innheimtubréf. Gjalddagi sem er notaður fyrir útreikning fer eftir stöðu innheimtubréfs í innheimtubréfaröðinni:
    - Biðtími fyrir innheimtubréf 1 stendur í samhengi við gjalddaga á reikningnum.
    - Biðtími fyrir innheimtubréf 2 og hærri er miðað við þá dagsetningu sem fyrri innheimtubréfið er bókaður eða prentaður, eftir því hvað var valið í Uppfærslu kóða innheimtubréfs svæðið á síðunni færibreytur viðskiptakrafna.  
16. Smelltu á **Bæta við** til að bæta við síðasta innheimtubréfinu í röðinni. Hægt er að bæta við allt að fimm kóðum innheimtubréfs fyrir röð innheimtubréfs.  
17. Í reitnum **Kóði innheimtubréfs** velurðu næsta innheimtubréf sem verður sent í röðinni.
18. Í reitinn **Lýsing** skal slá inn gildi.
19. Í reitnum **Aðallykill** skal skilgreina æskileg gildi.
20. Færið inn tölu í reitnum **Þóknun í gjaldmiðli**.
21. Í reitnum **VSK-flokkur vöru** skal smella á fellilistahnappinn til að opna leitina.
22. Í listanum skal smella á tengilinn í valinni línu.
23. Færið inn tölu í reitnum **Lágmarksupphæð vanskila**.
24. Í reitinn **Dagar** skal slá inn númer.
25. Veldu gátreitinn **Vaið** til að stöðva viðskiptamanninn í því að bæta við frekari afhendingum og reikningsfærslum. Veljið **Nei** í Reikningsfærsla og afhending í bið svæðið á síðunni Viðskiptavinir til að opna fyrir lykilinn.  
26. Útvíkkaðu flýtiflipann **Athugasemd**.
27. Færið inn textann sem birtist innheimtubréfinu fyrir valda innheimtubréfakóða. Hægt er að þýða þennan texta í á mörgum tungumálum með því að nota valmyndina Þýðingar yfir víxilkassanum.  

