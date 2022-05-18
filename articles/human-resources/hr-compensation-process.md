---
title: Launaútreikningur
description: Launaútreikningur gerir þér kleift að reikna nýjar grunnlaunaupphæðir fyrir starfsmenn þína á grundvelli launaleiðréttingar, marka verðleikaaukningar og afkasta.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: e4aa910d92c2905d54d96f656e1d3d1c36388636
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693865"
---
# <a name="process-compensation"></a>Launaútreikningur


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Launaútreikningur gerir þér kleift að reikna nýjar grunnlaunaupphæðir fyrir starfsmenn þína á grundvelli launaleiðréttingar, marka verðleikaaukningar og afkasta. Þetta efnisatriði fer yfir grunnflæði launavinnslu fyrir launafyrirkomulag með föstum launum án þess að tekið sé tillit til afkasta starfsmanns.

## <a name="plan-the-new-compensation-amounts-and-budgets"></a>Áætla nýjar launaupphæðir og setja saman áætlanir
Til að gefa starfsmönnum þínum verðleikaaukningu verður þú að setja upp fasta hækkun fjárhagsáætlunar fyrir hverja deild þína: **Launastjórnun** > **Tenglar** > **Markhópar verðleikaaukningar**. (Einnig er hægt að opna þessa síðu í gegnum deildina: **Fyrirtæki** > **Deildir**.) Þú getur tilgreint hvort starfsmenn í ákveðnu verkalýðsfélagi eða staðsetningu eigi að fá aðra prósentuhækkun. Reitirnir **Áætlun** og **Gjaldmiðill** eru til upplýsingar og þá má nota til að setja inn gjaldmiðilsupphæð fyrir áætlunina.

## <a name="set-up-the-compensation-process"></a>Setja upp launavinnslu
Á síðunni **Launavinnslur** getur þú tilgreint færibreyturnar fyrir launavinnsluna. Þar á meðal er tímabilið til að meta og ákvarða launaupphæðir og dagsetningin þegar nýjar launaupphæðir eiga að taka gildi.

Þú getur einnig haft með **Ráðningardagsetning fyrir föst hlutfallsleg laun** ef eitthvað launafyrirkomulag fastra launa notar prósentu sem ráðningarreglu. Fyrir slíkt fyrirkomulag munu allir sem voru ráðnir eftir **Upphafsdagsetningu ferlis** og á undan **Ráðningardagsetning fyrir föst hlutfallsleg laun** fá 100% af útreiknuðum verðleika eða almenna hækkun. Allir sem voru ráðnir eftir **Ráðningardagsetning fyrir föst hlutfallsleg laun** og á undan **Lokadagsetningu ferlis** munu fá hluta af útreiknaðri hækkun eftir því hversu marga daga þeir hafa verið við störf af heildartímabilinu. Ef ferlið keyrir til dæmis frá 1. janúar til 31. desember og ráðningardagsetning fastra hlutfallslegra launa er 1. apríl mun starfsmaður sem er ráðinn í mars fá útreiknaða hækkun að fullu á meðan starfsmaður sem var ráðinn 1. júlí mun fá u.þ.b. hálfa útreiknaða hækkun.

Vinnslutilvikið **Tímapunktur** er einungis notað fyrir úrvinnslu á ákveðnu breytilegu launafyrirkomulagi og ekki verður fjallað um það hér. **Yfirfara skilafrest** er fresturinn fyrir allar ráðleggingar þannig að hægt sé að setja nýja launaupphæð inn í starfsmannafærslu. Endurskoðunardagsetningin er einungis til upplýsingar.

Eftir að færibreytur vinnslutilviksins hafa verið vistaðar er hægt að smella á hnappinn **Uppsetning** til að velja áætlanirnar sem á að nota þegar ferlið er keyrt og hvaða aðgerða fastra launa á að grípa til fyrir hverja áætlun.

Smelltu á hnappinn **Bæta við** í flipanum **Áætlanir** til að bæta launafyrirkomulagi við vinnslutilvikið. Dálkarnir **Nota aðra vogun**, **Vogunarhlutfall** og **Lýsing vogunar** eru aðeins notaðir fyrir breytilegar launaáætlanir og ekki er fjallað um þá í þessu efnisatriði.

