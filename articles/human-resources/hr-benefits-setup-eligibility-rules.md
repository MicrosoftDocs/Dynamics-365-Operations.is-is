---
title: Grunnstilla hæfnireglur og valkosti
description: Þessi grein lýsir því hvernig á að stilla hæfisreglur og valkosti í fríðindastjórnun í Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b4c8cd4e32880df771a4a72237d212e061f849ce
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848253"
---
# <a name="configure-eligibility-rules-and-options"></a>Grunnstilla hæfnireglur og valkosti 


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þegar þú hefur stillt nauðsynlegar færibreytur fyrir fríðindastjórnun geturðu stofnað hæfnireglur, búnt, tímabil og áætlunarpakka sem þú munt tengja við fríðindaáætlanirnar þínar.

Hæfnisreglur eru notaðar til að ákvarða hvort starfsmenn uppfylli skilyrði áætlunar. Starfsmenn þurfa að uppfylla skilyrði a.m.k. einnar reglu til að teljast gjaldgengir fyrir fríðindi. Til dæmis ertu með tvær reglur um áætlun. Fyrsta reglan (lína 1) segir að gerð starfsmanns verði að vera **Starfsmaður**. Önnur reglan (lína 2) segir að starfsmaðurinn verði að vera í fullu starfi. Starfsmenn sem uppfylla reglu 1 eru því gjaldgengir þótt þeir séu einungis í hlutastarfi.

Það er hinsvegar hægt að setja upp eina reglu sem er með mörg skilyrði. Þá þurfa starfsmenn að uppfylla öll skilyrði reglunnar til að teljast gjaldgengir í fríðindum. Til dæmis ertu með reglu sem heitir **Starfsmaður í fullu starfi**. Þessi regla segir að gerð starfsmanns verður að vera **Starfsmaður** *og* starfsmaðurinn verður að vera í fullu starfi. Því þurfa starfsmenn að uppfylla bæði skilyrði reglunnar til að vera gjaldgengir.

> [!IMPORTANT]
> Að minnsta kosti ein hæfnisregla verður að vera tengd við fríðindaáætlun. Hægt er að tengja margar reglur við fríðindi.

## <a name="create-an-eligibility-rule"></a>Stofna hæfnireglu

Hæfisreglur skilgreina hvaða starfsmenn geta skráð sig í hverja bótaáætlun. Eftir að þú hefur skilgreint hæfisreglur, úthlutarðu þeim í fríðindaáætlun. Síðan er hægt að vinna úr hæfi innritunar til að sjá hvaða starfsmenn eru gjaldgengir í hverja áætlun. 

Meðan á opinni innritun stendur geta starfsmenn valið bótaráætlanir. Ef þeir uppfylla ekki skilyrði fríðindaáætlunar miðað við reglur um gjaldgengi eftir að þeir hafa þegar verið skráðir, eru þeir ekki sjálfkrafa afskráðir. Venjulega, þegar viðburður á sér stað sem hefur áhrif á hæfi áætlunar, er byrjað á innritunartímabili fyrir starfsmanninn til að velja áætlanir sem þeir eiga rétt á. 

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Hæfisreglur og valkostir**.

2. Í flipanum **Hæfnisreglur** skal velja **Ný** til að stofna hæfnisreglu. Veldu til að sjá áætlanir sem tengjast hæfisreglu **Meðfylgjandi áætlanir**.

