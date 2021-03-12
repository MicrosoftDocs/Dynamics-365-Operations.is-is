---
title: Rafræn skilaboð
description: Þetta efnisatriði veitir yfirlit og upplýsingar um uppsetningu fyrir rafræn skilaboð í Microsoft Dynamics 365 Finance.
author: ShylaThompson
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: d4ecc29e47d68129df424c4212505413cf6c8889
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968980"
---
# <a name="electronic-messaging"></a>Rafræn skilaboð

[!include [banner](../includes/banner.md)]

Þetta efnisatriði veitir yfirlit og upplýsingar um uppsetningu fyrir rafræn skilaboð.

Ríkisstjórnir og löggjafarvald í hinum ýmsu löndum og svæðum um allan heim hafa nýlega innleitt skýrslukröfur fyrir fyrirtæki sem eru skráð í þessum löndum og svæðum. Tilgangur kröfunnar er að gera það mögulegt að fá gögn frá þessum fyrirtækjum á rafrænu formi, beint frá kerfinu þar sem þau voru skráð, vistuð og unnin.

Virknin fyrir rafræn skilaboð í Finance styður ýmsa ferla rafrænnar samaðgerðar milli Finance og kerfanna sem ríkisstjórnir og löggjafarvald bjóða upp á hvað varðar skýrslugerð, afhendingu og móttöku á opinberum upplýsingum.

Virknin fyrir rafræn skilaboð er samþætt við eininguna **Rafræn skýrslugerð**. Því er hægt að setja upp snið rafrænnar skýrslugerðar fyrir rafræn skilaboð. Frekari upplýsingar eru í [Rafræn skýrslugerð](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting).

Rafræn skilaboð byggjast á eftirfarandi einingum:

- **Rafræn skilaboð** – Skýrsla eða yfirlýsing sem ber að tilkynna og/eða senda innbyrðis. Eitt dæmi er skýrsla sem er send til skattstofu.
- **Atriði rafrænna skilaboða** – Færslur sem ber að hafa með í skilaboðunum sem eru skráð.
- **Úrvinnsla rafrænna skilaboða** – Röð aðgerða sem ber að keyra til að safna saman nauðsynlegum gögnum, búa til skýrslur, vista gögn í blob-geymslu Microsoft Azure, flytja skýrslur út fyrir kerfið, fá viðbrögð utan kerfis og, á grundvelli móttekinna upplýsinga, uppfæra gagnagrunninn. Aðgerðirnar í röðinni geta verið annaðhvort tengdar eða ótengdar

Eftirfarandi skýringarmynd sýnir flæði gagna fyrir rafræn skilaboð.

![Gagnaflæði rafrænna skilaboða](media/electronic-messaging-data-flow.png)

Virkni rafrænna skilaboða styður eftirfarandi aðstæður:

- Stofna skilaboð og gera skýrslur handvirkt sem byggjast á útflutningstengdum sniðum rafrænnar skýrslugerðar af ýmsum gerðum: Microsoft Excel, XML, JavaScript Object Notation (JSON), PDF, texta og Microsoft Word.
- Stofna og vinna úr skilaboðum sjálfvirkt sem tengjast upplýsingum sem óskað var eftir og voru fengin frá yfirvöldum í gegnum útflutningstengt snið rafrænnar skýrslugerðar.
- Safna og vinna úr upplýsingum úr gagnaveitu sem skilaboðaatriði. Gagnagjafinn tafla í Finance.
- Geyma viðbótarupplýsingar og meta ýmis gildi með því að kalla á sérstaklega skilgreinda keyranlega klasa í tengslum við skilaboð eða skilaboðaatriði.
- Safna saman upplýsingum sem eru fengin í skilaboðaatriðum, skipta þeim upplýsingum eftir skilaboðum, og búa til skýrslur sem eru á útflutningstengdum sniðum rafrænnar skýrslugerðar.
- Senda skýrslurnar sem eru búnar til á vefþjónustu með því að nota öryggisupplýsingar sem eru geymdar í Azure-lyklageymslu.
- Fá svar frá vefþjónustu, túlka svarið og uppfæra gögn í Finance, eftir því sem við á.
- Geyma og yfirfara allar skýrslur sem eru búnar til.
- Geyma og yfirfara allar kladdaupplýsingar sem tengjast aðgerðum sem eru keyrðar fyrir skilaboð eða skilaboðaatriði.
- Stjórna vinnslu í gegnum ýmsar stöður skilaboða og skilaboðaatriða.

## <a name="set-up-electronic-messaging"></a>Setja upp rafræn skilaboð

Rafræn skilaboð auðveldað það að viðhalda mismunandi ferlum rafrænnar skýrslugerðar fyrir mismunandi skjalategundir. Í sumum flóknum aðstæðum eru rafræn skilaboð sett upp svo þau séu með samsetningu af mörgum skilaboðastöðum, stöðum skilaboðaatriða, aðgerðum, öðrum svæðum og keyranlegum klösum. Í þessum tilfellum er innflutningur á gagnaeiningapökkum í boði. Ef þessir gagnaeiningapakkar eru notaðir ætti að flytja þá inn í lögaðila með verkfæri gagnastjórnunar. Frekar upplýsingar um hvernig á að nota verkfæri gagnastjórnunar eru í [Gagnastjórnun](../../dev-itpro/data-entities/data-entities-data-packages.md).

Hægt er að setja upp virknina fyrir rafræn skilaboð handvirkt ef gagnaeiningapakki er ekki fluttur inn. Í þessu tilfelli þarf að setja upp eftirfarandi þætti:

