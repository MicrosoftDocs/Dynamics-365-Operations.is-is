---
title: Bilanagreining eignar
description: Þessi grein útskýrir bilanagreiningu eigna í Eignastýringu.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectFaultCalculate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d4503c39a643461c75878c6c7096d824642ad1a2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869779"
---
# <a name="asset-fault-analysis"></a>Bilanagreining eignar

[!include [banner](../../includes/banner.md)]

 

Í eignastýringu er hægt að greina skráningar eignabilana til að fá yfirsýn yfir heildarfjölda bilana sem eru skráðir á tilteknu tímabili. Hægt er að greina bilanaskráningar frá mismunandi sjónarhornum, til dæmis með áherslu á eignir, eignagerðir, virkar staðsetningar, bilunareinkenni eða bilanagerðir.

1. Smelltu á **Eignastýringu** > **Fyrirspurnir** > **Bilun eignar** > **Greiningu eignabilunar**.

2. Í glugganum **Útreikningur á greiningu eignabilunar** geturðu notað reitinn **Stig** til að gefa til kynna hversu ítarlegar þú vilt að eignabilanalínurnar séu varðandi virkar staðsetningar. 

    Til dæmis, ef þú setur inn töluna „1“ í reitinn, og þú ert með fjölþrepa skipulag virkra staðsetninga, verða allar eignabilanalínur fyrir virka staðsetningu sýndar á efsta stigi og því er hægt að bæta tímunum á línunni við af virkum staðsetningum sem eru staðsettar á lægra stigi. 
        
    Ef þú setur töluna „0“ inn í reitinn **Stig** muntu sjá ítarlega niðurstöður sem sýna allar eignabilanalínur á öllum virkum staðsetningarstigum sem þær tengjast.

3. Ef þú vilt takmarka leitina geturðu valið sérstakar eignir, bilunardagsetningar, bilunarástæður og bilunarúrræði á flýtiflipanum **Færslur til að taka með**.

4. Smellið á **Í lagi** til að byrja að reikna.

5. Á flipanum **Eignabilanagreining** smellirðu á hnappana **Flokka eftir...** til að birta smáatriðastigið sem þú vilt sjá. Virkjaðir hnappar eru auðkenndir. Virkjaður eða afvirkjaðu hnappa með því að smella á þá.

6. Smelltu á **Uppfæra útreikninga** til að sýna val þitt á skjánum. 

>[!NOTE]
>Í hvert skipti sem þú virkjar eða afvirkjar hnapp **Flokka eftir** skaltu muna að smella á hnappinn **Uppfæra útreikninga**. Þetta er nauðsynlegt vegna þess að mikið magn af gögnum er unnið þar sem þú ert að endurreikna villulíkindi.

## <a name="examples"></a>Dæmi

Það eru margar leiðir til að greina skráningar á bilunum. Þessi kafli er með fimm dæmi um hvernig mismunandi gagnaval getur veitt meiri innsýn og smáatriði við greiningu á skráningum eignabilana.

### <a name="group-by-symptoms"></a>Flokka eftir einkennum

Í skjámyndinni hér að neðan er aðeins hnappurinn **Einkenni** valinn.

- Bilanaskráningar hafa verið gerðar á þremur bilunareinkennum: „Loftleka“, „Sprungið öryggi“ og „Búnaður fastur“.  
- Í dálknum **Líkindi %** leggjast allar prósentur saman að 100%. Líkindi eru byggð á öllum skráningum **Einkenna** í þessari bilagreiningu.

![Mynd 1.](media/06-controlling-and-reporting.png)

### <a name="group-by-symptoms-and-time-period"></a>Flokka eftir einkennum og tímabili

Í skjámyndinni hér að neðan er **Ári** og **Mánuði** bætt við til að sýna hvernig hægt er að skoða bilanaskráningar á völdu tímabili.

- Bilunareinkennin eru nú sýnd sem skráningar á ári/mánuði.  
- Í dálknum **Líkindi %**, ef þú bætir við öllum prósentum fyrir hvern mánuð, leggjast þær saman upp að 100%. Líkindi eru byggð á skráningum **Einkenna** í þessari bilagreiningu. Ef þú ert með mikinn fjölda lína á eign, en hærri prósenta stendur upp úr á línu, þá væri það vísbending um bilunareinkenni til að skoða betur til að finna leið til að takmarka fjölda skráninga fyrir það bilunareinkenni.

