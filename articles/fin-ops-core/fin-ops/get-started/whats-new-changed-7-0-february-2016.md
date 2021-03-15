---
title: Hvað er nýtt eða breytt í Dynamics AX 7.0 (febrúar 2016)
description: Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum Microsoft Dynamics AX 7.0. Útgáfan inniheldur bæði eiginleika verkvangs og forrits og var gefið út í Febrúar 2016 .
author: sericks007
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 91243
ms.assetid: 515bc6e7-a85d-4995-95c6-6cab6c8aa0f9
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3c1b63ba623eb1699938476825a77fd40d838142
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797220"
---
# <a name="whats-new-or-changed-in-dynamics-ax-70-february-2016"></a>Hvað er nýtt eða breytt í Dynamics AX 7.0 (febrúar 2016)

[!include [banner](../includes/banner.md)]

Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum Microsoft Dynamics AX 7.0. Útgáfan inniheldur bæði eiginleika verkvangs og forrits og var gefið út í Febrúar 2016 .

## <a name="cost-management"></a>Kostnaðarstýring

<table>
<thead>
<tr>
<th>Hvað hægt er að gera?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Hví er þetta mikilvægt?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Sækja stutt yfirlit yfir birgðastöðuna, verk í vinnslu (VÍV) og hvað VÍV innstreymi og VÍV útstreymi birgða hafa verið fyrir valið fjárhagsár.</td>
<td>Ekki tiltækt</td>
<td><strong>Kostnaðarstjórnun</strong> vinnusvæðið inniheldur hluta þar sem birgðayfirlit eða VÍV-birgðayfirlit er sýnt fyrir valið fjárhagstímabil. Yfirlitið er byggt á grundvelli skyndiminni gagnasafns sem, að sjálfgefnu, er uppfært á 24 tíma fresti. Skyndiminni gagnasafns er hægt að skilgreina þannig að notendur geta uppfæra það handvirkt fyrir rauntíma skýrslugerð. <strong>Kort fyrir endurhleðslustöðu gagna</strong> í <strong>kostnaðarstjórnun</strong> vinnusvæði sýnir þegar skyndiminni var síðast uppfærð.</td>
<td>Fjármálastjórar hafa áhuga á að vita hvort birgðir eða VÍV-birgðastaða eykst eða minnkar með tímanum. Með því að flokka rekstrartilvik í yfirlitinu, getur fjármálastjóra fengið yfirlit yfir hvernig birgðaflæði er. Ef birgðir eða VíV-birgðir eru metnar með staðalkostnaði, mun skráð heildar frávik einnig sjáist.</td>
</tr>
<tr>
<td>Nota skal <strong>kostnaðarstjórnun</strong> kerfiseiningu.</td>
<td>Ekki tiltækt</td>
<td>Kostnaðarstjórnun er kynnt sem ákveðið svið. Kostnaðartengdar skilgreiningar og innsýn voru dreifðar um birgðastjórnun, framleiðslustýringu og Viðskiptaskuldir.</td>
<td>Þar sem öll verk sem tengjast stjórnun kostnaðar eru miðstýrðar í einu kerfi, verður auðveldara fyrir fjármálastjóra að viðhalda í kerfinu.</td>
</tr>
<tr>
<td>Bókunargerð sem tengist birgðabókhald og framleiðslubókhald hefur verið uppfært.</td>
<td>Merki á <strong>InventPosting</strong>, <strong>Resource</strong>, <strong>ResourceGroup</strong>, og <strong>ProductionGroup</strong> skjámyndir ekki eru alltaf samstilltar við <strong>LedgerPostingType</strong> merki sem eru raunverulega notuð. Ekki er auðvelt að skilja orðaforðann sem notað er í merki.</td>
<td>Merki hafa verið uppfærð svo merki á <strong>InventPosting</strong>, <strong>Resource</strong>, <strong>ResourceGroup</strong>, og <strong>ProductionGroup</strong> síðum stemma við raunveruleg <strong>LedgerPostingType</strong> merki. Öll merki hafa einnig verið endurnefndar svo að merki samsvara rekstrartilvikum.. Athugið að raunverulegum bókunarrökum hefur ekki verið breytt.</td>
<td>Það er auðveldara að stilla kerfið, þar sem ný merki tengjast rekstrartilvikum sem nota þessa bókunargerð.</td>
</tr>
<tr>
<td>Flytja Inn/út innkaupsverð, kostnað, eða söluverð úr Microsoft Excel í eða úr kostnaðarútgáfu.</td>
<td>Ekki er hægt að flytja verð eða kostnað á réttan hátt í kostnaðarútgáfu, þar sem gagnalíkan krefst kennis InventDim.</td>
<td>Nýjum gagnaeiningar gerir kleift að innleiða innflutnings- og útflutningseiginleika. Þessi eiginleiki gerir kleift að notendur geti flutt inn-og út verð eða kostnað í kostnaðarútgáfu.
<ul>
<li>Flytja inn ítarlegan lista yfir innkaupaverð næsta árs sem fæst frá Innkaupadeildinni.</li>
<li>Senda kostnað og staðlað söluverð úr höfuðstöðvum í einn eða fleiri sölufyrirtæki í einni aðgerð.</li>
</ul></td>
<td>Það er hægt að spara fjármálastjórum heilmikinn tíma þegar þeir vinna með kerfið, sérstaklega þegar þær verður að viðhalda fyrirframákveðnum kostnaði fyrir næsta fjárhagsár.</td>
</tr>
<tr>
<td>Sækja stutt yfirlit yfir birgðastöðu og hvað meðal einingarkostnaður er fyrir kostnaðarhlut.</td>
<td>Notandinn verður að opna á lager skjámyndina og velja birgðavíddirnar sem endurspegla kostnaðarhlut. Þess vegna notanda verður að þekkja hvaða birgðavíddir voru merktar fyrir fjárhagslegar birgðir fyrir tiltekna vöru.</td>
<td>Ný <strong>Kostnaðarhlutur</strong> síða er kynnt. Að sjálfgefnu sýnir þessi síða alla kostnaðarhluti sem tengist vörunni. Síðan sýnir gildandi birgðamagn, gildi og meðaleiningarkostnaður á hvern kostnaðarhlut.</td>
<td>Það fjarlægir sumar flókna aðgerðir og gerir auðveldar fyrir að vera fjármálastjóri.</td>
</tr>
<tr>
<td>Ný <strong>Kostnaðarfærslur</strong> síðu á meðan á birgðastjórnun stendur.</td>
<td>Það getur verið flókið að framkvæma birgðastýringu á skráðum birgðafærslur og tengdar uppgjör, þar sem sömu færslur geta verið efnisleg eða fjárhagsleg.</td>
<td>Síðan <strong>Kostnaðarfærslur</strong> býður upp á nýtt leið til að skoða birgðafærslur.
<ul>
<li>Færslur eru sýndar í tímaröð.</li>
<li>Aðeins færslur sem mynda kostnað eru hafðar með.</li>
<li>Það er ekkert minnst á efnislegan eða fjárhagslegab kostnað.</li>
<li>Það er ekkert minnst á efnislegt eða fjárhagslegt magn.</li>
<li>Kostnaðurinn er bætt við stigvaxandi.</li>
</ul></td>
<td>Það getur sparað fjármálastjórum heilmikinn tíma þegar þeir verður að viðhalda birgðastjórnun á stigi færslunnar.</td>
</tr>
<tr>
<td>Notaðu nýja <strong>VÍV-yfirlit Framleiðslu</strong> svarglugga til að sjá samantekin yfirlit yfir uppsafnaðan kostnað fyrir tiltekna vöru.</td>
<td>Ekki tiltækt</td>
<td>VÍV yfirlit sýnir samantekna vív-staða fyrir ákveðna framleiðslupöntun, flokkað í viðeigandi kostnaðartegund. Línurit sem sýnir, í tímaröð, hvernig um rekstrarbókanir hafa haft áhrif á vív-stöðu.</td>
<td>Það er hægt að spara fjármálastjórum heilmikinn tíma þegar þeir þurfa að vita hvað gildandi vív-staða er fyrir ákveðna framleiðslupöntun, eða hversu mikið efni hefur verið notuð á pöntun.</td>
</tr>
<tr>
<td>Nota Skoða kostnaðarsamanburð aðgerðina sem hefur verið kynnt í framleiðslupöntunum. Aðgerðin gerir það auðveldara að bera saman kostnað sem tengdur er við framleiðslupöntun.</td>
<td>Notandinn getur aðeins borið saman áætlaðan kostnað og raunkostnað. Samanburðurinn er hægt að gera á lægsta stigi.</td>
<td>Eiginleikann kostnaðarsamanburður gerir fjármálastjórum kleift að bera saman eftirfarandi gögn:
<ul>
<li>Virkur kostnaður á móti Áætlaður kostnaður = Áætlunarfrávik</li>
<li>Áætlaður kostnaður miðað við raunkostnað = frávik framleiðslu</li>
<li>Áætlunarfrávik + Afurðarfrávik = Samtala fráviks</li>
</ul>
Þessi aðgerð virkar óháð aðferð kostnaðarútreiknings sem er úthlutað á framleiddri vöru. Að sjálfgefnu sýnir línurit kostnaðarsamanburð eftir kostnaðarflokksgerð. Línurit sem gerir notendum kleift að kafa í ítarlegri stig.</td>
<td>Gerir það fjármálastjórum eða framleiðslustjórum kleift að greina hvar frávik í framleiðslu koma úr og hvað veldur þeim.</td>
</tr>
</tbody>
</table>

## <a name="developer"></a>Forritari

