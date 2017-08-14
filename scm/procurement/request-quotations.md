---
title: "Beiðni um tilboð"
description: "Þetta efnisatriði veitir yfirlit yfir tilboðsbeiðnir (BUT) sem fyrirtæki gefa út þegar þau þurfa að kaupa vöru eða þjónustu og vilja fá samkeppnishæf tilboð frá mörgum lánardrottnum."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchRFQCaseTable, PurchRFQCaseTableListPage, PurchRFQCompare, PurchRFQReplyTable, PurchRFQVendReplyTableListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2154
ms.assetid: 3936996e-d943-46ca-8385-84c042990f1d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 47e394c8642f502c698dbcd5506979b7cac0a830
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---

# <a name="request-for-quotations-rfqs"></a>Beiðni um tilboð

[!include[banner](../includes/banner.md)]


Þetta efnisatriði veitir yfirlit yfir tilboðsbeiðnir (BUT) sem fyrirtæki gefa út þegar þau þurfa að kaupa vöru eða þjónustu og vilja fá samkeppnishæf tilboð frá mörgum lánardrottnum. Í beiðni um tilboð, eru lánardrottnar beðnir um að leggja fram verð og afhendingartíma fyrir magn þeirra vara sem er tilgreint. Einnig er hægt að biðja lánardrottna að tilgreina hvort einhver tilfallandi gjöld eru, eins og sendingarkostnaður, eða hvort lánardrottinn býður upp á afslátt fyrir stórar pantanir eða flýtigreiðslu reiknings lánardrottins.

Beiðni um tilboð (BUT) ferli fjallar um eftirfarandi:

-   Stofna og senda beiðni um TILBOÐ í einum eða fleiri lánardrottnum.
-   Móttaka og skrá svör við tilboð.
-   Flytja samþykkt útboð yfir í innkaupapöntun, innkaupasamning eða innkaupabeiðni.

Eftirfarandi skýringarmynd veitir yfirlit yfir vinna beiðni um TILBOÐ.  

[![Ferlið beiðni um tilboð](./media/rfq-process-458x1024.jpg)](./media/rfq-process.jpg)  

Hægt er að stofna BUT frá áætlaðar pantanir, úr innkaupabeiðni eða úr handvirkum innslætti. BUT sem eru stofnuð eru kölluð BUT mál og þetta er grunnskjal sem er notað til að gefa út BUT á hvern lánardrottin. Eftir að búið er að útbúa BUT og bæta við lánardrottnum, smellið á **Senda** á BUT og BUT-færslubók er mynduð fyrir hvern lánardrottinn sem BUT er send til. Hægt er að skilgreina prentstýringaruppsetningu fyrir Senda aðgerð til að prenta skýrslu fyrir hvern lánardrottin í safni eða senda skýrslu á tölvupóstfang hvers lánardrottins. Þar að auki er hægt að nota BUT-færslubók  fyrir hvern lánardrottinn til að mynda skýrslu sem hægt er að senda eða endursenda seinna til lánardrottins. Einnig er hægt að skilgreina aðgerðina Senda til að mynda svarblað sem lánardrottinn getur fyllt út.  

Ef þarf að lagfæra BUT þegar búið er að senda hana, er hægt að endursenda BUT til lánardrottna þegar því hefur verið lokið.  

Þegar kauptilboð berast þarf að færa þau í **Svör við BUT** síðu. Ef valið er **Afrita gögn í svar** valkosturinn, eru gögn eins og magn og dagsetningar úr BUT afritaðar í svarið. Hægt er að breyta þessum gögnum til að endurspegla kauptilboð lánardrottins.  

Ef önnur ítrekun svars er krafist fyrir tiltekna lánardrottna, smellið á **Skila** á **Svör við BUT** síðu. Skilaaðgerð myndar nýja færslubók og skýrslu sem verða prentaðar, skjalaðar og send, í samræmi við prentstýringarstillingarnar.  

Ef skilyrði fyrir stigagjöf er bætt við BUT málið skal BUT svarið hafa vettvang fyrir stigagjöf þar sem hægt er að færa inn stig. Samtals stig birtast þegar borin eru saman svör á siðuni **bera Saman svör**, þar sem hægt er að bera saman önnur svargögn, svo sem línuverð, afhendingardag og heildarverð.  

