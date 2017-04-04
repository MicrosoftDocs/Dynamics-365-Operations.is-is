---
title: "Fartæki reikningssamþykktir"
description: "Fartæki getu í Microsoft Dynamics 365 aðgerða láta hanna fartæki reynslu viðskiptaferli notanda. Fyrir ítarlegri dæmi svæðis í einnig let&quot;s forriturum framlengja í getu sem þeir tryggja. Flestar virk leið til að fræðast sumar ný hugtök í fartæki er að fara gegnum ferlið fyrir nokkur dæmi hönnun. Í þessu efnisatriði er ætlað að gefa framkvæmd nálgun til að hanna fartæki aðstæður með því að taka reikningssamþykktir fyrir fartæki og notið svo lánardrottins. Í þessu efnisatriði eiga aðstoða við hönnun annar breytileiki í áætlanir og einnig er hægt að nota í öðrum aðstæðum þar sem ekki eru kostnaðarjafnaðar tengd reikningum lánardrottins."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 30229c0d24aed0bd927993b9af76b32d9bb073ee
ms.lasthandoff: 03/31/2017


---

# <a name="mobile-invoice-approvals"></a>Fartæki reikningssamþykktir

Fartæki getu í Microsoft Dynamics 365 aðgerða láta hanna fartæki reynslu viðskiptaferli notanda. Fyrir ítarlegri dæmi svæðis í einnig let's forriturum framlengja í getu sem þeir tryggja. Flestar virk leið til að fræðast sumar ný hugtök í fartæki er að fara gegnum ferlið fyrir nokkur dæmi hönnun. Í þessu efnisatriði er ætlað að gefa framkvæmd nálgun til að hanna fartæki aðstæður með því að taka reikningssamþykktir fyrir fartæki og notið svo lánardrottins. Í þessu efnisatriði eiga aðstoða við hönnun annar breytileiki í áætlanir og einnig er hægt að nota í öðrum aðstæðum þar sem ekki eru kostnaðarjafnaðar tengd reikningum lánardrottins.

<a name="prerequisites"></a>Forkröfur
-------------

| Skilyrði                                                                                            | lýsing                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fartæki handbook fyrirfram lesið                                                                                |(/ dynamics365/aðgerðir/dev-itpro/fartæki-netversluninni / mobile-platform.md)                                                                                                  |
| Dynamics 365 fyrir Aðgerðir                                                                             | Í umhverfi með Microsoft Dynamics 365 Aðgerðir útgáfu 1611 og Microsoft Dynamics fyrir Aðgerðir svæðis uppfæra 3 (Nóvember 2016)                   |
| Setja upp bráðabót KB 3204341.                                                                              | Verkskráning getur röngum skrá tvær Loka skipanir fyrir dropdown gluggum þetta tekinn með í Dynamics 365 Aðgerð svæðis uppfærslu 3 (Nóvember 2016 uppfæra) |
| Setja upp bráðabót KB 3207800.                                                                              | Þessa bráðabót gerir viðhengi til að skoða biðlarans fartæki þetta tekinn með í Dynamics 365 Aðgerð svæðis uppfærslu 3 (Nóvember 2016 uppfærslu).           |
| Setja upp bráðabót KB 3208224.                                                                              | Forritið kóðanum fyrir fartæki lánardrottins reiknings samþykki forritið þetta tekinn með í Microsoft Dynamics AX forritið 7.0.1 (Maí 2016).                          |
| Í Android eða iOS eða Windows tæki með fartæki forrits sem er sett upp fyrir Dynamics 365 fyrir Aðgerðir | Leita að forritið í versluninni viðeigandi forrits.                                                                                                                     |

## <a name="introduction"></a>Inngangur
Fartæki samþykki fyrir reikninga lánardrottins þurfa þrír bráðabætur sem nefnd eru í hlutanum "Forkröfur". Þessar bráðabætur ekki veita vinnusvæði fyrir samþykki reiknings. Til að læra hvað vinnusvæði er í samhengi við fartæki, lesa fartæki handbook sem nefnd eru í hlutanum "Forkröfur". Vinnusvæði samþykki reiknings verður að vera hannaðir. 

Hvert fyrirtæki orchestrates og skilgreinir mismunandi viðskiptaferli fyrir reikninga lánardrottins. Áður en fartæki reynslu fyrir samþykki reiknings lánardrottins, hanna ætti að íhuga að eftirfarandi þætti viðskiptaferlis. Hugmyndin er að nota þessi gögn vildarpunkta eins litlar heimildir og mögulegt er að fínstilla reynslu notanda á tækinu.