| Hvað hægt er að gera? | Dynamics AX 2012 | Dynamics AX 7.0 | Hví er þetta mikilvægt? |
|------------------|------------------|-----------------|------------------------|
| Stofna vefbyggt lausnir í skýinu sem eru aðgengilegar á mörgum tæki. | Ekki tiltækt | Gildandi útgáfu af Dynamics AX er byggð á nýjum biðlara á vefnum og biðlararamma. | Hægt er að veita notendum þínum lausnir af næstu kynslóð. |
| Notaðu Microsoft Visual Studio til að þróa lausnir. | Microsoft MorphX er aðal þróunarumhverfið, en sum þróun á sér stað í Visual Studio. | Visual Studio er eina þróunarumhverfið. | Hún heldur í vel þekkt Dynamics AX 2012 hugtök og aðlagar þær áreynslulaust að Visual Studio ramma og viðmiðum. Það virkjar staðlaða samvirkni með öðrum .NET -tungumálum og verk. |
| Compile Common Intermediate Language (CIL) fyrir alla eiginleika. | X ++ er tekinn saman í p-kóða. | Hinn nýji X ++ þýðandi myndar CIL fyrir alla eiginleika. CIL er sama millitungumál sem er notað af öðrum .NET tungumálum. | CIL er hraðvirkara, getur á hagkvæman hátt vísað til klasar í stýrðum gagnvirkum tenglasöfnum (DLLs) og er hægt að keyra á stórum verkfæragrunni .NET veita. |
| Hafðu með skýrslur viðskiptagreindar (BI) og sjónræna birtingu í Microsoft Dynamics AX biðlaranum. | Ekki tiltækt | Stofna mjög frumlega og flæðandi sjónrænar myndbirtingar. | Slíkt veitir innsýn í betri ákvarðanatöku sem byggist á viðskiptagreind. |
| Samþætt við Microsoft Office. | Ekki tiltækt | Ný geta er m.a. Excel Data Connector forritið, **Vinnubókarhönnuður** síðan, Flytja út API og skjalastjórnun. | Hægt er að stofna framleiðnilausnir fyrir endanotendur þína. |
| Gera sjálfvirka byggingu, prófun og notkun. | Tiltækur að hluta til | Virkja grannfræði Developer með því að nota sýndarvél Developer og Build. Skilgreindu sjálfvirkt sýndarvél Vm til að uppgötva, byggja kerfiseiningar frá Visual Studio Online (VSO), og keyra prófanir. C\# og X ++ kerfisþýðingu og tilvísanir eru studd. | Það eykur framleiðni hönnuðu með því að draga úr kostnaði og vinnu fyrir prófun og villuleit. |
| Sérstillt með yfirlögum og viðbótum. | Viðbætur eru ekki tiltækar. | Þessi útgáfa af Dynamics AX er með nýtt sérstillingarkerfi. | Hægt er að sérstillt upprunakóði og lýsigögn líkanaeininga sem eru send af Microsoft eða þriðja aðili Microsoft samstarfsaðila. |
| Byggja nýja stýringar og viðmótseiningar með því að nota X ++ og nútímalega vefumgjörð. | Sérstillt stýringar treysta á ytri ramma eins og Microsoft ActiveX og Windows Presentation Foundation (WPF). | Það er auðveldara að byggja stýringar í þessari útgáfu. Hægt er að nota X ++ rammanum fyrir hegðun forrits og viðskiptarök, og HTML/JavaScript-byggð biðlara býður upp á nútímalegar sjónræna birtingu.. | Stýringar þínar má hanna til að líta út og hegða sér rétt eins Dynamics AX út-úr-kassanum (OOB) stýringar. |
| Meta og stilla afköst með því að nota ný tæki. | PerfSDK, Data Expansion Toolkit, Trace Parser WEb app, og PerfTimer eru ekki tiltæk. | PerfSDK, Data Expansion Toolkit, Trace Parser Web app, og PerfTimer eru ný. | Hugbúnaðarþróunarpakki (SDK) gerir það mögulegt að prófa og villuleita öll mikilvæg viðskiptaferli fyrir afköst prófunarkeyrslu fyrir einn notanda og, ef við á, fjölda notenda. Gagnaútvíkkun verkfærapakkinn gerir mögulegt að útvíkka öll afkastaprófanir sem þarf að hafa aðalgagna og færslugögn rétt útvíkkuð. Rakningarþáttari gerir kleift að villuleita afkastapróf fyrir einn notanda eða keyrslu fyrir fjölda notanda. PerfTimer gerir kleift að sjá hvort einhver fyrirspurn eða eitthvert tiltekið aðferðarkall veldur vandamálum með afköst. Þess vegna er þarf ekki að framkvæma rakningu og greina allt í smáatriðum. |
| Sýna uppfæranleg ásýnd með því að nota OData. | Ekki tiltækt | Gildandi útgáfu af Dynamics AX kynnir í almenna OData endastöð þjónustu sem gerir aðgang að Dynamics AX gögnum virkan á samhæfðan hátt á milli breiðu sviði biðlara. | Þitt lausnir getur átt samskipti við RESTful þjónustur, samnýta gögn á hátt þannig að þau má uppgötva, og virkja breiða samþættingu með því að nota HTTP stafla samskiptareglu. |
| Nýta business connector til að heimila viðskiptarök og til að styðja samþættingar umhverfi. | Business connector er hægt að hringja inn í X ++ kóða úr stýrðum kóða. Við mælum með því að þú notir business connector aðeins til að heimila viðskiptarök í C\#, ekki fyrir samþættingaraðstæður. | Business connector er ekki studd lengur. Hönnunarkröfur ákvarðast af því að X ++ er þýddur í stýrðan kóða. Þess vegna interop er auðveldari. Samþættingarsviðsmyndir eru uppfylltar með því að nota OData. | Ekki er hægt að nota business connector áfram. |
| Velja kvarða (það er, fjölda aukastafa) á raunverulegum gagnagrunnsvæði og auknum gagnagerðum (Edt). | Vigt 16 er sjálfgefinn kvarði og forritara geta ekki breytt honum. | EDT og svæði hafa nú kvarðaeiginleika sem má nota á einstök svæði og EDT. Sjálfgefið er stillt á 6, ekki 16. | Afköst með NCCI töflur (stuðningur í minni í SQL) er hraðvirkara eftir magnpantanir þegar minni kvarði er notaður. Breyta kvarða eftir því sem þú notar einstaka reiti. |

## <a name="financial-management"></a>Fjármálastjórnun

<table>
<thead>
<tr>
<th>Hvað hægt er að gera?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Hví er þetta mikilvægt?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Flytja lykilskipulag út í Microsoft Excel.</td>
<td>Ekki tiltækt</td>
<td>Nú er hægt að velja lykilskipulag og flytja út í Excel.</td>
<td>Margir viðskiptavinir hafa beðið um möguleika á að flytja út lykilskipulag í Excel til að sía auðveldar.</td>
</tr>
<tr>
<td>Skoða fjárhag og ítarlegt regluskipulag sem tengjast lykilskipulag á einni síðu.</td>
<td> Notandi verður að fara í margar skjámyndir til að sjá fjárhag og lykilskipulag sem eru notaðar.</td>
<td>Upplýsingakassar hefur verið bætt við síðuna lykilskipulag.</td>
<td>Það er auðveldara að fá aðgang að mikilvægum upplýsingum þegar lykilskipulagi er skilgreint og breytt.</td>
</tr>
<tr>
<td>Skoða fjárhag sem tengjast bókhaldslykli á einni síðu.</td>
<td>Notandi verður að fara í hverju fyrirtæki og opna skjámynd fjárhags til að sjá bókhaldslykill sem úthlutað er í fjárhag.</td>
<td>Upplýsingakassar hefur verið bætt við síðuna <strong>bókhaldslykill</strong>.</td>
<td> Það er auðveldara að fá aðgang að mikilvægum upplýsingum þegar bókhaldslykill er skilgreint og úthlutað.</td>
</tr>
<tr>
<td>Skoða lokun leiðréttingar lokunarskjals og lokunarfærslur í aðskildum dálkum í á <strong>prófjöfnuð</strong> listasíðu.</td>
<td>Notendur sjá báðar gerðir færslna í einn dálkur.</td>
<td>Önnur færibreyta hefur verið bætt við í <strong>prófjöfnuð</strong> listasíðu.</td>
<td>Það leyfir samþjappaðri greiningu gagna og er einnig nauðsynlegt fyrir lögbundnu skýrslugerð í sumum löndum/svæðum.</td>
</tr>
<tr>
<td>Nota nýja <strong>Altæka almenna færslubók</strong> síðu.</td>
<td>Ekki tiltækt</td>
<td>Ný <strong>Altæka almennrar færslubókar</strong> síðu til að færa inn almennar færslubækur. Réttindi fyrir þessa síðu er bætt við hlutverkið <strong>Bókari</strong>.</td>
<td>Gerir mögulegt fyrir samnýttan þjónustubókara að færa inn almennar færslubækur milli fyrirtækja án þess að þurfa að fara úr skjámyndinni eða skipta um fyrirtækissamhengi.</td>
</tr> 
<tr>
<td>Nota nýja <strong>upprunaskoðun bókhalds</strong> síðu.</td>
<td>Tiltæk úr Dynamics AX 2012 R3 CU10.</td>
<td>Nýja <strong>upprunaskoðun bókhalds</strong> síðu og aðgerðir til að fletta þangað úr <strong>prófjöfnuð</strong> listasíðu og <strong>Fylgiskjalsfærslur</strong> síðu.</td>
<td>Gerir mögulegt að skoða nákvæmustu upplýsingar um uppruna fyrir prófjöfnuð eða bókhaldsfærslu í fjárhag, eða fyrir sérstaka greiningu.</td>
</tr>
<tr>
<td>Bæta við viðbótar bókunarlögum.</td>
<td>Það að Bæta við viðbótar bókunarlögum krafðist mikillar þekkingar af forriturum.</td>
<td>Tíu bókunarlög eru nú í boði.</td>
<td>Flestir viðskiptavinir bæta við frekari bókunarlög.</td>
</tr>
<tr>
<td>Nota valkostinn Tengt fylgiskjal.</td>
<td>Ekki tiltækt</td>
<td>Tengt fylgiskjal valkosturinn er tiltækur fyrir notendur til að sjá fylgiskjalið í mótfyrirtæki við bókun færslna innan samstæðu. Úr tengdum fylgiskjölum geta notendur smellt á upplýsingar og farið fljótt yfir í fylgiskjal mótfyrirtækis.</td>
<td>Við Bókun færslna innan samstæðu, höfðu notendur engin sýnileika eða rakningu til fylgiskjalsins sem var bókuð í mótfyrirtækis.</td>
</tr>
<tr>
<td>Fjöldalokun fjárhagstímabils</td>
<td>Ekki tiltækt</td>
<td>Notendur geta uppfært aðgang að kerfiseiningu og breytt stöðu tímabils fyrir mörg fyrirtæki í einu.</td>
<td>Fyrir aðgerðina þurftu notendur að breyta hvaða fyrirtæki þeir voru skráð í, fara í skjámynd fjárhagsdagatals og uppfæra handvirkt stöðu aðgangs og tímabils fyrir kerfið.</td>
</tr>
<tr>
<td>Notaðu Oanda til að keyfa gengi.</td>
<td>Að setja upp gengisveitu til að flytja inn gengi úr Oanda krafðist mikillar þekkingar forritara.</td>
<td>Ef notendur hafa lykil fyrir Oanda geta þeir fært hann inn þegar þeir stilla gengisveituna.</td>
<td>Notendur geta notað kosti út-úr-kassanum virkni með því að láta Oanda keyra gengið sem er flutt inn samkvæmt áætlun.</td>
</tr>
<tr>
<td>Sía fjárhagsskýrslur (Management Reporter) á grundvelli vídda, eiginda, dagsetningar og sviðsmyndum.</td>
<td> Síun allar skýrslur úr Management Reporter er meðhöndluð með hönnun skýrslunnar. til dæmis, Ef notandi sem hefur réttindi til skoðunar vill skoða skýrslu fyrir aðra dagsetningu, verður skýrsluhönnuður að gera breytinguna.</td>
<td>Valkostum skýrslu hefur verið bætt við, þannig að hægt er að nota mismunandi síur þegar notandi er að skoða skýrslu. Ný skýrsla er þá mynduð byggð á þeim síum.</td>
<td>Neytendum fjárhagsskýrslna geta notað mismunandi síur fyrir víddir, dagsetningar, eiginleika og sviðsmyndir án þess að krefjast uppfærslur fyrir skýrsluhannanir.</td>
</tr>
<tr>
<td>Skoða fjárhagsskýrslur (Management Reporter) í Microsoft Dynamics AX biðlara.</td>
<td>Aðskilin vefbiðlari var notað til að skoða skýrslur úr Management Reporter.</td>
<td>Hægt er að nálgast alla fjárhagsskýrslur í Dynamics AX biðlara. Notandi velur skýrslu til að skoða og skýrslan er birt í biðlaranum.</td>
<td>Hægt er að skoða fjárhagsskýrslur núna án þess að þurfa að fá aðgang að mismunandi biðlara/forritsins.</td>
</tr>
<tr>
<td>Prenta fjárhagsskýrslur (Management Reporter) úr Microsoft Dynamics AX biðlara.</td>
<td>Prentun skýrslu myndi nota prentvalkosti vafrans til að prenta og prentar aðeins það sem notandinn getur séð á skjánum.</td>
<td>Notandinn getur valið upplýsingastig og uppsetningu síðu fyrir skýrslu með því að nota valkostinn Prenta í fjárhagsskýrslu í Dynamics AX biðlara.</td>
<td>Prantaðar skýrslur eru prentaðar á hátt sem notendur búast við frekar en að prenta af vefsíðu.</td>
</tr><tr>
<td>Greina fjárhagsleg gögn með því að nota "fylgjast Með fjárhagslega frammistöðu“ (Monitor financial performance) Power BI efni.</td>
<td>Ekki tiltækt</td>
<td>Á PowerBI.com, veljið <strong>Sækja Gögn</strong>, og því næst velja <strong>Dynamics AX – Fjárhagslega frammistöðu</strong> efnispakka. Færið inn Vefslóð fyrir Dynamics AX endastöðina til að sjá gögn birtast á yfirliti.</td>
<td>Með þremur eða fjórum smellir, getur fyrirtæki virkja Power BI yfirlit sem inniheldur mikilvægt fjárhagsgögn. Efni má sérstilla af fyrirtæki.</td>
</tr>
<tr>
<td>Rekja lokunarferli fjárhagstímabils.</td>
<td>Ekki tiltækt</td>
<td>Lokunarsniðmát og áætlanir er má stofna með því að nota lokunarskilgreiningu Fjárhagstímabils. Nota skal <strong>lokun fjárhagstímabils</strong> vinnusvæði til að rekja framvindu lokunaráætlanir í mörgum fyrirtækjum.</td>
<td>Þessi vinnusvæði gerir óþörf handvirk kerfum til að skilgreina, áætla og miðla upplýsingum um lokunarverkþáttum. Þess vegna er fjöldi daga til að loka fækkað.</td>
</tr>
<tr>
<td>Fylgjast með fjárhagsáætlun samanborið við raungildi, og stofna fjárhagsspár með því að nota <strong>fjárhagsáætlanir og spár</strong> vinnusvæði og viðbótar fyrirspurnarskjámyndir.</td>
<td>Ekki tiltækt</td>
<td> Hægt er að komast í vinnusvæði gegnum yfirlit Dynamics AX. Innifaldar eru nokkrir nýjir tenglar Í nýjar fyrirspurnarsíður: <strong>Rauntölur miðað við samantekt fjárhagsáætlunarinnar</strong>, <strong>samantektartalnagögn fyrir fjárhagsáætlunarstýringu</strong>, <strong>færslur fjárhagsáætlunarskrár</strong>, og <strong>fjárhagsáætlunargerðir</strong>.</td>
<td>Nýja fyrirspurnarsíður virkja auðveld aðgang að fjárhagsáætlunarupplýsingum. Vinnusvæðið sameinar öll viðhaldsverk fjárhagsáætlunar og vöktunar á einn stað sem er auðvelt fyrir fjárhagsáætlunarstjóra eða aðalbókara að nota.</td>
</tr>
<tr>
<td>Stofna útlit fyrir fjárhagsáætlun og spá.</td>
<td>Skjalið <strong>Fjárhagsáætlun</strong> er álitið vera listi yfir línur sem hafa gildisdagsetningar og upphæðir fyrir samsetningar fjárhagsvídda . Notandi verður að stofna og nota Excel sniðmát til að skoða gögn fjárhagsáætlunar í PivotTable.</td>
<td>Ótakmarkaðan fjölda af útlit er tiltækt fyrir fjárhagsáætlunargerðir og spár. Hægt er að sameina valinn fjárhagsvídd, dálka skilgreinda eftir notanda, og aðrar línueigindir (t.d. athugasemd, verk, og eign) í útlit. Notendur geta skipta um útlit fyrir skjal fjárhagsáætlunargerðar eftir hentugleika og breyta gögnum með því að nota einhverja af völdu útliti. Skilgreining fjárhagsáætlunargerðar er einfaldað með því að sleppa aðstæðuskorðum og nota útlit til að skilgreina hvaða gögn má skoða og breyta í hverju stigi skjals fjárhagsáætlunargerðar.</td>
<td>Hún veitir sveigjanleika til að stofna og breyta fjárhagsáætlunum með því að nota bæði Excel og Dynamics AX biðlara. Hægt er að mynda sniðmát fyrir Excel-vinnubækur með því að nota uppsetningu fjárhagsáætlunarútlits.</td>
</tr>
<tr>
<td>Prenta <strong>Reikningsfærslur Lánardrottna</strong> skýrslu með upplýsingum úr <strong>Ítarlegur gjalddagalisti</strong> skýrslu, sem felur í sér daga fram yfir gjalddaga.</td>
<td>Prenta þarf tvo mismunandi skýrslur : <strong>Ítarlegur gjalddagalisti</strong> og <strong>Reikningsfærslur Lánardrottna</strong>.</td>
<td>Upplýsingar um tvær skýrslur hefur verið sameinað í <strong>Reikningsfærslur Lánardrottna</strong> skýrslu. Skýrslan <strong>Ítarlegur gjalddagalisti</strong> var afskrifuð.</td>
<td>Þannig verður óþarfi að prenta tvær aðskildar en tengdar skýrslur.</td>
</tr>
<tr>
<td>Mynda lögbundnar skýrslur beint í pdf-snið.</td>
<td>Mynda þarf fyrst lögbundna skýrslu á einu sniði og flytja þau síðan út í pdf-snið.</td>
<td>Pdf-snið er sjálfgefið snið fyrir lögbundnar skýrslur.</td>
<td>Hún veitir sameinuðum upplifun á birtingu hvort sem er á tölvuskjá eða prentaða pappírsformi.</td>
</tr>
<tr>
<td>Keyrðu Vsk-jöfnunarferlið sem runuvinnslu.</td>
<td>Ekki tiltækt</td>
<td>Á <strong>VSK-uppgjörstímabil</strong> síðu er hægt að tilgreina að jöfnunarferlið ætti að keyra í runuhætti.</td>
<td>Fyrir tímabil sem er með margar skattafærslur getur jöfnunarferlið getur tekið langan tíma og það gæti verið betra að keyra ferlið í bakgrunni sem runuvinnslu.</td>
</tr>
</tbody>
</table>

