---
title: Stilla afurðarvíddargildi þannig að þau birtist sem sýnishorn
description: Í þessu efnisatriði er lýst hvernig skilgreina afurðarvíddargildi sem sýnishorn í miðstöð Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-09-20
ms.dyn365.ops.version: Retail 10.0.20 update
ms.openlocfilehash: 08564ce7af7412f2501b917b3496942004402611
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117228"
---
# <a name="configure-product-dimension-values-to-appear-as-swatches"></a>Stilla afurðarvíddargildi þannig að þau birtist sem sýnishorn

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

Í þessu efnisatriði er lýst hvernig skilgreina afurðarvíddargildi sem sýnishorn í miðstöð Microsoft Dynamics 365 Commerce. Upplýsingar um afurðarvíddir er að finna í [Afurðarvíddir](../../supply-chain/pim/product-dimensions.md).

Dynamics 365 Commerce styður notkun stærðar-, stíls- og litavídda til að tákna afurðarafbrigði. Afurðarvíddir eru með stutt heiti sem eru sýnd á upplýsingasíðum afurða þannig að hægt sé að velja afurðarafbrigði. Dæmi um þessi stuttu heiti eru „Lítið“, „Miðlungs“ og „Stórt“ fyrir stærðir og „Svart“ og „Brúnt“ fyrir liti. Ef afurð styður hinsvegar mörg afbrigði þarf fjölval til að skoða myndina fyrir hvert afurðarafbrigði. Þess vegna getur það verið hægt og leiðinlegt ferli fyrir viðskiptavini að skoða og velja afurðarafbrigði.

Þegar víddir eru sýndar sem sýnishorn á upplýsingasíðum afurða fá viðskiptavinir að forskoða afbrigði afurða. Þeir geta auðveldlega skoðað marga liti, mynstur og áferðir og skoðað mismunandi samsetningar af vöruafbrigðum.

Birtingareiginleiki vídda sem sýnishorn gerir Commerce kleift að nota sextándakerfiskóði og myndir til að sýna víddir sem sýnishorn. Auk þess er hægt að flokka svipaðar víddir, eins og liti, á listasíðum afurða. Til dæmis er viðskiptavinur að leita að vörum sem eru bláar. Ef ýmis blá víddargildi eru flokkuð saman sýnir listasíða leitarniðurstöðu afurðir sem eru með mismunandi litbrigði af bláum. Víddaflokkun bætir afmörkunarupplifun afurðar umtalsvert og auðveldar viðskiptavinum að finna fleiri afurðir í gegnum eina leitarfyrirspurn afurðar.

> [!NOTE]
> Birtingareiginleiki vídda sem sýnishorn er í boði frá og með Dynamics 365 Commerce-útgáfu 10.0.20.

Eftirfarandi mynd sýnir dæmi þar sem litir birtast sem litaspjald á upplýsingasíðu afurðar í Commerce.

![Dæmi um liti sem sýndir eru sem litaspjald á upplýsingasíðu afurðar](../dev-itpro/media/swatch_pdp.png)

Eftirfarandi mynd sýnir dæmi þar sem litir birtast sem litaspjald á listasíðu leitarniðurstaðna í Commerce.

![Dæmi um liti sem sýndir eru sem litaspjald á listasíðu leitarniðurstaðna](../dev-itpro/media/swatch_searchresults.PNG)

## <a name="enable-the-display-dimensions-as-swatches-feature-in-commerce-headquarters"></a>Virkja birtingareiginleika vídda sem sýnishorn í Commerce Headquarters

Til að virkja birtingareiginleika vídda sem sýnishorn í Commerce Headquarters skal fara í **Vinnusvæði \> Eiginleikastjórnun** og kveikja á eiginleikanum **Virkja stuðning við mynd fyrir afurðarvíddargildi**. Þegar þessi eiginleikafáni er virkjaður eru þremur nýjum reitum bætt við fyrir hverja vídd í viðeigandi töflum í Commerce Headquarters: **Sextándakerfiskóði**, **URL** (fyrir myndir) og **RefinerGroup**.

## <a name="configure-dimension-values-in-commerce-headquarters"></a>Skilgreining víddargilda í Commerce Headquarters

Birtingareiginleiki vídda sem sýnishorn er studdur fyrir stærðar-, stíls- og litavíddir. Hægt er að tilgreina gildi sextándakerfiskóða og myndavefslóðar fyrir viðeigandi víddir í Commerce Headquarters. Ef gildi sextándakerfiskóða og myndavefslóðar eru ekki gefin upp fyrir vídd mun kerfið sjálfkrafa sýna textann á stuttu heiti víddar.

Skilgreininguna er hægt að gera á einhverju eftirfarandi stigi:

- **Vídd** – Opnið síðuna fyrir vídd í Commerce Headquarters með því að leita að **Lit**, **Stærð** eða **Stíl**. Á hverri síðu er listi yfir víddargildin. Hægt er að stýra birtingarröðun, sextándakerfiskóða og vefslóðargildum mynda. Eftirfarandi mynd sýnir dæmi um stillingar á síðunni **Litir**.

    ![Dæmi um skilgreiningu víddar á litasíðunni](../dev-itpro/media/swatch_Color.PNG)

- **Víddaflokkur** – Í Dynamics 365 Commerce er hægt að nota eiginleikann **RefinerGroup** til að stofna víddaflokka. Ef víddaflokkar eru skilgreindir skal opna viðeigandi síðu með því að leita að **Litaflokki**, **Stærðarflokki** eða **Stílflokki**. Á hverri síðu er hægt að stjórna flokkagildum sextándakerfiskóða, myndavefslóðar og afmörkunar. Eftirfarandi mynd sýnir dæmi um stillingar á síðunni **Litaflokkar**.

    ![Dæmi um skilgreiningu víddar á síðu litaflokks](../dev-itpro/media/swatch_colorGroup.PNG)

- **Afurðarvídd (við stofnun afurðar)** – Þegar ný afurð er stofnuð er hægt að nota síðuna **Afurðarvíddir** til að slá inn víddargildin. Fyrir núverandi afurðir er mögulega búið að stilla reitina **Sextándakerfiskóði**, **URL** (fyrir myndir) og **RefinerGroup**. Þó er hægt að breyta gildinu eins og nauðsynlegt er. Eftirfarandi mynd sýnir dæmi um skilgreiningu á síðunni **Afurðarvíddir**.

    ![Dæmi um skilgreiningu víddar á síðu afurðarvídda](../dev-itpro/media/swatch_product_dimensions.PNG)

> [!NOTE]
> Ferlið við stjórnun skilgreininga á sextándakerfiskóða og myndavefslóðar fylgir sama mynstrinu og er notað til að stjórna birtingarröð vídda.

## <a name="configure-dimension-values-by-using-hex-codes"></a>Skilgreina víddargildi með sextándakerfiskóðum

Fyrir flestar litastærðir ætti að gefa upp litagildi sextándakerfiskóða á víddarsíðum í Commerce Headquarters. Til dæmis ætti svarti liturinn að hafa hexkóðagildið **#00000**. Þegar Commerce sýnir síðu vefsvæðis er sextándakerfiskóðinn táknaður með litaspjaldi.

Eftirfarandi mynd sýnir dæmi þar sem litavíddir eru skilgreindar með því að nota gildi sextándakerfiskóða.

![Dæmi um skilgreiningu víddar sem notar sextándakerfiskóða](../dev-itpro/media/swatch_color_hexcode.png)

## <a name="configure-dimension-values-by-using-image-urls"></a>Skilgreina víddargildi með myndavefslóðum

Sumar litavíddir tákna mynstur, ekki fasta liti. Til dæmis gæti litavídd verið lýst sem „hlébarða“. Í slíkum tilvikum er hægt að sýna litavíddir á skilvirkari hátt með því að nota birtar myndir í stað sextándakerfiskóða fyrir litaspjöld.

Hlaða verður upp hverri mynd í vefsmið Commerce og birta hana. Færið síðan inn vefslóð myndar fyrir birtu myndina á viðeigandi víddarsíðum í Commerce Headquarters. Ef valið hefur verið að birta vídd sem sýnishorn, en sextándakerfiskóði er ekki skilgreindur, mun Commerce fletta upp myndum þegar það sýnir síðuna. Ef uppfletting myndar mistekst mun Commerce sýna textann á stuttu heiti víddar.

Eftirfarandi mynd sýnir dæmi þar sem vefslóðir mynda eru notaðar í skilgreiningu á síðunni **Litir**.

![Dæmi um skilgreiningu víddar sem notar vefslóðir mynda](../dev-itpro/media/swatch_color_urls.PNG)

Hægt er að nota sniðmát miðils til að skilgreina vefslóðir mynda, rétt eins og hægt er að gera fyrir myndir afurða og flokka. Þegar myndir eru hlaðnar upp í vefsmið þarf að vera samræmi í venjum skráarheita og skráarslóða.

Eftirfarandi mynd sýnir dæmi þar sem vefslóðir mynda eru notaðar í skilgreiningu á sniðmáti miðils.

![Dæmi um skilgreiningu á sniðmáti miðils](../dev-itpro/media/swatch_media_template.PNG)

## <a name="configure-dimension-values-by-using-both-hex-codes-and-image-urls"></a>Skilgreina víddargildi með bæði sextándakerfiskóðum og myndavefslóðum

Fyrir flestar litavíddir er hægt að skilgreina bæði sextándakerfiskóða og myndavefslóðir. Svörunarregla vegna myndþýðingar Commerce leitar sjálfkrafa að annaðhvort sextándakerfiskóða eða myndavefslóð til að sýna litaspjald. Með því að nota bæði sextándakerfiskóða og myndavefslóðir til að skilgreina litavíddir er myndastjórnun einfölduð þegar fjöldi lita er mikill.