-   Svæði úr reikningshausinn mun notandinn sjá á í fartæki reynslu og í hvaða röð?
-   Svæði úr reikningslína mun notandinn sjá á í fartæki reynslu og í hvaða röð?
-   Hversu margar línur á reikningi eru í reikning? Nota reglu 80 20 er hér og fínstilla fyrir 80 prósent.
-   Verða notendur á að sjá dreifingar á fjárhagsupphæð (reikningur aðgreining) í fartækinu við skoðunarferlum Ef svarið þessari spurningu er já, íhugið eftirfarandi spurningum:
    -   Hversu margar dreifingar á fjárhagsupphæð (heildarverð, vsk, gjöld, skiptir og svo framvegis) eru fyrir reikningslínuna? Nota aftur, 80 20 reglu.
    -   Reikningar einnig hefur dreifingu fjárhagsupphæða í haus reiknings? Ef svo er, þessar dreifingar á fjárhagsupphæð skuli tiltæk á tækið?

> [!NOTE]
> Í þessu efnisatriði ekki útskýra hvernig á að breyta dreifingu fjárhagsupphæða þar sem þessi virkni er ekki studd stendur fyrir fartæki aðstæður.

-   Verða notendur á að sjá viðhengi fyrir reikninginn á tækið

Hönnun fartæki reynslu fyrir reikningssamþykktir verður mismunandi eftir svörin við þessum spurningum. Markmiðið er að fínstilla reynslu notanda fyrir viðskiptaferli í fartæki innan fyrirtækisins. Afganginn í afganginn af þessu efnisatriði, mælt verður þvínæst tvær frávik aðstæður sem eru byggðar á mismunandi svör við spurningunum á undan. 

Á almennu leiðbeininga, þegar unnið er með fartæki hönnuður, sem ganga úr skugga um að 'birta' breytingarnar koma í veg fyrir uppfærslur mistókst.

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a>Hönnun í aðstæðum samþykki einfalt reiknings fyrir Contoso
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Sviðsmyndareigind</th>
<th>Svara</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Svæði úr reikningshausinn mun notandinn sjá á í fartæki reynslu og í hvaða röð?</td>
<td><ol>
<li>Nafn lánardrottins</li>
<li>Heildarupphæð reiknings</li>
<li>Reikningslykill</li>
<li>Númer reiknings</li>
<li>Reikningsdagsetning</li>
<li>Lýsing reiknings</li>
<li>Gjalddagi</li>
<li>Gjaldmiðill reiknings</li>
</ol></td>
</tr>
<tr class="even">
<td>Svæði úr reikningslína mun notandinn sjá á í fartæki reynslu og í hvaða röð?</td>
<td><ol>
<li>Innkaupategund</li>
<li>Magn</li>
<li>Einingarverð</li>
<li>Nettóupphæð línu</li>
<li>Upphæð 1099</li>
</ol></td>
</tr>
<tr class="odd">
<td>Hversu margar línur á reikningi eru í reikning? Nota reglu 80 20 er hér og fínstilla fyrir 80 prósent.</td>
<td>1</td>
</tr>
<tr class="even">
<td>Verða notendur á að sjá dreifingar á fjárhagsupphæð (reikningur aðgreining) í fartækinu við skoðunarferlum</td>
<td>Já</td>
</tr>
<tr class="odd">
<td>Hversu margar dreifingar á fjárhagsupphæð (heildarverð, vsk, gjöld, og svo framvegis) eru fyrir reikningslínuna? Nota aftur, 80 20 reglu.</td>
<td>Heildarverð: 2 vsk: 0 Gjöld: 0</td>
</tr>
<tr class="even">
<td>Reikningar einnig hefur dreifingu fjárhagsupphæða í haus reiknings? Ef svo er, þessar dreifingar á fjárhagsupphæð skuli tiltæk á tækið?</td>
<td>Ekki notað</td>
</tr>
<tr class="odd">
<td>Verða notendur á að sjá viðhengi fyrir reikninginn á tækið</td>
<td>Já</td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a>Stofna vinnusvæðið

1.  Opna Dynamics 365 fyrir Aðgerðir og skrá sig inn í vafra.
2.  Eftir að notandi hefur verið skráður bæta **& hamur = fartæki** vefslóð eins og sýnt er í eftirfarandi dæmi og endurnýja þarf síðuna: https://&lt;yoururl&gt;/? cmp = usmf & mi = DefaultDashboard**& hamur = fartæki**
3.  Smellið á **Stillingar** hnappinn (gear) í efra hægri á síðunni og smelltu svo á **Fartæki forrits**. Hönnuður fartæki forrits verður sýna eins og Verki verkskráningar sýnir upp.
4.  Smellið á **Bæta** til að stofna nýja vinnusvæðið. Til dæmis, heiti vinnusvæðið **Mínar samþykktir**.
5.  Færðu inn lýsingu.
6.  Veljið lit vinnusvæði. Litur vinnusvæði verða notaðar fyrir almenna stíl fyrir fartæki reynslu fyrir þessa vinnusvæðið.
7.  Velja tákn fyrir vinnusvæðið.
8.  Smellið á **Lokið**
9.  Smellið á **Birta vinnusvæði** til að vista breytingar

