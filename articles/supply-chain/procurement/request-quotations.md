---
title: "Beiðnir um tilboð (BUT)"
description: "Í þessu efnisatriði er að finna yfirlit yfir beiðnir um tilboð (BUT). Fyrirtæki gefa út beiðni um tilboð (BUT) þegar þau vilja taka á móti tilboðum frá mörgum lánardrottnum fyrir þær vörur eða þá þjónustu sem þau þurfa að kaupa inn."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchRFQCaseTable, PurchRFQCaseTableListPage, PurchRFQCompare, PurchRFQReplyTable, PurchRFQVendReplyTableListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 2154
ms.assetid: 3936996e-d943-46ca-8385-84c042990f1d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: b86363004b8702d1a654f2a1da49bba82fc8ff2a
ms.contentlocale: is-is
ms.lasthandoff: 03/26/2018

---

# <a name="requests-for-quotation-rfqs"></a>Beiðnir um tilboð (BUT)

[!include[banner](../includes/banner.md)]

Í þessu efnisatriði er að finna yfirlit yfir beiðnir um tilboð (BUT). Fyrirtæki gefa út beiðni um tilboð (BUT) þegar þau vilja taka á móti tilboðum frá mörgum lánardrottnum fyrir þær vörur eða þá þjónustu sem þau þurfa að kaupa inn. Í beiðni um tilboð, eru lánardrottnar beðnir um að leggja fram verð og afhendingartíma fyrir magn þeirra vara sem er tilgreint. Einnig er hægt að biðja lánardrottna að tilgreina hvort einhver tilfallandi gjöld eru, eins og sendingarkostnaður, eða hvort lánardrottinn býður upp á afslátt fyrir stórar pantanir eða flýtigreiðslu reiknings lánardrottins.

BUT ferlið samanstendur af eftirfarandi verkefnum:

1. Stofna og senda BUT til eins eða fleiri lánardrottna.
2. Móttaka og skrá svör við BUT (útboð).
3. Flytja samþykkt útboð yfir í innkaupapöntun, innkaupasamningur eða innkaupabeiðni.

Eftirfarandi skýringarmynd veitir yfirlit yfir BUT ferlið.

[![RFQ-ferli](./media/rfq-process-458x1024.jpg)](./media/rfq-process.jpg)

Hægt er að stofna BUT frá áætlaðar pantanir, úr innkaupabeiðni eða úr handvirkri færslu. BUT sem er stofnað er kallað BUT tilfelli. BUT tilfellið er grunnskjalið sem er notað til að gefa út BUT á hvern lánardrottin.

Eftir að búið er að útbúa BUT tilfelli og bæta við lánardrottnum, smellið á **Senda** á BUT tilfellið. BUT færslubók er mynduð fyrir hvern lánardrottinn sem BUT er send til. Hægt er að skilgreina stillingar prentstýringar fyrir Senda aðgerðina þannig að hún annað hvort prentar skýrslu fyrir hvern lánardrottin í safn eða sendir skýrslu á tölvupóstfang hvers lánardrottins. Þar að auki er hægt að nota BUT færslubók fyrir hvern lánardrottinn til að mynda skýrslu sem hægt er að senda eða endursenda seinna til lánardrottins. Einnig er hægt að skilgreina aðgerðina Senda til að mynda svarblað sem lánardrottinn getur fyllt út.

Þetta efni fjallar um ferlið við meðhöndlun BUT þegar lánardrottinn samstarf er ekki notað. Ef kerfið þitt er uppsett fyrir samstarf lánardrottna, geta lánardrottnar fært kauptilboð beint inn í Microsoft Dynamics 365 for Finance and Operations. Nánari upplýsingar er að finna í [Samstarf lánardrottna við viðskiptamenn](vendor-collaboration-work-customers-dynamics-365-operations.md).
 
Ef þarf að lagfæra BUT þegar búið er að senda hana, er hægt að endursenda BUT til lánardrottna þegar því hefur verið lokið með því að nota tvær lagfæringaraðgerðir: Stofna og Fullvinna.

Þegar kauptilboð berast gegnum tölvupóst þarf að færa þau í **Svör við BUT** síðu. Ef valið er **Afrita gögn í svar** valkosturinn, eru gögn eins og magn og dagsetningar úr BUT afritaðar í svarið. Hægt er að breyta þessum gögnum til að endurspegla kauptilboð lánardrottins.

