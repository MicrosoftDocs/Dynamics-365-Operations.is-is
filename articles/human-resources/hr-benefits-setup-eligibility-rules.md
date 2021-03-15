---
title: Grunnstilla hæfnireglur og valkosti
description: Settu hæfisreglur og valkosti í fríðindastjórnun hjá Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2920a03eaec226b306d03ebf8b899113128c410e
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112951"
---
# <a name="configure-eligibility-rules-and-options"></a>Grunnstilla hæfnireglur og valkosti

Eftir að þú hefur stillt nauðsynlegar breytur fyrir fríðindastjórnun í Microsoft Dynamics 365 Human Resources, getur þú búið til hæfisreglur, knippi, tímabil og forrit sem þú verður að tengja við fríðindaáætlanir þínar.

## <a name="create-an-eligibility-rule"></a>Stofna hæfnireglu

Hæfisreglur skilgreina hvaða starfsmenn geta skráð sig í hverja bótaáætlun. Eftir að þú hefur skilgreint hæfisreglur, úthlutarðu þeim í fríðindaáætlun. Síðan er hægt að vinna úr hæfi innritunar til að sjá hvaða starfsmenn eru gjaldgengir í hverja áætlun. 

Meðan á opinni innritun stendur geta starfsmenn valið bótaráætlanir. Ef þeir eru ekki gjaldgengir í bótaáætlun sem byggist á hæfisreglum eftir að þeir eru þegar skráðir, eru þeir ekki sjálfkrafa skráðir. Venjulega, þegar viðburður á sér stað sem hefur áhrif á hæfi áætlunar, er byrjað á innritunartímabili fyrir starfsmanninn til að velja áætlanir sem þeir eiga rétt á. 

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Hæfisreglur og valkostir**.

2. Í **Reglur um hæfi** flipann, veldu **Nýtt** til að búa til hæfisreglu. Veldu til að sjá áætlanir sem tengjast hæfisreglu **Meðfylgjandi áætlanir**.

3. Tilgreina gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- |
   | **Hæfnisregla** | Einkvæmt auðkenni fyrir hæfisregluna. |
   | **Lýsing** | Lýsing á hæfnisreglunni. |
   | **Gildir frá dagsetningu og tíma** | Upphafsdagur hæfisreglunnar. | 
   | **Gildir til dagsetningu og tíma** | Lokadagur hæfisreglunnar. |
   | **Gerð notandastarfsmanns** | Tilgreinir hvort nota eigi starfsmann starfsmannsins tegund hæfisreglunnar. |
   | **Gerð starfskrafts** | Verkamannategundin, ef **Notaðu tegund starfsmanna** rofi er stillt á **Já**. |
   | **Nota stöðu starfsmanns** | Tilgreinir hvort nota eigi starfsstöðu starfsmannsins í hæfisreglu fríðinda. |
   | **Staða** | Starfsmannastaðan, ef **Nota stöðu starfsmanna** rofi er stillt á **Já**. Ef **Nota stöðu starfsmanna** rofi er stillt á **Nei** er reiturinn ekki notaður. |
   | **Nota starfsgrein** | Tilgreinir hvort nota eigi gildi starfsmannsins **Atvinnuflokkur** sem hluta af hæfisreglu fríðinda. | 
   | **Starfsgrein** | Starfsmannaflokkur starfsmanns ef **Notaðu atvinnuflokk** rofi er stillt á **Já**. |
   | **Nota nýja ráðningarreglu** | Tilgreinir hvort nota eigi nýtt gildi leigutíma á nýjum leigutíma sem hluta af hæfisreglunni fyrir bætur. |
   | **Skráningartímabil** | Tímabilið þegar nýskráning á leigu er leyfð. Ef þú stillir þetta einnig í færibreytur, hefur færibreytustillingin forgang fram yfir þessa. |
   | **Nota fyrri stöðu á vinnumarkaði** | Tilgreinir hvort nota eigi fyrri atvinnustöðu starfsmanns sem hluta af hæfisreglu fríðinda. Til dæmis er hægt að tilgreina hæfisreglu sem afsalar biðtíma umfjöllunar fyrir alla starfsmenn sem hafa farið úr stöðunni **Sagt upp** í stöðuna **Ráðin(n)** innan 90 daga frá fyrri atvinnu þeirra. |