3. Tilgreinið gildi fyrir eftirfarandi reiti.

   | Svæði | lýsing |
   | --- | --- |
   | **Hæfnisregla** | Einkvæmt auðkenni fyrir hæfisregluna. |
   | **Lýsing** | Lýsing á hæfnisreglunni. |
   | **Gildir frá dagsetningu og tíma** | Upphafsdagur hæfisreglunnar. | 
   | **Gildir til dagsetningu og tíma** | Lokadagur hæfisreglunnar. |
   | **Gerð notandastarfsmanns** | Tilgreinir hvort nota eigi gerð starfsmannsins í hæfnisreglu fríðinda. |
   | **Gerð starfskrafts** | Verkamannategundin, ef **Notaðu tegund starfsmanna** rofi er stillt á **Já**. |
   | **Nota stöðu starfsmanns** | Tilgreinir hvort nota eigi ráðningarstöðu starfsmannsins í hæfnisreglu fríðinda. |
   | **Staða** | Starfsmannastaðan, ef **Nota stöðu starfsmanna** rofi er stillt á **Já**. Ef hnappurinn **Nota stöðu starfsmanns** er stilltur á **Nei** er reiturinn ekki notaður. |
   | **Nota starfsgrein** | Tilgreinir hvort nota eigi starfsmannagildið **Starfsgrein** sem hluta af hæfnisreglu fríðinda. | 
   | **Starfsgrein** | Starfsgrein starfsmannsins ef hnappurinn **Nota starfsgrein** er stilltur á **Já**. |
   | **Nota nýja ráðningarreglu** | Tilgreinir hvort nota eigi nýtt gildi ráðningartímabils fyrir nýja ráðningu sem hluta af hæfnisreglu fríðinda. |
   | **Skráningartímabil** | Tímabilið þegar nýskráning á leigu er leyfð. Ef þú stillir þetta einnig í færibreytur, hefur færibreytustillingin forgang fram yfir þessa. |
   | **Nota fyrri stöðu á vinnumarkaði** | Tilgreinir hvort nota eigi fyrri starfsstöðu starfsmanns sem hluta af hæfnisreglu fríðinda. Til dæmis er hægt að tilgreina hæfisreglu sem afsalar biðtíma umfjöllunar fyrir alla starfsmenn sem hafa farið úr stöðunni **Sagt upp** í stöðuna **Ráðin(n)** innan 90 daga frá fyrri atvinnu þeirra. |

4. Undir **Viðbótarskilyrði** skal velja eftirfarandi valkosti og bæta við upplýsingum eftir þörfum.

   | Valkostur | lýsing |
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
   | **Gjaldgengt verkalýðsfélag** | Tilgreinir aðild að verkalýðsfélagi sem fullnægir hæfisreglunni. Til dæmis Forklift Drivers of America.</br></br>Þegar notuð er hæfnisregla stéttarfélags verður stéttarfélagsfærsla starfsmannsins að vera með lokadagsetninguna útfyllta. Ekki má skilja hana eftir auða. |
   | **Hæfur vísir póstnúmers** | Tilgreinir póstnúmerin sem fullnægja hæfisreglunni. Til dæmis 58104. |

5. Undir **Viðbótarupplýsingar** er hægt að skoða eftirfarandi viðbótarupplýsingar.

   | Svæði | lýsing |
   | --- | --- |
   | **Svæði fyrir hæfan notanda** | Tilgreinir viðbótarhæfisreglur byggðar á skilgreindum reitum viðskiptavina. |
   | **Hæfnisgerð** | Tilgreinir viðmiðunarflokkinn sem þú valdir undir **Viðbótarviðmið**. |
   | **Hæfnistilvísun** | Tilgreinir gildin sem þú valdir undir **Viðbótarviðmið**. |
   | **Lýsing** | Lýsingin sem þú valdir undir **Viðbótarviðmið**. |

6. Veldu **Vista**.

## <a name="using-custom-fields-in-eligibility-rules"></a>Nota sérstillta reiti í hæfnireglum

Hægt er að stofna [Sérstillta reiti](hr-developer-custom-fields.md) innan Human Resources til að rekja viðbótarupplýsingar. Þessum reitum er hægt að bæta beint við notendaviðmótið og dálki er bætt við undirliggjandi töflu.  

Hægt er að nota sérstillta reiti í hæfisferlinu. Hæfnisreglur geta notað eitt eða fleiri gildi sérstilltra reita til að ákvarða hæfi starfsmanns.  Til að bæta sérstilltum reit við fyrirliggjandi reglu eða til að stofna nýja reglu skal fara í **Fríðindastjórnun > Tenglar > Uppsetning > Hæfnisreglur > Hæfi sérstillts reitis**. Á þessari síðu er hægt að stofna reglu sem notar einn eða marga sérstillta reiti og hægt er að skilgreina mörg gildi fyrir hvern sérstilltan reit til að ákvarða hæfi.

Eftirfarandi töflur styðja sérsniðna reiti sem hægt er að nota í hæfisvinnslu:

- Starfskraftur (HcmStarfsmaður)  
- Verk (HcmJob)  
- Staða (HcmPosition)  
- Upplýsingar um stöðu (HcmPositionDetail)  
- Stöðuúthlutun starfskrafts  
- Starf (HcmStarf)  
- EmploymentDetails (HcmEmploymentDetails)  
- Upplýsingar um verk (HcmJobDetails)  