Ef önnur ítrekun svars er krafist fyrir lánardrottinn, smellið á **Skila**á **Svör við BUT** síðu. Skilaaðgerð myndar nýja færslubók og skýrslu sem verða prentaðar, skjalaðar og send, í samræmi við prentstýringarstillingarnar.

Ef skilyrði fyrir stigagjöf er bætt við BUT málið skal BUT svarið hafa vettvang fyrir stigagjöf þar sem hægt er að færa inn stig. Samtals stig birtast þegar borin eru saman svör á síðunni **Bera saman svör**. Á þeirri síðu er einnig hægt að bera saman önnur svargögn, svo sem línuverð, afhendingardag og heildarverð.

Eftir að kauptilboð eða hluti af kauptilboði hefur verið valið er hægt að samþykkja það og hafna afganginum. Samþykki á færslubókum, höfnun á færslubókum og samsvarandi skýrslur eru myndaðar, og verða prentaðar, skjalaðar og sendar í samræmi við prentstýringarstillingarnar. Þegar þú samþykkir kauptilboð eða tilteknar línur í kauptilboði, er annaðhvort innkaupasamningur eða innkaupapöntun mynduð eða innkaupabeiðni er uppfærð, það fer eftir gerð BUT innkaupanna. Hægt er að stofna verðsamninginn sem hægt er að nota síðar fyrir hvaða svör sem er, óháð því hvort þau voru samþykkt eða þeim hafnað.

Staða BUT kemur fram í BUT hausnum og fer eftir stöðu BUT línanna. Staðan gefur til kynna að hversu miklu leyti búið er að vinna BUT. Hvert BUT hefur tvö gildi fyrir stöðu: lægstu stöðu og hæstu stöðu. Lægsta staða er ítarlega kosti stig línu í beiðni um TILBOÐ og hæsta staðan er oftast ítarlega stig línu í beiðni um TILBOÐ. Til dæmis, ef minnst ítarlegt stig í BUT er fyrir línu sem hefur verið stofnuð, er lægsta staða fyrir BUT **mynduð** . Ef mest ítarlega stig í BUT er fyrir línu sem hefur verið send til lánadrottna, er hæsta staða fyrir BUT **Sent** . Staða er uppfærð sjálfkrafa sem er að vinna beiðni um TILBOÐ.

Hægt er að skoða lægstu og hæstu stöðu fyrir BUT- haus á síðunni **Allar beiðnir um tilboð**. Hægt er að skoða lægstu og hæstu stöðu fyrir BUT-línu á flipanum **Línur** á síðunni **Beiðni um tilboð**.

Röð staða til að vinna BUT er sem hér segir:

1. **Stofnað**
2. **Sent**
3. **Móttekið**
4. **Samþykkt**, **Hætt við** eða **Hafnað**

Stöðunum verður lýst nánar í seinni hlutum þessa efnisatriðis.

## <a name="setting-up-rfq-functionality"></a>Setja upp virkni BUT

Áður en hægt er að stofna BUT-verk, verður að setja upp upplýsingar um BUT á síðunni **færibreytur Innkaupa og uppruna**. Þegar BUT-verk er stofnað er hægt að tilgreina sjálfgefin gildi eru afrituð í BUT. Þú getur tilgreint eftirfarandi sjálfgildi:

- Gerð innkaupa nýrra BUT: **Innkaupapöntun** eða **Innkaupasamningur**
- Lokadagur og -tími
- Upplýsingar um afhendingu og greiðsluskilmálar
- Svæðin sem á að fylgja með í BUT-svarinu

Hægt er að hnekkja þessi gildi fyrir tiltekið BUT-verk.

Einnig ætti að skilgreina ferli breytingar. Hluti af þessari stillingu er að hægt er að kveikja á svæðislæsingu. Þegar kveikt er á svæðislæsingu þarf innkaupastjóri sem vill lagfæra BUT fyrst að smella á **Stofna** í **Lagfæringar** hluta í **Tilboð** flipa. Síðan, etir að BUT hefur verið uppfærð með breytingum, þarf innkaupastjóri að ljúka við ferlið með því að smella á **Fullvinna**. Fullvinna aðgerðin býr til tölvupóst skilaboð sem lætur lánardrottna vita um lagfært BUT.

