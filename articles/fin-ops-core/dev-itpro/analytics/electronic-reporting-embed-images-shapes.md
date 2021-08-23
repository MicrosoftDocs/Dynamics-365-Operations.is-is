---
title: Felldu inn myndir og form í skjöl sem þú myndar með því að nota ER
description: Þetta efnisatriði útskýrir hvernig á að nota verkfæri rafrænnar skýrslugerðar til að búa til viðskiptaskjöl sem eru með innfelldar myndir og form.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 550ecca31af48e624e292b342d909abd6eb3e87af122f736eb388524b42f1e05
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730636"
---
# <a name="embed-images-and-shapes-in-documents-that-you-generate-by-using-er"></a>Felldu inn myndir og form í skjöl sem þú myndar með því að nota ER

[!include [banner](../includes/banner.md)]

Þú getur notað verkfæri rafrænnar skýrslugerðar til að hanna skýrslur sem þú getur keyrt til að búa til nauðsynleg rafræn skjöl. Hægt er að nota Microsoft Excel eða Microsoft Word skjöl til að tilgreina útlit skýrslu. Aðgerðarhönnuður rafrænnar skýrslugerðar gerir kleift að hengja Excel- eða Word-skjal við sem sniðmát fyrir skýrsluna. Tilgreindar einingar í viðhengdu sniðmáti tengjast sniðseiningum skýrslu í rafrænni skýrslugerð. Sniðseiningar skýrslunnar eru bundnar við gagnagjafa. Þessar einingar tilgreina gögnin sem verða slegin inn, á keyrslutíma, í skjölunum sem eru búin til.

Þessi nýja virkni er umfram núverandi möguleika rafrænnar skýrslugerðar til að búa til skjöl í Microsoft Office sniðum. Nánari upplýsingar er að finna í eftirfarandi verkleiðbeiningum. Þú getur fundið þessar verkleiðbeiningar undir þætti 7.5.4.3 Acquire/Develop IT service/solution (10677) viðskiptaferla.

- Rafræn skýrslugerð Hanna skilgreiningu til að mynda skýrslur á OPENXML-sniði
- Hanna rafræna skýrslugerð til að mynda skýrslur á sniði Microsoft WORD

## <a name="embed-an-image-in-an-excel-document"></a>Innfella mynd í Excel-skjali

### <a name="embed-an-image-in-an-excel-worksheet"></a>Innfella mynd í Excel-vinnublað

Fyrst þarf að bæta við staðgengli fyrir myndina í Excel-skjali. Opnaðu Excel-vinnubók og bættu við mynd sem staðgengli fyrir myndina sem þú bætir við síðar. Notaðu síðan verkfæri rafrænnar skýrslugerðar til að bæta nýrri skilgreiningu rafrænnar skýrslugerðar við til að hafa með skýrsluna sem er verið að hanna. Hengdu Excel-vinnubókina við sem sniðmát fyrir snið skýrslunnar og flyttu síðan innihald vinnubókarinnar inn í snið rafrænnar skýrslugerðar. Sniðskilgreiningin verður búin til sjálfkrafa. Staðgengill myndarinnar sem þú bættir við verður tekinn með í skilgreiningu á sniði rafrænnar skýrslugerðar sem einingin **CELL**.

> [!NOTE]
> Hægt er að tilgreina handvirkt skilgreiningu sniðs í stað þess að flytja það inn. Þegar þú vistar breytingarnar verður sniðið staðfest.