Eftirfarandi gerðir sérstilltra reita eru studdar í hæfisferlinu:

- Texti  
- Tínslulisti  
- Númer  
- Tugabrot  
- Gátreitur  

Eftirfarandi tafla sýnir sérsniðnar reitaupplýsingar um gjaldgengi eyðublaðsins.

| Svæði  | lýsing |
|--------|-------------|
| Nafn | Heiti skilyrðanna sem verið er að stofna. |
| Töfluheiti | Töfluheitið sem inniheldur sérsniðna reitinn sem verið er að nota fyrir hæfnisregluna. |
| Heiti reits | Reiturinn sem verður notaður fyrir hæfnisregluna. |
| Gerð virkja | Sýnir virknitáknið sem er notað í skilgreiningu á hæfi sérstillts reits. |
| Virði | Sýnir gildið sem er notað í skilgreiningu á hæfi sérstillts reits. |

## <a name="eligibility-logic"></a>Hæfisregla

Eftirfarandi hlutar útskýra hvernig unnið er úr hæfi fríðinda.

### <a name="rules-assigned-to-a-plan"></a>Reglum úthlutað á áætlun 
Þegar mörgum hæfisreglum er úthlutað á fríðindaáætlun verður starfsmaður að uppfylla að minnsta kosti eina reglu sem á að vera gjaldgengur í fríðindaáætluninni.  Í eftirfarandi dæmi verður starfsmaðurinn annaðhvort að uppfylla kröfur reglunnar **Starfsgerð** eða reglunnar **Virkir starfsmenn**.

![Starfsmaðurinn þarf annaðhvort að uppfylla kröfur starfagerðarinnar eða regluna um virka starfsmenn.](media/RulesAssignedToAPlan.png)
 
### <a name="criteria-within-an-eligibility-rule"></a>Skilyrði í gjaldgengisreglu 
Innan reglu eru skilyrði reglunnar skilgreind. Í dæminu hér að ofan eru viðmið reglunnar **Starfsgerð** þar sem starfsgerð = Stjórnendur. Því verður starfsmaðurinn að vera stjórnandi til að vera gjaldgengur. Þetta er regla þar sem aðeins eitt skilyrði er til staðar innan reglunnar.

Hægt er að tilgreina reglur með mörgum skilyrðum. Þegar mörg skilyrði eru skilgreind í hæfnisreglu verður starfsmaður að uppfylla öll skilyrðin í reglunni til að hafa rétt á fríðindaáætluninni. 

Til dæmis er reglan **Virkir starfsmenn** að ofan gerð úr eftirfarandi skilyrði. Til að starfsmaðurinn geti verið gjaldgengur samkvæmt reglunni **Virkir starfsmenn** verður starfsmaðurinn að vera ráðinn í lögaðila USMF *og* vera með starfsstöðuna fullt starf.  

![Skilyrði í gjaldgengisreglu.](media/CriteriaWithinAnEligibilityRule.png) 
 
### <a name="multiple-conditions-within-criteria"></a>Mörg skilyrði innan viðmiða

Það er hægt að útvíkka reglurnar enn frekar til að nota mörg skilyrði innan eins skilyrðis. Starfsmaðurinn verður að uppfylla minnst eitt skilyrði til að vera gjaldgengur. Til að nota dæmið hér að ofan er hægt að útvíkka regluna **Virkir starfsmenn** enn frekar til að taka einnig með starfsmenn sem eru ráðnir í hlutastarf. Þess vegna verður starfsmaðurinn nú að vera starfsmaður í USMF *og* annaðhvort starfsmaður í fullu starfi eða í hlutastarfi.  

![Mörg skilyrði innan viðmiðs.](media/MultipleConditionsWithinCriteria.png) 
 
### <a name="eligibility-conditions-within-a-custom-field-criterion"></a>Hæfnisskilyrði innan viðmiðs sérstillts reits 
Svipað og hér að ofan er hægt að nota sérstillta reiti þegar hæfnisreglur og vinna er búið til á sama hátt. Til dæmis gæti verið gott að bjóða starfsmönnum í Fargo og Kaupmannahöfn sem vinna heima fyrir endurgreiðslu á netinu, þar sem netkostnaður er hærri á þeim stöðum. Til að gera þetta skal búa til tvo sérstillta reiti: **Staðsetning skrifstofu** (tínslulisti) og **Vinn heima** (gátreitur). Búa síðan til reglu sem nefnist **Starfsmenn WFH**. Skilyrðið fyrir regluna er þar sem **Staðsetning skrifstofu = Fargo** eða **Kaupmannahöfn** *og* þar sem **Vinn heima = Já**.