Vistaðu færsluna og smelltu svo á hnappinn **Bæta við** í flipanum **Aðgerðir** til að bæta við aðgerðum fastra launa fyrir valda áætlun. Notaðu valkostinn **Virkja ráðleggingu** til að slá inn upphæð sem er önnur en útreiknuð leiðbeinandi hækkun fyrir aðgerðina. Til að reikna út aðgerð sem er byggð á niðurstöðu fyrri aðgerðar til að tengja margar launaaðgerðir skal merkja valkostinn **Nota síðustu niðurstöður**. Aðgerðir fastra launa eru gerðir af launarökum sem hægt er að gefa lýsandi heiti. Fyrir **Einkunn** og **Hljómsveit** áætlunum geturðu aðeins bætt við föstum bótaaðgerðum sem eru af eftirfarandi gerðum:

| Aðgerðir fastra launa | Virkni                  |
|-------------------------------|-------------------------------------------------------------------------|
| Eigið fé                        | Í launaleiðréttingaraðgerðum er launataxti starfsmanns frá og með lokadagsetningu ferlis borinn saman við lægsta viðmiðunarpunktinn fyrir það stig sem gefið er upp fyrir starf starfsmanns. Ef launataxti starfsmanns er lægri en lágmarks viðmiðunarpunkturinn er nauðsynleg hækkun til að ná starfsmanninum upp í lágmarkspunkt mengisins reiknuð út.                                                                                |
| Verðleiki                         | Verðleikaaðgerðir reikna út hækkun út frá launataxta starfsmanns frá og með lokadagsetningu ferlis og þeirri prósentuhækkun sem er að finna í áætlun fastrar aukningar fyrir deild, verkalýðsfélag og staðsetningu starfsmannsins.                                                                                                                                                                                         |
| Almennt                       | Í almennum aðgerðum er reiknuð út hækkun fyrir starfsmanninn, annaðhvort prósentuhækkun eða föst upphæð. Þetta er ákvarðað samkvæmt stillingunum **Föst laun** í flipanum **Almennt**.                                                                                                                                                                                                                        |
| Stöðuhækkun                     | Aðgerðir stöðuhækkunar gefa þér upp nefndan stað þar sem þú getur veitt stöðuhækkun. Merktu við valkostinn **Virkja tillögu** til að færa inn tillögu fyrir starfsmenn sem fá stöðuhækkanir.  Starfsmenn án ráðlagðrar hækkunar fá ekki aðgerðina **Stöðuhækkun** á fasta launaskrá sína.                                                                       |
| Önnur breyting á stigi            | Í fyrra dæminu er **Stöðulækkun** heiti aðgerðarinnar **Föst laun** með gerðina **Önnur breyting á stigi**. Þetta býr til reglu fyrir 0 (núll-breyting) þannig að þú getur sett inn ráðlagða upphæð til að breyta launataxta starfsmannsins. (Veldu valkostinn **Virkja tillögu**.) Starfsmenn án tillögu munu ekki fá þessari aðgerð bætt við færslur fastra launa. |

Aðeins er hægt að bæta við aðgerðunum **Föst laun** með áætlun af gerðinni Frá þrepi til þreps.

| Aðgerðir fastra launa | Virkni                |
|--------------------------------|------------------------------|
| Þrep                           | Í flipanum **Almennt** skal gefa til kynna hvort þessi þrepaaðgerð eigi að færa starfsmenn fram um núll þrep, eitt þrep eða tvö þrep.                                                                                  |
|                                | **0 þrep** - Starfsmaður fær launataxtann fyrir núverandi þrep hans.                                                                                                                      |
|                                | **1 þrep** - Kerfið kannar hvort starfsmaðurinn sé þegar á síðasta viðmiðunarpunkti fyrir sitt stig.                                                                                             |
|                                | **2 skref** - Starfsmaðurinn mun fara fram á við tvö skref á núverandi stigi. Starfsmaður gæti aðeins fært eitt eða núll skref ef hann nær síðasta viðmiðunarpunkti fyrir sitt stig. |

