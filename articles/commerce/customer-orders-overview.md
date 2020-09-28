---
title: Pantanir viðskiptavina á sölustað
description: Þetta efnisatriði gefur upplýsingar um pantanir viðskiptavinar á sölustað. Pantanir viðskiptavinar eru einnig þekktar sem sérpantanir. Efnisatriðið inniheldur umræðu um tengdar færibreytur og færsluflæði.
author: josaw1
manager: AnnBe
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 9e5770de82638e6cef6d4c1dffd1dc85549fb11f
ms.sourcegitcommit: 30e4dc0a45f7de5f0a7178b1e88f7c3d61a7395e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/03/2020
ms.locfileid: "3763702"
---
# <a name="customer-orders-in-point-of-sale-pos"></a>Pantanir viðskiptavina á sölustað

[!include [banner](includes/banner.md)]

Í þessu efnisatriði er að finna upplýsingar um hvernig á að stofna og stjórna pöntunum viðskiptavina á sölustað. Hægt er að nota pantanir viðskiptavina til að sækja sölur þar sem kaupendur vilja sækja afurðir á öðrum degi, sækja afurðir á annarri staðsetningu eða fá vörur sendar til sín. 

Í alhliða samskiptum netverslunar veita margir smásalar valkost pantana viðskiptavina eða sérpantana til að mæta ýmsum þörfum afurða og uppfyllingar. Hér eru nokkrar dæmigerðar aðstæður.

- Viðskiptavinur vill að afurð sé afhent á tilgreint aðsetur á tilgreindum degi.
- Viðskiptavinur vill taka til afurðir úr verslun eða staðsetningu sem er önnur en verslunin eða staðsetningin þar sem viðskiptamaðurinn keypti þær afurðir.
- Viðskiptavinur inni í verslun langar að panta afurðir í dag og sækja þær í sömu verslun á öðrum degi.

Smásalar geta notað pantanir viðskiptavina til að lágmarka tapaða sölu sem tómar birgðir gætu annars valdið, þar sem varninginn má afhenda eða taka til á öðrum tíma eða stað.

## <a name="set-up-customer-orders"></a>Setja upp pantanir viðskiptavinar
Áður en reynt er að nota pöntunarvirkni viðskiptavinar á sölustað skal ganga úr skugga um að hafa lokið öllum nauðsynlegum skilgreiningum í Commerce Headquarters.

### <a name="configure-modes-of-delivery"></a>Skilgreina afhendingarmáta

