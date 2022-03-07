---
title: Mynda fjárhagsskýrslur
description: Þetta efni inniheldur almennar upplýsingar um myndum reikningsskila.
author: jinniew
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 68843
ms.assetid: 271df6f4-12b7-4b3e-b2d7-36ea98ef1871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: c6cde37124d4a3337bca2a9b445af5fdfd87f453
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750011"
---
# <a name="generate-financial-reports"></a>Mynda fjárhagsskýrslur

[!include [banner](../includes/banner.md)]

Þetta efni inniheldur almennar upplýsingar um myndum reikningsskila.

Til að mynda skýrslu skal opna skýrsluskilgreininguna og velja svo hnappinn **Mynda** á tækjastikunni. Þá opnast síðan **Biðraðarstaða skýrslu** þar sem tilgreind er staðsetning skýrslu notandans í biðröðinni. Myndaða skýrslur verður sjálfgefið opnuð í Vefskoðun

Eftirtaldir valkostir eru í boði til að búa til skýrslu:

- Setja upp röðun til að mynda skýrslu eða skýrsluflokk sjálfkrafa
- Leita að týndum lyklum eða gögnum í skýrslu og sannprófa nákvæmni skýrslu

Þegar skýrsla er mynduð eru valkostina sem tilgreindir hafa verið á flipunum fyrir Skýrsluskilgreiningar notaðir.

## <a name="generate-a-financial-report"></a>Mynda fjárhagsskýrslu

Til að búa til fjárhagsskýrslu skal fara í **Fjárhag** \> **Fyrirspurnir og skýrslur** \> **Fjárhagsskýrslur**.

- Velja skýrslu sem á að búa til og veljið **Búa til**.
- Fylla út í reitinn **Dagsetning skýrslu** og velja **Í lagi**.

Eftir að skýrslan hefur verið búin til verður skýrslan tiltæk til skoðunar í **Skýrslur** hlutanum.

Þú getur valið að **Skoða** eða **Eyða** skýrslunni.

Til að búa til skýrslu með **Skýrsluhönnuður**, skal opna skilgreining skýrslu og smella á **Búa til** hnappinn á tækjastikunni. Þá opnast síðan **Biðraðarstaða skýrslu** þar sem tilgreind er staðsetning skýrslu notandans í biðröðinni. Myndaða skýrslur verður sjálfgefið opnuð í Vefskoðun

## <a name="report-groups"></a>Skýrsluhópar

Skýrsluhópar eru skilvirk leið til að búa til margar skýrslur samtímis. Til dæmis ef vitað er að í mánaðarlok muni notendur búa til átta skýrslur mánaðarlega. Stofnið skýrsluhóp og í stað þess að velja **Mynda** fyrir hverja skýrslu í hópnum er hægt að velja **Mynda** fyrir skýrsluhópinn og skýrslurnar átta verða myndaðar í einu skrefi. Þegar skýrslan í völdum skýrsluhóp hefur verið mynduð er hægt að fara í **Fjárhagsskýrslur** (**Fjárhagur > Fyrirspurnir og skýrslur > Fjárhagsskýrslur**) til að skoða hverja skýrslu fyrir sig. Ljúkið eftirfarandi skrefum til að setja upp skýrsluhóp.

1. Í skýrsluhönnuði skal velja **Skýrsluhópar**. 
2. Veljið fyrirliggjandi skýrsluskilgreiningar til að hafa með í skýrsluhópnum. 
3. Veljið að hnekkja stillingum fyrirtækis, upplýsinga og dagsetningar úr hverri skýrslu fyrir sig sem verður höfð með í hópnum.
   Við mælum með að stilla **Fyrirtæki**, **Tímabil**, **Ár** og **Upplýsingastig** fyrir hverja skýrslu. 
4. Vistið skýrsluhópinn.

## <a name="schedule-report-generation"></a>Skýrslumyndun áætluð
Mörg fyrirtæki eru með grunnsett af skýrslum sem eru keyrð með reglulegu millibili til samræmis við viðskiptaferla þeirra. Notandinn getur látið mynda skýrslu reglulega, eins og daglega, vikulega, mánaðarlega eða árlega. Þetta getur verið stök skýrsla eða skýrsluhópur sem felur í sér mörg fyrirtæki. Færa verður inn skilríki notanda fyrir hvert fyrirtækjanna sem tilgreind eru, eins og þau sem eru í skilgreiningu skipurits. Ef skilríkin eru ekki gild birtir skýrslan einungis upplýsingarnar sem notandinn hefur aðgangsheimild að, eins og um fyrirtækið sem notandinn er skráður inn í á þeim tíma. Fyrst eru lesnar frálagsupplýsingar úr skýrsluhópnum og síðan úr einstökum skýrslum.