- [Númeraraðir](#number-sequences)
- [Gerðir og stöður skilaboðaatriða](#message-item-types-and-statuses)
- [Stöður skilaboða](#message-statuses)
- [Önnur svæði](#additional-fields)
- [Keyranlegar klasastillingar](#executable-class-settings)
- [Fylla út færsluaðgerðir](#populate-records-actions)
- [Vefforrit](#web-applications)
- [Stillingar vefþjónustu](#web-service-settings)
- [Úrvinnsluaðgerðir skilaboða](#message-processing-actions)
- [Rafræn skilaboð í vinnslu](#electronic-message-processing)

Eftirfarandi hlutar veita frekari upplýsingar um hvern þátt fyrir sig.

### <a name="number-sequences"></a>Númeraraðir

Setja upp númeraraðir fyrir bæði skilaboð og skilaboðaatriði. Númeraraðir eru notaðar til að sjálfkrafa gefa skilaboðum og skilaboðaatriðum númer. Úthlutuð númer verða notuð sem einkvæm auðkenni fyrir skilaboðin og skilaboðaatriðin í kerfinu. Hægt er að setja upp númeraraðir fyrir rafræn skilaboð á síðunni **Færibreytur fjárhags** (**Fjárhagur** \> **Uppsetning fjárhags** \> **Færibreytur fjárhags**).

### <a name="message-item-types-and-statuses"></a>Gerðir og stöður skilaboðaatriða

Gerðir skilaboðaatriða bera kennsl á færslutegundir sem verða notaðar í rafrænum skilaboðum. Hægt er að setja upp gerðir skilaboðaatriða á síðunni **Gerðir skilaboðaatriða** (**Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Gerðir skilaboðaatriða**).

Stöður skilaboðaatriða bera kennsl á stöðurnar sem verða notaðar í skilaboðaatriðum í vinnslunni sem verið er að setja upp. Hægt er að setja upp gerðir skilaboðaatriða á síðunni **Stöður skilaboðaatriða** (**Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Stöður skilaboðaatriða**).

Færibreytan **Leyfa eyðingu** fyrir stöðu skilaboðaatriðis skilgreinir hvort notendur geti eytt skilaboðaatriðum sem eru með þessa stöðu á síðunni **Rafræn skilaboð** eða á síðunni **Rafræn skilaboðaatriði**.

### <a name="message-statuses"></a>Stöður skilaboða

Setja upp stöður skilaboða sem eiga að vera tiltæk í vinnslu skilaboða. Hægt er að setja upp stöður skilaboða á síðunni **Stöður skilaboða** (**Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Stöður skilaboða**).

Eftirfarandi tafla lýsir reitunum á síðunni **Skilaboðastöður**.

| Svæðisheiti          | Lýsing |
|---------------------|-------------|
| Staða boða      | Færið inn einkvæmt heiti fyrir stöðu skilaboðs. Skilaboðastöður eru notaðar til að einkenna stöðu rafrænna skilaboða á hverju augnabliki fyrir sig. Nafnið sem þú slærð inn birtist á síðunni **Rafræn skilaboð** og í kladda sem tengist rafrænum skilaboðum. |
| Lýsing         | Færa inn lýsingu á skilaboðastöðunni. |
| Gerð svars       | Velja gerð svars fyrir stöðu skilaboðs. Sumar aðgerðir í vinnslu geta gefið af sér fleiri en eina gerð svars. Til dæmis geta aðgerðir af gerðinni **Vefþjónusta** gefið svör af annaðhvort gerðinni **Framkvæmd heppnaðist** eða gerðinni **Tæknileg villa**, fer eftir niðurstöðu keyrslunnar. Í þessu tilviki er nauðsynlegt að skilgreina skilaboðastöður fyrir báðar svargerðirnar. Frekari upplýsingar um gerðir aðgerða og gerðir svara sem tengjast þeim er að finna í [Gerðir úrvinnsluaðgerðar skilaboða](#message-processing-action-types). |
| Staða skilaboðaatriðis | Stundum verður staða á rafrænum skilaboðum að hafa áhrif á stöðu tengdra skilaboðaatriða. Veldu stöðu skilaboðaatriðis í þessum reit til að tengja hana við skilaboðastöðu. |
| Leyfa eyðingu        | Veldu þennan reit ef notendur ættu að geta eytt rafrænum skilaboðum sem hafa þessa stöðu á síðunni **Rafræn skilaboð**. |

### <a name="additional-fields"></a>Önnur svæði

Virknin fyrir rafræn skilaboð gerir þér kleift að fylla út færslur úr færslutöflu. Þannig er hægt að undirbúa færslurnar fyrir skýrslugerð og síðan tilkynna þær. Hins vegar hafa færslutöflur stundum ekki nægar upplýsingar til að fylla út færslur á þann hátt að það uppfylli kröfur um skýrslugjöf. Til að fylla út allar upplýsingar sem þarf að tilkynna um færslu er hægt að setja upp önnur svæði. Önnur svæði geta tengst bæði skilaboðum og skilaboðaatriðum. Hægt er að setja upp önnur svæði á síðunni **Önnur svæði** (**Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Önnur svæði**).

Eftirfarandi tafla lýsir almennu svæðunum á síðunni **Önnur svæði**.

| Svæði       | Lýsing |
|-------------|-------------|
| Svæðisheiti  | Sláið inn heiti á viðbótareigind skilaboðaatriða sem tengjast vinnslunni. Þetta heiti birtist í notandaviðmótinu á meðan unnið er í vinnslunni. Einnig er hægt að nota það í stillingum rafrænnar skýrslugerðar sem tengjast vinnslunni. |
| Lýsing | Færa inn lýsingu á viðbótarsvæði. |
| Breyting notanda   | Stilla skal þennan valkost á **Já** ef notendur eiga að geta breytt gildinu á viðbótarsvæðinu úr notandaviðmótinu. |
| Teljari     | Stilltu þennan valkost í **Já** ef viðbótarsvæðið á að innihalda númeraröð í rafrænum skilaboðum. Gildi viðbótarsvæðisins verður fyllt út sjálfkrafa við keyrslu á aðgerð af gerðinni **Útflutningur rafrænna skýrslna**. |
| Falið      | Stilltu þennan valkost á **Já** ef viðbótarsvæðið á að vera falið í notandaviðmótinu. |

Sérhvert viðbótarsvæði getur haft mismunandi gildi fyrir vinnsluna. Þú skilgreinir þessi gildi í flýtiflipanum **Gildi**. Eftirfarandi tafla lýsir svæðunum.

| Svæði                | Lýsing |
|----------------------|-------------|
| Svæðisgildi          | Sláið inn svæðisgildi sem er notað fyrir skilaboð eða skilaboðaatriði við skýrslugerð. |
| Lýsing          | Færið inn lýsingu á gildi svæðisins. |
| Reikningsgerð         | Sum gildi svæða kunna að takmarkast við tilteknar lyklagerðir. Veljið eitt af eftirfarandi gildum: **Allar**, **Viðskiptamaður** eða **Lánardrottinn**. |
| Kóði lykils         | Ef þú valdir **Viðskiptamaður** eða **Lánardrottinn** í reitnum **Lykilgerð** er hægt að takmarka frekar notkun svæðisgildis við tilgreindan flokk eða töflu. |
| Númer lykils/flokks | Ef þú valdir **Viðskiptamaður** eða **Lánardrottinn** í reitnum **Lykilgerð** og ef þú færðir inn flokk eða töflu í reitinn **Kóði lykils** er hægt að færa inn tilgreindan flokk eða umboðsaðila í þennan reit. |
| Virkt            | Tilgreina dagsetningu þegar byrja á að taka tillit til gildisins. |
| Lok gildistíma           | Tilgreina dagsetningu þegar hætta á að taka tillit til gildisins. |

Sjálfgefið er að samsetningar af skilyrðum sem eru skilgreindar af svæðunum **Númer lykils/flokks**, **Kóði lykils**, **Virkt** og **Lok gildistíma** hafi ekki áhrif á valið á gildum fyrir önnur svæði. Hins vegar geta þessar samsetningar verið notaðar í keyrsluhæfum klasa til að innleiða tiltekna reiknireglu sem reiknar út gildi fyrir önnur svæði.

### <a name="executable-class-settings"></a>Keyranlegar klasastillingar

Keyranlegur klasi er X++ aðferð eða klasi sem úrvinnsla rafrænna skilaboða getur kallað á í tengslum við aðgerð ef þörf er á einhverju mati á ferlinu.

Hægt er að setja upp keyranlegan klasa handvirkt á síðunni **Keyranlegar klasastillingar** (**Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Keyranlegar klasastillingar**). Stofnið línu og stillið eftirfarandi svæði.

| Svæði                 | lýsing |
|-----------------------|-------------|
| Keyranlegur klasi      | Sláið inn heiti sem verður notað við uppsetningu á úrvinnsluaðgerð skilaboða sem klasinn þessu tengdur er kallaður. |
| lýsing           | Færið inn lýsingu á keyranlegum klasa. |
| Keyranlegt klasaheiti | Veljið X++ keyranlegan klasa. |
| Framkvæmdastig       | Þetta svæði er stillt sjálfkrafa vegna þess að gildið á að vera forskilgreint fyrir valdan keyranlegan klasa. Þetta svæði takmarkar stigið sem tengt mat er keyrt á. |
| Lýsing klasa     | Þetta svæði er stillt sjálfkrafa vegna þess að gildið á að vera forskilgreint fyrir valdan keyranlegan klasa. |

Sumir keyrsluhæfir klasar kunna að hafa áskildar færibreytur sem verður að skilgreina áður en keyrsluhæfur klasi er keyrður í fyrsta skipti. Til að skilgreina þessar færibreytur skal velja **Færibreytur** í aðgerðarúðunni, stilla svæðin í svarglugganum sem birtist og síðan velja **Í lagi**. Mikilvægt er að velja **Í lagi**. Annars vistast færibreyturnar ekki í gagnagrunninum og ekki verður kallað rétt á keyrsluhæfa klasann.

### <a name="populate-records-actions"></a>Fylla út færsluaðgerðir

„Fylla út færsluaðgerðir“ er notuð til að setja upp aðgerðir sem bæta færslum við töflu skilaboðaatriða svo hægt sé að bæta þeim við rafræn skilaboð. Ef rafrænu skilaboðin verða til dæmis að gefa skýrslu um reikninga viðskiptamanns er nauðsynlegt að setja upp aðgerð til að fylla út færslur sem tengist reitnum **Gagnaveita** í töflunni Reikningabók viðskiptavinar. Hægt er að setja upp „fylla út færsluaðgerðir“ á síðunni **Fylla út færsluaðgerðir** (**Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Fylla út færsluaðgerðir**). Stofnið nýja færslu fyrir hverja aðgerð sem á að bæta færslum við töflu, og stillið eftirfarandi svæði.

| Svæði       | Lýsing |
|-------------|-------------|
| Nafn        | Færið inn heiti á aðgerð sem fyllir út færslur í vinnslunni. |
| Lýsing | Færið inn lýsingu á aðgerð sem fyllir út færslur. |

Á flýtiflipanum **Uppsetning gagnagjafa** skal bæta við línu fyrir hvern gagnagjafa sem er notaður í vinnslunni, og stilla skal eftirfarandi svæði.

| Svæði                  | lýsing |
|------------------------|-------------|
| Nafn                   | Færið inn heiti á gagnaveitu. |
| Gerð skilaboðaatriðis      | Veljið gerð skilaboðaatriðis sem á að nota þegar færslur eru búnar til fyrir gagnaveitu. |
| Lykilgerð           | Veljið lykilgerð sem á að tengjast færslum úr gagnaveitu. |
| Aðaltöfluheiti      | Veldu töfluna sem ætti að vera gagnagjafi. |
| Reitur skjalnúmers  | Veljið reitinn í valdri töflu þar sem taka á skjalanúmerið úr. |
| Dagsetningarreitur skjals    | Veljið reitinn í valdri töflu þar sem taka á dagsetningu skjals úr. |
| Reikningsreitur skjals | Veljið reitinn í valdri töflu þar sem taka á lykil skjals úr. |
| Fyrirspurn notanda             | Ef þessi gátreitur er valinn er hægt að setja upp fyrirspurn með því að velja **Breyta fyrirspurn** fyrir ofan hnitanetið. Annars verða allar færslur útfylltar úr valdri gagnaveitu. |

### <a name="web-applications"></a>Vefforrit

Þú notar stillingar fyrir vefforrit til að setja upp vefforrit þannig að það styður Open Authorization (OAuth) 2.0. OAuth er opinn staðall sem gerir notendum kleift að veita „öruggan úthlutaðan aðgang“ að forritinu fyrir þeirra hönd, án þess að deila aðgangsupplýsingum þeirra. Einnig er hægt að fara í gegnum heimildarferlið með því að fá heimildarkóða og aðgangslykil. Hægt er að setja upp stillingar vefforrits á síðunni **Vefforrit** (**Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Vefforrit**).

Eftirfarandi tafla lýsir svæðunum á síðunni **Vefforrit**.

| Svæði                        | Lýsing |
|------------------------------|-------------|
| Heiti forrits             | Færið inn heiti á vefforritinu. |
| Lýsing                  | Færið inn lýsingu á vefforritinu. |
| Grunnvefslóð                     | Færið inn grunnveffangið fyrir vefforritið. |
| Vefslóð heimildar       | Tilgreindu slóðina sem er notuð til að búa til vefslóð heimildar. |
| Vefslóð merkis               | Tilgreindu slóðina sem er notuð til að búa til vefslóð merkis. |
| Framsendingarslóð                 | Færið inn vefslóð áframsendingar. |
| Biðlarakenni                    | Færið inn biðlarakenni vefforritsins. |
| Leynilykill biðlara                | Færið inn leynilykil biðlara fyrir vefforritið. |
| Þjónsmerki                 | Færið inn þjónsmerki vefforritsins. |
| Sniðsvörpun heimildar | Veljið snið rafrænnar skýrslugerðar sem er notað til að búa til beiðni um heimild. |
| Flytja inn líkanavörpun merkis   | Veljið líkanavörpun fyrir innflutning rafrænnar skýrslugerðar sem er notuð til að geyma aðgangslykil. |
| Veitt umfang                | Umfangið sem veitt fyrir beiðnir um forritið. Þessi reitur er uppfærður sjálfkrafa. |
| Aðgangsmerki rennur út eftir  | Eftirstandandi tími áður en aðgangslykillinn rennur út. | 
| Samþykkja                       | Tilgreinið eiginleikann **Samþykkja** fyrir vefbeiðnina. Færið til dæmis inn **application/vnd.hmrc.1.0+json**. |
| Gerð innihalds                 | Tilgreina gerð innihalds. Færið til dæmis inn **application/json**. |

Að auki eru eftirfarandi hnappar í boði á aðgerðasvæði síðunnar **Vefforrit** til að styðja heimildarferlið:

- **Fá heimildarkóða** - Frumstilla heimild vefforritsins.
- **Fá aðgangslykil** - Frumstilla ferlið til að fá aðgangslykil.
- **Endurnýja aðgangslykil** - Endurnýja aðgangslykil.

Þegar aðgangslykill að vefforriti er vistaður í gagnagrunni kerfisins á dulrituðu sniði, er hægt að nota hann fyrir beiðnir að vefþjónustu. Í öryggisskyni skal aðgangur að aðgangslykli takmarkast við þau öryggishlutverk sem verður að heimila að taka á þessum beiðnum. Ef notendur utan öryggisflokksins reyna að taka á beiðni fá þeir villu sem gefur til kynna að þeir séu ekki með leyfi til að vinna með valið vefforrit. Til að setja upp öryggishlutverk sem verða að hafa aðgang að aðgangslykli skal nota flýtiflipann **Öryggishlutverk** á síðunni **Vefforrit**. Ef öryggishlutverk eru ekki skilgreind fyrir vefforrit getur aðeins kerfisstjórinn unnið í gegnum þetta vefforrit.

### <a name="web-service-settings"></a>Stillingar vefþjónustu

Stillingar vefþjónustu eru notaðar til að setja upp beinan gagnaflutning til vefþjónustu. Hægt er að setja upp stillingar vefþjónustu á síðunni **Stillingar vefþjónustu** (**Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Stillingar vefþjónustu**).

Eftirfarandi tafla lýsir svæðunum á síðunni **Stillingar vefþjónustu**.

| Svæði                          | lýsing |
|--------------------------------|-------------|
| Vefþjónusta                    | Færið inn heiti á vefþjónustunni. |
| lýsing                    | Færið inn lýsingu á vefþjónustunni. |
| Internet-fang               | Færið inn veffangið á vefþjónustunni. Ef vefforrit er tilgreint fyrir vefþjónustuna, og ef veffang vefþjónustunnar er það sama og veffangið sem er skilgreint fyrir þetta vefforrit, skal velja **Afrita grunnvefslóð** til að afrita grunnvefslóð vefforritsins í þennan reit. |
| Skírteini                    | Veljið vottorð lyklageymslu sem hefur verið sett upp áður. |
| Vefforrit                | Veljið vottorð lyklageymslu sem hefur verið sett upp áður. |
| Gerð svars – XML        | Stillið þennan valkost á **Já** ef gerð svars er XML. |
| Aðferð beiðni                 | Tilgreinið aðferð beiðninnar. HTTP skilgreinir safn af beiðnum sem gefa til kynna aðgerðina sem á að framkvæma fyrir tiltekin tilföng. Aðferð beiðninnar getur verið **GET**, **POST** eða önnur HTTP-aðferð. |
| Haus beiðni                | Tilgreina haus beiðni. Haus beiðni er HTTP-haus sem hægt er að nota í HTTP-beiðni og sem tengist ekki innihaldi skilaboðanna. |
| Samþykkja                         | Tilgreinið eiginleikann **Samþykkja** fyrir vefbeiðnina. |
| Samþykkja kóðun                | Tilgreina gildið **Samþykkja kóðun**. HTTP beiðnishaus fyrir samþykki kóðunar gefur kóðun innihalds til kynna sem biðlarinn getur skilið. Þessi kóðun innihalds er venjulega þjappað reiknirit. |
| Gerð innihalds                   | Tilgreina gerð innihalds. HTTP-haus fyrir einingu innhaldsgerðar gefur til kynna miðilsgerð tilfanga. |
| Svarkóði tókst       | Tilgreindu HTTP-stöðukóðann sem gefur til kynna að beiðnin hafi heppnast. |
| Sniðsvörpun síðuhausa fyrir beiðnir | Veldu snið rafrænnar skýrslugerðar sem er notað til að búa til hausa fyrir vefbeiðnir. |

### <a name="message-processing-actions"></a>Úrvinnsluaðgerðir skilaboða

Úrvinnsluaðgerðir skilaboða eru notaðar til að stofna aðgerðir fyrir vinnslurnar og til að setja upp færibreytur þeirra. Hægt er að setja upp úrvinnsluaðgerðir á síðunni **Úrvinnsluaðgerðir skilaboða** (**Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Úrvinnsluaðgerðir skilaboða**).

Eftirfarandi töflur lýsa svæðunum á síðunni **Úrvinnsluaðgerðir skilaboða**.

#### <a name="general-fasttab"></a>Flýtiflipinn Almennt

| Svæði                       | lýsing |
|-----------------------------|-------------|
| Gerð aðgerðar                 | Veljið þessa gerð aðgerðar. Upplýsingar um tiltæka valkosti eru í kaflanum [Gerðir úrvinnsluaðgerða skilaboða](#message-processing-action-types). |
| Sniðsvörpun              | Veljið snið rafrænnar skýrslugerðar sem á að kalla á fyrir aðgerðina. Þetta svæði er aðeins í boði fyrir aðgerðir af gerðunum **Útflutningur á rafrænum skýrslum**, **Innflutningur á rafrænum skýrslum** og **Útflutningsskilaboð rafrænna skýrslna**. |
| Sniðsvörpun fyrir vefslóð | Veljið snið rafrænnar skýrslugerðar sem á að kalla á fyrir aðgerðina. Þetta svæði er aðeins í boði fyrir aðgerðir af gerðinni **Vefþjónusta**. Það er notað til að búa til slóð vefslóðarinnar sem verður bætt við grunnveffangið sem er tilgreint fyrir valinn vefþjón. |
| Gerð skilaboðaatriðis           | Veljið færslugerðir sem meta á aðgerðina fyrir. Þetta svæði er aðeins í boði fyrir aðgerðir af gerðunum **Framkvæmdastig skilaboðaatriða**, **Útflutningur á rafrænum skýrslum**, **Innflutningur á rafrænum skýrslum** og **Vefþjónusta** og einnig fyrir nokkrar aðrar gerðir. Ef þetta svæði er skilið eftir autt verða allar gerðir skilaboðaatriða metnar sem eru skilgreindar fyrir úrvinnslu skilaboða. |
| Keyranlegur klasi            | Veljið keyranlegar klasastillingar sem hafa verið stofnaðar áður. Þetta svæði er aðeins í boði fyrir aðgerðir af gerðunum **Framkvæmdastig skilaboðaatriða** og **Framkvæmdastig skilaboðaatriða**. |
| Fylla út færsluaðgerð     | Veljið áður uppsetta aðgerð sem fyllir út færslur. Þetta svæði er aðeins í boði fyrir aðgerðir af gerðinni **Fylla út færslur**. |
| Vefþjónusta                 | Veljið vefþjónustu sem var áður sett upp. Þetta svæði er aðeins í boði fyrir aðgerðir af gerðinni **Vefþjónusta**. |
| Skrárnafn                   | Tilgreinið heiti skráar sem verður niðurstaða aðgerðarinnar. Þessi skrá getur verið svarið frá vefþjóninum eða skýrslunni sem myndast. Þetta svæði er aðeins í boði fyrir aðgerðir af gerðunum **Vefþjónusta** og **Útflutningsskilaboð rafrænna skýrslna**. |
| Sýna svarglugga                 | Stilltu þennan valkost á **Já** ef sýna þarf notendum svarglugga áður en skýrsla er gerð. Þetta svæði er aðeins í boði fyrir aðgerðir af gerðinni **Útflutningsskilaboð rafrænna skýrslna**. |

##### <a name="message-processing-action-types"></a>Gerðir úrvinnsluaðgerðar skilaboða

Eftirfarandi valkostir eru í boði í svæðinu **Gerð aðgerðar**:

- **Stofna skilaboð** – Notið þessa gerð aðgerðar til að leyfa notendum að stofna skilaboð handvirkt á síðunni **Rafræn skilaboð**. Ekki er hægt að setja upp upphafsstöðu fyrir aðgerð af þessari gerð.
- **Fylla út færslur** - Aðgerð af gerðinni **Fylla út færslur** verður að hafa verið sett upp. Tengja þessa gerð aðgerðar við aðgerð sem fyllir út færslur svo sú aðgerð verði með í vinnslunni. Gert er ráð fyrir að þessi gerð aðgerðar sé notuð annaðhvort fyrir fyrstu aðgerðina í úrvinnslu skilaboða (þegar engin rafræn skilaboð eru búin til fyrirfram) eða fyrir aðgerð sem bætir skilaboðaatriðum við eldri skilaboð með aðgerð af gerðinni **Búa til skilaboð**. Fyrir aðgerðir af þessari gerð er þar af leiðandi aðeins hægt að setja upp lokastöðu fyrir skilaboðaatriði. Eingöngu er hægt að setja upp upphafsstöðu fyrir skilaboð.
- **Framkvæmdastig skilaboða** – Notið þessa gerð aðgerðar til að setja upp keyranlegan klasa sem á að vera metinn á skilaboðastigi.
- **Framkvæmdastig skilaboðaatriða** – Notið þessa gerð aðgerðar til að setja upp keyranlegan klasa sem á að vera metinn á stigi skilaboðaatriða.
- **Útflutningur á rafrænum skýrslum** – Notið þessa gerð aðgerðar fyrir aðgerðir sem eiga að búa til skýrslu sem miðast við skilgreiningu á útflutningi á rafrænum skýrslum á stigi skilaboðaatriða.
- **Útflutningsskilaboð rafrænna skýrslna** – Notið þessa gerð aðgerðar fyrir aðgerðir sem eiga að búa til skýrslu sem miðast við skilgreiningu á útflutningi á rafrænum skýrslum á skilaboðastigi (til dæmis þegar skilaboð eru ekki með nein skilaboðaatriði).
- **Innflutningur á rafrænum skýrslum** – Notið þessa gerð aðgerðar fyrir aðgerðir sem eiga að búa til skýrslu sem miðast við skilgreiningu á innflutningi á rafrænum skýrslum.
- **Úrvinnsla notanda á skilaboðastigi** – Notið þessa gerð aðgerðar fyrir aðgerðir sem gera ráð fyrir nokkrum handvirkum aðgerðum notanda á skilaboðastigi. Til dæmis gæti notandi uppfært stöðu skilaboða.
- **Úrvinnsla notanda** – Notið þessa gerð aðgerðar fyrir aðgerðir sem gerir ráð fyrir nokkrum handvirkum aðgerðum notanda á stigi skilaboðaatriðis. Til dæmis gæti notandi uppfært stöðu skilaboðaatriða.
- **Vefþjónusta** – Notið þessa gerð aðgerðar fyrir aðgerðir sem eiga að senda myndaða skýrslu til vefþjónustu. Þessi gerð aðgerðar er ekki notuð fyrir skýrslugerð ítalskra innkaupa- og sölureikningasamskipta. Fyrir aðgerðir af gerðinni **Vefþjónusta** inniheldur síðan **Úrvinnsluaðgerðir skilaboða** flýtiflipann **Ýmsar upplýsingar** þar sem hægt er að tilgreina staðfestingartexta. Þessi staðfestingartexti verður sýndur notendum áður en tekið er á beiðnum valinnar vefþjónustu.
- **Beiðni um sannprófun** – Notið þessa gerð aðgerðar til að óska eftir sannprófun frá þjóni.

#### <a name="initial-statuses-fasttab"></a>Flýtiflipi fyrir upphafsstöður

> [!NOTE]
> Flýtiflipinn **Upphafsstöður** er ekki í boði fyrir aðgerðir sem eru með upphafsgerð aðgerðar **Stofna skilaboð**.

| Svæði               | Lýsing |
|---------------------|-------------|
| Staða skilaboðaatriðis | Veljið stöðu skilaboðaatriðis sem á að meta valda úrvinnsluaðgerð skilaboða fyrir. |
| lýsing         | Lýsing á stöðu valins skilaboðaatriðis. |

#### <a name="result-statuses-fasttab"></a>Flýtiflipi fyrir lokastöður

| Svæði               | lýsing |
|---------------------|-------------|
| Staða skilaboða      | Veljið stöðu skilaboða sem á að meta valda úrvinnsluaðgerð skilaboða fyrir. Þetta svæði er aðeins í boði fyrir úrvinnsluaðgerðir skilaboða sem eru metnar á skilaboðastigi. Það er til dæmis í boði fyrir aðgerðir af gerðunum **Útflutningur rafrænna skýrslna** og **Innflutningur rafrænna skýrslna** en það er ekki í boði fyrir aðgerðir af gerðunum **Úrvinnsla notanda** og **Framkvæmdastig skilaboðaatriðis**. |
| lýsing         | Lýsing á stöðu valinna skilaboða. |
| Gerð svars       | Gerð svars fyrir valda stöðu skilaboða. |
| Staða skilaboðaatriðis | Veljið stöðurnar sem eiga að vera tiltækar eftir matið á úrvinnsluaðgerð valinna skilaboða. Þetta svæði er aðeins í boði fyrir úrvinnsluaðgerðir skilaboða sem eru metnar á stigi skilaboðaatriða. Það er til dæmis í boði fyrir aðgerðir af gerðunum **Úrvinnsla notanda** og **Framkvæmdastig skilaboðaatriða**. Fyrir úrvinnsluaðgerðir skilaboða sem eru metnar á skilaboðastigi, sýnir þetta svæði stöðu skilaboðaatriðis sem var sett upp fyrir valda stöðu skilaboða. |

Eftirfarandi tafla sýnir lokastöðurnar sem verður að setja upp fyrir mismunandi gerðir aðgerða og svargerðir.

| Gerð aðgerðar/svars fyrir rafræn skilaboð | Framkvæmt | Viðskiptavilla | Tæknileg villa | Notandaskilgreint | Hætta við |
|----------------------------------------------|-----------------------|----------------|-----------------|--------------|--------|
| Stofna skilaboð                               | X                     |                |                 |              |        |
| Útflutningur rafrænnar skýrslugerðar                  | X                     |                |                 |              |        |
| Innflutningur rafrænnar skýrslugerðar                  |                       |                |                 |              |        |
| Vefþjónusta                                  | X                     |                | X               |              |        |
| Í vinnslu hjá notanda                              |                       |                |                 |              |        |
| Framkvæmdastig skilaboða                      |                       |                |                 |              |        |
| Fylla út færslur                             |                       |                |                 |              |        |
| Framkvæmdastig skilaboðaatriðis                 |                       |                |                 |              |        |
| Biðja um staðfestingu                         | X                     | X              | X               |              |        |
| Útflutningsskilaboð rafrænnar skýrslugerðar          | X                     |                |                 |              |        |
| Úrvinnsla skilaboðastigs                |                       |                |                 |              |        |

### <a name="electronic-message-processing"></a>Rafræn skilaboð í vinnslu

Úrvinnsla á rafrænum skilaboðum er grundvallaratriði í virkni rafrænna skilaboða. Vinnslan safnar saman aðgerðum sem á að meta fyrir rafrænu skilaboðin. Hægt er að tengja aðgerðirnar í gegnum upphafsstöðu og lokastöðu. Annars er hægt að hefja hverja aðgerð fyrir sig af gerðinni **Úrvinnsla notanda**. Á síðunni **Úrvinnsla rafrænna skilaboða** (**Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Úrvinnsla rafrænna skilaboða**) er einnig hægt að velja önnur svæði sem eiga að vera studd fyrir úrvinnsluna annaðhvort á stigi skilaboða eða stigi skilaboðaatriðis.

Flýtiflipinn **Aðgerðir** gerir þér kleift að bæta forskilgreindum aðgerðum við úrvinnsluna. Hægt er að tilgreina hvort keyra verði aðgerð sérstaklega eða hvort vinnslan geti byrjað hana. Til að tilgreina að aðgerð í úrvinnslunni geti eingöngu verið frumstillt af notanda skal stilla reitinn **Keyra sérstaklega** á **Já** fyrir þessa aðgerð. Ef hefja á aðgerð með úrvinnslu á skilaboðum eða skilaboðaatriðum sem eru í stöðunni sem er skilgreind sem upphafsstaða fyrir aðgerðina skal stilla reitinn **Keyra sérstaklega** á **Nei**. Aðgerð af gerðinni **Aðgerð notanda** verður alltaf að keyra sérstaklega.

Stundum þarf að sameina nokkrar aðgerðir í röð, jafnvel þó að fyrsta aðgerðin sé sett upp þannig að hún keyri sérstaklega. Til dæmis verður notandi að frumstilla skýrslumyndun, en strax og skýrslan er búin til verður að senda hana á vefþjónustu og svarið frá vefþjónustunni verður að speglast í kerfinu. Við þessar kringumstæður er hægt að búa til óaðskiljanlega röð fyrir aðgerðirnar sem verður alltaf að keyra saman. Í flýtiflipanum **Aðgerð** skal velja **Óaðskiljanlegar raðir** fyrir ofan hnitanetið og stofna röð. Svo skal velja röðina fyrir allar aðgerðirnar sem keyra á saman í rietnum **Óaðskiljanleg röð**. Í þessu tilviki er hægt að stilla reitinn **Keyra sérstaklega** á **Já** fyrir fyrstu aðgerðina í röðinni en **Nei** fyrir allar aðrar aðgerðir.

Flýtiflipinn **Önnur svæði skilaboðaatriða** gerir þér kleift að bæta við öðrum forskilgreindum svæðum sem tengjast skilaboðaatriðum. Bæta verður við öðrum svæðum fyrir hverja gerð skilaboðaatriða sem svæðin tengjast.

Flýtiflipinn **Önnur svæði skilaboða** gerir þér kleift að bæta við öðrum forskilgreindum svæðum sem tengjast skilaboðum.

Flýtiflipinn **Öryggishlutverk** gerir þér kleift að setja upp öryggishlutverk sem eru forskilgreind í kerfinu fyrir tilteknar vinnslur. Notendur með tiltekið hlutverk sjá aðeins vinnslu sem er skilgreind fyrir það hlutverk.

Flýtiflipinn **Runa** gerir þér kleift að setja upp vinnslu til að vinna í runufyrirkomulagi.

## <a name="work-with-the-electronic-messages-functionality"></a>Vinna með virkni rafrænna skilaboða

Ef unnið er á skilaboðastigi, þá er gagnlegra að nota síðuna **Rafræn skilaboð** (**Skattur** \> **Fyrirspurnir og skýrslur** \> **Rafræn skilaboð** \> **Rafræn skilaboð**). Ef starfað er á stigi gagnasöfnunar (skilaboðaatriðis), þá er gagnlegra að nota síðuna **Rafræn skilaboðaatriði** (**Skattur** \> **Fyrirspurnir og skýrslur** \> **Rafræn skilaboð** \> **Rafræn skilaboðaatriði**).

### <a name="electronic-messages"></a>Rafræn skilaboð

Síðan **Rafræn skilaboð** birtir tiltæka vinnslu samkvæmt hlutverki þínu. Öryggishlutverk tengjast vinnslu við uppsetningu þeirrar vinnslu. Síðan sýnir rafræn skilaboð og upplýsingar sem tengjast hverri vinnslu sem er þér tiltæk.

Flýtiflipinn **Skilaboð** birtir rafræn skilaboð fyrir valda vinnslu. Það fer eftir stöðu valdra skilaboða og forskilgreindra vinnsla hvaða aðgerðir hægt er að keyra með því að nota hnappana fyrir ofan hnitanetið:

- **Ný** – Þessi hnappur tengist aðgerðum af gerðinni **Stofna skilaboð**.
- **Eyða** – Þessi hnappur er í boði ef gátreiturinn **Leyfa eyðingu** er valinn fyrir núgildandi stöðu á völdum skilaboðum.
- **Safna gögnum** - Þessi hnappur tengist aðgerðum af gerðinni **Fylla út færslur**.
- **Búa til skýrslu** – Þessi hnappur tengist aðgerðum af gerðinni **Útflutningsskilaboð rafrænna skýrslna**.
- **Senda skýrslu** – Þessi hnappur tengist aðgerðum af gerðinni **Vefþjónusta**.
- **Innflutningssvar** - Þessi hnappur tengist aðgerðum af gerðinni **Innflutningur rafrænna skýrslna**.
- **Uppfærslustaða** – Þessi hnappur er tengdur við aðgerðir af gerðinni **Úrvinnsla notanda á skilaboðastigi**.
- **Skilaboðaatriði** – Opnið síðuna **Rafræn skilaboðaatriði**.

Flýtiflipinn **Aðgerðakladdi** sýnir upplýsingar um allar aðgerðir sem hafa verið keyrðar fyrir valin skilaboð. Ef aðgerð olli villu eru upplýsingar um villuna tengdar við viðkomandi línu í hnitanetinu. Til að yfirfara upplýsingar um villuna skal velja línuna í hnitanetinu og síðan velja hnappinn **Viðhengi** (bréfaklemmutáknið) efst í hægra horninu á síðunni.

Flýtiflipinn **Önnur svæði skilaboða** sýnir öll önnur svæði sem eru skilgreind fyrir skilaboð í uppsetningu á vinnslu. Hann sýnir einnig gildi þessara svæða.

Flýtiflipinn **Skilaboðaatriði** sýnir öll skilaboðaatriði sem tengjast völdu skilaboði. Það fer eftir stöðu á völdu skilaboðaatriði hvaða aðgerðir hægt er að keyra með því að velja hnappana fyrir ofan hnitanetið:

- **Eyða** – Þessi hnappur er í boði ef gátreiturinn **Leyfa eyðingu** er valinn fyrir núgildandi stöðu á völdum skilaboðum.
- **Uppfærslustaða** – Þessi hnappur tengist aðgerðum af gerðinni **Úrvinnsla notanda**.
- **Upprunalegt skjal** - Opna síðu sem sýnir upprunalegt skjal fyrir valið skilaboðaatriði.

Allar skýrslur sem þegar hafa verið búnar til og mótteknar fyrir skilaboð eru hengdar við þessi skilaboð. Til að endurskoða viðhengin sem tengjast skilaboðum skal velja skilaboðin og síðan velja hnappinn **Viðhengi** (bréfaklemmutáknið) efst í hægra horni síðunnar.

![Hnappur viðhengis](media/attachment-icon.png)

Síðan **Viðhengi** sýnir öll viðhengi sem tengjast völdum skilaboðum. Til að skoða skrá skal velja hana af listanum til vinstri og velja síðan **Opna** á aðgerðasvæðinu.

![Hnappurinn opna](media/open-button.png)

Einnig er hægt að yfirfara viðhengi sem tengjast tiltekinni aðgerð sem var keyrð áður fyrir skilaboð. Á síðunni **Rafræn skilaboð** skal velja skilaboðin í flýtiflipanum **Skilaboð**, velja aðgerðina í flýtiflipanum **Aðgerðarkladdi** og síðan velja hnappinn **Viðhengi** efst í hægra horni síðunnar.

Einnig er hægt að keyra alla vinnsluna eða bara tiltekna aðgerð með því að velja **Keyra vinnslu** á aðgerðasvæðinu.

### <a name="electronic-message-items"></a>Rafræn skilaboðaatriði

Síðan **Rafræn skilaboðaatriði** birtir öll skilaboðaatriði og kladda yfir aðgerðir sem hafa verið keyrðar fyrir hvert skilaboðaatriði. Hún sýnir einnig önnur svæði sem eru skilgreind fyrir skilaboðaatriðin og gildi þessara svæða.

Eftirfarandi töflur lýsa svæðunum á síðunni **Skilaboðaatriði**.

<table>
<thead>
<tr>
<th>Svæði</th>
<th>lýsing</th>
</tr>
</thead>
<tbody>
<tr>
<td>Í vinnslu</td>
<td>Heiti vinnslunnar sem notuð var til að stofna skilaboðaatriðið.</td>
</tr>
<tr>
<td>Skilaboðaatriði</td>
<td>Auðkenni skilaboðaatriðis. Auðkenninu er úthlutað sjálfkrafa á grundvelli númeraraðar <strong>Skilaboðaatriðis</strong> sem er skilgreind á síðunni <strong>Færibreytur fjárhags</strong>.</td>
</tr>
<tr>
<td>Dagsetning skilaboðaatriðis</td>
<td>Dagsetning þegar skilaboðaatriði var stofnað.</td>
</tr>
<tr>
<td>Gerð skilaboðaatriðis</td>
<td>Gerð skilaboðaatriðis. Hægt er að setja upp nokkrar gerðir skilaboðaatriða fyrir sömu vinnsluna (til dæmis <strong>Reikningar á innleið</strong> og <strong>Reikningar á útleið</strong>). Aðeins er hægt að fylla þetta svæði út þegar reikningi er bætt við töflu skilaboðaatriða.</td>
</tr>
<tr>
<td>Staða skilaboðaatriðis</td>
<td>Raunveruleg staða skilaboðaatriðis. Tiltækar stöður eru breytilegar, fer eftir gerð skilaboðaatriðis. Hér eru nokkur dæmi:
<ul>
<li><strong>Fylla út</strong> – Færslu var bætt við töflu skilaboðaatriða.</li>
<li><strong>Metið</strong> – Viðbótareigindir voru reiknaðar fyrir skilaboðaatriði.</li>
<li><strong>Tilkynnt</strong> – Það tókst að bæta skilaboðaatriði við skýrslu.</li>
<li><strong>Útilokað</strong> – Þessi staða getur reynst gagnleg ef þarf að útiloka sum skilaboðaatriði frá skýrslu áður en hún er flutt út.</li>
</ul>
</td>
</tr>
<tr>
<td>Sendingardagsetning</td>
<td>Dagsetning þegar skilaboðaatriði var sent, fyrir vinnslu sem sendir myndaða skýrslu sjálfkrafa út fyrir kerfið.</td>
</tr>
<tr>
<td>Skjalnúmer</td>
<td>Þetta svæði er fyllt út sjálfkrafa á grundvelli uppsetningar á aðgerð sem fyllir út færslur. Aðeins er hægt að fylla þetta svæði út þegar reikningi er bætt við töflu skilaboðaatriða.</td>
</tr>
<tr>
<td>Reikningsnúmer</td>
<td>Reikningsnúmer viðskiptamanns eða lánardrottins (eða annað gildi svæðis, sem fer eftir svæðinu sem er skilgreint í aðgerðinni Fylla út færslur). Aðeins er hægt að fylla þetta svæði út þegar reikningi er bætt við töflu skilaboðaatriða.</td>
</tr>
<tr>
<td>Skilaboð</td>
<td>Númer skilaboðanna. Þessu númeri er úthlutað sjálfkrafa, á grundvelli númeraraðar fyrir <strong>Skilaboð</strong> sem er skilgreind á síðunni <strong>Færibreytur fjárhags</strong>.</td>
</tr>
<tr>
<td>Staða skilaboða</td>
<td>Raunveruleg staða rafrænna skilaboða.</td>
</tr>
<tr>
<td>Næsta aðgerð</td>
<td>Næstu aðgerðir sem hægt er að hefja fyrir núverandi stöðu skilaboðaatriðis.</td>
</tr>
</tbody>
</table>

Flipinn **Önnur svæði** sýnir önnur svæði fyrir valið skilaboðaatriði og gildin þeirra.

#### <a name="run-processing"></a>Keyra vinnslu

Veljið **Keyra vinnslu** á aðgerðasvæðinu til að keyra vinnslu fyrir skilaboðaatriði. Til að keyra tiltekna aðgerð skal, í svarglugganum **Keyra vinnslu**, stilla valkostinn **Velja aðgerð** á **Já** og síðan velja aðgerð. Til að keyra alla vinnsluna skal hafa valkostinn **Velja aðgerð** stilltan á **Nei**.

#### <a name="generate-report"></a>Búa til skýrslu

Veljið **Búa til skýrslu** á aðgerðasvæðinu til að búa til skýrslu. Þessi hnappur tengist aðgerðum af gerðinni **Útflutningur á rafrænum skýrslum**.

#### <a name="update-status"></a>Uppfæra stöðu

Veljið **Uppfæra stöðu** á aðgerðasvæðinu til að uppfæra stöðu á einu eða fleiri skilaboðaatriðum. Í svarglugganum **Uppfæra stöðu** skal nota flýtiflipann **Færslur til að taka með** til að velja skilaboðaatriði fyrir uppfærslu. Gangið úr skugga um að valskilyrði séu rétt skilgreind vegna þess að stöður skilaboðaatriða verða uppfærðar samkvæmt þessum skilyrðum, upphafsstöðu valdrar aðgerðar og gildinu sem var tilgreint fyrir **Ný staða**. Eftir að stöðuuppfærslu er lokið verður erfitt að finna út hvaða atriði voru uppfærð. Því verður erfitt að endurheimta stöðuuppfærsluna.

#### <a name="electronic-messages"></a>Rafræn skilaboð

Veljið **Rafræn skilaboð** á aðgerðasvæðinu til að yfirfara rafræn skilaboð sem tengjast völdu skilaboðaatriði.

Einnig er hægt að yfirfara allar skrár sem tengjast tilteknu skilaboðaatriði. Veljið svæðið **Skilaboð** fyrir skilaboðaatriði eða veljið **Rafræn skilaboð** á aðgerðasvæðinu. Á síðunni **Rafræn skilaboð** skal síðan velja skilaboðin til að yfirfara skrár fyrir, og síðan velja hnappinn **Viðhengi** (bréfaklemmutáknið) efst í hægra horni síðunnar.

![Hnappur viðhengis](media/attachment-icon.png)

Síðan **Viðhengi** sýnir öll viðhengi sem tengjast skilaboðunum. Til að skoða skrá skal velja hana af listanum til vinstri og velja síðan **Opna** á aðgerðasvæðinu.

![Hnappurinn opna](media/open-button.png)

#### <a name="original-document"></a>Upprunalegt skjal

Veljið **Upprunalegt skjal** á aðgerðasvæðinu til að opna upprunalegt skjal fyrir valið skilaboðaatriði.

## <a name="example-set-up-and-run-processing-to-call-a-simple-er-exporting-format-to-generate-an-excel-report"></a>Dæmi: Setjið upp og keyrið vinnslu til að kalla á einfalt útflutningssnið rafrænnar skýrslugerðar til að búa til Excel-skýrslu

Eftir að snið rafrænnar skýrslugerðar hefur verið stofnað, því varpað í gagnaveitur og því lokið, er hægt að keyra það með því að nota vinnusvæðið **Rafræn skýrslugerð**. Skýrsla er búin til og þú getur vistað hana á staðnum.

Til að stjórna eftirfarandi þáttum skýrslugerðarferlisins þarf að setja upp úrvinnslu á rafrænum skilaboðum:

- Skrá upplýsingar um þann sem bjó til skýrsluna.
- Skrá upplýsingar um hvenær skýrslan var gerð.
- Vista skýrslur sem voru búnar til fyrir fyrri tímabil.

Þessi hluti kemur með dæmi um hvernig hægt er að setja upp rafræn skilaboð til að búa til skýrslu sem byggist á útflutningssniði rafrænnar skýrslugerðar fyrir Excel. Ef þú vilt fylgja þessu dæmi verður útflutningssnið rafrænnar skýrslugerðar að hafa verið búið til, því varpað í gagnaveitur og því lokið. Auk þess verður númeraröð að vera uppsett fyrir rafræn skilaboð.

Þegar vinnsla er búin til er gagnlegt að skilgreina fyrst aðgerðir og stöður vinnslunnar sem verða settar upp. Eftirfarandi skýringarmynd sýnir hvernig vinnslan lítur út í þessu dæmi.

![Vinnsluskema](media/processing-scheme.png)

#### <a name="create-message-statuses"></a>Stofna skilaboðastöður

1. Opnið **Skattur \> Uppsetning \> Rafræn skilaboð \> Stöður skilaboða**.
2. Stofna eftirfarandi stöður skilaboða:

    - Nýjar
    - Undirbúið
    - Myndað

    ![Stöður skilaboða](media/message-statuses.png)

3. Í línunni fyrir stöðuna **Ný** skal velja gátreitinn **Leyfa eyðingu** til að gera notendum kleift að eyða skilaboðum sem eru með þessa stöðu.

#### <a name="create-additional-fields"></a>Stofna önnur svæði

1. Opnið **Skattur \> Uppsetning \> Rafræn skilaboð \> Önnur svæði**.
2. Bætið við öðrum svæðum og gildum þeirra. Eftirfarandi er dæmi.

    ![Önnur svæði](media/additional-fields.png)

3. Stillið valkostinn **Breyting notanda** á **Já** til að leyfa notendum að breyta svæðinu.

#### <a name="create-message-processing-actions"></a>Stofnið úrvinnsluaðgerðir skilaboða

Í þessu dæmi verða eftirfarandi aðgerðir stofnaðar:

- **Stofna skilaboð**
- **Uppfæra í undirbúið**
- **Búa til skýrslu**
- **Uppfæra í upphafsstöðu** (valfrjálst)

1. Opnið **Skattur \> Uppsetning \> Rafræn skilaboð \> Úrvinnsluaðgerðir skilaboða**.
2. Stofnið aðgerð með heitinu **Stofna skilaboð**. Á flýtiflipanum **Almennt**, í reitnum **Gerð aðgerðar** skal velja **Stofna skilaboð**.
3. Stofnið aðgerð með heitinu **Uppfæra í undirbúið** og stillið eftirfarandi svæði:

    - Á flýtiflipanum **Almennt**, á svæðinu **Gerð aðgerðar**, skal velja **Úrvinnsla notanda á skilaboðastigi**.
    - Á flýtiflipanum **Upphafsstöður**, á svæðinu **Staða skilaboða**, skal velja **Ný**.
    - Á flýtiflipanum **Lokastöður**, á svæðinu **Staða skilaboða**, skal velja **Undirbúin**. Á svæðinu **Gerð svars** skal fara í **Keyrsla heppnaðist**.

4. Stofnið aðgerð með heitinu **Búa til skýrslu** og stillið eftirfarandi svæði:

    - Á flýtiflipanum **Almennt**, á svæðinu **Gerð aðgerðar**, skal velja **Útflutningur á rafrænum skýrslum**. Á svæðinu **Vörpun sniðmáts** skal velja útflutningssnið rafrænnar skýrslugerðar. Valkostirnir eru **Excel**, **XML**, **JSON**, **Texti** og **Annað**.
    - Á flýtiflipanum **Upphafsstöður**, á svæðinu **Staða skilaboða**, skal velja **Undirbúin**.
    - Á flýtiflipanum **Lokastöður**, á svæðinu **Staða skilaboða**, skal velja **Mynduð**. Á svæðinu **Gerð svars** skal fara í **Keyrsla heppnaðist**.

    ![Aðgerð skýrslugerðar](media/generate-report-action.png)

5. Valfrjálst: Til að leyfa notendum að endurgera skýrslu nokkrum sinnum er hægt að stofna aðgerðina **Uppfæra í upphafsstöðu** og stilla eftirfarandi svæði:

    - Á flýtiflipanum **Almennt**, á svæðinu **Gerð aðgerðar**, skal velja **Úrvinnsla notanda á skilaboðastigi**.
    - Á flýtiflipanum **Upphafsstöður**, á svæðinu **Staða skilaboða**, skal velja **Myndaðar**.
    - Í flýtiflipanum **Lokastöður** skal bæta við aðskilinni línu fyrir hvora skilaboðastöðuna fyrir sig (**Undirbúið** og **Nýtt**). Fyrir báðar línur skal stilla svæðið **Gerð svars** á **Tókst að framkvæma**.

#### <a name="electronic-message-processing"></a>Rafræn skilaboð í vinnslu

Í þessu dæmi á að setja upp allar aðgerðirnar svo þær keyri hver fyrir sig. Gert er ráð fyrir að notandinn muni frumstilla allar aðgerðir.

1. Opnið **Skattur \> Uppsetning \> Rafræn skilaboð \> Úrvinnsla rafrænna skilaboða**.
2. Bætið við færslu fyrir vinnsluna og bætið við öllum áður skilgreindum aðgerðum og öðrum svæðum.
3. Valfrjálst: Á flýtiflipanum **Öryggishlutverk** skal skilgreina öryggishlutverk fyrir vinnslurnar til að takmarka aðgang að tilteknum skýrslum.
4. Opnið **Skattur \> Fyrirspurnir og skýrslur \> Rafræn skilaboð \> Rafræn skilaboð**.
5. Veljið **Ný** til að stofna ný skilaboð. Á þessum tímapunkti er hægt að bæta við dagsetningum og lýsingu. Einnig er hægt að uppfæra gildið á viðbótarsvæði eins og þörf krefur.

    ![Stofna rafræn skilaboð](media/create-electronic-message.png)

Fyllt er sjálfkrafa inn í hnitanetið á flýtiflipanum **Aðgerðakladdi** með kladda yfir allar aðgerðir sem eru framkvæmdar á skilaboðinu.

Nú er annaðhvort hægt að eyða eða uppfæra stöðu skilaboða. Til að uppfæra stöðu skilaboða skal velja **Uppfæra stöðu**. Í reitnum **Ný staða** skal velja **Undirbúið** og síðan velja **Í lagi**.

![Uppfæra stöðu skilaboða](media/update-status.png)

Staða skilaboða er uppfærð í **Undirbúin** og hægt er að búa til skýrsluna með því að velja **Búa til skýrslu**. Skýrslan er búin til og uppfærsla gerð á stöðu skilaboða og aðgerðakladda. Til að skoða myndaða skýrslu skal velja hnappinn **Viðhengi** (bréfaklemmutáknið) efst í hægra horni síðunnar.
