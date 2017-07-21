---
title: "Innskráning á upphafsstöðu launa"
description: "Þetta efnisatriði lýsir skrefum fyrir innskráningu á upphafsstöðu fyrir tekjukóða, frádrátt, fríðindi og skatta. Þessar upplýsingar eru mikilvægar fyrir samstarfsaðila til að yfirfæra eða flytja gögn fyrir nýja launainnleiðingu úr öðru kerfi."
author: kherr
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 911a51e2498800e7ee7b1562b66c56967eef0505
ms.openlocfilehash: e6213d2e01445b78c6d8f98fc6a55f7c551231b5
ms.contentlocale: is-is
ms.lasthandoff: 06/19/2017


---

# <a name="enter-payroll-beginning-balances"></a>Innskráning á upphafsstöðu launa

[!include[banner](../../includes/banner.md)]]

Þetta efnisatriði lýsir skrefum fyrir innskráningu á upphafsstöðu fyrir tekjukóða, frádrátt, fríðindi og skatta. Þessar upplýsingar eru mikilvægar fyrir samstarfsaðila sem flytja gögn fyrir nýja launainnleiðingu úr öðru kerfi. Til að undirbúa innskráningu launastöðu, staðfestum við eftirfarandi upplýsingar:

> * Starfsmannafærslur eru innskráðar og tiltækar í kerfinu
> * Eftirfarandi gögn eru sett upp og úthlutuð starfsmönnum:

> > * Greiðsluferli og launatímabil
> > * Tekjukóðar
> > * Skattar
> > * Hlunnindi og frádráttur

> * Fyrirtækið ætti að hafa valið dagsetningu sem stilla á upphafsstöðu launa eftir.

> * Upplýsingar voru teknar saman um allar tekjur, fríðindi/frádrátt, fríðindaframlög, skatta starfsmanna og skatta vinnuveitanda og upphæðir á árinu úr gamla kerfinu.

Þar sem ætlunin er að skrá inn upphafsstöður skal hafa í huga hversu ítarleg gögnin þurfa að vera. Flest fyrirtæki skrá eina, sameinaða upphæð það sem af er ári. Hins vegar má skrá uppsafnaðar upphæðir ársfjórðungslega ef þörf er á ítarlegri upplýsingum. Það hversu ítarlegar upplýsingarnar þurfa að vera sker úr um hversu mörg handvirk launayfirlit þarf að stofna fyrir hvern starfsmann. Ef um er að ræða eina upphæð fyrir það sem af er ári, þarf aðeins eitt handvirkt yfirlit fyrir hvern starfsmann. Til að gera þetta skaltu nota upphæðir það sem af er ári fyrir síðasta launayfirlit úr fyrra kerfi sem upphæðina sem skráð er inn í nýja launakerfið.

Eftirfarandi dæmi sýnir hvernig hægt er að færa upphafsstöðu launa fyrir starfsmanninn, þar á meðal tekjukóða, fríðindi/frádrátt og skatta. Í raunverulegu dæmi myndir þú hafa línuatriði fyrir hvern tekjukóða, frádrátt fríðinda, fríðindaframlag, skatta starfsmanns og skatta vinnuveitanda með upphæðinni sem skráð er sem upphæð það sem af er ári. Notaðu þann lista yfir kóða og upphæðir og fylgdu skrefunum fyrir stofnun handvirkra tekju- og launayfirlita með bókhald afvirkjað, til að flytja yfir upphafsstöður fyrir laun.  Bókhald er afvirkjað þar sem þú vilt ekki bóka þessa upphafsstöðu launayfirlits í fjárhag. Það var gert í eldra kerfinu og kemur yfir í nýja kerfið þegar upphafsstöður eru settar í fjárhag.

