---
title: Launaútreikningur
description: Launaútreikningur gerir þér kleift að reikna nýjar grunnlaunaupphæðir fyrir starfsmenn þína á grundvelli launaleiðréttingar, marka verðleikaaukningar og afkasta.
author: andreabichsel
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 979a4f311d59cb51cdf0fc6ce85d5b3338ffa870
ms.sourcegitcommit: 4a32634690a741535f3f4babfd753f7c227ad6fe
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/05/2020
ms.locfileid: "3958718"
---
# <a name="process-compensation"></a>Launaútreikningur

Launaútreikningur gerir þér kleift að reikna nýjar grunnlaunaupphæðir fyrir starfsmenn þína á grundvelli launaleiðréttingar, marka verðleikaaukningar og afkasta. Þessi grein fer yfir grunnflæði launavinnslu fyrir launafyrirkomulag með föstum launum án þess að tekið sé tillit til afkasta starfsmanns.

## <a name="plan-the-new-compensation-amounts-and-budgets"></a>Áætla nýjar launaupphæðir og setja saman áætlanir
Til að veita starfsmönnum verðleikaaukningu verður að setja upp áætlun fyrir fasta aukningu fyrir hverja deild: Launastjórnun > Tenglar > Mörk verðleikaaukningar. (Einnig er hægt að opna þessa skjámynd í gegnum Deild: Fyrirtæki > Deildir.) Hér geturðu tilgreint frekar hvort starfsmenn í ákveðnu verkalýðsfélagi eða staðsetningu eigi að fá aðra prósentuhækkun. Reitirnir **Áætlun** og **Gjaldmiðill** eru til upplýsingar og þá má nota til að setja inn gjaldmiðilsupphæð fyrir áætlunina.

## <a name="set-up-the-compensation-process"></a>Setja upp launavinnslu
Vinnslutilvik gerir kleift að tilgreina færibreytur fyrir launavinnslu. Þar á meðal er tímabilið til að meta og ákvarða launaupphæðir og dagsetningin þegar nýjar launaupphæðir eiga að taka gildi.

Einnig er hægt að hafa ráðningardagsetningu fyrir föst laun ef einhverjar fastar launaáætlanir notast við ráðningarreglu með prósentum. Fyrir þær áætlanir fær hver sá sem var ráðinn eftir upphafsdagsetningu ferlis og fyrir ráðningardagsetningu fyrir föst laun, 100% af sinni útreiknuðu verðleikaaukningu eða almennri hækkun. Hver sá sem var ráðinn eftir ráðningardagsetningu fyrir föst laun og fyrir lokadagsetningu tímabils fær hlutfall af útreiknaðri hækkun, á grundvelli fjölda ráðningardaga af heildardagafjölda tímabils. Ef tímabilið er til dæmis er frá 1. janúar til og með 31. desember og ráðningardagsetning fyrir föst laun er 1. apríl fær starfsmaður sem er ráðinn í mars alla útreiknaða hækkunina, á meðan starfsmaður sem ráðinn er 1. júlí fær u.þ.b. helming útreiknaðrar hækkunar.

Vinnslutilvikið **Tímapunktur** er einungis notað fyrir úrvinnslu á ákveðnu breytilegu launafyrirkomulagi og ekki verður fjallað um það hér. **Yfirfara skilafrest** er fresturinn fyrir allar ráðleggingar þannig að hægt sé að setja nýja launaupphæð inn í starfsmannafærslu. Endurskoðunardagsetningin er einungis til upplýsingar.

Þegar færibreytur vinnslutilviksins hafa verið vistaðar, geturðu smellt á hnappinn **Uppsetning** til að setja inn áætlanirnar sem eiga að vera með í þessari keyrslu og hvaða fastlaunaaðgerða eigi að grípa til fyrir hverja áætlun.

Smelltu á hnappinn **Bæta við** í flipanum **Áætlanir** til að bæta launaáætlun við vinnslutilvikið. Dálkarnir **Nota aðra vogun**, **Vogunarhlutfall** og **Lýsing vogunar** eru aðeins notaðir fyrir breytilegar launaáætlanir og ekki er fjallað um þá í þessari grein.

