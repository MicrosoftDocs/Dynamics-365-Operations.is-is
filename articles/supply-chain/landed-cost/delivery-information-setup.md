---
title: Uppsetning afhendingarupplýsinga
description: Þetta efnisatriði lýsir því hvernig setja á upp afhendingarupplýsingar í gegnum Heildarkostnaður eininguna.
author: Weijiesa
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMPortTable, ITMLeadTimeTable, ITMLegTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: a0b510e4f58ca1cfec940093d118618693c68d38
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694684"
---
# <a name="delivery-information-setup"></a>Uppsetning afhendingarupplýsinga

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig setja á upp afhendingarupplýsingar í gegnum **Heildarkostnaður** eininguna.

## <a name="shipping-ports"></a>Afhendingarhafnir

Afhendingarhafnir gefa upp hvaðan og hvert verið er að senda vörur. Fyrir hverja ferð eru „til“ og „frá“ hafnir skilgreindar samkvæmt ferðinni sem er valin fyrir skip ferðar. Afhendingarhafnir eru notaðar til að búa til leggi ferðar og einnig aðgerðir ferðar. Þær eru yfirleitt skilgreindar með því að nota heiti borgar og lands eða svæðis þar sem afhendingarhöfnin er staðsett.

Til að vinna með afhendingarhafnir skal fara í **Heildarkostnaður \> Uppsetning afhendingarupplýsinga \> Afhendingarhafnir**. Þar er hægt að skoða, bæta við og fjarlægja færslur fyrir afhendingarhafnirnar. Eftirfarandi tafla lýsir eritinum sem eru tiltækir fyrir hverja færslu.

| Svæði | lýsing |
|---|---|
| Afhendingarhöfn | Færið inn einkvæmt auðkennisheiti/númer fyrir sendingarhöfn. |
| lýsing | Færið inn lýsingu á afhendingarhöfninni. |

## <a name="tracking-control-center"></a><a name="tracking-control-center"></a>Stjórnstöð rakningar

Stjórnstöð rakningar er notuð til að setja upp afhendingartíma, stöðuuppfærslur og flæði upplýsinga sem tengjast ferð þar sem flutningagámarnir ferðast frá einum legg til þess næsta. Þegar færsla rakningarstýring er stofnuð er hún tengd við ákveðinn legg á leið ferðar. Þegar ferð uppfærir legg verður tengd færsla uppfærð og fyllt í hana samkvæmt skilgreiningu. Hægt er að uppfæra rakningarupplýsingar fyrir stakar ferðir á síðunni **Allar ferðir**.

Til að opna stjórnstöð rakningar skal fara í **Heildarkostnaður \> Uppsetning afhendingarupplýsinga \> Stjórnstöð rakningar**.

Stjórnstöð rakningar sýnir eina af þremur yfirlitssíðum eftir því hvaða gildi er valið í reitnum **Gerð stofnunar** á listasvæðinu: *Autt*, *Afhendingartími* eða *Stöðuuppfærsla*. Hver stofngerð uppfærir mismunandi safn upplýsinga sem tengjast framvindu ferðar frá upprunastað til lokaáfangastaðar.

### <a name="common-rule-settings"></a>Almennar stillingar á reglum

Eftirfarandi tafla sýnir svæðin sem eru í boði fyrir allar þrjár stofngerðirnar í stjórnstöð rakningar.

