---
title: Setja upp pöntunaruppfyllingu fyrir verslanir
description: Þessi grein veitir yfirlit yfir hvernig á að setja upp pöntunaruppfyllingu í verslun.
author: BrianShook
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 12c60de59f1007256b67a56a5ede0b83857b73bd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855031"
---
# <a name="set-up-order-fulfillment-for-stores"></a>Setja upp pöntunaruppfyllingu fyrir verslanir

[!include [banner](includes/banner.md)]

Margir smásalar vilja hámarka uppfyllingu pöntunar með því að gera verslanir kleift að fylla pantanir. Pöntunaruppfylling á verslunarstiginu getur hjálpað til við að draga úr hárri birgðastöðu fyrir tiltekna verslun, eða gæti verið nauðsynleg út frá skipulagslegu sjónarmiði í þeim tilvikum þar sem verslun hefur auka rúmtak eða er staðsett í minni flutningsfjarlægð frá viðskiptavininn. Til að bregðast við þessari þörf er í boði samræmd pöntunaruppfyllingaraðgerð við sölustað.

Pantanir til að uppfylla í tilteknum verslun er með vörugeymslu verslunarinnar útnefnda á hausnum eða í línum pöntunarinnar.

Pöntunaruppfyllingaraðgerðin í sölustaðnum veitir eitt vinnusvæði í sölustað sem hægt er að nota til að vinna pantanir. Þetta felur í sér allt frá því að samþykkja pöntunina, merkja hana sem senda, eða setja af stað afhendingu í verslun.

## <a name="set-up-the-order-fulfillment-operation"></a>Setja upp pöntunaruppfyllingaraðgerðina

Pöntunaruppfyllingu, [Aðgerðarnúmer 928](pos-operations.md), má nota til að fá aðgang að vinnusvæði uppfyllingar pöntunar fyrir verslun á sölustaðnum.

Fylgdu leiðbeiningunum í [Bæta aðgerðinni við hnappahnit](pos-screen-layouts.md) til að tilgreina hvaða færibreytu á að nota þegar þú kallar fram pöntunaruppfyllinguna á sölustað. Sjálfgefið er að velja **Allar pantanir** eftir að pöntunaruppfyllingaraðgerðir er tilgreind. Þegar skilgreint er með þessari breytu mun aðgerðin skrá alla pöntunarlínur til uppfyllingar í núverandi verslun. Einnig er í boði **Pantanir til að senda** sem hægt er að úthluta á hnapp og nota þegar notandinn vill aðeins sjá pantanir sem verða sendar frá versluninni. Að lokum er **Sóttar pantanir**. Þegar kallað fram á sölustaðnum, birtir þetta aðeins listi yfir pantanir sem sóttar eru í versluninni. Hægt er að úthluta mismunandi færibreytur á mismunandi hnappa til að gefa notandanum ýmsar leiðir til að skoða pöntunaruppfyllingu.

### <a name="enable-users-to-access-order-fulfillment-at-the-point-of-sale"></a>Gera notendum kleift að fara inn á pöntunaruppfyllingu á sölustað

Pöntunaruppfyllingaraðgerðin eru ekki með eigin heimild út-úr-kassanum, en í framtíðinni geta notendur verið krafðir um **Leyfa að sækja pöntun** heimild til að kalla fram aðgerðina frá sölustað.

Á verslunarstigi er skilgreiningarstilling í boði til að ákvarða hvort pöntunarlína skuli samþykkt handvirkt innan sölustaðarins. Ef þessi valkostur fyrir skilgreiningu er ekki stilltur verða pöntunarlínur samþykkt sjálfgefið. Ef kveikt er á þessum skilgreiningarvalkostum þurfa notendur á sölustaðnum að hafa **Leyfa að samþykkja pöntun** heimild til að samþykkja pantanir innan frá sölustað.

### <a name="enable-manual-order-acceptance"></a>Virkja handvirkt samþykki pöntunar

Að sjálfgefnu eru pöntunarlínur sem eru úthlutað á verslun merktar sem **Samþykktar**. Þetta þýðir að það er gert ráð fyrir að þær verði uppfyllt frá úthlutað versluninni og mun ekki verða háð frekari úthlutunum. Í ákveðnum tilvikum geta smásalar viljað samþykkja pantanir handvirkt áður en hægt er að uppfylla þær. Til dæmis, ef verslun er með fáa starfsmenn og ófær um að uppfylla pantanir, mun verslunarstjóri aðeins samþykkja eins mörg pantanir til vinnslu eins og þeir telja unnt að vinna með fullnægjandi hætti á tilteknum degi. Þar til pöntun er samþykkt getur henni verið endurúthlutað af bakvinnslunni í aðra verslun. Á þennan hátt veitir pöntunarsamþykki einnig leið til að gefa til kynna að pöntun hafi verið viðurkennd af verslun og verður uppfyllt.

Pöntunarlínur fyrir afhendingu í verslun eru merktar sem **Í bið** og eru ekki háðar samþykki.