Eftir að kauptilboð eða hluti af kauptilboði hefur verið skilgreint er hægt að samþykkja það og hafna afganginum. Samþykki á færslubókum, höfnun færslubækur og samsvarandi skýrslur eru myndaðar. Þær verða prentaðar, skjalaðar og sendar í samræmi við prentstýringarstillingarnar. Þegar þú samþykkir kauptilboð eða tilteknar línur í kauptilboði, er annaðhvort innkaupasamningur eða innkaupapöntun mynduð eða innkaupabeiðni er uppfærð, það fer eftir gerð BUT innkaupanna. Hægt er að stofna verðsamninginn sem hægt er að nota síðar fyrir hvaða svör sem er, óháð því hvort þau voru samþykkt eða þeim hafnað.  

Staða BUT kemur fram í BUT hausnum og fer eftir stöðu BUT-línanna. Staðan tilgreinir að hversu miklu leyti búið er að vinna BUT. Hver beiðni um TILBOÐ hefur tvö gildi fyrir stöðu: lægstu og hæstu. Lægsta staða er ítarlega kosti stig línu í beiðni um TILBOÐ og hæsta staðan er oftast ítarlega stig línu í beiðni um TILBOÐ. Til dæmis, ef minnst ítarlegt stig í BUT er fyrir línu sem hefur verið stofnuð, er lægsta staða fyrir BUT **mynduð** . Ef mest ítarlega stig í BUT er fyrir línu sem hefur verið send til lánadrottna, er hæsta staða fyrir BUT **Sent** . Staða er uppfærð sjálfkrafa sem er að vinna beiðni um TILBOÐ.  

Hægt er að skoða lægstu og hæstu stöðu fyrir BUT- haus á síðunni **Allar beiðnir um tilboð**. Hægt er að skoða lægstu og hæstu stöðu fyrir BUT-línu á flipanum **Línur** á síðunni **Beiðni um tilboð**.  

Röð staða til að vinna BUT er sem hér segir:

1.  **Stofnað**
2.  **Send**
3.  **Móttekið**
4.  **Samþykkt**/**Hætt við**/**Hafnað**

Stöðunum verður lýst nánar í seinni hlutum þessa efnisatriðis.

## <a name="setting-up-rfq-functionality"></a>Setja upp virkni BUT
Áður en hægt er að stofna BUT-verk, verður að setja upp upplýsingar um BUT á síðunni **færibreytur Innkaupa og uppruna**. Þegar BUT-verk er stofnað er hægt að tilgreina sjálfgefin gildi eru afrituð í BUT. Þú getur tilgreint eftirfarandi sjálfgildi:

-   Gerð innkaupa fyrir nýjar tilboðsbeiðnir: **Innkaupapöntun** eða **Innkaupasamningur**.
-   Stillingar fyrir lokadag og -tíma.
-   Upplýsingar um greiðslu og afhendingarskilmála.
-   Svæðin sem eiga að fylgja með í svari við tilboðsbeiðni.

Hægt er að hnekkja þessi gildi fyrir tiltekið BUT-verk. Einnig ætti að skilgreina ferli breytingar. Hluti af þessari stillingu er að hægt er að kveikja á svæðislæsingu. Þegar kveikt er á svæðislæsingu þarf innkaupastjóri sem vill lagfæra BUT fyrst að smella á **Stofna** í **Breytingar** hluta í **Tilboð** flipa. Eftir að tilboðsbeiðni hefur verið uppfærð með breytingum, verður innkaupastjóri að ljúka við ferlið með því að smella á **Ljúka**. Aðgerðin **Ljúka** býr til tölvupóst sem tilkynnir lánardrottnum um breytta tilboðsbeiðni. Velja sniðmát fyrir tilkynningu í tölvupósti sem er send til lánardrottna á síðunni **færibreytur Innkaupa og uppruna**. Þegar sniðmát er stofnað getur það innihaldið eftirfarandi endurnýjunartákn:

-   %Ástæða fyrir ógildingu tilboðs%
-   %Ástæða breytinga%
-   %Breytingar gerðar af%
-   %Fyrirtæki%

% Ástæða skila kauptilboðs % og % Ástæða fyrir breytingum % tákn er skipt út fyrir texta sem innkaupastjóri getur fært inn þegar hann eða hún lýkur við breytingar í **Breytingar** leiðsagnarforritinu. Gildi fyrir % Breytingar gerðar af % og % Fyrirtækis % tákn eru sjálfkrafa tekin úr BUT.  

Ef óskað er að nota ástæðukóða á svari við BUT til að tilgreina hvers vegna tilboði var hafnað eða samþykkt verður að setja upp ástæðukóða á síðunni **ástæður Lánardrottna**.  