> [!NOTE] 
> Viljir þú endurtaka sömu skrefin fyrir neðan getur þú notað sýnigögnin. Hægt er að hlaða niður sýnigögnum á PartnerSource

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a>A. Uppsetning tekjukóða sem nota á í upphafsstöðu launa
Þegar upphafsstöður launa eru slegnar inn, gakktu þá úr skugga um að tekjukóðarnir sem þú notar séu skilgreindir með valkostinn „Leyfa breytingar á töxtum í tekjuyfirliti“ virkjaðan. Það gerir þér kleift að lykla upphæðina handvirkt úr eldra kerfinu. 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a>B. Stofna tekjuyfirlit svo starfsmaður fái upphafsstöðu
Þetta skref stofnar tekjuyfirlit handvirkt fyrir hvern starfsmann fyrir síðasta launatímabil eldra kerfisins, sem stofnar launayfirlitslínur í nýja launakerfinu. Færðu inn eina línu fyrir hvern tekjukóða og upphæðir og tíma fyrir það sem af er ári. Sýnisskrefin eru sem hér segir:

1. Opnaðu síðuna **Öll tekjuyfirlit** og smelltu á **Nýtt**.  

Færa inn eftirfarandi: 

| Svæði      | Virði                 |
|------------|-----------------------|
| Starfskraftur     | Michael Redmond       |
| Greiðsluferli  | sm                    |
| Launatímabil | 6/16/2017 - 6/30/2017 |

2. Á flipanum **Tekjuyfirlitslínur** færirðu inn eftirfarandi:

Lína 1: Flipinn **Tekjuyfirlitslína**

| Svæði            | Virði       |
|------------------|-------------|
| Tekjukóði    | Regluleg laun |
| Magn         | 1,00        |
| Rage             | 30.000      |
| Flipi fyrir línuupplýsingar |             |
| Handvirkt           | (merkt)    |

Lína 2: Flipinn **Tekjuyfirlitslína**

| Svæði            | Virði    |
|------------------|----------|
| Tekjukóði    | Kaupauki    |
| Magn         | 1.0000   |
| Taxti             | 4250.00  |
| Flipi fyrir línuupplýsingar |          |
| Handvirkt           | (merkt) |

Lína 3: Flipinn **Tekjuyfirlitslína**

| Svæði           | Virði      |
|-----------------|------------|
| Tekjukóði   | Þóknun |
| Magn        | 1.0000     |
| Taxti            | !,299.00   |
| Taxti            | 1,299.00   |
| Flipi fyrir línuupplýsingar |            |
| Handvirkt          | (merkt)   |

> [!NOTE]
> Merking við stillingu gátreitsins Handvirkt á flipanum **Línuupplýsingar** fyrir hverja tekjuyfirlitslínu er lykilatriði til þess að hafa upphafsstöðu launa innskráða fyrir hvern starfsmann.

3. Á rúðunni **Aðgerð** smellirðu á **Birta tekjuyfirlit** USA-FED-ER-FICA.

4. Á rúðunni **Aðgerð** smellirðu á **Launayfirlit** til að opna síðuna **Búa til launayfirlit** og stillir eftirfarandi:

| Svæði              | Virði     |
|--------------------|-----------|
| Dagsetning greiðslu       | 6/30/2017 |
| Keyrslugerð greiðslu   | Handvirkt    |
| Gera bókhald óvirkt | (merkt)  |

> [!NOTE] 
> Þetta er aðeins í boði þegar keyrslugerð launa er handvirk og þar sem notandinn vill afvirkja bókhald í launakeyrslu.

Smelltu á **Í lagi** og lokaðu **Athugasemdum**.

#### <a name="why-disable-accounting-checkbox-needs-to-be-turned-on-when-generating-pay-statements"></a>Ástæða þess að það þarf að vera kveikt á gátreitnum Gera bókhald óvirkt þegar búin eru til launayfirlit.
Það kemur í veg fyrir að öllum línum í launayfirliti sé skipt og þær bókaðar í fjárhag. Ekki á að bóka þessa upphafsstöðu launayfirlits þar sem gildin eru þegar í fjárhag úr eldra kerfinu. Þessi innlestur stöðu er aðeins notaður fyrir skýrslugerð og takmarkanir.

### <a name="c-create-pay-statements-for-employees"></a>C. Stofna launayfirlit fyrir starfsmenn
Eftir að þú hefur búið til launayfirlit sem hafa upphafsstöður verður þú að sannreyna að launayfirlit endurspegli launagögn réttilega. Þú verður einnig að uppfæra upplýsingar um fríðindi og skatta handvirkt þannig að þær passi við gildin í fyrra launakerfi. Þegar búið er að sannreyna að upphæðir úr fyrra launakerfi séu þær sömu og á núverandi launayfirlitum, verður þú að leggja lokahönd á launayfirlitin.

