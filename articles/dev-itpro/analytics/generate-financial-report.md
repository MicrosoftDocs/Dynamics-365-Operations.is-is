---
title: "Mynda fjárhagsskýrslu"
description: "Þetta efni inniheldur almennar upplýsingar um myndum reikningsskila."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 68843
ms.assetid: 271df6f4-12b7-4b3e-b2d7-36ea98ef1871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 01bb8999e5d9c0e16f133a621ebfe1d102565f2f
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="generate-a-financial-report"></a>Mynda fjárhagsskýrslu

[!include[banner](../includes/banner.md)]


Þetta efni inniheldur almennar upplýsingar um myndum reikningsskila. 

Til að mynda skýrslu skal opna skýrsluskilgreininguna og smella svo á hnappinn Mynda á tækjastikunni. Þá opnast glugginn Biðraðarstaða skýrslu þar sem tilgreind er staðsetning skýrslu notandans í biðröðinni. Myndaða skýrslur verður sjálfgefið opnuð í Vefskoðun
| ![Athugasemd](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Athugasemd")**Athugasemd**        |
|------------------------------------------------------------------------------------------------|
| Aðeins er hægt að mynda skýrslur í möppum og staðsetningar sem notandi hefur aðgangsheimild að. |

Eftirfarandi tafla útskýrir valkosti sem eru tiltækir fyrir myndun á skýrslum.

| Valkostur                                                                                | Frekari upplýsingar |
|---------------------------------------------------------------------------------------|----------------------|
| Setja upp röðun til að mynda skýrslu eða skýrsluflokk sjálfkrafa              |                      |
| Leita að týndum lyklum eða gögnum í skýrslu og sannprófa nákvæmni skýrslu |                      |

Þegar skýrsla er mynduð eru valkostina sem tilgreindir hafa verið á flipunum fyrir Skýrsluskilgreiningar notaðir. Flipinn Frálag og dreifing gerir notanda kleift að tilgreina staðsetningu skýrslusafns, en þannig er mjög auðvelt að deila skýrslunni.

## <a name="schedule-report-generation"></a>Skýrslumyndun áætluð
Mörg fyrirtæki eru með grunnsett af skýrslum sem eru keyrð með reglulegu millibili til samræmis við viðskiptaferla þeirra. Notandinn getur látið mynda skýrslu reglulega, eins og daglega, vikulega, mánaðarlega eða árlega. Þetta getur verið stök skýrsla eða skýrsluhópur sem felur í sér mörg fyrirtæki. Færa verður inn skilríki notanda fyrir hvert fyrirtækjanna sem tilgreind eru, eins og þau sem eru í skilgreiningu skipurits. Ef skilríkin eru ekki gild birtir skýrslan einungis upplýsingarnar sem notandinn hefur aðgangsheimild að, eins og um fyrirtækið sem notandinn er skráður inn í á þeim tíma. Fyrst eru lesnar frálagsupplýsingar úr skýrsluhópnum og síðan úr einstökum skýrslum.

Þegar skýrsluáætlanir eru stofnaðar og vistaðar eru þær birtar á yfirlitssvæðinu undir Skýrsluáætlanir. Hægt er að stofna möppur til að skipuleggja skýrslurnar. Ef ein skýrsla í ætlun er ekki keyrð er haldið áfram að keyra allar aðrar skýrslur.
| ![Mikilvægt](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Mikilvægt")**Mikilvægt**                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Til að stofna, breyta og eyða skýrsluáætlunum þarf að hafa hlutverk hönnuðar eða stjórnanda. Þegar skýrsla er keyrð eru skilríki notandans sem stofnaði áætlunina notuð til að mynda skýrsluna. |

### <a name="create-a-report-schedule"></a>Skýrsluáætlun stofnuð

1.  Á valmyndinni Skrá í Skýrsluhönnun skal smella á Nýtt og velja svo Skýrsluáætlun. Svarglugginn Ný skýrsluáætlun opnast.
2.  Undir Stillingar skal velja einstaka skýrslu eða skýrsluhóp sem á að setja á áætlun. Einungis eru tiltækar skýrslur eða skýrsluhópar fyrir fyrirtækis- eða einingarvalið sem notandinn er sem stendur skráður inn í.
3.  Veljið gátreitinn Virkt til að kveikja á skýrsluáætluninni. Einungis stofnandi skýrslunnar eða stjórnandi geta gert skýrsluáætlun virka eða óvirka.
4.  Smellið á hnappinn Heimildir til að færa inn skilríki fyrir fyrirtæki. Sjálfgefið er að innskráningarupplýsingar notanda séu notaðar fyrir fyrirtækið sem notandinn er skráður inn í þá stundina. Ef önnur fyrirtæki eru tekin með, eins og í skilgreiningum skipurits, skal velja Nota aðskilin skilríki og færa síðan inn skilríkin fyrir öll önnur fyrirtæki sem tekin eru með í skýrsluáætluninni. Hægt er að velja Windows-sannvottun eða færa inn notandanafn og aðgangsorð fyrir hvert fyrirtæki. Veljið gátreitinn Vista skilríki til að vista skilríkin fyrir þessi fyrirtæki og smellið svo á Í lagi og lokið svarglugganum.
5.  Undir Tíðni, í reitnum Hefja endurtekningu, skal velja dagsetninguna þegar áætlunin á að hefjast. Að sjálfgefnu er núverandi kerfisdagsetning biðlaratölvunnar valin.
6.  Í reitnum Keyra skýrslu á skal velja tímann þegar keyra á skýrsluna. Ef færður er inn tími sem er á undan núverandi kerfistíma er skýrslan keyrð á næstu áætluðu dagsetningu.
7.  Í svæðinu Endurtekningarmynstur er tilgreint hversu oft skýrslan er keyrð. Að sjálfgefnu er Daglega valinn með gildið 1 í Bil (dagar). Aðrir valkostir eru Vikulega, Mánaðarlega og Árlega.
8.  Á svæðinu Svið endurtekningar skal velja hvenær hætta á að mynda skýrsluna.
    -   Engin lokadagsetning – Skýrslan er keyrð endalaust.
    -   Velja fjölda skipta – Skýrsluáætlunin er keyrð í tilgreindan fjölda skipta og síðan gerð óvirk.
    -   Ljúka – Skýrsluáætluninni lýkur á tilgreindum degi.

9.  Smellið á Vista á tækjastikunni. Í svarglugganum Vista sem er fært inn einkvæmt heiti og lýsing fyrir skýrsluáætlunina.

Ef afrita á skýrsluáætlun þarf að hafa hlutverk hönnuðar eða stjórnanda. Jafnvel þótt stjórnandi breyti skýrsluáætluninni viðheldur skýrslan skilríkjum notandans sem stofnaði skýrsluna.
### <a name="copy-a-report-schedule"></a>Skýrsluáætlun afrituð

1.  Í Skýrsluhönnun er smellt á Skýrsluáætlanir á yfirlitssvæðinu og skýrsluáætlun opnuð sem á að afrita.
2.  Á valmyndinni Skrá skal smella á Vista sem og færa inn nýtt heiti og lýsingu fyrir áætlunina í svarglugganum Vista sem. Smellt er á Í lagi og nýja áætlunin birtist á yfirlitssvæðinu.
3.  Í nýju áætluninni skal breyta reitunum og upplýsingunum eftir þörfum og smella svo á Vista á tækjastikunni, eða smella á Vista á valmyndinni Skrá.

Ef eyða á skýrsluáætlun þarf notandinn að vera eigandi skýrsluáætlunarinnar að hafa hlutverk stjórnanda.
### <a name="delete-a-report-schedule"></a>Skýrsluáætlun eytt

1.  Í Skýrsluhönnun er smellt á Skýrsluáætlanir á yfirlitssvæðinu.
2.  Valin er skýrsluáætlun sem á að eyða og síðan smellt á Eyða eða ýtt á Delete-lykilinn.
3.  Í svarglugganum fyrir staðfestingu eyðingar er smellt á Já til að eyða skýrsluáætluninni varanlega. Ef notandinn er ekki með heimild til að eyða áætluninni birtast skilaboð og skýrslunni er ekki eytt.

### <a name="credentials-and-report-schedules"></a>Skilríki og skýrsluáætlanir

Ef ekki eru færð inn skilríki sem krafist er fyrir öll fyrirtæki sem tekin eru með í skýrslunni birtast eftirfarandi skilaboð þegar skýrsluáætlunin er vistuð: „Færa verður inn skilríki fyrir fyrirtækin sem þessi skýrsluáætlun inniheldur. Veljið hnappinn Heimildir til að færa inn skilríki notanda.“

Til dæmis skráir Pála sig inn í Fyrirtæki A með notandanafni sínu og aðgangsorði. Hún stofnar áætlun fyrir staka skýrslu sem notar skipuritsskilgreiningu til að safna gögnum frá mörgum fyrirtækjum. Þegar þessi skýrsluáætlun er vistuð fær Pála kvaðningu um að færa inn skilríkin fyrir hin fyrirtækin sem tilgreind eru í skipuritsskilgreiningunni. Þegar skilríki notanda renna út eru skýrslurnar sem það hefur áhrif á ekki myndaðar fyrr en skilríkin hafa verið uppfærð. Skilaboð birtast einnig í skýrslubiðröðinni til að gefa til kynna að uppfæra þurfi heimildir. Skýrsluáætlunin bregst ef einhver af eftirfarandi aðstæðum koma upp (þar sem þær krefjast skilríkja):
-   Nýju fyrirtæki er bætt við skipuritið fyrir einstaka skýrslu.
-   Skýrslu í skýrsluhópi er breytt.
-   Nýrri skýrslu fyrir annað fyrirtæki er bætt við skýrsluhópinn.

Smellið á hnappinn Heimildir í svarglugganum Skýrslugerð samkvæmt áætlun til að halda áfram og færið síðan inn viðeigandi skilríki.

## <a name="missing-account-analysis-feature"></a>Eiginleiki greiningar reiknings sem vantar
Hægt er að leita að fjárhagsreikningum og víddum sem hugsanlega gæti vantað þvert yfir línuskilgreiningar, skilgreiningar skipurits og skilgreiningar skýrslu í einingahóp. Þetta er gagnlegt þegar stofnaðir eða uppfærðir eru margir reikningar eða einingar á stuttu tímabili og staðfesta á að allar nýjar upplýsingar séu innfaldar í skýrslunum.

Ákvörðun um það hvaða reikninga vantar er gerð með því að nota hæsta og lægsta gildi línuskilgreiningarinnar eða skipuritsskilgreiningarinnar og birta svo lista yfir reikninga sem ekki eru í línuskilgreiningunni eða skipuritsskilgreiningunni, en eru í fjárhagsgögnunum. Ef reikningur sem vantar er hærri eða lægri en gildin í línuskilgreiningunni er sá reikningur ekki með á listanum yfir reikninga sem vantar.
| ![Ábending](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Ábending")**Ábending**                                             |
|----------------------------------------------------------------------------------------------------------------------------------|
| Hvað staðfestingu varðar ætti þetta ferli að vera keyrt áður en myndaðar eru mánaðarlegar skýrslur og þegar nýjar einingar eru stofnaðar. |

Ólíklegra er að skýrslur sem hafa svið gilda vanti reikninga. Þegar mögulegt er skal nota svið í einingunni til að hafa nýja reikninga með þegar þeir eru stofnaðir. Ef einhver skýrsluskilgreining er stillt á @ANY fyrirtæki er hægt að skrá sig inn á tiltekið fyrirtæki og keyra greiningu á reikningum sem vantar fyrir það fyrirtæki.
| ![Athugasemd](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Athugasemd")**Athugasemd**                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ef nýju fyrirtæki hefur verið bætt við, verður að bæta nýja fyrirtækinu við skipuritið í öllum núverandi skýrslum, annars mun fyrirtækið ekki vera innfalið í greiningu á reikningum sem vantar. |

### <a name="run-missing-account-analysis"></a>Keyrsla reikningsgreiningar sem vantar

1.  Smellið á Verkfæri í Skýrsluhönnun og smellið svo á Reikningsgreiningu vantar.
2.  Í reitnum Fyrirtækisafmörkun skal velja fyrirtæki til að afmarka niðurstöður við eða velja Allt (engin afmörkun) til að birta niðurstöður frá öllum tiltækum fyrirtækjum.
3.  Í reitnum Víddarafmörkun skal velja vídd til að afmarka niðurstöður við eða velja Allt (engin afmörkun) til að skoða allar víddarupplýsingar um tiltækar víddir.
4.  Í reitnum Flokka eftir skal velja hvernig raða á niðurstöðunum. Hægt er að raða niðurstöðunum eftir einingunni sem verður fyrir áhrifum, en einnig er hægt að raða niðurstöðum eftir vídd og gildasamstæðum.
5.  Farið yfir niðurstöðurnar sem birtast. Þegar atriði er valið á efra svæðinu birtast viðbótarupplýsingar um undantekninguna á neðra svæðinu. Þetta innifelur tengdar víddir, gildi og skýrslur.
6.  Til þess að opna atriðið skal smella á tengt tákn sem birtist á svæðislistanum eða hægrismella á atriðið og velja Opna. Til að velja mörg atriði skal halda Ctrl-lyklinum niðri um leið og valin eru atriði á neðra svæðinu.
7.  Ef einhverjum gildum, einingum eða skýrslum er skilað sem ættu ekki að vera innfalin í greiningunni skal hægrismella á atriðið og velja Útiloka eða velja gátreitinn Útiloka við hlið atriðisins til þess að fjarlægja atriðið af listanum. Útilokuð atriði eru ekki tekin með þegar listinn er endurnýjaður. Til að velja margar vörur, halda niðri Ctrl-lykilinn meðan verið er að velja vörurnar í neðri rúðunni. Til að skoða allar vörur, þ.m.t. öllum niðurstöðum sem áður var valin til að útiloka frá fyrir greiningu á Sýna útilokað grunneiningar og gildi gátreitinn, og smellið síðan á Endurnýja.
8.  Smellið á Endurnýja til að endurnýja undantekningar sem hafa verið afgreiddar. Smellið á Já til að endurhlaða öllum niðurstöðunum eða Nei til þess að endurhlaða að hluta til atriði sem eru afgreidd.
    | ![Athugasemd](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Athugasemd")**Athugasemd**                    |
    |------------------------------------------------------------------------------------------------------------|
    | Sniðið er sjálfkrafa endurhlaðið þegar það er opnað, nema ef sniðið hefur verið opnað á síðustu 15 mínútunum. |

9.  Þegar vandamálin hafa verið leyst er smellt á Í lagi til að loka svarglugganum.

## <a name="keyboard-shortcuts-for-missing-account-analysis"></a>Flýtilyklar fyrir greiningu á reikningum sem vantar
Þegar keyrð er greining á reikningum sem vantar eru eftirfarandi flýtilyklar í boði.

| Til að gera þetta                           | Notið þennan flýtilykil |
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

 
<a name="see-also"></a>Sjá einnig
--------

[Fjárhagsskýrslugerð](financial-reporting-intro.md)

[Skýrsluhönnunarviðmót](report-designer-interface.md)



