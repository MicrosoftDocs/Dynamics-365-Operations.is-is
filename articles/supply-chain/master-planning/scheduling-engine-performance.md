---
title: Bæta frammistöðu röðunarvélar
description: Í þessu efnisatriði er að finna upplýsingar um röðunarvélina og hvernig á að bæta afköst.
author: ChristianRytt
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: ''
ms.author: crytt
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2495339f25469af705cff841f090c5df95b4d996
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578441"
---
# <a name="improve-scheduling-engine-performance"></a>Bæta frammistöðu röðunarvélar

[!include [banner](../includes/banner.md)]

Röðunarvél tilfanga er notuð þegar leiðir eru tímasettar fyrir áætlaðar og útgefnar framleiðslupantanir. Vélin var upphaflega gefin út sem hluti af Dynamics AX 2012 og hefur farið í gegnum nokkrar úrbætur frá útgáfu hennar.

[Vandamál við tímasetningu verka](https://en.wikipedia.org/wiki/Job_shop_scheduling) er gríðarlega flókið vandamál samsetningar þar sem úrlausnartíminn tekur veldisvöxt með fjölda ákvörðunarbreyta. Oft og tíðum setja viðskiptavinir upp framleiðsluleiðir og tengd gögn þannig að úr verði vandamál við tímasetningu sem ekki er hægt að leysa innan viðunandi tíma, jafnvel fyrir nýjasta vélbúnaðinn. Þetta efnisatriði varpar betra ljósi á röðunarvélina og hvernig tiltekin uppsetning getur haft áhrif á afköstin.

Þegar kemur að því að bæta afköst áætlunargerðar mæla almennar viðmiðunarreglur með því að draga úr margbreytileika vandans sem vélin þarf að leysa. Sumir helstu þættir sem geta haft áhrif á afköst eru:

- Leiðir með mörgum aðgerðum
- Leiðir með hliðstæðum aðgerðum
- Aðgerðir með magn af tilföngum sem eru hærri en eitt
- Aðgerðir með mörgum tilföngum sem eiga við
- Notkun harðra tengla
- Notkun takmarkaðrar getu
- Fjöldi mismunandi dagatala sem er notaður
- Fjöldi vinnutímahólfa á dag í dagatalinu
- Samtals tímalengd leiðarinnar
- Margar röðunarvélar keyrðar samhliða

## <a name="overview-of-basic-scheduling-flow"></a>Yfirlit yfir grunnröðun flæðis

Til að skilja hvernig tiltekin uppsetning getur haft áhrif á afköst, er mikilvægt að skilja flæði verkferla, bæði innan vélarinnar og í X++ kóðanum sem fylgir henni.

Grunnferlið við að tímasetja pöntun felur í sér þrjú meginskref:

- **Hleðslugögn** - Hér er X++ gagnalíkönum breytt í innra gagnalíkan vélarinnar í formi verka og takmarkanna.
- **Röðun** – Þetta er aðaluppruni fyrir röðunina sem vinnur úr gefnu líkani og takmörkunum og kemur með niðurstöður. Meðan á þessu ferli stendur, biður vélin um upplýsingar um vinnutíma og fyrirliggjandi frátekna afkastagetu frá X++ eftir því sem þörf krefur.
- **Vista gögn** – Niðurstöður vélar á formi hólfa fyrir frátekna afkastagetu vinnu er unnið úr af X++ kóða til að vista frátekna afkastagetu og uppfæra upphafs- og lokatíma verka/aðgerðar/pöntunar.

## <a name="load-data-into-the-engine"></a>Hlaða gögnum inn í vélina

Röðunarvélin er með óhlutbundnara gagnalíkan en gagnagrunnur Supply Chain Management vegna þess að hún hefur verið smíðuð sem almenn vél sem getur meðhöndlað mismunandi uppruna gagna. Hugmyndir um leiðir, aukaaðgerðir og keyrslutíma þurfa að vera „þýddar“ yfir á almenna verkið og takmörkunarlíkanið sem vélin birtir. Rökin fyrir því að byggja líkanið eru með talsvert magn viðskiptagrunns og er mismunandi eftir því hver upprunagögnin eru. Tilheyrandi X++ klasi er `WrkCtrScheduler` og hann er með afleidda klassa fyrir áætlaðar framleiðslupantanir, útgefnar framleiðslupantanir og verkspár.

Sem dæmi skal hafa í huga leið sem birtist í eftirfarandi töflu og mynd, sem virðist tiltölulega einföld.

| Aðg.nr. Nei. | Forgangur | Uppsetningartími | Keyrslutími | Biðtími eftir | Fjöldi tilfanga | Næst |
| --- | --- | --- | --- | --- | --- | --- |
| 10 | Aðal | 1.00 | 2.00 | | 1 | 20 |
| 10 | Auka&nbsp;1 | | | | 1 | 20 |
| 20 | Aðal | | 3.00 | 1.00 | 3 | 0 |

![Dæmi um skýringarmynd leiðar.](media/scheduling-engine-route.png "Skýringarmynd með dæmi um leið")

Þegar þetta er sent til vélarinnar, er því skipt niður á átta vinnslur eins og sýnt er í eftirfarandi skýringarmynd (veljið myndina til að stækka hana).

[![Verk röðunarvélar](media/scheduling-engine-jobs.png "Verk röðunarvélar.")](media/scheduling-engine-jobs-large.png)

Staðlaður tengill á milli tveggja vinnsla er `FinishStart`, sem þýðir að lokatími einnar vinnu verður að vera á undan upphafstíma annarrar vinnu. Vegna þess að uppsetningin verður að vera framkvæmd af sama tilfangi sem síðar gerir ferlið, eru `OnSameResource` takmarkanir á milli þeirra. Milli vinnsla fyrir fyrstu og aðra aðgerð fyrir 10, eru `StartStart` og `FinishFinish` tenglar, sem þýðir að vinnslurnar verða að báðar að hefjast og enda á sama tíma og það eru `NotOnSameResource` takmarkanir, sem kemur í veg fyrir sama tilfangið fyrir fyrsta og annað.

Fyrir aðgerð 20, þar sem magn tilfanga hefur verið stillt á 3, hefur vinnsluferlinu verið skipt í þrjú aðskilin verk þar sem öll verkin verða að vera keyrð á nákvæmlega sama tíma.
Í þessu tilfelli hefur leiðaflokkurinn verið settur upp til að taka ekki frá afkastagetu fyrir biðröð eftir tíma, sem er ástæðan fyrir því að aðeins eitt verk fyrir biðröðina eftir á.

Röðunarvélin skilur aðeins hugtök vinnslu en skilur ekki aðgerðir. Þetta þýðir að þegar aðgerðaáætlun er gerð er aðgerðunum einnig skipt í vinnslur, þótt þær verði ekki viðvarandi í gagnagrunninum.

Fyrir hverja vinnslu munum við einnig skilgreina hver afkastaþörf vinnslunnar er (sekúndufjöldinn sem þarf til). Eftir því hvernig tilfangaþarfir hafa verið skilgreindar, er einnig hugsanlegt, fyrir hvert verk, að senda lista yfir öll hugsanleg viðeigandi tilföng sem vinnslan gæti keyrt á og hver afkastaþörfin er fyrir þetta tiltekna tilfang. Jafnvel þótt listi yfir viðeigandi tilföng sé sendur þegar líkanið er smíðað, þarf vélin enn að tryggja að úthlutun tilfangs sé í raun gild fyrir allan tímann sem vinnslan tekur.

## <a name="scheduling-engine-internals"></a>Innsýn í röðunarvél

### <a name="scheduling-engine-interface"></a>Viðmót röðunarvélar

Til að fá hugmynd um hvernig vélin virkar að innan, er best að líta á virknina sem hún sýnir út á við. Í X++ er aðalviðmótið `WrkCtrSchedulerEngineInterface`. Það er með aðferðirnar sem lýst er í eftirfarandi undirhlutum.

#### <a name="general-engine"></a>Almenn vél

| **Aðferð** | **Málefni** |
| --- | --- |
| `run` | Tímasetur allar hlaðnar vinnslur og skilar villukóðum. |
| `getJobSchedulingSequenceResult` | Fær niðurstöður röðunar og fyrstu vinnsluvilluna fyrir röðina sem tiltekin vinnsla finnur. |
| `validateJobCapacityReservations` | Villuleitar frátekna afkastagetu fyrir allar vinnslur sem vélin geymir. |
| `setReservationsTimeStamp` | Sendir tímastimpil á vélina sem er sett á alla nýja frátekna afkastagetu fyrir tímasettar vinnslur í skyndiminni vélarinnar. |
| `addPropertyToGroupAggregation` | Bætir forskeyti eiginleika við safn eiginleika sem notað er þegar afkastagetu er safna saman. |
| `addResource` | Bætir tilfangi við tilfangahóp röðunarvélar. |
| `addResourceGroup` | Bætir tilfangaflokki við hóp tilfangaflokks röðunarvélar. |
| `addResourceGroupMembership` | Bætir tilfangi sem aðila við tilfangaflokk. |
| `addOptimizationGoal` | Bætir við markmiði áætlunarfínstillingar (tímalengd eða forgangur). |

#### <a name="individual-jobs"></a>Einstakar vinnslur

| **Aðferð** | **Málefni** |
| --- | --- |
| `addJobInfo` | Bætir við upplýsingafærslu vinnslu sem segir vélinni frá vinnslu sem ætti að tímasetja. |
| `addConstraintJobEndsAt` | Bætir við skorðun um að vinnsla eigi að enda á tilteknum degi og tíma. |
| `addConstraintJobStartsAt` | Bætir við skorðun um að vinnsla eigi að hefjast á tilteknum degi og tíma. |
| `addConstraintMaxJobDays` | Skilgreinir takmörkun sem vinnsla getur náð yfir fyrir tiltekinn hámarksfjölda daga. |
| `addConstraintResourceRequirement` | Bætir takmörkunum um að vinnslan verði að vera tímasett fyrir tiltekið tilfang. |
| `addJobBindPriority` | Bætir við forgangi fyrir bindingu vinnslu fyrir (vinnslu, stig takmörkunar) par. Hærra forgangsgildi þýðir að vinnslubreytur verða bundnar fyrr. Vinnslan verður unnin á undan vinnslum með lægri forgang í sömu röðinni. |
| `addJobCapacity` | Bætir við upplýsingum um álag fyrir vinnslu (eins og nauðsynlegan keyrslutíma vinnslu) óháð því hvaða tilföng vinnslan keyrir á. |
| `addJobResourceCapacity` | Bætir tilföngum við safn tilfanga sem hægt er að nota til að framkvæma vinnslu og gefur upp afkastagetuna sem þarf þegar keyrt er á þessu tilfangi. |
| `addJobGoal` | Bætir við upplýsingum um markmið vinnslu fyrir tiltekið takmörkunarstig (fyrsti lokatími eða síðasti upphafstími). |
| `addJobResourcePriority` | Bætir við forgangi sem á að nota þegar vinnsla tímasett á tilfangi. |
| `addJobResourceRuntime` | Tilgreinir vinnslutíma sem er háður tilfangi sem vinnslan verður raðað á. |
| `addJobRuntime` | Tilgreinir vinnslutíma sem er óháður tilfangi sem vinnslan verður raðað á. |
| `scheduleJobOnResourceGroup` | Merkir vinnslu fyrir röðun á stigi tilfangaflokks. |
| `setJobResourcePreemptionAllowed` | Stillir hvort forgangur er leyfðir fyrir vinnslu á tilfangi (ef vélin má tímasetja vinnsluna í afkastahólfum sem ekki eru hlið við hlið). |
| `setRequiredNumberOfResources` | Stillir fjölda tilfanga sem þarf til að áætla vinnslu (aðeins fyrir aðgerðaröðun). |

#### <a name="constraints-between-jobs"></a>Takmarkanir á milli vinnsla

| **Aðferð** | **Málefni** |
| --- | --- |
| `addJobLink` | Bætir við tengli (t.d. ljúka\>hefja) á milli tveggja vinnsla. |
| `addConstraintEndsDelayed` | Skilgreinir takmörkunina um að vinnsla geti ekki endað áður en önnur vinnsla endar ásamt einhverjum töfum. |
| `addConstraintJobListWorkingTimeIntersect` | Bætir við takmörkun um að afkastahólfin sem eru tekin frá fyrir vinnslurnar verði að vera vinnutímum sem skarast fyrir tvö tilföng sem vinnslurnar nota. |
| `addConstraintJobOverlap` | Bæta við takmörkun sem skilgreinir hvernig vinnslum er raðað þegar hægt er að færa uppgefið vörumagn milli tveggja tilfanga á meðan enn er ekki búið að vinna úr fyrsta tilfanginu, þannig að næsta tilfang geti hafið úrvinnslu. |
| `addConstraintNotOnSameResource` | Bætir við takmörkun um að ekki eigi að raða tveimur vinnslum á sama tilfangið. |
| `addConstraintOnSameResource` | Bætir við takmörkun um að tvær vinnslur verði að nota sama tilfangið. |
| `addJobSameReservations` | Bætir við takmörkun um að vinnsla verði á endanum að vera með fráteknar afkastagetur fyrir sömu tímahólfin sem aðalvinnslu. |
| `setPrimaryParallelJob` | Bæta við upplýsingum um það hvaða vinnsla er aðalvinnsla í nokkrum samhliða vinnslum |

### <a name="solver"></a>Leysari

Vélin sjálf er í meginatriðum sérhæfð úrlausn á takmörkunum með sérstilltum leiðsagnarreglum bætt við. Úrlausnin byggir á tveimur meginþáttum: breytum og takmörkunum.

#### <a name="variable"></a>Breyta

Breyta táknar svið mögulegra gilda. Röðunarvél er með tvær gerðir af breytum:

- **DateTime-breyta** - Er með svið allra dagsetninga og tímasetninga og hægt er að takmarka sviðið með því að færa neðri og efri mörkin fyrir tímasetningu breytunnar nær hvort öðru.
- **Tilfangabreyta** - Er með svið tilfanga sem eiga við, og hægt er að takmarka sviðið með því að eyða tilföngum úr listanum.

#### <a name="constraint"></a>Skorða

Skorðun virkar á breytur með því að takmarka svið þeirra, en það fer líka eftir breytum þannig að hún virkjast þegar breytur breytast. Ferlið „útbreiðsla skorðunar“ á við um skorðun sem framkvæmir meginaðgerð sína og tilkynnir hana til aðalreiknireglunnar ef hún tekst.

Breyta er talin bundin þegar ekki er hægt að takmarka hana enn frekar, sem þýðir fyrir DateTime-breytuna að efri og neðri mörk eru þau sömu, og fyrir tilfangabreytuna að hún hafi aðeins eitt tilfang sem á við. Þegar allar breytur eru bundnar finnst lausn.

### <a name="constraint-levels"></a>Skorðunarstig

Þegar áætlunargerð er keyrð sem hluti af þekjuáfanga áætlanagerðar efnisþarfa, verða pantanirnar tímasettar aftur í tímann frá dagsetningu þarfa. Hins vegar, ef ekki er hægt að finna áætlun sem hefst í dag eða síðar og lýkur fyrir dagsetningu þarfa, verður stefna áætlanagerðarinnar breytt í frá og með deginum í dag.

Þessi megin viðskiptaregla er meðhöndluð með því að skipuleggja skorðanir í stig. Ef engin lausn finnst þegar skorðanir eru notaðar á hæsta stigi, þá er öllu skorðunum á því stigi sleppt og neðra stigið er reynt. Í framkvæmd þýðir þetta að fyrir röðun afturábak inniheldur líkanið stig 1 með vinnslumarkmið seinasta upphafstíma og hámarks lokatíma skorðunar (þarfadagsetningin) og stig 0 með vinnslumarkmiðum fyrsta lokatíma og lágmarks upphafstíma skorðunar fyrir daginn í dag.

### <a name="algorithm"></a>Algrím

Helstu skref reiknirits vélarinnar eru:

1. Finna raðir (vinnslukeðjur) sem hægt er að leysa sérstaklega.
1. Reyna að finna fyrstu lausn fyrir röðina á hæsta stigi skorðunar.
    1. Raða vinnslum í röðinni út frá markmiði og forgangi vinnslunnar, þannig að upphafsvinnsla finnist.
    1. Keyrið vinnslurnar í lykkju í eftirfarandi röð:
        1. Finnið allar skorðanir sem þarf að dreifa og keyrið dreifinguna.
        1. Ef allar breytur fyrir vinnsluna hafa verið bundnar, þá hefur lausn fyrir þessa vinnslu fundist.
        1. Ef ekki var hægt að binda eina af breytunum án þess að brjóta skorðurnar, þá skal taka til baka breytubindinguna, reyna annað gildi á sviðinu (fyrir tilfangabreyta) og keyra aftur dreifingu skorðunar.
1. Ef engin lausn fannst eru allar skorður á núverandi skorðunarstigi fjarlægðar, stig skorðunar lækkað (ef einhver lægri stig eru tiltæk) og leit að lausn reynd aftur með nýju skorðunarsafni.
1. Ef hagkvæm lausn fannst, þá hefst áfangi fínstillingar, sem reynir að finna betri lausn þar til tímalokun fínstillingar næst eða þegar allar samsetningar tilfanga hafa verið reyndar.

Úrlausn skorðunar veit ekki af sérstökum þáttum reiknirits röðunarinnar. Það er í skilgreiningu og samsetningu hinna ýmsu skorðana sem „galdurinn“ gerist.

### <a name="determining-working-times"></a>Skilgreina vinnutíma

Stór hluti af (innri) skorðunum í vélinni stjórna vinnutímanum og afkastagetu tilfangs. Í meginatriðum gengur verkið út á að fara yfir hólf vinnutíma fyrir tilfang á uppgefnum punkti í ákveðna átt og finna nógu langt bil þar sem nauðsynleg afkastageta (tími) vinnslu passar inn.

Til að gera þetta þarf vélin að vita vinnutíma tilfangs. Gagnstætt aðalgagnalíkaninu, eru vinnutímarnir *Hlaðið við skoðun*, sem þýðir að þeir eru hlaðnir inn í vélina eftir þörfum. Ástæðan fyrir þessari nálgun er sú að oft eru vinnutímar í Supply Chain Management fyrir dagatal með mjög löngu tímabili og yfirleitt eru mörg dagatöl til staðar þannig að gögnin eru nokkuð stór til að forhlaða.

Vélin biður um dagatalsupplýsingar í bútum, með því að virkja X++ klasaaðferðina `WrkCtrSchedulingInteropDataProvider.getWorkingTimes`. Beiðnin er fyrir tiltekið dagatalskenni á ákveðnu tímabili. Háð stöðu á skyndiminni þjónsins í Supply Chain Management, gæti hver þessara beiðna endað í mörgum gagnagrunnsköllum, sem taka langan tíma (í samanburði við hreinan reiknitíma). Einnig, ef dagatalið inniheldur mjög vandaðar vinnutímaskilgreiningar með mörgum vinnutímabilum á dag, bætist það við tímann sem hleðslan tekur.

Þegar gögn um vinnutíma eru hlaðin í röðunarvélina, er þetta varðveitt í innra skyndiminni fyrir tiltekið dagatal, sem þýðir að ef aðrar vinnslur eða tilföng eru að nota sama dagatalið, þá verður hægt að framkvæma næstu uppflettingar á fljótlegan hátt úr minni. Ein algeng orsök slæmrar frammistöðu er ef sérstakt dagatalskenni er notað fyrir hvert tilfang vegna þess að þá verður nauðsynlegt að biðja um gögn fyrir hvert dagatal jafnvel þótt innihald dagatalanna kunni að vera það sama.

### <a name="finite-capacity"></a>Takmörkuð geta

Þegar takmörkuð geta er notuð, er vinnutímahólfum úr dagatalinu skipt niður og minnkuð út frá fyrirliggjandi frátekningum afkastagetu. Þessar frátekningar eru einnig sóttar í gegnum sama `WrkCtrSchedulingInteropDataProvider`-klasann og dagatölin, en nota í staðinn aðferðina `getCapacityReservations`. Þegar raðað er við aðaláætlanagerð eru frátekningar fyrir tiltekna aðaláætlunina teknar til greina og ef þær eru virkjaðar á síðunni **Færibreytur aðaláætlanagerðar**, er frátekningar úr staðfestum framleiðslupöntunum einnig hafðar með. Á sama hátt, þegar framleiðslupöntun er áætluð, er einnig valkostur að taka með frátekningar úr fyrirliggjandi áætluðum pöntunum, þó að þetta sé ekki eins algengt og hin leiðin.

Notkun takmarkaðrar getu veldur því að röðun tekur lengri tíma af ýmsum ástæðum:

- Að sækja afkastagetuupplýsingar úr gagnagrunni er hæg aðgerð og vistun á þessum upplýsingum í skyndiminni þjónsins er yfirleitt ekki eins góð og fyrir vinnutíma vegna þess að þeir eru ekki samnýttir á meðal tilfanga eins og dagatöl yfirleitt eru.
- Fjöldi vinnutímahólfa til að fara í gegnum eykst vegna skiptinganna og hólf fyrir lengri tímabil þarf að skoða sérstaklega áður en lausn finnst.
- Eftir að röðuninni er lokið verður að framkvæma athugun á misræmi í frátekningum (sjá hlutann „Keyra röðunarvélar samhliða“ til að fá frekari upplýsingar).

### <a name="examining-the-resource-combinations"></a>Samsetningar tilfanga skoðaðar

Ef vinnsluröðin inniheldur aðeins staðlaða `FinishStart`-tengla, sem þýðir að hún myndar einfalda keðju án greina, er hægt að ná ákjósanlegri niðurstöðu (séð út frá stakri pöntun, ekki öllum pöntunum) með því að finna bestu lausnina fyrir fyrstu vinnsluna og halda síðan áfram til að finna bestu lausnina fyrir næstu vinnslu. Besta lausnin fyrir vinnslu þýðir það að finna tilfang sem getur fengið frá og til dagsetningar vinnslunnar sem næst markmiði vinnslunnar (í röðun fram í tímann þýðir þetta að sækja lokadagsetningu vinnslunnar sem fyrst) meðan skorðunum er enn fylgt.

Þegar til staðar eru samhliða vinnslur getur leit að lausn falið í sér að skoða mismunandi samsetningar af tilföngum. Fjöldi mögulegra samsetninga á tilföngum er afurðin af fjölda viðeigandi tilfanga fyrir tengdar samhliða vinnslur. Sérstaklega þegar röð aftur í tímann er áætluð út frá þarfadagsetningunni, þá getur það tekið langan tíma fyrir reikniregluna að átta sig á því að það er engin lausn á vandanum sem gerir að verkum að samhliða vinnslurnar passi á undan deginum í dag, því að hún þarf að athuga allar samsetningar vegna þess að það gætu verið einhver tilföng sem voru með meiri skilvirkni eða annað dagatal sem gæti skilað niðurstöðu. Þetta þýðir að ef engin tímamörk hafa verið sett, verður hún keyrð í langan tíma áður en stefnunni er breytt í áfram.

Þessi reikniregla samsetningar þýðir einnig það að bæta við fleiri viðeigandi tilföngum getur gert að verkum að vélin hægir á sér. Ef afkastavandamál eiga sér stað við samhliða aðgerðir og röðun með ótakmarkaðri afkastagetu, getur það að hluta til verið lagfært með því að láta leiðarhönnuðinn taka ákvörðun um hvaða tilfang eigi að nota og úthluta svo tilfanginu beint á aðgerðina (vegna þess að vélin í flestum tilvikum mun alltaf enda á því að velja sama tilfangið, þannig að lokaniðurstaðan verði sú sama).

### <a name="hard-links"></a>Harðir tenglar

Ef gerð tengils milli tveggja vinnsla er stillt á harða gerð, er búið að tryggja að ekkert bil er á milli lok fyrstu vinnslu og upphafs þeirrar næstu. Þetta getur verið mjög gagnlegt í aðstæðum eins og þegar málmur er hitaður í einni vinnslu og síðan unnið úr honum í næstu vinnslu, þar sem ekki er æskilegt að málmurinn kólni inn á milli.

Með stöðluðum mjúkum tenglum og röðun fram í tímann, ef leiðin myndar einfalda keðju án greina, er hægt að komast að niðurstöðu með því að finna lausn fyrir fyrstu vinnsluna sem fullnægir eigin takmörkunum og halda síðan áfram í gegnum keðjuna með því að dreifa lokatímanum frá fyrri vinnslu yfir á næstu vinnslu. Ef núverandi vinnsla getur ekki fundið neina afkastagetu, verður upphafstími fyrir hana fluttur lengra áfram, án þess að fyrri vinnslur myndi hugsanlega bil milli vinnslanna. Hins vegar með hörðum tenglum (sérstaklega í tengslum við takmarkaða afkastagetu) við sömu aðstæður, það að ein vinnsla seinna í keðjunni finnur ekki afkastagetu, þýðir að „draga“ þarf allar fyrri raðaðar vinnslur áfram ein af annarri og þar af leiðandi endurraðað nokkrum sinnum. Sérstaklega í aðstæðum með hárri hleðslu fyrir mörg tilföng, geta harðir tenglar valdið keðjuverkun þar sem vinnslurnar hafa áhrif hver á aðra og gera þarf margar ítrekanir áður en jafnvægi kemst á niðurstöðuna í hentugri röð.

## <a name="running-scheduling-engines-in-parallel"></a>Röðunarvélar keyrðar samhliða

Þegar röðun er framkvæmd sem hluti af keyrslu aðaláætlanagerðar þar sem hjálparar eru notaðir, getur hver þessara hjálparþráða aðaláætlanagerðar einnig sótt röðunarverk framleiðslupöntunar. Þetta þýðir að hægt er að keyra margar röðunarvélar á sama tíma. Að vinna með mörgum þráðum hefur almennt séð umtalsverð áhrif á afköst, en þó eru til staðar nokkrir neikvæðir þættir þegar kemur að röðun.

Í MRP er öllum framleiðslupöntunum fyrir tiltekið uppskriftastig raðað í röð þarfadagsetningar, sem þýðir að þær pantanir sem eru með fyrstu þarfadagsetninguna ætti að vera raðað fyrst og hafa þannig mestan möguleika á því að fá tiltæka afkastagetu tilfanga. Hins vegar, með margar vélar sem eru taka úr listanum yfir óraðaðar pantanir, er ekki lengur hægt að tryggja röðina, þar sem ein gæti klárað hraðar en hin.

Einnig, þegar takmörkuð afkastageta er notuð við röðun og þegar mörg tilvik vélar eru að reyna að raða pöntunum sem eru hugsanlega að nota sömu tilföngin á sama tímabilinu, á sér stað keppni. Fjöldi slíkra keppnisaðstæðna eru skráðar í reitinn **Árekstrum raðað** á ferilsíðu aðaláætlunar. Úrlausnarrökin fyrir árekstra eru eftirfarandi:

- Tímasetja pöntun (ólæst) og fá frátekningar afkastagetu.
- Takið lásinn.
- Kannið hvort nýjar frátekningar á afkastagetu eru til staðar fyrir áætluð tilföng innan tímans sem um ræðir.
  - Ef nei, skal skrifa afkastagetuna og losa lásinn.
  - Ef já, skal losa lásinn og endurraða pöntuninni frá upphafi.

Þannig að þegar verið er að áætla með mörgum vélartilvikum er niðurstaðan ekki fullmótuð vegna þess að hún mun ráðast af nákvæmri tímasetningu hvers þráðar fyrir sig.

## <a name="operation-scheduling-performance"></a>Afköst aðgerðaröðunar

Jafnvel þótt aðgerðaröðun sé einnig þekkt sem afkastagetuáætlun í grófum dráttum, séð út frá vélinni, getur hún verið erfiðara vandamál að leysa ef takmörkuð afkastageta er notuð, því að þörf er á meiri gögnum til að ákvarða hentugleika.

Afkastageta tilfangaflokks veltur á því hvaða og hve mörg tilföng eru meðlimir tilfangaflokksins. Tilfangaflokkur í sjálfu sér er ekki með neina afkastagetu&mdash;aðeins þegar tilföng eru hluti af flokknum fá þær afkstagetu. Vegna þess að aðild að tilfangaflokknum getur verið breytileg eftir tíma, þarf að meta afkastagetu á hverjum degi.

Í aðgerðaröðun er dagatal tilfangaflokks notað til að ákvarða upphafs- og lokatíma fyrir hverja aðgerð. Þetta þýðir að dagatal tilfangaflokks setur mörk á það hversu mikill tími getur verið raðað af aðgerðum fyrir eina aðgerð á einum degi í einum tilfangaflokki. Gagnstætt dagatali fyrir tiltekin tilföng eru nýtingargögn dagatals hunsuð fyrir tilfangaflokkinn þar sem þau tákna einfaldlega opnunartíma en ekki raunverulega afkastagetu.

Til dæmis, ef vinnutími fyrir tilfangaflokk á einni tiltekinni dagsetningu er frá 8:00 til 16:00 getur ein aðgerð ekki sett meiri hleðslu á tilfangaflokkinn en það sem hægt er að gera á 8 klukkustundum, sama hversu mikla tiltæka afkastagetu tilfangaflokkurinn er með í heildina á þeim degi. Tiltæk afkastageta getur hins vegar takmarka hleðsluna enn frekar.

Hleðslan úr vinnsluröðun í öllum tilföngum sem eru í tilfangaflokknum á ákveðnum degi eru tekin til greina þegar tiltæk afkastageta fyrir tilfangaflokkinn á sama deginum er reiknuð. Fyrir hverja dagsetningu er útreikningurinn:

*Tiltæk afkastageta tilfangaflokks = afkastageta fyrir tilföng í flokknum byggt á dagatali &ndash; Vinnsluröðuðu hleðslunni á tilföngum í flokknum &ndash; Operations áætluð hleðsla á tilföngum í flokknum &ndash; Operations áætluð hleðsla á forðaflokknum*

Í flipanum **Tilfangaþarfir** í leiðaraðgerðinni, er hægt að tilgreina tilfangaþörfina með því að nota annaðhvort tiltekið tilfang (í slíku tilfelli verður aðgerðinni raðað með því að nota það tilfang), fyrir tilfangaflokk, fyrir tilfangagerð eða fyrir eina eða fleiri getu, hæfni, námskeið eða vottorð. Þegar allir þessir valmöguleikar eru notaðir er mikill sveigjanleiki fólginn í hönnun leiðar, hún flækir einnig röðun vélarinnar þar sem taka verður afkastagetu getu greina fyrir hvern „eiginleika“ (óhlutbundið heiti sem notað er í vélinni fyrir getu, hæfni o.s.frv.).

Afkastageta tilfangaflokks fyrir getu er samtala afkastagetu allra tilfanga í tilfangaflokknum sem er með umrædda getu. Ef tilfang í flokknum er með getu verður það tekið til greina sama hvaða stig getunnar er nauðsynlegt.

Í aðgerðaröðun verður tiltæk afkastageta fyrir tiltekna getu fyrir tilfangaflokk minnkuð þegar henni er hlaðið með aðgerð sem krefst getunnar sem um ræðir. Ef aðgerðin þarf fleiri en eina getu, verður afkastagetan minnkuð fyrir allar nauðsynlegar getur.

Fyrir hverja dagsetningu er nauðsynlegur útreikningur:

*Tiltæk afkastageta fyrir getu = afkastageta fyrir getu &ndash; Vinnsluröðuðu álagi á tilföngum með tilgreindum getu, tekin með í tilfangaflokki &ndash; Operations áætluð hleðsla á tilföngum með tilgreindum getu, tekin með í tilfangaflokki &ndash; Operations áætluð hleðsla á forðaflokknum sjálfu sem útheimtir tiltekna getu*

Þetta þýðir að ef álag er á tilteknu tilfangi er álagið talið með í útreikningi á tiltækri afkastagetu tilfangaflokks fyrir hverja getu, því að álagið á tilteknu tilfangi dregur úr framlagi þess til afkastagetu tilfangaflokksins fyrir getu, sama hvort álagið á tilteknu tilfangi er fyrir þessa tilteknu getu. Ef álag er á stigi tilfangaflokksins, er það tekið með í útreikningi á tiltækri afkastagetu tilfangaflokksins fyrir hverja getu eingöngu ef álagið kemur til vegna aðgerðar sem krefst tiltekinnar getu.

Ofangreind reiknirök eru flókin því að það er það sama fyrir hverja gerða af „eiginleika“, þannig að aðgerðaröðun með takmarkaða afkastagetu krefst umtalsverðs gagnamagns til að vera hlaðin.

## <a name="viewing-scheduling-engine-input-and-output"></a>Skoða inntak og úttak röðunarvélar

Til að fá tilteknar upplýsingar um inntak og úttak röðunarferlis skal virkja innskráningu með því að fara í **Fyrirtækisstjórnun \> Uppsetning \> Röðun \> Stjórnklefi röðunarrakningar**.

Á þessari síðu skal fyrst velja **Virkja innskráningu** á aðgerðasvæðinu. Keyrið síðan röðunina fyrir framleiðslupöntunina. Þegar því er lokið skal fara aftur á síðuna **Stjórnklefi röðunarrakningar** og velja **Slökkva á skráningu** á aðgerðasvæðinu. Endurhlaðið síðuna og ný lína birtist í hnitanetinu. Velja skal nýju línuna og velja **Niðurhal** á aðgerðasvæðinu. Þetta mun gefa upp þjappaða zip-möppu sem inniheldur eftirfarandi skrár:

- **Log.txt** - Þetta er kladdaskráin sem lýsir skrefunum sem vélin fer í gegnum. Hún er mjög ítarleg og getur verið dálítið yfirþyrmandi, en þegar hún er notuð sem hluti af því að prófa uppsetningu leiðar til að leysa úr vandamálum vegna afkasta, þá skal fyrst skoða tímamismuninn milli fyrstu og síðustu línu, þar sem þetta mun gefa nákvæman tíma sem áætlunin hefur notað.
- **XmlModel.xml** - Þetta inniheldur líkanið sem er smíðað í X++ og sem vélin vinnur á. `JobId` sem notað er í skránni samsvarar `RecId` úr upprunatöflunni sem inniheldur vinnslurnar (`ReqRouteJob` eða `ProdRouteJob`). Dæmigerður hlutur sem á að leita að í þessari skrá er sá að dagsetningarnar sem eru gefnar upp í `ConstraintJobStartsAt` og `ConstraintJobEndsAt` eru eins og búist er við, að `JobGoal` eiginleikinn sé rétt stilltur og að vinnslurnar tengist hver annarri í gegnum `JobLink`-takmarkanir.
- **XmlSlots.xml** - Þetta inniheldur alla vinnutímana og fráteknar afkastagetur sem vélin hefur beðið um. Aðeins vélin mun óska eftir vinnutímum og frátekningum dagatalsins fyrir tímabilin þar sem hún reynir að koma vinnunni fyrir (og aukalegan biðtíma), þannig að ef skráin inniheldur tíma langt fram í tímann, gæti það verið vísbending um vandamál með uppsetninguna. `ResourceProperty`-hnútarnir birtast fyrir hvert tilfang í þeim tilfangaflokki og getu sem það tengist fyrir það tímabil.
- **Result.xml** - Þetta inniheldur niðurstöður fyrir röðunarkeyrsluna.

Athugið að rakningarvirknin getur aukið álagið umtalsvert, þannig að eingöngu skal nota hana til að skoða röðun á tilteknum pöntunum á kerfisbundinn hátt. Ef kveikt er á henni meðan aðaláætlanagerðin er í gangi, nær hún fljótt upp í hámarksstærð og hættir.

## <a name="troubleshooting-performance"></a>Afköst úrræðaleituð

Af fyrri köflunum að dæma er skiljanlegt að ýmsar hindranir geta komið upp þegar kemur að uppsetningunni og notkun á röðunarvélinni, sem geta leitt til afkastavandamála. Eftirfarandi gátlista er hægt að nota til að leysa úr slíkum vandamálum. Mikilvægt er að skoða öll atriðin þar sem vandinn er oftast samblanda af mörgum þáttum sem leiða til vandamála.

### <a name="performing-scheduling-as-part-of-mrp-when-it-is-not-needed"></a>Framkvæma áætlanagerð sem hluta af MRP þegar þess gerist ekki þörf

Jafnvel þótt leiðir séu notaðar til að stýra framleiðslu, svo sem kostnaður og skýrslugerð, er það ekki endilega nauðsynlegt til að taka tillit til þeirra meðan MRP er í gangi. Í sumum tilvikum er nóg að vera með hefðbundinn afhendingartíma framleiðslu gefinn upp fyrir vöruna fyrir áætlanagerð. Til að slökkva á áætlanagerð leiðar skal stilla tímamörk afkastagetu á núll. Ef gera á áætlanagerð, þarf að stilla tímamörk afkastagetunnar vel og vandlega því að hugsanlega er ekki nauðsynlegt að taka tillit til leiða að öllu leyti fyrir tímamörk á umfangi MRP.

Athugið að ef pöntunin er ekki tímasett meðan MRP er í gangi, þar í staðinn að tímasetja hana þegar áætluð pöntun er staðfest. Þetta þýðir að staðfestingarferlið tekur lengri tíma, þannig að það fer eftir því hversu margar af ráðlögðum áætluðum pöntunum verða staðfestar hvort afkastaaukningin meðan MRP er í gangi tapist við staðfestingu.

### <a name="route-with-unnecessary-operations"></a>Leið með ónauðsynlegum aðgerðum

Þegar leiðin er hönnuð getur verið freistandi að líkja eftir raunverulegum aðstæðum með öllum skrefunum sem framleiðslan fer í gegnum. Þótt þetta geti reynst gagnlegt í einhverjum tilfellum, hjálpar það ekki afköstunum því að líkanið sem vélin þarf að keyra á stækkar (bæði hvað varðar vinnslur og takmarkanir) og fleiri SQL-skipanir verða keyrðar fyrir innsetningu og uppfærslu á vinnslum og frátekinni afkastagetu. Einnig gætir áhrifa eftir á þegar þarf að tilkynna framvindu vinnslanna, sem hægt er að flytja með sjálfvirkum bókunum. Ef gögnin eru ekki notuð í neitt, skapar það óþarfa álag.

Við mælum með því að aðeins nauðsynlegar aðgerðir séu búnar til fyrir áætlanagerð (sem eru yfirleitt flöskuhálstilföngin) og/eða kostnaðarútreikninga. Að öðrum kosti ætti að flokka margar smærri aðgreindar aðgerðir í eina stærri aðgerð sem stendur fyrir stærri hluta ferlisins.

### <a name="many-applicable-resources-for-an-operation"></a>Mörg viðeigandi tilföng fyrir aðgerð

Fjöldi viðeigandi tilfanga fyrir aðgerð er ákvarðaður með tilfangaþörfinni sem er stillt í aðgerðartengslunum. Þörfin getur annaðhvort verið fyrir tiltekið (stakt) tilfang eða það getur byggt á aðild tilfangs að tilfangaflokki eða getu.

Ef áætlanagerð er ekki gerð með takmarkaðri getu og öll viðeigandi tilföng eru með sama dagatalið og skilvirkni, mun röðunarvélin alltaf enda á því að velja sama tilfangið fyrir aðgerð, en aðeins eftir að hafa reynt viðeigandi tilföng til að athuga hvort að eitt þeirra er „betra“ en hin. Í slíku tilfelli er hægt að minnka álagið á áætlanagerð til muna með því einfaldlega að úthluta alltaf tilteknu tilfangi á aðgerðina á hönnunartíma leiðarinnar.

### <a name="route-with-parallel-operations"></a>Leið með samhliða aðgerðum

Samhliða aðgerðir (aðal/auka) eru öflugt verkfæri til að líkja eftir aðstæðum þegar bæði þarf vél og notanda til að framkvæma tiltekið verk, en þær eru einnig rótin að ýmsum vandamálum varðandi afköstin. Ef þörf fyrir tilttekið stakt tilfang er úthlutað á bæði aðal- og aukaaðgerð, veldur það yfirleitt ekki vandræðum. En ef mörg möguleg tilföng eru til staðar fyrir hverja þessara aðgerða, þá eykst flækjustig útreikninga áætlanagerðar umtalsvert.

Önnur leið en að nota samhliða aðgerðir er annaðhvort líkja eftir pörunum sem „sýndar“tilföng (sem stendur þá alltaf fyrir teymið sem fer saman í gegnum aðgerðina) eða einfaldlega ekki líkja ekki eftir neinni aðgerð ef hún stendur ekki fyrir flöskuháls.

### <a name="route-with-quantity-of-resources-higher-than-1"></a>Leiðir með fjölda tilfanga hærri en 1

Ef fjöldi tilfanga sem þarf fyrir aðgerð er stilltur á hærra en einn, þá kemur það út á það sama og að nota aðal-/aukaaðgerðir vegna þess að margar samhliða vinnslur eru sendar til vélarinnar. Hins vegar, fyrir þetta tilfelli er ekki möguleiki á að nota sérstakar úthlutanir tilfanga vegna þess að fjöldi sem er hærra en einn krefst þess að fleiri en eitt tilfang eigi við um aðgerðina.

### <a name="excessive-use-of-finite-capacity"></a>Óhófleg notkun á takmarkaðri getu

Notkun takmarkaðrar afkastagetu krefst þess að vélin hlaði upplýsingum um afkastagetu úr gagnagrunni og geti haft reikningsálag vegna þess að það verður erfiðara að finna lausn, sérstaklega í umhverfum þar sem tilföngin eru bókuð nálægt hámarksafkastagetu þeirra. Þar af leiðandi er mikilvægt að meta vandlega hvort tilfang þurfi raunverulega að nota takmarkaða afkastagetu því annars gætu þau verið yfirbókuð. Vegna þess að það gæti verið mismunur á milli tilfanga takmarkaðrar afkastagetu í því hversu mikilvægt er að yfirbóka þau ekki, er mælt með því að nota valkost flöskuháls á tilfang í samsetningu við sérstakt gildi í áætluninni í „Tímamörk afkastagetu fyrir flöskuhálstilföng“. Með því að nota flöskuhálsinn er hægt að gera kleift að lækka almenn tímamörk takmarkaðrar afkastagetu.

### <a name="setting-hard-links"></a>Harðir tenglar settir upp

Stöðluð tenglagerð leiðarans er *mjúk*, sem þýðir að bil er leyfilegt á milli lokatíma einnar aðgerðar og upphafs þeirrar næstu. Ef þetta er gert getur það haft óheppileg áhrif, ef efni eða afkastageta er ekki í boði fyrir eina af aðgerðunum í mjög langan tíma, gæti framleiðslan verið aðgerðalaus um nokkurt skeið, sem þýðir mögulega aukningu á verkum í vinnslu. Þetta gerist ekki með hörðum tenglum vegna þess að lok og upphaf verða að passa fullkomlega saman. En ef harðir tenglar eru settir upp gerir það áætlanagerð erfiðara um vik vegna þess að skaranir á vinnutíma og afkastagetu verða að vera reiknaðar út fyrir bæði tilföng aðgerðanna. Ef það eru einnig samhliða aðgerðir til staðar, eykst tími útreiknings til muna. Ef tilföng aðgerðanna tveggja eru með mismunandi dagatöl sem skarast ekki á neinn hátt, er ekki hægt að leysa vandamálið.

Aðeins er mælt með því að nota harða tengla þegar það er algjörlega nauðsynlegt og íhuga vel og vandlega hvort þeir eru nauðsynlegir fyrir hverja aðgerð leiðarinnar.

Til að draga úr verkum í vinnslu án þess að nota harða tengla er ein leiðin að áætla pöntunina tvisvar sinnum og breyta stefnu hennar í hina áttina í seinna skiptið. Ef fyrsta áætlunin var gerð afturábak frá afhendingardegi, ætti hin síðari að vera gerð áfram frá áætluðum upphafsdegi. Þetta leiðir til þess að vinnslunum verði þjappað saman eins vel og mögulegt er þannig að verk í vinnslu verði lágmarkað.

### <a name="separate-calendar-for-each-resource"></a>Aðskilið dagatal fyrir hvort tilfang

Einn helsti gagnagjafi röðunarvélarinnar eru dagatalsupplýsingar, sem getur verið dýrt að hlaða úr gagnagrunninum. Þar sem dagatöl eru mynduð út frá sniðmátum, getur verið freistandi að búa til dagatal fyrir hvert tilfang og laga svo upplýsingarnar til í þessu dagatali þegar tilfangið er með niðurtíma og önnur vandamál. Ef þetta er gert dregur það hins vegar umtalsvert úr getu vélarinnar til að vista dagatalsgögn í skyndiminni, þar sem hún þyrfti að óska eftir nýjum gögnum fyrir hvert tilfang og það getur leitt til umtalsverðra vandamála varðandi afköst. Þess í stað er mælt með því að endurnýta dagatölin eins mikið og hægt er á milli tilfanganna og síðan stjórna breytingum á niðurtíma með því að úthluta öðru dagatalskenni fyrir tímabil.

### <a name="high-number-of-working-time-slots-per-calendar-day"></a>Mikill fjöldi vinnutímahólfa á almanaksdag

Vegna þess að vélin vinnur með því að skoða afkastagetu hvers tímahólfs fyrir sig, er gagnlegt að lágmarka fjölda tímahólfa á almanaksdag. Þetta gæti verið gert, t.d. með því að velta fyrir sér hvort það sé mikilvægt að væntanleg áætlun endurspegli það að starfsmenn fái 5 mínútna hlé á klukkustundarfresti.

### <a name="large-or-none-scheduling-timeouts"></a>Stórar (eða engar) tímalokanir áætlanagerðar

Hægt er að hámarka afköst röðunarvélar með því að nota færibreytur sem er að finna á síðunni **Færibreytur röðunar**. Stillingarnar **Tímalokun áætlanagerðar virkjuð** og **Hámörkun tímalokunar áætlanagerðar virkjuð** eiga alltaf að vera á **Já**. Ef stillt er á **Nei** getur röðunin mögulega keyrt endalaust ef óæskileg leið með mörgum valkostum hefur verið búin til.

Gildið fyrir **Hámarkstími röðunar á hverja röð** stjórnar því hversu margar sekúndur að hámarki má eyða í að reyna að finna lausn fyrir eina röð (í flestum tilfellum á röð við um staka pöntun). Gildið sem á að nota hér fer mjög eftir flækjustigi leiðarinnar og stillingum eins og takmarkaðri afkastagetu, gott er að byrja á hámarki sem nemur u.þ.b 30 sekúndum.

Gildi fyrir **Tímalokun á tilraunum hámörkunar** stjórnar því hversu margar sekúndur má nota í mesta lagi til að finna betri lausn en þá sem fannst fyrst. Þetta mun aðeins hafa áhrif á leiðir sem nota samhliða aðgerðir þar sem þær gera það nauðsynlegt til að prófa mismunandi samsetningar.

> [!NOTE]
> Gildin sem eru sett upp fyrir tímalokanir verða bæði notuð fyrir röðun útgefinna framleiðslupantana og áætlaðra pantana sem hluta af MRP. Þar af leiðandi gætu mjög há gildi bætt umtalsvert við keyrslutíma MRP þegar áætlun er keyrð með mörgum framleiðslupöntunum.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]