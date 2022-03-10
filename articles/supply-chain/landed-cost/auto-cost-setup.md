---
title: Uppsetning sjálfvirks kostnaðar
description: Þetta efnisatriði lýsir því hvernig setja á upp kostnaðarreglur fyrir mismunandi ferðastig á innleið. Á grundvelli þessara reglna reiknar kerfið út kostnað og bætir þeim sjálfkrafa við. Því þurfa notendur ekki að bæta kostnaði við handvirkt.
author: sherry-zheng
ms.date: 01/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMCostAutoSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-21
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 0fe795127300ac99c3f5ee65cb1f6e0841ad4d95
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575801"
---
# <a name="auto-costs-setup"></a>Uppsetning sjálfvirks kostnaðar

[!include [banner](../../includes/banner.md)]

Hægt er að nota síðuna **Sjálfvirkur kostnaður** til að setja upp kostnaðarreglur fyrir ýmsa kostnaðarþætti (t.d. ferðir, sendingu, gáma, fólíó, innkaupapantanir, vörur eða flutningspöntunarlínur). Út frá reglunum og reitunum sem notendur velja þegar þeir stofna færslur fyrir einn kostnaðarþáttinn mun kerfið reikna kostnaðinn og bæta honum sjálfkrafa við. Því þurfa notendur ekki að bæta kostnaði við handvirkt.

Til að vinna með sjálfvirkan kostnað er farið í **Heildarkostnaður \> Kostnaðaruppsetning \> Sjálfvirkur kostnaður**. Setjið síðan upp sjálfvirkrar kostnaðarreglur eins og lýst er hér á eftir.

## <a name="work-with-cost-areas"></a>Unnið með kostnaðarþætti

Sjálfvirkur kostnaður virkar eins og viðskiptasamningar og ýmis gjöld. Sérhver færsla sjálfvirk kostnaðar tilheyrir tilteknu kostnaðarstigi. Notið reitinn **Kostnaðarþáttur** á listasvæðinu á síðunni **Sjálfvirkur kostnaður** til að velja kostnaðarþáttinn sem ætlunin er að vinna með. Listasvæðið sýnir aðeins sjálfvirkan kostnað sem tilheyrir valda kostnaðarsvæðinu. Allur sjálfvirkur kostnaður sem er stofnaður mun tilheyra kostnaðarsvæðinu sem er valið.

Kostnaðarþættir gera kerfinu kleift að skipta kostnaði niður á innkaupapöntunarlínur í kostnaðarþætti. Til dæmis mun kostnaður fyrir einn gám skipta virðinu niður á allar afurðir í flutningsgámnum. Ef um er að ræða tvo eða fleiri gáma er hægt að tilgreina sömu kostnaðargerðina fyrir hvern gám. Þess vegna er hægt að nota gámagerðina til að finna réttan sjálfvirkan kostnað.

## <a name="buttons-on-the-action-pane"></a>Hnappar á aðgerðasvæðinu

Eftirfarandi tafla lýsir þeim hnöppum sem eru á aðgerðarúnunni **Sjálfvirkur kostnaður** síðunnar.

| Hnappur | lýsing |
|---|---|
| Breyta | Breyta fyrirliggjandi sjálfvirkum kostnaði. |
| Nýjar | Búa til sjálfvirkan kostnað. |
| Eyða | Eyða sjálfvirkum kostnaði. |
| Afrita úr | Stofnið nýja færslu fyrir sjálfvirkan kostnað sem byggir á fyrirliggjandi færslu. Svo er hægt að breyta nýju færslunni. Þessi hnappur hjálpar til við að stofna nýjan sjálfvirkan kostnað á fljótlegan hátt. |
| Sýna víddir | Opnið svarglugga þar sem hægt er að velja birgðavíddirnar sem eru sýndar fyrir kostnaðarfærslurnar sem eru skoðaðar. Ef gátreitir eru hreinsaðir birtast færri birgðavíddir fyrir kostnaðarfærslurnar. Þess vegna verða minni upplýsingar sýndar fyrir færsluna. Ef birgðavídd er tilgreind fyrir sjálfvirkan kostnað verður sjálfvirkur kostnaður aðeins notaður þegar tilgreind birgðavídd er notuð fyrir vöruna á ferð. |