4. Undir **Viðbótarviðmið**, veldu eftirfarandi valkosti og bættu við upplýsingum eftir þörfum:

   | Valkostur | Lýsing |
   | --- | --- |
   | **Gjaldgengur aldur** | Tilgreinir aldursbil eða svið sem þarf til að fullnægja hæfisreglunni. |
   | **Gjaldgeng deild** | Tilgreinir þá deild eða deildir sem starfsmaður þarf að vera í til að fullnægja hæfisreglunni. |
   | **Gjaldgeng störf** | Tilgreinir þá starfsgerð eða -gerðir sem starfsmaður þarf að vera flokkaður í til að fullnægja hæfisreglunni. Til dæmis í fullu starfi eða hlutastarfi. |
   | **Gjaldgengt starf** | Tilgreinir starfið eða störfin sem fullnægja hæfisreglunni. Störf eru tengd stöðum og stöður útfylltar af starfsmönnum. |
   | **Gjaldgengt starfshlutverk** | Tilgreinir starfshlutverk sem fullnægja hæfisreglu. Til dæmis sölumenn eða tæknimenn. |
   | **Gjaldgengt starfagerð** | Tilgreinir starfsgerð eða -gerðir sem fullnægja hæfisreglunni. Til dæmis ritari eða framkvæmdastjóri. |
   | **Gjaldgengur lögaðili** | Tilgreinir lögaðila eða lögaðila sem gilda fyrir hæfisregluna. Til dæmis Contoso Entertainment System USA. |
   | **Gjaldgengt launasvæði** | Tilgreinir staðsetningu starfsmanns sem fullnægir hæfisreglunni. Til dæmis, central US. |
   | **Gjaldgeng staða** | Tilgreinir starfsstöðu eða -stöður sem fullnægja hæfisreglunni. Til dæmis HR aðstoðarmaður eða HR framkvæmdastjóri. |
   | **Gjaldgengar starfstöður** | Tilgreinir stöðugerð eða -gerðir sem fullnægja hæfisreglunni. Til dæmis í fullu starfi. |
   | **Hæft ástand** | Tilgreinir fylki eða héruð sem fullnægja hæfisreglunni. Til dæmis Norður-Dakóta í Bandaríkjunum eða Breska Kólumbía, Kanada. |
   | **Gjaldgengir ráðningarskilmálar** | Tilgreinir ráðningarskilmála sem fullnægja hæfisreglunni. Til dæmis, að vild eða hópsamningur. |
   | **Gjaldgengt verkalýðsfélag** | Tilgreinir aðild að verkalýðsfélagi sem fullnægir hæfisreglunni. Til dæmis Forklift Drivers of America. </br></br>Þegar nothæfisregla sem byggir á stéttarfélagi er notuð verður verkalýðsfélagaskrá að hafa lokadaginn byggð. Þú getur ekki skilið það eftir autt. |
   | **Hæfur vísir póstnúmers** | Tilgreinir póstnúmerin sem fullnægja hæfisreglunni. Til dæmis 58104. |

5. Undir **Viðbótarupplýsingar**, geturðu skoðað eftirfarandi viðbótarupplýsingar:

   | Svæði | Lýsing |
   | --- | --- |
   | **Svæði fyrir hæfan notanda** | Tilgreinir viðbótarhæfisreglur byggðar á skilgreindum reitum viðskiptavina. |
   | **Hæfnisgerð** | Tilgreinir viðmiðunarflokkinn sem þú valdir undir **Viðbótarviðmið**. |
   | **Hæfnistilvísun** | Tilgreinir gildin sem þú valdir undir **Viðbótarviðmið**. |
   | **Lýsing** | Lýsingin sem þú valdir undir **Viðbótarviðmið**. |

6. Veljið **Vista**.

## <a name="configure-bundles"></a>Skilgreina búnt

Búnt eru mengi tengdra bótaáætlana. Þú getur notað bótaknippi til að hópa bótakerfi sem starfsmaður verður að velja til að skrá sig í tilteknar bæturáætlanir sem geta verið háðar öðrum skráningum í bótakerfi. Dæmi um hvenær þú vilt kannski nota búnt eru:

- Búnt heilbrigðisáætlunar sem inniheldur mikla frádráttarbærar sjúkratryggingar með tilheyrandi heilsusparnaðarreikningi (HSA).

- Líftryggingaráætlun með lögboðinni líftryggingaráætlun starfsmanna ásamt lífeyrisáætlun. Þetta myndi tryggja að starfsmaður geti ekki valið háð lífskjör án þess að skrá sig í umfjöllun starfsmannsins.

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Hæfisreglur og valkostir**.

2. Í **Búnt** flipann, veldu **Nýtt** til að búa til búnt. Veldu til að sjá áætlanir sem tengjast búnti **Meðfylgjandi áætlanir**.