Hægt er að skilgreina útlit prentaðra eða vistaðra BUT- skjala á síðunni **Uppsetning bréfs** í Innkaup og uppruna. 

**Athugaðu:** Ef stillingar fyrir opinbera geirann eru notaðar, kalla allar breytingar á tilboðsbeiðni sem hafa þegar verið sendar á notkun breytingaferlisins. Þegar tilboðsbeiðni er send eru reitir læstir, þannig að til að gera breytingar á tilboðsbeiðni verður að smella á **Stofna** til að nota breytingaferlið eins og lýst er að ofan.
Þessu er stýrt af svæðislæsingunni **Læsa beiðnum um tilboð þegar þær eru sendar** í **Færibreytur innkaupa og aðfanga**. Þessi færibreyta er stillt á **Já** og fyrir stillingu opinbera geirans er þetta sjálfgildi sem ekki er hægt að breyta. Þetta þýðir að þó að hægt sé að meðhöndla breytingaferlið handvirkt í stillingu fyrir einkageirann, er meðhöndlun breytinga með læsingu reita eftir að tilboðsbeiðni hefur verið send skyldubundin fyrir opinbera geirann.

Þegar þú stofnar BUT fyrir innkaupapöntun, og bætir birgðavöru við BUT, er birgðafærsla stofnuð sem hefur innhreyfingarstöðuna **Innhreyfing Tilboðs**. Hafðu aðeins BUT-línur af þessu tagi í huga þegar þú notar aðaláætlun til að reikna vistir. Ef óskað er eftir að aðaláætlun innihaldi BUT-línur sem áætluð innhreyfing þarf að skilgreina þessa hegðun í uppsetningu á áætlanagerð.  

Sem innkaupastjóri eða umboðsmaður, getur þú stofnað og viðhaldið beiðnagerðum til að samsvara innkaupakröfum fyrirtækis þíns. Hver beiðnagerð getur keyrt stigagjöf aðferðir. Aðgerðir við stigagjöf samanstendur af safni skilyrða sem hægt er að nota þegar tilboðum fá stigagjöf. Setja verður upp beiðnagerðir, stigagjöf og skilyrða á síðunum **gerð Beiðni** og **Stigagjöf**.

## <a name="creating-and-sending-an-rfq"></a>Stofna og senda inn beiðni um TILBOÐ
Þú stofnar BUT, velur þá lánardrottna sem óskað er að gera kauptilboð fyrir BUT og sendir BUT til lánardrottna. Hægt er að nota prentstjórnunarkerfið til að beina BUT-skýrslunni og svarblaðs skýrslum á æskilegan áfangastað.  

Þú getur gert BUT fyrir **Innkaupapöntun** eða **Innkaupasamning** innkaupagerðir.  

Ef BUT er mynduð úr innkaupabeiðni er **Innkaupabeiðni** gerð sjálfkrafa úthlutað. Ekki er hægt að stofna BUT handvirkt með **Innkaupabeiðni** gerð. Ef BUT er af gerðinni **innkaupapöntun**:

-   Þegar BUT-línur eru stofnaðar, eru birgðafærslur myndaðar með innhreyfingarstöðuna **innhreyfing Tilboðs**.
-   Þegar kauptilboð er samþykkt, er innkaupapöntun mynduð.

Ef BUT er af gerðinni **Innkaupasamningur**:

-   BUT er notað sem samningur um að kaupa ákveðið magn eða virði vöru yfir tíma. Ef valin er þessi gerð innkaupa þarf að velja dagsetningasvið sem á við innkaupasamninginn og nafn þess einstaklings sem hefur umsjón með innkaupasamningnum.
-   Þegar kauptilboð er samþykkt, er innkaupasamningur myndaður.

Þú getur aðeins stofnað BUT úr innkaupabeiðni ef staða innkaupabeiðninnar er **í yfirferð** og  næsta verkflæðisverki er úthlutað á þig. Línur í innkaupabeiðninni eru uppfærðar sjálfkrafa þar sem hægt er að samþykkja línur úr svörum við BUT (kauptilboð) sem voru mótteknar frá lánardrottnum. Ekki er hægt að framkvæma aðgerðir í innkaupabeiðninni á borð við að ljúka henni, hafna eða samþykkja á meðan BUT er í vinnslu.  

Þegar BUT er stofnað er hægt að velja tiltekna gerð beiðni. Gerð beiðni ákvarðar safn skilyrða sem notuð er til að stiga svör við BUT.  

Hægt er að bæta spurningalista við BUT-verk. Þessi spurningalisti birtist síðan í öllum svörum eftir að BUT er sent.  

