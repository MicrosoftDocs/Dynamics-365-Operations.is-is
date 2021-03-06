---
title: Tölvupóstur ER-gerð áfangastaðar
description: Þetta efnisatriði útskýrir hvernig á að skilgreina áfangastað tölvupósts fyrir hverja MÖPPU eða SKRÁARHLUTA rafræns skýrslugerðarsniðs.
author: NickSelin
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: a575c04a5042e4db08f387bc7bce46225c109844
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753505"
---
# <a name="email-er-destination-type"></a>Tölvupóstur ER-gerð áfangastaðar

[!include [banner](../includes/banner.md)]

Þegar snið rafrænnar skýrslugerðar er keyrt er hægt að mynda eitt eða fleiri skjöl á útleið. Sniðsíhlutirnir **Mappa** eða **Skrá** eru notaðir í ER-sniðinu til að tilgreina skipulagið á skjölum á útleið. Hægt er að skilgreina áfangastað tölvupósts fyrir þessar gerðir íhluta til að senda skjöl á útleið sem tölvupóstviðhengi.

Hægt er að stilla áfangastað tölvupósts fyrir hverja **Möppu** eða **Skrá** á rafrænu skýrslugerðarsniði. Í slíku tilviki **er hvert skjal á útleið sent í tölvupósti hvert fyrir sig**. Byggt á þessari stillingu á áfangastað, er myndað skjal afhent sem viðhengi í tölvupósti. 

> [!NOTE]
> Ef ekkert skjal er myndað vegna þess að segðin **Virkjuð** fyrir viðkomandi íhlut **Skráar** hefur verið grunnstillt til að skila Boole-gildinu **Rangt**, er enginn tölvupóstur sendur þó að viðtökustaður tölvupósts sé grunnstilltur og virkur fyrir hlutinn.