## <a name="foundation"></a>Sjóður

<table>
<thead>
<tr>
<th>Hvað hægt er að gera?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Hví er þetta mikilvægt?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Fáðu aðgang að biðlara hvar og hvenær sem er.</td>
<td>AX 2012 biðlara biðlaraforrits veitir heildarsafn skjámyndum, en það er hægt að keyra aðeins í tölvum sem keyra Microsoft Windows og krefst uppsetningar. Útstöðvarþjónn er oft notað með biðlaraforrits til að virkja aðgang yfir víðsvæðisnet (WAN). Vefbiðlari Enterprise Portal veitir safn færri skjámynda.</td>
<td>Tveimur AX 2012 biðlurum hefur verið skipt út fyrir einn, vefbiðlari sem byggir á stöðlum sem veitir heildarsafn virkni biðlaraforritssins ásamt umfangi Enterprise Portal biðlara.</td>
<td>Það kemur í veg fyrir að þróunarvinna sé skipt á milli tveggja UI vettvanga. Með því að nota staðlaða vefþjónustu viðmót, það er óþarfi að vera með útstöðvarþjón..</td>
</tr>
<tr>
<td>Vertu framleiðinn með því að nota ný verkskráningu.</td>
<td>AX 2012 verkskráning krefst beins aðgangs að Þjóni Hugbúnaðarhluta (AOS) tölvu og aukinna réttinda og veitir ekki möguleika á að breyta neinu.</td>
<td>Hægt er að nota ný verkskráning beint úr vefbiðlara. Aðgangur að verkskráning ekki krefjast kerfisstjóraréttindi. Skráð skref er hægt að skoða í beinni á meðan verið er að skrá, ný breytingavalkostir hafa verið innleiddur, og verkskráning styður fleiri aðstæður auk fyrirliggjandi viðskiptaferlavinnslu (BPM) aðstæður.</td>
<td>Ný verkskráning veitir straumlínulagaða reynslu og drífur áfram nýjar getur í Dynamics AX. Sumar þessara geta eru tiltækar nú og fleiri mun fylgja í framtíðinni.</td>
</tr>
<tr>
<td>Hjálpa notendum að skilja betur þá vinnu sem bíður þeirra með vinnusvæðum.</td>
<td>Hlutverkamiðstöðvar veita yfirlit yfir upplýsingar sem tengjast starfshlutverki notanda í fyrirtækinu eða stofnuninni.</td>
<td>Vinnusvæði eru nýtt hugtak í Dynamics AX sem ætlað er að skipta út hlutverkamiðstöðvum sem aðal leið til að fletta í verk og tilteknar síður. Þær veita einnar síðu yfirlit yfir viðskiptastarfsemi og hjálpa notendum að skilja núverandi stöðu, vinnu sem bíður þeirra, og afköst vinnslunnar eða notandans. Vinnusvæði eru grófari að gerð en AX 2012 hlutverkamiðstöðvar, og notandi getur haft aðgang að mörgum vinnusvæði.</td>
<td>Vinnusvæða er ætlað að auka afköst notenda hennar. Forritara þurfa að stofna vinnusvæði fyrir hvern mikilvægan „verkþátt“ sem er studdur í afurðinni. Eldri hlutverkamiðstöð úr AX 2012 er yfirleitt skipt út af mörgum vinnusvæða í gildandi útgáfu af Dynamics AX.</td>
</tr>
<tr>
<td>Gera skjámyndir gagnvirkar fyrir skoðunargátt vafra eða stærð tækis.</td>
<td>Í AX 2012 var innihald skjámynda sett fram í fastri mynd með dálkum, og heildar hæð og breidd skjámyndar var aðallega ákvörðuð á grundvelli stjórntækja á skjámyndinni.</td>
<td>Með breytingu yfir á vefinn í síðustu Dynamics AX, eru víddir skjámyndar nú grundvallaðar á stærð skoðunargáttar í vafra eða stærð tækis. Stjórntæki og útlitsfæribreytur hefur verið breytt eða bætt við til að bregðast beur við breytingum á stærð skoðunargáttarinnar.</td>
<td>innihald Skjámyndar þarf að vera gagnvirkara til að nota bestu mögulegu hæð/breidd vafra eða tækis. að fá fram gagnvirkni getur krafist breytinga á því hvernig skjámynd er mótuð.</td>
</tr>
<tr>
<td>Notið mynstur fyrir bætta þróunarupplifun á skjámyndum.</td>
<td>Skjámyndasniðmát voru tiltæk sem byrjunarreitir fyrir þróun skjámynda í AX 2012 á grundvelli skjámyndarstíls. Skjámyndin athugun á stíl, sem er valfrjáls viðbót, veitti upplýsingar um hvernig skjámynd var frábrugðin tilsvarandi sniðmáti.</td>
<td>Í núverandi útgáfu Dynamics AX hafa verið kynntar til leiks mynstur skjámyndar. Mynstur Skjámyndar standa fyrir samsetningu skjámyndasniðmáta og athugun á stíl skjámyndar sem eru kyrfilega samþætt við þróunarupplifun. Mynstur hafa verið skilgreindar á stigi skjámyndar (eins og AX 2012) með viðbótar undirmynstrum sem eru núna tiltæk á stigi hóps og flipasíðu.</td>
<td>Skjámyndir sem halda sig við mynstur hafa marga kosti þar á meðal samræmt notendaviðmótinu, einfaldari þróunarupplifun, einfaldari uppfærsluslóð skjámyndar, og aukið öryggi í gagnvirkni útlits skjámyndar.</td>
</tr>
</tbody>
</table>

## <a name="help"></a>Hjálp

<table>
<thead>
<tr>
<th>Hvað hægt er að gera?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Hví er þetta mikilvægt?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Fáðu Aðgang að leiðsögn fyrir ferli (verkefnaleiðbeiningar) og hugtökum með því að smella á <strong>Hjálp</strong>.</td>
<td>AX 2012 hjálparkerfi vísar til í HTML efnis sem vistaðar eru á staðbundna vefþjóninn. Viðskiptavinur og söluaðilar getur búið til þeirra eigin Hjálp.</td>
<td>Hjálparkerfi í gildandi útgáfu af Dynamics AX birtir verkefnaleiðbeiningar sem eru geymdar í Microsoft Dynamics Lifecycle Services (LCS) BPM. Hjálparkerfið birtir einnig efni frá Microsoft skráarsíðunni. Fyrir frekari upplýsingar sjá <a href="help-overview.md" data-raw-source="[Help system](help-overview.md)">Hjálparkerfi</a> og <a href="new-task-guides-available-february-2016.md" data-raw-source="[New task guides (February 2016)](new-task-guides-available-february-2016.md)">Nýjar leiðbeiningar (febrúar 2016)</a>.</td>
<td>Verkefnaleiðbeiningar gefa leiðsögn, gagnvirka reynslu sem fer með þig í gegnum þrep í verki eða viðskiptaferli. Hægt er að sækja og sérsníða verkefnaleiðbeiningar sem Microsoft veitir. Þetta efnisatriði veitir hraðari og sveigjanlegri leið til að stofna, afhenda og uppfæra fylgiskjal afurðar. Því hjálpar það að tryggja að þú hafir aðgang að nýjustu tækniupplýsingunum.</td>
</tr>
</tbody>
</table>

## <a name="human-capital-management"></a>Mannauðsstjórnun