Það eru þrjár leiðir til að velja þá lánardrottna til að bæta við BUT-verk:

-   Bæta við lánardrottnum einum í senn.
-   Leita að öllum lánardrottnum sem uppfylla tiltekiin skilyrði.
-   Bæta sjálfkrafa við öllum lánardrottnum sem hafa verið samþykktir fyrir innkaupategundir sem notaðar eru í BUT- línum.

Þegar BUT-verkið er tilbúið er smellt á **Senda**. Aðgerðin Senda myndar færslubók og skýrslu sem verða prentaðar, skjalaðar og sendar í samræmi við prentstýringarstillingarnar.  

Ef valið er **Nota lánardrottin til að endurreikna verð** og **Nota vöruupplýsingar sem eiga við lánardrottna** gátreitina á **Sending tilboðsbeiðni** síðunni þegar beiðni er send til lánadrottna, eru sumar upplýsingar tiltekins lánardrottins sjálfkrafa færðar inn. Hægt er að breyta þessum upplýsingum á siðunni **Beiðni um svar við tilboði**.  

Eftirfarandi tafla sýnir stöðubreytingar BUT þegar BUT er stofnuð og send til lánardrottna.

|                                    |                              |                                                 |                            |                             |
|------------------------------------|------------------------------|-------------------------------------------------|----------------------------|-----------------------------|
| **Aðgerð**                         | **Lægsta hausstaða BUT** | **Hæsta hausstaða BUT**                   | **Lægsta línustaða BUT** | **Hæsta línustaða BUT** |
| Stofna beiðni um TILBOÐ hauss og línu.    | Stofnaður                      | Stofnaður                                         | Stofnaður                    | Stofnaður                     |
| Senda beiðni um tilboð á tiltekinn lánardrottin. | Sent                         | Sent                                            | Sent                       | Sent                        |
| Bæta við öðrum lánardrottni.                | Stofnaður                      | Sent(beiðni um tilboð hefur aðeins verið send til einn lánardrottins.) | Stofnaður                    | Sent                        |
| Senda tilboðsbeiðni til síðari lánardrottins. | Sent                         | Sent                                            | Sent                       | Sent                        |

**Ábending:** Hægt er að bæta fleiri lánardrottnum við BUT hvenær sem er og lægsta og hæsta staða breytast til að endurspegla lánardrottna sem var bætt við. Til dæmis, ef kauptilboð er móttekið frá öllum lánadrottnum og minnst ein lína kauptilboðs er samþykkt er lægsta staða í haus BUT **Hafnað**, og hæsta staðan er **Samþykkt**. Ef bætt er við nýjum lánardrottni er lægsta staða í línu nú **Stofnað**. Þess vegna breytist lægsta staða í haus BUT í **Stofnað**,og hæsta staða helst **Samþykkt** .

## <a name="amending-an-rfq"></a>Að laga BUT
Einstaka sinnum þarf að breyta BUT þegar búið er að senda hana. Þetta getur til dæmis gerst ef afhendingardagur hefur breyst, eða þú vilt bæta við vörum eða breyta magni. Hægt er að skilgreina ferli breytingar þannig að það er annað hvort meira eða minna takmarkandi.  

Ef notað er meira takmarkandi breytingaferli þarf að smella á **Stofna** á BUT-verkið til að hefja breytingu áður en hægt er að breyta reitum á BUT-verkinu. Eftir að lokið hefur verið við breytingar, verður að smella á **Ljúka**. Þú verður svo að leiddur í gegnum ferlið við að bæta upplýsingum við tölvupóstskilaboðin sem eru send til að tilkynna lánardrottnum um breytingar. Uppfærð BUT skýrsla, sem felur í sér athugasemd um breytingar, tengist sjálfkrafa við skilaboðin.  

Ef notað er minna takmarkandi breytingaferli þarf ekki að stofna breytingu áður en hægt er að breyta reitum BUT sem hefur þegar verið send. Hins vegar þarf að bæta athugasemd um breytingar við BUT.

## <a name="receiving-and-registering-rfq-replies"></a>Móttaka og skrá svör við BUT
Þegar BUT er send, er svarblað stofnað sjálfkrafa. Þegar þú færð svör (kauptilboð) við BUT skaltu slá inn upplýsingarnar frá hverjum lánardrottni á svarblað BUT fyrir lánardrottna. Ef þú hefur bætt við stigagjöf, getur þú stigað svörin. Hægt er að bera tilboð lánardrottna saman með því að raða þeim eftir stigagjöf, svo sem besta heildarverði eða besta afhendingartíma samtals.  

