---
title: Reikningssamþykktir í fartækjum
description: Í þessu efnisatriði er ætlað að gefa praktíska nálgun til að hanna farsímaaðstæður með því að taka reikningssamþykktir fyrir fartæki sem notkunartilvik.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 83d95ef6d9fcff060ac992b11ab5773af075fea5409e43430b4826dc097570c7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737356"
---
# <a name="mobile-invoice-approvals"></a>Reikningssamþykktir í fartækjum

[!include [banner](../includes/banner.md)]

Farsímageta gerir fyrirtækjanotenda kleift að hanna farsímaupplifun. Fyrir ítarlegri dæmi leyfir kerfið forriturum einnig að framlengja getu eins og þeir vilja. Skilvirkasta leiðin til að læra sum af nýju hugtökunum í fartæki er að fara gegnum ferlið að hanna ný dæmi. Í þessu efnisatriði er ætlað að gefa praktíska nálgun til að hanna farsímaaðstæður með því að taka reikningssamþykktir fyrir fartæki sem notkunartilvik. Þetta efnisatriði á að aðstoða við hönnun á öðrum frávikum á aðstæðum og einnig er hægt að nota það í öðrum aðstæðum sem eru ekki eru tengdar reikningum lánardrottins.

## <a name="prerequisites"></a>Frumskilyrði

