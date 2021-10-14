---
title: Yfirlit yfir beiðnir um tilboð
description: Í þessu efnisatriði er að finna yfirlit yfir beiðnir um tilboð (BUT). Fyrirtæki gefa út beiðni um tilboð (BUT) þegar þau vilja taka á móti tilboðum frá mörgum lánardrottnum fyrir þær vörur eða þá þjónustu sem þau þurfa að kaupa inn.
author: Henrikan
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchRFQCaseTable, PurchRFQCaseTableListPage, PurchRFQCompare, PurchRFQReplyTable, PurchRFQVendReplyTableListPage, BOMExpandPurchRFQ, PurchRFQReplyFollowupItem, PurchRFQCaseVend, PurchRFQReplyFollowup, PurchRFQCaseAmendmentInfo, PurchRFQReplyFollowupCase, PurchRFQReplyStatus, PurchRFQCaseReplyFields, PurchRFQAddQuestionnaire, PurchRFQAmendmentWizard, PurchRFQReplyTableStatus, PurchRFQReplyTableListPage, PurchRFQCancelWizard
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "2154"
- intro-internal
ms.assetid: 3936996e-d943-46ca-8385-84c042990f1d
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9965e906bdbbf93cdced66b8b39b85a47c62b080
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569482"
---
# <a name="requests-for-quotation-rfqs-overview"></a>Yfirlit yfir beiðnir um tilboð

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er að finna yfirlit yfir beiðnir um tilboð (BUT). Fyrirtæki gefa út beiðni um tilboð (BUT) þegar þau vilja taka á móti tilboðum frá mörgum lánardrottnum fyrir þær vörur eða þá þjónustu sem þau þurfa að kaupa inn. Í beiðni um tilboð, eru lánardrottnar beðnir um að leggja fram verð og afhendingartíma fyrir magn þeirra vara sem er tilgreint.
Einnig er hægt að biðja lánardrottna að tilgreina hvort einhver tilfallandi gjöld eru, eins og sendingarkostnaður, eða hvort lánardrottinn býður upp á afslátt fyrir stórar pantanir eða flýtigreiðslu reiknings lánardrottins.

BUT ferlið samanstendur af eftirfarandi verkefnum:

1. Stofna og senda BUT til eins eða fleiri lánardrottna.
1. Móttaka og skrá tilboð (BUT-svör).
1. Flytja samþykkt útboð yfir í innkaupapöntun, innkaupasamningur eða innkaupabeiðni.

Eftirfarandi skýringarmynd veitir yfirlit yfir BUT ferlið.

[![BUT-ferli.](./media/rfq-process-458x1024.jpg)](./media/rfq-process.jpg)

Hægt er að stofna BUT-verk úr áætluðum pöntunum, úr innkaupabeiðni eða úr handvirkri færslu. BUT tilfellið er grunnskjalið sem er notað til að gefa út BUT á hvern lánardrottin.

Eftir að búið er að útbúa BUT-verk og bæta við lánardrottnum skal velja **Senda** (**Senda og birta** fyrir hið opinbera) á BUT-verkinu. BUT færslubók er mynduð fyrir hvern lánardrottinn sem BUT er send til. Hægt er að skilgreina prentvalkost fyrir Senda aðgerðina þannig að hún annað hvort prentar skýrslu fyrir hvern lánardrottin í safn eða sendir skýrslu á tölvupóstfang hvers lánardrottins. Þar að auki er hægt að nota BUT færslubók fyrir hvern lánardrottinn til að mynda skýrslu sem hægt er að senda eða endursenda seinna til lánardrottins. Einnig er hægt að skilgreina aðgerðina Senda til að mynda svarblað sem lánardrottinn getur fyllt út.

Þetta efni fjallar um ferlið við meðhöndlun BUT þegar lánardrottinn samstarf er ekki notað. Ef kerfið þitt er uppsett fyrir samstarf lánardrottna, geta lánardrottnar fært kauptilboð beint inn í Supply Chain Management. Nánari upplýsingar er að finna í [Samstarf lánardrottna við viðskiptavini](/dynamics365/unified-operations/supply-chain/procurement/vendor-collaboration-work-customers-dynamics-365-operations) og [Samstarf lánardrottna við ytri lánardrottna](vendor-collaboration-work-external-vendors.md).