3. Tilgreina gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- |
   | **Búnt** | Einkvæmt kennimerki fyrir búntið. |
   | **Lýsing** | Lýsing á búnti. |
   | **Næstefsta stig** | Gefur til kynna hvort eitt af áætlunum í búntinu verði að vera merkt sem aðalskipulagið. Velja þarf aðalskipulagið við opna skráningu sem hluta af búntinu áður en bótarekandinn getur staðfest fríðindaval starfsmannsins. |
   | **Gildir frá dagsetningu og tíma** | Dagsetning og tími þegar búntið verður virkt. |
   | **Gildir til** | Dagsetningin sem búntið rennur út. Sjálfgildið er 12/31/2154, sem táknar aldrei. |

4. Veljið **Vista**.

## <a name="configure-periods"></a>Grunnstilla tímabil

Tímabil skilgreina hvenær fríðindi eru í gildi og hvenær starfsmenn mega skrá sig. Þú getur búið til eins mörg tímabil og þú vilt til að viðhalda opinni innskráningu fríðnda og umfjöllunar á tímabili. Fríðindaáætlunarár fylgja kannski ekki almanaksári. 

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Hæfisreglur og valkostir**.

2. Í **Tímabil** flipann, veldu **Nýtt** til að búa til tímabil. Veldu til að keyra ferli sem tengir allar gildar virkar fríðindaáætlanir við bótatímabilið **Hengdu við áætlanir**. Veldu til að sjá áætlanir sem tengjast búnti **Meðfylgjandi áætlanir**. 

3. Tilgreina gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- |
   | **Tímabil** | Einkvæmt kenni fyrir tíma. |
   | **Gildir frá dagsetningu og tíma** | Upphafsdagur og tími þegar bótatímabilið er virkt. |
   | **Gildir til dagsetningu og tíma** | Dagur og tími þegar bótatímabilið verður virkt. |
   | **Upphaf skráningar** | Upphafsdagsetning fyrir opna innskráningu. Opin innritun er þegar starfsmaður getur boðið kjör í sjálfsafgreiðslu. |
   | **Lok skráningar** | Lokadagsetning fyrir opna innskráningu. |
   | **Opnar** | Gefur til kynna hvort tímabilið sé opið miðað við kerfisdagsetningu og gildir frá og til dagsetningar og tíma. | 
   | **Fyrra tímabil** | Tilgreinir bótatímabilið sem er á undan völdum bótatímabili. Þessar upplýsingar eru notaðar við skráningu bótahæfileika til að úthluta áætlunum, umfjöllunarvalkostum og tilmælendum frá fyrra ári. |
 
4. Veljið **Vista**.

## <a name="use-a-flex-credit-program"></a>Nota sveigjanlega útgjaldaáætlun

Þú getur notað flex kredit forrit til að skrá starfsmenn í bætur samkvæmt fyrirfram ákveðnum fjölda sveigjanlegra eininga. Starfsmenn geta valið hvernig þeir eiga að úthluta sveigjanlegum einingum. Til dæmis, ef starfsmaður fellur undir sjúkratryggingaráætlun maka síns, gæti verið að hann vilji nota inneignina sem þeir hefðu annars notað á heilsuvernd gagnvart öðrum bótum.

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Hæfisreglur og valkostir**.

2. Í **Tímabil** flipann, veldu **Flex lánstraust forrit**.