Þegar skýrsluáætlanir eru stofnaðar og vistaðar eru þær birtar á yfirlitssvæðinu undir Skýrsluáætlanir. Hægt er að stofna möppur til að skipuleggja skýrslurnar. Ef ein skýrsla í ætlun er ekki keyrð er haldið áfram að keyra allar aðrar skýrslur.

> [!IMPORTANT]
> Til að stofna, breyta og eyða skýrsluáætlunum þarf að hafa hlutverk hönnuðar eða stjórnanda. Þegar skýrsla er keyrð eru skilríki notandans sem stofnaði áætlunina notuð til að mynda skýrsluna.

### <a name="create-a-report-schedule"></a>Skýrsluáætlun stofnuð

1. Í valmyndinni **Skrá** í skýrsluhönnuði skal velja **Ný** og síðan velja **Skýrsluáætlun**. Svarglugginn **Inheritance Overrides** opnast.
2. Undir **Stillingar**, veljið einstaka skýrslu eða flokk til að raða skýrslunni. Einungis eru tiltækar skýrslur eða skýrsluhópar fyrir fyrirtækis- eða einingarvalið sem notandinn er sem stendur skráður inn í.
3. Velja á **Virka** gátreit til að kveikja á áætlun skýrslu. Einungis stofnandi skýrslunnar eða stjórnandi geta gert skýrsluáætlun virka eða óvirka.
4. Smellið á hnappinn **Heimildir** til að færa inn skilríki fyrirtækis. Sjálfgefið er að innskráningarupplýsingar notanda séu notaðar fyrir fyrirtækið sem notandinn er skráður inn í þá stundina. Ef önnur fyrirtæki eru teknar með, eins og skýrslugerð skilgreiningar á trénu, skal velja **Nota aðskilinn skilríki**, og færið inn skilríki fyrir önnur fyrirtæki sem er tekin með í skýrslunni áætlun. Hægt er að velja **Windows-Sannvottun** eða sláið inn notandanafn og aðgangsorð fyrir hvert fyrirtæki. Veljið gátreitinn **Vista skilríki** til að vista skilríkin fyrir þessi fyrirtæki og veljið síðan **Í lagi** til að loka svarglugganum.
5. Undir **Tíðni** í á **Ræsa endurtekningu** svæðinu, veljið dagsetninguna þegar áætlunin er til að hefja. Að sjálfgefnu er núverandi kerfisdagsetning biðlaratölvunnar valin.
6. Í því **Keyra skýrslu á** svæðinu, veljið tíma þegar skýrslan á að keyra. Ef færður er inn tími sem er á undan núverandi kerfistíma er skýrslan keyrð á næstu áætluðu dagsetningu.
7. Í því **endurtekningarmynstur** svæði, tilgreina hversu oft skýrslan er keyrð. Að sjálfgefnu er **Daglega** valinn með gildið 1 í Bil (dagar). Aðrir valkostir eru Vikulega, Mánaðarlega og Árlega.
8. Á svæðinu Svið endurtekningar skal velja hvenær hætta á að mynda skýrsluna.

    - **Engin lokadagsetning** – keyrir skýrslu áætlun án takmarkana.
    - **Stilla fjölda tilvika** – keyrir fyrir tiltekinn fjölda skipta áætlun skýrslu, og svo er gert óvirkt.
    - **Eftir að ljúka** – áætlun skýrslu lýkur á tiltekinni dagsetningu.

9. Veljið **Vista**. Í því **Vista Sem** svarglugganum, færið inn einkvæmt heiti og lýsingu fyrir áætlunina skýrslu.

Ef afrita á skýrsluáætlun þarf að hafa hlutverk hönnuðar eða stjórnanda. Jafnvel þótt stjórnandi breyti skýrsluáætluninni viðheldur skýrslan skilríkjum notandans sem stofnaði skýrsluna.

### <a name="copy-a-report-schedule"></a>Skýrsluáætlun afrituð