Ef þarf að lagfæra BUT þegar búið er að senda hana, er hægt að endursenda BUT til lánardrottna þegar því hefur verið lokið með því að nota tvær lagfæringaraðgerðir: Stofna og Fullvinna.

Þegar tilboð berast í tölvupósti er hægt að vinna með þessi tilboð á síðunni **Beiðni um tilboð**.

Ef krafist er annarrar ítrekunar um svar frá lánardrottni skal velja **Skila** á síðunni **Beiðni um tilboð**. Skilaaðgerð myndar nýja færslubók og skýrslu sem verða prentaðar, skjalaðar og sendar í samræmi við prentstillingar.

Ef skilyrði fyrir stigagjöf er bætt við BUT-verkið mun BUT hafa vettvang fyrir stigagjöf þar sem hægt er að færa inn stig. Samtals stig birtast á BUT og þegar borin eru saman svör á síðunni **Bera saman svör**. Á síðunni **Bera saman svör** er einnig hægt að bera saman önnur svargögn, svo sem línuverð, afhendingardag og heildarverð.

Eftir að tilboð er valið eða fjöldi lína í tilboði getur þú samþykkt allar eða nokkrar línur og hafnað afganginum. Samþykki á færslubókum, höfnun á færslubókum og samsvarandi skýrslur eru myndaðar og verða prentaðar, skjalaðar og sendar í samræmi við prentstillingarnar. Þegar þú samþykkir kauptilboð eða tilteknar línur í kauptilboði, er annaðhvort innkaupasamningur eða innkaupapöntun mynduð eða innkaupabeiðni er uppfærð, það fer eftir gerð BUT innkaupanna. Hægt er að stofna verðsamninginn sem hægt er að nota síðar fyrir hvaða svör sem er, óháð því hvort þau voru samþykkt eða þeim hafnað.

BUT-verk hefur tvær stöður: lægstu og hæstu, hægt er að skoða stöðuna á listasíðunni fyrir **Allar beiðni um tilboð**. Lægsta staðan er minnst þróaða stigið af öllum línum sem eru í BUT-verki og hæsta staðan er mest þróaða stigið af öllum línum sem eru í BUT-verki. Segjum sem dæmi að BUT-verk með þremur línum sé sent til tveggja lánardrottna, þannig að það eru tvær BUT hvor með þrjár línur. Allar línur eru **Sendar**. Nú er tilboð slegið inn frá einum lánardrottnanna og BUT-línurnar fá stöðuna **Móttekið**. Þetta þýðir að af línunum þremur í BUT-verkinu eru þær allar **Sendar** fyrir eina BUT og **Mótteknar** fyrir aðrar BUT. Lægsta staða verður þá **Sent** og hæsta staða er **Móttekið.**

Stöðunum verður lýst nánar í seinni hlutum þessa efnisatriðis.

## <a name="setting-up-rfq-functionality"></a>Setja upp virkni BUT

Áður en hægt er að stofna BUT-verk, verður að setja upp upplýsingar um BUT á síðunni **færibreytur Innkaupa og uppruna**. Þegar BUT-verk er stofnað er hægt að tilgreina sjálfgefin gildi eru afrituð í BUT. Þú getur tilgreint eftirfarandi sjálfgildi:

- Gerð innkaupa nýrra BUT: **Innkaupapöntun** eða **Innkaupasamningur**
- Mótfærður lokadagur og -tími frá þeim degi sem BUT-verkið er stofnað.
- Beiðnagerð sem getur sjálfgefið gefið ákveðna aðferð við stigagjöf BUT-verksins.
- Upplýsingar um greiðslu og afhendingarskilmála.

Hægt er að hnekkja þessi gildi fyrir tiltekið BUT-verk.

