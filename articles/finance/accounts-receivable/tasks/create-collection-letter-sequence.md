---
title: Stofna innheimtubréfaröð
description: Notið þetta ferli fyrir verk til að stofna innheimtubréfaröð.
author: JodiChristiansen
ms.date: 12/07/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CollectionLetterCourse
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af5d0a001fbe705834e116516933be67f2de8826
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734159"
---
# <a name="create-a-collection-letter-sequence"></a>Stofna innheimtubréfaröð

[!include [banner](../../includes/banner.md)]

Notið þetta ferli fyrir verk til að stofna innheimtubréfaröð. Þetta verkefni notar USMF-sýnifyrirtækið.

1. Fara til **Inneign og innheimtur > Uppsetning > Setja upp innheimtubréfaröð**.
2. Smellt er á **Nýtt**.
3. Í reitnum **Röð innheimtubréfa** skal færa inn kenni raðar sem mun standa fyrir röðina. Það verður notuð þegar þú setur upp bókunarreglu.
4. Í reitinn **Lýsing** skal slá inn gildi. Greiðsluskilmálar eru valfrjálsar. Ef fært er inn hér gildi, reikningur þóknunar innheimtubréfs nota þessar greiðsluskilmála í stað greiðsluskilmálar geymd með viðskiptavini.  
5. Í reitnum **Kóði innheimtubréfas** skal velja kóða fyrir fyrsta innheimtubréfið sem á að senda. Fyrsta innheimtubréf er stofna samkvæmt gjalddagi á reikningur, gildi sem þú færa inn fyrir biðtími í svæði dagar á þessari línu, og aðrar upplýsingar sem þú færa inn á þessari línu.  
6. Í reitinn **Lýsing** skal slá inn gildi. 
7. Sjálfgefinn gjaldmiðill fyrir gjaldið er gjaldmiðill lögaðilans. Þessi gjaldmiðilskóði getur verið annað en gjaldmiðli reikningsins.   
8. Smelltu á **Bæta við** til að bæta við næsta innheimtubréf sem verður sent í röðinni. Í mörgum tilvikum fyrsta innheimtubréfið er bara viðvörun. Hægt er að bæta þóknun ef þörf krefur.  
9. Í reitnum **Kóði innheimtubréfs** velurðu næsta innheimtubréf sem verður sent í röðinni.
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
25. Veldu gátreitinn **Vaið** til að stöðva viðskiptamanninn í því að bæta við frekari afhendingum og reikningsfærslum. Til að opna reikninginn skaltu velja **Nei** í **Innheimta og afhending í bið** sviði á **Viðskiptavinir** síðu.  
26. Útvíkkaðu flýtiflipann **Athugasemd**.
27. Færið inn textann sem birtist innheimtubréfinu fyrir valda innheimtubréfakóða. Þú getur þýtt þennan texta á mörg tungumál með því að nota **Þýðingar** valmynd fyrir ofan athugasemdareitinn.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