Velja sniðmát fyrir tilkynningu í tölvupósti sem er sent til lánardrottna í **Færibreytur innkaupa og aðfanga** síðu. Þegar sniðmát er stofnað getur það innihaldið eftirfarandi endurnýjunartákn:

- %BUT mál%
- %Ástæða fyrir ógildingu tilboðs%
- %Ástæða breytinga%
- %Breytingar gerðar af%
- %Fyrirtæki%
- %BUT mál heiti%
- %ExpiryDateTime%
- % Dagsetning%

% Ástæða skila kauptilboðs % og % Ástæða fyrir breytingum % tákn er skipt út fyrir texta sem innkaupastjóri getur fært inn þegar hann eða hún lýkur við breytingar í **Breytingar** leiðsagnarforritinu. Gildi fyrir % Breytingar gerðar af % og % Fyrirtækis % tákn eru sjálfkrafa tekin úr BUT. %Date% tákninu er skipt út fyrir núgildandi dagsetningu.

Einnig er krafist tölvupóstsniðs ef þú hættir við BUT eftir að það hefur verið sent. Þessi tölvupóstsniðmát er notað til að senda tilkynninguna um afturköllun til tengiliðsaðila lánardrottins. Sniðmátið verður að vera valið á síðunni **Færibreytur innkaupa og aðfanga**. Þegar sniðmát er stofnað getur það innihaldið eftirfarandi endurnýjunartákn:

- %Ástæða afturköllunar%
- %BUT mál% 
- %BUT afturkallað af%
- %Fyrirtæki%
- %BUT mál heiti%
- % Dagsetning%

%Ástæða afturköllunar kauptilboðs% tákn er skipt út fyrir texta sem innkaupastjóri getur fært inn í **Afturköllun** leiðsagnarforritinu. %Date% tákninu er skipt út fyrir núgildandi dagsetningu.

Ef óskað er að nota ástæðukóða á svari við BUT til að tilgreina hvers vegna tilboði var hafnað eða samþykkt verður að setja upp ástæðukóða á síðunni **ástæður Lánardrottna**.

Hægt er að skilgreina útlit prentaðra eða vistaðra BUT-skjala á síðunni **Uppsetning eyðublaða** í Innkaup og aðföng.

> [!NOTE]
> Í grunnstillingum fyrir hið opinbera verður þú að nota leiðréttingarferlið til að breyta BUT sem hefur þegar verið sent. Þegar BUT er sent eru reitir læstir. Þar af leiðir, að til þess að gera breytingar á BUT verður þú að velja **Búa til** til að hefja lagfæringuna, eins og lýst er hér að framan. Læsingar hegðun er stjórnað af **Læsa BUT þegar þeir eru sendir** valkostur á **Innkaup og aðföng færibreytur** síðunni. Sjálfgefið er þessi færibreyta stilltur á **Já** í grunnstillingum fyrir hið opinbera, ekki er hægt að breyta sjálfgefin stilling. Þess vegna, þótt lagfæringarferlið geti verið meðhöndluð handvirkt í grunnstillingum fyrir óopinbera aðila, verður að nota það í grunnstillingum fyrir opinbera aðila.

Þegar þú stofnar BUT fyrir innkaupapöntun, og bætir birgðavöru við BUT, er birgðafærsla stofnuð sem hefur innhreyfingarstöðuna **Innhreyfing Tilboðs**. Hafðu aðeins BUT-línur af þessu tagi í huga þegar þú notar aðaláætlun til að reikna vistir. Ef óskað er eftir að aðaláætlun innihaldi BUT-línur sem áætluð innhreyfing þarf að skilgreina þessa hegðun í uppsetningu á áætlanagerð.

Sem innkaupastjóri eða umboðsmaður, getur þú stofnað og viðhaldið beiðnagerðum til falla að innkaupakröfum fyrirtækis þíns. Hverja beiðnagerð má tengja við aðferðir við stigagjöf. Aðgerðir við stigagjöf samanstendur af safni skilyrða sem hægt er að nota þegar tilboðum fá stigagjöf. Setja verður upp beiðnagerðir, stigagjöf og skilyrða á síðunum **gerð Beiðni** og **Stigagjöf**.

## <a name="creating-and-sending-an-rfq"></a>Stofna og senda inn beiðni um TILBOÐ