1. Í skýrsluhönnun skal velja **Skýrsluáætlanir** á yfirlitssvæðinu og opna skýrsluáætlun til að afrita.
2. Í valmyndinni **Skrá** skal smella á **Vista sem** og færa inn nýtt heiti og lýsingu fyrir áætlunina í svarglugganum **Vista sem**. Veljið **Í lagi** og nýja áætlunin birtist á yfirlitssvæðinu.
3. Í nýju áætluninni skal breyta reitunum og upplýsingunum eftir þörfum og velja svo **Vista** á tækjastikunni, eða velja **Vista** í valmyndinni **Skrá**.

Ef eyða á skýrsluáætlun þarf notandinn að vera eigandi skýrsluáætlunarinnar að hafa hlutverk stjórnanda.

### <a name="delete-a-report-schedule"></a>Skýrsluáætlun eytt

1. Í skýrsluhönnun skal velja **Skýrsluáætlanir** á yfirlitssvæðinu.
2. Valin er skýrsluáætlun sem á að eyða og síðan valið **Eyða** eða ýtt á lykilinn **Eyða**.
3. Í svarglugganum fyrir staðfestingu eyðingar er smellt á **Já** til að eyða skýrsluáætluninni til frambúðar. Ef notandinn er ekki með heimild til að eyða áætluninni birtast skilaboð og skýrslunni er ekki eytt.

### <a name="credentials-and-report-schedules"></a>Skilríki og skýrsluáætlanir

Ef þú færir ekki inn skilríki sem eru nauðsynleg fyrir öll fyrirtæki í skýrslum, berast þér eftirfarandi skilaboð þegar skýrsluáætlun er vistuð: „Tilgreina verður skilríkin fyrir þau fyrirtæki sem eru til staðarí þessari skýrsluáætlun. Smellið á hnappinn „Heimildir“ til að færa inn skilríkin þín.“

Til dæmis skráir notandi sig inn á Fyrirtæki A með sinni innskráningu og aðgangsorði. Notandi stofnar áætlun fyrir skýrslu sem notar skýrslugerð tré skilgreiningu til að safna gögnum frá mörgum fyrirtækjum. Þegar áætlun þessi skýrsla er vistuð er notandinn beðinn um að notendaheimildir færðar inn í öðrum fyrirtækjum sem eru tilgreind í skilgreiningu reporting tréð. Þegar skilríki notanda renna út eru skýrslurnar sem það hefur áhrif á ekki myndaðar fyrr en skilríkin hafa verið uppfærð. Skilaboð birtast einnig í skýrslubiðröðinni til að gefa til kynna að uppfæra þurfi heimildir. Skýrsluáætlunin bregst ef einhver af eftirfarandi aðstæðum koma upp (þar sem þær krefjast skilríkja):

- Nýju fyrirtæki er bætt við skipuritið fyrir einstaka skýrslu.
- Skýrslu í skýrsluhópi er breytt.
- Nýrri skýrslu fyrir annað fyrirtæki er bætt við skýrsluhópinn.

Veljið hnappinn **Heimildir** í svarglugganum **Skýrslugerð** til að halda áfram og færið síðan inn viðeigandi skilríki.

## <a name="missing-account-analysis-feature"></a>Eiginleiki greiningar reiknings sem vantar
Hægt er að leita að fjárhagsreikningum og víddum sem hugsanlega gæti vantað þvert yfir línuskilgreiningar, skilgreiningar skipurits og skilgreiningar skýrslu í einingahóp. Þetta er gagnlegt þegar stofnaðir eða uppfærðir eru margir reikningar eða einingar á stuttu tímabili og staðfesta á að allar nýjar upplýsingar séu innfaldar í skýrslunum.

Ákvörðun um það hvaða reikninga vantar er gerð með því að nota hæsta og lægsta gildi línuskilgreiningarinnar eða skipuritsskilgreiningarinnar og birta svo lista yfir reikninga sem ekki eru í línuskilgreiningunni eða skipuritsskilgreiningunni, en eru í fjárhagsgögnunum. Ef reikningur sem vantar er hærri eða lægri en gildin í línuskilgreiningunni er sá reikningur ekki með á listanum yfir reikninga sem vantar.

> [!TIP]
> Hvað staðfestingu varðar ætti þetta ferli að vera keyrt áður en myndaðar eru mánaðarlegar skýrslur og þegar nýjar einingar eru stofnaðar.

