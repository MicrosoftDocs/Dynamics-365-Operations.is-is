---
title: Rafræn skilaboð
description: Þetta efnisatriði veitir yfirlit og upplýsingar um uppsetningu fyrir rafræn skilaboð í Microsoft Dynamics 365 for Finance and Operations.
author: ShylaThompson
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 5326642553c7efcebc6c6af953e2dafe9e62e9ec
ms.sourcegitcommit: f6fc90585632918d9357a384b27028f2aebe9b5a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/11/2019
ms.locfileid: "832196"
---
# <a name="electronic-messaging"></a>Rafræn skilaboð

[!include [banner](../includes/banner.md)]

Þetta efnisatriði veitir yfirlit og upplýsingar um uppsetningu fyrir rafræn skilaboð í Microsoft Dynamics 365 for Finance and Operations.

Ríkisstjórnir og löggjafarvald í hinum ýmsu löndum og svæðum um allan heim hafa nýlega innleitt skýrslukröfur fyrir fyrirtæki sem eru skráð í þessum löndum og svæðum. Tilgangur kröfunnar er að gera það mögulegt að fá gögn frá þessum fyrirtækjum á rafrænu formi, beint frá kerfinu þar sem þau voru skráð, vistuð og unnin.

Virknin fyrir rafræn skilaboð í Finance and Operations styður ýmsa ferla rafrænnar samaðgerðar milli Finance and Operations og kerfanna sem ríkisstjórnir og löggjafarvald bjóða upp á hvað varðar skýrslugerð, afhendingu og móttöku á opinberum upplýsingum.

Virknin fyrir rafræn skilaboð er samþætt við eininguna **Rafræn skýrslugerð**. Því er hægt að setja upp snið rafrænnar skýrslugerðar fyrir rafræn skilaboð. Frekari upplýsingar eru í [Rafræn skýrslugerð](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting).

Rafræn skilaboð byggjast á eftirfarandi einingum:

- **Rafræn skilaboð** – Skýrsla eða yfirlýsing sem ber að tilkynna og/eða senda innbyrðis. Eitt dæmi er skýrsla sem er send til skattstofu.
- **Atriði rafrænna skilaboða** – Færslur sem ber að hafa með í skilaboðunum sem eru skráð.
- **Úrvinnsla rafrænna skilaboða** – Röð aðgerða, annaðhvort tengdar eða ótengdar, sem ber að keyra til að safna saman nauðsynlegum gögnum, búa til skýrslur, vista gögn í blob-geymslu Microsoft Azure, flytja skýrslur út fyrir kerfið, fá viðbrögð utan kerfis og uppfæra gagnagrunninn, á grundvelli móttekinna upplýsinga.

Eftirfarandi skýringarmynd sýnir flæði gagna fyrir rafræn skilaboð.

![Gagnaflæði rafrænna skilaboða](media/electronic-messaging-data-flow.png)

Virkni rafrænna skilaboða styður eftirfarandi aðstæður:

- Stofna skilaboð og gera skýrslur handvirkt sem byggjast á útflutningstengdum sniðum rafrænnar skýrslugerðar af ýmsum gerðum: Microsoft Excel, XML, JavaScript Object Notation (JSON), PDF, texta og Microsoft Word.
- Stofna og vinna úr skilaboðum sjálfvirkt sem tengjast upplýsingum sem óskað var eftir og voru fengin frá yfirvöldum í gegnum útflutningstengt snið rafrænnar skýrslugerðar.
- Safna og vinna úr upplýsingum úr gagnaveitu (tafla Finance and Operations) sem skilaboðaatriði.
- Geyma viðbótarupplýsingar og meta ýmis gildi með því að kalla á sérstaklega skilgreinda keyranlega klasa í tengslum við skilaboð eða skilaboðaatriði.
- Safna saman upplýsingum sem eru fengin í skilaboðaatriðum, skipta þeim upplýsingum eftir skilaboðum, og búa til skýrslur sem eru á útflutningstengdum sniðum rafrænnar skýrslugerðar.
- Senda skýrslur sem eru búnar til á vefþjónustu með því að nota öryggisupplýsingar sem eru geymdar í Azure-lyklageymslu.
- Fá svar frá vefþjónustu, túlka svarið og uppfæra gögn í Finance and Operations eftir því sem við á.
- Geyma og yfirfara allar skýrslur sem eru búnar til.
- Geyma og yfirfara allar kladdaupplýsingar sem tengjast aðgerðum sem eru keyrðar fyrir skilaboð eða skilaboðaatriði.
- Stjórna vinnslu í gegnum ýmsar stöður skilaboða og skilaboðaatriða.

## <a name="set-up-electronic-messaging"></a>Setja upp rafræn skilaboð

Rafræn skilaboð auðveldað það að viðhalda mismunandi ferlum rafrænnar skýrslugerðar fyrir mismunandi skjalategundir. Í sumum flóknum aðstæðum eru rafræn skilaboð sett upp til að vera með samsetningu af mörgum skilaboðastöðum, stöðum skilaboðaatriða, aðgerðum, öðrum svæðum og keyranlegum klösum. Í þessum tilfellum er innflutningur á gagnaeiningapökkum í boði. Ef þessir gagnaeiningapakkar eru notaðir ætti að flytja þá inn í lögaðila með verkfæri gagnastjórnunar. Frekar upplýsingar um hvernig á að nota verkfæri gagnastjórnunar eru í [Gagnastjórnun](../../dev-itpro/data-entities/data-entities-data-packages.md).

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

Setja upp númeraraðir fyrir bæði skilaboð og skilaboðaatriði. Númeraraðir eru notaðar til að sjálfkrafa gefa skilaboðum og skilaboðaatriðum númer, og úthlutuð númer verða notuð sem einkvæm auðkenni fyrir skilaboðin og skilaboðaatriðin í kerfinu. Hægt er að setja upp númeraraðir fyrir rafræn skilaboð á síðunni **Færibreytur fjárhags** (**Fjárhagur** \> **Uppsetning fjárhags** \> **Færibreytur fjárhags**).