Ef spurningalisti er tengd við BUT, verður að færa svör við spurningunum handvirkt í svarblaðið.  

Ef þarf að færa inn aðrar línur og BUT-verkið heimilar það, skal, í flýtiflipanum fyrir **Innkaupatilboðslínur** smella á **Bæta við línu**. Færðu síðan inn upplýsingar um vöruna, eins og vörunúmer eða innkaupaflokk, magn, verð og afslátt.  

Ef svar hefur verið fært inn en krafist er að fá nýtt tilboð frá lánardrottni er hægt að endursenda BUT. Þetta býr til nýja færslubók og skýrslu sem hægt er að nota til að óska eftir breytingum frá lánardrottni.  

Hægt er að sjá yfirlit yfir allar BUT og stöður svara þeirra á síðunni **Eftirfylgni BUT**.  

Eftirfarandi tafla sýnir stöðubreytingar BUT eftir því sem kauptilboð eru móttekin og upplýsingar skráðar í svarblað BUT.

|                                                |                       |                        |                              |                               |                            |                             |
|------------------------------------------------|-----------------------|------------------------|------------------------------|-------------------------------|----------------------------|-----------------------------|
| **Aðgerð**                                     | **Staða lægsta boðs** | **Staða hæsta boðs** | **Lægsta hausstaða BUT** | **Hæsta hausstaða BUT** | **Lægsta línustaða BUT** | **Hæsta línustaða BUT** |
| Skrá í tilboð lánardrottins, og vista.        | Sent                  | Móttekið               | Sent                         | Móttekið                      | Sent                       | Móttekið                    |
| Skrá annað tilboð lánardrottins og vista það. | Móttekið              | Móttekið               | Móttekið                     | Móttekið                      | Móttekið                   | Móttekið                    |

**Ábending:** Ef kauptilboði er skilað til lánardrottins til frekari samningaviðræðna mun lægsta og hæsta staðan vera áfram **Móttekið**.

### <a name="accepting-and-rejecting-bids-and-transferring-accepted-bids-to-downstream-documents"></a>Samþykkja og hafna kauptilboðum og flytja samþykkt kauptilboð yfir í skjöl á niðurleið

Eftir að þú hefur greint bestu kauptilboðin, svo sem kauptilboðið sem býður upp á bestu heildarverð, samþykkir þú kauptilboðið. Staða á svari til lánardrottins við BUT er uppfærð í **Samþykkt** . Þegar kauptilboð eru ákveðnar línur úr kauptilboði er samþykkt er innkaupapöntun eða innkaupasamningur myndað sjálfkrafa og tilboðum frá öðrum lánardrottnum má hafna.  

Þegar svar við BUT er samþykkt sem **Innkaupabeiðni**, eru svarlínur BUT uppfærðar í innkaupabeiðnilínunum með eftirfarandi upplýsingum:

-   Einingarverð
-   Afsláttarprósenta
-   Afsláttarupphæð
-   Innkaupagjöld
-   Línugjöld
-   Lánardrottinn
-   Ytra númeri
-   Ytri lýsing

Við svar, er hægt að bæta inn ástæðukóða til að útskýra hvers vegna kauptilboð var samþykkt eða hafnað.  

Sumar línur í kauptilboði eru hægt að samþykja og hafna öðrum. Einnig er hægt að samþykkja línur úr öðrum lánardrottnum. Hafðu í huga að ef sumar línur er samþykktar, verður beðið um að hafna öllum öðrum línum. Þess vegna, ef óskað er að samþykkja aðrar línur verður að smella á **Hætta Við** þegar sú beiðni berst.  

Eftirfarandi tafla sýnir stöðubreytingar BUT þegar kauptilboð frá lánardrottnum eru samþykkt og hafnað.

|                         |                       |                        |                              |                               |                            |                             |
|-------------------------|-----------------------|------------------------|------------------------------|-------------------------------|----------------------------|-----------------------------|
| **Aðgerð**              | **Staða lægsta boðs** | **Staða hæsta boðs** | **Lægsta hausstaða BUT** | **Hæsta hausstaða BUT** | **Lægsta línustaða BUT** | **Hæsta línustaða BUT** |
| Samþykkja eitt af tilboðunum. | Móttekið              | Samþ.                 | Móttekið                     | Samþ.                        | Móttekið                   | Samþ.                      |
| Hafna öðrum kauptilboðum.  | Hafnað              | Samþ.                 | Hafnað                     | Samþ.                        | Hafnað                   | Samþ.                      |