1. Opnaðu síðuna **Öll launayfirlit**.

2. Merktu síðasta launayfirlit fyrir Michael Redmond

3. Smelltu á **Breyta** til að opna síðuna **Launayfirlit**.

4. Opnaðu flipann **Frádráttur fríðinda** og sláðu inn eftirfarandi:

| Svæði                           | Virði            |
|---------------------------------|------------------|
| Fríðindi                         | Upphæð frádráttar |
| 401K | Þátttaka              | 3000.00          |
| Tannlæknistrygging | SubSp                  | 495.00           |
| Kostnaður við tryggingar skjólstæðinga | Þátttaka | 2500.00          |
| Framtíðarsýn | SupSp                  | 500,00           |

5. Á flipanum **Frádráttur fríðinda** slærðu inn eftirfarandi: 

| Svæði                           | Virði            |
|---------------------------------|------------------|
| Fríðindi                         | Upphæð frádráttar |
| 401K | Þátttaka              | 3000.00          |
| Tannlæknistrygging | SubSp                  | 495.00           |
| Kostnaður við tryggingar skjólstæðinga | Þátttaka | 2500.00          |
| Framtíðarsýn | SupSp                  | 500,00           |

6. Á flipanum **Fríðindaframlög** slærðu inn eftirfarandi:

| Svæði              | Virði               |
|--------------------|---------------------|
| Fríðindi            | Upphæð framlags |
| 401K | Þátttaka | 3000,00             |
| Tannlæknistrygging | SubSp     | 495.00              |
| Framtíðarsýn | SubSp     | 500,00              |

7. Á flipanum **Skattafrádráttur** slærðu inn eftirfarandi:

| Svæði           | Virði            |
|-----------------|------------------|
| Skattkóði        | Upphæð frádráttar |
| USA-FED-ER-FICA | 1600.00          |
| USA-FED-ER-MEDI | 825.75           |

8. Á flipanum **Skattaframlög** slærðu inn eftirfarandi:

9. Smelltu á **Reikna út**.
> [!IMPORTANT] 
> Villuleitaðu samtölur launayfirlita þannig að þær passi við tölur það sem af er ári úr eldra kerfi fyrir starfsmanninn. Það gæti verið ráðlegt að bíða með að ljúka við næsta skref, til að villuleita öll launayfirlit saman. Þegar öll launayfirlit hafa verið villuleituð ferðu í gegnum þau og leggur lokahönd á þau.

Hægt er að framkvæma sama ferlið uppsafnað ársfjórðungslega ef það er nauðsynlegt fyrir alla fyrri fjórðunga hvert ár. Þetta er aðeins nauðsynlegt ef viðskiptavinurinn þarf að skoða gögnin eftir ársfjórðungum án þess að fara aftur í eldra kerfið.

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a>Ef þú gerir mistök við skráningu upphafsstöðu fyrir starfsmann
Er mögulegt að bakfæra og endurskrá færslur. Til að bakfæra færsluna þarftu bara að ljúka við eftirfarandi skref á síðunni **Öll launayfirlit**.

1. Smelltu á **Bakfæra**.

2. Smelltu á **Já** þegar skilaboðin „Þegar þetta launayfirlit er bakfært verður launayfirlit bakfærslu stofnað fyrir mótbókun á þessu launayfirliti. Hvorugu launayfirlitinu er hægt að breyta. Á að bakfæra þetta launayfirlit?“ birtast. 

Eftir að þú bakfærir launayfirlitið getur þú búið til nýtt launayfirlit fyrir starfsmanninn úr tekjuyfirlitum sem þú hefur stofnað áður í aðgerðinni „Búa til tekjuyfirlit og launayfirlit sem hafa upphafsstöður“ fyrr í þessu efnisatriði. Gættu þess að leiðrétta allar rangar línur í tekjuyfirlitinu áður en þú býrð til nýtt launayfirlit og endurtaktu svo aðgerðina „Uppfæra launayfirlit sem hafa upphafsstöður fyrir fríðindi og skatta“ í þessu efnisatriði.

