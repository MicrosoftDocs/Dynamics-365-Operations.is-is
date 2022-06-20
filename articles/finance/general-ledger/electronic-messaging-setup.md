---
title: Setja upp rafræn skilaboð
description: Þessi grein veitir upplýsingar um hvernig á að setja upp rafræn skilaboð (EM) virkni.
author: liza-golub
ms.date: 11/18/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2021-06-23
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 6ac6e4fbc37165a3126de3b1f937a43c980410b4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874552"
---
# <a name="set-up-electronic-messages"></a>Setja upp rafræn skilaboð

[!include [banner](../includes/banner.md)]

Virkni **Rafrænna skilaboða** auðvelda að viðhalda mismunandi ferlum rafrænnar skýrslugerðar fyrir mismunandi skjalategundir. Í sumum flóknum aðstæðum sem styðja [skýrslugerðareiginleika tiltekins lands](electronic-messaging.md#country-specific-regulatory-features-supported-by-the-em-functionality) er virkni rafrænna skilaboða sett upp svo hún sé með samsetningu af mörgum skilaboðastöðum, stöðum skilaboðaatriða, öðrum svæðum og keyranlegum klösum. Í þessum tilfellum er innflutningur á gagnaeiningapökkum í boði. Ef þessir gagnaeiningapakkar eru notaðir skal flytja þá inn í lögaðila með verkfæri gagnastjórnunar. Frekar upplýsingar um hvernig á að nota verkfæri gagnastjórnunar eru í [Gagnastjórnun](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).

Hægt er að setja upp virknina rafrænna skilaboða handvirkt ef gagnaeiningapakki er ekki fluttur inn. Í þessu tilfelli þarf að setja upp eftirfarandi þætti:

- [Númeraraðir](#sequences)
- [Gerðir skilaboðaatriðis](#types)
- [Stöður skilaboðaatriðis](#item)
- [Stöður skilaboða](#statuses)
- [Önnur svæði](#additional)
- [Keyranlegar klasastillingar](#executable)
- [Fylla út færsluaðgerðir](#populate)
- [Fylltu út skrár frá mörgum fyrirtækjum](#multiple-companies-populate)
- [Vefforrit](#applications)
- [Stillingar vefþjónustu](#settings)
- [Úrvinnsluaðgerðir skilaboða](#actions)
- [Rafræn skilaboð í vinnslu](#processing)

Eftirfarandi hlutar veita frekari upplýsingar um hvern þátt fyrir sig.

## <a name="number-sequences"></a><a id="sequences"></a>Númeraraðir

Setja upp númeraraðir fyrir bæði skilaboð og skilaboðaatriði. Númeraraðir eru þá notaðar til að sjálfkrafa gefa skilaboðum og skilaboðaatriðum númer. Úthlutuð númer eru notuð sem einkvæm auðkenni fyrir skilaboðin og skilaboðaatriðin í kerfinu. Hægt er að setja upp númeraraðir fyrir rafræn skilaboð með því að fara á síðuna **Fjárhagur** \> **Uppsetning fjárhags** \> **Færibreytur fjárhags**.

## <a name="message-item-types"></a><a id="types"></a>Gerðir skilaboðaatriðis

Gerðir skilaboðaatriða bera kennsl á færslutegundir sem eru notaðar í rafrænum skilaboðum. Hægt er að setja upp gerðir skilaboðaatriða með því að fara á síðuna **Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Gerðir skilaboðaatriðis**.

## <a name="message-item-statuses"></a><a id="item"></a>Stöður skilaboðaatriðis

Stöður skilaboðaatriða bera kennsl á stöðurnar sem gilda um skilaboðaatriði í vinnslunni sem verið er að setja upp. Hægt er að setja upp stöður skilaboðaatriða með því að fara á síðuna **Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Stöður skilaboðaatriða**.

Færibreytan **Leyfa eyðingu** fyrir stöðu skilaboðaatriðis skilgreinir hvort hægt sé að eyða skilaboðaatriðum sem eru með þessa stöðu á síðunni **Rafræn skilaboð** eða á síðunni **Rafræn skilaboðaatriði**.

## <a name="message-statuses"></a><a id="statuses"></a>Stöður skilaboða

Setja upp stöður skilaboða sem eiga að vera tiltæk í vinnslu skilaboða. Hægt er að setja upp stöður skilaboða með því að fara á síðuna **Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Stöður skilaboða**.

Eftirfarandi tafla lýsir reitunum á síðunni **Skilaboðastöður**.

| Svæðisheiti          | Lýsing |
|---------------------|-------------|
| Staða boða      | Færið inn einkvæmt heiti fyrir stöðu skilaboðs. Skilaboðastöður eru notaðar til að einkenna stöðu rafrænna skilaboða á hverju augnabliki fyrir sig. Nafnið sem þú slærð inn birtist á síðunni **Rafræn skilaboð** og í kladda sem tengist rafrænum skilaboðum. |
| Lýsing         | Færa inn lýsingu á skilaboðastöðunni. |
| Gerð svars       | Veldu svargerðina fyrir skilaboðastöðuna. Sumar aðgerðir í vinnslu geta gefið af sér fleiri en eina gerð svars. Til dæmis getur aðgerð af gerðinni **Vefþjónusta** gefið svör af annaðhvort gerðinni **Framkvæmd heppnaðist** eða gerðinni **Tæknileg villa**, fer eftir niðurstöðu keyrslunnar. Í þessu tilviki skal skilgreina skilaboðastöður fyrir báðar svargerðirnar. Fyrir frekari upplýsingar um gerðir aðgerða og tegundir svara sem tengjast þeim, sjáðu [Gerðir aðgerða fyrir skilaboðavinnslu](#action-types) kafla síðar í þessari grein. |
| Staða skilaboðaatriðis | Stundum verður staða á rafrænum skilaboðum að hafa áhrif á stöðu tengdra skilaboðaatriða. Veldu stöðu skilaboðaatriðis í þessum reit til að tengja hana við skilaboðastöðu. |
| Leyfa eyðingu        | Veldu þennan reit ef notendur ættu að geta eytt rafrænum skilaboðum sem hafa þessa stöðu á síðunni **Rafræn skilaboð**. |

## <a name="additional-fields"></a><a id="additional"></a>Önnur svæði

EM virkni gerir þér kleift að safna færslum úr viðskiptatöflum inn Microsoft Dynamics 365 Fjármál sem skilaboðaliðir. Þannig er hægt að undirbúa færslurnar fyrir skýrslugerð og síðan tilkynna þær. Hins vegar hafa færslutöflur stundum ekki nægar upplýsingar til að fylla út færslur á þann hátt að það uppfylli kröfur um skýrslugjöf. Til að fylla út allar upplýsingar sem þarf að tilkynna um færslu er hægt að setja upp önnur svæði. Önnur svæði geta tengst skilaboðum og skilaboðaatriðum. Hægt er að setja upp önnur svæði með því að fara á síðuna **Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Önnur svæði**.

Eftirfarandi tafla lýsir almennu svæðunum á síðunni **Önnur svæði**.

| Svæði       | lýsing |
|-------------|-------------|
| Heiti reits  | Sláið inn heiti á viðbótarsvæðinu fyrir rafræn skilaboð eða skilaboðaatriði sem tengjast vinnslunni. Þetta heiti birtist í notandaviðmótinu á meðan unnið er í vinnslunni. Einnig er hægt að nota heitið í stillingum rafrænnar skýrslugerðar sem tengjast vinnslunni. |
| lýsing | Færa inn lýsingu á viðbótarsvæði. |
| Breyting notanda   | Stilla skal þennan valkost á **Já** ef notendur eiga að geta breytt gildinu á viðbótarsvæðinu í notandaviðmótinu. |
| Teljari     | Stilltu þennan valkost í **Já** ef viðbótarsvæðið á að innihalda númeraröð í rafrænum skilaboðum. Gildi viðbótarsvæðisins verður fyllt út sjálfkrafa við keyrslu á aðgerð af gerðinni **Útflutningur rafrænnar skýrslugerðar**. |
| Falið      | Stilltu þennan valkost á **Já** ef viðbótarsvæðið á að vera falið í notandaviðmótinu á síðunni **Rafræn skilaboð** eða síðunni **Rafræn skilaboðaatriði**. |

Í flýtiflipanum **Gildi** er hægt að skilgreina fyrirfram gildi sem viðbótarsvæði getur fengið. Notendur geta þá valið úr þessum gildum. Þar af leiðandi þarf ekki að fylla þau út handvirkt við úrvinnslu. Eftirfarandi tafla lýsir svæðunum.

| Svæði                | lýsing |
|----------------------|-------------|
| Svæðisgildi          | Sláið inn svæðisgildi sem er notað fyrir skilaboð eða skilaboðaatriði við skýrslugerð. |
| Lýsing          | Færið inn lýsingu á gildi svæðisins. |
| Reikningsgerð         | Sum gildi svæða kunna að takmarkast við tilteknar lyklagerðir. Veljið eitt af eftirfarandi gildum: **Allar**, **Viðskiptamaður** eða **Lánardrottinn**. |
| Kóði lykils         | Ef þú valdir **Viðskiptamaður** eða **Lánardrottinn** í reitnum **Lykilgerð** er hægt að takmarka frekar notkun svæðisgildis við tilgreindan flokk eða töflu. |
| Númer lykils/flokks | Ef þú valdir **Viðskiptamaður** eða **Lánardrottinn** í reitnum **Lykilgerð** og ef þú færðir inn flokk eða töflu í reitinn **Kóði lykils** er hægt að færa inn tilgreindan flokk eða umboðsaðila í þennan reit. |
| Virkt            | Tilgreina dagsetningu þegar byrja á að taka tillit til gildisins. |
| Lok gildistíma           | Tilgreina dagsetningu þegar hætta á að taka tillit til gildisins. |

Sjálfgefið er að samsetningar af skilyrðum sem eru skilgreindar af svæðunum **Númer lykils/flokks**, **Kóði lykils**, **Virkt** og **Lok gildistíma** hafi ekki áhrif á valið á gildum fyrir önnur svæði. Hins vegar geta þessar samsetningar verið notaðar í keyrsluhæfum klasa til að innleiða tiltekna reiknireglu sem reiknar út gildi fyrir önnur svæði.

## <a name="executable-class-settings"></a><a id="executable"></a>Keyranlegar klasastillingar

Keyranlegur klasi er X++ aðferð eða klasi sem úrvinnsla rafrænna skilaboða getur kallað á í tengslum við aðgerð ef þörf er á einhverju mati á ferlinu.

Hægt er að setja handvirkt upp keyranlegan klasa sem þarf að kalla á við úrvinnslu með því að fara á síðuna **Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Keyranlegar klasastillingar**. Á síðunni **Keyranlegar klasastillingar** skal stofna línu og stilla eftirfarandi svæði.

| Svæði                 | lýsing |
|-----------------------|-------------|
| Keyranlegur klasi      | Sláið inn heiti sem verður notað við uppsetningu á úrvinnsluaðgerð skilaboða sem klasinn þessu tengdur er kallaður. |
| lýsing           | Færið inn lýsingu á keyranlegum klasa. |
| Keyranlegt klasaheiti | Veljið X++ keyranlegan klasa. |
| Framkvæmdastig       | Þetta svæði er stillt sjálfkrafa vegna þess að gildið er forskilgreint fyrir valdan keyranlegan klasa. Þetta svæði takmarkar stigið sem tengt mat er keyrt á. |
| Lýsing klasa     | Þetta svæði er stillt sjálfkrafa vegna þess að gildið er forskilgreint fyrir valdan keyranlegan klasa. |
| Gerð aðgerðar           | Þetta svæði er tiltækt þegar kveikt er á eiginleikanum **\[Rafræn skilaboð\] Gerð keyranlegrar klasaaðgerðar** á vinnusvæðinu **Eiginleikastjórnun**. Notaðu þetta svæði til að tilgreina gerð aðgerðar fyrir keyranlega klasann. Þessi reitur gefur nákvæmari stjórn á næstu aðgerðum sem eru tiltækar fyrir rafrænu skilaboðin á síðunni **Rafræn skilaboð**. |

Sumir keyrsluhæfir klasar kunna að hafa áskildar færibreytur sem verður að skilgreina áður en keyrsluhæfur klasi er keyrður í fyrsta skipti. Til að skilgreina þessar færibreytur skal á aðgerðasvæðinu velja **Færibreytur**. Í svarglugganum sem birtist skal stilla reitina og síðan velja **Í lagi**. Mikilvægt er að velja **Í lagi**. Annars vistast færibreyturnar ekki í gagnagrunninum og ekki verður kallað rétt á keyrsluhæfa klasann.

## <a name="populate-records-actions"></a><a id="populate"></a>Fylla út færsluaðgerðir

„Fylla út færsluaðgerðir“ er notuð til að setja upp aðgerðir sem bæta færslum við töflu skilaboðaatriða svo hægt sé að bæta þeim við rafræn skilaboð. Ef rafrænu skilaboðin verða til dæmis að gefa skýrslu um reikninga viðskiptamanns er nauðsynlegt að setja upp aðgerð til að fylla út færslur sem tengist reitnum **Gagnaveita** í töflunni Reikningabók viðskiptavinar.

Hægt er að setja upp „fylla út færsluaðgerðir“ með því að fara í **Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Fylla út færsluaðgerðir**. Stofnið nýja færslu fyrir hverja aðgerð sem á að bæta færslum við töflu, og stillið eftirfarandi svæði.

| Svæði       | Lýsing |
|-------------|-------------|
| Nafn        | Færið inn heiti á aðgerð sem fyllir út færslur í vinnslunni. |
| Lýsing | Færið inn lýsingu á aðgerð sem fyllir út færslur. |

Á flýtiflipanum **Uppsetning gagnagjafa** skal bæta við línu fyrir hvern gagnagjafa sem er notaður í vinnslunni, og stilla skal eftirfarandi svæði.

| Svæði                  | lýsing |
|------------------------|-------------|
| Nafn                   | Færið inn heiti á gagnaveitu. |
| Gerð skilaboðaatriðis      | Veljið gerð skilaboðaatriðis sem á að nota þegar færslur eru búnar til fyrir gagnaveituna. |
| Lykilgerð           | Veljið lykilgerð sem á að tengjast færslum úr gagnaveitunni. |
| Aðaltöfluheiti      | Veldu töfluna sem á að vera gagnaveita. |
| Reitur skjalnúmers  | Veldu reitinn í valdri aðaltöflu þar sem taka á skjalanúmerið úr. Gildi þessa reits er notað sem gildið í reitnum **Skjalanúmer** fyrir skilaboðaatriðið. |
| Dagsetningarreitur skjals    | Veldu reitinn í valdri aðaltöflu þar sem taka á skjaladagsetninguna úr. Gildi þessa reits er notað sem gildið í reitnum **Dagsetning skilaboðaatriðis** fyrir skilaboðaatriðið. |
| Reikningsreitur skjals | Veldu reitinn í valdri aðaltöflu þar sem taka á skjalareikninginn úr. Gildi þessa reits er notað sem gildið í reitnum **Reikningsnúmer** fyrir skilaboðaatriðið. |
| Fyrirt.                  | Þessi reitur er í boði þegar kveikt er á eiginleikanum **Fyrirspurnir milli fyrirtækja fyrir aðgerð færslufyllingar** á vinnusvæðinu **Eiginleikastjórnun**. Notaðu þennan eiginleika til að setja upp gagnagjafa milli fyrirtækja fyrir aðgerðir færslufyllingar. Hægt er að sækja gögn frá mörgum fyrirtækjum. |
| Fyrirspurn notanda             | <p>Ef sett er upp fyrirspurn með því að velja **Breyta fyrirspurn** fyrir ofan hnitanetið og tilgreint er skilyrðið sem þarf að nota í valda aðaltöflu sem útfyllt gögn koma úr, verður þessi gátreitur sjálfkrafa valinn. Annars eru allar færslurnar fylltar út frá völdum upppruna aðaltöflu.</p><p>Þegar kveikt er á eiginleikanum **Fyrirspurnir milli fyrirtækja fyrir aðgerðir færslufyllingar** á vinnusvæðinu **Eiginleikastjórnun** og safna þarf færslum frá ýmsum fyrirtækjum, skal bæta við línu fyrir hvernig viðbótar lögaðila sem á að vera með í skýrslugjöfinni. Fyrir hverja nýja línu skal velja **Breyta fyrirspurn** og tilgreina tengt skilyrði sem á við um lögaðilann sem er tilgreindur í reitnum **Fyrirtæki** í línunni. Þegar því er lokið mun hnitanetið **Uppsetning gagnagjafa** innihalda línur fyrir alla lögaðilana sem þarf að hafa með í skýrslugerðinni.</p> |

## <a name="populate-records-from-multiple-companies"></a><a id="multiple-companies-populate"></a> Fylltu út skrár frá mörgum fyrirtækjum

Ef fyrirtæki þitt verður að tilkynna frá mörgum lögaðilum í sama fjármálagagnagrunni skaltu setja upp [fylla færslur aðgerðir](#populate) fyrir alla þá lögaðila sem gögn skulu koma frá í skýrslugerð.

Til að virkja þessa möguleika í fjármálaumhverfi þínu skaltu fylgja þessum skrefum. 

1. Fara til **Vinnurými** \> **Eiginleikastjórnun**.
2. Finndu og veldu **Fyrirspurnir þvert á fyrirtæki fyrir aðgerðir til að fylla út færslur** eiginleiki á listanum.
3. Veldu **Virkja núna**. 

Til að setja upp [fylla færslur aðgerðir](#populate) fyrir mörg fyrirtæki sem gögn verða að vera með í skýrslugerð, fylgdu þessum skrefum.

1. Fara til **Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Fylltu færslur aðgerðir**.

    Þegar **Fyrirspurnir þvert á fyrirtæki fyrir aðgerðir til að fylla út færslur** eiginleiki er virkur, the **Uppsetning gagnaheimilda** rist á **Fylltu færslur aðgerð** síða inniheldur a **Fyrirtæki** sviði. Fyrir núverandi færslur sem voru búnar til við almenna uppsetningu á [fylla færslur aðgerðir](#populate), þessi reitur sýnir auðkenni núverandi lögaðila.

2. Í **Uppsetning gagnaheimilda** grid, bæta við línu fyrir hvern dótturlögaðila sem þarf að vera með í skýrslugerð og stilla eftirfarandi reiti.

    | Heiti svæðis             | Gildi |
    |------------------------|-------|
    | Nafn                   | Sláðu inn textagildi sem hjálpar þér að skilja hvaðan þessi skrá kemur. Til dæmis, slá inn **Nafn gagnagjafa - Dótturfélag 1**. |
    | Gerð skilaboðaatriðis      | Veldu tegund skilaboðahluta sem þarf fyrir EM vinnslu þína. |
    | Lykilgerð           | Tilgreindu reikningsgerðina sem þarf fyrir EM vinnslu þína. Ef EM vinnslan þín hefur engar sérstakar reikningsgerðir skaltu velja **Allt**. |
    | Aðaltöfluheiti      | Tilgreindu nafn aðaltöflunnar sem þarf fyrir EM vinnslu þína. |
    | Reitur skjalnúmers  | Tilgreindu reitinn sem inniheldur skjalnúmerið í skrám yfir EM vinnslu þína. |
    | Dagsetningarreitur skjals    | Tilgreindu reitinn sem inniheldur skjaldagsetninguna í skrám yfir EM vinnslu þína. |
    | Reikningsreitur skjals | Tilgreindu reitinn sem inniheldur skjalareikninginn í skrám yfir EM vinnslu þína. |
    | Fyrirtæki                | Veldu auðkenni dótturfélags lögaðila. |
    | Fyrirspurn notanda             | Þessi gátreitur er sjálfkrafa valinn þegar þú skilgreinir viðmið með því að velja **Breyta fyrirspurn**. |

3. Veldu fyrir hverja nýja línu **Breyta fyrirspurn**, og tilgreindu tengd viðmið fyrir lögaðilann sem er tilgreindur í **Fyrirtæki** sviði á línunni.

## <a name="web-applications"></a><a id="applications"></a>Vefforrit

Notaðu stillingar fyrir vefforrit til að setja upp vefforrit þannig að það styður Open Authorization (OAuth) 2.0. OAuth er opinn staðall sem gerir notendum kleift að veita „öruggan úthlutaðan aðgang“ að forritinu fyrir þeirra hönd, án þess að deila aðgangsupplýsingum þeirra. Einnig er hægt að fara í gegnum heimildarferlið með því að fá heimildarkóða og aðgangslykil. Hægt er að setja upp stillingar vefforrits með því að fara í **Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Vefforrit**.

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
| Aðgangsmerki rennur út eftir  | Eftirstandandi tími áður en aðgangslykillinn rennur út. Þessi reitur er uppfærður sjálfkrafa. | 
| Samþykkja                       | Tilgreinið eiginleikann **Samþykkja** fyrir vefbeiðnina. Færið til dæmis inn **application/vnd.hmrc.1.0+json**. |
| Gerð innihalds                 | Tilgreina gerð innihalds. Færið til dæmis inn **application/json**. |

Að auki eru eftirfarandi hnappar í boði á aðgerðasvæði síðunnar **Vefforrit** til að styðja heimildarferlið:

- **Fá heimildarkóða** - Frumstilla heimild vefforritsins. Þessi virkni notar snið rafrænnar skýrslugerðar sem er tilgreint í reitnum **Sniðsvörpun heimildar** til að búa til heimildarbeiðni.
- **Fá aðgangslykil** - Frumstilla ferlið til að fá aðgangslykil.
- **Endurnýja aðgangslykil** - Endurnýja aðgangslykil. Þessi virkni notar snið rafrænnar skýrslugerðar sem er tilgreint í reitnum **Flytja inn líkanavörpun lykils** til að flytja inn upplýsingar um móttekinn aðgangslykil.

Þegar aðgangslykill að vefforriti er vistaður í gagnagrunni kerfisins á dulrituðu sniði, er hægt að nota hann fyrir beiðnir að vefþjónustu. Í öryggisskyni skal aðgangur að aðgangslykli takmarkast við þau öryggishlutverk sem mega taka á þessum beiðnum. Ef einhver utan öryggisflokksins reynir að taka á beiðni fær hann villu sem gefur til kynna að hann sé ekki með leyfi til að vinna með valið vefforrit. Til að setja upp öryggishlutverk sem hafa aðgang að aðgangslykli skal nota flýtiflipann **Öryggishlutverk** á síðunni **Vefforrit**. Ef öryggishlutverk eru ekki skilgreind fyrir vefforrit getur aðeins kerfisstjórinn unnið í gegnum þetta vefforrit.

Fyrir hverja aðgerð með völdu vefforriti vistar flýtiflipinn **Aðgerðarkladdi** upplýsingar um notandann ásamt dagsetningu og tíma.

Sumar vefþjónustur gætu krafist þess að mismunandi hausar séu með í beiðnunum. Kerfisstjóri getur sett upp aukalega hausa og gildi þeirra í flýtiflipann **Fleiri hausar** og síðan notað þá við myndun beiðni.

## <a name="web-service-settings"></a><a id="settings"></a>Stillingar vefþjónustu

Notaðu stillingar vefþjónustu til að setja upp beinan gagnaflutning til vefþjónustu. Hægt er að setja upp stillingar vefþjónustu með því að fara í **Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Stillingar vefþjónustu**.

Eftirfarandi tafla lýsir svæðunum á síðunni **Stillingar vefþjónustu**.

| Svæði                          | lýsing |
|--------------------------------|-------------|
| Vefþjónusta                    | Færið inn heiti á vefþjónustunni. |
| lýsing                    | Færið inn lýsingu á vefþjónustunni. |
| Internet-fang               | <p>Færið inn veffangið á vefþjónustunni. Ef vefforrit er tilgreint fyrir vefþjónustuna, og ef veffang vefþjónustunnar er það sama og veffangið sem er skilgreint fyrir þetta vefforrit, skal velja **Afrita grunnvefslóð**. Grunnslóð vefforritsins er síðan afrituð í þennan reit.</p><p>**Viðvörun:** Þjónusta þriðja aðila eða önnur þjónusta sem þú stillir hér þarf ekki endilega að vera vottuð og hugsanlegt er að hún uppfylli ekki persónuverndarstaðla Microsoft. Þú ættir að fara yfir persónuverndarstefnu hverrar þjónustu og vinna með hverjum þjónustuaðila til að kanna enn frekar hvers konar reglufylgni þessi þjónusta býður upp á. Þú berð ábyrgð á því að þessi þjónusta samræmist öryggis-, persónuverndar- og lagalegum stöðlum þínum. Þú berð áhættuna á því að nota þjónustuna. Microsoft veitir engar sérstakar ábyrgðir, ábyrgðir eða skilyrði. Eindregið er mælt með því að þú notir aðeins þjónustu sem veitir öruggar og viðurkenndar tengingar, t.d. HTTPS.</p> |
| Vottorð                    | Veljið vottorð Azure-lyklageymslu sem hefur verið sett upp áður. |
| Vefhugbúnaður                | Veljið vefforrit sem hefur verið sett upp áður. |
| Gerð svars – XML        | Stillið þennan valkost á **Já** ef gerð svars er XML. |
| Aðferð beiðni                 | Tilgreinið aðferð beiðninnar. HTTP skilgreinir safn af beiðnum sem gefa til kynna aðgerðina sem á að framkvæma fyrir tiltekin tilföng. Aðferð beiðninnar getur verið **GET**, **POST** eða önnur HTTP-aðferð. |
| Haus beiðni                | Tilgreina haus beiðni. Haus beiðni er HTTP-haus sem hægt er að nota í HTTP-beiðni. Hún tengist ekki innihaldi skilaboðanna. |
| Samþykkja                         | Tilgreinið samþykktareiginleika vefbeiðnarinnar. |
| Samþykkja kóðun                | Tilgreindu gildi kóðasamþykktar. HTTP beiðnishaus fyrir samþykki kóðunar gefur kóðun innihalds til kynna sem biðlarinn getur skilið. Þessi kóðun innihalds er venjulega þjappað reiknirit. |
| Gerð innihalds                   | Tilgreina gerð innihalds. HTTP-haus fyrir einingu innhaldsgerðar gefur til kynna miðilsgerð tilfanga. |
| Svarkóði tókst       | Tilgreindu HTTP-stöðukóðann sem gefur til kynna að beiðnin hafi heppnast. |
| Sniðsvörpun síðuhausa fyrir beiðnir | Veldu snið rafrænnar skýrslugerðar sem er notað til að búa til hausa fyrir vefbeiðnir. |

## <a name="message-processing-actions"></a><a id="actions"></a>Úrvinnsluaðgerðir skilaboða

Úrvinnsluaðgerðir skilaboða eru notaðar til að stofna aðgerðir fyrir vinnslurnar og til að setja upp færibreytur þeirra. Hægt er að setja upp aðgerðir skilaboðaúrvinnslu með því að fara í **Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Úrvinnsluaðgerðir skilaboða**.

Eftirfarandi töflur lýsa svæðunum á síðunni **Úrvinnsluaðgerðir skilaboða**.

### <a name="general-fasttab"></a>Flýtiflipinn Almennt

| Svæði                                     | lýsing |
|-------------------------------------------|-------------|
| Gerð aðgerðar                               | Veljið þessa gerð aðgerðar. Fyrir upplýsingar um tiltæka valkosti, sjá [Gerðir aðgerða fyrir skilaboðavinnslu](#action-types) kafla síðar í þessari grein. |
| Sniðsvörpun                            | Veljið snið rafrænnar skýrslugerðar sem á að kalla á fyrir aðgerðina. Þetta svæði er aðeins í boði fyrir aðgerðir af gerðunum **Útflutningur á rafrænum skýrslum**, **Innflutningur á rafrænum skýrslum** og **Útflutningsskilaboð rafrænna skýrslna**. |
| Sniðsvörpun fyrir vefslóð               | Veljið snið rafrænnar skýrslugerðar sem á að kalla á fyrir aðgerðina. Þetta snið er notað til að búa til slóð vefslóðarinnar sem verður bætt við grunnveffangið sem er tilgreint fyrir valinn vefþjón. Þetta svæði er aðeins í boði fyrir aðgerðir af gerðinni **Vefþjónusta**. |
| Gerð skilaboðaatriðis                         | Veljið færslugerðir sem meta á aðgerðina fyrir. Þetta svæði er aðeins í boði fyrir aðgerðir af gerðunum **Framkvæmdastig skilaboðaatriða**, **Útflutningur á rafrænum skýrslum**, **Innflutningur á rafrænum skýrslum** og **Vefþjónusta** og fyrir aðrar gerðir. Ef þetta svæði er skilið eftir autt verða allar gerðir skilaboðaatriða metnar sem eru skilgreindar fyrir úrvinnslu skilaboða. |
| Keyranlegur klasi                          | Velja skal stillingu á keyranlegum klasa sem er til staðar. Þetta svæði er aðeins í boði fyrir aðgerðir af gerðunum **Framkvæmdastig skilaboðaatriða** og **Framkvæmdastig skilaboðaatriða**. |
| Fylla út færsluaðgerð                   | Velja skal aðgerð færsluútfyllingar sem er til staðar. Þetta svæði er aðeins í boði fyrir aðgerðir af gerðinni **Fylla út færslur**. |
| Vefþjónusta                               | Velja skal vefþjónustu sem er til staðar. Þetta svæði er aðeins í boði fyrir aðgerðir af gerðinni **Vefþjónusta**. |
| Skráarheiti sem á að senda                         | Sláðu inn nafn viðhengis við rafræn skilaboð sem verða að senda með þessari aðgerð. Ef mörg viðhengi hafa sama upprunalega skráarnafnið verður það nýjasta sent. Ef ekkert viðhengi finnst sem hefur tilgreint upprunalega skráarnafn verður beiðnin send án innihalds. Þetta svæði er aðeins í boði fyrir aðgerðir af gerðinni **Vefþjónusta**. |
| Skrárnafn                                 | Tilgreinið heiti skráar sem verður niðurstaða aðgerðarinnar. Þessi skrá getur verið svarið frá vefþjóninum eða skýrslunni sem myndast. Þetta svæði er aðeins í boði fyrir aðgerðir af gerðunum **Vefþjónusta** og **Útflutningsskilaboð rafrænna skýrslna**. |
| Hengja skrár við upprunaskjöl          | Velja skal þennan gátreit til að hengja myndaðar skrár við færslur í aðaltöflunni sem vísað er til fyrir atriði rafrænna skilaboða. Þetta svæði er aðeins í boði fyrir aðgerðir af gerðinni **Útflutningur rafrænnar skýrslugerðar** og **Vefþjónusta**. |
| Hengja skrár úr frálagssöfnum við atriði | Veldu þennan gátreit til að draga út aðskildar XML-skrár úr frálagssafnskrá og hengja þær við viðeigandi rafræn skilaboðaatriði. Þetta svæði er aðeins í boði fyrir aðgerðir af gerðinni **Útflutningur rafrænnar skýrslugerðar**. |
| Fjöldi skilaboðaatriða í hverjum útflutningi        | Tilgreindu hámark á fjölda skilaboðaatriða sem verður að vera með í einni skrá (skilaboðum). Þetta svæði er aðeins í boði fyrir aðgerðir af gerðinni **Útflutningur rafrænnar skýrslugerðar**. |
| Nota uppruna rafrænnar skýrslugerðar                             | Veldu þennan gátreit til að nota færibreytur fyrir uppruna rafrænnar skýrslugerðar fyrir innflutning. Annars er viðhengið úr rafrænu skilaboðunum notað. Þetta svæði er aðeins í boði fyrir aðgerðir af gerðinni **Innflutningur rafrænnar skýrslugerðar**. |
| Sýna svarglugga                               | Stilltu þennan valkost á **Já** ef sýna þarf notendum svarglugga áður en skýrsla er gerð. Þetta svæði er aðeins í boði fyrir aðgerðir af gerðinni **Útflutningsskilaboð rafrænna skýrslna**. |

#### <a name="message-processing-action-types"></a><a id="action-types"></a>Gerðir úrvinnsluaðgerðar skilaboða

Eftirfarandi valkostir eru í boði í svæðinu **Gerð aðgerðar**:

- **Stofna skilaboð** – Notið þessa gerð aðgerðar til að leyfa notendum að stofna skilaboð handvirkt á síðunni **Rafræn skilaboð**. Ekki er hægt að setja upp upphafsstöðu fyrir aðgerð af þessari gerð.
- **Fylla út færslur** – Þessi gerð aðgerðar verður að vera sett upp. Tengdu þetta við aðgerð sem fyllir út færslur svo sú aðgerð verði með í vinnslunni. Gert er ráð fyrir að þessi gerð aðgerðar sé notuð fyrir fyrstu aðgerðina í úrvinnslu skilaboða (þegar engin rafræn skilaboð eru búin til fyrirfram) eða fyrir aðgerð sem bætir skilaboðaatriðum við eldri skilaboð með aðgerð af gerðinni **Búa til skilaboð**. Fyrir aðgerðir af þessari gerð er þar af leiðandi aðeins hægt að setja upp lokastöðu fyrir skilaboðaatriði. Eingöngu er hægt að setja upp upphafsstöðu fyrir skilaboð.
- **Framkvæmdastig skilaboða** – Notið þessa gerð aðgerðar til að setja upp keyranlegan klasa sem á að vera metinn á skilaboðastigi.
- **Framkvæmdastig skilaboðaatriða** – Notið þessa gerð aðgerðar til að setja upp keyranlegan klasa sem á að vera metinn á stigi skilaboðaatriða.
- **Útflutningur á rafrænum skýrslum** – Notið þessa gerð aðgerðar fyrir aðgerðir sem eiga að búa til skýrslu sem miðast við skilgreiningu á útflutningi á rafrænum skýrslum á stigi skilaboðaatriða.
- **Útflutningsskilaboð rafrænna skýrslna** – Notið þessa gerð aðgerðar fyrir aðgerðir sem eiga að búa til skýrslu sem miðast við skilgreiningu á útflutningi á rafrænum skýrslum á skilaboðastigi (til dæmis þegar skilaboð eru ekki með nein skilaboðaatriði).
- **Innflutningur á rafrænum skýrslum** – Notið þessa gerð aðgerðar fyrir aðgerðir sem eiga að búa til skýrslu sem miðast við skilgreiningu á innflutningi á rafrænum skýrslum.
- **Úrvinnsla notanda á skilaboðastigi** – Notið þessa gerð aðgerðar fyrir aðgerðir sem gera ráð fyrir nokkrum handvirkum aðgerðum notanda á skilaboðastigi. Til dæmis gæti notandi uppfært stöðu skilaboða.
- **Úrvinnsla notanda** – Notið þessa gerð aðgerðar fyrir aðgerðir sem gerir ráð fyrir nokkrum handvirkum aðgerðum notanda á stigi skilaboðaatriðis. Til dæmis gæti notandi uppfært stöðu skilaboðaatriða.
- **Vefþjónusta** – Notið þessa gerð aðgerðar fyrir aðgerðir sem eiga að senda myndaða skýrslu til vefþjónustu. Þessi gerð aðgerðar er ekki notuð fyrir skýrslugerð ítalskra innkaupa- og sölureikningasamskipta. Fyrir þessa gerð aðgerðar inniheldur síðan **Úrvinnsluaðgerðir skilaboða** flýtiflipann **Ýmsar upplýsingar** þar sem hægt er að tilgreina staðfestingartexta. Þessi staðfestingartexti er sýndur notendum áður en tekið er á beiðnum valinnar vefþjónustu.
- **Beiðni um sannprófun** – Notið þessa gerð aðgerðar til að óska eftir sannprófun frá þjóni.

### <a name="initial-statuses-fasttab"></a>Flýtiflipi fyrir upphafsstöður

> [!NOTE]
> Flýtiflipinn **Upphafsstöður** er ekki í boði fyrir aðgerðir sem eru með upphafsgerð aðgerðar **Stofna skilaboð**.

| Svæði               | Lýsing |
|---------------------|-------------|
| Staða skilaboðaatriðis | Veljið stöðu skilaboðaatriðis sem á að meta valda úrvinnsluaðgerð skilaboða fyrir. |
| lýsing         | Lýsing á stöðu valins skilaboðaatriðis. |

### <a name="result-statuses-fasttab"></a>Flýtiflipi fyrir lokastöður

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

## <a name="electronic-message-processing"></a><a id="processing"></a>Rafræn skilaboð í vinnslu

Úrvinnsla á rafrænum skilaboðum er grundvallaratriði í virkni rafrænna skilaboða. Vinnslan safnar saman aðgerðum sem á að meta fyrir rafrænu skilaboðin. Hægt er að tengja aðgerðirnar með því að nota upphafsstöðu og lokastöðu. Annars er hægt að hefja hverja aðgerð fyrir sig af gerðinni **Úrvinnsla notanda**. Til að setja upp úrvinnslu á rafrænum skilaboðum skal opna **Skattur** \> **Uppsetning** \> **Rafræn skilaboð** \> **Úrvinnsla rafrænna skilaboða**.

Flýtiflipinn **Aðgerðir** gerir þér kleift að bæta forskilgreindum aðgerðum við úrvinnsluna. Hægt er að tilgreina hvort keyra verði aðgerð sérstaklega eða hvort vinnslan geti byrjað hana. Til að tilgreina að aðgerð í úrvinnslunni geti eingöngu verið frumstillt af notanda skal stilla reitinn **Keyra sérstaklega** á **Já** fyrir þessa aðgerð. Ef hefja á aðgerð með úrvinnslu á skilaboðum eða skilaboðaatriðum sem eru í stöðunni sem er skilgreind sem upphafsstaða fyrir aðgerðina skal stilla reitinn **Keyra sérstaklega** á **Nei**. Aðgerð af gerðinni **Aðgerð notanda** verður alltaf að keyra sérstaklega.

Stundum þarf að sameina nokkrar aðgerðir í röð, jafnvel þó að fyrsta aðgerðin sé sett upp svo hún keyri sérstaklega. Til dæmis verður notandi að frumstilla skýrslugerð. En strax og skýrslan er búin til verður að senda hana á vefþjónustu og svarið frá vefþjónustunni verður að endurspeglast í kerfinu. Í slíku tilfelli er hægt að búa til óaðskiljanlega röð fyrir aðgerðirnar sem verður alltaf að keyra saman. Í flýtiflipanum **Aðgerð** skal velja **Óaðskiljanlegar raðir** fyrir ofan hnitanetið og stofna röð. Svo skal fyrir allar aðgerðir sem þurfa að keyra saman í einni röð velja röðina í reitnum **Óaðskiljanleg röð**. Í þessum dæmi er hægt að stilla reitinn **Keyra sérstaklega** á **Já** fyrir fyrstu aðgerðina í röðinni en **Nei** fyrir allar aðrar aðgerðir.

Aðgerðir af gerðunum **Útflutningur rafrænnar skýrslugerðar** og **Útflutningsskilaboð rafrænnar skýrslugerðar** keyra snið rafrænnar skýrslugerðar sem er með innsláttarfæribreytum. Ef úrvinnsla rafrænna skilaboða felur í sér aðgerðir af annaðhvorri gerðinni verður að tilgreina gildi fyrir innsláttarbreytur áður en skýrsla er búin til. Á þennan hátt getur kerfið notað runufyrirkomulag til að búa til skýrsluna. Þú getur valið **Færibreytur** fyrir ofan hnitanetið til að setja upp færibreyturnar fyrir valda gerð aðgerðar (**Útflutningur rafrænnar skýrslugerðar** eða **Útflutningsskilaboð rafrænnar skýrslugerðar**). Veldu gátreitinn **Nota færibreytur** fyrir aðgerðina sem þarf að keyra með tilgreindum færibreytum í runufyrirkomulagi.

Notaðu flýtiflipann **Önnur svæði skilaboðaatriða** til að bæta við öðrum forskilgreindum svæðum sem tengjast skilaboðaatriðum. Bæta verður við öðrum svæðum fyrir hverja gerð skilaboðaatriða sem svæðin tengjast. Þú getur skilgreint sjálfgefið gildi sem verður úthlutað á viðbótarreitinn meðan á vinnslu stendur.

Notaðu flýtiflipann **Önnur svæði skilaboða** til að bæta við öðrum forskilgreindum svæðum sem tengjast skilaboðum. Þú getur skilgreint sjálfgefið gildi sem verður úthlutað á viðbótarreitinn meðan á vinnslu stendur.

Notaðu flýtiflipann **Öryggishlutverk** til að setja upp öryggishlutverk sem eru forskilgreind í kerfinu fyrir tilteknar vinnslur. Notendur með tiltekið hlutverk sjá aðeins vinnsluna sem er skilgreind fyrir það hlutverk.

Notaðu flýtiflipann **Runa** til að setja upp vinnslu til að vinna í runufyrirkomulagi. Mælt er með að setja upp runufyrirkomulag fyrir úrvinnsluna beint á síðunni **Rafræn skilaboð** eða **Rafræn skilaboðaatriði** þegar þú velur **Keyra vinnslu** á aðgerðasvæðinu til að hefja úrvinnsluna.