Einnig er hægt að [flokka](#grouping) nokkrar íhluti fyrir **Möppu** og **Skrá** saman og síðan grunnstilla viðtökustað tölvupósts fyrir alla íhlutina í flokknum. Í þessu tilfelli eru öll skjöl á útleið mynduð af íhlutum sem tilheyra flokknum **eru send sem mörg viðhengi í einum tölvupósti**. Byggt á þessari stillingu á áfangastað, er hvert myndað skjal afhent sem viðhengi í einum tölvupósti.

> [!NOTE]
> Ef að minnsta kosti eitt skjal er myndað af íhlutinum **Skrá** í flokki íhluta er tölvupóstur sendur. Ef ekkert skjal er myndað af flokkuðum íhlutum vegna þess að segðin **Virkjuð** fyrir íhlut **Skráar** hefur verið grunnstillt til að skila Boole-gildinu **Rangt**, er enginn tölvupóstur sendur þó að viðtökustaður tölvupósts sé grunnstilltur og virkur fyrir þann flokk íhluta.
>
> **Netfang** er eini viðtökustaðurinn sem hægt er að skilgreina fyrir flokk íhluta. Til að afhenda skjal sem er sent í tölvupósti samkvæmt stillingu á viðtökustað tölvupósts fyrir flokk, skal bæta við einni færslu viðtökustaðar, velja íhlutinn sem óskað er eftir og skilgreina svo annan viðtökustað fyrir þessa færslu.

Hægt er að skilgreina marga flokka íhluta fyrir grunnstillingu á einu ER-sniði. Á þennan hátt er hægt að skilgreina viðtökustað tölvupósts fyrir hvern hóp íhluta og viðtökustað tölvupósts fyrir hvern íhlut.

## <a name="configure-an-email-destination"></a>Skilgreina áfangastað tölvupósts

Til að senda úttaksskrá eða nokkrar úttaksskrár í tölvupósti, á síðunni **Viðtökustaður rafrænnar skýrslugerðar**, í flýtiflipanum **Viðtökustaður skráar**, skal velja íhlut eða flokk íhluta í hnitanetinu og velja síðan **Stillingar**. Í svarglugganum **Stillingar viðtökustaðar** sem birtist, í flipanum **Netfang**, skal stilla valkostinn **Virkjað** á **Já**. Þá er hægt að tilgreina viðtakendur tölvupósts og breyta efni og meginmál tölvupóstsins. Annaðhvort er hægt að setja upp fastan texta fyrir efni og meginmál tölvupósts eða nota [formúlur](er-formula-language.md) rafrænnar skýrslugerðar til að stofna gagnvirkt texta tölvupósts.

Hægt er að grunnstilla netföng fyrir rafræn skýrslugerð á tvo vegu. Hægt er að ljúka grunnstillingunni á sama hátt og eiginleiki prentstýringar lýkur henni, eða finn út netfang með því að nota beina tilvísun í skilgreiningu rafrænnar skýrslugerðar í gegnum formúlu.

[![Valkostur virkjunar stilltur á Já fyrir viðtökustað tölvupósts](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)

## <a name="email-address-types"></a>Gerðir tölvupóstfanga

Ef valið er **Breyta** við hliðina á reitunum **Til** eða **Cc** í svarglugganum **Stillingar viðtökustaðar**, birtist svarglugginn **Senda tölvupóst til**. Veljið **Bæta við** og svo rétta gerð tölvupóstfangs til að nota. Tvær gerðir eru í augnablikinu studdar: **Tölvupóstur vegna prentstýringar** og **Tölvupóstur grunnstillingar**.

[![Val á gerð tölvupóstfangs](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)

### <a name="print-management-email"></a>Tölvupóstur vegna prentstýringar

Ef valið er **Tölvupóstur vegna prentstýringar** sem tegund tölvupóstfangs, er hægt að slá inn föst tölvupóstföng í svargluggann **Senda tölvupóst til** með því að stilla eftirfarandi reiti:

- Í reitnum **Uppruni tölvupósts** skal velja **Enginn**.
- Í reitinn **Viðbótarnetföng, aðskilin með „;“** skal slá inn föst netföng.

Að öðrum kosti er hægt að fá netföng frá tengiliðaupplýsingum aðilans sem skjal á útleið er búið til fyrir. Til að nota tölvupóstföng sem eru ekki föst, skal í reitnum **Uppruni tölvupósts** velja [hlutverk](../../fin-ops/organization-administration/overview-global-address-book.md#party-roles) aðilans fyrir viðtökustað skráar. Eftirfarandi hlutverk eru studd:

- Viðskiptavinur
- Lánardrottinn
- Viðfang
- Tengiliður
- Keppinautur
- Starfsmaður
- Umsækjandi
- Væntanlegur lánardrottinn
- Bannaður lánardrottinn

Til dæmis til að grunnstilla viðtökustað tölvupósts fyrir ER-snið sem er notað til að vinna úr lánardrottnagreiðslum skal velja hlutverkið **Lánardrottinn**.

Þegar búið er að velja æskilegt hlutverk skal velja hnappinn **Binda** (keðjutákn) við hliðina á reitnum **Upprunareikningur tölvupósts** til að opna síðuna [Formúluhönnuður](general-electronic-reporting-formula-designer.md). Síðan er hægt að nota þessa síðu til að grunnstilla formúlu sem skilar við keyrslu lykilnúmeri aðilans sem úthlutað er á skilgreindu hlutverki úr unna skjalinu á viðtökustað tölvupóstsins.

> [!NOTE]
> Formúlur eru við tilgreindar fyrir skilgreiningu rafrænnar skýrslugerðar.

Á síðunni **Formúluhönnuður**, í reitinn **Formúla**, skal slá inn skjalatilvísun í stutt hlutverk. Í stað þess að slá tilvísunina inn í svæðið **Gagnagjafi** skal finna og velja þann gagnagjafahnútinn sem stendur fyrir lykil skilgreinda hlutverksins og síðan velja **Bæta við gagnagjafa** til að uppfæra formúluna. Til dæmis ef viðtökustaður tölvupóstsins er skilgreindur fyrir skilgreininguna **ISO 20022 Kreditfærsla** sem er notuð til að vinna úr greiðslum lánardrottins, er hnúturinn sem stendur fyrir lánardrottnalykil `'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.

![Skilgreining uppruna tölvupóstfangs](./media/er_destinations-emaildefineaddresssource.gif)

Ef lykilnúmer skilgreinda hlutverksins eru einkvæm fyrir allt tilvik Microsoft Dynamics 365 Finance, má reiturinn **Fyrirtæki tölvupóstsuppruna** í svarglugganum **Senda tölvupóst til** vera áfram auður.

Einnig gæti komið um sú staða þar sem mismunandi aðilar í [Altækri aðsetursbók](../../fin-ops/organization-administration/overview-global-address-book.md) hafi verið skráðir í mismunandi fyrirtæki ([lögaðilar](../../fin-ops/organization-administration/organizations-organizational-hierarchies.md#legal-entities)) á þann hátt að þeir nota allir sama lykilnúmerið til að fylla út skilgreint hlutverk. Í þessu tilviki eru lykilnúmer fyrir skilgreint hlutverk ekki einkvæm fyrir allt Finance-tilvikið. Til að velja ákveðinn aðila er þess vegna ekki hægt að tilgreina aðeins lykilnúmer. Einnig þarf að tilgreina fyrirtækið sem aðilinn hefur verið skráður í til að fylla út skilgreint hlutverk. Velja skal hnappinn **Binda** (keðjutáknið) við hliðina á reitnum **Fyrirtæki tölvupóstsuppruna** í svarglugganum **Senda tölvupóst til** til að opna síðuna [Formúluhönnuður](general-electronic-reporting-formula-designer.md). Síðan er hægt að nota þessa síðu til að skilgreina formúlu sem skilar við keyrslu kóða fyrirtækisins sem æskilegur uppruni verður að finnast í.

> [!TIP]
> Ef nauðsynlegt er að nota fyrirtækjakóða til að keyra snið rafrænnar skýrslugerðar, en snið rafrænnar skýrslugerðar veitir engan gagnagjafa þar sem hægt er að ná í fyrirtækjakóðann, skal skilgreina `GetCurrentCompany()` formúluna með því að nota innbyggðu aðgerðina [GETCURRENTCOMPANY](er-functions-other-getcurrentcompany.md) fyrir rafræna skýrslugerð.

> [!NOTE]
> Formúlur eru við tilgreindar fyrir skilgreiningu rafrænnar skýrslugerðar.

Til að tilgreina gerð netfanga sem þarf að nota við keyrslu skal í svarglugganum **Senda tölvupóst til** velja **Breyta** við hliðina á reitnum **Til** til að opna fellilistann **Úthluta netfangi**. Stillið svo eftirfarandi reiti:

- Í reitnum **Tilgangur** skal velja tilganginn sem á við. Aðeins netföng valins tilgangs úr tengiliðum fundinna aðila verða notuð.
- Stillið valkostinn **Aðaltengiliður** á **Já** til að nota netfang sem er skilgreint fyrir fundinn aðila sem aðalnetfangið.

> [!NOTE]
> Ef tilgangur er valinn í reitnum **Tilgangur** og valkosturinn **Aðaltengiliður** er stilltur á **Já** á sama tíma, verða öll netföng sem uppfylla a.m.k. eitt skilgreint skilyrði notuð við keyrslu.

### <a name="configuration-email"></a>Skilgreiningartölvupóstur

Veljið **Skilgreiningartölvupóstur** sem gerð netfangs ef skilgreiningin sem er notuð er með hnút í gagnagjöfunum sem skila annaðhvort einu netfangi eða mörgum netföngum sem eru aðgreind með semikommu (;). Hægt er að nota [gagnagjafa](general-electronic-reporting.md#FormatComponentOutbound) og [aðgerðir](er-formula-language.md#functions) í formúluhönnuðinum til að ná í rétt sniðið netfang eða rétt sniðin netföng sem eru aðgreind með semikommum. Til dæmis ef notuð er skilgreiningin **ISO 20022 Kreditfærsla**, er hnúturinn sem táknar aðalnetfang lánardrottins úr tengiliðaupplýsingum lánardrottins sem senda bréfið á er `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.

[![Skilgreining uppruna tölvupóstfangs](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)

## <a name="group-format-components"></a><a id="grouping"></a>Flokka sniðshluti

Til að flokka sniðshluti skal á síðunni **Viðtökustaður rafrænnar skýrslugerðar**, í flýtiflipanum **Viðtökustaður skráar**, velja hlutina í hnitanetinu og síðan velja **Flokka**.

**Netfang** er eini áður skilgreindi viðtökustaðurinn sem er enn tiltækur fyrir valda íhluti. Engir aðrir áður skilgreindir viðtökustaðir eru tiltækir vegna þess að þeir eru taldir óstuddir fyrir flokk íhluta. Þú færð tilkynningu um þessar breytingar eins og þörf er á.

Litið er á færsluna sem var áður bætt við sem haus flokksins sem er stofnaður. Þessi hausafærsla inniheldur stillingar fyrir viðtökustað tölvupósts fyrir flokkinn. Aðrar færslur eru hluti af flokknum sem nota stillingar fyrir viðtökustað tölvupósts í hausafærslu flokksins.

Til að taka sniðshluti úr flokk skal í flýtiflipanum **Viðtökustaður skráar** velja færslu sem tilheyrir flokknum og síðan velja **Sleppa flokkun**.

- Ef hausfærsla er valin verður allur flokkurinn leystur upp.
- Ef valin er færsla meðlims og hún er síðasta meðlimafærslan í flokki, verður allur flokkurinn leystur upp.
- Ef valin er meðlimafærsla sem er ekki síðasta meðlimafærslan í flokki, verður sú færsla tekin úr núverandi flokki.

Eftirfarandi mynd sýnir skipulag á sniði rafrænnar skýrslugerðar sem var skilgreint til að búa til þjappaða skrá á útleið sem inniheldur athugasemd innheimtubréfs og viðeigandi reikninga viðskiptavinar á PDF-sniði.

[![Skiplag á sniði rafrænnar skýrslugerðar sem myndar skjöl á útleið](./media/ER_Destinations-Email-Grouping1.png)](./media/ER_Destinations-Email-Grouping1.png)

Eftirfarandi mynd sýnir ferlið, eins og lýst er í þessu efnisatriði, um flokkun einstakra hluta og virkjun á viðtökustað **Tölvupósts** fyrir nýja flokkinn þannig að athugasemd innheimtubréfs er sent ásamt viðeigandi reikningum viðskiptavinar sem tölvupóstviðhengi.

[![Flokkun einstakra hluta og virkjun á viðtökustað tölvupósts](./media/ER_Destinations-Email-Grouping2.gif)](./media/ER_Destinations-Email-Grouping2.gif)

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)
- [Áfangastaðir fyrir rafræna skýrslugerð](electronic-reporting-destinations.md)
- [Formúluhönnuður í rafrænni skýrslugerð (ER)](general-electronic-reporting-formula-designer.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]