Einnig ætti að skilgreina ferli breytingar. Hluti af þessari stillingu er að hægt er að kveikja á svæðislæsingu. Þegar kveikt er á svæðislæsingu þarf innkaupastjóri sem vill lagfæra BUT fyrst að velja **Stofna** í **Breytingar** hluta í **Tilboð** flipa í BUT-verki. Síðan eftir að BUT-verkið hefur verið uppfært með breytingum, þarf innkaupastjóri að ljúka við ferlið með því að velja **Ljúka**. Fullvinna aðgerðin býr til tölvupóst skilaboð sem lætur lánardrottna vita um lagfært BUT.

Velja sniðmát fyrir tilkynningu í tölvupósti sem er sent til lánardrottna í **Færibreytur innkaupa og aðfanga** síðu. Þegar sniðmát er stofnað í **Sniðmát fyrir tölvupóst** getur það innihaldið eftirfarandi endurnýjunartákn:

- %BUT mál%
- %Ástæða fyrir ógildingu tilboðs%
- %Ástæða breytinga%
- %Breytingar gerðar af%
- %Company%
- %BUT mál heiti%
- %Lokadagur Tími%
- %Date%

%Ástæða skila kauptilboðs% og %Ástæða fyrir breytingum% tákn er skipt út fyrir texta sem innkaupastjóri getur fært inn þegar hann lýkur við breytingar í **Breytingar** leiðsagnarforritinu. Gildi fyrir %Breytingar gerðar af% og %Company% tákn eru sjálfkrafa tekin úr tilboðsbeiðni. %Date% tákninu er skipt út fyrir núgildandi dagsetningu.

Ef á að hætta í BUT eftir að það hefur verið sent, er hægt að gera það frá RFQ-verkinu. Fyrir afturköllun á sniðmáti fyrir tölvupóst er þess krafist að senda tilkynningu afturköllunar til tengiliðs lánardrottins. Sniðmátið verður að vera valið á síðunni **Færibreytur innkaupa og aðfanga**. Þegar sniðmát er stofnað getur það innihaldið eftirfarandi endurnýjunartákn:

- %Ástæða afturköllunar%
- %BUT mál%
- %BUT afturkallað af%
- %Company%
- %BUT mál heiti%
- %Date%

%Ástæða afturköllunar kauptilboðs% tákn er skipt út fyrir texta sem innkaupastjóri getur fært inn í **Afturköllun** leiðsagnarforritinu. %Date% tákninu er skipt út fyrir núgildandi dagsetningu.

Ef óskað er að nota ástæðukóða á tilboði til að tilgreina hvers vegna því var hafnað eða samþykkt verður að setja upp ástæðukóða á síðunni **Ástæður lánardrottins**.

Hægt er að skilgreina útlit prentaðra eða vistaðra BUT-skjala á síðunni **Uppsetning eyðublaða** í Innkaup og aðföng.

> [!NOTE]
> Í grunnstillingum fyrir hið opinbera verður þú að nota leiðréttingarferlið til að breyta BUT sem hefur þegar verið sent. Þegar BUT er sent eru reitir læstir.
Þar af leiðir, að til þess að gera breytingar á BUT verður þú að velja **Búa til** til að hefja lagfæringuna, eins og lýst er hér að framan. Læsingar hegðun er stjórnað af **Læsa BUT þegar þeir eru sendir** valkostur á **Innkaup og aðföng færibreytur** síðunni. Sjálfgefið er þessi færibreyta stilltur á **Já** í grunnstillingum fyrir hið opinbera, ekki er hægt að breyta sjálfgefin stilling. Þess vegna, þótt lagfæringarferlið geti verið meðhöndluð handvirkt í grunnstillingum fyrir óopinbera aðila, verður að nota það í grunnstillingum fyrir opinbera aðila.

Þegar BUT-verk er stofnað af gerð innkaupapöntunar og birgðavöru er bætt við BUT, er birgðafærsla mynduð sem hefur innhreyfingarstöðuna **Innhreyfing tilboðs**. Aðeins BUT-línur sem hafa þessa stöðu eru teknar til greina þegar aðaláætlun er notuð til að reikna vistir. Ef óskað er eftir að aðaláætlun innihaldi BUT-verklínur sem áætluð innhreyfing þarf að skilgreina þessa hegðun í uppsetningu á aðaláætlanagerð.