Vistaðu færsluna og smelltu svo á hnappinn **Bæta við** í flipanum **Aðgerðir** til að bæta fastlaunaaðgerðum við valda áætlun. Notaðu valkostinn **Virkja ráðleggingu** til að slá inn upphæð sem er önnur en útreiknuð leiðbeinandi hækkun fyrir aðgerðina. Viljir þú að aðgerð sé reiknuð út eftir niðurstöðu síðustu aðgerðar til að tengja saman margar launaaðgerðir, skaltu merkja við valkostinn **Nota síðustu niðurstöður**, aðgerðar fastra launa eru launareglur sem hægt er að gefa lýsandi nöfn. Ef um er að ræða launaþrep eða greiningaráætlanir getur þú aðeins bætt við aðgerðum fastra launa sem eru af eftirfarandi gerðum:

| Aðgerðir fastra launa | Virkni                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Eigið fé                        | Í launaleiðréttingaraðgerðum er launataxti starfsmanns frá og með lokadagsetningu ferlis borinn saman við lægsta viðmiðunarpunktinn fyrir það stig sem gefið er upp fyrir starf starfsmanns. Ef launataxti starfsmanns er lægri en lágmarks viðmiðunarpunkturinn er nauðsynleg hækkun til að ná starfsmanninum upp í lágmarkspunkt mengisins reiknuð út.                                                                                |
| Verðleiki                         | Verðleikaaðgerðir reikna út hækkun út frá launataxta starfsmanns frá og með lokadagsetningu ferlis og þeirri prósentuhækkun sem er að finna í áætlun fastrar aukningar fyrir deild, verkalýðsfélag og staðsetningu starfsmannsins.                                                                                                                                                                                         |
| Almennt                       | Í almennum aðgerðum er reiknuð út hækkun fyrir starfsmanninn, annaðhvort prósentuhækkun eða föst upphæð. Þetta er ákvarðað samkvæmt stillingunum **Föst laun** í flipanum **Almennt**.                                                                                                                                                                                                                        |
| Stöðuhækkun                     | Stöðuhækkunararaðgerðir gefa þér upp tiltekinn stað þar sem þú getur veitt stöðuhækkun. Gættu þess því að merkja við valkostinn **Virkja ráðleggingu** þannig að hægt sé að færa inn ráðleggingu fyrir þá starfsmenn sem fá stöðuhækkun.  Starfsmenn án ráðlagðrar hækkunar fá ekki aðgerðina **Stöðuhækkun** á fasta launaskrá sína.                                                                       |
| Önnur breyting á stigi            | Í dæminu á undan er **Stöðulækkun** heiti aðgerðarinnar **Föst laun**, ásamt gerðinni **Önnur breyting á stigi**. Þetta býr til reglu fyrir 0 (núll-breyting) þannig að þú getur sett inn ráðlagða upphæð til að breyta launataxta starfsmannsins. (Gangið úr skugga um að merkja við valkostinn **Virkja ráðleggingu**.) Starfsmenn án ráðleggingar fá ekki þessa aðgerð í fasta launaskrá sína. |

Aðeins er hægt að bæta við aðgerðunum **Föst laun** með áætlun af gerðinni Frá þrepi til þreps.

| Aðgerðir fastra launa | Virkni                                                                                                                                                                                           |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Þrep                           | Gefðu til kynna á flipanum Almennt hvort þessi þrepaaðgerð eigi að færa starfsmenn áfram upp um 0 þrep, 1 þrep eða 2 þrep.                                                                                  |
|                                | **0 þrep** - Starfsmaður fær launataxtann fyrir núverandi þrep hans.                                                                                                                      |
|                                | **1 þrep** - Kerfið kannar hvort starfsmaðurinn sé þegar á síðasta viðmiðunarpunkti fyrir sitt stig.                                                                                             |
|                                | **2 þrep** - Kerfið færir starfsmanninn upp um tvö þrep á núverandi stigi hans. Kerfið getur mögulega fært starfsmann um eitt eða ekkert þrep ef hann hefur þegar náð síðasta viðmiðunarpunkti fyrir sitt stig. |