Eftirfarandi mynd sýnir dæmi þar sem bæði sextándakerfiskóðar og vefslóðir mynda eru notaðar í skilgreiningu á síðunni **Litir**.

![Dæmi um skilgreiningu víddar sem notar bæði sextándakerfiskóða og vefslóðir mynda](../dev-itpro/media/swatch_color_hexandimage.png)

## <a name="configure-refiner-groups"></a>Skilgreina afmörkunarflokka

Þegar sextándakerfiskóði eða myndavefslóð er skilgreind fyrir víddargildi er einnig hægt að tilgreina gildi fyrir reitinn **RefinerGroup**. Þessi reitur skilgreinir víddina sem nota á til að flokka saman svipuð víddargildi í upplifun afmörkunar.

Ef víddargildi lita eru til dæmis „blár“, „bláköflóttur“, „tær blár“ og „dökkblár“ er hverju gildi varpað í mismunandi sextándakerfiskóða eða myndavefslóð. Þar af leiðandi birtist hvert gildi sem mismunandi litur á upplýsingasíðum afurða og afurðarspjöldum fyrir viðeigandi afurðir. Ef öllum þessum víddargildum lita er hinsvegar varpað í gildi **RefinerGroup** fyrir **Bláan** mun leit að „bláum“ afurðum leiða til leitarniðurstaðna á listasíðu fyrir afurðir sem eru með litavíddargildin „blár“, „bláköflóttur“, „tær blár“ og „dökkblár“.

Dæmið í eftirfarandi mynd sýnir venslin milli eiginleikanna **Litur** og **RefinerGroup** í Commerce Headquarters.

![Dæmi um stjórnun afmörkunarflokks](../dev-itpro/media/swatch_refiner_group.png)

## <a name="manage-images-in-commerce-site-builder"></a>Stjórna myndum í Commerce Site Builder

Ef vefslóðir mynda eru notaðar fyrir einhver víddargildi þarf að hlaða samsvarandi myndum upp í vefsmið Commerce. Staðsetning hverrar myndar verður að samsvara skrárheiti og möppuslóð sem eru skilgreind fyrir myndina í Commerce Headquarters. Hlaða verður upp myndaskrám í viðeigandi staðsetningar flokka í vefsmið. Til dæmis verður að hlaða upp litamyndum í möppuflokkinn **Litur**. Frekari upplýsingar um hvernig á að hlaða upp myndum í vefssmið er að finna í [Hlaða upp myndum](../dam-upload-images.md).

Eftirfarandi mynd sýnir dæmi þar sem svarglugginn **Hlaða upp skrám** er notaður til að hlaða upp myndum í miðlasafn vefsmiðs. Hún undirstrikar flokkana **Stærð**, **Litur** og **Stíll** sem er hægt að velja.

![Dæmi um flokka myndaskráa við upphleðslu í miðlasafn vefsmiðs](../dev-itpro/media/swatch_sitebuilder.png)

## <a name="enable-swatch-display-on-e-commerce-site-pages"></a>Virkja birtingu sýnishorns á síðum rafrænna viðskipta

Áður en sýnishorn geta birst á síðum rafrænna viðskipta sem þurfa víddarval, eins og upplýsingasíður afurða og listasíður, þarf að skilgreina svæðisstillingar vídda í Commerce Headquarters. Frekari upplýsingar er að finna í [Nota svæðisstillingar fyrir víddir](../dimension-settings.md).

Auk þess ætti að virkja eiginleikann **Hafa afurðareigindir með í leitarniðurstöðum** fyrir einingar leitarniðurstaðna. Ef svæðið notar sérstilltar flokkasíður ætti að uppfæra einingar leitarniðurstaðna sem eru notaðar á þessum síðum þannig að eiginleikinn **Hafa afurðareigindir með í leitarniðurstöðum** sé virkjaður. Frekari upplýsingar er að finna í [Leitarniðurstöðueining](../search-result-module.md).

## <a name="display-swatches-in-pos-and-other-channels"></a>Sýna sýnishorn á sölustað og öðrum rásum

Sem stendur er Commerce ekki með tilbúna uppsetningu sem styður birtingu sýnishorna á sölustað og í öðrum rásum. Hins vegar er hægt að innleiða virkni fyrir birtingu sýnishorns sem viðbót sem gerir að verkum að API rása skilar sextándakerfiskóðum og myndavefslóðum sem þarf til að birta sýnishorn.

## <a name="additional-resources"></a>Frekari upplýsingar

[Leitarniðurstöðueining](../search-result-module.md)

[Nota svæðisstillingar fyrir víddir](../dimension-settings.md)

[Afurðarvíddir](../../supply-chain/pim/product-dimensions.md)

[Hlaða upp mynd](../dam-upload-images.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