Sem innkaupastjóri eða umboðsmaður, getur þú stofnað og viðhaldið beiðnagerðum til falla að innkaupakröfum fyrirtækis þíns. Hverja beiðnagerð má tengja við aðferðir við stigagjöf. Aðgerðir við stigagjöf samanstendur af safni skilyrða sem hægt er að nota þegar tilboðum fá stigagjöf. Setja verður upp beiðnagerðir, stigagjöf og skilyrða á síðunum **gerð Beiðni** og **Stigagjöf**.

## <a name="choose-default-fields-to-include-in-vendor-rfq-reply-forms"></a><a name="default-reply-fields"></a>Velja sjálfgefna reiti sem á að hafa með í eyðublöðum fyrir svar við tilboðsbeiðni

Hægt er að tilgreina tilteknar gerðir af upplýsingum sem þú vilt fá frá lánardrottnum þegar þeir svara (bjóða í) beiðni um tilboð (RFQ). Reitir sem eru merktir sem sjálfgefnir eru teknir með í eyðublaðinu á netinu fyrir samstarf lánardrottna. Til að gera þessar stillingar:

1. Ef það hefur ekki þegar verið gert er hægt að nota síðuna [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að virkja eiginleikann *Velja reiti tilboðsbeiðni sem á að hafa með í eyðublöðum sem innihalda svar lánardrottins við tilboðsbeiðni*.
1. Farið í **Innkaup og aðföng > Uppsetning > Færibreytur innkaupa og aðfanga**.
1. Opnið flipann **Beiðni um tilboð**.
1. Veljið tengil svarreitanna **Sjálfgefin tilboðsbeiðni** undir hausnum **Setja upp sjálfgildi fyrir beiðnir um tilboð**.
1. Svarglugginn **Sjálfgefnir svarreitir tilboðsbeiðni** opnast.
1. Hlutinn **Reitir tilboðsbeiðni sem hafðir eru með í eyðublöðum sem innihalda svar lánardrottins við tilboðsbeiðni** inniheldur sleða fyrir hvern reit sem hægt er að nota í eyðublöðum fyrir svar við tilboðsbeiðni. Reitir sem eru stilltir á *Já* í þessum hluta verða teknir með (ásamt gildunum þeirra) í eyðublöðum fyrir svar við tilboðsbeiðni. Stillið sleðann á *Nei* fyrir hvern reit þar sem koma á í veg fyrir að lánardrottnar sjái gögn þegar tilboð er skoðað. Þetta gerir þér kleift að færa inn áætluð eða væntanleg gildi við færslu tilboðsbeiðni til nota innanhúss án þess að lánardrottinn sjái hvað hefur verið fært inn.

Hægt er að hnekkja þessum stillingum fyrir einstök tilvik tilboðsbeiðna eftir þörfum.

## <a name="creating-and-sending-an-rfq"></a>Stofna og senda inn beiðni um TILBOÐ

BUT-verk er stofnað, lánardrottnar eru valdir sem óskað er að gera kauptilboð fyrir BUT-verkið og síðan er BUT sent til lánardrottna. Hægt er að nota prentstillingum til að beina BUT-skýrslunni og svarblaðsskýrslum á æskilegan áfangastað.

Hægt er að stofna BUT-verk handvirkt fyrir annaðhvort innkaupagerðina **Innkaupapöntun** eða **Innkaupasamningur**.

Ef BUT-verkið er af gerðinni **Innkaupapöntun** mun eftirfarandi hegðun eiga sér stað sem víkur frá öðrum gerðum af BUT-verkum:

- Þegar BUT-verklínur eru stofnaðar eru birgðafærslur myndaðar með innhreyfingarstöðuna **Innhreyfing tilboðs**.
- Þegar kauptilboð er samþykkt, er innkaupapöntun mynduð.

Ef BUT er af gerðinni **Innkaupasamningur**, á eftirfarandi hegðun sér stað sem víkur frá öðrum BUT-verkum:

- BUT-verk er notað sem samningur um að kaupa ákveðið magn eða virði afurðar yfir tíma. Ef valin er þessi gerð innkaupa þarf að velja dagsetningasvið sem á við innkaupasamninginn og nafn þess einstaklings sem hefur umsjón með innkaupasamningnum.
- Þegar kauptilboð er samþykkt, er innkaupasamningur myndaður.

Ef BUT-verk er myndað úr innkaupabeiðni er gerðinni **Innkaupabeiðni** sjálfkrafa úthlutað. Ekki er hægt að stofna BUT-verk handvirkt með gerðina **Innkaupabeiðni**.

Hægt er að stofna BUT-verk úr innkaupabeiðni aðeins ef staða innkaupabeiðninnar er **Í yfirferð** og næsta verkflæðisverki er úthlutað á þig. Línur í innkaupabeiðninni eru uppfærðar sjálfkrafa þegar þú samþykkir línur úr tilboðum (BUT-svör) sem voru móttekin frá lánardrottnum. Ekki er hægt að ljúka, hafna, samþykkja eða framkvæma aðrar aðgerðir á innkaupabeiðninni fyrr en innkaupabeiðnilínan er uppfærð með samþykktri BUT-línu eða hætt er við BUT-verkið.

Þegar BUT-verk er stofnað er hægt að velja tiltekna beiðnagerð. Beiðnagerðin ákvarðar safn skilyrða sem notuð eru til að meta BUT-svör við BUT-verkum.

Hægt er að bæta spurningalista við BUT-verk. Þessi spurningalisti birtist síðan í öllum BUT-svörum eftir að BUT er sent. Það er áskilið verk að ljúka spurningalistanum áður en hægt er að senda tilboðið.

Þó að sjálfgildin séu gefin upp er hægt að breyta stillingunum **Reitir tilboðsbeiðni sem hafðir eru með í eyðublöðum sem innihalda svar lánardrottins við tilboðsbeiðni** fyrir hverja tilboðsbeiðni fyrir sig eftir þörfum. Til að gera það skal stofna eða opna tilvik af tilboðsbeiðni. Síðan, á aðgerðasvæðinu, skal opna flipann **Tilboð** og, úr hlutanum **Svör**, skal velja **Stilla sjálfgildi svars við tilboðsbeiðni**. Svarglugginn **Sjálfgefnir svarreitir tilboðsbeiðni** opnast, sem virkar á sama hátt og þegar sjálfgildin eru stillt fyrir eyðublöð fyrir svar við tilboðsbeiðni lánardrottins, fyrir utan að breytingarnar hér hafa aðeins áhrif á núverandi svar tilboðsbeiðni. Frekari upplýsingar um hvernig á að virkja þessa virkni og hvernig hún virkar er að finna í [Velja sjálfgefna reiti sem á að hafa með í eyðublöðum fyrir svar við tilboðsbeiðni](#default-reply-fields).

Það eru þrjár leiðir til að velja þá lánardrottna til að bæta við BUT-verk:

- Bæta við lánardrottnum einum í senn.
- Leita að öllum lánardrottnum sem uppfylla tiltekiin skilyrði.
- Bæta sjálfkrafa við öllum lánardrottnum sem hafa verið samþykktir fyrir innkaupategundir sem notaðar eru í BUT-verklínum.

Þegar BUT-málið er tilbúið er smellt á **Senda**. Aðgerðin Senda myndar færslubækur og skýrslur sem verða prentaðar, skjalaðar og sendar í samræmi við prentstillingarnar.

Ef þú stillir **Nota lánardrottin til að endurreikna verð** og **Nota vöruupplýsingar sem eiga við lánardrottna** á **Já** á síðunni **Sendir tilboðsbeiðni** þegar BUT er send til lánardrottins, eru sumar upplýsingar tengdar lánardrottnum sjálfkrafa færðar inn í BUT fyrir þann lánardrottin.

## <a name="amending-an-rfq-case"></a>Breyting á BUT-verki

Einstaka sinnum þarf að breyta BUT-verki þegar búið er að senda það. Þú gætir þurft að breyta BUT-verki, ef til dæmis afhendingardagsetningum hefur verið breytt eða ef þú vilt fleiri afurðir eða annað magn afurða. Hægt er að skilgreina ferli lagfæringar þannig að það er annað hvort meira eða minna takmarkandi.

Ef notað er meira takmarkandi lagfæringarferli þarf að smella á **Stofna** á BUT-málinu til að hefja lagfæringu áður en hægt er að breyta reitum á BUT-máli sem þegar hefur verið sent. Eftir að lokið hefur verið við lagfæringar, verður að smella á **Fullvinna**. Þú verður svo að leiddur í gegnum ferlið við að bæta upplýsingum við tölvupóstinn sem eru send til að tilkynna lánardrottnum um lagfæringar. Uppfærð BUT skýrsla, sem felur í sér athugasemd um lagfæringar, tengist sjálfkrafa við skilaboðin.

Ef grunnstilling þín felur í sér minna takmarkandi lagfæringarferli þarf ekki að velja **Stofna** áður en hægt er að breyta reitum BUT-máls sem hefur þegar verið send. Hins vegar þarf að bæta athugasemd um lagfæringu handvirkt við BUT og senda málið aftur. Hafðu í huga að þessi nálgun er aðeins hægt að nota ef ekkert svaranna (tilboðin) hefur verið breytt. Ef þú hefur slegið inn svar og það er í **Móttekið** ástandi er **Senda** hnappurinn ekki tiltækur. Í þessu tilfelli verður þú að velja **Búa til** og síðan **Fullvinna**, eins og þú verður að gera í meira takmarkandi ferli. Svarið er síðan endurstillt til að endurspegla breytingar á BUT-málinu.

Ef lánardrottnar nota lánardrottna samstarfsviðmótið til að slá inn tilboð verður þú alltaf að nota lagfæringarferlið til að tilkynna lánardrottnum um breytingar á BUT-málinu. Þetta ferli hjálpar til við að koma í veg fyrir aðstæður þar sem lánardrottnar bjóða í úrelt BUT-verk á meðan tilboð þeirra er í vinnslu. Nánari upplýsingar um samstarf lánardrottna er að finna í [Samstarf lánardrottna við utanaðkomandi lánardrottna](/dynamics365/unified-operations/supply-chain/procurement/vendor-collaboration-work-external-vendors).

Ef þú vilt bjóða fleiri lánardrottnum að bjóða, og engar breytingar hafa verið gerðar á BUT-málinu, getur þú notað **Senda** hnappinn. Söluaðilarnir sem þú bættir við munu birtast á síðunni **Senda** og fá tölvupóstboðið.

## <a name="receiving-and-registering-rfq-replies"></a>Móttaka og skrá svör við BUT

Þegar BUT er send, er svarblað stofnað sjálfkrafa. Þegar kauptilboð berast í BUT verður að slá þau inn á síðunni **Beiðni um tilvitnun** með því að smella á aðgerðina **Breyta BUT-svari.** Þetta mun leyfa þér að slá inn tilboðsupplýsingarnar í sérstöku tilboðsformi. Upphaflega mun **Svarframvinda** vera **Ekki byrjað**. Þegar smellt er á **Breyta BUT-svari** er framvindustaðan **Innkaupandi er að uppfæra** þar til tilboðið er sent inn. Smelltu á **Senda** þegar þú hefur slegið inn tilboðsupplýsingar. Staða á framvindu svars mun breytast í **Sent af innkaupanda.** Á svipaðan hátt, með samstarf lánardrottna virkt, mun **Svarframvinda** uppfærast þegar lánardrottinn vinnur með tilboðið. Staðan breytist síðan frá **Lánardrottinn er að uppfæra** í **Sent af lánardrottni**. Þegar tilboðið er lagt fram er færslubók stofnuð sem **Móttekin**. Svarið (tilboðið) þarf að leggja fram til að hægt sé að skrá það sem móttekið og aðeins þá er hægt að vinna það frekar sem samþykkt eða hafnað.

Ef reynist þörf á að uppfæra tilboðið ætti að fara í gegnum sama ferlið og að ofan og senda inn aftur.

Athuga skal að breyting á eyðublaðinu **Beiðni um tilboð** er aðeins leyfð fyrir upplýsingar sem tengjast vinnslu tilboðsins, ekki til að slá inn tilboðið. Til að slá inn eða breyta tilboði skal smella á **Breyta BUT-svari.**

Þegar tilboðsupplýsingar eru slegnar inn og ef BUT-verkið leyfir aðrar línur, er hægt að bæta við öðrum línum fyrir línur sem aðeins hafa innkaupategund og ekki tilgreint vörulistaratriði. Smelltu á **Bæta við öðrum** til að bæta við öðrum línum.

Ef svar hefur verið fært inn en krafist er að fá nýtt tilboð frá lánardrottni er hægt að skila BUT. Ný færslubók og skýrsla er mynduð sem hægt er að senda til lánardrottins.

Hægt er að sjá yfirlit yfir allar BUT og stöður þeirra: **Sent, móttekið, samþykkt, hafnað, hætt við, neitað** á síðunni **Eftirfylgni á beiðni um tilboð**.

### <a name="accepting-and-rejecting-bids-and-transferring-accepted-bids-to-downstream-documents"></a>Samþykkja og hafna kauptilboðum og flytja samþykkt kauptilboð yfir í skjöl á niðurleið

Eftir að þú hefur greint bestu kauptilboðin, svo sem kauptilboðið sem býður upp á bestu heildarverð, samþykkir þú kauptilboðið. Sumar línur í kauptilboði eru hægt að samþykja og hafna öðrum.
Einnig er hægt að samþykkja línur úr öðrum lánardrottnum. Hafðu í huga að ef sumar línur er samþykktar, verður beðið um að hafna öllum öðrum línum. Þess vegna, ef óskað er að samþykkja aðrar línur verður að smella á **Hætta Við** þegar sú beiðni berst. Staða á BUT svari til sérhvers lánardrottins sem þú samþykkir kauptilboð eða línur frá, er uppfærð í **Samþykkt**.

Ef þarf, á meðan innkaupapöntun eða innkaupasamningur er undirbúinn, að bæta við viðbótarlínu við BUT er hægt að gera það með því að smella á **Bæta við línu** á hnitaneti síðunnar **Beiðni um tilboð**. Einungis er hægt að skoða og breyta þessari línu á síðunni **Beiðni um tilboð**. Hún verður sýnileg á tilboðssíðunni þegar hún er samþykkt.

Þegar kauptilboð eða ein eða fleiri línur úr kauptilboði er innkaupapöntun eða innkaupasamningur myndaður sjálfkrafa. Þú getur þá hafnað tilboðum frá öllum öðrum lánardrottnum.

Við svar, er hægt að bæta inn ástæðukóða til að útskýra hvers vegna kauptilboð var samþykkt eða hafnað.

Þegar kauptilboð er samþykkt af gerðinni **Innkaupabeiðni** verður innkaupabeiðnilínur uppfærðar með eftirfarandi upplýsingum sem endurspegla upplýsingar um samþykkt tilboð:

- Einingarverð
- Afsláttarprósenta
- Afsláttarupphæð
- Innkaupagjöld
- Línugjöld
- Lánardrottinn
- Ytra númeri
- Ytri lýsing

Eftirfarandi tafla sýnir stöðubreytingar BUT þegar kauptilboð frá lánardrottnum eru samþykkt og hafnað.

## <a name="statuses--highest-and-lowest"></a>Stöður - hæsta og lægsta

Á flipa lánardrottins í BUT-verki er hægt að sjá línurnar með hæstu og lægstu stöðu tiltekins lánardrottins. Þegar lánardrottni er bætt við og engar línur hafa enn verið sendar eru bæði lægsta og hæsta staðan <strong>Stofnað.</strong> Þegar beiðni um tilboð er send til lánardrottins með öllum línum verður staða línanna tveggja <strong>Sent</strong>. Ef einhverjar línur í kauptilboði frá lánardrottni eru samþykktar og öðrum er hafnað munu höfnuðu línurnar fá lægstu stöðu sem er <strong>Hafnað</strong> og samþykktu línurnar fá hæstu stöðu sem er <strong>Samþykkt</strong>.

Á BUT-verklínum er hægt að sjá hæstu og lægstu stöður fyrir hverja línu yfir alla lánardrottna. Ef lína hefur verið send á alla lánardrottna í BUT-verki og enginn hefur brugðist við eru bæði lægsta og hæsta staða **Sent.** Þegar að minnsta kosti einn lánardrottin bregst við mun hæsta staðan breytast í **Móttekið**. Ef nýjum lánardrottna er bætt við verkið mun lægsta staða breytast í **Stofnað**

Hæsta og lægsta staða í BUT-verki er uppsöfnun á stöðunni á \<Flipa lánardrottins og flipa línu.

Stöðunum er raðað á eftirfarandi hátt frá lægsta til hæsta: Stofnað, sent, móttekið, hafnað, samþykkt, neitað, hætt við.

Eftirfarandi töflur sýna hvernig staða BUT-verks breytist þegar BUT-verk er stofnað með línum og sendir það síðan til lánardrottna.

| **Aðgerð**                                | **Lægsta staða BUT-verks** | **Hæsta staða BUT-verks** | **Lægsta staða BUT-verklínu** | **Hæsta staða BUT-verklínu** |
|-------------------------------------------|----------------------------|-----------------------------|---------------------------------|----------------------------------|
| Búið til BUT-verkhaus og línu.      | Búið til                    | Búið til                     | Búið til                         | Búið til                          |
| Senda BUT til allra lánardrottna í BUT-verki. | Sent                       | Sent                        | Sent                            | Sent                             |
| Bæta við öðrum lánardrottni.                       | Búið til                    | Sent                        | Búið til                         | Sent                             |
| Senda tilboðsbeiðni til síðari lánardrottins.        | Sent                       | Sent                        | Sent                            | Sent                             |

Allar línur í BUT sem tengjast BUT-verkinu verða í **Sent** ástandi.

Eftirfarandi tafla sýnir stöðubreytingar BUT eftir því sem kauptilboð eru móttekin og upplýsingar skráðar í svarblað BUT.

| **Aðgerð**                                               | **Lægsta staða yfir allar línur í öllum BUT** | **Hæsta staða yfir allar línur í öllum BUT** | **Lægsta staða BUT-verkhauss** | **Hæsta staða BUT-verkhauss** | **Lægsta staða BUT-verklínu** | **Hæsta staða BUT-verklínu** |
|----------------------------------------------------------|------------------------------------------------|-------------------------------------------------|-----------------------------------|------------------------------------|---------------------------------|----------------------------------|
| Skrá eitt tilboð lánardrottins á BUT og vista það.        | Sent                                           | Móttekið                                        | Sent                              | Móttekið                           | Sent                            | Móttekið                         |
| Skrá annað tilboð lánardrottins á BUT og vista það. | Móttekið                                       | Móttekið                                        | Móttekið                          | Móttekið                           | Móttekið                        | Móttekið                         |


Í dæminu hér að neðan er hægt að sjá hæstu og lægstu stöðu í BUT-verki þar sem eitt kauptilboð hefur verið móttekið og hitt tilboðið hefur verið samþykkt. Þegar mótteknu kauptilboði er hafnað mun lægsta staðan breytast frá móttekinni stöðu til hafnaðrar stöðu í BUT-verkhaus og línu.


|            <strong>Aðgerð</strong>             | <strong>Lægsta staða yfir allar línur í öllum BUT</strong> | <strong>Hæsta staða yfir allar línur í öllum BUT</strong> | <strong>Lægsta staða BUT-verkhauss</strong> | <strong>Hæsta staða BUT-verkhauss</strong> | <strong>Lægsta staða BUT-verklínu</strong> | <strong>Hæsta staða BUT-verklínu</strong> |
|------------------------------------------------|-------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------|-------------------------------------------------|----------------------------------------------|-----------------------------------------------|
| Samþykkja eitt af tilboðunum. (eða að minnsta kosti ein lína) |                          Móttekið                           |                           Samþ.                           |                    Móttekið                    |                    Samþ.                     |                   Móttekið                   |                   Samþ.                    |
|           Hafna öllum öðrum kauptilboðum.           |                          Hafnað                           |                           Samþ.                           |                    Hafnað                    |                    Samþ.                     |                   Hafnað                   |                   Samþ.                    |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]