## <a name="run-the-compensation-process"></a>Keyra Launavinnsla
Eftir að vinnslutilvikið hefur verið sett upp með nauðsynlegum dagsetningareitum, áætlunum og aðgerðum, geturðu smellt á **Keyra vinnslu** á síðunni **Vinnslutilvik**. Sé það gert, opnast svarglugginn **Keyra launavinnslu**. Í þessum svarglugga geturðu smellt á valkostinn **Sýna niðurstöður vinnslu** til að sjá hvernig launaupphæðir voru reiknaðar fyrir hvern starfsmann. Sé smellt á **Í lagi** er launavinnsla keyrð fyrir alla starfsmenn sem eru í þeirri launaáætlun sem er valin frá og með lokadagsetningu ferlis.

## <a name="view-the-process-results"></a>Skoða niðurstöður vinnslu
Til að skoða niðurstöður ferlis opnarðu síðuna **Vinna niðurstöður**. Nýtt launatilvik er stofnað í hvert sinn sem vinnslutilvik er keyrt. Þannig er hægt að gera prufukeyrslur, gera leiðréttingar og keyra launatilvik mörgum sinnum til að sjá hvernig hinar ýmsu breytingar hafa áhrif á laun starfsmanns.

Síðan **Vinna niðurstöður** inniheldur upplýsingar um keyrsluna, þar á meðal hvenær keyrslan átti sér stað, notandann sem setti keyrsluna í gang og hvort einhverjar villur komu upp við keyrslu ferlisins. Einnig er hægt að merkja við valkostinn **Læst** til að afvirkja hnappinn **Hlaða laun** og koma í veg fyrir að einhver hlaði launatilviki niður í starfsmannaskrár. Sé smellt á hnappinn **Starfsmannaniðurstöður** birtist listi yfir starfsmenn sem eru með í keyrslunni.

Valkosturinn **Niðurstöður starfsmanna** sýnir upplýsingar um ferlið sjálf, auk allra launaaðgerða sem framkvæmdar voru í ferlinu. Hlutinn **Föst laun** mun innihalda færslu fyrir hverja aðgerð í vinnslutilvikinu fyrir launafyrirkomulagið. Dálkarnir **Gildandi leiðbeining** og **Ráðlegging** munu birta fleiri upplýsingar fyrir aðgerðina sem valin er í hlutanum **Föst laun**. Ef **Virkja ráðleggingar** var merkt fyrir aðgerðina, verður hægt að breyta reitunum fyrir Ráðleggingar. Þetta gerir þér kleift að leiðrétta handvirkt upphæðirnar fyrir starfsmanninn. Athugaðu að ef þú hefur merkt **Nota síðustu niðurstöður** fyrir aðgerðina í vinnslutilvikinu, verður þú að uppfæra handvirkt upphæðirnar í öllum tengdum aðgerðum.

Þegar launaupphæðirnar hafa verið endurskoðaðar fyrir starfsmann og einhverjar leiðréttingar á ráðlögðum gildum hafa verið gerðar, getur þú breytt **Stöðu** í línunni **Starfsmannatilvik** til að gefa til kynna hvort tilvik hafi verið samþykkt eða ætti að hunsa. Einnig er hægt að eyða öllum breytingum sem gerðar eru á ráðleggingum starfsmanns með því að smella á hnappinn **Endurreikna**. Þetta merkir núverandi starfsmannatilvik með stöðunni Hunsa og stofnar nýtt starfsmannatilvik með endurreiknuðum gildum.

## <a name="loading-approved-compensation-changes"></a>Innlestur á launabreytingum samþykktur
Þegar eitt eða fleiri starfsmannatilvik hafa fengið uppfærða stöðu í Samþykkt er hægt að lesa þau inn í fastar launaskrár starfsmanna. Hægt er að gera þetta annaðhvort með því að velja eitt starfsmannatilvik í einu og smella á hnappinn **Hlaða launum starfsmanns** á síðunni **Niðurstöður starfsmanns**, eða með því að smella á **Hlaða launum** á síðunni **Vinna niðurstöður** til að hlaða öllum samþykktum starfsmannatilvikum í einu.

Sé smellt á **Í lagi** í svarglugganum **Hlaða laun** bætir það launaaðgerðalínum sem eru ekki núll við síðuna **Föst laun starfsmanns**.