### <a name="message-item-types-and-statuses"></a>Gerðir og stöður skilaboðaatriða

Gerðir skilaboðaatriða bera kennsl á færslutegundir sem verða notaðar í rafrænum skilaboðum. Hægt er að setja upp gerðir skilaboðaatriða á síðunni **Gerðir skilaboðaatriða** (**Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Gerðir skilaboðaatriða**).

Stöður skilaboðaatriða bera kennsl á stöðurnar sem verða notaðar í skilaboðaatriðum í vinnslunni sem verið er að setja upp. Hægt er að setja upp gerðir skilaboðaatriða á síðunni **Stöður skilaboðaatriða** (**Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Stöður skilaboðaatriða**).

Færibreytan **Leyfa eyðingu** fyrir stöðu á skilaboðaatriði skilgreinir hvort notanda verði leyft að eyða skilaboðaatriði í þessar stöðu í gegnum skjámyndina **Rafræn skilaboð** eða skjámyndina **Rafræn skilaboðaatriði**. 

### <a name="message-statuses"></a>Stöður skilaboða

Setja upp stöður skilaboða sem eiga að vera tiltæk í vinnslu skilaboða. Hægt er að setja upp stöður skilaboða á síðunni **Stöður skilaboða** (**Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Stöður skilaboða**).

Lýsing svæðis:

| Svæðisheiti           | Lýsing |
|----------------------|-------------|
|Staða boða        | Einkvæmt heiti á stöðu rafrænna skilaboða sem einkennir stöðu skilaboða á hverju augnabliki. Þetta heiti er sýnt í skjámynd rafrænna skilaboða og í kladda sem tengist rafrænum skilaboðum. |
|Lýsing           | Lýsing sem tengist stöðunni á rafrænum skilaboðum      |
|Gerð svars         | Sumar aðgerðir í vinnslu geta gefið af sér fleiri en eina gerð svars. Sem dæmi, aðgerð af gerðinni **Vefþjónusta** getur leitt til gerð svars sem er annaðhvort **Tókst að framkvæma** eða **Tæknileg villa**, fer eftir niðurstöðu keyrslunnar. Í þessu tilviki verður að skilgreina skilaboðastöðu fyrir báðar svargerðirnar. Leitaðu í [Gerðir úrvinnsluaðgerðar skilaboða](#message-processing-action-types) til að fá frekari upplýsingar um gerðir aðgerða og svargerðir sem tengjast þeim. |
|Staða skilaboðaatriðis   |Það eru tilfelli þegar rafræn skilaboðastaða verður að hafa áhrif á stöður tengdra skilaboðaatriða. Tengja stöðu slíks skilaboðaatriðis í þessu svæði með því að velja það úr uppflettingu. |
|Leyfa eyðingu          | Færibreytan **Leyfa eyðingu** fyrir stöðu á rafrænu skilaboðaatriði skilgreinir hvort notanda verði leyft að eyða rafrænu skilaboðaatriði í þessar stöðu í gegnum skjámyndina **Rafræn skilaboð**.            |

### <a name="additional-fields"></a>Önnur svæði

Virknin fyrir rafræn skilaboð gerir þér kleift að fylla út færslur úr færslutöflu. Þannig er hægt að undirbúa færslurnar fyrir skýrslugerð og síðan tilkynna þær. Stundum eru ekki nægar upplýsingar í færslutöflunni til að gefa skýrslu um færslu samkvæmt skýrslukröfum. Þú getur fyllt út allar upplýsingar sem þarf að tilkynna um færslu með því að setja upp önnur svæði. Önnur svæði geta tengst bæði skilaboðum og skilaboðaatriðum. Hægt er að setja upp önnur svæði á síðunni **Önnur svæði** (**Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Önnur svæði**).

Eftirfarandi tafla lýsir almennu svæðunum á síðunni **Önnur svæði**:

| Svæði                | Lýsing |
|----------------------|-------------|
| Svæðisheiti           | Sláið inn heiti á viðbótareigind skilaboðaatriða sem tengjast vinnslunni. Þetta heiti birtist í notandaviðmótinu á meðan unnið er í vinnslunni. Einnig er hægt að nota það í stillingum rafrænnar skýrslugerðar sem tengjast vinnslunni. |
| lýsing          | Færið inn lýsingu á viðbótareigind skilaboðaatriða sem tengjast vinnslunni. |
| Breyting notanda            | Í tilfelli þegar notandi verður að geta breytt gildi á viðbótarsvæði í notandaviðmótinu, skal setja upp þennan gátreit **Já**, annars **Nei**. |
| Teljari              | Þegar viðbótarsvæðið verður að innihalda númeraröð innan rafrænna skilaboða skal haka við þennan gátreit. Gildi viðbótarsvæðisins verður fyllt út sjálfkrafa við keyrslu á aðgerð af gerðinni „Útflutningur rafrænna skýrslna“.  |
| Falið               | Þegar viðbótarsvæðið verður að vera falið frá notandaviðmótinu skaltu merkja þennan gátreit.  |

Sérhvert viðbótarsvæði getur haft mismunandi gildi fyrir vinnsluna. Þú getur skilgreint þessi gildi á flýtiflipanum fyrir gildi:

| Svæði                | Lýsing |
|----------------------|-------------|
| Svæðisgildi          | Sláið inn svæðisgildi sem er notað í tengslum við skilaboð eða skilaboðaatriði við skýrslugerð. |
| Lýsing svæðis    | Færið inn lýsingu á svæðisgildi sem er notað í tengslum við skilaboð eða skilaboðaatriði við skýrslugerð. |
| Reikningsgerð         | Sum gildi annarra svæða kunna að takmarkast við tilteknar lyklagerðir. Veljið eitt af eftirfarandi gildum: **Allar**, **Viðskiptamaður** eða **Lánardrottinn**. |
| Kóði lykils         | Ef þú valdir **Viðskiptamaður** eða **Lánardrottinn** í reitnum **Lykilgerð** er hægt að takmarka frekar notkun svæðisgilda við tilgreindan flokk eða töflu. |
| Númer lykils/flokks | Ef þú valdir **Viðskiptamaður** eða **Lánardrottinn** í reitnum **Lykilgerð** og ef þú færðir inn flokk eða töflu í reitinn **Kóði lykils** er hægt að færa inn tilgreindan flokk eða umboðsaðila í þennan reit. |
| Virkt            | Tilgreina dagsetningu þegar byrja á að taka tillit til gildisins. |
| Lok gildistíma           | Tilgreina dagsetningu þegar hætta á að taka tillit til gildisins. |

Samsetningar skilyrða sem eru skilgreind í **Númer lykils/flokks**, **Kóði lykils**, **Virkt**, **Gildistími** hafa ekki áhrif að sjálfgefnu á val á gildi fyrir viðbótarsvæði en hægt er að nota þær í keyrsluhæfum klasa til að innleiða einhverja tiltekna reiknireglu fyrir gildi viðbótarsvæðis.

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

Sumir keyranlegir klasar kunna að hafa áskildar færibreytur sem verður að skilgreina áður en keyrsluhæfur klasi er keyrður í fyrsta skipti. Til að skilgreina slíka færibreytur skaltu smella á hnappinn **Færibreytur** í aðgerðarúðunni, setja upp viðeigandi gildi og svæði í svarglugga og smella á hnappinn **Í lagi**. Hér er mikilvægt að smella á hnappinn **Í lagi** annars vistast færibreyturnar ekki í grunninn og ekki verður kallað á keyranlega klasann með viðeigandi hætti.

### <a name="populate-records-actions"></a>Fylla út færsluaðgerðir

„Fylla út færsluaðgerðir“ er notuð til að setja upp aðgerðir sem bæta færslum við töflu skilaboðaatriða svo hægt sé að bæta þeim við rafræn skilaboð. Ef rafrænu skilaboðin verða til dæmis að gefa skýrslu um reikninga viðskiptamanns er nauðsynlegt að setja upp aðgerðina **Fylla út færslur** sem er tengd við töfluna **Reikningabók viðskiptamanns** (í reitnum **Gagnaveita**). Hægt er að setja upp „fylla út færsluaðgerðir“ á síðunni **Fylla út færsluaðgerðir** (**Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Fylla út færsluaðgerðir**). Stofnið nýja færslu fyrir hverja aðgerð sem á að bæta færslum við töflu, og stillið eftirfarandi svæði.

| Svæði       | lýsing                                                               |
|-------------|---------------------------------------------------------------------------|
| Nafn        | Færið inn heiti á aðgerð sem fyllir út færslur í vinnslunni.       |
| lýsing | Færið inn lýsingu á aðgerð sem fyllir út færslur í vinnslunni. |

Á flýtiflipanum **Uppsetning gagnagjafa** skal bæta við línu fyrir hvern gagnagjafa sem er notaður í vinnslunni, og stilla skal eftirfarandi svæði.

| Svæði                  | lýsing |
|------------------------|-------------|
| Nafn                   | Færið inn heiti á gagnaveitu. |
| Gerð skilaboðaatriðis      | Veljið gerð skilaboðaatriðis sem á að nota þegar færslur eru búnar til fyrir gagnaveitu. |
| Lykilgerð           | Veljið lykilgerð sem á að tengjast færslum úr gagnaveitu. |
| Aðaltöfluheiti      | Veljið töfluna í Finance and Operations sem á að vera gagnaveita. |
| Reitur skjalnúmers  | Veljið reitinn í valdri töflu þar sem taka á skjalanúmerið úr. |
| Dagsetningarreitur skjals    | Veljið reitinn í valdri töflu þar sem taka á dagsetningu skjals úr. |
| Reikningsreitur skjals | Veljið reitinn í valdri töflu þar sem taka á lykil skjals úr. |
| Fyrirspurn notanda             | Ef þessi gátreitur er valinn er hægt að setja upp fyrirspurn með því að velja **Breyta fyrirspurn** fyrir ofan hnitanetið. Annars verða allar færslur gagnaveitunnar fylltar út. |

### <a name="web-applications"></a>Vefforrit

Þú notar síðu vefforrita til að setja upp færibreytur fyrir vefforrit til að styðja opinn staðal OAuth 2.0 sem leyfir notendum að veita „öruggan úthlutaðan aðgang“ að forritinu fyrir þeirra hönd, án þess að deila aðgangsupplýsingum. Frá þessari síðu getur þú einnig farið í gegnum heimildarferlið með því að fá heimildarkóða og aðgangslykil. Hægt er að setja upp stillingar vefforrits á síðunni **Vefforrit** (**Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Vefforrit**).

Eftirfarandi tafla lýsir svæðunum á síðunni **Vefforrit**.

| Svæði                         | Lýsing |
|-------------------------------|-------------|
| Heiti forrits              | Færið inn heiti á vefforritinu. |
| Lýsing                   | Færið inn lýsingu á vefforritinu. |
| Grunnvefslóð                      | Færið inn grunnveffangið fyrir vefforritið. |
| Vefslóð heimildar        | Tilgreinið slóðina til að búa til vefslóð fyrir heimild.  |
| Vefslóð merkis                | Tilgreinið slóðina til að búa til vefslóð fyrir lykil.  |
| Framsendingarslóð                  | Færið inn vefslóð áframsendingar.  |
| Biðlarakenni                     | Færið inn biðlarakenni vefforritsins.  |
| Leynilykill biðlara                 | Færið inn leynilykil biðlara fyrir vefforritið.  |
| Þjónsmerki                  | Færið inn þjónsmerki vefforritsins.  |
| Sniðsvörpun heimildar  | Veljið snið rafrænnar skýrslugerðar sem verður notað til að búa til beiðni um heimild.   |
| Flytja inn líkanavörpun merkis    | Veljið líkanavörpun fyrir innflutning rafrænnar skýrslugerðar sem verður notuð til að geyma aðgangslykla.  |
| Leyfilegt umfang      Aðgangslykill rennur út eftir  | Þessi reitur verður uppfærður sjálfkrafa. Gildi hans sýnir veitt umfang beiðna að vefforritinu.  |
| Samþykkja                        | Tilgreinið samþykktareiginleika vefbeiðni. Til dæmis „application/vnd.hmrc.1.0+json“.  |
| Gerð innihalds           | Tilgreina efnisgerðir. Til dæmis „application/json“.  |

Eftirfarandi aðgerðir eru tiltækar af síðunni **Vefforrit** til að styðja heimildarferli:
-   **Fá heimildarkóða** - til að frumstilla heimild vefforritsins.
-   **Fá aðgangslykil** - til að frumstilla afhendingu á aðgangslykli.
-   **Endurnýja aðgangslykil** - til að endurnýja aðgangslykil.

Þegar aðgangslykill að vefforriti sem er vistaður í gagnagrunni kerfisins er á dulrituðu sniði, er hægt að nota hann fyrir beiðnir að vefþjónustu. Í öryggisskyni skal aðgangur að aðgangslykli takmarkast eingöngu við þau öryggishlutverk sem verður að heimila að taka á þessum beiðnum. Þegar notandi utan öryggisflokks reynir að takast á við beiðni, mun undantekning upplýsa notanda um að honum/henni sé ekki heimilt að starfa í gegnum valið vefforrit.
Notaðu flýtitöfluna **Öryggishlutverk** á síðunni Skattur > Uppsetning > Rafræn skilaboð > Vefforrit til að setja upp hlutverk sem verða að hafa aðgang að aðgangslykli. Þegar öryggishlutverk eru ekki skilgreind fyrir vefforrit, getur kerfisstjóri aðeins unnið í gegnum þetta vefforrit.

### <a name="web-service-settings"></a>Stillingar vefþjónustu

Stillingar vefþjónustu eru notaðar til að setja upp beinan gagnaflutning til vefþjónustu. Hægt er að setja upp stillingar vefþjónustu á síðunni **Stillingar vefþjónustu** (**Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Stillingar vefþjónustu**).

Eftirfarandi tafla lýsir svæðunum á síðunni **Stillingar vefþjónustu**.

| Svæði                   | lýsing |
|-------------------------|-------------|
| Vefþjónusta             | Færið inn heiti á vefþjónustunni. |
| lýsing             | Færið inn lýsingu á vefþjónustunni. |
| Internet-fang        | Færið inn veffangið á vefþjónustunni. Ef vefforrit er tilgreint fyrir vefþjónustu og veffangið á að vera það sama og er skilgreint fyrir valið vefforrit skal smella á hnappinn **Afrita grunnvefslóð** til að afrita **Grunnvefslóð** úr vefforriti í svæðið **Vefsvæði** hjá vefþjónustu.  |
| Skírteini             | Veljið vottorð lyklageymslu sem hefur verið sett upp áður. |
| Vefforrit         | Veljið vottorð lyklageymslu sem hefur verið sett upp áður. |
| Gerð svars – XML | Stillið þennan valkost á **Já** ef gerð svars er XML. |
| Aðferð beiðni          | Tilgreinið aðferð beiðninnar. HTTP skilgreinir safn af beiðnum sem gefa til kynna aðgerðina sem á að framkvæma fyrir tiltekin tilföng. Aðferðin getur verið **GET**, **POST** eða önnur HTTP-aðferð. |
| Haus beiðni         | Tilgreina haus beiðni. Haus beiðni er HTTP-haus sem hægt er að nota í HTTP-beiðni og sem tengist ekki innihaldi skilaboðanna. |
| Samþykkja                  | Tilgreina samþykktareiginleika vefbeiðni. |
| Samþykkja kóðun         | Tilgreina samþykki kóðunar. HTTP beiðnishaus fyrir samþykki kóðunar gefur kóðun innihalds til kynna sem biðlarinn getur skilið. Þessi kóðun innihalds er venjulega þjappað reiknirit. |
| Gerð innihalds            | Tilgreina gerð innihalds. Haus fyrir einingu innhaldsgerðar gefur til kynna miðilsgerð tilfanga. |
| Svarkóði tókst   | Tilgreina stöðukóða HTTP sem gefur til kynna að beiðnin hafi heppnast. |
| Sniðsvörpun síðuhausa fyrir beiðnir  | Veljið snið rafrænnar skýrslugerðar til að búa til hausa vefbeiðni. |

### <a name="message-processing-actions"></a>Úrvinnsluaðgerðir skilaboða

Úrvinnsluaðgerðir skilaboða eru notaðar til að stofna aðgerðir fyrir vinnslurnar og til að setja upp færibreytur þeirra. Hægt er að setja upp úrvinnsluaðgerðir á síðunni **Úrvinnsluaðgerðir skilaboða** (**Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Úrvinnsluaðgerðir skilaboða**).

Eftirfarandi töflur lýsa svæðunum á síðunni **Úrvinnsluaðgerðir skilaboða**.

#### <a name="general-fasttab"></a>Flýtiflipinn Almennt

| Svæði                   | lýsing |
|-------------------------|-------------|
| Gerð aðgerðar             | Veljið þessa gerð aðgerðar. Upplýsingar um tiltæka valkosti eru í kaflanum [Gerðir úrvinnsluaðgerða skilaboða](#message-processing-action-types). |
| Sniðsvörpun          | Veljið snið rafrænnar skýrslugerðar sem á að kalla á fyrir aðgerðina. Þetta svæði er aðeins í boði fyrir aðgerðir af gerðunum **Útflutningur á rafrænum skýrslum**, **Innflutningur á rafrænum skýrslum**, **Útflutningsskilaboð rafrænna skýrslna**. |
| Sniðsvörpun fyrir vefslóð | Veljið snið rafrænnar skýrslugerðar sem á að kalla á fyrir aðgerðina. Þetta svæði er eingöngu í boði fyrir aðgerðir af gerðinni **Vefþjónusta** og er notað til að búa til slóð fyrir veffang sem verður bætt við grunnveffangið sem er tilgreint fyrir valinn vefþjón. |
| Gerð skilaboðaatriðis       | Veljið færslugerðir sem meta á aðgerðina fyrir. Þetta svæði er aðeins í boði fyrir aðgerðir af gerðunum **Framkvæmdastig skilaboðaatriða**, **Útflutningur á rafrænum skýrslum** og **Innflutningur á rafrænum skýrslum**, **Vefþjónusta** og einnig fyrir nokkrar aðrar gerðir. Ef þetta svæði er skilið eftir autt verða allar gerðir skilaboðaatriða metnar sem eru skilgreindar fyrir úrvinnslu skilaboða. |
| Keyranlegur klasi        | Veljið keyranlegar klasastillingar sem hafa verið stofnaðar áður. Þetta svæði er aðeins í boði fyrir aðgerðir af gerðunum **Framkvæmdastig skilaboðaatriða** og **Framkvæmdastig skilaboðaatriða**. |
| Fylla út færsluaðgerð | Veljið áður uppsetta aðgerð sem fyllir út færslur. Þetta svæði er aðeins í boði fyrir aðgerðir af gerðinni **Fylla út færslur**. |
| Vefþjónusta  | Veljið vefþjónustu sem var áður sett upp. Þetta svæði er aðeins í boði fyrir aðgerðir af gerðinni **Vefþjónusta**.  |
| Skrárnafn  | Tilgreindu heiti skráarinnar sem mun leiða til aðgerðarinnar sem svar frá vefþjóni eða myndun á skýrslu. Þetta svæði er aðeins í boði fyrir aðgerðir af gerðinni **Vefþjónusta** og **Útflutningsskilaboð rafrænna skýrslna**.   |
| Sýna svarglugga  | Merktu við þennan gátreit ef birta þarf svarglugga fyrir notanda áður en skýrsla er búin til. Þetta svæði er aðeins í boði fyrir aðgerðir af gerðinni **Útflutningsskilaboð rafrænna skýrslna**.   |

##### <a name="message-processing-action-types"></a>Gerðir úrvinnsluaðgerðar skilaboða

Eftirfarandi valkostir eru í boði í svæðinu **Gerð aðgerðar**:

- **Stofna skilaboð** – Notið þessa gerð til að leyfa notendum að stofna skilaboð handvirkt á síðunni **Rafræn skilaboð**. Ekki er hægt að setja upp upphafsstöðu fyrir aðgerð af þessari gerð.
- **Fylla út færslur** – Aðgerðin **Fylla út færslur** verður að hafa verið sett upp áður. Tengið hana við aðgerð af gerðinni **Fylla út færslur** til að virkja hana svo hún geti verið hluti af úrvinnslu. Gert er ráð fyrir að þessi gerð aðgerðar sé notuð annaðhvort fyrir fyrstu aðgerðina í úrvinnslu skilaboða (þegar engin rafræn skilaboð eru búin til fyrirfram) eða sem aðgerð sem bætir skilaboðaatriðum við eldri skilaboð (með aðgerð af gerðinni **Búa til skilaboð**). Þess vegna er hægt að setja upp lokastöðu fyrir eingöngu skilaboðaatriði fyrir aðgerð af þessari gerð. Eingöngu er hægt að setja upp upphafsstöðu fyrir skilaboð.
- **Framkvæmdastig skilaboða** – Notið þessa gerð til að setja upp keyranlegan klasa sem á að vera metinn á skilaboðastigi.
- **Framkvæmdastig skilaboðaatriða** – Notið þessa gerð til að setja upp keyranlegan klasa sem á að vera metinn á stigi skilaboðaatriða.
- **Útflutningur á rafrænum skýrslum** – Notið þessa gerð fyrir aðgerðir sem eiga að búa til skýrslu sem miðast við skilgreiningu á útflutningi á rafrænum skýrslum á stigi skilaboðaatriða.
- **Útflutningsskilaboð rafrænna skýrslna** – Notið þessa gerð fyrir aðgerðir sem eiga að búa til skýrslu sem miðast við skilgreiningu á útflutningi á rafrænum skýrslum á skilaboðastigi (til dæmis þegar skilaboð eru ekki með nein skilaboðaatriði).
- **Innflutningur á rafrænum skýrslum** – Notið þessa gerð fyrir aðgerðir sem eiga að búa til skýrslu sem miðast við skilgreiningu á innflutningi á rafrænum skýrslum.
- **Úrvinnsla notanda á skilaboðastigi** – Notið þessa gerð fyrir aðgerðir sem gera ráð fyrir nokkrum handvirkum aðgerðum notanda. Til dæmis gæti notandi uppfært stöðu skilaboða.
- **Úrvinnsla notanda** – Notið þessa gerð fyrir aðgerðir sem gera ráð fyrir nokkrum handvirkum aðgerðum notanda. Til dæmis gæti notandi uppfært stöðu skilaboðaatriða.
- **Vefþjónusta** – Notið þessa gerð fyrir aðgerðir sem eiga að senda myndaða skýrslu til vefþjónustu. Þessi gerð aðgerðar er ekki notuð fyrir skýrslugerð ítalskra innkaupa- og sölureikningasamskipta. Fyrir aðgerðir af gerðinni **Vefþjónusta** er hægt að tilgreina **Staðfestingartexti** í flýtiflipanum **Ýmsar upplýsingar** í **Úrvinnsluaðgerðir skilaboða**. Þessi staðfestingartexti verður sýndur notandanum áður en tekið verður á beiðni til valdrar vefþjónustu.
- **Beiðni um sannprófun** – Notið þessa gerð til að óska eftir sannprófun frá þjóni.

#### <a name="initial-statuses-fasttab"></a>Flýtiflipi fyrir upphafsstöður

> [!NOTE]
> Flýtiflipinn **Upphafsstöður** er ekki í boði fyrir aðgerðir sem eru með upphafsgerðina **Stofna skilaboð**.

| Svæði               | Lýsing                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------|
| Staða skilaboðaatriðis | Veljið stöðu skilaboðaatriðis sem á að meta valda úrvinnsluaðgerð skilaboða fyrir. |
| lýsing         | Lýsing á stöðu valins skilaboðaatriðis.                                                  |

#### <a name="result-statuses-fasttab"></a>Flýtiflipi fyrir lokastöður

| Svæði               | lýsing |
|---------------------|-------------|
| Staða skilaboða      | Veljið stöðu skilaboða sem á að meta valda úrvinnsluaðgerð skilaboða fyrir. Þetta svæði er aðeins í boði fyrir úrvinnsluaðgerðir skilaboða sem eru metnar á skilaboðastigi. Það er í boði fyrir aðgerðir af gerðunum **Útflutningur á rafrænum skýrslum** og **Innflutningur á rafrænum skýrslum**. Það er ekki í boði fyrir aðgerðir af gerðunum **Úrvinnsla notanda** og **Framkvæmdastig skilaboðaatriða**. |
| lýsing         | Lýsing á stöðu valinna skilaboða. |
| Gerð svars       | Gerð svars fyrir valda stöðu skilaboða. |
| Staða skilaboðaatriðis | Veljið stöðurnar sem eiga að vera tiltækar eftir matið á úrvinnsluaðgerð valinna skilaboða. Þetta svæði er aðeins í boði fyrir úrvinnsluaðgerðir skilaboða sem eru metnar á stigi skilaboðaatriða. Það er til dæmis í boði fyrir aðgerðir af gerðunum **Úrvinnsla notanda** og **Framkvæmdastig skilaboðaatriða**. Fyrir úrvinnsluaðgerðir skilaboða sem eru metnar á skilaboðastigi, sýnir þetta svæði stöðu skilaboðaatriðis sem var sett upp fyrir valda stöðu skilaboða. |

Eftirfarandi tafla sýnir hvaða lokastöður verða að vera uppsettar hvað varðar gerðir aðgerða:

| Gerð rafrænnar skilaboðaaðgerðar \ Gerð svars  | Framkvæmt  | Viðskiptavilla  | Tæknileg villa  | Notandaskilgreint  | Hætta við  |
|-------------------------------------------------|--------------|---------|-------|-----|-----------------|
| Stofna skilaboð                                  | X            |         |       |     |                 |
| Útflutningur rafrænnar skýrslugerðar                     | X            |         |       |     |                 |
| Innflutningur rafrænnar skýrslugerðar                     |              |         |       |     |                 |
| Vefþjónusta                                     | X            |         | X     |     |                 |
| Í vinnslu hjá notanda                                 |              |         |       |     |                 |
| Framkvæmdastig skilaboða                         |              |         |       |     |                 |
| Fylla út færslur                                |              |         |       |     |                 |
| Framkvæmdastig skilaboðaatriðis                    |              |         |       |     |                 |
| Biðja um staðfestingu                            | X            |  X      | X     |     |                 |
| Útflutningsskilaboð rafrænnar skýrslugerðar             | X            |         |       |     |                 |
| Úrvinnsla skilaboðastigs                   |              |         |       |     |                 |

### <a name="electronic-message-processing"></a>Rafræn skilaboð í vinnslu

Úrvinnsla á rafrænum skilaboðum er grundvallaratriði í virkni rafrænna skilaboða. Vinnslan safnar saman aðgerðum sem á að meta fyrir rafrænu skilaboðin. Hægt er að tengja aðgerðirnar í gegnum upphafsstöðu og lokastöðu. Annars er hægt að hefja hverja aðgerð fyrir sig af gerðinni **Úrvinnsla notanda**. Á síðunni **Úrvinnsla rafrænna skilaboða** (**Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Úrvinnsla rafrænna skilaboða**) er einnig hægt að velja önnur svæði sem eiga að vera studd fyrir úrvinnsluna annaðhvort á stigi skilaboða eða stigi skilaboðaatriðis.

Flýtiflipinn **Aðgerðir** gerir þér kleift að bæta forskilgreindum aðgerðum við úrvinnsluna. Hægt er að tilgreina hvort keyra verði aðgerð sérstaklega eða hvort vinnslan geti ræst hana. Til að tilgreina hvort eingöngu notandi geti frumstillt aðgerðina skal merkja gátreitinn **Keyra sérstaklega** fyrir aðgerðina í úrvinnslunni. Afmerkja færibreytuna **Keyra sérstaklega** ef þú vilt að aðgerðin hefjist með vinnslu þegar skilaboð eða skilaboðaatriði í stöðunni eru skilgreind sem upphafsstaða fyrir þennan hluta. Aðgerð af gerðinni **Aðgerð notanda** má eingöngu keyra sérstaklega. 

Stundum getur það reynst nauðsynlegt til að safna saman nokkrum aðgerðum í röð, jafnvel þótt fyrsta aðgerðin er skilgreind til að keyrast sérstaklega. Til dæmis, þegar krafist er að skýrslumyndun verði frumstillt af notanda en þegar skýrslan er mynduð verður að senda hana strax á vefþjónustu og svar vefþjónustunnar verður að koma fram í kerfinu. Í slíkum tilgangi er hægt að nota **Óaðskiljanlega röð**. Til að gera það er smellt á hnappinn **Óaðskiljanleg röð** í aðgerðarúðunni í flýtiflipanum **Aðgerð** á síðunni **Úrvinnsla rafrænna skilaboða**, búa til röð og velja hana í dálknum **Óaðskild röð** fyrir þær aðgerðir sem þarf alltaf að keyra saman. Fyrsta aðgerðin í þessu tilfelli er hægt að setja upp sem **Keyra sérstaklega** en ekki hinar aðgerðirnar.

Flýtiflipinn **Önnur svæði skilaboðaatriða** gerir þér kleift að bæta við öðrum forskilgreindum svæðum sem tengjast skilaboðaatriðum. Bæta verður við öðrum svæðum fyrir hverja gerð skilaboðaatriða sem svæðin tengjast.

Flýtiflipinn **Önnur svæði skilaboða** gerir þér kleift að bæta við öðrum forskilgreindum svæðum sem tengjast skilaboðum.

Flýtiflipinn **Öryggishlutverk** gerir þér kleift að setja upp öryggishlutverk sem eru forskilgreind í kerfinu fyrir tilteknar vinnslur. Notendur með tiltekið hlutverk sjá aðeins vinnslu sem er skilgreind fyrir það hlutverk.

Flýtiflipinn **Runa** gerir þér kleift að setja upp vinnslu til að vinna í runufyrirkomulagi.

## <a name="work-with-electronic-messages-functionality"></a>Vinna með virkni rafrænna skilaboða

Ef unnið er á skilaboðastigi, þá er gagnlegra að nota síðuna **Rafræn skilaboð** (**Skattur** \> **Fyrirspurnir og skýrslur** \> **Rafræn skilaboð** \> **Rafræn skilaboð**). Ef starfað er á stigi gagnasöfnunar (skilaboðaatriðis), þá er gagnlegra að nota síðuna **Rafræn skilaboðaatriði** (**Skattur** \> **Fyrirspurnir og skýrslur** \> **Rafræn skilaboð** \> **Rafræn skilaboðaatriði**).

### <a name="electronic-messages"></a>Rafræn skilaboð

Síðan **Rafræn skilaboð** birtir tiltæka vinnslu samkvæmt hlutverki þínu. Öryggishlutverk tengjast vinnslu við uppsetningu þeirrar vinnslu. Síðan sýnir rafræn skilaboð og upplýsingar sem tengjast hverri vinnslu sem er þér tiltæk.

Flýtiflipinn **Skilaboð** birtir rafræn skilaboð fyrir valda vinnslu. Það fer eftir stöðu valdra skilaboða og forskilgreindra vinnsla hvaða aðgerðir hægt er að keyra með því að velja hnappana fyrir ofan hnitanetið:

- **Ný** – Þessi hnappur tengist aðgerðum af gerðinni **Stofna skilaboð**.
- **Eyða** – Þessi hnappur er í boði ef gátreiturinn **Leyfa eyðingu** er valinn fyrir núgildandi stöðu á völdum skilaboðum.
- **Safna gögnum** - Þessi hnappur tengist aðgerð af gerðinni **Fylla út færslur**.
- **Búa til skýrslu** – Þessi hnappur tengist aðgerðum af gerðinni **Útflutningsskilaboð rafrænna skýrslna**.
- **Senda skýrslu** – Þessi hnappur tengist aðgerðum af gerðinni **Vefþjónusta**.
- **Innflutningssvar** - Þessi hnappur tengist aðgerðum af gerðinni **Innflutningur rafrænna skýrslna**.
- **Uppfærslustaða** – Þessi hnappur er tengdur við aðgerðir af gerðinni **Úrvinnsla notanda á skilaboðastigi**.
- **Skilaboðaatriði** – Opnið síðuna **Rafræn skilaboðaatriði**.

Flýtiflipinn **Aðgerðakladdi** sýnir upplýsingar um allar aðgerðir sem hafa verið keyrðar fyrir valin skilaboð. Ef aðgerð leiddi til villu verða upplýsingar um villuna festar við tengda línu aðgerðakladda. Veldu línuna og smelltu á hnappinn **myndskeið** efst í hægra horninu á síðunni til að yfirfara upplýsingar um villuna.

Flýtiflipinn **Önnur svæði skilaboða** sýnir öll önnur svæði sem eru skilgreind fyrir skilaboð í uppsetningu á vinnslu. Hann sýnir einnig gildi þessara svæða.

Flýtiflipinn **Skilaboðaatriði** sýnir öll skilaboðaatriði sem tengjast völdu skilaboði. Fyrir sérhvert skilaboðaatriði er hægt að nota eftirfarandi virkni, fer eftir stöðu á þessu skilaboðaatriði:

- **Eyða** – Þessi hnappur er í boði ef gátreiturinn **Leyfa eyðingu** er valinn fyrir núgildandi stöðu á völdum skilaboðum.
- **Uppfærslustaða** – Þessi hnappur tengist aðgerðum af gerðinni **Úrvinnsla notanda**.
- **Upprunalegt skjal** - Þessi hnappur gerir notanda kleift að opna síðu með upprunalegu skjali valins skilaboðs.

Hægt er að yfirfara öll viðhengi valinna skilaboða. Þessi viðhengi eru skýrslur sem hafa þegar verið búnar til og mótteknar. Veljið skilaboðin þar sem yfirfara á viðhengi, og veljið svo hnappinn **Viðhengi** á aðgerðasvæðinu.

![Hnappur viðhengis](media/attachment-icon.png)

Síðan **Viðhengi** sýnir öll viðhengi sem tengjast skilaboðunum. Til að skoða skrá skal velja hana af listanum til vinstri og velja síðan **Opna** á aðgerðasvæðinu.

![Hnappurinn opna](media/open-button.png)

Til að yfirfara viðhengi sem tengist tiltekinni aðgerð sem var keyrð áður fyrir skilaboð skal velja skilaboðin á síðunni **Rafræn skilaboð** og síðan velja aðgerðina á flýtiflipanum **Aðgerðakladdi**. Veljið síðan hnappinn **Viðhengi** á aðgerðasvæði.

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
<td>Reikningsnúmer viðskiptamanns eða lánardrottins (eða annað gildi svæðis, sem fer eftir svæðinu sem er skilgreint í aðgerðinni <strong>Fylla út færslur</strong>). Aðeins er hægt að fylla þetta svæði út þegar reikningi er bætt við töflu skilaboðaatriða.</td>
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
<td>Næstu aðgerðir sem hægt er að ræsa fyrir núverandi stöðu skilaboðaatriðis.</td>
</tr>
</tbody>
</table>

Flipinn **Önnur svæði** sýnir önnur svæði fyrir valið skilaboðaatriði og gildin þeirra.

#### <a name="run-processing"></a>Keyra vinnslu

Veljið **Keyra vinnslu** á aðgerðasvæðinu til að keyra vinnslu fyrir skilaboðaatriði. Til að keyra tiltekna aðgerð skal, í gátreitnum **Keyra vinnslu**, stilla valkostinn **Velja aðgerð** á **Já** og síðan velja aðgerð. Til að keyra alla vinnsluna skal hafa valkostinn **Velja aðgerð** stilltan á **Nei**.

#### <a name="generate-report"></a>Búa til skýrslu

Veljið **Búa til skýrslu** á aðgerðasvæðinu til að búa til skýrslu. Þessi hnappur tengist aðgerðum af gerðinni **Útflutningur á rafrænum skýrslum**.

#### <a name="update-status"></a>Uppfæra stöðu

Veljið **Uppfæra stöðu** á aðgerðasvæðinu til að uppfæra stöðu á einu eða fleiri skilaboðaatriðum. Í gátreitnum **Uppfæra stöðu** skal nota flýtiflipann **Færslur til að taka með** til að velja skilaboðaatriði fyrir uppfærslu. Gangið úr skugga um að valskilyrði séu rétt skilgreind vegna þess að stöður skilaboðaatriða verða uppfærðar samkvæmt þessum skilyrðum, upphafsstöðu valdrar aðgerðar og gildinu sem var stillt fyrir **Ný staða**. Eftir að stöðuuppfærslu er lokið verður erfitt að finna út hvaða atriði voru uppfærð. Því verður erfitt að endurheimta stöðuuppfærslur.

#### <a name="electronic-messages"></a>Rafræn skilaboð

Veljið **Rafræn skilaboð** á aðgerðasvæðinu til að yfirfara rafræn skilaboð sem tengjast völdu skilaboðaatriði.

Einnig er hægt að yfirfara allar skrár sem samsvara skilaboðaatriðinu. Veljið svæðið **Skilaboð** úr skilaboðaatriði eða veljið **Rafræn skilaboð** á aðgerðasvæðinu. Á síðunni **Rafræn skilaboð** skal velja skilaboðin þar sem yfirfara á skýrslu, og veljið svo hnappinn **Viðhengi** á aðgerðasvæðinu.

![Hnappur viðhengis](media/attachment-icon.png)

Síðan **Viðhengi** sýnir öll viðhengi sem tengjast skilaboðunum. Til að skoða skrá skal velja hana af listanum til vinstri og velja síðan **Opna** á aðgerðasvæðinu.

![Hnappurinn opna](media/open-button.png)

#### <a name="original-document"></a>Upprunalegt skjal

Veljið **Upprunalegt skjal** á aðgerðasvæðinu til að opna upprunalegt skjal fyrir valið skilaboðaatriði.

## <a name="example"></a>Dæmi

Eftir að snið rafrænnar skýrslugerðar hefur verið stofnað, því varpað í gagnaveitur og því lokið, er hægt að keyra það með því að nota vinnusvæðið **Rafræn skýrslugerð**. Skýrsla er búin til sem hægt er að vista á staðnum.

Til að stjórna eftirfarandi þáttum skýrslugerðarferlisins þarf að setja upp úrvinnslu á rafrænum skilaboðum:

- Skrá upplýsingar um þann sem bjó til skýrsluna.
- Skrá hvenær skýrslan var búin til.
- Vista skýrslur sem voru búnar til fyrir fyrri tímabil.

Þessi hluti kemur með dæmi um hvernig hægt er að setja upp virkni rafrænna skilaboða til að búa til vinnslu skýrslugerðar.

### <a name="set-up-and-run-processing-to-call-a-simple-er-exporting-format-to-generate-an-excel-report"></a>Setjið upp og keyrið vinnslu til að kalla á einfalt útflutningssnið rafrænnar skýrslugerðar til að búa til Excel-skýrslu

Þessi hluti kemur með dæmi um hvernig hægt er að setja upp rafræn skilaboð til að búa til skýrslu sem byggist á útflutningssniði rafrænnar skýrslugerðar fyrir Excel. Til að fylgja þessu dæmi verður útflutningssnið rafrænnar skýrslugerðar að hafa verið búið til, því varpað í gagnaveitur og því lokið. Númeraröð verður að vera uppsett fyrir rafræn skilaboð.

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
    - Á flýtiflipanum **Lokastöður**, á svæðinu **Staða skilaboða**, skal velja **Undirbúin** eða (og) **Ný**. Á svæðinu **Gerð svars** skal fara í **Keyrsla heppnaðist**.

#### <a name="electronic-message-processing"></a>Rafræn skilaboð í vinnslu

Í þessu dæmi á að setja upp allar aðgerðirnar svo þær keyri hver fyrir sig. Gert er ráð fyrir því að notandi frumstilli hverja aðgerð.

1. Opnið **Skattur \> Uppsetning \> Rafræn skilaboð \> Úrvinnsla rafrænna skilaboða**.
2. Bætið við færslu fyrir vinnsluna og bætið við öllum áður skilgreindum aðgerðum og öðrum svæðum.
3. Valfrjálst: Á flýtiflipanum **Öryggishlutverk** skal skilgreina öryggishlutverk fyrir vinnslurnar til að takmarka aðgang að tilteknum skýrslum.
4. Opnið **Skattur \> Fyrirspurnir og skýrslur \> Rafræn skilaboð \> Rafræn skilaboð**.
5. Veljið **Ný** til að stofna ný skilaboð. Á þessum tímapunkti er hægt að bæta við dagsetningum og lýsingu. Einnig er hægt að uppfæra gildið á viðbótarsvæði eins og þörf krefur.

    ![Stofna rafræn skilaboð](media/create-electronic-message.png)

Fyllt er sjálfkrafa inn í hnitanetið á flýtiflipanum **Aðgerðakladdi** með kladda yfir allar aðgerðir sem eru framkvæmdar á skilaboðinu.

Nú er annaðhvort hægt að eyða eða uppfæra stöðu skilaboða. Til að uppfæra stöðu skilaboða skal velja svæðið **Uppfæra stöðu** og síðan, í svæðinu **Ný staða**, skal velja **Undirbúin**. Veljið síðan **Í lagi**.

![Uppfæra stöðu skilaboða](media/update-status.png)

Staða skilaboða er uppfærð í **Undirbúin** og hægt er að búa til skýrsluna með því að velja **Búa til skýrslu**. Skýrslan er búin til og uppfærsla gerð á stöðu skilaboða og aðgerðakladda. Til að skoða skýrsluna sem var búin til skal velja hnappinn **Viðhengi** á aðgerðasvæðinu.