Því næst skal binda eininguna **CELL** fyrir snið rafrænnar skýrslugerðar við reitinn úr gagnagjafa sniðsins sem geymir gögn myndarinnar á tvíundarsniði við keyrslu. Þegar gagnalíkan rafrænnar skýrslugerðar er notað sem gagnagjafi sniðs verður gagnagerð reitsins að vera [Geymsla](er-formula-supported-data-types-composite.md#container). Sem stendur er hægt að binda reit gagnalíkans rafrænnar skýrslugerðar sem er með gagnagerðina [Geymsla](er-formula-supported-data-types-composite.md#container) við ýmsar gerðir af gagnagjöfum sem skila myndum á tvíundarsniði. Hægt er að fá aðgang að reit í gagnatöflu og skrá sem tengd er við skrá gagnatöflunnar með því að nota skjalastjórnunarrammann.

> [!IMPORTANT]
> - Ef þú vilt fylla út staðgengil myndarinnar í skjalinu sem þú ert að búa til með því að nota Excel-sniðmátið, verður snið rafrænnar skýrslugerðar að innihalda eininguna **CELL** sem vísar í tilgreinda myndeind í Excel-sniðmátinu. Að öðrum kosti mun engin staðgengilsmynd birtast í útkomu skýrslunnar. Ef binding á **CELL** einingu skilar engum gögnum við keyrslu mun skjalið sem myndast sýna staðgengil myndarinnar úr sniðmátinu. Til að fela mynd í skjalinu sem þú ert að búa til skaltu skilgreina **CELL** einingu og tilgreina að segðin **Virkjar** eigi að skila gildinu **FALSE**.
> - Í Excel-sniðmátinu skal nota einkvæmt heiti fyrir hverja einingu. Þessar einingar fela í sér myndir og hólf. Ef þú tvítekur heiti einingar verður efni skýrslunnar sem er gerð óljóst og ruglingslegt.

### <a name="embed-images-in-the-header-and-footer-of-an-excel-worksheet"></a>Fella myndir inn í síðuhaus og síðufót Excel-vinnublaðs

Notaðu skjal Excel-vinnubókar sem sniðmát til að velja útlit skýrslu. Vinnubókin getur innihaldið mörg vinnublöð sem hvert um sig er hægt að hanna þannig að hún sé með síðuhaus og síðufót. Excel styður allt að þrjár myndir í síðuhaus og síðufót fyrir hvert vinnublað. Hægt er að hliðra myndunum til vinstri, hægri eða miðjusetja þær.

Í Finance útgáfu 10.0.21 er hægt að stjórna myndum í síðuhaus og síðufót sem eru búnar til af lausn rafrænnar skýrslugerðar sem er með Excel-sniðmát.

Ef þú vilt að sjálfgefin mynd birtist í síðuhaus eða síðufæti skjals sem búið er til, er hægt að bæta mynd við síðuhaus eða síðufót vinnublaðs fyrir sniðmát rafrænnar skýrslugerðar. Til að fá aðgang að þessari mynd í sniði rafrænnar skýrslugerðar þarf að bæta við hlutnum **Mynd** undir [Síðuhaus](er-fillable-excel.md#header-component) eða [Síðufót](er-fillable-excel.md#footer-component) sniðsins. Skilgreindu stillinguna á **Myndhlutanum** eins og hentar. 

Einnig er hægt að nota **Myndhlutann** til að setja myund í síðuhaus eða síðufót á mynduðu skjali við keyrslu, jafnvel þótt sniðmátið innihaldi enga sjálfgefna mynd. Til að tilgreina margmiðlunarefni sem á að setja í síðuhaus eða síðufót myndaðs skjals sem annaðhvort ýja mynd eða staðgengil fyrir sjálfgefna mynd þarf að binda **Myndhlutann** við gagnagjafa af gerðinni [Geymsla](er-formula-supported-data-types-composite.md#container) sem stendur fyrir mynd á tvíundarsniði.

Hver hlutur **Síðuhauss** og **Síðufótar** getir geymt einn **Myndhluta** fyrir hverja studda textajöfnun: **Vinstri**, **Miðja** og **Hægri**.

Eiginleikinn **Skala hæðina** í **Myndhlutanum** gerir þér kleift að skilgreina bindingu til að stjórna stærð myndar:

- Veldu **Upprunalegt** til að halda upprunalegri stærð myndarinnar.
- Veldu **Hlutfallslegt** til að skala hæð myndarinnar í hlutfalli við hæð síðuhaussins eða síðufótarins þar sem myndin er.

    - Í þessu tilviki verður að skilgreina hæð myndarinnar sem prósentu af yfireiningu síðuhauss eða síðufótar.
    - Ef skölunargildið fer yfir 100 prósent gæti myndin farið yfir gagnasvæði samsvarandi vinnublaðs.
    - Ef hæð myndarinnar er breytt þegar skölun er notuð breytist breiddin líka til að viðhalda upprunalegu myndhlutfalli myndarinnar.

- Veldu **Fast** til að breyta myndstærðinni samkvæmt gildum hæðar og breiddar (í pixlum) sem gefin eru upp á hönnunartíma.

    - Ef uppgefin hæð er meiri en hæð yfireiningar síðuhauss eða síðufótar gæti myndin farið út fyrir gagnasvæði samsvarandi vinnublaðs.

Einnig er hægt að nota eiginleikann **Virkjað** fyrir **Myndhlutann** til að stjórna sýnileika myndar sem er sett í myndað skjal með því að nota þennan hluta.

> [!NOTE]
> Þú verður að nota sniðshönnuð rafrænnar skýrslugerðar til að bæta **Myndhluta** við breytanlegt snið rafrænnar skýrslugerðar. Ekki er hægt að bæta við hlutanum þegar vinnusvæðið [Stjórnun viðskiptaskjala](er-business-document-management.md) er notað til að breyta sniðmáti viðskiptaskjals.

Til að fá frekari upplýsingar um þessa virkni skal fylgja skrefunum í [Hanna snið rafrænnar skýrslugerðar til að mynda skýrslu á Excel-sniði með innfelldum myndum í síðuhausum eða síðufótum](er-embed-images-header-footer-excel-reports.md).

## <a name="embed-a-shape-in-an-excel-document"></a>Fella form inn í Excel-skjal

Fyrst þarf að bæta við staðgengli fyrir formið í Excel-skjali. Opnaðu Excel-vinnubók og veldu **Form**, **Textareit** eða **WordArt** sem staðgengil fyrir formið. Notaðu síðan verkfæri rafrænnar skýrslugerðar til að bæta nýrri skilgreiningu rafrænnar skýrslugerðar við til að hafa með skýrsluna sem er verið að hanna. Hengdu Excel-vinnubókina við sem sniðmát fyrir snið skýrslunnar og flyttu síðan innihald vinnubókarinnar inn í snið rafrænnar skýrslugerðar. Sniðskilgreiningin verður búin til sjálfkrafa. Staðgengill formsins sem þú bættir við verður tekinn með í skilgreiningu á sniði rafrænnar skýrslugerðar sem **CELL** eining sem vísar í tilgreinda einingu Excel-forms.

> [!NOTE]
> Hægt er að tilgreina handvirkt skilgreiningu sniðs í stað þess að flytja það inn. Þegar þú vistar breytingarnar verður sniðið staðfest.

Því næst skal binda **CELL** einingu á sniði rafrænnar skýrslugerðar við reitinn úr gagnagjafa sniðsins sem geymir gögnin við keyrslu. Hægt er að breyta þessum gögnum í textastreng. Þegar **CELL** einingin í sniði rafrænnar skýrslugerðar vísar í formeiningu í Excel-sniðmát sem styður texta, textann sem er gefinn upp í gegnum þessa bindingu við keyrslu mun koma fram í formi í skjali sem er myndað.

> [!IMPORTANT]
> - Ef nota á Excel-sniðmátið sem inniheldur staðgengil formsins til að búa til nýtt skjal verður snið rafrænnar skýrslugerðar að innihalda **CELL** einingu sem vísar í einingu Excel-sniðsins. Að öðrum kosti mun ekkert staðgengilsform birtast í útkomu skýrslunnar. Ef binding á **CELL** einingu sem vísar á tilgreinda einingu Excel-forms skilar engum gögnum við keyrslu mun skjalið sem myndast sýna texta fyrir staðgengil formsins úr Excel-sniðmátinu. Til að fela form í skjalinu sem er myndað skal skilgreina **CELL** einingu sem vísar á tilgreinda einingu Excel-forms og tilgreina að segðin **Virkjar** eigi að skila gildinu **FALSE**.
> - Í Excel-sniðmátinu skal nota einkvæmt heiti fyrir hverja einingu. Þessar einingar eru meðal annars form og hólf. Ef þú tvítekur heiti einingar verður efni skýrslunnar sem er gerð óljóst og ruglingslegt.

## <a name="embed-an-image-in-a-word-document"></a>Innfella mynd í Word-skjali
> [!IMPORTANT]
> Hægt er að endurnýta snið rafrænnar skýrslugerðar sem notar Excel-sniðmát til að búa til skjöl sem innihalda innfelldar myndir. Á sniði rafrænnar skýrslugerðar skal ganga úr skugga um heiti sé tilgreint fyrir **CELL** einingu sem vísar í tilgreinda myndeind í Excel og sem er bundin við gagnagjafa sem skilar mynd við keyrslu.

Fyrst verður að skilgreina útlit Word-skjalsins. Notaðu stýringuna **Innihald myndar** til að búa til staðgengil fyrir innfellda mynd. Til að fá aðgang að þessari stýringu þarf fyrst að gera flipann **Þróunaraðili** sýnilegan á Word-borðanum.

Því næst skaltu eyða Excel-sniðmátinu úr sniði rafrænnar skýrslugerðar og hengja skjal Word-sniðmátsins við. Uppfærðu tilvísunina í sniðmátið og vistaðu breytingarnar. Skipulag núverandi sniðs rafrænnar skýrslugerðar er vistað í Word-sniðmátið sem nýr sérstilltur XML-hluti sem heitir **Skýrsla**.

Því næst skal vista Word-sniðmátið fyrir núverandi snið rafrænnar skýrslugerðar á staðbundna tölvu. Opnaðu sniðmátið og opnaðu svæðið **XML-vörpun**. Finndu sérstilltan XML-hluta sem heitir **Skýrsla** og bentu síðan á **CELL** eininguna í skýrslu rafrænnar skýrslugerðar sem er bundin við gagnagjafa sem skilar mynd á tvíundarsniði. Varpaðu þessu atriði XML-hluta í valda stýringu fyrir **Innihald myndar** og vistaðu breytingarnar.

[![fella inn myndir.](./media/embed-images-shapes-01.png)](./media/embed-images-shapes-01.png)

Að lokum skaltu eyða Word-sniðmátinu úr sniði rafrænnar skýrslugerðar og hengja Word-skjalið við sem inniheldur varpaða sérstillta XML-hluta. Uppfærðu sniðstilvísun í sniðmátið og vistaðu breytingarnar sem þú gerðir á þessu sniði rafrænnar skýrslugerðar.

## <a name="more-information"></a>Meiri upplýsingar
Til að kynna sér smáatriðin í þessum eiginleika skaltu spila verkleiðbeiningasafnið, **Rafræn skýrslugerð - Gera skýrslur á MS Office-sniði með innfelldum myndum**. Þessar verkleiðbeiningar sýna þér hvernig þú getur fellt inn myndir af lógói fyrirtækis og heimilaða undirskrift einstaklings í greiðsluávísunum sem eru búnar til með því að nota verkfæri rafrænnar skýrslugerðar í Excel- og Word-skjölum.

Í eftirfarandi töflu er listi yfir skrár sem þarf til að ljúka við verkleiðbeininguna **Rafræn skýrslugerð - Gera skýrslur á MS Office-sniði með innfelldum myndum**. Sæktu og vistaðu skrárnar á staðbundna tölvu.

| lýsing                                          | Skrárnafn                   |
|------------------------------------------------------|-----------------------------|
| Skilgreining á gagnalíkani í ER                          | [Model for cheques.xml](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| ER Sníða skilgreiningu                              | [Cheques printing format.xml](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| Mynd af merki fyrirtækis                                   | [Company logo.png](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| Mynd af undirskrift                                      | [Signature image.png](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| Önnur mynd af undirskrift                          | [Signature image 2.png](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| Microsoft Word-sniðmát fyrir prentun greiðsluávísana  | [Cheque template Word.docx](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |
| Microsoft Excel-sniðmát fyrir prentun greiðsluávísana | [Cheque template.xlsx](https://download.microsoft.com/download/1/f/6/1f671963-73aa-48d5-ae69-45f21fe7dfb4/Cheque%20template.xlsx)        |

Eftirfarandi mynd sýnir dæmi um prufuprentun á greiðsluávísun sem er búin til úr Excel-sniðmáti.

[![Prufuprentun greiðsluávísunar.](./media/embed-images-shapes-02.png)](./media/embed-images-shapes-02.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