### <a name="vendor-invoices-assigned-to-me"></a>Reikningar lánardrottins tengdir notanda

Fyrstu fartæki síðunnar sem ætti að hanna lista yfir reikninga sem eru úthlutaðar notandanum til skoðunar er. Til að hanna þessa fartæki síðu, skal nota við **VendMobileInvoiceAssignedToMeListPage** síðu í Dynamics 365 fyrir Aðgerðir. Áður en lokið er við þetta ferli gangið úr skugga um að sem minnst einn lánardrottinsreikning þér er úthlutað til skoðunar og reikningslínunni hefur tvær dreifingar. Þessi uppsetning uppfyllir kröfur fyrir þetta dæmi.

1.  Í Dynamics 365 Aðgerðir Vefslóð, skipta heiti valmyndaratriðis með **VendMobileInvoiceAssignedToMeListPage** til að opna fartæki útgáfu í **Biðreikninga lánardrottins sem mér eru úthlutaðir** listasíðu í á **Viðskiptaskuldir** kerfiseiningu. Eftir fjölda reikninga sem hafa verið í kerfinu sem er, þessi síða sýnir þá reikninga. Af tilteknum reikningi er að nota síuna vinstra megin. Þó er mælt ekki að þurfa til ákveðins reiknings í þessu dæmi. Við höfum krefjast rétt sumar reiknings sem úthlutað er til sem á að leyfa að hanna fartæki síðu. Nýjar síður sem eru tiltækar hafa verið hannaðar sérstaklega fyrir þróun fartæki aðstæður fyrir reikning lánardrottins. Þess vegna verður að nota þessar síður. Vefslóð á resemble eftirfarandi SLÓÐ og þegar hann er færður inn, verður birtast síðan sem birtist í skýringarmynd: https://&lt;yourURL&gt;/? cmp = usmf & mi =**VendMobileInvoiceAssignedToMeListPage**& hamur = fartæki [![Biðreikninga lánardrottins sem mér eru úthlutaðir síðuna](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)
2.  Smellið á **Stillingar** hnappinn (gear) í efra hægri á síðunni og smelltu svo á **Fartæki forrits**
3.  Veljið vinnustöð og smellið á **Breyta**
4.  Smellið á **Bæta síðu** til að stofna fartæki fyrstu síðu.
5.  Færið inn heiti, eins og **Mínar lánardrottnareikninga**, og lýsingu, eins og **reikninga Lánardrottins sem mér eru úthlutaðir til skoðunar**.
6.  Click **Done**.
7.  Í fartæki hönnuður á í **Svæði** flipanum, smellið **Velja svæði**. Dálkar á listasíðunni verður resemble eftirfarandi dæmi. [![Dálka í lánardrottnareikninga í Bið úthlutaðar mér síðu](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)
8.  Bæta þarf dálkum úr listasíðu sem verður að sýna notendur í fartæki síðu. Pöntun sem er bætt við er pöntunin sem svæðin birtast notandanum með forskoðunaraðgerðinni. Eina leiðin til að breyta röðun svæði verður með því að velja aftur öll svæði. Samkvæmt kröfur fyrir þetta dæmi í eftirfarandi átta svæði krafist. Hins vegar sumir notendur gætu hafa í huga átta svæði of mikið af upplýsingum til að hafa í farsíma. Þess vegna er mælt verður að sýna aðeins mikilvægustu svæði í fartæki lista. Eftirstandandi svæði birtast í upplýsingayfirlit mælt verður hanna seinna. Núna, mælt mun bæta við fyrir eftirfarandi svæði. Smellið á plúsmerkið (**+**) í þessum dálka til að bæta fartæki síðu.
    1.  Nafn lánardrottins
    2.  Heildarupphæð reiknings
    3.  Reikningslykill
    4.  Númer reiknings
    5.  Reikningsdagsetning

    Eftir svæðum er bætt við síðuna fartæki verður resemble eftirfarandi dæmi. [![Þegar svæðum er bætt við Síðu](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)
9.  Verður líka að bæta eftirfarandi dálka núna, þannig að við höfum hægt er að virkja verkflæðisaðgerðir síðar.
    1.  Sýna ljúka verki
    2.  Sýna úthluta verki
    3.  Sýna afturkalla verks
    4.  Sýna hafna verkefni
    5.  Sýna lokaverkefni beiðni
    6.  Sýna endursenda verks

10. Smellið á **Gert** til að fara úr breytingarham.
11. Smellið á **Aftur** og síðan **Gert** til að hætta við vinnusvæði
12. Smellið á **Birta vinnusvæði** til að vista breytingar sínar.
13. Virkja **Birta samtölu á biðstöðu lánardrottins reiknings reikninga lista** í færibreytuskjámynd viðskiptaskulda er notaður í **Reiknings**. Athugið, aðeins með því að virkja þessa færibreytu reikningssamtölur verður reiknuð birtast á listasíðu lánardrottnareikninga í bið lánardrottins. Þetta er hluti af fyrirfram requisite heitt laga 3208224 nýrri getu.

### <a name="vendor-invoice-details"></a>Upplýsingar um reikning lánardrottins

Til að hanna upplýsingasíðunni reiknings fyrir fartæki, í **VendMobileInvoiceHeaderDetails** síðu í Dynamics 365 fyrir Aðgerðir. Athugið að, allt eftir fjölda reikninga sem eru í kerfinu, þessi síða sýnir elsta reiknings (reikningur var stofnaður fyrst). Af tilteknum reikningi er að nota síuna vinstra megin. Þó er mælt ekki að þurfa til ákveðins reiknings í þessu dæmi. Við mælum rétt krefjast sum gögn sem mælt er hægt að hanna fartæki síðu. [![Verkflæði síðu](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)

1.  Í Dynamics 365 Aðgerðir Vefslóð, skipta heiti valmyndaratriðis með **VendMobileInvoiceHeaderDetails** til að opna skjámyndina
2.  Opnið hönnuðinn fartæki úr á **Stillingar** hnappinn (gear).
3.  Smellið á **Breyta** hnappinn til að hefja breytingarham í vinnusvæðið.
4.  Velja á ** Mínar lánardrottnareikninga ** síðunni sem þú stofnaðir áður, og smellið síðan á **Breyta**.
5.  Á við **Svæði** flipanum, smellið á **Hnitaneti** dálkhaus.
6.  Smellið á **Eiginleika**&gt;**Bæta síðu**. **Athugasemd:** Þegar smellt er á í **Hnitaneti** fyrirsögn og bæta síðan vensl við síðu er sjálfvirkt komið upplýsingar.
7.  Færa inn síðutitill, eins og **upplýsingar Um**, og lýsingu, eins og **Skoða línuupplýsingar og reikningshausinn**.
8.  Smellið á **Velja svæði**. Athugið, pöntun sem er bætt við er pöntunin sem svæðin birtast notandanum með forskoðunaraðgerðinni. Eina leiðin til að breyta röðun svæði verður með því að velja aftur öll svæði.
9.  Bætið eftirfarandi svæðum úr haus, eftir þörfum fyrir aðstæðurnar:
    1.  Nafn lánardrottins
    2.  Heildarupphæð reiknings
    3.  Reikningslykill
    4.  Númer reiknings
    5.  Reikningsdagsetning
    6.  Lýsing reiknings
    7.  Gjalddagi
    8.  Gjaldmiðill reiknings

10. Bæta við eftirfarandi svæðum úr töflunni línur á síðu:
    1.  Innkaupategund
    2.  Magn
    3.  Einingarverð
    4.  Nettóupphæð línu
    5.  Upphæð 1099

11. Eftir að öllum svæðum úr fyrri tvö skref hefur verið bætt við, smellið á **Gert**. Síðan verður resemble eftirfarandi dæmi. [![Þegar svæðum er bætt við Síðu](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)
12. Smellið á **Gert** til að fara úr breytingarham.
13. Smellið á **Aftur** og síðan **Gert** til að hætta við vinnusvæði
14. Smellið á **Birta vinnusvæði** til að vista skal vinnuna

### <a name="workflow-actions"></a>Verkflæðisaðgerðir

Til að bæta verkflæðisaðgerðir sem er í **VendMobileInvoiceHeaderDetails** síðu í Dynamics 365 fyrir Aðgerðir. Til að opna þessa síðu er að skipta heiti valmyndaratriðis í Vefslóð, sem var áður. Opna síðan fartæki hönnuður úr á **Stillingar** hnappinn (gear). Fylgið eftirfarandi skrefum til að bæta verkflæðisaðgerðir á upplýsingasíðu.

1.  Smellið á **Breyta** hnappinn til að hefja breytingarham í vinnusvæðið.
2.  Velja skal **upplýsingar Um** síðunni sem þú stofnaðir áður, og smellið síðan á **Breyta**.
3.  Á við **Aðgerðir** flipanum, smellið **Bæta aðgerð**.
4.  Færa inn aðgerð titill eins og **Samþykkja**, og lýsingu, eins og **Samþykkja reikninginn**. Athugið titill aðgerðarinnar sem færð er inn hér verður heiti aðgerðarinnar sem sýnd eru notanda í fartæki forrits.
5.  Click **Done**.
6.  Smellið á **Velja svæði**.
7.  Fara í gegnum verkflæðisferlið í **VendMobileInvoiceHeaderDetails** síðunni og ljúka við aðgerðina sem óskað er að skrá. Gangið úr skugga um að færa inn athugasemdir verkflæði meðan á þessu stendur þannig að svæði athugasemdir er einnig tekin með í fartæki reynslu.
8.  Eftir að aðgerð verkflæðis er keyrð, smellið á **Gert** að ljúka verkinu fyrir Valið svæði.
9.  Smellið á **Gert** til að fara úr breytingarham.
10. Smellið á **Aftur** og síðan **Gert** til að hætta við vinnusvæði
11. Smellið á **Birta vinnusvæði** til að vista skal vinnuna
12. Endurtakið skref 3 til 11 til að skrá öll áskilin verkflæðisaðgerðir. Athugið að, er þörf á að hafa reikninga úthlutað sem eru í ríkið sem á að gera verkflæði aðgerðir tiltækar sem hægt er að hanna til.
13. Opna Notepad eða Microsoft Visual Studio og líma eftirfarandi kóða. Skrána skal vista sem skrá .js. Þessi kóði er tveggja verið:
    1.  Það felur aukagjöldum tengjast verkflæði dálka sem mælt bætt við fyrr í fartæki listasíðu. Við mælum bætt þessum dálka þannig að forritið sem upplýsingar í samhengi og hægt er að gera á næsta skref.
    2.  Byggt á verkflæðisskrefi sem er virk er hún við viðskiptagrunninn til að sýna aðeins þær aðgerðir.

Athugið, nafn síður og aðrar stýringar í JS kóða verður að vera sú sama frá vinnusvæðið.

1.  Aðgerð aðal (metadataService dataService, cacheService, $q) {skila {appInit: aðgerð (appMetadata) {/ / Fela stýringar sem þarf að vera til staðar en ekki sýnilegur metadataService.configureControl (' Mínar--lánardrottnareikninga starfsmannsins, 'ShowAccept' {falið: satt}); metadataService.configureControl (' Mínar--lánardrottnareikninga starfsmannsins, 'ShowApprove' {falið: satt}); metadataService.configureControl (' Mínar--lánardrottnareikninga starfsmannsins, 'ShowReject' {falið: satt}); metadataService.configureControl (' Mínar--lánardrottnareikninga starfsmannsins, 'ShowDelegate' {falið: satt}); metadataService.configureControl (' Mínar--lánardrottnareikninga starfsmannsins, 'ShowRequestChange' {falið: satt}); metadataService.configureControl (' Mínar--lánardrottnareikninga starfsmannsins, 'ShowRecall' {falið: satt}); metadataService.configureControl (' Mínar--lánardrottnareikninga starfsmannsins, 'ShowComplete' {falið: satt}); metadataService.configureControl (' Mínar--lánardrottnareikninga starfsmannsins, 'ShowResubmit' { falinn: satt}); }, pageInit: aðgerð (pageMetadata, færibreytur) {ef (pageMetadata.Name == '-reikningsupplýsingar') {/ / Sýna/fela verkflæðisaðgerðir verkflæði á grundvelli skrefi metadataService.configureAction ('Samþykkja' {sýnilegt: satt}); metadataService.configureAction ('Samþykkja' {sýnilegt: satt}); metadataService.configureAction ('Hafna' {sýnilegt: satt}); metadataService.configureAction ('Úthluta' {sýnilegt: satt}); metadataService.configureAction (' beiðni Um breytingu ', {sýnilegt: satt}); metadataService.configureAction ("Afturköllun" {sýnilegt: satt}); metadataService.configureAction ('Lokið' {sýnilegt: satt}); metadataService.configureAction ('Endursending' {sýnilegt: satt});

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                       var showRejectControl = Boolean(rejectControl == 1);
                      var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                     metadataService.configureAction('Resubmit', { visible: showResubmitControl });
                   }
                 },
           };
        }

2.  Hlaða upp skrá kóða vinnusvæðið með því að velja á **Viðskiptagrunninn** flipa
3.  Smellið á **Gert** til að fara úr breytingarham.
4.  Smellið á **Aftur** og síðan **Gert** til að hætta við vinnusvæði
5.  Smellið á **Birta vinnusvæði** til að vista skal vinnuna

### <a name="vendor-invoice-attachments"></a>Viðhengi fyrir reikninga lánardrottins

1.  Smellið á **Stillingar** hnappinn (gear) í efra hægri á síðunni og smelltu svo á **Fartæki forrits**
2.  Smellið á **Breyta** hnappinn til að hefja breytingarham í vinnusvæðið.
3.  Velja skal ** upplýsingar Um ** síðunni sem þú stofnaðir áður, og smellið síðan á **Breyta**.
4.  Setja skal **Skjalastjórnun** valkosturinn að **Já** eins og sýnt er hér að neðan. **Athugasemd:** Ef það eru engar þarfir til að sýna viðhengi í fartækinu, hægt er að skilja þennan valkost að setja **Nei**, sem er sjálfgefin stilling.
5.  [![docmanagement](./media/docmanagement-216x300.png)](./media/docmanagement.png)
6.  Smellið á **Gert** til að fara úr breytingarham.
7.  Smellið á **Aftur** og síðan **Gert** til að hætta við vinnusvæði
8.  Smellið á **Birta vinnusvæði** til að vista skal vinnuna

### <a name="vendor-invoice-line-distributions"></a>Lína dreifingar fyrir reikning lánardrottins

Kröfur fyrir þetta dæmi staðfesta verður að aðeins-línustigi dreifingar og reikningur er alltaf með eina línu. Þar sem þessar aðstæður er einfalt reynslu notenda í fartækinu verður einnig að vera einfalt nógu sem notandinn er ekki með að kafa niður í nokkrum þrepum til að skoða dreifingu. Lánardrottnareikninga í Dynamics 365 aðgerða með möguleikanum á að sýna allar dreifingar úr haus reiknings. Þessi reynslu er hvað þarf mælt fartæki aðstæðum. Notið þess vegna mælum við verður í **VendMobileInvoiceAllDistributionTree** síðu til að hanna þessa hluti fartæki aðstæður. 

> [!NOTE] 
> Vita hver fjarvistartímabilsins yrði kröfur hjálpar okkur að ákveða hvaða tiltekna síðu til að nota og hvernig nákvæmlega til að efla fartæki reynslu notanda þegar mælt hannaður sem dæmi. Í seinni aðstæður mælt mun nota mismunandi síðu til að sýna dreifingar, þar sem þarfir fyrir aðstæður sem fyrir eru mismunandi.

1.  Í Vefslóð, skrifa yfir nafn valmyndaratriði, sem var áður en. Síðan sem birtist á resemble eftirfarandi dæmi. [![Allar dreifingar síðu](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)
2.  Opnið hönnuðinn fartæki úr á **Stillingar** hnappinn (gear).
3.  Smellið á **Breyta** hnappinn til að hefja breytingarham í vinnusvæðið. **Athugasemd:** sjást tvær nýjar síður var sjálfkrafa stofnuð. Kerfið stofnar þessar síður þar sem kveikt á skjalastjórnun í fyrri hluta. Þú mátt hunsa þessi nýjar síður.
4.  Smellið á **Bæta síðu**.
5.  Færa inn síðutitill, eins og **Skoða bókhald**, og lýsingu, eins og **Skoða bókhald fyrir reikning**.
6.  Click **Done**.
7.  Á við **Svæði** flipanum, smellið **Velja svæði**, veljið eftirfarandi svæði frá síðunni dreifingar og smellið síðan á **Gert**:
    1.  Upphæð
    2.  Gjaldmiðill
    3.  Fjárhagslykill

> [!NOTE] 
> Mælt lauk ekki að velja á **Lýsing** dálkur úr hnitaneti dreifingar, þar sem þarfir fyrir aðstæðurnar staðfest útvíkkað verð er aðeins upphæðin sem verður að vera dreifingar fyrir. Þess vegna er ekki notandi krefjast annað svæði til að ákvarða gerð upphæðar sem dreifingu fyrir. Hins vegar í næsta aðstæður mælt **verður** nota þessar upplýsingar, þar sem þarfir fyrir sem aðstæður sem hafa aðrar gerðir upphæð dreifingar (t.d. vsk).
8.  Smellið á **Gert** til að fara úr breytingarham.
9.  Smellið á **Aftur** og síðan **Gert** til að hætta við vinnusvæði
10. Smellið á **Birta vinnusvæði** til að vista skal vinnuna

**Athugasemd:** á **Skoða bókhald** fartæki síðu tekjureglur nú tengd neinum fartæki síður sem mælt hafa verið hannaðar hingað. Þar sem notandinn ætti að hafa til að fara í í **Skoða bókhald** frá síðunni á **upplýsingar Um** síðu í fartækinu, mælt verður að veita yfirlitstegundar úr á **upplýsingar Um** síðuna á í **Skoða bókhald** síðu. Þessi yfirlitstegundar mælt koma með því að nota viðbótar viðskiptagrunninn gegnum JavaScript.

1.  Opna skrá .js sem þú stofnaðir áður og bæta við línum sem eru auðkenndar í eftirfarandi kóða. Þessi kóði er tveggja verið:
    1.  Það hjálpar við að tryggja samræmda sem notendur má ekki fara beint í frá vinnusvæði til á **Skoða bókhald** síðu.
    2.  Það kemur víddarsamsetningar eftirlit úr skoðunarrúðunni í **upplýsingar Um** síðuna á í **Skoða bókhald** síðu.

> [!NOTE] 
> Nafn síður og aðrar stýringar í JS kóða verður að vera sama úr vinnusvæðið.

1.  Aðgerð aðal (metadataService dataService, cacheService, $q) {skila {appInit: aðgerð (appMetadata) {/ / Fela stýringar sem þarf að vera til staðar en ekki sýnilegur metadataService.configureControl (' Mínar--lánardrottnareikninga starfsmannsins, 'ShowAccept' {falið: satt}); metadataService.configureControl (' Mínar--lánardrottnareikninga starfsmannsins, 'ShowApprove' {falið: satt}); metadataService.configureControl (' Mínar--lánardrottnareikninga starfsmannsins, 'ShowReject' {falið: satt}); metadataService.configureControl (' Mínar--lánardrottnareikninga starfsmannsins, 'ShowDelegate' {falið: satt}); metadataService.configureControl (' Mínar--lánardrottnareikninga starfsmannsins, 'ShowRequestChange' {falið: satt}); metadataService.configureControl (' Mínar--lánardrottnareikninga starfsmannsins, 'ShowRecall' {falið: satt}); metadataService.configureControl (' Mínar--lánardrottnareikninga starfsmannsins, 'ShowComplete' {falið: satt}); metadataService.configureControl (' Mínar--lánardrottnareikninga starfsmannsins, 'ShowResubmit' { falinn: satt}); Fela síður á ekki við fyrir skoðunarrúðu metadataService.hideNavigation('View-accounting') rót; Tengilinn til að skoða bókhald metadataService.addLink ('-reikningsupplýsingar starfsmannsins, ' Skoða bókhald ', '-bókhalds-skilahnappur-yfirlitsstýringin ", 'Skoða bókhald', satt); }, pageInit: aðgerð (pageMetadata, færibreytur) {ef (pageMetadata.Name == '-reikningsupplýsingar') {/ / Sýna/fela verkflæðisaðgerðir verkflæði á grundvelli skrefi metadataService.configureAction ('Samþykkja' {sýnilegt: satt}); metadataService.configureAction ('Samþykkja' {sýnilegt: satt}); metadataService.configureAction ('Hafna' {sýnilegt: satt}); metadataService.configureAction ('Úthluta' {sýnilegt: satt}); metadataService.configureAction (' beiðni Um breytingu ', {sýnilegt: satt}); metadataService.configureAction ("Afturköllun" {sýnilegt: satt}); metadataService.configureAction ('Lokið' {sýnilegt: satt}); metadataService.configureAction ('Endursending' {sýnilegt: satt});

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                     var showRejectControl = Boolean(rejectControl == 1);
                       var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                       metadataService.configureAction('Resubmit', { visible: showResubmitControl });
        }
                 },
           };
        }

2.  Hlaða upp skrá kóða vinnusvæðið með því að velja á **Viðskiptagrunninn** flipa til að skrifa yfir fyrri kóða
3.  Smellið á **Gert** til að fara úr breytingarham.
4.  Smellið á **Aftur** og síðan **Gert** til að hætta við vinnusvæði
5.  Smellið á **Birta vinnusvæði** til að vista skal vinnuna

### <a name="validation"></a>Prófun

Opna forritið og tengjast við Dynamics 365 fyrir tilvik Aðgerðir úr fartækis. Gangið úr skugga um að sem að skrá sig inn í fyrirtækið þar sem reikningar lánardrottna eru úthlutuð til skoðunar. Ætti að vera hægt að framkvæma eftirfarandi aðgerðir:

-   Finna skal **Mínar samþykktir** vinnusvæði.
-   Kafa í á **Mínar samþykktir** vinnusvæði og sjá á **Mínar lánardrottnareikninga** síðu.
-   Kafa í á **Mínar lánardrottnareikninga** síðunni og til að sjá lista yfir reikninga sem eru úthlutuð.
-   Kafa í einn af reikningunum og sjá upplýsingar um haus og upplýsingar um innkaupapöntunarlínu.
-   Upplýsingar um síðuna sjá tengil viðhengi og notið þennan tengil til að fara í viðhengi lista og skoða í viðhengi.
-   Á síðunni upplýsingar, sjá tengil í **Skoða bókhald** síðunni og hægt er að nota þennan tengil til að fletta að síðu dreifingar og skoða dreifingu.
-   Á upplýsingasíðu, smellið á **Aðgerðir** valmynd neðst, og framkvæma aðgerðir í verkflæði sem á við um skref í verkflæði.

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a>Hönnun í aðstæðum samþykki flókið reikningi fyrir Fabrikam
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Sviðsmyndareigind</th>
<th>Svara</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Svæði úr reikningshausinn mun notandinn sjá á í fartæki reynslu og í hvaða röð?</td>
<td><ol>
<li>Nafn lánardrottins</li>
<li>Reikningsupphæð</li>
<li>Reikningslykill</li>
<li>Númer reiknings</li>
<li>Reikningsdagsetning</li>
<li>Lýsing reiknings</li>
<li>Gjalddagi</li>
<li>Gjaldmiðill reiknings</li>
</ol></td>
</tr>
<tr class="even">
<td>Svæði úr reikningslína mun notandinn sjá á í fartæki reynslu og í hvaða röð?</td>
<td><ol>
<li>Innkaupategund</li>
<li>Magn</li>
<li>Einingarverð</li>
<li>Nettóupphæð línu</li>
<li>Upphæð 1099</li>
</ol></td>
</tr>
<tr class="odd">
<td>Hversu margar línur á reikningi eru í reikning? Nota reglu 80 20 er hér og fínstilla fyrir 80 prósent.</td>
<td>5</td>
</tr>
<tr class="even">
<td>Verða notendur á að sjá dreifingar á fjárhagsupphæð (reikningur aðgreining) í fartækinu við skoðunarferlum</td>
<td>Já</td>
</tr>
<tr class="odd">
<td>Hversu margar dreifingar á fjárhagsupphæð (heildarverð, vsk, gjöld, og svo framvegis) eru fyrir reikningslínuna? Nota aftur, 80 20 reglu.</td>
<td>Heildarverð: 2 vsk: 2 Gjöld: 2</td>
</tr>
<tr class="even">
<td>Reikningar einnig hefur dreifingu fjárhagsupphæða í haus reiknings? Ef svo er, þessar dreifingar á fjárhagsupphæð skuli tiltæk á tækið?</td>
<td>Ekki notað</td>
</tr>
<tr class="odd">
<td>Verða notendur á að sjá viðhengi fyrir reikninginn á tækið</td>
<td>Já</td>
</tr>
</tbody>
</table>

### <a name="exercise"></a>Exercise

Eftirfarandi afbrigði er hægt að gera aðstæðum 1, eftir þörfum fyrir aðstæður 2. Nota þessa hluta sem á exercise sem hægt er að ljúka fyrir learning tilgangi.

1.  Þar sem fleiri línur á reikningi eru væntanlegar í dæmi 2, eru eftirfarandi breytingar hönnunina mun aðstoða við stillingu reynslu notenda í fartækinu:
    1.  Í stað þess að skoða reikningslínur á upplýsingasíðu (og dæmi 1), notendur hægt að velja að skoða línur á sérstakri síðu fartæki.
    2.  Þar sem fleiri en einn reikningslínu búist er við í þessu dæmi, ef við **VendMobileInvoiceAllDistributionTree** síða er notuð til að hanna síðan dreifingar fyrir fartæki (og dæmi 1), það gæti verið confusing notandans til að láta línur dreifingar. Notið þess vegna er **VendMobileInvoiceLineDistributionTree** síðu til að hanna síðan dreifingar.
    3.  Góð regla er dreifing skuli sýnd í samhengi við reikningslínu í þessu dæmi. Þess vegna tryggja að getur notandinn kafað í línu til að sjá síðan dreifingar. Nota getu tengil á síðuna til að koma á kafa gegnum, rétt eins og var fyrir haus og upplýsingar um síðurnar í dæmi 1.

2.  Þar sem búist er við fleiri en eina gerð upphæðar í dreifingu í dæmi 2 (vsk, gjöld, og svo framvegis) verður að gagni til að sýna lýsingu á gerð upphæðar. (Mælt sleppt þessar upplýsingar í dæmi 1.)

## <a name="conclusion"></a>Niðurstaða
Fartæki svæðis og getu forritið gera kleift að hanna fartæki aðstæður sem er fínstillt fyrir grunngerð innan fyrirtækis notanda. Byggt á dæmunum sem veittar eru í þessu efnisatriði er hægt að reyna annar breytileiki og stofna mismunandi reynslu sem uppfylla tiltekna þörf.