Setja þyrfti upp sérstilltar hæfnisreglur eins og gefið er til kynna á eftirfarandi mynd. 

![Hæfnisskilyrði innan skilyrðis sérstillts reits.](media/EligibilityConditionsWithinACustomFieldCriterion.png) 
 
## <a name="configure-bundles"></a>Skilgreina búnt

Búnt eru mengi tengdra bótaáætlana. Þú getur notað bótaknippi til að hópa bótakerfi sem starfsmaður verður að velja til að skrá sig í tilteknar bæturáætlanir sem geta verið háðar öðrum skráningum í bótakerfi. Dæmi um hvenær þú vilt kannski nota búnt eru:

- Búnt heilbrigðisáætlunar sem inniheldur mikla frádráttarbærar sjúkratryggingar með tilheyrandi heilsusparnaðarreikningi (HSA).

- Líftryggingaráætlun með lögboðinni líftryggingaráætlun starfsmanna ásamt lífeyrisáætlun. Þetta myndi tryggja að starfsmaður geti ekki valið háð lífskjör án þess að skrá sig í umfjöllun starfsmannsins.

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Hæfisreglur og valkostir**.

2. Í **Búnt** flipann, veldu **Nýtt** til að búa til búnt. Veldu til að sjá áætlanir sem tengjast búnti **Meðfylgjandi áætlanir**.

3. Tilgreinið gildi fyrir eftirfarandi reiti.

   | Svæði | lýsing |
   | --- | --- |
   | **Búnt** | Einkvæmt kennimerki fyrir búntið. |
   | **Lýsing** | Lýsing á búnti. |
   | **Næstefsta stig** | Gefur til kynna hvort eitt af áætlunum í búntinu verði að vera merkt sem aðalskipulagið. Velja skal aðaláætlunina við opna skráningu sem hluta af búntinu áður en stjórnandi fríðinda getur staðfest fríðindaval starfsmannsins. |
   | **Gildir frá dagsetningu og tíma** | Dagsetning og tími þegar búntið verður virkt. |
   | **Gildir til** | Dagsetningin sem búntið rennur út. Sjálfgildið er 12/31/2154, sem táknar aldrei. |

4. Veljið **Vista**.

## <a name="configure-periods"></a>Grunnstilla tímabil

Tímabil skilgreina hvenær fríðindi eru í gildi og hvenær starfsmenn mega skrá sig. Þú getur búið til eins mörg tímabil og þú vilt til að viðhalda opinni innskráningu fríðnda og umfjöllunar á tímabili. Fríðindaáætlunarár fylgja kannski ekki almanaksári. 

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Hæfisreglur og valkostir**.

2. Í **Tímabil** flipann, veldu **Nýtt** til að búa til tímabil. Veldu til að keyra ferli sem tengir allar gildar virkar fríðindaáætlanir við bótatímabilið **Hengdu við áætlanir**. Veldu til að sjá áætlanir sem tengjast búnti **Meðfylgjandi áætlanir**. 

3. Tilgreinið gildi fyrir eftirfarandi reiti.

   | Svæði | lýsing |
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

Þú getur notað flex kredit forrit til að skrá starfsmenn í bætur samkvæmt fyrirfram ákveðnum fjölda sveigjanlegra eininga. Starfsmenn geta valið hvernig þeir eiga að úthluta sveigjanlegum einingum. Ef starfsmaður er til dæmis tryggður í sjúkratryggingu maka síns gæti hann viljað nota inneignina sem hann hefði annars notað í sjúkratryggingu í önnur fríðindi.

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Hæfisreglur og valkostir**.

2. Í **Tímabil** flipann, veldu **Flex lánstraust forrit**.