## <a name="settings-on-the-header"></a>Stillingar á hausnum

Samsetning stillinganna í haushlutanum ákvarðar hvenær og hvernig tilteknum sjálfvirkum kostnaði er bætt við ferð. Sjálfvirkur kostnaður verður aðeins notaður í ferð, flutningsgám eða fólíó þegar upplýsingar um sjálfvirkan kostnað passa við upplýsingarnar í haus þess kostnaðarþáttar. Samtala alls samsvarandi sjálfvirks kostnaðs ákvarðar áætlaðan heildarkostnað ferðar. Þessum kostnaði er skipt á milli allra varanna í skipinu eða í ferðinni.

Eftirfarandi tafla lýsir öllum reitum sem geta birst í haushlutanum. Hins vegar eru tilteknir reitir sem eru í boði breytilegir eftir því hver kostnaðarþátturinn er og birtar víddir sem eru valdar.

| Svæði | lýsing |
|---|---|
| **Kóði lykils** | <p>Veljið eitt af eftirfarandi gildum:</p><ul><li>**Tafla** – Kostnaðarreglan á aðeins við um tiltekinn lánardrottin.</li><li>**Flokkur** – Kostnaðarreglan gildir fyrir tiltekinn lánardrottnaflokk. Kerfið mun leita að [kostnaðargerðarflokki lánardrottins](costing-parameters-setup.md) sem tengist lánardrottnafærslunni.</li><li>**Allt** – Kostnaðarreglan gildir fyrir alla lánardrottna. |
| **Flutningsfyrirtæki** | Veljið lánardrottin eða lánardrottnaflokk sem kostnaðarreglan gildir um. Þessi reitur er aðeins tiltækur ef *Tafla* eða *Flokkur* er valið í reitnum **Kóði lykils**. |
| **Tollmiðlari** | Veljið lánardrottin eða lánardrottnaflokk sem kostnaðarreglan gildir um. Þessi reitur er aðeins tiltækur ef *Tafla* eða *Flokkur* er valið í reitnum **Kóði lykils**. |
| **Vörukóði** | <p>Veljið eitt af eftirfarandi gildum:</p><ul><li>**Tafla** – Kostnaðarreglan á aðeins við um tiltekna vöru.</li><li>**Flokkur** – Kostnaðarreglan gildir fyrir tiltekinn vöruflokk. Kerfið mun leita að [kostnaðargerðarflokki vöru](costing-parameters-setup.md) sem tengist vörufærslu.</li><li>**Allt** – Kostnaðarreglan gildir fyrir allar vörur.|
| **Vöruvensl** | Veljið vöruna eða vöruflokkinn sem kostnaðarreglan á við um. Þessi reitur er aðeins tiltækur ef *Tafla* eða *Flokkur* er valið í reitnum **Vörukóði**. |
| **Afhendingarmáti** | Veljið afhendingarmáta (svo sem í lofti eða á sjó) sem kostnaðarreglan gildir um. |
| **Tegund gáms** | Gerð gámsins sem varningurinn verður sendur í. Aðeins er hægt að nota sjálfvirkan kostnað á ferð ef gámagerðin í uppsetningu sjálfvirks kostnaðar passar við gámagerð ferðarinnar. |
| **Frá höfn** og **Til hafnar** | Upprunahöfn („frá“) og áfangahöfn („til“) í ferðinni. (Sumir flutningsgámar gætu verið með mismunandi „til“ höfn vegna þess að ferðin gæti haft viðdvöl í mörgum höfnum.) Hægt er að nota sjálfvirkan kostnað á ferð eingöngu ef „frá“ og „til“ hafnir í uppsetningu sjálfvirks kostnaðar passar við „frá“ og „til“ hafnir ferðarinnar. |
| **Sjálfvirk kostnaðarnúmer** | Einkvæmt auðkenni reglu fyrir sjálfvirkan kostnað. Gildi þessa reits er sjálfkrafa myndað á grundvelli númeraraðarinnar sem er sett upp á síðunni **Færibreytur heildarkostnaðar**. |
| **Birgðavíddir** | Sumir kostnaðarþættir gerir kleift að hafa með eina eða fleiri vöruvíddir í hausnum (t.d. stærð, lit, vöruhús og rununúmer). Veljið **Birtar víddir** á aðgerðasvæði til að velja víddirnar sem á að taka með. |

