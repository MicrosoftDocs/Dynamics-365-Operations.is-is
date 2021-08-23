---
title: Stofna skil á sölustað
description: Í þessu efnisatriði er lýst hvernig á að hefja skil á staðgreiðslufærslum eða viðskiptavinapöntunum í forriti Microsoft Dynamics 365 Commerce sölustaðar.
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.20
ms.openlocfilehash: 4a0d5efe043d72f936a15ec9a8ead9987fdb22b891a5a3ae94f95aa5ea7a6e67
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715531"
---
# <a name="create-returns-in-pos"></a>Stofna skil á sölustað

[!include [banner](includes/banner.md)]

Í þessu efnisatriði er lýst hvernig á að hefja skil á staðgreiðslufærslum eða viðskiptavinapöntunum í Microsoft Dynamics 365 Commerce forriti sölustaðar.

> [!NOTE]
> Í Commerce-útgáfu 10.0.20 og nýrri er boðið upp á nýjan eiginleika sem heitir **Upplifun samræmdrar skilavinnslu á sölustað**. Þessi eiginleiki býður upp á áreiðanlega og samræmda vinnslu á skilum á sölustað burtséð frá færslugerðinni (staðgreiðslu eða viðskiptavinapöntun) eða upprunalegri rás sem pöntunin var stofnuð í. Við mælum með að öll fyrirtæki kveiki á þessum nýja eiginleika til að stuðla að auknum áreiðanleika á vinnslu skila í gegnum sölustað.
>
> Ekki er hægt að slökkva á eiginleikanum eftir að kveikt er á honum.

## <a name="process-returns-by-using-the-return-transaction-operation"></a>Vinna úr skilum með skilafærsluaðgerðinni

Mælt er með að skilfærsluaðgerðinni sé bætt við [skjáútlið](pos-screen-layouts.md) sölustaðar. Í útgáfum á undan Commerce-útgáfu 10.0.20 styður skilafærslan réttilega vinnslu á skilum fyrir staðgreiðslur eingöngu. Þegar kveikt er á eiginleikanum **Upplifun samræmdrar skilavinnslu fyrir sölustað** í Commerce-útgáfu 10.0.20 eða nýrri, styður skilafærsluaðgerðin einnig vinnslu á skilum sem eiga uppruna sinn í viðskiptavinapöntunum, t.d. „sótt“ eða „heimsent“ pantanir sem eru þegar reikningsfærðar.

Í skilafærsluaðgerðinni geta notendur leitað að staðgreiðslufærslum eða viðskiptavinapöntun sem á að skila með því að færa inn einhver af eftirfarandi fjórum leitarskilyrðum. Notendur geta slegið inn þessi skilyrði með því að nota lyklaborð tækis, lyklaborð á skjá eða strikamerkjaskanna.

- Móttökukenni
- Pöntunarnúmer
- Tilvísunarkenni rásar (einnig þekkt sem auðkenni pöntunarstaðfestingar)
- Reikningskenni

Ef færsla eða pöntun finnst sem passar við leitarskilyrðið birtist síðan **Afurðir sem hægt er að skila**. Þar geta notendur tilgreint vörurnar sem verið er að skila. Þeir geta einnig slegið inn skilamagn og ástæðukóða.

Fyrir hverja pöntunarlínu í listanum yfir vörur sem hægt er að skila sýnir sölustaður upplýsingar um upprunalegt magn innkaupa og magn allra skila sem hefur verið unnið úr. Skilamagnið sem notandi slær inn fyrir pöntunarlínu verður að vera minna en eða jafnt og gildið í reitnum **Hægt að skila**.

![Síða afurða sem hægt er að skila.](media/returnslist.png)

Við úrvinnslu á skilum, ef notandi er með efnislegu afurðina og sú afurð er með strikamerki, getur notandinn skannað strikamerkið til að skrá skilin. Hver skönnun á strikamerkinu eykur skilamagnið um eitt stykki. Ef strikamerkið er hinsvegar með innfellt magn verður magnið fært inn í reitinn **Skilað núna**.

Notendur geta einnig valið vörur handvirkt til að skila á síðunni **Afurðir sem hægt er að skila** og síðan uppfæra reitinn **Skilað núna** með því að nota upplýsingasvæðið hægra megin.

Ef verið er að tilgreina tiltækt hámarksmagn á **Skilað núna** fyrir færslu getur notandinn valið aðgerðina **Velja allt** á forritastiku sölustaðar til að stilla hámarksmagn á því sem hægt er að skila í öllum línum.

Fyrir hverja línu sem er með magn fyrir **Skilað núna** verður notandinn að velja ástæðukóða skila með því að nota upplýsingasvæðið. Fyrir skil á staðgreiðslufærslum eru ástæðukóðar skila skilgreindir sem upplýsingakóðar í virknireglu verslunar. Fyrir skil á viðskiptavinapöntunum eru ástæðukóðar skila skilgreindir á síðunni **Ástæðukóðar skila** í Dynamics 365 Commerce höfuðstöðvum.