![Mynd 2.](media/07-controlling-and-reporting.png)

### <a name="group-by-multiple-symptoms-and-assets"></a>Flokka eftir margfeldi einkenna og eigna

Samsetning eigna og eignategund er notuð til grundvallar við útreikninga sem sýndir eru í þremur skjámyndunum hér að neðan sem munu aukast í smáatriðum.  

Almennt innihalda hnapparnir í **Flokka eftir dagsetningu**, **Flokka eftir eign**, **Flokka eftir virkri staðsetningu** aðgerðasvæðinu, sem og **Villa** hnappurinn (bilunarkenni), tímabil eða eignatengsl. Hnapparnir **Einkenni**, **Svæði**, **Gerð**, **Orsök** og **Úrræði** eru flokkanir sem notaðar eru í bilunastjórnun til að greina skráningu eignabilana og finna vandamálasvið.  

**Flokka eftir einkennum, eignum og eignategundum**

Í skjámyndinni hér að neðan var **Eignir** og **Gerð eigna** bætt við til að veita nánari upplýsingar varðandi skráningar á bilunum.

- Bilunareinkennunum er nú skipt upp í samsetningarnar **Eignir** / **Gerð eigna** / **Einkenni**.  
- Í dálknum **Líkindi %**, ef þú leggur saman allar prósentur fyrir samsetninguna **Eign** / **Eignagerð** / **Einkenni** í þessari röð verður útkoman 100%. Líkindi eru byggð á skráningum **Einkenna** í þessari bilagreiningu. Ef þú ert með mikinn fjölda lína á eign, en hærri prósenta stendur upp úr á línu, þá væri það vísbending um bilunareinkenni til að skoða betur til að finna leið til að takmarka fjölda skráninga fyrir það bilunareinkenni.

![Mynd 3.](media/08-controlling-and-reporting.png)

**Flokka eftir tveimur einkennum, eignum og eignategundum**

Í skjámyndinni hér að neðan var **Svæði** bætt við **Einkenni**, **Eign** og **Gerð eigna** til að veita nánari upplýsingar varðandi skráningar á bilunum.

- Í dálknum **Líkindi %**, ef þú leggur saman allar prósentur fyrir samsetninguna **Eign** / **Eignagerð** / **Einkenni** á eign verður útkoman 100%. Líkindi eru byggð á samsetningunni **Einkenni** og **Svæði** í þessari bilagreiningu. Ef þú ert með mikinn fjölda lína á eign, en hærri prósenta stendur upp úr á línu, þá væri það vísbending um bilunarsvæði til að skoða betur til að finna leið til að takmarka fjölda skráninga fyrir það bilunarsvæði.  

![Mynd 4.](media/09-controlling-and-reporting.png)

**Flokka eftir þremur einkennum, eignum og eignategundum**

Í skjámyndinni hér að neðan var **Gerð** bætt við og ítarlegasti útreikningurinn í þessu dæmi er sýndur.
 
- Í dálknum **Líkindi %**, ef þú leggur saman allar prósentur fyrir samsetninguna **Eign** / **Eignagerð** / **Einkenni** á eign verður útkoman 100%. Líkindi eru byggð á samsetningunni **Einkenni**, **Svæði** og **Gerð** í þessari bilagreiningu. Ef þú ert með mikinn fjölda lína á eign, en hærri prósenta stendur upp úr á línu, þá væri það vísbending um bilunargerð til að skoða betur til að finna leið til að takmarka fjölda skráninga á þeirri bilunargerð.

![Mynd 5.](media/10-controlling-and-reporting.png)


>[!NOTE]
>Til að fá yfirlit yfir allar bilanaskráningar sem stofnaðar eru í verkbeiðnum og viðhaldsbeiðnum smellirðu á **Eignastýringu** > **Fyrirspurnir** > **Bilun eignar** > **Bilanir eigna**. Á síðunni **Bilanir eigna** skaltu velja eignarbilunarskráningu og stækka gluggann **Tengdar upplýsingar** til að sjá upplýsingar varðandi tengda verkbeiðni eða viðhaldsbeiðni.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]