| Skilyrði                                                                                            | lýsing                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fyrirframlestur farsímahandbókar                                                                                |[Fartækjaverkvangur](../../fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| Dynamics 365 Finance                                                                              | Vertu viss um að þú sért að nota umhverfi sem er með útgáfu 1611 og uppfærslu verkvangs 3 (nóvember 2016).                   |
| Setja upp bráðabót KB 3204341.                                                                              | Verkskráning getur skráð rangt tvær Loka skipanir fyrir felliglugga; þetta er innifalið í uppfærslu verkvangs 3 (uppfærsla nóvember 2016). |
| Setja upp bráðabót KB 3207800.                                                                              | Þessi bráðabót leyfir að viðhengi séu skoðuð í farsímabiðlara; þetta er innifalið í uppfærslu verkvangs 3 (uppfærsla í nóvember 2016).           |
| Setja upp bráðabót KB 3208224.                                                                              | Forritakóði fyrir farsímasamþykkt reiknings lánardrottins; þetta er innifalið í útgáfu 7.0.1 (maí 2016).                          |
| Í tæki með Android eða iOS eða Windows sem er með farsímaforritið sem er uppsett. | Leita að forritinu í viðeigandi forritaverslun.                                                                                                                     |

## <a name="introduction"></a>Inngangur
Farsímasamþykktir fyrir reikninga lánardrottins þurfa þrjár bráðabætur sem nefndar eru í hlutanum „Forkröfur“. Þessar bráðabætur veita ekki vinnusvæði fyrir reikningssamþykki. Til að læra hvað vinnusvæði er í samhengi við fartæki, skaltu lesa farsímahandbókina sem er nefnd í hlutanum „Forkröfur“. Vinnusvæði reikningssamþykkta verður að vera hannað. 

Hvert fyrirtæki skipuleggur og skilgreinir mismunandi viðskiptaferli fyrir reikninga lánardrottins. Áður en farsímaupplifun fyrir samþykktir reiknings lánardrottins er hönnuð ætti að íhuga að eftirfarandi þætti viðskiptaferlis. Hugmyndin er að nota þessa gagnapunkta eins mikið og hægt er til að hámarka reynslu notanda á tækinu.

-   Hvaða svæði úr reikningsfyrirsögninni mun notandi vilja sjá í farsímareynslunni og í hvaða pöntun?
-   Hvaða svæði úr reikningslínunum mun notandi vilja sjá í farsímareynslunni og í hvaða pöntun?
-   Hversu margar reikningslínur eru í reikningi? Nota reglu 80-20 hér og fínstilla fyrir 80 prósent.
-   Munu notendur vilja sjá dreifingar á fjárhagsupphæð (reikningskóðun) í fartækinu við skoðunarferlum? Ef svarið þessari spurningu er já, íhugið eftirfarandi spurningar:
    -   Hversu margar dreifingar á fjárhagsupphæð (heildarverð, vsk, gjöld, skipti og svo framvegis) eru fyrir reikningslínu? Aftur skal nota 80-20 reglu.
    -   Eru reikningarnir einnig með dreifingu fjárhagsupphæða í haus reiknings? Ef svo er, ættu þessar dreifingar á fjárhagsupphæð að vera tiltækar í tækinu?

    > [!NOTE]
    > Þetta efnisatriði útskýrir ekki hvernig á að breyta dreifingu fjárhagsupphæða þar sem þessi virkni er ekki studd eins og stendur fyrir farsímaaðstæður.

-   Munu notendur vilja sjá viðhengi fyrir reikninginn í tækinu?

Hönnun farsímareynslu fyrir reikningssamþykktir verður mismunandi, eftir því hver svörin verða við þessum spurningum. Markmiðið er að fínstilla reynslu notanda fyrir viðskiptaferli í fartæki innan fyrirtækisins. Í afganginum af þessu efnisatriði skoðum við tvær frávikaaðstæður sem byggjast á mismunandi svörum við spurningunum hér á undan. 

Almennt séð, þegar unnið er með farsímahönnuði, þarf að ganga úr skugga um að 'birta' breytingarnar til að koma í veg fyrir uppfærslur mistakist.

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a>Hönnun á einföldum aðstæðum reikningssamþykktar fyrir Contoso
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
<td>Hvaða svæði úr reikningsfyrirsögninni mun notandi vilja sjá í farsímareynslunni og í hvaða pöntun?</td>
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
<td>Hvaða svæði úr reikningslínunum mun notandi vilja sjá í farsímareynslunni og í hvaða pöntun?</td>
<td><ol>
<li>Innkaupategund</li>
<li>Magn</li>
<li>Einingarverð</li>
<li>Nettóupphæð línu</li>
<li>Upphæð 1099</li>
</ol></td>
</tr>
<tr class="odd">
<td>Hversu margar reikningslínur eru í reikningi? Nota reglu 80-20 hér og fínstilla fyrir 80 prósent.</td>
<td>1</td>
</tr>
<tr class="even">
<td>Munu notendur vilja sjá dreifingar á fjárhagsupphæð (reikningskóðun) í fartækinu við skoðunarferlum?</td>
<td>Já</td>
</tr>
<tr class="odd">
<td>Hversu margar dreifingar á fjárhagsupphæð (heildarverð, vsk, gjöld og svo framvegis) eru fyrir reikningslínuna? Aftur skal nota 80-20 reglu.</td>
<td>Heildarverð: 2 vsk: 0 Gjöld: 0</td>
</tr>
<tr class="even">
<td>Eru reikningarnir einnig með dreifingu fjárhagsupphæða í haus reiknings? Ef svo er, ættu þessar dreifingar á fjárhagsupphæð að vera tiltækar í tækinu?</td>
<td>Ekki notað</td>
</tr>
<tr class="odd">
<td>Munu notendur vilja sjá viðhengi fyrir reikninginn í tækinu?</td>
<td>Já</td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a>Stofna vinnusvæðið

1.  Í vafra og skráðu þig inn í forritið.
2.  Eftir að notandi hefur verið skráður bæta **&mode = fartæki** vefslóð eins og sýnt er í eftirfarandi dæmi og endurnýja þarf síðuna: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**
3.  Smellið á hnappinn **Stillingar** (tannhjól) í efst til hægri á síðunni og smelltu svo á **Fartæki forrits**. Hönnuður fartæki forrits verður birtast eins og Verkskráning birtist.
4.  Smelltu á **Bæta við** til að búa til nýtt vinnusvæði. Í þessu dæmi er vinnusvæðinu gefið heitið **Samþykktir**.
5.  Færðu inn lýsingu.
6.  Velja lit vinnusvæðis Litur vinnusvæðisins verður notaður fyrir heildarstíl fyrir farsímareynslu fyrir þetta vinnusvæði.
7.  Velja tákn fyrir vinnusvæðið.
8.  Smelltu á **Lokið**
9.  Smelltu á **Birta vinnusvæði** til að vista breytingarnar

### <a name="vendor-invoices-assigned-to-me"></a>Reikningar lánardrottins tengdir notanda

Fyrsta farsímasíðan sem ætti að hanna er listi yfir reikninga sem eru úthlutaðir notandanum til skoðunar. Til að hanna þessa farsímasíðu notarðu síðuna **VendMobileInvoiceAssignedToMeListPage**. Áður en lokið er við þetta ferli skal ganga úr skugga um að a.m.k. einn lánardrottinsreikningur sé úthlutaður til þín til skoðunar og að reikningslínan hafi tvær dreifingar. Þessi uppsetning uppfyllir kröfur fyrir þetta dæmi.

1.  Í vefslóðinni skal skipta út heiti valmyndaratriðis með **VendMobileInvoiceAssignedToMeListPage** til að opna farsímaútgáfu af listasíðunni **Biðreikningar lánardrottins sem mér eru úthlutaðir** í kerfiseiningunni **Viðskiptaskuldir**. Það fer eftir fjölda reikninga sem er úthlutað til þín í kerfinu en þessi síða sýnir þá reikninga. Til að finna tilgreindan reikning er hægt að nota síuna til vinstri. Hins vegar þurfum við ekki tilgreindan reikning fyrir þetta dæmi. Við þurfum bara reikning sem úthlutað er til þín, sem gerir þér kleift að hanna farsímasíðuna. Nýjar síður sem eru tiltækar hafa verið hannaðar sérstaklega fyrir þróun farsímaaðstæðna fyrir reikning lánardrottins. Þess vegna verður að nota þessar síður. Vefslóðin á að líkjast eftirfarandi vefslóð og þegar hún hefur verið færð inn verður síðan sem er sýnd á skýringarmyndinni að birtast: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile 

    [![Síðan Reikningar lánardrottins í bið sem notanda hefur verið úthlutað.](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)
    
2.  Smellið á hnappinn **Stillingar** (tannhjól) í efra hægra horni síðunnar og svo á **Farsímaforrit**.
3.  Veljið vinnustöð og smellið á **Breyta**
4.  Smellið á **Bæta við síðu** til að stofna fyrstu farsímasíðuna.
5.  Færið inn heiti, eins og **Mínar lánardrottnareikningar**, og lýsingu, eins og **Reikninga lánardrottins sem mér eru úthlutaðir til skoðunar**.
6.  Smelltu á **Lokið**.
7.  Í farsímahönnuði, á flipanum **Svæði** er smellt á **Velja svæði**. Dálkar á listasíðunni verða að líkjast eftirfarandi mynd. 

    [![Dálkar á síðunni Reikningar lánardrottins í bið sem notanda hefur verið úthlutað.](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)
    
8.  Bæta þarf dálkum af listasíðunni, sem verða að birtast notendum á farsímasíðunni. Röðin sem þú bætir við er sú röð sem svæðin eru birt notanda. Eina leiðin til að breyta röðun svæða verður með því að velja aftur öll svæði. Samkvæmt kröfum fyrir þetta dæmi er eftirfarandi átta svæða krafist. Hins vegar gæti sumum notendum þótt átta svæði of mikið af upplýsingum til að hafa í farsíma. Þess vegna munum við aðeins sýna mikilvægustu svæðin í farsímalistayfirlitinu. Eftirstandandi svæði birtast í upplýsingayfirliti sem við munum hanna seinna. Eins og stendur bætum við eftirfarandi svæðum við. Smellið á plúsmerkið (**+**) í þessum dálkum til að bæta við farsíðu.
    - Nafn lánardrottins
    - Heildarupphæð reiknings
    - Reikningslykill
    - Númer reiknings
    - Reikningsdagsetning

    Eftir að svæðum er bætt við síðuna verður farsímasíðan að líkjast eftirfarandi dæmi. 
    
    [![Síðan eftir að svæðum hefur verið bætt við.](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)

9.  Einnig verður að bæta eftirfarandi dálkum við núna, svo að við getum virkjað verkflæðisaðgerðir síðar.
    - Sýna lokin verk
    - Sýna úthlutað verk
    - Sýna afturkallað verk
    - Sýna hafnað verk
    - Sýna verk með umbeðin lok
    - Sýna endursent verk

10. Smellið á **Lokið** til að fara úr breytingarstillinigu.
11. Smellið á **Til baka** og síðan **Lokið** til að fara af vinnusvæðinu
12. Smelltu á **Birta vinnusvæði** til að vista verkið.
13. Virkja **Birta samtölu á biðstöðu lánardrottins reiknings reikninga lista** í færibreytuskjámynd viðskiptaskulda undir **Reikningur**. Athugið að aðeins með því að virkja þessa færibreytu verða reikningssamtölur reiknaðar til að birtast á listasíðu lánardrottnareikninga í bið. Þetta er ný geta sem er hluti af frumskilyrðum bráðabóta 3208224.

### <a name="vendor-invoice-details"></a>Reikningsupplýsingar lánardrottins

Til að hanna reikningsupplýsingasíðu fyrir farsíma skal nota síðuna **VendMobileInvoiceHeaderDetails**. Athugið að það fer eftir fjölda reikninga sem er úthlutað til þín í kerfinu en þessi síða sýnir elsta reikninginn (reikninginn sem var stofnaður fyrst). Til að finna tilgreindan reikning er hægt að nota síuna til vinstri. Hins vegar þurfum við ekki tilgreindan reikning fyrir þetta dæmi. Við þurfum bara reikningsgögn svo að við getum hannað farsímasíðuna. 

[![Verkflæðissíða.](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)

1. Í vefslóðinni skal skipta út heiti valmyndaratriðis með **VendMobileInvoiceHeaderDetails** til að opna skjámyndina

2. Opnið hönnuðinn fartæki með hnappninum **Stillingar** (tannhjól).

3. Smellið á **Breyta** hnappinn til að hefja breytingarham í vinnusvæðið.

4. Veldu síðuna **Reikningar lánardrottna minna** sem þú bjóst til áður og smelltu síðan á **Breyta**.

5. Á flipanum **Svæði** smellirðu á dálkhausinn **Hnitanet**.

6. Smellið á **Eiginleikar &gt; Bæta við síðu**. **Athugasemd:** Þegar smellt er á fyrirsögnina **Hnitanet** og síðu bætt við, er venslum við upplýsingasíðu sjálfvirkt komið á.

7. Færðu inn síðutitill, eins og **Upplýsingar um reikning**, og lýsingu, eins og **Skoða línuupplýsingar og reikningshausinn**.

8. Smellið á **Velja svæði**. Athugið að röðin sem þú bætir við er sú röð sem svæðin verða birt notanda. Eina leiðin til að breyta röðun svæða verður með því að velja aftur öll svæði. 

9. Bættu við eftirfarandi reitum úr haus, samkvæmt kröfum fyrir þetta dæmi.
   - Nafn lánardrottins
   - Heildarupphæð reiknings
   - Reikningslykill
   - Númer reiknings
   - Reikningsdagsetning
   - Lýsing reiknings
   - Gjalddagi
   - Gjaldmiðill reiknings

10. Bæta við eftirfarandi svæðum úr línutöflunni á síðuna:
    - Innkaupategund
    - Magn
    - Einingarverð
    - Nettóupphæð línu
    - Upphæð 1099

11. Eftir að öllum svæðum úr fyrri tvö skref hefur verið bætt við, smellið á **Lokið**. Dálkar á listasíðunni verða að líkjast eftirfarandi dæmi.
    
    [![Mynd sem sýnir viðbótarreiti bætt við.](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)

12. Smellið á **Lokið** til að fara úr breytingarstillinigu.

13. Smellið á **Til baka** og síðan **Lokið** til að fara af vinnusvæðinu

14. Smelltu á **Birta vinnusvæði** til að vista verkið

### <a name="workflow-actions"></a>Verkflæðisaðgerðir

Til að bæta við verkflæðisaðgerðum skal nota síðuna **VendMobileInvoiceHeaderDetails**. Til að opna þessa síðu skal skipta út heiti valmyndaratriðis í vefslóð, eins og gert var áður. Síðan skal opna hönnuðinn fartæki með hnappninum **Stillingar** (tannhjól). Fylgið þessum skrefum til að bæta við verkflæðisaðgerðum á upplýsingasíðuna. Þú verður að hafa reikninga úthlutaða þér með rétta stöðu svo að verkflæðisaðgerðir sem þú ætlar að hanna fyrir séu tiltækar þér.

#### <a name="record-workflow-actions"></a>Skráning verkflæðisaðgerða
1.  Smellið á **Breyta** hnappinn til að hefja breytingarham í vinnusvæðið.
2.  Veldu síðuna **Upplýsingar um reikning** sem þú stofnaðir áður og smelltu síðan á **Breyta**.
3.  Á flipanum **Aðgerðir** er smellt á **Bæta aðgerð við**.
4.  Færðu inn aðgerðatitill eins og **Samþykkja**, og lýsingu, eins og **Samþykkja reikninginn**. Athugið að titill aðgerðarinnar sem er færður hér inn verður heiti aðgerðarinnar sem er birt notanda í farsímaforritinu.
5.  Smelltu á **Lokið**.
6.  Smellið á **Velja svæði**.
7.  Fara í gegnum verkflæðisferlið í **VendMobileInvoiceHeaderDetails** síðunni og ljúka við aðgerðina sem óskað er að skrá. Gangið úr skugga um að færa inn athugasemdir um verkflæðið meðan á því stendur þannig að athugasemdasvæðið sé einnig innifalið í farsímareynslunni.
8.  Þegar aðgerð verkflæðis hefur verið keyrð er smellt á **Gert** að ljúka verkinu fyrir Valið svæði.
9.  Smellið á **Lokið** til að fara úr breytingarstillinigu.
10. Smellið á **Til baka** og síðan **Lokið** til að fara af vinnusvæðinu
11. Smelltu á **Birta vinnusvæði** til að vista verkið
12. Endurtaktu fyrra skref til að skrá allar nauðsynlegar verkflæðisaðgerðir. 

#### <a name="create-a-js-file"></a>Stofnaðu .js-skrá
1. Opna Notepad eða Microsoft Visual Studio og líma eftirfarandi kóða. Vista skýrsluna sem .js-skrá Þessi kóði gerir eftirfarandi:
    - Hann felur aukalega dálka sem tengjast verkflæði, sem við bættum við áður á fartæki listasíðu. Við bættum þessum dálkum við svo að forritið hafi upplýsingar í samhengi og geti framkvæmt næsta skref.
    - Á grunni verkflæðisskrefsins sem er virkt notar það rök til að sýna aðeins þær aðgerðir.

    > [!NOTE]
    > Heiti síðnanna og annarra stýringa í kóðanum verða að vera þau sömu og heitin í vinnusvæðinu.

    ```javascript
    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

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
    ```

2.  Hlaða upp kóðaskrá á vinnusvæðið með því að velja flipann **Röklegt**
3.  Smellið á **Lokið** til að fara úr breytingarstillinigu.
4.  Smellið á **Til baka** og síðan **Lokið** til að fara af vinnusvæðinu
5.  Smelltu á **Birta vinnusvæði** til að vista verkið

### <a name="vendor-invoice-attachments"></a>Viðhengi reiknings lánardrottins

1. Smellið á hnappinn **Stillingar** (tannhjól) í efra hægra horni síðunnar og svo á **Farsímaforrit**.

2. Smellið á **Breyta** hnappinn til að hefja breytingarham í vinnusvæðið.

3. Veldu Síðuna <strong>Reikningsupplýsingar** sem þú stofnaðir áður áðan og smelltu síðan **Breyta</strong>.

4. Stilltu valkostinn **Skjalastjórnun** á **Já** eins og sýnt er hér að neðan. **Athugasemd:** Ef ekki þarf að sýna viðhengi í fartækinu er hægt að hafa þennan valkost stilltan á **Nei**, sem er sjálfgefin stilling.
   
   ![Skjalastjórnun.](./media/docmanagement-216x300.png)

5. Smellið á **Lokið** til að fara úr breytingarstillinigu.

6. Smellið á **Til baka** og síðan **Lokið** til að fara af vinnusvæðinu

7. Smelltu á **Birta vinnusvæði** til að vista verkið

### <a name="vendor-invoice-line-distributions"></a>Línudreifingar fyrir reikning lánardrottins

Kröfur fyrir þetta dæmi staðfesta að það verða aðeins dreifingar á línustigi dreifingar og að reikningur verður alltaf með aðeins eina línu. Þar sem þessar aðstæður eru einfaldar verður notendaupplifunin í fartækinu einnig að vera nógu einföld til að notandinn þurfi ekki að kafa niður nokkrum þrep til að skoða dreifingu. Lánardrottnareikningar hafa þann valkost að sýna alla skiptingu úr haus reiknings. Þessi reynsla er það sem þarf fyrir farsímaaðstæðurnar. Þess vegna munum við nota síðuna **VendMobileInvoiceAllDistributionTree** til að hanna þennan hluta farsímaaðstæðnanna. 

> [!NOTE] 
> Þegar við þekkjum kröfurnar hjálpar það okkur að ákveða hvaða tiltekna síðu á að nota og hvernig á að fínstilla notandaupplifun farsíma nákvæmlega þegar við hönnum aðstæðurnar. Í seinni aðstæðunum munum við nota aðra síðu til að sýna dreifingarnar, þar sem kröfur fyrir þær aðstæður eru aðrar.

1.  Í vefslóðinni skiptirðu út heiti valmyndaratriðis, eins og þú gerðir áður. Síðan sem birtist á líkjast eftirfarandi mynd.

    [![Síðan Allar dreifingar.](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)

2.  Opnið hönnuðinn fartæki með hnappninum **Stillingar** (tannhjól).

3.  Smellið á **Breyta** hnappinn til að hefja breytingarham í vinnusvæðið. **Athugasemd:** Þú munt sjá að tvær nýjar síður voru sjálfkrafa stofnaðar. Kerfið stofnar þessar síður þar sem kveikt var á skjalastjórnun í fyrri hluta. Þú mátt hunsa þessi nýjar síður.

4.  Smella á **Bæta við síðu**.

5.  Færa inn síðutitill, eins og **Skoða bókhald**, og lýsingu, eins og **Skoða bókhald fyrir reikning**.

6.  Smelltu á **Lokið**.

7.  Á flipanum **Svæði** er smellt á **Velja svæði**, veljið eftirfarandi svæði af dreifingasíðunni og smellið síðan á **Gert**:
    1.  Upphæð
    2.  Gjaldmiðill
    3.  Fjárhagslykill

    > [!NOTE] 
    > Við völdum ekki dálkinn **Lýsing** dálkur úr hnitaneti dreifinga, þar sem kröfur fyrir aðstæðurnar staðfestu að heildarverð er aðeins upphæðin sem dreifingar verða að vera fyrir. Þess vegna krefst notandi ekki annars svæðis til að ákvarða gerð upphæðar sem dreifingin er fyrir. Hins vegar **munum** við nota þessar upplýsingar í næstu aðstæðum, þar sem kröfur fyrir þær aðstæður tilgreina að aðrar upphæðagerðir hafi dreifingar (t.d. vsk).

8.  Smellið á **Lokið** til að fara úr breytingarstillinigu.

9.  Smellið á **Til baka** og síðan **Lokið** til að fara af vinnusvæðinu

10. Smelltu á **Birta vinnusvæði** til að vista verkið

#### <a name="adding-navigation-to-view-accounting-page"></a>Leiðsögn bætt við síðuna „Skoða bókhald“

Eins og er er fartækjasíðan **Skoða bókhald** ekki tengd við neina af þeim fartækjasíðum sem við höfum hannað hingað til. Þar sem notandinn ætti að geta flett að síðunni **Skoða bókhald** af síðunni **Upplýsingar um reikning** í fartækinu, verðum við að veita flettingar af síðunni **Upplýsingar um reikning** á síðuna **Skoða bókhald**. Við komum þessari flettingu á með því að nota viðbótar rök í gegnum JavaScript.

1.  Opnaðu .js-skrána sem þú stofnaðir áður og bættu við línum sem eru auðkenndar í eftirfarandi kóða. Þessi kóði gerir tvennt:
    1.  Hann hjálpar við að tryggja að notendur geti ekki farið beint af vinnusvæðinu á síðuna **Skoða bókhald**.
    2.  Hann kemur á flettistýringu af síðunni **Upplýsingar um reikning** á síðuna **Skoða bókhald**.

    > [!NOTE] 
    > Heiti síðnanna og annarra stýringa í kóðanum verða að vera þau sömu og heitin í vinnusvæðinu.

    ```javascript
    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
                   // Hide pages not applicable for root navigation
                   metadataService.hideNavigation('View-accounting');
                   //Link to view accounting
                   metadataService.addLink('Invoice-details', 'View-accounting', 'View-accounting-nav-control', 'View accounting', true);
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

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
    ```
    
2.  Hlaða upp skrá kóða vinnusvæðið með því að velja flipann **Röklegt** til að yfirskrifa fyrri kóða
3.  Smellið á **Lokið** til að fara úr breytingarstillinigu.
4.  Smellið á **Til baka** og síðan **Lokið** til að fara af vinnusvæðinu
5.  Smelltu á **Birta vinnusvæði** til að vista verkið

### <a name="validation"></a>Villuleit

Opnaðu forritið úr fartækinu og tengdu við tilvikið. Athugaðu að þú skráir þig inn í fyrirtæki þar sem reikningum lánardrottna eru úthlutuð til þín til skoðunar. Þú ættir að geta framkvæmt eftirfarandi aðgerðir:

-   Sjá vinnusvæðið **Mínar samþykktir**.
-   Farðu niður í vinnusvæðið **Mínar samþykktir** og sjáðu síðuna **Mínir reikningar lánardrottins**.
-   Farðu niður í vinnusvæðið **Mínar samþykktir** og sjáðu lista yfir reikninga sem var úthlutað til þín.
-   Kafa í einn af reikningunum og sjá upplýsingar um haus og línuupplýsingar.
-   Á upplýsingasíðunni sjá tengil við viðhengi og notið þennan tengil til að fara í viðhengjalista og skoða viðhengin.
-   Á upplýsingasíðunni sjá tengil við síðuna **Skoða bókhald** og notið þennan tengil til að fara á dreifingasíðuna og skoða dreifingarnar.
-   Á upplýsingasíðu, smellið á valmyndina **Aðgerðir** neðst, og framkvæma verkflæðisaðgerðir sem eiga við um skref í verkflæði.

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a>Hönnun á flóknum aðstæðum reikningssamþykkta fyrir Fabrikam
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
<td>Hvaða svæði úr reikningsfyrirsögninni mun notandi vilja sjá í farsímareynslunni og í hvaða pöntun?</td>
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
<td>Hvaða svæði úr reikningslínunum mun notandi vilja sjá í farsímareynslunni og í hvaða pöntun?</td>
<td><ol>
<li>Innkaupategund</li>
<li>Magn</li>
<li>Einingarverð</li>
<li>Nettóupphæð línu</li>
<li>Upphæð 1099</li>
</ol></td>
</tr>
<tr class="odd">
<td>Hversu margar reikningslínur eru í reikningi? Nota reglu 80-20 hér og fínstilla fyrir 80 prósent.</td>
<td>5</td>
</tr>
<tr class="even">
<td>Munu notendur vilja sjá dreifingar á fjárhagsupphæð (reikningskóðun) í fartækinu við skoðunarferlum?</td>
<td>Já</td>
</tr>
<tr class="odd">
<td>Hversu margar dreifingar á fjárhagsupphæð (heildarverð, vsk, gjöld og svo framvegis) eru fyrir reikningslínuna? Aftur skal nota 80-20 reglu.</td>
<td>Heildarverð: 2 vsk: 2 Gjöld: 2</td>
</tr>
<tr class="even">
<td>Eru reikningarnir einnig með dreifingu fjárhagsupphæða í haus reiknings? Ef svo er, ættu þessar dreifingar á fjárhagsupphæð að vera tiltækar í tækinu?</td>
<td>Ekki notað</td>
</tr>
<tr class="odd">
<td>Munu notendur vilja sjá viðhengi fyrir reikninginn í tækinu?</td>
<td>Já</td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a>Næstu skref

Eftirfarandi frávik er hægt að gera fyrir aðstæður 1, byggt á þörfum fyrir aðstæður 2. Þennan hluta má nota til að endurbæta umhverfi fartækjaforrits þíns.

1.  Þar sem fleiri línur á reikningi eru væntanlegar í dæmi 2, munu eftirfarandi breytingar á hönnuninni aðstoða við fínstillingu á notendaupplifun í fartækinu:
    1.  Í stað þess að skoða reikningslínur á upplýsingasíðu (eins og í dæmi 1), geta notendur valið að skoða línur á sérstakri farsímasíðu.
    2.  Þar sem búist er við fleiri en einni reikningslínu í þessu dæmi, ef síðan **VendMobileInvoiceAllDistributionTree** er notuð til að hanna dreifingarsíðu fyrir fartæki (eins og í dæmi 1), gæti það verið ruglandi fyrir notandann að tengja línur við dreifingar. Notið þess vegna síðuna **VendMobileInvoiceLineDistributionTree** til að hanna dreifingasíðuna.
    3.  Góð regla er að dreifing skuli sýnd í samhengi við reikningslínu í þessu dæmi. Þess vegna þarf að tryggja að notandinn geti kafað í línu til að sjá dreifingasíðuna. Notaðu tenglagetu síðunnar til að koma á köfun, rétt eins og gert var fyrir haus og upplýsingasíðurnar í dæmi 1.

2.  Þar sem búist er við fleiri en einni gerð upphæðar í dreifingu í dæmi 2 (vsk, gjöld, og svo framvegis) verður gagnlegt að sýna lýsingu á gerð upphæðar. (Þessum upplýsingum var sleppt í dæmi 1.)






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