## <a name="settings-on-the-lines-fasttab"></a>Stillingar á flýtiflipanum Línur

Í flýtiflipanum **Línur** skal bæta við línu fyrir hvern gjaldmiðil sem hægt er að nota þegar kostnaður er settur á innkaupapöntunarlínu í ferð. 

Fyrir vörur og innkaupapantanir mun kerfið stemma gjaldmiðil hverrar innkaupapöntunarlínu við gjaldmiðlana sem eru tilgreindir í flýtiflipanum **Línur**. Það mun aðeins gilda um kostnaðarvirðið sem er stillt fyrir viðkomandi línu eða vöru. Ef engin lína er sett upp fyrir gjaldmiðil línu eða vöru verður sjálfvirkur kostnaður ekki notaður fyrir þá línu eða vöru.

Fyrir aðrar gerðir kostnaðarþátta munu allar línur í flýtiflipanum **Línur** eiga við um hverja ferð, flutningagám, fólíó eða flutningspöntunarlínu sem stemmir við gildin sem eru sett í hausinn.

Eftirfarandi tafla lýsir öllum reitunum sem geta birst í hverri línu fyrir sig. Hins vegar eru tilteknir reitir sem eru í boði breytilegir eftir því hvaða kostnaðarþáttur er valinn.

| Svæði | lýsing |
|---|---|
| **Gjaldmiðill** | Veljið gjaldmiðil fyrir þessa línu. Þessi gjaldmiðill tengist innkaupapöntun. Þegar kerfið reynir að finna sjálfvirkan kostnað sem á að leggja á ferð og línur hennar mun það velja línuna sem er með sama gjaldmiðilinn og innkaupapöntunin. Þessi reitur er aðeins í boði þegar reiturinn **Kostnaðarsvæði** er stilltur á *Innkaupapöntun* eða *Vara*. |
| **Kostnaðargerðarkóði** | Kostnaðartegund. |
| **Skiptingaraðferð** | <p>Aðferðin sem notuð er til að dreifa kostnaði á línur. Eftirtaldir valkostir eru í boði:</p><ul><li><p>**Prósenta** – Gildið í reitnum **Kostnaðarvirði** er prósenta sem gildir um heildarvirði varanna.</p><p>Ef til dæmis reiturinn **Kostnaðarvirði** er stilltur á *10* og heildarvirði varanna er $800, verður kostnaðarvirðið $80 (= $800 x 10 prósent).</p></li><li>**Magn** – Kostnaðurinn skiptist samkvæmt magni varanna.</li><li>**Upphæð** – Kostnaðurinn skiptist samkvæmt virði varanna.</li><li>**Rúmmála** – Kostnaðurinn skiptist samkvæmt rúmmáli varanna. Rúmmál er tilgreint í sniðmáti vörunnar.</li><li>**Þyngd** – Kostnaðurinn skiptist samkvæmt þyngdar varanna. Þyngd er tilgreind í sniðmáti vörunnar.</li><li>**Rúmmálsmæling** - Kostnaðurinn skiptist samkvæmt rúmmálsmælingu varanna.</li><li><p>**Mæling** – Þessi valkostur gerir notendum kleift að tilgreina mælingu í einingunni **Heildarkostnaður**. Hún er oft notuð af fyrirtækjum sem vita ekki rúmmál eða þyngd varanna, en þurfa nákvæmari skiptingu en valkostirnir **Upphæð** og **Magn** bjóða upp á. Flutningsmiðlarinn eða umboðsmaðurinn mun láta fyrirtækið fá þyngdina eða rúmmálsmælinguna á annaðhvort vörustigi eða innkaupapöntunarstigi.</p><p>Til dæmis flutningur sjóleiðis sem jafngildir $900. Vara A er 800 kíló (kg) að þyngd og rúmmál hennar er 2 rúmmetrar (m³). Vara B er 100 kg að þyngd og rúmmál hennar er 1 m³. Hér eru niðurstöðurnar þegar kostnaði er skipt eftir þyngd:</p><ul><li>Vara A = $800</li><li>Vara B = $100</li></ul><p>Hér eru niðurstöðurnar þegar kostnaði er skipt eftir rúmmáli:</p><ul><li>Vara A = $600</li><li>Vara B = $300</li></ul><p>**Athugið:** Þegar reiturinn **Skiptingaraðferð** er stilltur á *Mæling* notar kerfið mælingar sem eru færðar inn fyrir bæði kostnaðarþáttinn (flutningsgáminn) og línurnar. Þessar mælingar þurfa ekki endilega að passa saman við væntanlega samtölu. Ef hins vegar gerð er krafa um að þær jafngildi væntanlegri samtölu er hægt að gera athugun með því að nota tölfræðina til að yfirfara mælingu samtölunnar. Stilling fyrir kvaðningu mælingar og sjálfvirk uppfærsla mælingarinnar á sendingar- eða gámastigi eru stillt í haus ferðarinnar.</p></li></ul> |
| **Frá dagsetning** | Tilgreinið upphafsdag dagsetningabils fyrir kostnað, ef dagsetningabil er til staðar. Þessi dagsetning er fyrsta dagsetningin þegar sjálfvirkur kostnaður gildir. |
| **Lokadagsetning** | Tilgreinið lokadag dagsetningabils fyrir kostnað, ef dagsetningabil er til staðar. Þessi dagsetning er síðasta dagsetningin þegar sjálfvirkur kostnaður gildir. |
| **Tegund** | <p>Veljið aðferðina sem á að nota til að reikna út kostnað. Eftirtaldir valkostir eru í boði:</p><ul><li>**Fastur** – Kostnaðurinn er reiknaður samkvæmt skiptingu.</li><li>**Stykki** – Kostnaður skiptist eftir stykkjum. Þess vegna verður skiptingaraðferðin ekki notuð.</li><li>**Prósent** – Prósentu af virði varanna verður bætt við. Þess vegna verður skiptingaraðferðin ekki notuð.</li><li>**Taxti** – Veljið þennan valkost ef magn er brotið niður. Reiturinn **Skiptingaraðferð** fyrir línuna verður að vera stilltur á *Mæling*.</li><ul> |
| **Sundurliðað eftir magni** | <p>Veljið þennan gátreit til ganga úr skugga um að hnappurinn **Sundurliðun magns** sé tiltækur í flýtiflipanum **Línur**. Sundurliðun magns gerir kleift að sundurliða kostnaðinum og að hafa hann breytilegan, allt eftir því hvert magnið er í innkaupapöntunarlínu ferðarinnar. Þessi virkni er oft notuð þegar flutningsmátinn er loftleiðis. Reiturinn **Flokkur** fyrir línuna verður að vera stilltur á *Taxti*.</p><p>Magnið snertir þann valkost sem valinn er í reitnum **Skiptingaraðferð**. Kostnaðargildið verður upp að því magni sem er fært inn í reitinn **Kostnaðarvirði**.<p>Til dæmis magn sem er 45–100 kg leiðir til gjalds upp á $6,00 á hverja mælingu (t.d. kg/m³). Magn sem fer yfir 100 kg leiðir til gjalds upp á $5,50 á hverja mælingu (t.d. kg/m³).</p> |
| **Kostnaðarvirði** | Slá inn gildi kostnaðar. |
| **Gjaldmiðilskóði kostnaðar** | Veljið gjaldmiðil kostnaðar. |
| **VSK-flokkur vöru** | Vljið skattkóða fyrir kostnaðinn. |
| **Lágmarkskostnaður** | <p>Þessi reitur á aðeins við ef gátreiturinn **Sundurliðað eftir magni** er valinn. Ef mælingin nær ekki þessu gildi er lágmarksgildið valið óháð kostnaði sem er tilgreindur á síðunni **Sundurliðun magns**.<p>Til dæmis magn sem er 0–45 kg leiðir til gjalds upp á $6 á hverja mælingu (kg/m³). Magn sem er 46–100 kg leiðir til gjalds upp á $5,50 á hverja mælingu (kg/m³). Ef 2 kg eru flutt mun sundurliðun magns búa til kostnaðarvirði upp á $12. Ef reiturinn **Lágmarkskostnaður** er hins vegar stilltur á *$100* verður lokakostnaðurinn $100.</p> |
| **Samanlagt** | Veljið þennan gátreit til að gera notendum kleift að flytja þennan kostnað af stigi flutningsgáms yfir á stig ferðar. Í þessu tilviki er hægt að reikna kostnað sjálfkrafa á stigi flutningsgáms. Hins vegar er einnig hægt að sameina hann og skipta honum niður á allar vörur í öllum gámunum í ferð í stað allra varanna í einum flutningsgámi. |
| **Tengd kostnaðargerð** | <p>Tengið núverandi línu við aðra línu í sömu sjálfvirku kostnaðarfærslunni með því að tilgreina gildið **Kostnaðargerðarkóði** fyrir línuna sem á að tengja við. Þessi virkni er aðeins í boði þegar reiturinn **Flokkur** fyrir núverandi línu er stilltur á *Prósenta*. Þegar núverandi lína er tengd við aðra línu verður kostnaður núverandi línu byggður á kostnaði hinnar línunnar.</p><p>Til dæmis er farmur $1000 og þú vilt að eldsneytisgjaldið verði 10 prósent af kostnaði farmsins. Í þessu tilfelli verður línan að vera með gildið **Flokkur** sem *Prósenta*, gildið **Kostnaðarvirði** upp á *10%*, og gildið **Tengd kostnaðargerð** sem *Farmur*.</p> |
| **Leiðrétting virðis** og **Leiðréttingarupphæð** | <p>Notið þessa reiti til að leiðrétta gildi og upphæð fyrir ýmis prósentugildi. Þeir eru aðeins í boði þegar reiturinn **Kostnaðarþáttur** er stilltur á *Vara*.</p><p>Hægt er að setja upp mismunandi kostnaðarútreikning fyrir mismunandi hluta vöru. Einn hluti vöru gæti verið með mismunandi kostnaðarprósentu en aðrir hlutar þeirrar vöru. Þessi nálgun er stundum nauðsynleg til að meta tiltekinn hluta varanna á mismunandi taxta.</p><p>Til dæmis er gjald fyrir úr reiknað með tveimur töxtum: einn hlutur úrsins er með 10 prósent toll og annar hlutur er með 2 prósenta tolli. Í þessu tilviki verður kostnaðarútreikningi skipt á milli tveggja hluta.</p><p>Kostnaðurinn er reiknaður fyrir vöruna en kostnaðarvirðið er leiðrétt eftir gildi hlutanna sem eru með mismunandi kostnaðartegund. Síðan er hægt er að reikna út kostnað eftirstandandi hluta með því að nota upphæðina sem nemur leiðréttingu fyrri útreiknings.</p><p>Til dæmis er hluti A á úrinu með kostnaðinn $9,50 og toll upp á 10 prósent, og hluti B er með kostnaðinn $0,50 og toll sem nemur 2 prósentum. Því er heildarkostnaður $10,00. Fyrsta færslan er fyrir 10 prósent línuna. Þa notar eftirfarandi gildi:</p><ul><li>**Flokkur:** *Prósent*</li><li>**Kostnaðarvirði:** *10*</li><li>**Leiðrétt gildi:** *Leiðrétta um*</li><li>**Leiðrétt gildi:** *-0,50*</li></ul><p>Þessi uppsetning tilgreinir að lækka þurfi kostnað vörunnar ($10) um $0,50 (verð hluta B) áður en 10 prósenta tollur er reiknaður. Þess vegna verða 10 prósent lögð á $9,50.</p><p>Seinni færslan er fyrir 2 prósenta línuna ($0,50 sem fyrri færslan var leiðrétt um). Þa notar eftirfarandi gildi:</p><ul><li>**Flokkur:** *Prósent*</li><li>**Kostnaðarvirði:** *2*</li><li>**Leiðrétt gildi:** *Nota*</li><li>**Leiðrétting:** *0,50*</li></ul><p>Þessi uppsetning reiknar út eftirstandandi toll sem greiða þarf af hluta B.</p> |