Þú stofnar BUT, velur þá lánardrottna sem óskað er að gera kauptilboð fyrir BUT og sendir BUT til lánardrottna. Hægt er að nota prentstjórnunarkerfið til að beina BUT-skýrslunni og svarblaðs skýrslum á æskilegan áfangastað.

Þú getur gert BUT fyrir annað hvort **Innkaupapöntun** eða **Innkaupasamning** innkaupagerðir.

Ef BUT er af gerðinni **innkaupapöntun**, á eftirfarandi hegðun sér stað:

- Þegar BUT-línur eru stofnaðar, eru birgðafærslur myndaðar með innhreyfingarstöðuna **innhreyfing Tilboðs**.
- Þegar kauptilboð er samþykkt, er innkaupapöntun mynduð.

Ef BUT er af gerðinni **Innkaupasamningur**, á eftirfarandi hegðun sér stað:

- BUT er notað sem samningur um að kaupa ákveðið magn eða virði vöru yfir tíma. Ef valin er þessi gerð innkaupa þarf að velja dagsetningasvið sem á við innkaupasamninginn og nafn þess einstaklings sem hefur umsjón með innkaupasamningnum.
- Þegar kauptilboð er samþykkt, er innkaupasamningur myndaður.

Ef BUT er mynduð úr innkaupabeiðni er **Innkaupabeiðni** gerð sjálfkrafa úthlutað. Ekki er hægt að stofna BUT handvirkt með **Innkaupabeiðni** gerð.

Þú getur aðeins stofnað BUT úr innkaupabeiðni ef staða innkaupabeiðninnar er **Í yfirferð** og næsta verkflæðisverki er úthlutað á þig. Línur í innkaupabeiðninni eru uppfærðar sjálfkrafa þegar þú samþykkir línur úr svörum við BUT (kauptilboð) sem voru mótteknar frá lánardrottnum. Ekki er hægt að framkvæma aðgerðir í innkaupabeiðninni á borð við að ljúka henni, hafna eða samþykkja á meðan BUT er í vinnslu.

Þegar BUT er stofnað er hægt að velja tiltekna gerð beiðni. Gerð beiðni ákvarðar safn skilyrða sem notuð er til að stiga svör við BUT.

Hægt er að bæta spurningalista við BUT-verk. Þessi spurningalisti birtist síðan í öllum svörum eftir að BUT er sent.

Það eru þrjár leiðir til að velja þá lánardrottna til að bæta við BUT-verk:

- Bæta við lánardrottnum einum í senn.
- Leita að öllum lánardrottnum sem uppfylla tiltekiin skilyrði.
- Bæta sjálfkrafa við öllum lánardrottnum sem hafa verið samþykktir fyrir innkaupategundir sem notaðar eru í BUT- línum.

Þegar BUT-málið er tilbúið er smellt á **Senda**. Aðgerðin Senda myndar færslubækur og skýrslur sem verða prentaðar, skjalaðar og sendar í samræmi við prentstýringarstillingarnar.

Ef þú stillir **Nota lánardrottin til að endurreikna verð** og **Nota vöruupplýsingar sem eiga við lánardrottna** á **Já** á **Sendir tilboðsbeiðni** síðunni þegar BUT er send til lánadrottna, eru sumar upplýsingar tengdar lánardrottnum sjálfkrafa færðar inn. Hægt er að breyta þessum upplýsingum á siðunni **Beiðni um svar við tilboði**.

Eftirfarandi tafla sýnir stöðubreytingar BUT þegar BUT er stofnuð og send til lánardrottna.

| Aðgerð                             | Lægsta hausstaða tilboðsbeiðni | Hæsta staða hauss Tilboðsbeiðni                        | Lægsta línustaða tilboðsbeiðni | Hæsta staða línu beiðni um TILBOÐ |
|------------------------------------|--------------------------|--------------------------------------------------|------------------------|-------------------------|
| Stofna beiðni um TILBOÐ hauss og línu.    | Stofnaður                  | Stofnaður                                          | Stofnaður                | Stofnaður |
| Senda beiðni um tilboð á tiltekinn lánardrottin. | Sent                     | Sent                                             | Sent                   | Sent |
| Bæta við öðrum lánardrottni.                | Stofnaður                  | Sent(beiðni um tilboð hefur aðeins verið send til einn lánardrottins.) | Stofnaður                | Sent |
| Senda tilboðsbeiðni til síðari lánardrottins. | Sent                     | Sent                                             | Sent                   | Sent |