<table>
<thead>
<tr>
<th>Hvað hægt er að gera?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Hví er þetta mikilvægt?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Flytja hæfni og skírteini á þátttakendur í kennslu að námskeiði ljúki.</td>
<td>Þetta er handvirk ferli.</td>
<td>Þegar námskeiði er lokið verður nýr valkost tiltækur til að uppfæra færslur þátttakanda með nýrri hæfni og nýjum skírteinum.</td>
<td>Hún veitir nýja og skilvirka leið til að uppfæra starfsmannafærslur.</td>
</tr>
<tr>
<td>Staðfesta ráðningu á skjótan hátt.</td>
<td>Þetta er handvirk ferli.</td>
<td>Þitt MA-deild getur á fljótlegan hátt staðfesta ráðningu með því að nota síðu vinnusvæðis eða starfsmanna.</td>
<td>Mannauðsdeild hefur ekki lengur aðgang að mörgum síðum til að staðfesta gögn upphafsdagsetningar, stjórnanda, mánuðir í stöðu og laun.</td>
</tr>
<tr>
<td>Leyfa starfsmenn skoða, uppfæra og eyða upplýsingar í kerfinu.</td>
<td>Tiltækt, en með takmarkaða skoðunar- og uppfærslueiginleika</td>
<td>Eiginleikinn er gerður virkur og gerir kleift að starfsmenn og verktaka skoða margvíslegan persónulegum upplýsingum. Einnig er hægt að nota verkflæði þegar upplýsingum er stofnuð, uppfærðar eða eytt.</td>
<td>Það leyfir starfsmönnum að taka stjórn á þeirra upplýsingar, hvort sem það felur í sér uppfærslu á aðsetur eða tengiliðaupplýsingar, sækja um starf, svara spurningalista eða uppfæra mynd þeirra. Þegar verkflæði er virkt geta upplýsingar verið endurskoða með samþykkjandi eða sjálfkrafa samþykkt, samkvæmt þínum viðskiptaferlum.</td>
</tr>
<tr>
<td>Leyfa stjórnendum að skoða eða Breyta starfsmannaupplýsingum.</td>
<td>Tiltækt, en með takmarkaða skoðunar- og uppfærslueiginleika</td>
<td>Allt eftir skilgreiningarstillingar og öryggi , geta stjórnendur skoða eða breyta starfsmannaupplýsingum.</td>
<td>Það leyfir stjórnendum að fá aðgang að mikilvægum starfsmannaupplýsingum, svo þeir geti tekið betri ákvarðanir um tilfangaplön, afkoma og þróun starfsmanna.</td>
</tr>
<tr>
<td>Nýta sjálfsafgreiðslu stjórnanda virkni.</td>
<td>Ekki tiltækt</td>
<td>Stjórnendur geta nú senda beiðnir fyrir nýráðningar (starfsmenn og verktaka), flutningum og starfslok (ljúka ráðningu). Stjórnendur geta einnig beðið um nýja stöðu, lengja tímalengd stöðu, eða biðja um breytingar á stöðu.</td>
<td>Þessar aðstæður voru áður aðeins sýndar í Mannauði. Virkjun þessara aðstæður veitir öflug verkfæri fyrir stjórnendur innan fyrirtækisins. Hægt er að virkja valfrjáls verkflæði til að veita rétt stig yfirferðar og samþykkis.</td>
</tr>
<tr>
<td>Opna niðurstöður launavinnsla.</td>
<td>Niðurstöður eru aðeins tiltækar við vinnslu.</td>
<td>Nú er hægt að nálgast niðurstöður úrvinnslu launa hvenær eftir að búið er að keyra ferlið.</td>
<td>Hún veitir framúrskarandi endurskoðun ferlisins og niðurstöðu ferlisins. Það veitir einnig ítarlegt yfirlit yfir gögn áður en starfsmannafærslur eru uppfærðar.</td>
</tr>
<tr>
<td>Opna niðurstöður fríðindavinnsla.</td>
<td>Niðurstöður eru aðeins tiltækar við vinnslu.</td>
<td>Nú er hægt að nálgast niðurstöður úrvinnslu fríðinda hvenær eftir að búið er að keyra ferlið.</td>
<td>Hún veitir ítarlegt yfirlit yfir gögn sem er uppfærð með fríðindaúthlutun og breytingar á kostnaði.</td>
</tr>
<tr>
<td>Skoða breytingar á tímaás „Gildisdagsetningar".</td>
<td>Ekki tiltækt</td>
<td>Þessi samanburðarverkfæri er tiltæk fyrir starfsmenn, stöður, og verk. Hún veitir ítarlegt yfirlit yfir breytingar úr einni útgáfu færslu til annarrar.</td>
<td>Það sparar þér tíma þegar þú skoðar breytingar sem eiga sér stað yfir tíma á starfsmenn, staða, og færslur verka. Það leyfir þér að bera saman tvær útgáfur færslu eða allar færslur yfir ákveðið tímabil.</td>
</tr>
<tr>
<td>Skoða starfsmenn eftir fyrirtæki.</td>
<td>Þetta er handvirk ferli sem er framkvæmd í gegnum síun.</td>
<td>Listar starfsmanna og verktaka eru sjálfkrafa síaðir af fyrirtækinu sem þú ert skráður inn í.</td>
<td>Hún veitir síað yfirlit yfir starfsmenn sem eru ráðnir í fyrirtækinu sem maður er innskráður í. Fyrir ósíað yfirlit yfir alla starfsmenn og verktaka, þá er starfsmannalistinn enn tiltækur. Í þessari útgáfu Dynamics AX, breytir kerfið ekki fyrirtæki á grunni starfsmannsins sem er valin í listanum.</td>
</tr>
<tr>
<td>Uppfæra námskeiðsþátttakandalistann.</td>
<td>Ekki tiltækt</td>
<td>Þátttakendur í námskeiði er hægt að fjarlægja af þátttakandalistanum.</td>
<td>Hún veitir auðvelda leið til að uppfæra þátttakendur námskeiðs sem eru skráðir fyrir mistök.</td>
</tr>
<tr>
<td>Stjórna launatilvikum í flokki.</td>
<td>Ekki tiltækt</td>
<td>Þessi eiginleiki straumlínulagar ferli launabreytingar fyrir starfsmenn.</td>
<td>Hún veitir einfalt, straumlínulagað ferli fyrir uppfærslu starfsmannafærslur með vinnusvæði launa og tengdar síður.</td>
</tr>
</tbody>
</table>

## <a name="inventory-management"></a>Birgðastjórnun

Engum nýjum eiginleikum hefur verið bætt við.

## <a name="localization"></a>Þýðing

<table>
<thead>
<tr>
<th>Hvað hægt er að gera?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Hví er þetta mikilvægt?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Skilgreina og mynda rafræn skjöl til að uppfylla lögboðnar kröfur í ýmsum löndum/svæðum.</td>
<td>Rafræn skjöl eru harðkóðuð í X ++ eða sem Extensible Stylesheet Language Transformations (Xslt). Allar leiðréttingar sniðs krefjast þróunarvinna . Aðgang að gögnum og snið eru ekki einangrað. Uppsetning Leiðrétts sniðs krefst nýrri Microsoft Dynamics AX bráðabótarpakka sem hnekkir fyrirliggjandi sniði. Sérstillt breytingar á hverju sniði verður að tengja handvirkt við upprunakóða nýrrar Microsoft Dynamics AX bráðabótarpakka.</td>
<td>Rafrænnar Skýrslugerðar (ER) er ný verkfæri fyrir skilgreiningu og myndun rafræn skjöl sem beinast að viðskiptanotanda frekar en forritara. Rafræn skýrslugerð gerir kleift að setja upp gagnalíkan sem tengjast ákveðnum lénum og eru óháð Microsoft Dynamics AX gagnagrunninum sem gagnaveitur fyrir skjalasnið. Viðskiptanotandagetur skilgreina þessi snið byggt á þessum gagnalíkönum tengdum ákveðnum lénum (til dæmis, fyrir greiðslur, intrastat-skýrslur eða skattaskýrslur). Notandi skilgreinir sniðin með því að nota einfaldar sjónræn verkfæri sem eru svipaðar Excel. ER (rafræn skýrslugerð) styður núna myndun rafrænna skjala í texta, XML, og skrársniðmátin Excel. Þessi skjöl má mynda samtímis og pakka í zip-skrár. Gagnalíkön og snið styðja útgáfuupplýsingar. Útgáfur sniðs getur haft gildistímabil. Hvert gagnalíkan eða sniðsútgáfu er geymt í sér skilgreiningu og þeim dreift til viðskiptaaðilum og viðskiptavinum í gegnum LCS. Viðskiptaaðilar og viðskiptavinir geta sérsníða gagnalíkön og snið Microsoft, og stofna sína eigin. ER vistar skilgreiningarbreytingar samstarfsaðila og viðskiptavina sem delta í Microsoft skilgreiningar, sem einfaldar uppfærslur í nýjar útgáfur af Microsoft skilgreiningar. Með því að nota LCS geta samstarfsaðila einnig samnýtt þeirra gagnalíkan og sniðskilgreiningar með öðrum samstarfsaðila og viðskiptavina, sem geta sérsníða og deila þeim. Delta sérsnið og auðveld uppfærslu er studd gegnum allt sérsniðskeðjuna.</td>
<td>ER einfaldar stofnun, viðhald og uppfærslu rafræna skjalasnið til að uppfylla lögboðnar kröfur í ýmsum löndum/svæðum. ER gerir ferli að stofna eða breyta rafræna skjalasnið hraðar og auðveldari. Þessar breytingar geta viðskiptanotendur gert í stað forritara. ER gerir hraðar og auðvelda viðskiptaaðilum og viðskiptavinum að uppfæra þeirra sniðsforstillingar í nýjar útgáfur af sniðin sem eru gefnar út af Microsoft eða öðrum viðskiptaaðilum. ER veitir eina almenna leið (gegnum LCS) fyrir Microsoft og samstarfsaðila til að dreifa skilgreiningar rafræna skjals á aðra samstarfsaðila og viðskiptavina. ER auðveldar einnig samstarfsaðilum og viðskiptavinum að sérsníða, uppfærslu og dreifa rafrænt skjal-snið fyrir kröfur tiltekins fyrirtækis síns.</td>
</tr>
<tr>
<td>(MEX) Mynda reglubundnar skýrslur virðisaukaskatts (VSK) í mexíkó</td>
<td>Þú Verður að mynda <strong>Sölu og Innkaups VSK</strong> skýrslur með því að nota óinnleystu vsk-aðgerðina, þannig að notendur geta auðkenna færslur sem tilheyra innleystan og óinnleystan hluta sem byggja á stöðu.</td>
<td><strong>Sölu og Innkaupa VSK</strong> skýrslur var breytt og taka nú til greina eiginleika skilyrts skatts aðeins með því að nota tiltekinn vsk-tímabil fyrir óinnleystan og innleystan vsk-kóða.</td>
<td>Breytingar á skilgreiningu á vsk-kóða er krafist áður en notendur geta búið til þessar skýrslur rétt. Eiginleiki skilyrts söluskatts er áskilin, og notandinn þarf að skilgreina sérstaka jöfnunartímabil, óinnleystan og innleystan, til að auðkenna færslur í svæðum tengdra hluta.</td>
</tr>
<tr>
<td>(JPN) Stjórna japönsku yfirlýsingarskjali hraðaðrar afskriftar eigna.</td>
<td>Ekki tiltækt</td>
<td>Mikilvægar upplýsingar yfirlýsinga er geymt miðlægt í einu skjali fyrir betri viðhald.</td>
<td>Samræmi skjala og auðveld umsjón hjálpa til við að fækka vandamálum á meðan á endurskoðun stendur og öðrum athugunum.</td>
</tr>
<tr>
<td>(JPN) Staðfesta JBA stafir á bankareikning.</td>
<td>Ekki tiltækt</td>
<td>Hægt er að staðfesta kana nafnareitir inniheldur aðeins stafi sem eru leyfð af JBA bankasniði.</td>
<td>Það hjálpar að draga úr truflunum hjá notendum á meðan verið er að stofna greiðsluskrá vegna ógildra stafa.</td>
</tr>
<tr>
<td>(JPN) Vinndu upp japönskum auramismun eigna í lok fjárhagsársins.</td>
<td>Ekki tiltækt</td>
<td>Á við <strong>eignafæribreytur</strong> síðu er hægt að velja að vinna upp í lok fjárhagstímabilsins eða í lok fjárhagsárs.</td>
<td>Hún veitir sveigjanleika til að passa við staðbundnar venjur.</td>
</tr>
<tr>
<td>(JPN) Mynda Japönsk viðhengdar töflur 16. seríu fyrir skattskýrslu fyrirtækja á samantekin upphæð með aðalgerð eignar.</td>
<td>Ekki tiltækt</td>
<td>Í virðislíkönum eigna er hægt að velja að gera samantekt eftir aðalgerð. Sjálfgefið er að þessi virkni er notað fyrir nýstofnaðar eigna.</td>
<td>Fyrir stórum stofnunum sem hafa þúsundum eigna, samantekt skýrslur minnka mjög stærð skýrslu sem er mynduð.</td>
</tr>
<tr>
<td>(JPN) Byrja að úthluta sérstaka fráteknum afskriftum frá næsta fjárhagsár fyrir eignir í Japan.</td>
<td>Ekki tiltækt</td>
<td>Í virðislíkönum eigna sem hefur viðeigandi óregluleg afskriftarregla, er hægt að velja að hefja úthlutun frá næsta fjárhagstímabils eða næsta fjárhagsár.</td>
<td>Hún veitir sveigjanleika til að passa við staðbundnar venjur.</td>
</tr>
<tr>
<td>(JPN) Mynda neysluskattskýrslu Japans sem inniheldur endurskoðuð skatthlutfall.</td>
<td>Neysluskattsskýrsla er tiltækt fyrir skatthlutfall upp á 5 prósent.</td>
<td>Neysluskattskýrsla inniheldur hluta fyrir endurskoðuð skatthlutfall (t.d. 8 prósent).</td>
<td>Útlitið var nýlega tilkynnt af stjórnvöldum.</td>
</tr>
<tr>
<td>(ESB) Skilgreina sléttunarstillingar fyrir esb-sölulista.</td>
<td>Sléttunarstillingar fyrir skýrslugerð esb-sölulista fyrir ýmis lönd/svæði eru harðkóðaða í X ++ eða Extensible Stylesheet Language Transformations (Xslt).</td>
<td>Sléttunarstillingar er bætt við færibreytur Erlendra viðskipta. Hægt er að skilgreina sléttunar nákvæmni, sléttunaraðferð, nákvæmni úttaks og hegðun fyrir upphæðir minni en sléttunar nákvæmni.</td>
<td>Þetta sameinar og einfaldar skilgreiningu á skýrslugerð esb-sölulista. Leiðrétting á sléttunarstillingar krefst ekki lengur þróunarvinnu.</td>
</tr>
<tr>
<td>(ESB) Skilgreina reglur um hæfi bakfærðra gjalda.</td>
<td>Reglum um hæfi bakfært gjald eru harðkóðaða fyrir aðstæðum fyrir bakfærðra gjalda innanlands . Hægt er að setja upp þröskuld fyrir hæfi fyrir hvern vöruflokk. Aðgerðin er aðeins í boði fyrir Stóra-Bretland.</td>
<td>Hægt er að skilgreina reglum um hæfi bakfært gjald eftir gerð skjals (innkaupapöntun/sölupöntun, reikning lánardrottins, reikningur með frjálsum texta, o. s. frv.) og flokkur bakfærðra gjalda sem sameinar vörur, vöruflokka og innkaupa-/sölutegundir. Reglur um hæfi eru gildar eftir dagsetningum. Einnig er hægt að merkja einstaka vsk-kóðar i vsk-flokka sem gilda fyrir bakfærð gjöld. Skýrslan sölureikningur er leiðrétt til að tákna upplýsingar um notuð bakfærð gjöld. Virkni er tiltæk fyrir öll Evrópska lönd/svæði.</td>
<td>Þessi breyting sameinar skilgreiningu á hæfireglum um bakfærð gjöld og styður innleiðingu á reglugerðum Evrópska lönd/svæði um bakfærð gjöld innanlands.</td>
</tr>
<tr>
<td>(DE) Búa til Þýsk endurskoðunarskrá - GDPdUGoBD</td>
<td>Notendur geta sett upp skilgreiningu á töflur sem innihalda fjárhagsleg gögn til að flytja út sniði samþykktu af Þýskum endurskoðendur og yfirvalda.</td>
<td>Aðgerðin hefur verið útfærð sem skilgreining fyrir rafræna skýrslugerð . Virknin er tiltæk fyrir þýskaland og Austurríki.</td>
<td>Þessi breyting veitir notanda möguleika á mun meiri möguleika á að sníða til gögn, breyta, og veitir einnig öllum fríðindum úr líftímastjórnun skilgreininga fyrir rafræna skýrslugerð, eins og að skipta auðveldlega út skilgreiningum, útgáfum, o.s.frv.</td>
</tr>
<tr>
<td>(FR) Stöðulisti með skýrslu fyrir flokkssamtölulyklum.</td>
<td>Stöðulisti með skýrslu fyrir flokkssamtölulyklum er innleitt sem ssrs-skýrsla (LedgerAccountSum_FR).</td>
<td>Stöðulisti með skýrslu fyrir flokkssamtölulyklum er innleitt sem Management Reporter-skýrsla sem er tiltæk möppunni Staðfærðar fjárhagsskýrslur LCS eignasafns.</td>
<td>Þetta gerir notendum kleift að fá allar fríðindi og frelsi í sérsníðingu með því að nota fjárhagsskýrslur í Management Reporter.</td>
</tr>
<tr>
<td>(ESB) greiðslutilkynning, þáttökuathugasemd og eftirlitsskýrslur fyrir greiðslur.</td>
<td>Allar Þessar skýrslur eru innleiddar og SSRS-skýrslur.</td>
<td>Þessar skýrslur hafa verið innleiddar sem Opna XML-sniðmát sem nota á í Microsoft Excel.</td>
<td>Skilgreiningar fyrir Rafræn greiðsla innihalda uppsetningu greiðsluskrársniðs og sniðmát. Þetta gerir notendum kleift að fá allar fríðindi og frelsi í sérsníðingu skýrslna með því að rafræna skýrslugerð.</td>
</tr>
<tr>
<td>(ESB) Skilgreina sléttunarstillingar fyrir Intrastat.</td>
<td>Sléttunarstillingar fyrir skýrslugerð Instrastat eru harðkóðaða í X ++ eða Extensible Stylesheet Language Transformations (Xslt).</td>
<td>Sléttunarstillingar er bætt við færibreytur Erlendra viðskipta. Hægt er að skilgreina sléttunar nákvæmni, sléttunaraðferð, nákvæmni úttaks og hegðun fyrir upphæðir minni en sléttunar nákvæmni.</td>
<td>Þetta sameinar og einfaldar skilgreiningu á skýrslugerð Instrastat. Leiðrétting á sléttunarstillingar krefst ekki lengur þróunarvinnu.</td>
</tr>
<tr>
<td>(ESB) Setja upp intrastat-vörukóðum á í tegundastigveldum.</td>
n<td>Intrastat-vörukóðum er aðgreindur listi. Meðan tegundastigveldi af gerðinni vörukóði er til staðar, gætu þessir vörukóðar verið sjálfgefnir í Retail HQent og sölutegundir.</td>
<td>Aðgreindur listi yfir intrastat-vörukóða er sameinaður við afurðastigveldi af gerðinni vörukóði.</td>
<td>Þetta sameinar nálgun til að úthluta vörukóðum á útgefnar afurðir og tegundir í sölu- og innkaupaskjölum.</td>
</tr>
<tr>
<td>(ESB) Gefa skýrslu um magn fyrir viðbótareiningar fyrir Intrastat með því að nota stillingu fyrir umreikning eininga.</td>
<td>Intrastat-vörukóða hefur textasvæði til að auðkenna viðbótareiningar, og korti fyrir <strong>Afurð</strong> hefur svæði til að auðkenna magn viðbótareininga í kílóum.</td>
<td>Viðbótareiningar fyrir intrastat-vörukóða er valið úr lista yfir Einingar. Magn viðbótareininga er reiknað í gegnum stillingar fyrir umreikningur eininga.</td>
<td>Þetta sameinar nálgunin fyrir umreikning úr færslueiningum í viðbótareiningar.</td>
</tr>
<tr>
<td>(RSB) Úthluta sjálfgefna flutningsaðferð í afhendingarmáta.</td>
<td>Ekki tiltækt</td>
<td>Reitur fyrir sjálfgefna flutningsaðferð er bætt við afhendingarmátann.</td>
<td>Þetta einfaldar undirbúning intrastat-skýrslugerðar.</td>
</tr>
<tr>
<td>(ESB) Merkja útgefin afurð til að vera ekki sett í skýrslu í Instrastat.</td>
<td>Ekki tiltækt</td>
<td>Valkostur til að útiloka vöru frá intrastat-skýrslugerð er bætt við útgefin afurð.</td>
<td>Þetta einfaldar undirbúning intrastat-skýrslugerðar.</td>
</tr>
</tbody>
</table>