Til að kveikja á handvirku samþykki fyrir pöntunarlínur skal fara í **Retail og Commerce** \> **Rásir** \> **Verslanir** \> **Allar verslanir**. Veldu verslunina og smelltu á kenni verslunar til að skoða upplýsingar um verslunina. Smellið á **Breyta**. Á **Almennt** flýtiflipanum skaltu finna **Pöntunaruppfylling** undirhausinn og breyta **Handvirkt samþykki** frá **Nei** til **Já**.

### <a name="enable-reject-order-line-capability"></a>Virkja getu höfnunar pöntunarlínu

Einnig er hægt að hafna pöntunarlínum frá sölustað. Það að hafna pöntunarlína táknar að hún verði ekki uppfyllt í þeirri verslun og sendir pöntunarlínuna aftur til endurúthlutunar í aðra verslun eða vöruhús. Heimild til höfnunar pöntunarlínu er veitt í gegnum **Leyfa að hafna pöntun** heimild í POS heimildarhópnum sem tengist starfsmanninum. Um leið og þeir hafna línu, geta smásalar krafið starfsmanna sinna til að veita ástæðu fyrir höfnun. Þetta er hægt að ná fram með því að nota upplýsingakóða af gerðinni **Virkni upplýsingakóða** **Pöntunaruppfylling** og úthluta upplýsingakóðanum til **Hafna pöntunarlínu** í virknireglunni sem tengist rásinni.

> [!NOTE]
> Aðeins upplýsingakóðar af gerðinni **Virkni upplýsingakóða** **Pöntunaruppfylling** er hægt að úthluta til **Hafna pöntunarlínu** aðgerð.

### <a name="synchronize-changes-to-the-channel-database"></a>Samstilla breytingar við gagnagrunn rásar

Eftir að aðgerðin hefur verið úthlutað á hnappahnit, réttar heimildir hafa verið úthlutað og rásin er grunnstillt, verða breytingarnar að vera samstilltar við rásargagnagrunninn. Þetta er gert með því að fara í **Retail og Commerce** \> **Upplýsingatækni í Retail og Commerce** \> **Dreifingaráætlun**. Veldu áætlun „1090-afgreiðslukassar“ til að samstilla hnappahnitsbreytingar og smelltu síðan á **Keyra núna**. Næst skal samstilla breytingar á heimildum með því að velja „1060-Starfsmenn“ og smellið síðan á **Keyra núna**. Næst skal samstilla breytingar á rásum með því að velja „1070-Skilgreining rása“ og smellið síðan á **Keyra núna**. Að lokum skaltu samstilla nýstofnuðu upplýsingakóðann fyrir ástæðu höfnunar með því að velja „1110-Altæk skilgreining“ og smella á **Keyra núna**.

## <a name="use-order-fulfillment-at-the-point-of-sale"></a>Nota pöntunaruppfyllingu á sölustað

Opnaðu sölustað og veldu pöntunaruppfyllingaraðgerðina. Eftir því hvernig það er stillt, annaðhvort allar línur, pöntunarlínur fyrir afhendingu eða pöntunarlínur til sendingar verður skráðar.

### <a name="order-fulfillment-view"></a>Yfirlit yfir uppfylling pöntunar

Yfirlitið yfir pöntunaruppfyllingu sýnir lista yfir pöntunarlínur til uppfyllingar í versluninni og inniheldur eftirfarandi dálka:

- Pöntunarnúmer
- Afurðarnúmer
- lýsing
- Magn pantað
- Umbeðin afhendingardagsetning
- Nafn viðskiptavinar
- Uppfyllingarstaða

Frekari upplýsingar fyrir tiltekna pöntunarlína er hægt að skoða með því að velja pöntunarlínuna og svo opna hliðargluggavalmyndina sem er staðsett rétt fyrir neðan innskráðan notanda/vakt upplýsingarnar sem birtist í haus sölustaðar. Þessi valmynd inniheldur 2 flipa: eitt fyrir upplýsingar um línu og annað fyrir upplýsingar um pöntun. Upplýsingaflipi línunnar felur í sér eftirfarandi upplýsingar:

- Magn pantað
- Eftirstandandi magn sem skal senda/afhenda
- Tiltekið magn
- Pakkað magn
- Reikningsfært magn (þegar afhent eða sent)
- Afhendingarmáti
- Afh.aðsetur

Hliðargluggavalmynd upplýsinga hefur einnig flipa sem veitir meira upplýsingar um pöntunarstig, þar á meðal:

- Nafn viðskiptavinar
- Auðkenni viðskiptavinar
- Pöntunarnúmer
- Heildarupphæð pöntunar
- Staða pöntunar

Neðst í yfirliti yfir pöntunaruppfyllingu er Aðgerðarúða. Þetta inniheldur allar aðgerðir sem hægt er að beina gegn pöntunarlínu. Ef aðgerð er ekki tiltæk miðað við stöðu línunnar verður aðgerðin ekki tiltæk.