Eftir að skilamagn og ástæðukóði hafa verið stillt fyrir hverja vöru sem á að skila getur notandinn valið aðgerðian **Skila** á forritastiku sölustaðar til að halda áfram með vinnsluna. Færslusíða sölustaðar birtist þar sem skilanlegum vörum sem voru valdar á fyrri síðu hefur verið bætt við körfuna. Magnið **Skilað núna** fyrir vörurnar birtast sem línur með neikvæðu magni í færslunni og heildarendurgreiðslan er reiknuð út.

Notendur geta bætt línum við skilafærslu ef þeir eru að stofna skiptipöntun. Notendur geta einnig bætt fleirum tilfallandi skilavörum við skilafærslu með því að nota aðgerðina **Skila afurð** fyrir valdar sölulínur með jákvæðu magni sem hefur verið bætt við.

> [!NOTE]
> Aðgerðin **Skila afurð** á sölustað býður ekki upp á neina staðfestingu gagnvart neinni upprunalegri færslu og leyfi ekki að neinni afurð sé skilað. Þess vegna mælum við með að aðeins heimilaðir notendur megi framkvæma þessa aðgerð, eða að hnekking stjórnandi sé nauðsynleg ef þessi aðgerð er notuð.

Ef endurgreiðsla á að fara fram í greiðsluferlinu geta fyrirtæki stillt [endurgreiðslureglur](refund_policy_returns.md) sem takmarka greiðslumáta sem nota má til að endurgreiða viðskiptavinum. Ef upprunalega færslan var greidd með kreditkorti fer það eftir greiðsluvinnslunni og kerfisskilgreiningum hvort notendur hafi möguleikann á að [senda endurgreiðslu á upprunalega kortið](dev-itpro/linked-refunds.md). Í því tilviki er hægt að vinna úr endurgreiðslunni án þess að krefjast þess að viðskiptavinurinn renni kortinu sínu aftur. Upprunalega greiðslumerkið er notað til að senda endurgreiðsluna.

## <a name="other-return-options-in-pos"></a>Aðrir skilamöguleikar í sölustað

Þegar kveikt er á eiginleikanum **Upplifun samræmdrar skilavinnslu á sölustað** geta notendur einnig notað aðgerðina **Sýna færslubók** á sölustað til að hefja skil fyrir staðgreiðslufærslu eða viðskiptavinapöntun. Þeir geta þá valið færslu í færslubókinni og síðan valið aðgerðina **Skil** á forritastiku sölustaðar. Þessi aðgerð er einungis í boði ef það eru línur í pöntuninn sem má skila. Hún setur af stað sömu notandaupplifun og aðgerðin **Skilafærsla**.

Notendur geta einnig notað aðgerðina **Endurkalla pöntun** á sölustað til að leita að og endurkalla pantanir viðskiptavinar. (Ekki er hægt að nota þessa aðgerð fyrir staðgreiðslufærslur). Í þessu tilviki, eftir að pöntun viðskiptavinar er valin, er hægt að nota aðgerðina **Skil** á forritastiku sölustaðar til að hefja skil fyrir pöntun viðskiptavinar. Þessi aðgerð er einungis í boði ef það eru línur í pöntuninn sem má skila. Hún setur af stað sömu notandaupplifun og aðgerðin **Skilafærsla** eða **Sýna færslubók**.

## <a name="return-orders-are-posted-to-commerce-headquarters-as-sales-orders"></a>Skilapantanir eru bókaðar í Commerce Headquarters sem sölupantanir 

Þegar kveikt er á eiginleikanum **Upplifun samræmdrar skilavinnslu á sölustað** verða öll skil sem stofnuð eru á sölustað skrifuð til Commerce Headquarters sem sölupantanir með neikvæðum línum. Í útgáfum á undan Commerce-útgáfu 10.0.20 geta notendur valið hvort bóka eigi skilapantanir sem sölupantanir með neikvæðum línum eða hvort þær eigi að vera skilapantanir sem eru stofnaðar í gegnum ferli vöruskilaheimildar (RMA). 

Í eiginleikanum **Upplifun samræmdrar skilavinnslu á sölustað** hefur möguleikinn á að nota RMA-ferli til að stofna skil á sölustað verið úreltur. Þegar kveikt hefur verið á þessum eiginleika verða öll skil stofnuð sem sölupantanir með neikvæðum línum.

## <a name="offline-return-processing-improvements"></a>Endurbætur á skilavinnslum utan nets

Í flestum tilvikum þegar unnið er úr skilum á sölustað reynir kerfið að framkvæma þjónustukall í rauntíma (RST) til Commerce Headquarters til að staðfesta núverandi magn sem boðið er upp á að skila. Þessi staðfesting hjálpar til við að koma í veg fyrir sviksamlegt athæfi þar sem viðskiptavinur reynir að skila sömu vörunni á mörgum stöðum.