3. Veldu flex kredit forrit til að sækja um. Reitirnir innihalda eftirfarandi upplýsingar.

   | Svæði | lýsing |
   | --- | --- |
   | **Auðkenni fríðindaútgjalda** | Einstakt auðkenni Flex Credit áætlunarinnar. |
   | **Lýsing** | Lýsing á flex kredit forritinu. | 
   | **Dagsetning frá** | Dagsetningin þegar flex-lánsfjáráætlunin verður virk. |
   | **Lokadagsetning** | Lokadagsetningin þegar flex-lánsfjáráætlunin. Þú getur skilið sjálfgefna gildið eftir (12/31/2154) til að gefa til kynna að áætlunarpakki sveigjanlegrar inneignar sé ekki með áætlaðan gildistíma. |
   | **Útgjaldavirði samtals** | Fjöldi eininga sem hver starfsmaður verður að nota fyrir fríðindi sín. |
   | **Hlutfallsskiptaregla** | Reglan sem nota á til að pródata flex-einingar þegar starfsmaður er ráðinn á miðju flex-lánstímabilinu. </br></br><ul><li>**Enginn** - Starfsmaðurinn fær engin sveigjanleiki ef þeir eru ráðnir eftir að tímabil lánsfjárlána hefst.</li><li>**Full inneign** - Starfsmaðurinn fær alla upphæð sveigjanlegra eininga, óháð því hvenær þeir eru ráðnir.</li><li>**Hlutfallsskipta** - Starfsmaðurinn fær hlutfallslegt magn af flex-einingum miðað við upphafsdag.</li></ul> |
   | **Hlutfallsskiptaformúla sveigjanlegra útgjalda** | Reglan sem nota á til að pródata flex-einingar fyrir starfsmenn sem eru ráðnir á miðju fríðindatímabili fyrir flex-lánstímabilið. Ræktunin byggist á upphafsdegi ráðningarinnar. Þessi reitur er aðeins notaður ef þú velur það **Hlutfallsskipta** í reitnum **Hlutfallsregla**. </br></br><ul><li>**Daglega** - Hlutfallsskiptir fjölda sveigjanlegra eininga sem starfsmaður fær til dags. Heildarfjöldi sveigjanlegra eininga er deilt með fjölda daga á tímabilinu. Til dæmis, ef fríðindatímabil þitt er 400 dagar, mun kerfið skipta heildarfjölda sveigjanlegra eininga um 400 til að reikna út fjölda sveigjanlegra eininga sem starfsmenn fá á dag.</li><li>**Núverandi mánuður** - Hlutfallsskiptir fjölda sveigjanlegra eininga sem starfsmaður fær til mánaðarstigs, námundaður að núverandi mánuði. Heildarfjöldi sveigjanlegra eininga er deilt með fjölda mánaða á tímabilinu. Til dæmis, ef fríðindatímabil þitt er 15 mánuðir, mun kerfið skipta heildarfjölda sveigjanlegra eininga um 15 til að reikna út fjölda sveigjanlegra eininga sem starfsmenn fá á mánuði.</li><li>**Næsti mánuður** - Hlutfallsskiptir fjölda sveigjanlegra eininga sem starfsmaður fær til mánaðarstigs, námundaður að næsta mánuði. Heildarfjöldi sveigjanlegra eininga er deilt með fjölda mánaða á tímabilinu. Til dæmis, ef fríðindatímabil þitt er 15 mánuðir, skiptir kerfið heildarfjölda sveigjanlegra eininga um 15 til að reikna út fjölda sveigjanlegra eininga sem starfsmenn fá á mánuði.</li></ul> |
   
   Vertu viss um að hver bótaáætlun er skráð í aðeins eitt flex-lánakerfi á hverju bótatímabili. Að öðrum kosti veit kerfið ekki hvaða áætlunarpakka sveigjanlegrar inneignar eigi að nota til að bjóða upp á sveigjanlega inneign og vandamál munu koma upp. 

## <a name="configure-programs"></a>Stilla forrit

Forrit eru sett af fríðindaáætlunum sem deila sameiginlegu setti hæfisreglna. Þú getur skilgreint hæfisreglur fyrir allt forritið í staðinn fyrir hverja einstaka áætlun. Sem dæmi má nefna FTE-áætlun Contoso Kanada eða framkvæmdarstig Contoso Europe. 

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Hæfisreglur og valkostir**.

2. Í **Áætlanir** flipann, veldu **Nýtt** til að búa til áætlun. Veldu til að gera undantekningar fyrir starfsmenn sem uppfylla ekki kröfur um hæfisreglur **Hæfnisregla hnekkt**. Veldu til að sjá áætlanir sem tengjast áætlun **Meðfylgjandi áætlanir**.

3. Tilgreinið gildi fyrir eftirfarandi reiti.

   | Svæði | lýsing |
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