| Svæði | lýsing |
|---|---|
| Upprunatafla, Upprunareitur | Þessir reitir auðkenna upprunatöflu og reit í gagnagrunninum. Reglan mun hlaða gildinu í reitinn og síðan nota hann eins og það er skilgreint af öðrum stillingum reglunnar. |
| Marktafla, Markreitur | Þessir reitir auðkenna marktöflu og reit í gagnagrunninum. Reglan mun hlaða gildinu í reitinn og síðan nota hann (eða skrifa yfir hann) eins og það er skilgreint af öðrum stillingum reglunnar. |
| Aðgerð | Þessi reitur gefur til kynna gerð aðgerðar sem á að nota á flutningagám sem samsvarar reglu. |
| Samsvarandi skilyrði | Þessi reitur sker úr um hvernig kerfið auðkennir samsvörun fyrir reglu. Í hverju tilviki fer kerfið yfir gögnin í töflum uppruna- og áfangastaðar til að ákvarða hvort og hvenær eigi að uppfæra reit í marktöflunni.<p>Til dæmis er upprunataflan *Ferðir* og marktaflan er *Innkaupahaus* eða *Innkaupalínur*. Taflan *Ferðir* er með gildi fyrir **Frá höfn** sem er *Hong Kong* og taflan *Innkaupahaus* er með gildi fyrir **Frá höfn** sem er *Shanghai*. Regla er síðan stofnuð sem er með *Hong Kong* sem „frá“ höfn. Í þessu tilviki munu gildin í reitnum **Samsvarandi skilyrði** virka á eftirfarandi hátt:</p><ul><li>**Báðir** – Markreiturinn verður ekki uppfærður því að ein af tveimur höfnum passar ekki.</li><li>**Uppruni** – Markreiturinn verður uppfærður vegna þess að „frá“ höfn upprunatöflunnar er *Hong Kong*.</li><li>**Mark** – Markreiturinn verður ekki uppfærður vegna þess að „frá“ höfn upprunatöflunnar er *Shanghai* (ekki *Hong Kong*).</li></ul> |
| Afrita aðgerð | Tiltæk gildi eru *Afrita* og *Sjálfgefið*. Veljið *Afrita* til að afrita gildið í upprunareitinum í markreitinn. Veljið *Sjálfgefið* til að stilla fast gildi fyrir reit áfangastaðar. |
| Sjálfgefinn | Þegar reiturinn **Afrita aðgerð** er stilltur á *Sjálfgefið* skilgreinir reiturinn **Sjálfgefið** sjálfgefið gildi fyrir reit áfangastaðar. Til dæmis, ef aðgerðin tengist uppfærslu hafnar, og reiturinn **Afrita aðgerð** er stilltur á *Sjálfgefið* auðkennir reiturinn **Sjálfgefið** höfn. |
| Leggur | Þessi reitur auðkennir legg ferðarinnar þar sem tiltekin aðgerð gerist, t.d. hleðsla eða tollur. |
| Þjónustuaðili | Ef sérstakur þjónustuaðili er notaður fyrir núverandi stöðuuppfærslu/legg ferðar mun þessi reitur auðkenna þjónustuaðilann. Þjónustuaðilar eru skilgreindir í lánardrottnalykli. |

### <a name="lead-time-rules"></a>Reglur afhendingartíma

Afhendingartími er áætlaður tími sem ferð þarf til að ljúka skilgreindum legg á leið ferðar. Afhendingartími fyrir hvern legg ferðar er notaður til að reikna út áætlaðan afhendingardag ferðarinnar. Sú dagsetning er síðan færð inn í reitinn **Staðfestur afhendingardagur** í allar innkaupalínur ferðarinnar.

Reglur um afhendingartíma eru notaðar til að stjórna uppfærslum á dagsetningum. Aðgerðir eru sjálfkrafa myndaðar þegar ferðasniðmát er notað fyrir ferð.

Til að bæta reglu um afhendingartíma við stjórnstöð rakningar skal fylgja þessum skrefum.

1. Fylgið einu af eftirfarandi skrefum:

    - Farið í **Heildarkostnaður \> Uppsetning ferðar með mörgum leggjum \> Leggir**. Veljið legginn sem á að setja upp afhendingartíma fyrir og því næst á aðgerðasvæðinu skal velja **Stjórnstöð rakningar**. Stjórnstöð rakningar er forhlaðin með upplýsingum um valda legginn.
    - Farið í **Heildarkostnaður \> Uppsetning afhendingarupplýsinga \> Stjórnstöð rakningar**. Því næst þarf að velja handvirkt legg í skrefi 4 í þessu ferli.

1. Á listasvæðinu skal stilla reitinn **Gerð stofnunar** á *Afhendingartími*.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Ef hafist var handa úr stjórnstöð rakningar í skrefi 1 skal stilla reitinn **Leggur** á legginn sem ætlunin er að stofna reglu afhendingartíma fyrir. Ef hafist var handa á síðunni **Leggir** er reiturinn **Leggur** forstilltur á legginn sem var valinn áður en stjórnstöð rakningar var opnuð.

    Í samræmi við gildið í reitnum **Leggur** verða nokkrir reitir stilltir sjálfkrafa eins og sýnt er hér:

    - **Upprunatafla:** *Gámaaðgerðir*
    - **Upprunareitur:** *Upphafsdagsetning*
    - **Marktafla:** *Gámaaðgerðir*
    - **Markreitur:** *Áætluð lokadagsetning*

1. Í reitnum **Aðgerð** skal velja aðgerðina sem núverandi regla ætti að gilda um.
1. Í reitinn **Afhendingartími** skal færa inn afhendingartímann (í dögum) sem á að nota þegar núverandi regla er ræst.

### <a name="status-update-rules"></a>Reglur stöðuuppfærslu

Færslur þar sem reiturinn **Gerð stofnunar** er stilltur á *Stöðuuppfærsla* mun uppfæra stöðu innkaupapöntunarlína eða stöðuna á stigi ferðar, flutningagáms eða fólíós. Hægt er að stilla stöður óháð hver annari. Notið þær til að upplýsa notandann eða deildina um stöðu ferðar (t.d. móttekin skjöl eða vörur í flutningi).