Að sjálfgefnu, munu pantanir hafa stöðuna **Samþykkt**. Pöntunarstaða er hægt að skoða sem dálkur í listanum yfir pöntunarlínur. Ef **Handvirkt samþykkt** er grunnstillt á rás stigi munu allar línur sem á að senda birtast sem **Í bið** og verða að vera samþykkt áður en hægt er að uppfylla þær. Pantanir fyrir afhendingu í verslun eru **Í bið** sjálfgefið og þurfa ekki að vera samþykkt.

### <a name="order-fulfillment-line-actions"></a>Línuaðgerðir pöntunaruppfyllingar

- **Breyta** – Ef staða pöntunar er í bið er hægt að breyta henni á sölustað. Pantanir sem þegar hafa verið tilteknar að hluta, pakkað eða reikningsfærðar er ekki hægt að breyta í yfirliti pöntunaruppfyllingar.
- **Samþykkja** – Ef **Handvirkt samþykki** er grunnstillt á rásarstiginu, þarf fyrst að samþykkja línurnar áður en þær geta farið í gegnum vinnslu pöntunaruppfyllingar.
- **Taka til** – Taka til valkosturinn styður nokkrar aðgerðir. Í fyrsta lagi að **Tiltekt** uppfærir stöðu pöntunarlínu þannig að aðrir í versluninni reyni ekki að taka til sömu línu. Næst prentar **Prenta tiltektarlista** tiltektarlista fyrir valda línuna eða línurnar og uppfærir einnig stöðu þeirra í **Tiltekt**. Sniðum tiltektarlista er stjórnað sem hluti af sniðum innhreyfingar. Til að fá nánari upplýsingar um uppsetningu sniðs innhreyfingar skal sjá [Prentun og sniðmát innhreyfingar](receipt-templates-printing.md). Að síðustu, **Merkja sem tiltekið** gefur til kynna að línan hafi verið tiltekin. **Merkja sem tiltekið** hrindir af stað samsvarandi birgðafærslu í bakvinnslu. Hægt er að framkvæma tiltektaraðgerðir á sama tíma fyrir margar pöntunarlínur þvert yfir pantanir og fyrir allan afhendingarmáta.
- **Hafna** – Línur eða línur að hluta má hafna. Þetta gerir þeim kleift að vera endurúthlutað frá bakvinnslunni til annars verslunar eða vöruhús. Línum er aðeins hægt að hafnað ef þeir hafa ekki enn verið tiltekin eða pakkað. Til að hafna línu sem hefur þegar verið tekin til eða pakkað verður afturkalla tiltekt eða pökkun fyrir þessa lína frá bakvinnslunni.
- **Pakka** – Pakka valkosturinn styður tvær aðgerðir: **Prenta fylgiseðil** mun prenta fylgiseðil fyrir valdar línur og **Merkja sem pakkað** mun merkja línurnar sem pakkaðar og merkja línurnar sem afhentar á bakvinnslunni. Aðeins pöntunarlínur sem tilheyra sömu pöntun og hafa sömu flutningsmáta má pakka á sama tíma. Snið fylgiseðils eru stjórnað sem hluti af sniði innhreyfingar. Til að fá nánari upplýsingar um uppsetningu sniðs innhreyfingar skal sjá [Prentun og sniðmát innhreyfingar](receipt-templates-printing.md).
- **Senda** – Sendingaraðgerðin mun merkja völdum línum sem **Afhent** í bakvinnslunni. Eftir að línan hefur verið send að fullu birtist hún ekki lengur á skjá uppfyllingar pöntunar.
- **Afhending** – Afhendingaraðgerðin bætir línurnar við færsluyfirlitið fyrir afhendingu. Ef það eru aðrar línur í pöntuninni sem ekki er verið að afhenda, þá verður þeim bætt við færsluyfirlitið með magn upp á núll. Eftir að lína hefur verið að fullu afhent birtist hún ekki lengur í yfirliti yfir pöntunaruppfyllingu.

### <a name="order-fulfillment-filtering"></a>Síun pöntunaruppfyllingar

Pöntunaruppfylling á sölustað felur í sér síun til að hjálpa notandanum að finna auðveldlega það sem þeir þurfa. Hægt er að breyta síum á aðgerðarúðunni neðst á **Sölustaður** skjánum. Sjálfgefið er að **Afhendingarmáti** síu er beitt, byggt á því hvernig aðgerðin er sett upp. Ef aðgerðin er sett upp með færibreytu **Allar pantanir**, þá er þeirri síu beitt við aðgang að pöntunaruppfyllingu. Sama gildir um **Sótt í verslun** og **Sent frá verslun** færibreytur. Aðrir síur sem hægt er að beita á yfirlit pöntunaruppfyllingar innihalda:

- Númer viðskiptavinar
- Nafn viðskiptavinar
- Netfang viðskiptavinar
- Pöntunarnúmer
- Afhendingarmáti
- Kvittunarnúmer
- Rásartilvísunarkenni
- Númer upprunaverslunar
- Staða línu
- Búið til þann
- Afhendingardagur
- Móttökudagsetning


[!INCLUDE[footer-include](../includes/footer-banner.md)]