> [!NOTE]
> Hægt er að bæta fleiri lánardrottnum við BUT hvenær sem er og lægsta og hæsta staða uppfærist til að endurspegla lánardrottna sem var bætt við. Til dæmis, ef kauptilboð er móttekið frá öllum lánadrottnum og minnst ein lína kauptilboðs er samþykkt er lægsta staða í haus BUT **Hafnað**, og hæsta staðan er **Samþykkt**. Ef bætt er við nýjum lánardrottni er lægsta staða í línu nú **Stofnað**. Þess vegna uppfærist lægsta staða í haus BUT í **Stofnað**, en hæsta staða helst **Samþykkt**.

## <a name="amending-an-rfq"></a>Að laga BUT

Einstaka sinnum þarf að breyta BUT þegar búið er að senda hana. Þú gætir þurft að breyta BUT, ef til dæmis afhendingardagsetningum hefur verið breytt eða ef þú vilt fleiri vörur eða annað magn vöru. Hægt er að skilgreina ferli lagfæringar þannig að það er annað hvort meira eða minna takmarkandi.

Ef notað er meira takmarkandi lagfæringarferli þarf að smella á **Stofna** á BUT-málinu til að hefja lagfæringu áður en hægt er að breyta reitum á BUT-máli sem þegar hefur verið sent. Eftir að lokið hefur verið við lagfæringar, verður að smella á **Fullvinna**. Þú verður svo að leiddur í gegnum ferlið við að bæta upplýsingum við tölvupóstinn sem eru send til að tilkynna lánardrottnum um lagfæringar. Uppfærð BUT skýrsla, sem felur í sér athugasemd um lagfæringar, tengist sjálfkrafa við skilaboðin.

Ef grunnstilling þín felur í sér minna takmarkandi lagfæringarferli þarf ekki að velja **Stofna** áður en hægt er að breyta reitum BUT-máls sem hefur þegar verið send. Hins vegar þarf að bæta athugasemd um lagfæringu handvirkt við BUT og senda málið aftur. Hafðu í huga að þessi nálgun er aðeins hægt að nota ef ekkert svaranna (tilboðin) hefur verið breytt. Ef þú hefur slegið inn svar og það er í **Móttekið** ástandi er **Senda** hnappurinn ekki tiltækur. Í þessu tilfelli verður þú að velja **Búa til** og síðan **Fullvinna**, eins og þú verður að gera í meira takmarkandi ferli. Svarið er síðan endurstillt til að endurspegla breytingar á BUT-málinu. 

Ef lánardrottnar nota lánardrottna samstarfsviðmótið til að slá inn tilboð verður þú alltaf að nota lagfæringarferlið til að tilkynna lánardrottnum um breytingar á BUT-málinu. Þessi krafa hjálpar til við að koma í veg fyrir aðstæður þar sem lánardrottnar bjóða í úrelt BUT-mál á meðan tilboð þeirra er í vinnslu. Nánari upplýsingar um samstarf lánardrottna er að finna í [Samstarf lánardrottna við utanaðkomandi lánardrottna](vendor-collaboration-work-external-vendors.md). 

Ef þú vilt bjóða fleiri lánardrottnum að bjóða, og engar breytingar hafa verið gerðar á BUT-málinu, getur þú notað **Senda** hnappinn. Söluaðilarnir sem þú bættir við munu birtast á síðunni **Senda** og fá tölvupóstboðið.

## <a name="receiving-and-registering-rfq-replies"></a>Móttaka og skrá svör við BUT

Þegar BUT er send, er svarblað stofnað sjálfkrafa. Þegar þú færð svör (kauptilboð) við BUT skaltu slá inn upplýsingarnar frá hverjum lánardrottni á svarblað BUT fyrir lánardrottna. Ef þú hefur bætt við stigagjöf, geturðu gefið stig fyrir svörin. Hægt er að bera tilboð lánardrottna saman með því að raða þeim eftir stigagjöf, svo sem besta heildarverði eða besta afhendingartíma samtals.

Ef spurningalisti er tengdur við BUT-málið, verður að færa svör við spurningunum handvirkt í svarblaðið.