3. Veldu flex kredit forrit til að sækja um. Reiturinn inniheldur eftirfarandi upplýsingar:

   | Svæði | Lýsing |
   | --- | --- |
   | Auðkenni fríðindaútgjalda | Einstakt auðkenni Flex Credit áætlunarinnar. |
   | Lýsing | Lýsing á flex kredit forritinu. | 
   | Dagsetning frá | Dagsetningin þegar flex-lánsfjáráætlunin verður virk. |
   | Lokadagsetning | Lokadagsetningin þegar flex-lánsfjáráætlunin. Þú getur skilið eftir sjálfgefið gildi (12/31/2154) til að gefa til kynna að flex kredit forritið sé ekki með áætlaðan lokun. |
   | Útgjaldavirði samtals | Fjöldi eininga sem hver starfsmaður verður að nota fyrir fríðindi sín. |
   | Hlutfallsskiptaregla | Reglan sem nota á til að pródata flex-einingar þegar starfsmaður er ráðinn á miðju flex-lánstímabilinu. </br></br><ul><li>**Enginn** - Starfsmaðurinn fær engin sveigjanleiki ef þeir eru ráðnir eftir að tímabil lánsfjárlána hefst.</li><li>**Full inneign** - Starfsmaðurinn fær alla upphæð sveigjanlegra eininga, óháð því hvenær þeir eru ráðnir.</li><li>**Hlutfallsskipta** - Starfsmaðurinn fær hlutfallslegt magn af flex-einingum miðað við upphafsdag.</li></ul> |
   | Hlutfallsskiptaformúla sveigjanlegra útgjalda | Reglan sem nota á til að pródata flex-einingar fyrir starfsmenn sem eru ráðnir á miðju fríðindatímabili fyrir flex-lánstímabilið. Ræktunin byggist á upphafsdegi ráðningarinnar. Þessi reitur er aðeins notaður ef þú velur það **Hlutfallsskipta** í reitnum **Hlutfallsregla**. </br></br><ul><li>**Daglega** - Hlutfallsskiptir fjölda sveigjanlegra eininga sem starfsmaður fær til dags. Heildarfjöldi sveigjanlegra eininga er deilt með fjölda daga á tímabilinu. Til dæmis, ef fríðindatímabil þitt er 400 dagar, mun kerfið skipta heildarfjölda sveigjanlegra eininga um 400 til að reikna út fjölda sveigjanlegra eininga sem starfsmenn fá á dag.</li><li>**Núverandi mánuður** - Hlutfallsskiptir fjölda sveigjanlegra eininga sem starfsmaður fær til mánaðarstigs, námundaður að núverandi mánuði. Heildarfjöldi sveigjanlegra eininga er deilt með fjölda mánaða á tímabilinu. Til dæmis, ef fríðindatímabil þitt er 15 mánuðir, mun kerfið skipta heildarfjölda sveigjanlegra eininga um 15 til að reikna út fjölda sveigjanlegra eininga sem starfsmenn fá á mánuði.</li><li>**Næsti mánuður** - Hlutfallsskiptir fjölda sveigjanlegra eininga sem starfsmaður fær til mánaðarstigs, námundaður að næsta mánuði. Heildarfjöldi sveigjanlegra eininga er deilt með fjölda mánaða á tímabilinu. Til dæmis, ef fríðindatímabil þitt er 15 mánuðir, skiptir kerfið heildarfjölda sveigjanlegra eininga um 15 til að reikna út fjölda sveigjanlegra eininga sem starfsmenn fá á mánuði.</li></ul> |
   
   Vertu viss um að hver bótaáætlun er skráð í aðeins eitt flex-lánakerfi á hverju bótatímabili. Annars mun kerfið ekki vita hvaða flex credit forrit sem á að nota til að veita flex credits og þú lendir í vandræðum. 

## <a name="configure-programs"></a>Stilla forrit

Forrit eru sett af fríðindaáætlunum sem deila sameiginlegu setti hæfisreglna. Þú getur skilgreint hæfisreglur fyrir allt forritið í staðinn fyrir hverja einstaka áætlun. Sem dæmi má nefna FTE-áætlun Contoso Kanada eða framkvæmdarstig Contoso Europe. 

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Hæfisreglur og valkostir**.

2. Í **Áætlanir** flipann, veldu **Nýtt** til að búa til áætlun. Veldu til að gera undantekningar fyrir starfsmenn sem uppfylla ekki kröfur um hæfisreglur **Hæfnisregla hnekkt**. Veldu til að sjá áætlanir sem tengjast áætlun **Meðfylgjandi áætlanir**.

3. Tilgreina gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- |
   | **Áætlun** | Einkvæmt auðkenni fyrir áætlunina. |
   | **Lýsing** | Lýsing á áætluninni. | 
   | **Gildir frá dagsetningu og tíma** | Dagsetning og tími þegar áætlunin verður virk. |
   | **Gildir til dagsetningu og tíma** | Dagsetning og tími þegar áætlunin rennur út. Sjálfgildið er 12/31/2154, sem táknar aldrei. |
   | **Biðtími tryggingar** | Tímabilið sem starfsmaður verður að bíða áður en umfjöllun hefst vegna bótaáætlunarinnar. |
   | **Biðtími frádráttar** | Tímabilið sem starfsmaður bíður áður en frádráttur hefst vegna bótaáætlunarinnar. |
   | **Hæfnisreglur** | Veldu hæfisreglur sem eiga við um bótakerfið. Þú skilgreinir hæfisreglur á **Reglur um hæfi** flipann á þessari síðu. |
   
4. Veljið **Vista**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]