Til að nota pantanir viðskiptavina þarf að skilgreina afhendingarmáta sem verslunarrásin getur notað. Skilgreina þarf að minnsta kosti einn afhendingarmáta sem hægt er að nota þegar pöntunarlínur eru sendar til viðskiptavinar úr verslun. Einnig þarf að skilgreina að minnsta kosti einn afhendingarmáta fyrir sóttar vörur sem hægt er að nota þegar pöntunarlínur eru sóttar í versluninni. Afhendingarmátar eru skilgreindir á síðunni **Afhendingarmáti** í Commerce Headquarters. Frekari upplýsingar um uppsetningu afhendingarmáta fyrir viðskiptarásir er að finna í [Skilgreina afhendingarmáta](https://docs.microsoft.com/dynamics365/commerce/configure-call-center-delivery#define-delivery-modes).

![Síða afhendingarmáta](media/customer-order-modes-of-delivery.png)


### <a name="set-up-fulfillment-groups"></a>Setja upp uppfyllingarflokka

Sumar verslunar- eða vöruhúsastaðsetningar geta hugsanlega ekki uppfyllt pantanir viðskiptavina. Með því að skilgreina uppfyllingarflokka getur fyrirtæki tilgreint hvaða verslunar- og vöruhúsastaðsetningar verði sýndar sem valmöguleiki fyrir notendur sem stofna pantanir viðskiptavina á sölustað. Uppfyllingarflokkar eru skilgreindir á síðunni **Uppfyllingarflokkar**. Fyrirtæki geta stofnað eins marga uppfyllingarflokka og þörf er á. Eftir að uppfyllingarflokkur hefur verið skilgreindur er hann tengdur við verslun með því að nota hnapp í flipanum **Setja upp** á aðgerðasvæði síðunnar **Verslanir**.

Í Commerce-útgáfu 10.0.12 og síðar geta fyrirtæki skilgreint hvort hægt sé að nota vöruhúsið eða samsetningar vöruhúss/verslunar sem eru skilgreindar í uppfyllingarflokkum fyrir sendingar, sótt eða bæði sendingar og sótt. Þar af leiðandi hefur verslunin aukinn sveigjanleika til að keyra valmöguleika vöruhúss og verslunar sem sýndir eru notendum sem stofna pöntun fyrir afhendingu í samanburði við pöntun sem á að senda. Til að nýta sér þessa stillingarmöguleika þarf að kveikja á eiginleikanum **Geta til að tilgreina staðsetningar sem „Sending“ eða „Afhending“ í uppfyllingarflokki**. Ef vöruhús sem er tengt við uppfyllingarflokk er ekki verslun er aðeins hægt að skilgreina það sem sendingarstað. Ekki er hægt að nota það þegar pantanir sem á að afhenda eru skilgreindar á sölustað.

![Síða uppfyllingarflokka](media/customer-order-fulfillment-group.png)

### <a name="configure-channel-settings"></a>Skilgreina stillingar rásar

Þegar unnið er með pantanir viðskiptavina á sölustað verður að hafa í huga nokkrar stillingar verslunarrásarinnar. Þessar stillingar er að finna á síðunni **Verslanir** í Commerce Headquarters.

- **Vöruhús** – Þessi reitur tilgreinir vöruhúsið sem notað er til að uppfylla pantanir sem skilgreindar eru fyrir sendingu úr versluninni.
- **Úthlutun uppfyllingarflokks** – Veljið þennan hnapp (í flipanum **Setja upp** á aðgerðasvæðinu) til að tengja uppfyllingarflokkana sem vísað er í til að sýna valmöguleika fyrir afhendingarstaði eða upprunastaði sendinga þegar pantanir viðskiptavina eru stofnaðar á sölustað.
- **Nota skatt áfangastaðar** – Þessi valkostur gefur til kynna hvort heimilisfang viðtakanda sé notað til að ákvarða skattflokkinn sem á að nota fyrir pöntunarlínur sem eru sendar á heimilisfang viðskiptavinar.
- **Nota skatt viðskiptavinar** – Þessi valkostur gefur til kynna hvort skattflokkurinn sem skilgreindur er fyrir heimilisfang viðskiptavinar sé notaður til skattleggja pantanir viðskiptavina sem eru stofnaðar á sölustað fyrir sendingu til heimilis viðskiptavinar.

![Uppsetning verslunarrásar á verslunarsíðum](media/customer-order-all-stores.png)

### <a name="set-up-customer-order-parameters"></a>Setja upp færibreytur viðskiptavinapantana

Áður en reynt er að stofna pantanir viðskiptavina á sölustað verður að skilgreina viðeigandi færibreytur í Commerce Headquarters. Hægt er að finna þessar færibreytur í flipanum **Pantanir viðskiptavina** á síðunni **Commerce-færibreytur**.

- **Sjálfgefin gerð pöntunar** – Hægt er að tilgreina gerð pöntunar sem er sjálfkrafa úthlutað á viðskiptavinapantanir sem stofnaðar eru á sölustað. Þessar pantanir viðskiptavina geta verið annaðhvort sölupantanir eða tilboðspantanir. Óháð sjálfgefinni gerð pöntunar, geta notendur enn stofnað bæði sölupantanir og viðskiptavinapantanir á sölustað.
- **Sjálfgefin innborgunarprósenta** – Tilgreinið prósentuna fyrir heildarupphæð pöntunar sem viðskiptavinurinn þarf að greiða sem innborgun áður en hægt er að staðfesta pöntun. Það veltur á réttindum starfsfólks verslunar hvort það geti hnekkt upphæðinni með því að velja aðgerðina **Hnekking innborgunar** á sölustað, ef sú aðgerð er skilgreind fyrir færsluskjáinn.
- **Afhendingarmáti afhendingar** – Tilgreinið afhendingarmáta sem á að nota í sölupöntunarlínum sem eru skilgreindar fyrir afhendingu á sölustað.
- **Afhendingarmátinn taka með** – Tilgreinið afhendingarmáta sem á að nota í sölupöntunarlínum sem er litið á sem „taka með“ pöntunarlínur þegar blönduð karfa er stofnuð, þar sem sumar línur verða sóttar eða sendar og aðrar línur tekur viðskiptavinurinn með sér strax.
- **Prósenta afpöntunargjalds** – Ef nota á gjald þegar hætt er við pöntun viðskiptavinar, skal skilgreina upphæð þess gjalds.
- **Kóði afpöntunargjalds** – Tilgreinið gjaldakóða viðskiptakrafa sem á að nota þegar afpöntunargjald er notað fyrir viðskiptavinapantanir í gegnum sölustað sem hætt er við. Gjaldakóðinn skilgreinir fjárhagsbókunarrökin fyrir afpöntunargjaldið.
- **Kóði sendingargjalds** – Ef valkosturinn **Nota ítarleg sjálfvirk gjöld** er stilltur á **Já**, hefur þessi færibreytustilling engin áhrif. Ef þessi valkostur er stilltur á **Nei** verða notendur beðnir um að færa handvirkt inn sendingargjald þegar pantanir viðskiptavina eru stofnaðar á sölustað. Notið þessa færibreytu til að varpa gjaldakóða viðskiptakrafa sem verður notaður á pantanir þegar notendur færa inn sendingargjald. Gjaldakóðinn skilgreinir fjárhagsbókunarrökin fyrir sendingargjaldið.
- **Nota ítarleg sjálfvirk gjöld** - Stillið þennan valkost á **Já** til að nota sjálfvirk gjöld sem kerfið reiknar út þegar pantanir viðskiptavina eru stofnaðar á sölustað. Hægt er að nota þessi sjálfvirku gjöld til að reikna út sendingargjöld eða önnur gjöld sem tengjast pöntun eða vöru. Frekari upplýsingar um hvernig setja á upp og nota ítarleg sjálfvirk gjöld er að finna í [Ítarleg sjálfvirk gjöld fyrir omni-rás](https://docs.microsoft.com/dynamics365/commerce/omni-auto-charges).

![Flipi viðskiptavinapantana á færibreytusíðu Commerce](media/customer-order-parameters.png)

### <a name="update-transaction-screen-layouts-in-pos"></a>Uppfæra útlit færsluskjás á sölustað

Gangið úr skugga um að [skjáútlit](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts) sölustaðar sé skilgreindur til að styðja stofnun og stjórnun á pöntunum viðskiptavina og að allar nauðsynlegar aðgerðir sölustaðar séu skilgreindar. Hér eru nokkrar aðgerðir sölustaðar sem mælt er með til að styðja rétt við stofnun og stjórnun viðskiptavinapöntunar:
- **Senda allar afurðir** – Þessi aðgerð er notuð til að tilgreina að allar línur í færslukörfunni verði sendar á áfangastað.
- **Senda valdar afurðir** – Þessi aðgerð er notuð til að tilgreina að valdar línur í færslukörfunni verði sendar á áfangastað.
- **Sækja allar afurðir** – Þessi aðgerð er notuð til að tilgreina að allar línur í færslukörfunni verði sóttar á valdri staðsetningu verslunar.
- **Sækja valdar afurðir** – Þessi aðgerð er notuð til að tilgreina að valdar línur í færslukörfunni verði sóttar á valdri staðsetningu verslunar.
- **Taka allar afurðir strax** – Þessi aðgerð er notuð til að tilgreina að allar línur í færslukörfunni verða teknar um leið. Ef þessi aðgerð er notuð á sölustað verður pöntun viðskiptavinar breytt í staðgreiðslufærslu.
- **Taka valdar vörur strax** - Þessi aðgerð er notuð til að tilgreina að viðskiptavinurinn taki með sér valdar línur í færslukörfunni við greiðslu. Þessi aðgerð er aðeins gagnleg í atburðarás [blandaðrar pöntunar](https://docs.microsoft.com/dynamics365/commerce/hybrid-customer-orders).
- **Afturkalla pöntun** – Þessi aðgerð er notuð til að leita að og sækja pantanir viðskiptavina þannig að notendur sölustaðar geti breytt, hætt við eða framkvæmt uppfyllingaraðgerðir á þeim eins og þörf er á.
- **Breyta afhendingarmáta** - Hægt er að nota þessa aðgerð til að breyta á fljótlegan hátt afhendingarmáta fyrir línur sem eru þegar skilgreindar fyrir sendingu, án þess að gera kröfu um að notendur fari í gegnum flæðið „senda allar afurðir“ eða „senda valdar afurðir“ aftur.
- **Hnekking innborgunar** – Hægt er að nota þessa aðgerð til að breyta upphæð innborgunar sem viðskiptavinurinn greiðir fyrir valda pöntun viðskiptavinar.

![Aðgerðir á færsluskjá sölustaðar](media/customer-order-screen-layout.png)

## <a name="working-with-customer-orders-in-pos"></a>Unnið með pantanir viðskiptavina á sölustað

### <a name="create-a-customer-order-for-products-that-will-be-shipped-to-the-customer"></a>Stofna pöntun viðskiptavinar fyrir afurðir sem verða sendar til viðskiptavinarins

1. Á færsluskjá sölustaðar skal bæta viðskiptavini við færsluna.
2. Bæta afurðum við körfuna.
3. Veljið **Senda valið** eða **Senda allt** til að senda afurðir á aðsetur viðskiptavinalykils.
4. Veljið valkostinn til að stofna pöntun viðskiptavinar.
5. Staðfestið eða breytið staðsetningunni „senda frá“, staðfestið eða breytið heimilisfangi viðtakanda og veljið sendingarmáta.
6. Færið inn æskilega sendingardagsetningu viðskiptavinapöntunar.
7. Notið greiðsluaðgerðirnar til að greiða allar reiknaðar upphæðir sem eru á gjalddaga, eða notið aðgerðina **Hnekking innborgunar** til að breyta upphæðunum sem eru á gjalddaga, og veljið síðan greiðslu.
8. Ef heildarupphæð pöntunar var ekki greidd skal færa inn kreditkort sem verður notað fyrir stöðuna sem er á gjalddaga fyrir pöntunina þegar hún er reikningsfærð.

### <a name="create-a-customer-order-for-products-that-the-customer-will-pick-up"></a>Stofna pöntun viðskiptavinar fyrir afurðir sem viðskiptavinurinn mun sækja

1. Á færsluskjá sölustaðar skal bæta viðskiptavini við færsluna.
2. Bæta afurðum við körfuna.
3. Veljið **Sækja valið** eða **Sækja allt** til að setja af stað skilgreiningu pöntunar sem er sótt.
4. Veljið staðsetningu verslunar þar sem viðskiptavinurinn mun sækja valdar afurðir.
5. Veljið afhendingardag.
6. Notið greiðsluaðgerðirnar til að greiða allar reiknaðar upphæðir sem eru á gjalddaga, eða notið aðgerðina **Hnekking innborgunar** til að breyta upphæðunum sem eru á gjalddaga, og veljið síðan greiðslu.
7. Ef pöntunin var ekki greidd að fullu, skal velja hvort viðskiptavinurinn greiði seinna meir (við afhendingu) eða hvort kreditkort verður eyrnamerkt núna og síðan notað við afhendingu.

### <a name="edit-an-existing-customer-order"></a>Breyta fyrirliggjandi pöntun viðskiptavinar

Smásölupantanir sem annaðhvort eru stofnaðar á netrásinni eða verslunarrásinni er hægt að endurkalla og breyta í gegnum sölustað eftir þörfum.

> [!IMPORTANT]
> Pantanir sem stofnaðar eru í símaversrás er ekki hægt að breyta í gegnum sölustað ef kveikt er á stillingunni [Virkja lok pöntunar](https://docs.microsoft.com/dynamics365/commerce/set-up-order-processing-options#enable-order-completion) fyrir símaversrásina. Til að tryggja rétta úrvinnslu á greiðslu, þarf að breyta pöntunum sem gerðar voru í símaversrás og sem nota aðgerðina „Virkja lok pöntunar“ í gegnum símaversforritið í Commerce Headquarters.

Í Commerce-útgáfu 10.0.13 og eldri geta notendur breytt studdum pöntunum viðskiptavina í gegnum sölustað ef pantanirnar eru opnaðar að fullu. Ef búið er að vinna úr einhverjum línum pöntunar til uppfyllingar (sækja, pakka o.s.frv.) verður læst fyrir breytingar á pöntuninni á sölustað.

> [!NOTE]
> Í Commerce-útgáfu 10.0.14 gerir eiginleiki sem hefur verið gefinn út í [opinni forútgáfu](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms) notendum sölustaðar kleift að breyta pöntunum viðskiptavina í gegnum sölustað, jafnvel þótt pöntunin hefur verið uppfyllt að hluta til. Hins vegar er ekki hægt að breyta pöntunum í gegnum sölustað sem hafa verið reikningsfærðar að fullu. Til að prófa þessa forútgáfu og veita frekari athugasemdir skal kveikja á eiginleikanum **(Forskoðun) Breyta pöntunum á sölustað sem hafa verið uppfylltar að hluta til** á vinnusvæðinu **Eiginleikastjórnun**. Ekki er hægt að breyta viðskiptavinapöntunum sem voru stofnaðar í símaversrás og sem nota aðgerðina „Virkja lok pöntunar“ jafnvel eftir að þessi eiginleiki er virkjaður.

1. Veljið **Afturkalla pöntun**.
2. Notið **Leita að** til að færa inn síur til að finna pöntunina og veljið síðan **Nota**.
3. Veljið pöntunina úr listanum yfir niðurstöður og veljið síðan **Breyta**. Ef hnappurinn **Breyta** er ekki tiltækur, er pöntunin í stöðu þar sem ekki er hægt að breyta henni.
4. Gerið allar nauðsynlegar breytingar á pöntun viðskiptavinar í færslukörfunni. Einhverjar breytingar gætu verið bannaðar meðan verið er að breyta.
5. Ljúkið við breytingarferlið með því að velja greiðsluaðgerð.
6. Til að fara úr breytingaferlinu án þess að vista breytingar er hægt að nota aðgerðina **Ógilda færslu**.



### <a name="cancel-a-customer-order"></a>Hætta við pöntun viðskiptavinar

1. Veljið **Afturkalla pöntun**.
2. Notið **Leita að** til að færa inn síur til að finna pöntunina og veljið síðan **Nota**.
3. Veljið pöntunina á listanum yfir niðurstöður og veljið síðan **Hætta við**. Ef hnappurinn **Hætta við** er ekki tiltækur er pöntunin í stöðu þar sem ekki er lengur hægt að hætta við hana.
4. Ef afpöntunargjöld eru skilgreind skal staðfesta þau. Hægt er að breyta afpöntunargjöldunum áður en þau eru staðfest eftir þörfum. 
5. Í færslukörfunni skal ljúka við afturköllunarferlið með því að velja greiðsluaðgerð. Ef innborganir sem voru greiddar eru umfram afturköllunargjaldið gætu endurgreiðslur verið á gjalddaga.
6. Til að hætta við afturköllunarferlið án þess að vista neinar breytingar er hægt að nota aðgerðina **Ógilda færslu**.

## <a name="finalizing-the-customer-order-shipment-or-pickup-from-pos"></a>Gengið frá sendingu viðskiptavinapöntunar eða afhendingu á sölustað

Eftir að pöntun er stofnuð verða vörurnar sóttar af viðskiptavininum á staðsetningu verslunar eða sendar, en það fer eftir skilgreiningu pöntunarinnar. Frekari upplýsingar um þetta ferli er að finna í fylgiskjölunum [uppfylling pöntunar í verslun](https://docs.microsoft.com/dynamics365/commerce/order-fulfillment-overview).

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Ósamstillt færsluflæði fyrir pantanir viðskiptavinar

Hægt er að stofna pantanir viðskiptavina á sölustað í annaðhvort samstilltum ham eða ósamstilltum ham. Ef tekið er eftir vandamálum vegna afkasta eða töfum notanda þegar pantanir viðskiptavina eru stofnaðar á sölustað, skal íhuga að kveikja á ósamstilltri stofnun pöntunar.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Gera virkt að pantanir viðskiptavinar séu stofnaðar í ósamstilltum ham

1. Í Commerce Headquarters, á síðunni **Virknireglur**, skal velja virkniregluna sem samsvarar versluninni sem ætlunin er að skilgreina.
2. Á flipanum **Almennt** stillirðu valkostinn **Stofna viðskiptavinapöntun í ósamstilltri stillingu** á **Já**.

Þegar valkosturinn **Stofna pöntun viðskiptavinar í ósamstilltri stillingu** er stilltur á **Já** verða pantanir viðskiptavinar alltaf stofnaðar í ósamstilltri stillingu, jafnvel þó að Retail Transaction Service (RTS) er tiltækt. Ef þessi valkostur er stilltur á **Nei** verða pantanir viðskiptavinar alltaf stofnaðar í samstilltum ham með því að nota RTS. Þegar pantanir viðskiptavina eru stofnaðar í ósamstilltum ham, er náð í þær og þær stofnaðar sem smásölufærslur í Commerce Headquarters úr Commerce Pull-verkum. Samsvarandi sölupantanir fyrir smásölufærslurnar eru stofnaðar þegar **Samstilla pantanir** er keyrt annaðhvort handvirkt eða með runuvinnslu.

## <a name="additional-resources"></a>Frekari upplýsingar

[Blandaðar pantanir viðskiptavinar](hybrid-customer-orders.md)