## <a name="manufacturing"></a>Framleiðsla

| Hvað hægt er að gera? | Dynamics AX 2012 |
|------------------|------------------|
| Framkvæma athugun á efnisframboð fyrir framleiðslupantanir á sérstakri síðu sem er opnuð í **Stjórnun á framleiðslugólfi** vinnusvæði. | Ekki tiltækt |
| Byrjaðu og skrifaðu skýrslu um framleiðsluverk með því að nota nýju síðuna **Verkspjaldstæki**. | **Starfsskráning** skjámynd er aðallega ætlað fyrir stóra skjái á afgreiðslustöðvar og Notendaviðmóti eru yfirleitt opnuð með músarsmellum. |

## <a name="master-planning-and-forecasting"></a>Aðaláætlanagerð og spár

| Hvað hægt er að gera? | Dynamics AX 2012 | Dynamics AX 7.0 | Hví er þetta mikilvægt? |
|------------------|------------------|-----------------|------------------------|
| vara notandann við ef sölupöntun eða framleiðslupöntun er ekki tilbúin til afhendingar fyrir áætlaða dagsetningu. | Viðvaranir sem eru stofnaðar af aðaláætlanagerð kallast *framvirk skilaboð*. *Framvirkur* er samningur milli tveggja aðila um að kaupa eða selja eign fyrir verð sem er umsamin í dag (í *framvirk verð*), jafnvel þótt afhendingu og greiðslan eiga sér stað á síðari tímapunkti (í *afhendingardagsetning*). | *Framvirk skilaboð* og *framvirkar dagsetningar* hafa verið endurnefndar *reiknaðar seinkanir* og *frestaðar dagsetningar*, í þessari röð. | Orðalisti sem er notað í AX 2012 var ónákvæmur og leiddi til rangra þýðinga. |
| Fá skjóta innsýn í stöðu á keyrslu aðaláætlanagerðar, áríðandi áætlaðar pantanir og áætlaðar pantanir sem valda seinkunum. | Upplýsingar eru tiltækar, en hún er dreifð í margar skjámyndir. | **Aðaláætlanagerð** vinnusvæðið býður upp á upplýsingar í fljótu bragði um það hvenær síðasta áætlanagerðarlotu lauk, hvort einhverjar villur komu upp, hverjar áríðandi áætlaðar pantanir eru, og hvaða áætlaðar pantanir valda seinkunum. | Þú færð ávinning af yfirlitinu sem vinnusvæðið veitir. Viðeigandi upplýsingar eru tekin saman í til handleiðslu við aðaláætlanagerð og auka framleiðni. |
| Notið Excel til að uppfæra eftirspurnarspár. | Ekki tiltækt | Þú getur nýta heilsteypta samþættingu við Excel þegar er fært inn eftirspurnarspár , uppfærir og eyðir eftirspurnarspár. | Það hjálpar til við að auka skilvirkni og afköst. |
| Meta má framtíðareftirspurn og stofna eftirspurnarspá á grundvelli færslugagna. | Í Microsoft Dynamics AX 2012 R3, eru spálíkön í Microsoft SQL Server Analysis Service notuð til að stofna spár fyrir eftirspurnarspár. | Áætla síðari eftirspurn með afli og miklu umfangi þjónustu Microsoft Azure Machine Learning skýinu. Það er auðvelt að nota og framlengja spálíkön í Machine Learning til að uppfylla kröfur viðskiptavinar. Þjónustan framkvæmir besta val á líkönum og býður upp á afkastavísar (KPI) sem hægt er að nota til að reikna út nákvæmni spár. | Mynda nákvæmari spá með Machine Learning tækni. |
| Fínstilla pöntunardagsetningu og magn, byggt á sjónrænu yfirlit yfir tengdar aðgerðir úr keyrslu aðaláætlanagerðar. | Yfirlit yfir aðgerðalínurit býðst en sýnir allar tengdar aðgerðir. Þegar aðgerðir eru notaðar hverfa þær strax úr yfirliti. | Aðgerðalínurit veitir betra yfirlit. Það felur í sér valkostunum sem leyfir þér að sýna aðeins aðgerðir og beint tengdar aðgerðir. Þegar aðgerðir eru notaðar birtast þær í deyfðu en eru enn sýndar. Þess vegna er yfirlit varðveitt. Frekari upplýsingar er bætt við the aðgerðalínurit til að sýna gögn á einni síða. | Þú hagnast á bættri framleiðni, þar sem áhersla er aðeins á viðeigandi aðgerðir. |

## <a name="procurement-and-sourcing"></a>Innkaup og aðföng