## <a name="run-the-compensation-process"></a>Keyra Launavinnsla
Eftir að vinnslutilvikið hefur verið sett upp með nauðsynlegum dagsetningareitum, áætlunum og aðgerðum skal smella á **Keyra vinnslu** á síðunni **Vinnslutilvik**, þetta opnar gluggann **Keyra tilvik launavinnslu**. Smelltu á valkostinn **Sýna niðurstöður vinnslu** til að sjá hvernig launaupphæðir voru reiknaðar út fyrir hvern starfsmann. Sé smellt á **Í lagi** er launavinnsla keyrð fyrir alla starfsmenn sem eru í þeirri launaáætlun sem er valin frá og með lokadagsetningu ferlis.

## <a name="view-the-process-results"></a>Skoða niðurstöður vinnslu
Til að skoða niðurstöður ferlis opnarðu síðuna **Vinna niðurstöður**. Nýtt launatilvik er stofnað í hvert sinn sem vinnslutilvik er keyrt. Þetta leyfir prufukeyrslur, gerir leiðréttingar og keyrir launatilvikið mörgum sinnum til að komast að því hvort hinar og þessar breytingar hafi áhrif á laun starfsmanns.

Síðan **Vinna niðurstöður** inniheldur upplýsingar um keyrsluna, þar á meðal hvenær keyrslan átti sér stað, notandann sem setti keyrsluna í gang og hvort einhverjar villur komu upp við keyrslu ferlisins. Veldu valkostinn **Læst** til að gera hnappinn **Hlaða laun** óvirkan og koma í veg fyrir að einhver geti hlaðið launatilvikum í starfsmannafærslurnar. Sé smellt á hnappinn **Starfsmannaniðurstöður** birtist listi yfir starfsmenn sem eru með í keyrslunni.

Valkosturinn **Niðurstöður starfsmanna** sýnir upplýsingar um ferlið sjálf, auk allra launaaðgerða sem framkvæmdar voru í ferlinu. Hlutinn **Föst laun** mun innihalda færslu fyrir hverja aðgerð í vinnslutilvikinu fyrir launafyrirkomulagið. Dálkarnir **Gildandi leiðbeining** og **Ráðlegging** munu birta fleiri upplýsingar fyrir aðgerðina sem valin er í hlutanum **Föst laun**. Ef **Virkja ráðleggingar** var merkt fyrir aðgerðina verða reitirnir **Tillaga** breytanlegir. Þetta gerir þér kleift að leiðrétta handvirkt upphæðirnar fyrir starfsmanninn. Athugaðu að ef þú hefur merkt **Nota síðustu niðurstöður** fyrir aðgerðina í vinnslutilvikinu, verður þú að uppfæra handvirkt upphæðirnar í öllum tengdum aðgerðum.

Þegar launaupphæðirnar hafa verið endurskoðaðar fyrir starfsmann og einhverjar leiðréttingar á ráðlögðum gildum hafa verið gerðar, getur þú breytt **Stöðu** í línunni **Starfsmannatilvik** til að gefa til kynna hvort tilvik hafi verið samþykkt eða ætti að hunsa. Einnig er hægt að eyða öllum breytingum sem gerðar eru á ráðleggingum starfsmanns með því að smella á hnappinn **Endurreikna**. Þetta merkir núverandi starfsmannatilvik með stöðunni Hunsa og stofnar nýtt starfsmannatilvik með endurreiknuðum gildum.

## <a name="loading-approved-compensation-changes"></a>Innlestur á launabreytingum samþykktur
Þegar eitt eða fleiri tilvik starfsmanna hafa fengið stöðuna uppfærða í **Samþykkt** er hægt að hlaða þeim í starfsmannafærslur fastra launa. Hægt er að gera þetta annaðhvort með því að velja eitt starfsmannatilvik í einu og smella á hnappinn **Hlaða launum starfsmanns** á síðunni **Niðurstöður starfsmanns**, eða með því að smella á **Hlaða launum** á síðunni **Vinna niðurstöður** til að hlaða öllum samþykktum starfsmannatilvikum í einu.

Sé smellt á **Í lagi** í svarglugganum **Hlaða laun** bætir það launaaðgerðalínum sem eru ekki núll við síðuna **Föst laun starfsmanns**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