Þegar reiturinn **Gerð stofnunar** er stilltur á *Stöðuuppfærsla* inniheldur stjórnstöð rakningar flýtiflipann **Línur** þar sem hægt er að skilgreina kostnaðarþátt og uppfærða stöðu ferðarinnar. Til dæmis er lína þar sem reiturinn **Kostnaðarþáttur** er stilltur á *Gámur* og reiturinn **Staða ferðar** er stilltur á *Vörur í flutningi*. Í þessu tilviki, þegar pöntun lýkur tilteknum legg, mun reiturinn **Staða ferðar** fyrir flutningagáminn uppfærast í *Vörur í flutningi*.

Stöðuuppfærslur gefa upp stöðu ferðar í gegnum ferðalínur og innkaupapöntunarlínur sem tengjast þeirri ferð. Þar sem ferðinni vindur áfram frá höfninni, siglingu og tollum, yfir í vöruhús áfangastaðar býður reiturinn **Staða ferðar** í færslu ferðar upp á flýtiyfirlit yfir stigið sem vörurnar eru á.

Til að bæta reglu stöðuuppfærslu við Stjórnstöð rakningar skal fylgja þessum skrefum.

1. Fylgið einu af eftirfarandi skrefum:

    - Farið í **Heildarkostnaður \> Uppsetning ferðar með mörgum leggjum \> Leggir**. Veljið legginn sem á að setja upp stöðuuppfærslu fyrir og því næst á aðgerðasvæðinu skal velja **Stjórnstöð rakningar**. Stjórnstöð rakningar er forhlaðin með upplýsingum um valda legginn.
    - Farið í **Heildarkostnaður \> Uppsetning afhendingarupplýsinga \> Stjórnstöð rakningar**. Því næst þarf að velja handvirkt legg í skrefi 4 í þessu ferli.

1. Á listasvæðinu skal stilla reitinn **Gerð stofnunar** á *Stöðuuppfærslu*.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Ef hafist var handa úr stjórnstöð rakningar í skrefi 1 skal stilla reitinn **Leggur** á legginn sem ætlunin er að stofna reglu stöðuuppfærslu fyrir. Ef hafist var handa á síðunni **Leggir** er reiturinn **Leggur** forstilltur á legginn sem var valinn áður en stjórnstöð rakningar var opnuð.

    Í samræmi við gildið í reitnum **Leggur** verða nokkrir reitir stilltir sjálfkrafa eins og sýnt er hér:

    - **Upprunatafla:** *Gámaaðgerðir*
    - **Upprunareitur:** *Raunverulegur lokadagur*
    - **Marktafla:** Þessi reitur er hafður auður.
    - **Markreitur:** Þessi reitur er hafður auður.

1. Í reitnum **Verkþáttur** skal velja verkþáttinn sem reglan ætti að gilda um.
1. Á flýtiflipanum **Línur** skal slá inn stöðuuppfærslur fyrir hvert kostnaðarsvæði.

### <a name="blank-type-rules"></a>Reglur auðra lína

Færslur sem eru með gildið **Gerð stofnunar** sem *Autt* eru notaðar til að hnekkja eða færa inn reitargildi samkvæmt gögnum annars reits. Reitur úr heildarkostnaði mun skrifa yfir gögn á öðrum svæðum Microsoft Dynamics 365 Supply Chain Management samkvæmt reglum sem eru settar upp í stjórnstöð rakningar.

1. Farið í **Heildarkostnaður \> Uppsetning afhendingarupplýsinga \> Stjórnstöð rakningar**.
1. Á listasvæðinu skal stilla reitinn **Gerð stofnunar** á *Autt*.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Skilgreinið gildi upprunastaðar og áfangastaðar, samsvarandi gildi, afrita aðgerð og aðrar færibreytur sem eiga við eins og þörf krefur fyrir regluna.

### <a name="required-tracking-control-setup"></a>Nauðsynleg uppsetning rakningarstýringar

Fyrir hvert ferðasniðmát þarf að setja upp tvær færslur í stjórnstöð rakningar. Báðar þessar færslur eru með gildið **Gerð stofnunar** sem *Autt* og eru notaðar í öllum innleiðingum heildarkostnaðar. Þær tryggja að staðfest dagsetning innkaupa og væntanlegar dagsetningar fyrir vörur í flutningi séu uppfærðar fyrir ferðir og í tengdum innkaupapöntunarlínum eins og ætlast er til.

Fyrsta færslan er nauðsynleg til að uppfæra innkaupalínur. Eftirfarandi stillingar verða að vera til staðar:

- **Upprunatafla:** *Gámaaðgerðir*
- **Upprunareitur:** *Áætluð lokadagsetning*
- **Marktafla:** *Innkaupalínur*
- **Markreitur:** *Staðfest eða afhendingardagur*

Önnur færslan er nauðsynleg til að uppfæra færslur fyrir vörur í flutningi. Eftirfarandi stillingar verða að vera til staðar:

- **Upprunatafla:** *Gámaaðgerðir*
- **Upprunareitur:** *Áætluð lokadagsetning*
- **Marktafla:** *Vöruflutningspöntun*
- **Markreitur:** *Væntanleg dagsetning*