| Hvað hægt er að gera? | Dynamics AX 2012 | Dynamics AX 7.0 | Hví er þetta mikilvægt? |
|------------------|------------------|-----------------|------------------------|
| Nota skal **undirbúningi innkaupapöntunar** vinnusvæði til að fá skjótt innlit í stöðu innkaupapantanir sem er verið að undirbúa. | Ekki stutt | Vinnusvæðið **Undirbúningur innkaupapöntunar** veitir yfirlit yfir pantanir frá þeim tíma þegar þær eru stofnaðar sem drög og eru raktar, gegnum stöðu verkflæðissamþykkis og áfram til staðfestingar. | Innkaupadeild fyrirtækisins þarf ekki lengur að leita að upplýsingum úr margar síður en hagnast nú á yfirlit sem vinnusvæðið veitir . |
| Nota skal **móttöku og eftirfylgni innkaupapöntunar** vinnusvæði til að fá skjótt innlit í innkaupapöntunum sem bíða móttöku, til að aðstoða við eftirfylgni. | Ekki stutt | **Móttöku og eftirfylgni innkaupapöntunar** vinnusvæði veitir yfirlit yfir staðfestar innkaupapantanir sem bíða sendingar eða innhreyfingar. Vinnusvæðið inniheldur lista yfir innhreyfingar sem komnar eru framyfir á tíma og innhreyfingar í bið til að aðstoða við fyrirbyggjandi yfirferð og eftirfylgni af birgi. Vinnusvæðið er einnig með lista yfir innkaupapantanir sem komuskráningu hefur verið gerð fyrir í vöruhúsi, til að aðstoða við að tryggja að móttöku er bókuð. Innkaupapöntun sem hefur ekki enn verið sendar eru einnig tiltækar til skoðunar. | Innkaupadeild hagnast af yfirlit sem vinnusvæðið veitir. Viðeigandi upplýsingar eru tekin saman í til handleiðslu við eftirfylgni og auka framleiðni. |
| Senda Innkaupapantanir fyrir staðfestingu á gátt lánardrottins sem er hýst í Dynamics AX-biðlaranum. Láta lánardrottins staðfesta eða hafna. | Ekki stutt | Viðmót gáttar lánardrottins heimilar lánardrottna að fá innkaupapantanir til að staðfesta eða hafna. Þetta leyfir einnig lánardrottins til að sjá yfirlit yfir allar staðfestar innkaupapantanir fyrir lykil. Innkaupaaðili getur sent innkaupapöntun sem krefst staðfestingar hjá lánardrottins. Lánardrottinn þarf að vera skráður Microsoft Azure Active Directory (Azure AD) notandi í Dynamics AX, vera tengiliður lánardrottins og hafa sérstakan öryggishlutverk. | Innkaupadeild fyrirtækisins hagnast á því að draga úr pappírsnotkun og handvirkt fylgjast með svör á innkaupapöntunum, þar sem flæði beint inn í kerfið. Að vera með einn uppruna sannleikans dregur úr misskilningi milli viðskiptavinar og lánardrottins. |

## <a name="projects"></a>Verk

| Hvað hægt er að gera? | Dynamics AX 2012 | Dynamics AX 7.0 | Hví er þetta mikilvægt? |
|------------------|------------------|-----------------|------------------------|
| Bóka starfsmenn sem tilföngum á verk. | Svipað tilföngum, eru starfsmenn bókaðir beint á verk til viðbótar við tilföng. | Nú er hægt að nota vinnustöðvartaflan þar sem tilfanga fyrir framleiðslu eru geymdar má nú nota til að bóka starfsmenn sem tilföngum á verk. | Þegar þú bókar verk þarf aðeins að bóka tilföng. |

## <a name="retail-sales-marketing-and-customer-service"></a>Smásala, markaðssetning, og þjónustudeild

### <a name="retail-hq"></a>Retail HQ (Höfuðstöðvar smásölu)

Microsoft Azure-hýst HQ Retail býður upp á miðstýrðar stjórnun á og heildstæða sýn inn í öllum þáttum smásöluaðgerða gegnum vefbiðlara.

<table>
<thead>
<tr>
<th>Hvað hægt er að gera?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Hví er þetta mikilvægt?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Framkvæmið markaðsaðgerðir.</td>
<td>Notendur þurfa að opna margar skjámyndir til að stýra þessum gögnum:
<ul>
<li>Stjórnun flokka</li>
<li>Afurðastjórnun</li>
<li>Afurðareigindir rásar</li>
<li>Úrval</li>
<li>Umsjón vörulista</li>
<li>Sett</li>
<li>Afsláttur &amp; af verði</li>
</ul></td>
<td><strong>Flokka- og afurðastjórnun</strong> vinnusvæði virkjar eftirfarandi virkni:
<ul>
<li>Stjórnun vöruúrvals</li>
<li>Rakning lífsferils úrvals</li>
<li>Stjórnun útgefinna afurða</li>
</ul>
<strong>Stjórnunarvinnusvæði verðs og afsláttar</strong> kveikir á eftirfarandi virkni:
<ul>
<li>Stjórnun verðs og afsláttar fyrir tiltekna rás og flokk</li>
<li>Stjórnun flokksverðsreglu</li>
<li>Forgangar verðs og afsláttar leyfar þér að úthluta forgangi á verðflokka og afslætti, þannig að hægt er að stýra röðinni sem þeim er beitt í</li>
<li>Stjórnun Fyrirtækjatengsla og afsláttar vörulista</li>
</ul>
<strong>Vörulistastjórnun</strong> vinnusvæðið virkjar eftirfarandi virkni:
<ul>
<li>Samantekt yfir Virkir vörulistar</li>
<li>Lífsferilsrakning vörulista á einni staðsetningu</li>
</ul></td>
<td><ul>
<li>Vinnusvæði auka skilvirkni og afköst fyrir starfsmenn með því að leyfa þeim að hafa umsjón með verkum og aðgerðir sem tengjast markaðshlutverki þeirra.</li>
<li>Forgangur Verð og afsláttur eiginleikinn veitir viðskiptavinir meiri stjórn á því hvernig verð og afslættir eru notuð. Eiginleikinn gerir virkjar einnig nýjar aðstæður þar sem hærri verð í verslun hafa betur en stöðluð verðum.</li>
</ul></td>
</tr>
<tr>
<td>Stjórna uppsetningu og aðgerðum smásölurásar.</td>
<td>Notendur þurfa að opna margar skjámyndir til að stýra þessum Framkvæma eftirfarandi verk:
<ul>
<li>Stofna og skilgreina nýja rásir og tengdum einingum.</li>
<li>Stjórna daglegar aðgerðir verslunar.</li>
<li>Vinna með smásölufærslur í Microsoft Dynamics AX, mynda smásöluuppgjör og uppfæra Microsoft Dynamics AX birgðir og fjárhag.</li>
</ul>
</td>
<td><strong>Uppsetning rásar</strong> vinnusvæði gerir kleift að framkvæma eftirfarandi verkefni:
<ul>
<li>Stofna nýja rásir og tengdum einingum.</li>
<li>Rekja framvinda skilgreiningar smásöluverslunar.</li>
<li>Skrefunum sem þarf til að ljúka við verkefni eða veita upplýsingar til að ljúka verkinu.</li>
<li>Fylgst með stöðu tæki, og beint villuleita og hlaða niður Retail Modern POS (MPOS) uppsetningu forrits í verslunum.</li>
<li>Fá aðgang að allar tengdar síður.</li>
</ul>
<strong>Stjórnun smásöluverslunar</strong> vinnusvæði gerir kleift að framkvæma eftirfarandi verkefni:
<ul>
<li>Stjórna starfsmanna og heimildir starfsmanna í POS.</li>
<li>Rekja vaktastöðu fyrir tiltekna verslun eða verslunarflokk.</li>
<li>Villuleita beint og hlaða niður MPOS uppsetningu forrits í verslunum.</li>
<li>Prenta skýrslur og opna tengdar síða.</li>
</ul>
<strong>Fjármál smásöluverslunar</strong> vinnusvæði gerir kleift að framkvæma eftirfarandi verkefni:
<ul>
<li>Búa til að reikna út og bóka uppgjör fyrir tiltekna rás.</li>
<li>Áætla runuvinnslu til að uppfæra birgðir, og reikna út og bóka uppgjör.</li>
<li>Rekja opin uppgjör.</li>
<li>Rekja vaktastöðu fyrir tiltekna verslun eða verslunarflokk.</li>
<li>Prenta skýrsla og Fá skjótan aðgang að allar tengdar síður.</li>
</ul></td>
<td>Vinnusvæði auka skilvirkni og afköst fyrir starfsmenn með því að leyfa þeim að hafa umsjón með verkum og aðgerðir sem tengjast uppsetningu rása, stjórnun verslunar og fjármál.</td>
</tr>
<tr>
<td>Stjórna aðgerðum fyrir upplýsingatækni smásölu.</td>
<td>Notendur þurfa að opna margar skjámyndir.</td>
<td><strong>Smásöluupplýsingatækni</strong> vinnusvæði virkjar fyrirspurnir Commerce Data Exchange í einn stað fyrir ákveðna rás, þannig að hægt er að framkvæma eftirfarandi verkefni:
<ul>
<li>Niðurhalslotur.</li>
<li>Upphalslotur.</li>
<li>Rekja mislukkaðar lotur og hefja aftur eða keyra þau aftur.</li>
<li>Skoða eða keyra væntanleg verk.</li>
</ul></td>
<td>Vinnusvæði auka skilvirkni og afköst fyrir starfsmenn með því að leyfa þeim að hafa umsjón með verkum og aðgerðir sem tengjast aðgerðum tengdum upplýsingatækni smásölu.</td>
</tr>
<tr>
<td>Innflutningur/flytja út gögn með því að nota gagnaeiningar.</td>
<td>AX 2012 styður út-úr-boxinu Microsoft Dynamics Retail Management System (RMS) yfirfærslu gegnum gagnarammann fyrir Inn-og Útflutning.</td>
<td>Gagnaeiningar smásölu hafa verið útvíkkaðar til að styðja öll sniðmát og tilvísunargögn sem tengjast smásölu. Það er einnig aukinn stuðning fyrir gagnaeiningar þvert á allar lausnir Dynamics AX.</td>
<td>Gagnaeiningar leyfa viðskiptavinum að gera innflutning og útflutning gagna á grunni lýsigagna. Einingar OData leyfa einnig viðskiptavini a‘ samþætta Dynamics AX við forrit þriðja aðila.</td>
</tr>
<tr>
<td>Framkvæma snjalla greiningu með BI skýrslum frá Dynamics Microsoft AX og biðlara sölustaðar.</td>
<td>Fleiri en 25 back-office skýrslur og fimm skýrslur samhliða rásum eru tiltækar.</td>
<td>Fleiri en 30 back-office skýrslur og 10 skýrslur samhliða rásum eru tiltækar.</td>
<td>Þessar skýrslur láta viðskiptavini hafa fleiri BI til að spá fyrir um leitni, afhjúpa innsýn, og starfa á stanslausum hámarksafköstum.</td>
</tr>
<tr>
<td>Greina sölugögn smásölurásar með því að nota "fylgjast Með frammistöðu smásölurásar“ Power BI efni.</td>
<td>Ekki tiltækt</td>
<td>Á PowerBI.com, veljið <strong>Sækja Gögn</strong>, og því næst velja <strong>Dynamics AX – frammistaða smásölurásar</strong> efnispakka. Færið inn Vefslóð fyrir Dynamics AX endastöðina til að sjá gögn birtast á yfirliti.</td>
<td>Með þremur eða fjórum smellir, getur fyrirtæki virkja Power BI yfirlit sem inniheldur mikilvægt fjárhagsgögn. Efni má sérstilla af fyrirtæki. Þar að auki geta notendur haft með Power BI yfirlitsreiti í þeirra sérsniðinn vinnusvæða í Dynamics AX þannig að geti síðan séð greiningarupplýsingar í fljótu bragði.</td>
</tr>
<tr>
<td>Grunnstilla notandaheimildir.</td>
<td>Ekki tiltækt</td>
<td>Viðskiptavinum getur valið hvort aðgerðir POS getur verið tiltækur neytendum. Smásöluþjónn notar heimildir fyrir forritunarviðmót forrits (API) innhringingar.</td>
<td>Hún veitir getuna til að skilgreina heimildir á stigi neytandans.</td>
</tr>
<tr>
<td>Stjórna og villuleita skilgreiningar eininga.</td>
<td>Ekki tiltækt</td>
<td>Skilgreiningastjórnun og villuprófari kveikir á eftirfarandi virkni:
<ul>
<li>Margar upphleðslur skilgreiningargagna</li>
<li>Villuleit Viðskiptaeiningar</li>
</ul></td>
<td>Hún býður upp á möguleika ræsa skilgreiningu með ræsiforriti, og villuleita stöðu og fullkomleika skilgreiningar fyrir ýmsar skilgreiningareiningar.</td>
</tr>
</tbody>
</table>

### <a name="retail-hardware-station"></a>Vélbúnaðarstöð smásölu