Til að meðhöndla aðstæður þar sem ekki er hægt að framkvæma RTS-kall út af net- eða tengivandamáli hefur ferli verið komið á til að samstilla gögn skilamagns með regluglegu millibili úr Commerce Headquarters við gagnagrunnsrás verslunar. Þessi skilarakning rásar hjálpar til við að tryggja að magnið fyrir **Hægt að skila** sem er sýnt á sölustað sé nógu nákvæmt jafnvel þegar sölustaður er utan nets. Það tryggir einnig að sölustaður geti haldið áfram að staðfesta upplýsingar rásarmegin til að stuðla að því að koma í veg fyrir sviksamleg skil.

Til að nota skilaferli utan nets á réttan hátt ættu fyrirtæki að áætla runuvinnsluna **Uppfæra skilamagn** í Commerce Headquarters þannig að hún keyri reglulega. Við mælum með að þetta verk keyri jafn oft og P-vinnslan sem sækir nýjar færslur úr Commerce-rásum og sendir til Commerce Headquarters.

Vinnslan **Uppfæra skilamagn** reiknar út magnið sem er hægt að skila fyrir allar sölupantanir sem finnast í Commerce Headquarters. Þá þarf að senda gögnin sem verkið reiknar út til gagnagrunna rásar þannig að hægt sé að uppfæra rásir verslunar. Dreifingarvinnslan **Skilamagn** (1200) er notað í þessu skyni. Þar sem gögn um magn sem hægt er að skila eru samstillt úr Commerce Headquarters, ef unnið er úr skilum á sölustað, en ekki er hægt að gera RTS-kall, getur sölustaður notað skilaupplýsingar rásarinnar til að staðfesta magnið fyrir **Hægt að skila** fyrir tilgreinda sölulínu.

Þegar ekki er hægt að framkvæma RTS-köll og sölustaðurinn notar gögn rásarinnar fyrir staðfestingu á skilum koma upp viðvörunarboð sem upplýsa notanda um að hann sé að stofna skil „utan nets“. Þar af leiðandi er hann meðvitaður um að magnið fyrir **Hægt að skila** sem er sýnt á sölustað er hugsanlega gamalt og ekki lengur nákvæmt, eftir því hvenær vinnslan **Uppfæra skilamagn** var síðast unnin og samstillt við rásina.

Dæmi: Viðskiptavinur vann nýlega úr skilum fyrir pöntunarlínu í annarri rás, en þau gögn hafa ekki enn verið samstillt við gagnagrunna rásarinnar í gegnum vinnsluna **Uppfæra skilamagn**. Viðskiptavinurinn fer þá í aðra verslun og reynir að skila sömu vörunni aftur. Í þessu tilviki, ef verslunin getur ekki framkvæmt RTS-kall til Commerce Headquarters til að fá gögn um skil í rauntíma, mun sölustaðurinn leyfa að vörunni sé skilað aftur. Notandinn er hins vegar varaður við því að upplýsingarnar sem notaðar eru til að staðfesta skilin gætu verið úreltar. Skilaboðin sem notandinn fær eru aðeins viðvörunarboð. Þau koma ekki í veg fyrir að notandinn geti haldið áfram að vinna úr skilunum.

Ef upplýsingar rásar eru ekki þær nýjustu af einhverjum ástæðum og unnið er úr skilum utan nets fyrir magn sem fer umfram raunverulegt magn fyrir því sem **Hægt er að skila** gæti villa komið upp þegar bókun uppgjörs er keyrð til að búa til færsluna í Commerce Headquarters.

> [!NOTE]
> Þegar kveikt er á eiginleikanum **Upplifun samræmdrar skilavinnslu á sölustað** munu nýir valfrjálsir eiginleikar sem styðja staðfestingu á skilum á raðaðri afurð verða tiltækir. Frekari upplýsingar er að finna í [Skila raðnúmerastýrðum afurðum á sölustað](POS-serial-returns.md).

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a>Virkja viðeigandi skattaútreikning fyrir skil á hluta af magni

Þessi eiginleiki tryggir að þegar pöntun er skilað með því að nota marga reikninga verði skattar að lokum jafnir þeirri skattupphæð sem var upprunalega innheimt.
1.  Farðu á vinnusvæðið **Eiginleikastjórnun** og leitaðu að **Virkja viðeigandi skattaútreikning fyrir skil á hluta af magni**.
2.  Veldu **Virkja viðeigandi skattaútreikning fyrir skil á hluta af magni** og smelltu á **Virkja**.


## <a name="additional-resources"></a>Frekari upplýsingar

[Skila raðnúmerastýrðum afurðum á sölustað](POS-serial-returns.md)

[Tengdar endurgreiðslur á áður samþykktum og staðfestum færslum](dev-itpro/linked-refunds.md)

[Búa til og uppfæra reglu um skil og endurgreiðslur fyrir rás](refund_policy_returns.md)

[Sjónrænar skilgreiningar fyrir notandaviðmót sölustaðar](pos-screen-layouts.md)