Ólíklegra er að skýrslur sem hafa svið gilda vanti reikninga. Þegar mögulegt er skal nota svið í einingunni til að hafa nýja reikninga með þegar þeir eru stofnaðir. Ef skýrslugreining er stillt á @ANY fyrirtæki, þá getur notandi skráð sig inn á tiltekið fyrirtæki og keyrt reikningsgreiningu sem vantar fyrir það fyrirtæki.

> [!NOTE]
> Ef nýju fyrirtæki hefur verið bætt við, verður að bæta nýja fyrirtækinu við skipuritið í öllum núverandi skýrslum, annars mun fyrirtækið ekki vera innfalið í greiningu á reikningum sem vantar.

### <a name="run-missing-account-analysis"></a>Keyrsla reikningsgreiningar sem vantar

1. Í skýrsluhönnun skal velja **Verkfæri** og svo velja **Reikningsgreiningu vantar**.
2. Í á **Fyrirtæki síu** skal velja fyrirtæki til að sía niðurstöður eða velja **Allar (engin sía)** til að birta niðurstöður úr tiltæk öllum fyrirtækjum.
3. Í á **víddarsía** skal velja víddina til að sía niðurstöður eða velja **Allar (engin sía)** til að skoða allar víddarupplýsingar fyrir allar víddir tiltækar.
4. Í því **Flokka eftir** skal velja valkost til að raða niðurstöðunum. Hægt er að raða niðurstöðunum eftir einingunni sem verður fyrir áhrifum, en einnig er hægt að raða niðurstöðum eftir vídd og gildasamstæðum.
5. Farið yfir niðurstöðurnar sem birtast. Þegar atriði er valið á efra svæðinu birtast viðbótarupplýsingar um undantekninguna á neðra svæðinu. Þetta innifelur tengdar víddir, gildi og skýrslur.
6. Til þess að opna atriðið skal velja tengt tákn sem birtist á svæðislistanum eða hægrismella á atriðið og velja **Opna**. Til að velja mörg atriði skal halda **Ctrl**-lyklinum niðri um leið og valin eru atriði á neðra svæðinu.
7. Ef einhverjar gildi, grunneiningar eða skýrslum er skilað sem ekki á að fylgja með greiningu, hægrismellið á vöru og velja **Útiloka**, eða velja þá **Útiloka** gátreitinn við hliðina á atriðinu til að fjarlægja vöruna úr listanum. Útilokuð atriði eru ekki tekin með þegar listinn er endurnýjaður. Til að velja mörg atriði skal halda **Ctrl**-lyklinum niðri um leið og valin eru atriði á neðra svæðinu. Til þess að skoða öll atriði, þar á meðal niðurstöður sem áður hafa verið valdar til útilokunar frá greiningunni, skal velja gátreitinn **Sýna útilokaðar einingar** og gildi og velja síðan **Endurnýja**.
8. Veljið **Endurnýja** til að endurnýja undantekningar sem hafa verið afgreiddar. Veljið **Já** til að endurhlaða öllum niðurstöðunum eða **Nei** til þess að endurhlaða að hluta til atriði sem eru afgreidd.

    > [!NOTE]
    > Sniðið er sjálfkrafa endurhlaðið þegar það er opnað, nema ef sniðið hefur verið opnað á síðustu 15 mínútunum.

9. Þegar vandamálin hafa verið leyst er valið **Í lagi** til að loka svarglugganum.

## <a name="keyboard-shortcuts-for-missing-account-analysis"></a>Flýtilyklar fyrir greiningu á reikningum sem vantar
Þegar keyrð er greining á reikningum sem vantar eru eftirfarandi flýtilyklar í boði.

| Til að gera þetta                           | Ýta á  |
|--------------------------------------|----------------------------|
| Afmarka eftir fyrirtæki                    | Alt+C                      |
| Afmarka eftir vídd                  | Alt+D                      |
| Veljið reitinn Flokka eftir            | Alt+G                      |
| Sýna útilokaðar einingar og gildi      | Alt+S                      |
| Endurhlaða niðurstöður                      | Alt+R                      |
| Útiloka valda einingu  | Alt+X                      |
| Útiloka valda línuskilgreiningu  | Ctrl+B                     |
| Útiloka valið víddargildi | Ctrl+D                     |
| Opna valda skýrsluskilgreiningu  | Ctrl+R                     |
| Opna valda línuskilgreiningu     | Ctrl+O                     |


## <a name="additional-resources"></a>Frekari upplýsingar

[Fjárhagsskýrslugerð](financial-reporting-intro.md)

[Viðmót Report Designer](report-designer-interface.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