| Hvað hægt er að gera? | Dynamics AX 2012 | Dynamics AX 7.0 | Hví er þetta mikilvægt? |
|------------------|------------------|-----------------|------------------------|
| Virkja POS til að tengjast jaðarbúnaði á borð við prentara, peningaskúffur eða greiðslubúnað. | Vélbúnaðarregla MPOS er notuð til að tilgreina tæki sem eru notaðar. | Viðbætt Vélbúnaðarregla styður fleiri margbreytilegir vélbúnaðinn úr einni stöð á þá næstu. Ný forstilling Vélbúnaðarstöðvar styður einkvæmt Kenni afgreiðslustöðvar fyrir hverja Vélbúnaðarstöð þegar færslur rafrænu kortamillifærsluþjónustunni (EFT) eru unnar. KORTAMILLIFÆRSLA stuðning hefur verið sameinaður vélbúnaðarstöð til að minnka afskipti MPOS í greiðsluvinnslu kortamillifærslu. | Hún veitir meiri sveigjanleiki fyrir framkvæmd. Það einnig veitir aukinn öryggi og minnka snertingu við kreditkortagögn . |

### <a name="retail-server-and-data-management"></a>Retail-þjónn og gagnastjórnun

Retail Server og gagnastjórnun gerir kleift neytendum og fyrirtæki að stofna omni-rásar innnkaupaupplifun þvert á rásir á netinu, í verslun og símaveri.

<table>
<thead>
<tr>
<th>Hvað hægt er að gera?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Hví er þetta mikilvægt?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Tengjast við gagnagrunn commerce runtime (CRT) sem geymir viðskiptagögn rásarinnar með því að nota CRT-þjónustu.</td>
<td>OData V3 er stutt.</td>
<td>OData V4 er stutt.</td>
<td>Það hjálpar viðskiptavinum að vera í takt við gildandi með OData stöðlum. Hún stofnar einnig kraftmikla omni-rásar upplifun með samþætting sölu þvert á rásir verslunar, fartæki og á netinu.</td>
</tr>
<tr>
<td>Þjónustan Support retail er hýsanlegt sett þjónusta.</td>
<td>E-commerce API er ekki studdur gegnum Retail-þjónn.</td>
<td>E-commerce API er nú tiltækt gegnum Retail-Þjóns til að styðja aðstæður á netinu.</td>
<td>Hún veitir hýstur og kvarðanleg e-commerce þjónustu sem hægt er að nota með netverslunarþjónustu þriðja aðila.</td>
</tr>
<tr>
<td>Flytja gögn milli bakskrifstofu Microsoft Dynamics AX og smásölurása með notkun Commerce Data Exchange.</td>
<td>Commerce Data Exchange er kerfi sem flytur gögn milli Microsoft Dynamics AX og smásölurása, eins og netverslanir eða hefðbundnar verslanir. Frekari upplýsingar er að finna í <a href="https://technet.microsoft.com/library/dn741440.aspx">Commerce Data Exchange [AX 2012]</a>.</td>
<td>Það er virknitvístæða með Microsoft Dynamics AX 2012 CU8. Athugið hins vegar eftirfarandi upplýsingar:
<ul>
<li>Commerce Data Exchange hefur verið endurhannað fyrir skýið.</li>
<li>Async þjónusta notar beinan aðgang að gagnagrunni í gagnagrunn rásar.</li>
<li>Commerce Data Exchange: Real-time Service er hýst sem sérsniðna þjónustu Microsoft Dynamics AX.</li>
<li>MPOS stjórnar samstilling á milli ótengdan gagnagrunn og Retail-Þjóns.</li>
</ul></td>
<td>Commerce Data Exchange hefur verið endurhannað fyrir vettvang skýsins. Það heldur áfram að stjórna flutningum gagna milli Microsoft Dynamics AX og smásölurása, eins og netverslanir eða hefðbundnar verslanir.</td>
</tr>
<tr>
<td>Styður plug and play, hálf-samþætt milli-rásar greiðsluvinnslu með notkun greiðslu SDK.</td>
<td>AX 2012 veitir eftirfarandi aðgerðir:
<ul>
<li>Stuðningur fyrir allar rásir: POS, e-commerce og símaveri</li>
<li>Stuðningur fyrir kort sem er til staðar og kort sem er ekki til staðar</li>
<li>Síða til að samþykkja greiðslu</li>
<li>Jaðarbúnaðarstuðning við LS5300 og MX925 sem sýniskóða í Retail SDK</li>
</ul></td>
<td>Þessi útgáfu af Dynamics AX styður allar fyrirliggjandi Microsoft Dynamics AX fyrir Retail 2012 kredit/debet-kort aðgerðir og fjórum nýja viðbætur.</td>
<td>Það leyfir viðskiptavini að vinna kredit/debet kortafærslur fyrir greiðslur.</td>
</tr>
<tr>
<td>Virkja tæki með því að nota a Microsoft lykill (Microsoft Azure Active Directory (Azure AD)).</td>
<td>Ekki tiltækt</td>
<td>Eftirfarandi aðgerðir eru veittar:
<ul>
<li>Aukið öryggi með Azure AD virkjun fyrir í skýið.</li>
<li>Aukið öryggi fyrir táknastjórnun</li>
<li>Aukinn áreiðanleika, úrræðaleit og villuskilaboð meðan á virkjun stendur</li>
<li>Einfölduð stjórnunarverkefni upplýsingatækni sem tengjast virkjun</li>
<li>Endurskoðað líkan fyrir ógnir og öryggisatriði sem var kippt í liðinn</li>
</ul></td>
<td>Það veitir eftirfarandi ávinning:
<ul>
<li>Öryggi er bætt með Azure AD og tækjatákn/Kenni (RS símtöl sem nota tákn, notandatengdum geymsla forrita).</li>
<li>Það stöðvar óheimilaða notkun fjartengda notkun MPOS (múrsteinstæki).</li>
<li>Það rekur MPOS tæki fyrir PCI samræmi.</li>
<li>Það kortleggur efnisleg tæki á viðskiptaeiningar (afgreiðslukassa) með því að nota tákn tækis.</li>
<li>Það virkjar Stillingar fyrir hnökralausa MPOS virkni (númeraraðir og vélbúnaðarreglur) sem fyrsta snertipunkt MPOS.</li>
<li>Það veitir skýrslur um tækisupplýsingar úr höfuðstöðvum.</li>
</ul></td>
</tr>
<tr>
<td>Stjórna miðlaefni til að hanna og afgreiða úr Media Gallery.</td>
<td>Ekki tiltækt</td>
<td><ul>
<li>Styður upphleðslu myndar, og einnig skoða, stjórna og eyða úr Media Gallery fyrir bæði myndir hýstar ytra og hýstar í smásölu.</li>
<li>Styður upphleðslu myndar og skoða úr síðum einingar (<strong>Afurðir</strong>, <strong>Vörulista</strong>og svo framvegis) með því að tengja mynd úr safni og upphleðslu myndar úr á skjáborði.</li>
<li>Betrumbæta the myndir fyrir smámynd, sérstillt stærð, og upprunalega mynd.</li>
<li>Fjöldatengja einingar með því að nota sniðmát og vinnslur í bakgrunni fyrir fjöltengingar.</li>
<li>Microsoft Excel-samþætting hnekkir takmörkun eigindarflokks fyrir heitavenjur og forskilgreindar slóðir.</li>
<li>Styðja myndir sem ekki eru á netinu og tryggja myndir fyrir persónugreinanlegar upplýsingar (PII) efni, t.d. smásöluhýstar myndir starfsmaður og viðskiptavinur .</li>
</ul></td>
<td><ul>
<li>Það tekur til krafna um myndir sem eru hýstar ytra, þannig að hægt að forðast að fara fram og til baka, og þess í stað stjórna öllu í einum stað.</li>
<li>Hún veitir öflug efnisstýringu gegnum Media Gallery fyrir upphlöðnum myndum og myndum sem eru hýstar ytra, og veitir jafnframt síun til aðstoðar við að finna myndir.</li>
<li>Það er hægt að stofna auðveldlega fjöltengingar á milli mynda hýstum ytra og eininga, svo sem vörulista og afurðir.</li>
<li>Hann styður Smásöluhýsta geymslu fyrir myndir og samþættingu í Excel til að uppfæra á auðveldan hátt.</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="rich-clientele-experience"></a>Ríkuleg upplifun fastagesta

Smásala býður upp á frábæra fartækja upplifun hvar sem er, hvenær sem er og á hvaða tæki sem er. Þessi aðgerð bætir innkaupa og verslunar reynslu þvert á öllum rásum.

<table>
<thead>
<tr>
<th>Hvað hægt er að gera?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Hví er þetta mikilvægt?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Leita að, fletta, fletta upp, eða skanna afurðir, bæta afurðum í körfu , samþykkja greiðslu og útskráningar með snjöllum snertingivænni, ríkulegri og frábærri upplifun notanda á MPOS.</td>
<td>AX 2012 virkjar eftirfarandi aðgerðir:
<ul>
<li>Framkvæma sölu, skil og ógildingar.</li>
<li>Stofna, breyta, og sækja pantanir viðskiptavinar.</li>
<li>Framkvæma aðgerðir vakta og peningaskúffu.</li>
<li>Taka til og móttakist pantanir, og framkvæma birgðatalning.</li>
<li>Skoða skýrslur í verslun.</li>
</ul></td>
<td>Virkt tvístæða með AX 2012 MPOS er veitt. Þetta felur í sér eftirfarandi virkni:
<ul>
<li>Uppfletting viðskiptavina á milli verslanir/rása</li>
<li>Geta til að stofna pantanir viðskiptavinar án þess að opna rauntímaþjónustu</li>
<li>Bætt verkflæði við virkjun tækis , stöðu og villuboð</li>
<li>Lagfæringar á stækkunarhæfni, eins og kveikjur forbókunar og aðgerðastuðning til að bæta sérsnið</li>
</ul></td>
<td>Sölumaður geti unnið sölufærslur og pantanir viðskiptavina og framkvæma daglegum aðgerðum og birgðastjórnun, með því að nota fartæki alls staðar í versluninni.</td>
</tr>
<tr>
<td>Ræsa POS sem vefforrit í gegnumsölukerfi í skýinu.</td>
<td>Ekki tiltækt</td>
<td>Virkt tvístæða með MPOS er veitt. Þetta felur í sér eftirfarandi virkni:
<ul>
<li>Virkjun tækis með því að nota AAD</li>
<li>Góð svörun í hönnun útlits</li>
<li>Stuðningur fyrir Edge, Internet Explorer og Chrome vafra.</li>
</ul></td>
<td>Hún veitir POS vefforrit hefur virkni sem er ekki samhæf MPOS og sem hægt er að nota á milli vettvanga og vöfrum án uppsetningarkostnaðar.</td>
</tr>
<tr>
<td>Samþætta með efnisstýringarkerfum til að búa til omni-rásar e-commerce vefsíðu.</td>
<td>Microsoft SharePoint og búðargluggar þriðja aðila eru studd.</td>
<td>E-commerce verkvangur er veittur sem styður búðarglugga þriðja aðila. Vettvangurinn felur í sér eftirfarandi:
<ul>
<li>Ríkulegt API fyrir neytanda</li>
<li>Samþætting sannvottunar fyrir alla veitendur opinna kenna þriðja aðila</li>
<li>Samþætting greiðslu</li>
</ul></td>
<td>Viðskiptavinir hafa nú sveigjanleika til að nota efnisstýringarkerfi að þeirra vali.</td>
</tr>
<tr>
<td>Ná til viðskiptavinum í gegnum póstvörulista og straumlínulaga aðgerðir gegnum skjóta innfærslu pantana, aðstoð við sölu, og uppfyllingar með Símaveri.</td>
<td><ul>
<li>Rás símavers</li>
<li>Póstvörulistar</li>
<li>Hröð pöntunarfærsla og aðstoð við sölu</li>
<li>Betri uppfylling pantana</li>
<li>Þjónustudeild</li>
<li>Samþætt verðlagning og kynningartilboð/afsláttur</li>
</ul></td>
<td>Eiginleiki tvístæða með AX 2012 símaverslausn er tiltækt, að undanskildum verðhnekkingum.</td>
<td>Símaver eru tegund smásölurásar sem leyfir starfsmenn taka pantanir viðskiptavina yfir síma og stofna sölupantanir.</td>
</tr>
</tbody>
</table>

### <a name="commerce-essentials"></a>Grunnþættir viðskipta

Skilgreiningarvalkosturinn sem snýr að Smásölu og viðskiptum hjálpar til við að auðvelda virkjun smásölu.