Þú getur einnig slegið inn aðra línur, ef BUT-málið leyfir aðrar línur. Á flýtiflipanum **Innkaupatilboðslínur** velurðu **Bæta við línu**. Færðu síðan inn upplýsingar um vöruna, eins og vörunúmer eða innkaupaflokk, magn, verð og afslátt.

Ef svar hefur verið fært inn en krafist er að fá nýtt tilboð frá lánardrottni er hægt að endursenda BUT. Þetta býr til nýja færslubók og skýrslu sem hægt er að nota til að óska eftir breytingum frá lánardrottni.

Hægt er að sjá yfirlit yfir allar BUT og stöður svara þeirra á síðunni **Eftirfylgni BUT**.

Eftirfarandi tafla sýnir stöðubreytingar BUT eftir því sem kauptilboð eru móttekin og upplýsingar skráðar í svarblað BUT.

| Aðgerð                                         | Staða lægsta boðs | Hæsta tilboðsstaða | Lægsta hausstaða tilboðsbeiðni | Hæsta staða hauss Tilboðsbeiðni | Lægsta línustaða tilboðsbeiðni | Hæsta staða línu beiðni um TILBOÐ |
|------------------------------------------------|-------------------|--------------------|--------------------------|---------------------------|------------------------|-------------------------|
| Skrá eitt tilboð lánardrottins og vista það.        | Sent              | Móttekið           | Sent                     | Móttekið                  | Sent                   | Móttekið |
| Skrá annað tilboð lánardrottins og vista það. | Móttekið          | Móttekið           | Móttekið                 | Móttekið                  | Móttekið               | Móttekið |

> [!NOTE]
> Ef kauptilboði er skilað til lánardrottins til frekari samningaviðræðna mun lægsta og hæsta staðan vera áfram **Móttekið**.

### <a name="accepting-and-rejecting-bids-and-transferring-accepted-bids-to-downstream-documents"></a>Samþykkja og hafna kauptilboðum og flytja samþykkt kauptilboð yfir í skjöl á niðurleið

Eftir að þú hefur greint bestu kauptilboðin, svo sem kauptilboðið sem býður upp á bestu heildarverð, samþykkir þú kauptilboðið. Sumar línur í kauptilboði eru hægt að samþykja og hafna öðrum. Einnig er hægt að samþykkja línur úr öðrum lánardrottnum. Hafðu í huga að ef sumar línur er samþykktar, verður beðið um að hafna öllum öðrum línum. Þess vegna, ef óskað er að samþykkja aðrar línur verður að smella á **Hætta Við** þegar sú beiðni berst. Staða á BUT svari til sérhvers lánardrottins sem þú samþykkir kauptilboð eða línur frá, er uppfærð í **Samþykkt**. 

Þegar kauptilboð eða ákveðnar línur úr kauptilboði er samþykkt er innkaupapöntun eða innkaupasamningur myndað sjálfkrafa. Þú getur þá hafnað tilboðum frá öllum öðrum lánardrottnum.

Við svar, er hægt að bæta inn ástæðukóða til að útskýra hvers vegna kauptilboð var samþykkt eða hafnað.

Þegar svar við BUT er samþykkt sem **Innkaupabeiðni**, eru svarlínur BUT uppfærðar í innkaupabeiðnilínunum með eftirfarandi upplýsingum:

- Einingarverð
- Afsláttarprósenta
- Afsláttarupphæð
- Innkaupagjöld
- Línugjöld
- Lánardrottinn
- Ytra númeri
- Ytri lýsing

Eftirfarandi tafla sýnir stöðubreytingar BUT þegar kauptilboð frá lánardrottnum eru samþykkt og hafnað.

| Aðgerð                      | Staða lægsta boðs | Staða hæsta boðs | Lægsta hausstaða BUT | Hæsta staða hauss Tilboðsbeiðni | Lægsta línustaða tilboðsbeiðni | Hæsta staða línu beiðni um TILBOÐ |
|-------------------------    |-------------------|--------------------|--------------------------|---------------------------|------------------------|-------------------------|
| Samþykkja eitt af tilboðunum.     | Móttekið          | Samþ.             | Móttekið                 | Samþ.                    | Móttekið               | Samþ.   |
| Hafna öllum öðrum kauptilboðum.  | Hafnað          | Samþ.             | Hafnað                 | Samþ.                    | Hafnað               | Samþ.   |