| Hvað hægt er að gera? | Dynamics AX 2012 | Dynamics AX 7.0 | Hví er þetta mikilvægt? |
|------------------|------------------|-----------------|------------------------|
| Nota yfirlit grundvallaratriði viðskipta. | Svæðissíðu með tengla í valmyndaratriði er tiltæk. | Yfirlit fyrir Grunnþættir viðskipta veitir tengla í algeng verk, þar á meðal tengla í vinnusvæði, Power BI vefstýringar, uppáhalds atriði, nýlegar síður, og núverandi vinnuliði. | Bætt yfirlit gefur starfsmönnum getu með því að gera þá skilvirkari og útvegar sveigjanlega upphafspunkt fyrir öll verkefni smásölu. |
| Nota Gagnaeiningar til að opna breytingar á lyklum. | Breytingar á lyklum eru fluttar í möppu á skrárkerfinu. | Lykill breytingar eru aðgengilegur í gegnum gagnaeiningar. | Eiginleikinn veitir meiri sveigjanleiki þegar gagna flutt milli ólíkum kerfum. Þessi eiginleiki getur verið endurbætt gegnum OData forrit, einnig. |
| Nota sölukerfi í skýinu og MPOS. | Aðeins Enterprise POS (EPOS) er studd úr-úr-kassanum. | MPOS og sölukerfi í skýinu koma í stað EPOS biðlari. Rás e-Commerce hefur einnig verið bætt við grundvallaratriði viðskipta sjálfgefið. | Þessi aðgerð virkjar stuðning við rás út-úr-kassanum með hratt virkjanlegir sölustaðs biðlara. |
| Nota og vinna með tveggja laga uppbyggingu. | Rammi fyrir inn- og útflutning gagna veitir getuna til að flytja gögn milli AX 2012 og kerfi þriðja aðila. | Gagnaeiningar stofnuð til að auka stuðning við tveggja laga uppbyggingu . | Gagnaeiningar og OData forrit veita sértekningin sem fæst með lagi til að gera tveggja laga aðstæður auðveldari í notkun og viðhaldi. |
| Einfalda skjámyndir. | Sérstillt kóði á að einfalda notendaviðmótið. | Viðbætur Skjámyndar og valmyndarveita staðlaða einföldun notendaviðmóts. | Eiginleikinn veitir hraðar og auðveldari leið til að fínstilla skjámyndir samkvæmt þörfum fyrirtækisins í smásölu. |

### <a name="pos-task-recorder"></a>Verkskráning sölustaðar

<table>
<thead>
<tr>
<th>Hvað hægt er að gera?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Hví er þetta mikilvægt?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Stofna og deila verkefnaleiðbeiningar og skjöl fyrir Modern POS.</td>
<td>Ekki tiltækt</td>
<td>Verkskráning MPOS styður eftirfarandi aðgerðir:
<ul>
<li>Stofna verkskráningu fyrir ýmis verk sem eru framkvæmdar í MPOS.</li>
<li>Mynda skjal sem innifelur skrefunum og skjáskotum, og tengja hana við hnút í líkani viðskiptaferlis.</li>
</ul></td>
<td>Samstarfsaðila og óháðir lánardrottna hugbúnaðar (ISV) geta sérsníða MPOS og veita stuðning við skjöl til að þjálfa þeirra notendur.</td>
</tr>
</tbody>
</table>

### <a name="extensibility"></a>Stækkunarhæfni

<table>
<thead>
<tr>
<th>Hvað hægt er að gera?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Hví er þetta mikilvægt?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Styðja á umfangsmikla og auðveldlega virkjanlegir íhluti á milli höfuðstöðva, e-commerce, Símaveri, og Sölustað.</td>
<td>Hægt er að auka íhluti með því að nota Retail SDK. Engin pökkunar og virkjunargetu eru studd.</td>
<td>Stækkunarhæfnikrókar eru bættir á milli ýmislegra íhlutur til að styðja betur við kóðaeinangrun og þjónustugetu. Hér eru sumar aðgerðir sem eru teknar með:
<ul>
<li>Verkflæði, verkþáttur, og virkni</li>
<li>For-kveikjur og bókunarkveikjur sem leyfa þér að útvíkka verkflæði</li>
<li>Kveikjur forrita og aðgerða</li>
</ul>
Þar að auki er ramma tiltæk fyrir að byggja og pakka þessir íhlutir með MSBuild og virkja síðan hnökralaust sérsnið þitt gegnum Microsoft Dynamics Lifecycle Services (LCS).</td>
<td>Smásala hafa mjög sérstakar kröfur, byggt á mismunandi stigum framleiðslu og landsbundinni virkni. Með því að veita auðveldlega útvíkkanlegan verkvang virkjum við notkun á milli framleiðslu og markaða. Þar sem smásala hefur einnig mjög dreifða uppbygging, er getan að geta sett í notkun hnökralaust eitthvað sem bætir framleiðni mjög.</td>
</tr>
</tbody>
</table>

### <a name="lifecycle-management"></a>Líftímastjórnun

Lifecycle Services (LCS) býður upp á safn þjónustu sem viðskiptaaðilar og viðskiptavinir geta notað til að stjórna lífsferli kerfisins frá skráningar til daglegra aðgerða.

<table>
<thead>
<tr>
<th>Hvað hægt er að gera?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Hví er þetta mikilvægt?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Stjórna forritið gegnum virkjunarþjónustu skýs.</td>
<td>Ekki tiltækt</td>
<td>Hægt er að nota eftirfarandi grannfræði í skýið:
<ul>
<li>Smásölu eins kassa reynslu grannfræði</li>
<li>Smásölu fjölkassa grannfræði með miklum tiltækileika.</li>
<li>Forritara grannfræði með Retail SDK</li>
</ul>
Til staðar er bætt "lágsnertingar" uppsetning á íhlut biðlara í gegnum sjálfsafgreiðsluuppsetningu:
<ul>
<li>Retail Modern POS.</li>
<li>Vélbúnaðarstöð smásölu</li>
<li>Stuðningur fyrir upphleðslu og dreifingu sérsniðna pakka gegnum uppsetningar sjálfsafgreiðslu</li>
</ul></td>
<td>Virkjunarþjónustur skýs veita eftirfarandi ávinning:
<ul>
<li>Miklu minni virkjunarvinna og flækjustig fyrir Retail HQ íhluti</li>
<li>Innbyggð uppsetning í Microsoft Azure opið ský.</li>
<li>Bætt uppsetning sjálfsafgreiðslu fyrir íhluta í verslun til að gera skilgreiningu auðveldari og snjallari</li>
</ul></td>
</tr>
<tr>
<td>Fylgjast með ástandi kerfisins og greina villur og vandamál.</td>
<td>Þessi aðgerð krefst <a href="https://www.microsoft.com/download/details.aspx?id=42636">System Center 2012 Management Pack fyrir Microsoft Dynamics AX 2012 R3 CU8 Retail</a>.</td>
<td>Eftirlit og greining fyrir íhluti Smásölu er nú tiltækt gegnum í <strong>innsýn í aðgerðir</strong> yfirlit í LCS.</td>
<td><strong>Innsýn í aðgerðir</strong> yfirlit er í vöktunartengi sem byggist á skýi sem kemur í stað þarfarinnar að setja upp uppbyggingu System Center Operations Manager (SCOM).</td>
</tr>
<tr>
<td>Stofna, skilgreina, hlaða niður, og setja upp vélbúnaðarstöð smásölu og tæki með því að nota sjálfsafgreiðslu.</td>
<td>Með því að nota uppsetningar pakkara og Enterprise Portal, getur notandi unnið við sjálfvirka uppsetningu og skilgreiningu allra íhluta sem nauðsynlegir eru á tiltekinni tölvu, samkvæmt tilgreindri grannfræði.</td>
<td>Þar sem aðeins eru tveimur uppsetningarpakka, ein fyrir MPOS biðlara og hinn fyrir valinn íhlut vélbúnaðarstöðvar smásölu, hefur sjálfsafgreiðslu minnka magn vinnunnar sem er krafist á hverju stigi til að setja upp þessir íhlutir biðlara.</td>
<td>Sjálfsafgreiðsla miðar að því að minnka kröfur og að auðvelda fyrir notanda sem á að framkvæma uppsetningar.</td>
</tr>
</tbody>
</table>

## <a name="sales"></a>Sala

<table>
<thead>
<tr>
<th>Hvað hægt er að gera?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Hví er þetta mikilvægt?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Sækja stutt yfirlit yfir aðra valkosti afhendingar þegar þú lofar pöntunum til viðskiptavina.</td>
<td>Þegar skorður eru á afurðaframboði og umbeðinni afhendingardagsetningu viðskiptavinar fyrir eina eða fleiri afurðir í pöntun er ekki hægt að uppfylla, verður pöntun lofað að áskorun. Til að finna aðrar leiðir sem geta jafnað tap fyrir vandamál í tiltækileika og sendingartíma þannig að umbeðin dagsetning: viðskiptavinar megi standa við, eða að bjóða viðskiptavini lausn á afhendingu sem þeir geta samþykkt og treyst, getur pantanavinnslan þurft að opna nokkrar skjámyndir, sem hver býður aðeins hlutmengi nauðsynlegra upplýsinga. Nánar, einni skjámynd sýnir lagerbirgðir milli svæða, annarri skjámynd sýnir lagerbirgðir í samstæðustillingu, þriðja skjámynd gerir notendum kleift að reikna út fyrstu tiltækar dagsetningar fyrir eitt svæði/afbrigði í einu, og fjórða sýnir birgðapöntunum. Þess vegna finnst notendum þeir ekki vissir um að hafa íhugað alla viðeigandi valkosti í stað þess bara að velja lausn sem er skjót en ekki fyrsti kostur. Notendur líka finn ekki árangri, vegna þess að fjölmargir truflanir eiga sér stað á meðan á flæði pöntunar lofaðar þegar þeir opna og loka margar síður, og sameina innsýn og möguleikar.</td>
<td>Byggt á fyrirliggjandi reiknireglum fyrir útreikning afhendingardagsetningar, síðan <strong>Aðrir valkostir afhendingar </strong>býður upp á nýja reynslu notanda fyrir lofaða pöntun:
<ul>
<li>Það sameinar viðeigandi upplýsingar úr margar skjámyndir í eitt bil.</li>
<li>Hún býður „tilbúnir til afgreiðslu“-pakka, eins og í samsetningunni svæði/vöruhús/afbrigði/flutningsmáti, byggt á hröðustu skilyrðum afhendingar (fyrsta tiltæka dagsetningin) sem notandi getur valið úr.</li>
<li>Það gerir notanda kleift að velja valkosti úr hermunarviðmóti og flytja þá í sölupöntunarlínu.</li>
</ul></td>
<td>Fyrirtæki sem þrá að veita háa þjónustu við viðskiptavini á meðan þeir skuldbinda sig að veita hagræðingu birgðastefnu verða að vera fær um að lofa pöntunum á áreiðanlegan og samkeppnishæfan hátt. Eftir allt saman krefjast fyrirtæki viðskiptavina þeirra þess að vörur séu tiltækar á réttum tíma. <strong>Aðrir valkostir afhendingar</strong> verksíðan gerir pöntun á lofuðu verkefni sneggri, auðveldari og kerfisbundnari með því að auðkenna og mæla með bestu annarri afhendingardagsetningu á einum gagnvirkum stað.</td>
</tr>
</tbody>
</table>

## <a name="service-management"></a>Þjónustustjórnun

Engum nýjum eiginleikum hefur verið bætt við.

## <a name="transportation-management"></a>Flutningsstjórnun

Engum nýjum eiginleikum hefur verið bætt við.

## <a name="travel-and-expense"></a>Ferðalög og kostnaður

Engum nýjum eiginleikum hefur verið bætt við.

## <a name="warehouse-management"></a>Vöruhúsakerfi

| Hvað hægt er að gera? | Dynamics AX 2012 | Dynamics AX 7.0 | Hví er þetta mikilvægt? |
|------------------|------------------|-----------------|------------------------|
| Hlaða niður, setja upp og stilla gátt fyrir fartæki vöruhúss. | Hægt er að sækja, setja upp og skilgreina gátt á meðan Microsoft Dynamics AX uppsetningarferlið er í gangi, með staðlaða uppsetningu. Það er hannað fyrir sjálfsknúna skilgreiningu og á staðnum. | Hægt er að hlaða niður sjálfstæðu uppsetningarforriti í gegnum valmyndaratriði í vöruhúsakerfi. Það er hannað fyrir sjálfsknúna skilgreiningu og á staðnum. | Þegar verið er að setja upp aðgerð fartækis, verður að setja upp og skilgreina Fartækjagátt Vöruhúss staðbundið og fá tengingu við Dynamics AX í skýinu. |

## <a name="additional-resources"></a>Frekari upplýsingar

[Nýjungar eða breytingar í Finance and Operations heimasíða](whats-new-changed.md)

[Nýjar verkefnaleiðbeiningar (febrúar 2016)](new-task-guides-available-february-2016.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]