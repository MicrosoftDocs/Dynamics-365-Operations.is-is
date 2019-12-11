---
title: Skilgreina matsumhverfi rafrænna viðskipta
description: Þessi handbók veitir skref-fyrir-skref leiðbeiningar um útvegun og stillingu Microsoft Dynamics 365 Commerce Forskoða umhverfi.
author: v-chgri
manager: annbe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b0dce2796e69cd8dee87cba176a521c26c81eb1a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771681"
---
# <a name="configure-an-e-commerce-evaluation-environment"></a>Skilgreina matsumhverfi rafrænna viðskipta

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Þessi handbók veitir skref-fyrir-skref leiðbeiningar um útvegun og stillingu Microsoft Dynamics 365 Commerce Forskoða umhverfi. Áður en þú byrjar, mælum við með að þú rennir að minnsta kosti í gegnum fylgiskjölin til að fá hugmynd um hvað ferlið felur í sér og hvað leiðbeiningarnar innihalda.

*Athugasemd: Ef þér hefur ekki verið veittur aðgangur að Microsoft Dynamics 365 Commerce Forskoðun ennþá geturðu beðið um forsýningaraðgang af [Vefsíða viðskipta](https://aka.ms/Dynamics365CommerceWebsite).*

## <a name="summary"></a>Samantekt
Til að sjá fyrir umhverfinu með góðum árangri þarf að búa til verkefnið með tilteknu afurðarheiti og gerð. Umhverfið og Retail Cloud Scale Unit hafa einnig nokkrar sérstakar færibreytur sem þú þarft að nota til að hefja úthlutun rafrænna viðskipta síðar. Leiðbeiningarnar í þessari handbók innihalda öll nauðsynleg skref sem þú þarft að taka og breytur sem þú þarft að nota.

Eftir árangursríka úthlutun eru nokkur skref sem fylgja þarf eftir að þú þarft að taka til að undirbúa forsýningarumhverfið þitt. Sum skref eru valkvæð, eftir því hvaða þætti kerfisins þú vilt meta. Ef þú skiptir um skoðun síðar geturðu alltaf keyrt valkvæð skref síðar.

Láttu okkur vita ef þú hefur einhverjar spurningar um ráðstöfunarskrefin eða lendir í einhverjum vandræðum [Microsoft Dynamics 365 Commerce Forskoðun Yammer hópur](https://aka.ms/Dynamics365CommercePreviewYammer). 

## <a name="prerequisites"></a>Forkröfur
Eftirfarandi eru forsendur til að útvega Dynamics 365 Preview umhverfi þitt:
* Þú hefur aðgang að **Lifecycle Services-gáttinni (LCS)**
* Þú fékkst **samþykkt inn í Dynamics 365 Commerce Forskoða dagskrá**
* Þú hefur nauðsynlegar heimildir til að búa til verkefni fyrir **Væntanlegar forsölur** eða **Flytja, búa til lausnir og læra**
* Þú ert meðlimur í hlutverkinu **Umhverfisstjóri** eða **Eigandi verks** í verkinu þar sem þú verður að sjá um umhverfið
* Þú hefur stjórnandaaðgang að Azure áskriftinni þinni eða hafðu samband við áskriftarstjórann sem getur framkvæmt skrefin tvö sem krefjast stjórnunarheimilda fyrir þína hönd
* Þú hefur þitt **AAD-leigjandakenni** í boði
* Þú hefur búið til **AAD-öryggishópur** til að nota sem **kerfisstjórahóp netverslunar** og þú ert með kenni hans tiltækt
* Þú hefur búið til **AAD-öryggishóp** til að nota sem **Stjórnandahóp einkunna og umsagna** og þú ert með kenni hans tiltækt (getur verið sama SG og kerfisstjórahópurinn hér að ofan)
## <a name="provisioning-preview-environment"></a>Úthlutun á forsýningarumhverfi
Þessar leiðbeiningar ná til veitingar á Microsoft Dynamics 365 Commerce Forskoða umhverfi. Þegar þessum skrefum er lokið muntu hafa forsýningarumhverfi sem er tilbúið til stillingar. Allar þær aðgerðir sem lýst er hér fara fram í LCS-gáttinni.

*Vinsamlegast hafðu í huga að forsýningaraðgangurinn er bundinn við LCS reikninginn og stofnunina sem þú tilgreindi í forsýningarforritinu. Þú verður að nota sama reikning til að veita. Ef þú verður að nota annan LCS reikning eða leigjanda fyrir forsýningarumhverfið þarftu að veita okkur þessar upplýsingar. Fyrir upplýsingar um tengilið, vinsamlegast sjá "Viðbótarupplýsingar" hér að neðan.*
### <a name="before-starting"></a>Áður en byrjað er
##### <a name="grant-access-to-e-commerce-applications"></a>Veita aðgang að forritum með rafræn viðskipti

*Athugasemd: **Sá sem skráir sig inn þarf að vera AAD-leigjandastjórnandi**. Ef þetta skref er ekki klárað mun restin af úthlutunarskrefunum ekki takast.*

1. Fyrir þetta skref þarftu **AAD-leigjandakenni**. Þú verður að heimila rafræn viðskipti forrit til að fá aðgang að Azure áskriftinni þinni. Auðveldasta leiðin til að ná þessu er að setja saman slóð eins og þessa:

https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345

2. **Ekki smella á slóðina beint**, þess í stað skaltu afrita og líma það í vafrann þinn eða textaritil og skipta út **\{AAD_TENANT_ID\}** fyrir **AAD-leigjandakenni** áður en þú ferð á vefslóðina.
3. Þér verður kynntur Microsoft AAD innskráningargluggi þar sem þú staðfestir að þú viljir veita „Dynamics 365 Commerce (Forskoðun)“ aðgang að áskriftinni þinni.
4. Þér verður beint á síðu sem staðfestir hvort aðgerðin hafi gengið vel.

##### <a name="log-in-to-the-lcs"></a>Skráðu þig inn LCS
1. Skráðu þig inn LCS-gáttina: https://lcs.dynamics.com
1. Gakktu úr skugga um að þú sért skráð/ur inn með sama LCS reikning og þú notaðir til að biðja um aðgang að forsýningunni.
##### <a name="confirm-that-preview-features-are-available-and-enabled"></a>Staðfestu að forskoðunaraðgerðir séu tiltækar og virkar
1. Flettu alla leið til hægri á forsíðu LCS og smelltu á reitinn **Forskoðun aðgerðastjórnunar**.
1. Skrunaðu niður að „PRIVATE PREVIEW FEATURES“ og vertu viss um að eftirfarandi aðgerðir séu tiltækar og virkar:
    1. **Mat á rafrænum viðskipta**
    1. **Forritsumhverfi forskoðunar á Commerce**
1. Ef þú getur ekki séð þessa eiginleika á listanum, vinsamlegast hafðu samband við okkur með vinnupóstinum þínum, LCS reikningi og leigjandaupplýsingum. Vinsamlegast sjáðu **Viðbótarupplýsingar** hér að neðan til að fá upplýsingar um hvernig á að hafa samband við okkur.

![Stjórnun forskoðunarreits](./media/preview1.png)

![Forskoðunaraðgerðir](./media/preview2.png)
### <a name="create-project"></a>Stofna verk
##### <a name="creating-new-project"></a>Nýtt verk stofnað
1. Smelltu á **+** til að stofna nýtt verk.
1. Ef þú ert félagi skaltu velja **Flytja, búa til lausnir og læra**.
1. Veldu viðskiptavin ef þú ert viðskiptavinur **Væntanlegar forsölur**.
1. Sláðu inn nafn, lýsingu og atvinnugrein eins og þér sýnist.
1. Fyrir **Afurðaheiti**, veldu **Dynamics 365 Retail**.
1. Fyrir **Afurðaútgáfa**, veldu **Dynamics 365 Retail**.
1. Fyrir **Aðferð**, veldu **Dynamics Retail útfærsluaðferð**.
1. Þú getur flutt inn hlutverk og notendur úr fyrirliggjandi verki ef þess er óskað.
1. Smellið á **Stofna**.
1. Þér ert beint á verkefnaskjáinn.
##### <a name="add-azure-connector"></a>Bæta við Azure-tengingu
1. Ef þú ert félagi skaltu smella á **Stillingar verks** af tólareitunum lengst til hægri.
1. Ef þú ert viðskiptavinur velurðu **Stillingar verks** af efstu valmyndinni.
1. Velja **Azure-tengingar**.
1. Smelltu á **+Bæta við** til að bæta við Azure-tengingu.
1. Færið inn heiti.
1. Sláðu inn **Azure-áskriftarkenni** þitt.
1. Virkjaðu **Skilgreina að nota Azure Resource Manager (ARM)**.
1. Staðfestu að **Azure áskrift AAD leigjandaléns (eða kenni)** sé rétt. Hafðu samband við Azure áskriftarstjórann þinn, ef þörf krefur.
1. Smelltu á **Næsta**.
1. Fylgdu leiðbeiningunum á skjánum til að veita nauðsynlegum forritum aðgang að áskriftinni þinni. Hafðu samband við Azure áskriftarstjórann þinn, ef þörf krefur:
    1. Skráðu þig inn Azure-gáttina: https://portal.azure.com/
    1. Gangið úr skugga um að rétt skráasafn sé valið.
    1. Smelltu á **Áskrift** af valmyndinni vinstra megin.
    1. Finndu rétta áskrift af listanum og veldu hana. Notaðu leit ef þess er krafist.
    1. Veldu **Aðgangsstýring (IAM)** af valmyndinni.
    1. Smelltu á **Bæta við** undir **Bæta við hlutverkaúthlutun** á hægri hlið. Glugginn **Bæta við hlutverki** opnast.
    1. Fyrir **Hlutverk** velurðu **Þátttakandi**.
    1. Fyrir **Úthluta aðgangi að** skaltu hafa **Azure AD notandi, hópur eða þjónustustjóri**.
    1. Undir **Velja** slærðu inn **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.
    1. Veldu **Virkjunarþjónusta Dynamics [wsfed-enabled]** af listanum.
    1. Smellt er á **Vista**.
1. Smelltu á **Næsta**.
1. Fylgdu leiðbeiningunum á skjánum til að veita nauðsynlegum forritum aðgang að áskriftinni þinni. Hafðu samband við Azure áskriftarstjórann þinn, ef þörf krefur.
1. Smelltu á **Næsta**.
1. Fyrir **Azure-svæðið** velurðu annaðhvort **Austur-BNA**, **Austur-BNA 2**, **Vestur-BNA** eða **Vestur-BNA 2**.
1. Smelltu á **Tengja**.
1. Azure tengið þitt ætti að birtast á listanum.
### <a name="import-extension"></a>Flytja inn viðbót
1. Farðu aftur á forsíðu verksins með því að smella á heiti verksins efst.
1. Ef þú ert félagi skaltu smella á **Eignasafn** af tólareitunum lengst til hægri.
1. Ef þú ert viðskiptavinur velurðu **Eignasafn** af efstu valmyndinni.
1. Veldu **Virkjanlegur hugbúnaðarpakki** af listanum til vinstri.
1. Smelltu á **IMPORT** úr aðgerðaglugganum.
1. Veldu **Grunnviðbótin Forskoðunarsýnishorn af Commerce** af eignalistanum undir **SHARED ASSET LIBRARY**.
1. Smelltu á **Taka til**.
1. Þér verður beint aftur í Eignasafnið og þú ættir að sjá viðbótina á listanum.

![Stofnun verks - útgáfur](./media/import.png)
### <a name="deploy-environment"></a>Setja upp umhverfi

*Athugasemd: Hugsanlegt er að skref 6, 7 og/eða 8 verði ekki sýnd þar sem skjám með einum valkosti er sleppt. Þegar þú ert í **Færibreytur umhverfis** skaltu vinsamlegast staðfesta að þú hafir textann „Dynamics 365 Commerce (Forskoðun) - Demo (10.0.6 með uppfærslu verkvangs 30)" beint fyrir ofan reitinn **Heiti umhverfis**. Sjá skjámyndina hér að neðan.*

1. Veldu í efstu valmyndinni **Umhverfi í skýi**.
1. Smelltu á **+ Bæta við** til að bæta við umhverfi.
1. Fyrir **Útgáfa forrits** velurðu **10.0.6**.
1. Fyrir **Útgáfa verkvangs** velurðu **Uppfærsla verkvangs 30**.
1. Smelltu á **Næsta**.
1. Fyrir umhverfisgrannfræði velurðu **DEMO**.
1. Fyrir umhverfisgrannfræði **Dynamics 365 Commerce (Forsýning) - kynning**.
1. Ef þú stilltir upp eitt Azure tengi áður verður það notað fyrir þetta umhverfi. Ef þú stilltir upp mörgum Azure tengjum hefurðu möguleika á að velja hvaða tengi þú vilt nota: **Austur-BNA**, **Austur-BNA 2**, **Vestur-BNA** eða **Vestur-BNA 2** (mælt með besta árangri frá lokum til enda)
1. Sláðu inn **Heiti umhverfis**.
1. Stilltu VM stærðina eins og þér sýnist. (Við mælum með VM SKU **D13 v2**.)
1. Hafðu **Ítarlegar stillingar** eins og þær eru.
1. Eftir að hafa skoðað verðlagningu og leyfisskilmála á skjánum skaltu haka við reitinn til að gefa til kynna samning.
1. Smelltu á **Næsta**.
1. Á staðfestingarskjánum, eftir að hafa staðfest að upplýsingarnar séu réttar, smellirðu á **Setja upp**.
1. Þú munt fara aftur í gluggann **Umhverfi í skýi** og umhverfi þitt ætti að birtast á listanum.
1. Umbeðið umhverfi þitt birtist í biðröð og síðan er það notað. Það mun taka nokkurn tíma fyrir alla verkferla umhverfisins að ljúka, svo endilega komdu aftur eftir nokkrar klukkustundir (u.þ.b. 6 - 9 klukkustundir).
1. Áður en lengra er haldið skaltu ganga úr skugga um að staða umhverfis sé **Uppsett**.

![Stofnun verks - útgáfur](./media/project1.png)

![Stofnun verks - grannfræði 1](./media/project2.png)

![Stofnun verks - grannfræði 2](./media/project3.png)

![Stofnun verks - umhverfisbreytur](./media/project4.png)
### <a name="initialize-rcsu"></a>Frumstilla RCSU
1. Í glugganum **Umhverfi í skýi** velurðu umhverfi þitt af listanum.
1. Úr umhverfisglugganum hægra megin á skjánum smellirðu á **Nánari upplýsingar**. Umhverfisupplýsingaskjárinn birtist.
1. Undir **ENVIRONMENT FEATURES** smellirðu á **Stjórna**.
1. Af flipanum **Retail** smellirðu á **Frumstilla**. Skjár RCSU frumstillingarifæribreyta birtist.
1. Fyrir **REGION** velurðu annaðhvort **Austur-BNA**, **Austur-BNA 2**, **Vestur-BNA** eða **Vestur-BNA 2**.
1. Fyrir **VERSION** velurðu fyrst **Tilgreina útgáfu** af fellilistanum og tilgreinir síðan **9.16.19262.5** í textareitnum sem birtist hér að neðan. *Athugið: Gakktu úr skugga um að **tilgreina nákvæma útgáfu** hér til að forðast að þurfa að uppfæra RCSU seinna til að rétta útgáfu.*
1. Virkjaðu **Nota viðbót**.
1. Af listanum yfir viðbætur velurðu **Grunnviðbótin Forskoðunarsýnishorn af Commerce**.
1. Smellið á **Frumstilla**.
1. Á staðfestingarskjánum, eftir að hafa staðfest að upplýsingarnar séu réttar, smellirðu á **Já**.
1. Þér er snúið aftur á skjáinn **Smásölustjórnun** með flipann **Smásala** virkan. RCSU þinn hefur verið í biðröð vegna úthlutunar.
1. Bíddu þar til RCSU staðan þín er **SUCCESS** áður en lengra er haldið (mun taka um það bil 2 - 5 klukkustundir).
### <a name="initialize-e-commerce"></a>Frumstilla rafræn viðskipti
1. Skiptu yfir á flipann **rafræn viðskipti (forsýning)**.
1. Eftir að hafa skoðað samþykki fyrir forskoðun, smelltu á **Uppsetning**.
1. Sláðu inn nafn fyrir **nafn leigjanda rafrænna viðskipta**. Athugaðu þó að þetta verður sýnilegt í sumum slóðum sem vísa til netverslunartilviksins.
1. Fyrir **Heiti Retail Cloud Scale Unit**, veldu RCSU þinn af listanum (listi ætti aðeins að hafa einn valkost).
1. **Landafræði rafrænna viðskipta** er sjálfkrafa útfyllt og ekki er hægt að breyta.
1. Smella á **Næst** til að halda áfram.
1. Fyrir **Studd hýsilheiti**, sláðu inn gilt lén (td www.fabrikam.com).
1. Fyrir **AAD öryggishópur fyrir kerfisstjóra**, sláðu inn AAD SG auðkennið sem þú vilt nota sem kerfisstjórahópur fyrir rafræn viðskipti.
1. Fyrir **AAD öryggishópur fyrir mat og umsjón stjórnanda**, sláðu inn AAD SG auðkennið sem þú vilt nota sem hóps með mati og umsögnum.
1. Hafðu gildin **B2C** auð (7 reitir sem byrja á B2C).
1. Hafðu **Virkja einkunnir og skoðaðu þjónustu** virkt.
1. Smellið á **Frumstilla**.
1. Þér er snúið aftur á skjáinn **Smásölustjórnun** með flipann **rafræn viðskipti (forsýning)** virkan. Frumstilling rafrænna viðskipta er hafin.
1. Áður en lengra er haldið skaltu bíða þar til frumstillingarstaðan þín í netverslun er **FRUMSTILLING TÓKST**.
1. Undir **TENGLUM** neðst til hægri.
    * Athugaðu tengilinn **rafrænt viðskiptasvæði**. Þetta er hlekkurinn á rót C2 síðuna þína.
    * Athugaðu tengilinn **Stjórnunarverkfæri rafrænt viðskiptasvæði**. Þetta er hlekkurinn á vefumsjónartólið (C1 höfundatól).
## <a name="post-provisioning-steps"></a>Eftirfylgniskref
Á þessu stigi hefur umhverfinu verið úthlutað enda á milli, en enn eru stillingar skref sem þarf að gæta áður en þú getur byrjað að meta umhverfið.
### <a name="before-starting"></a>Áður en byrjað er
1. Veldu í efstu valmyndinni **Umhverfi í skýi**.
1. Veldu umhverfið af listanum.
1. Smelltu á **Nánari upplýsingar** úr umhverfisupplýsingunum til hægri.
1. Smelltu á **Skrá inn** til að opna valmynd, veldu **Skrá inn í umhverfi**.

Gakktu úr skugga um að lögaðilinn **USRT** sé valinn (efst í hægra horninu).

### <a name="configure-pos"></a>Stilla POS
##### <a name="associate-worker-with-your-identity"></a>Tengdu starfsmann við sjálfsmynd þína
1. Farðu í valmyndina til vinstri **Einingar > Retail > Starfsmenn > Starfsmenn**.
1. Í listanum skal finna og velja skrána **000713 - Andrew Colette**.
1. Í aðgerðaglugganum smellirðu á **Retail**.
1. Smelltu á **Tengja fyrirliggjandi kenni**.
1. Í reitinn **Netfang** (til hægri við **Leita með tölvupósti**), sláðu inn netfangið þitt.
1. Smellið á **Leita**.
1. Veldu skrána með nafni þínu.
1. Smellt er á **OK**.
1. Smellt er á **Vista**.
##### <a name="activate-cloud-pos"></a>Virkja sölukerfi í skýinu
1. Skráðu þig inn LCS-gáttina.
1. Flettu að verkinu þínu.
1. Veldu í efstu valmyndinni **Umhverfi í skýi**.
1. Veldu umhverfið af listanum.
1. Smelltu á **Nánari upplýsingar** úr umhverfisupplýsingunum til hægri.
1. Smelltu á **Skrá inn** til að opna valmynd, veldu **Skrá inn á sölustað í skýi**, POS ætti að hlaða sig.
1. Smelltu á **Næsta**.
1. Skrá inn með AAD-reikningni.
1. Undir **Verslunarheiti**, veldu **San Fransiskó**.
1. Smelltu á **Næsta**.
1. Undir **Skráning og tæki**, veldu **SANFRAN-1**.
1. Smellið á **Virkja**.
1. Þú ættir að vera skráð/ur út og enda á POS innskráningarskjánum.
1. Þú getur nú skráð þig inn á Cloud POS reynsluna með kenni rekstraraðila **000713** og lykilorð **123**.
### <a name="site-setup"></a>Uppsetning svæðis
1. Skráðu þig inn á **tól til að stjórna vefnum** með því að nota slóðina sem þú bentir á áðan.
1. Smelltu á svæðið **Fabrikam** til að opna uppsetningarglugga svæðisins.
1. Veldu lénið sem þú slóst inn áður þegar rafræn viðskipti voru frumstillt.
1. Veldu sjálfgefna rás **Fabrikam útvíkkuð netverslun**. *Athugasemd: Gakktu úr skugga um að þú veljir **framlengdur** netverslun*
1. Veldu sjálfgefið tungumál **en-us**.
1. Hafðu **Slóð** eins og það er.
1. Smellt er á **OK**.
1. Þú verður sendur á síðulistann á svæðinu.
### <a name="enable-jobs"></a>Virkja vinnslur
1. Skráðu þig inn í umhverfið (HQ).
1. Farðu í valmyndina til vinstri **Retail > Fyrirspurnir og skýrslur> Runuvinnslur**.
1. Framkvæmdu eftirfarandi skref fyrir sérhverja af vinnslunum á listanum að neðan:
    * **Vinna úr tilkynningartölvupósti smásölupöntunar**.
    * **Tiltækar afurðir**.
    * **P-0001**.
    * **Samstilla pantanavinnslu**.
1. Notaðu hraðsíuna til að leita að vinnslunni með því að nota nafn hennar (talin upp hér að ofan).
1. Ef staða vinnslunnar er **Halda eftir**, framkvæma eftirfarandi skref:
    1. Veldu skrána.
    1. Úr aðgerðarglugganum opnarðu **Runuvinnslu**-borðann og smellir á **Breyta stöðu**.
    1. Veldu **Bíður** og smelltu á **Í lagi**.
### <a name="run-full-data-sync"></a>Keyra fulla samstillingu gagna
1. Með valmyndinni til vinstri ferðu í **Einingar > Retail > Uppsetning höfuðstöðva > Smásöluáætlunarbúnaður > Rásagagnagrunnur**.
1. **Sjálfgefin** rás er valin af listanum til vinstri. *Veldu hina rásina sem til er (nefnd **scXXXXXXXXX**)*.
1. Smelltu á **Samstilling allra gagna** úr aðgerðarglugganum.
1. Skráðu **9999** sem dreifingaráætlun.
1. Smellt er á **OK**.
1. Smellt er á **OK**.
### <a name="after-these-steps-you-are-ready-to-start-evaluating-your-preview-environment"></a>Eftir þessi skref ertu tilbúin/n að meta forsýningarumhverfið þitt!
Notaðu slóðina **stjórnunartæki fyrir netverslun** til að skoða C1 höfundarreynsluna og slóðina **rafrænt viðskiptasvæði** til að skoða C2 vefsvæðið.

## <a name="additional-resources"></a>Frekari upplýsingar
### <a name="how-to-find-your-aad-tenant-id"></a>Hvernig á að finna AAD leigjandaauðkenni þitt
AAD leigjandaauðkenni er GUID og lítur út eins og þetta dæmi: **72f988bf-86f1-41af-91ab-2d7cd011db47**
##### <a name="from-azure-portal"></a>Úr Azure-gátt
1. Skráðu þig inn Azure-gáttina: https://portal.azure.com/
1. Gangið úr skugga um að rétt skráasafn sé valið.
1. Smelltu á **Azure Active Directory** úr valmyndinni vinstra megin.
1. Veldu **Eiginleikar** undir **Stjórna**.
1. AAD leigjandaauðkenni er sýnt undir **Skráasafnskenni**.
##### <a name="from-openid-connect-metadata"></a>Frá OpenID Connect lýsigögnum
Búa til **OpenID slóð** með því að skipta út **\{YOUR_DOMAIN\}** með léninu þínu, t.d. microsoft.com: https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration myndi verða https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration

1. Flettu að **OpenID slóð** með lénið þitt í því.
1. AAD leigjandaauðkenni má sjá í mörgum eiginleikagildum.
1. Finndu **authorization_endpoint** og dragðu GUID út beint eftir **login.microsoftonline.com/**.
### <a name="how-to-find-the-id-of-your-aad-security-group"></a>Hvernig á að finna kenni AAD öryggishópsins þíns
AAD kenni öryggishóps er GUID og lítur út eins og þetta dæmi: **436ea7f5-ee6c-40c1-9f08-825c5811066a**

Þetta skref gerir ráð fyrir að notandinn sé meðlimur í hópnum sem hann er að reyna að finna kenni fyrir.
1. Flettu til línuritsins: https://developer.microsoft.com/en-us/graph/graph-explorer#
1. Smelltu á **Skráðu inn með Microsoft** og skráðu þig inn með persónuskilríkjum þínum.
1. Eftir að hafa skráð þig inn smellirðu á **sýna fleiri sýni** frá vinstri.
1. Virkja **Hópar** úr hægri glugganum.
1. Lokaðu hægri glugganum.
1. Smelltu á **alla hópa sem ég tilheyri**.
1. Finndu hópinn þinn í textareitnum **Forskoðun svara**.
1. Auðkenni öryggishóps er tekið fram undir eiginleikanum **kenni**.
### <a name="test-credit-card-information-to-perform-test-purchases"></a>Prófaðu kreditkortaupplýsingar til að framkvæma prófakaup
Til að framkvæma prófunarviðskipti á vefnum geturðu notað þessar prófkreditkortaupplýsingar:

Kortanúmer: 4111-1111-1111-1111, gildistími: 10/20, CVV: 737

*Athugið: Þú ættir ekki að reyna að nota raunverulegar kreditkortaupplýsingar á prófunarstaðnum undir neinum kringumstæðum!*
### <a name="useful-links"></a>Gagnlegir tenglar
* [LCS (Lifecycle Services)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)
* [RCSU (Retail Cloud Scale Unit)](https://docs.microsoft.com/en-us/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)
* [Microsoft Azure-gátt](https://azure.microsoft.com/en-us/features/azure-portal)
* [Dynamics 365 Commerce vefsvæði](https://aka.ms/Dynamics365CommerceWebsite)
* [Hjálpartilföng fyrir Dynamics 365 Retail](../retail/index.md)
### <a name="microsoft-dynamics-365-commerce-preview-support"></a>Stuðningurinn Microsoft Dynamics 365 Commerce Forskoðun
Ef þú lendir í vandræðum meðan þú gerir úthlutunarskrefin skaltu fara á [Microsoft Dynamics 365 Commerce Forskoðun Yammer hópur](https://aka.ms/Dynamics365CommercePreviewYammer) fyrir aðstoð. 

Ef þú ert í vandræðum með aðgang að Yammer-hóp geturðu líka náð til okkar með tölvupósti á **Dynamics365Commerce@microsoft.com**. Ekki er fylgst með þessu netfangi með virkum hætti svo búist við seinkun á svari.
***
## <a name="prerequisites-for-optional-features"></a>Forsendur fyrir valfrjálsa eiginleika
Ef þú vilt meta viðskipti tölvupóstsaðgerða verður að uppfylla eftirfarandi forsendur:
* Þú ert með tölvupóst netþjón (SMTP miðlara) sem hægt er að nota úr Azure áskrift þar sem þú útvegar forsýningarumhverfið.
* Þú ert með FQDN/IP netþjóninn, SMTP-gáttarnúmer og staðfestingu upplýsingar tiltækar.

Ef þú vilt meta stafrænan eignastýringu, taka sérstaklega inn nýjar myndir um rásina, verður að uppfylla eftirfarandi forsendur:
* Þú þarft að hafa þitt **Nafn leigjanda CMS** laust. Leiðbeiningar til að finna þetta nafn eru hér að neðan.
### <a name="configure-image-backend-optional"></a>Stilla bakvinnslu myndar (valfrjálst)
##### <a name="finding-your-media-base-url"></a>Finndu grunnvefslóð miðla
*Athugasemd: Áður en þú getur klárað þetta skref verður þú að ljúka **Svæðisuppsetning**.*
1. Skráðu þig inn á tól til að stjórna vefnum með því að nota slóðina sem þú bentir á áðan.
1. Opnið svæðið **Fabrikam**.
1. Veldu á **Eignir** af valmyndinni vinstra megin.
1. Veldu einhverja staka myndeign.
1. Finndu **Opinber slóð** frá eiginleikaeftirlitsmanninum til hægri. Það er með slóð í sér.
    * Dæmi um slóð: https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC
1. Skiptu út síðasta auðkenni í slóðinni (MA1nQC í dæminu URL hér að ofan) með eftirfarandi streng: **search?fileName=**
    * Dæmi um slóð eftir skipti: https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=
    * Þetta er þitt **Grunnslóð miðla** - skrifaðu það niður.
##### <a name="updating-the-media-base-url"></a>Uppfærsla á grunnvefslóð miðla
1. Skráðu þig inn í umhverfið (HQ).
1. Með valmyndinni til vinstri ferðu í **Einingar > Retail > Uppsetning rásar > Rásaforstillingar**.
1. Smellið á **Breyta**.
1. Úr **Forstillingareiginleikar** skiptirðu út eiginleikagildi fyrir **Grunnvefslóð miðlaþjóns** með **Grunnvefslóð miðla** sem þú bjóst til áður.
1. Veldu aðra rás af listanum til vinstri, undir rásinni **Sjálfgefið**.
1. Undir **Forstillingareiginleikar** smellirðu á **+ Bæta við**.
1. Fyrir eiginleikann sem bætt var við velurðu **Grunnvefslóð miðla** sem eiginleikalykil og fyrir eiginleikagildi slærðu inn **Grunnvefslóð miðla** sem þú bjóst til áður.
1. Smellt er á **Vista**.

### <a name="configure-email-server-optional"></a>Stilla tölvupóstþjón (valfrjálst)
Vinsamlegast hafðu í huga að SMTP miðlarinn eða tölvupóstþjónustan sem þú slærð inn hér verður að vera aðgengileg innan Azure áskriftarinnar sem þú notar fyrir umhverfið.
1. Skráðu þig inn í umhverfið (HQ).
1. Með valmyndinni til vinstri ferðu í **Einingar > Retail > Uppsetning höfuðstöðva > Færibreytur > Tölvupóstfæribreytur**.
1. Smellið á flipann **SMTP-stillingar**.
1. Í reitnum **Þjónn fyrir sendan póst**, sláðu inn FQDN eða IP tölu SMTP netþjónsins eða tölvupóstþjónustunnar.
1. Í reitinn **SMTP gáttarnúmer** slærðu inn gáttarnúmerið (sjálfgefið er 25 þegar SSL er ekki notað).
1. Í reitinn **Notandanafn** slærðu inn gildi (ef staðfesting er nauðsynleg).
1. Í reitinn **Aðgangsorð** slærðu inn gildi (ef staðfesting er nauðsynleg).
1. Smellt er á **Vista**.
1. Smellið á **Endurnýja**.
1. Smelltu á flipann **Prufa tölvupóst**.
1. Veldu í reitinn Netþjónustufyrirtæki **SMTP**.
1. Í reitinn **Senda til** slærðu inn netfangið þar sem þú vilt að prufupóstfangið verði afhent.
1. Smelltu á **Senda prufupóst**.
### <a name="configure-email-templates-optional"></a>Stilla tölvupóstsniðmát (valfrjálst)
Uppfæra þarf tölvupóstsniðmátið fyrir hvern viðskiptaviðburð sem þú vilt senda tölvupóst með giltu netfang sendanda.
1. Með valmyndinni til vinstri ferðu í **Einingar > Fyrirtækisstjórnun > Uppsetning > Sniðmát tölvupósts fyrirtækis**.
1. Smelltu á **Sýna lista**.
1. Fyrir hvert sniðmát á listanum:
    1. Í reitinn **Netfang sendanda** slærðu inn netfang sendanda fyrir þetta tölvupóstsniðmát.
    1. (Valfrjálst) Í reitinn **Nafn sendanda** slærðu inn nafn sem verður notað sem sendandi fyrir þetta tölvupóstsniðmát.
1. Smellt er á **Vista**.
### <a name="customizing-email-templates-optional"></a>Sérsnið á tölvupóstsniðmátum (valfrjálst)
Þú gætir viljað aðlaga tölvupóstsniðmátin til að nota mismunandi myndir eða uppfæra krækjurnar í sniðmátinu til að tengjast aftur í forsýningarumhverfið. Skrefin hér að neðan útskýra hvernig á að hala niður sjálfgefnu sniðmátunum, aðlaga þau og uppfæra sniðmátin í kerfinu.
1. Hlaðið niður með vafra [Microsoft Dynamics 365 Commerce Forskoða sjálfgefið tölvupóstsniðmát.zip-skrá](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) sem inniheldur eftirfarandi HTML skjöl í tölvunni þinni.
    1. Eining pöntunarsniðmáts
    1. Gefa út sniðmát gjafakorts
    1. Nýtt pöntunarsniðmát
    1. Umbúðapöntunarsniðmát
    1. Tiltektarpöntunarsniðmát
1. Sérsniðið sniðmátin með texta- eða HTML ritstjóra. Vinsamlegast sjáðu lista yfir studd tákn hér að neðan.
1. Skráðu þig inn í umhverfið (HQ).
1. Með valmyndinni til vinstri ferðu í **Einingar > Retail > Uppsetning höfuðstöðva > Færibreytur > Sniðmát tölvupósts fyrirtækis**.
1. Stækkaðu listann vinstra megin til að sjá öll sniðmát.
1. Framkvæmdu eftirfarandi skref fyrir hvert sniðmát sem þú vilt aðlaga:
    1. Veldu sniðmátið úr listanum.
    1. Undir **Innihald tölvupóstskilaboða** velurðu viðeigandi tungumálarútgáfu af listanum (sjálfgefið **en-us**).
    1. Undir **Innihald tölvupóstskilaboða** smellirðu á **Breyta**, þú ættir að sjá gluggann **Hlaða upp sniðmáti fyrir tölvupóst** opnast.
    1. Smelltu á **Fletta** og finndu HTML skjalið með sérsniðnu innihaldi.
    1. Smelltu á **Hlaða upp**, sniðmátið þitt er hlaðið inn í kerfið og forsýning birtist.
    1. Smellt er á **OK**.
    1. (Valfrjálst) Sérsníddu eiginleikann **Efni** í sniðmátinu.
    1. Smellt er á **Vista**.

#### <a name="supported-tokens-in-the-email-template"></a>Studd tákn í tölvupóstsniðmátinu
Þessum táknum verður skipt út þegar tölvupóstur er gefinn út fyrir raunveruleg gildi sem eiga við viðskiptavini og pöntun þeirra.

**Sölupöntun** - Eftirfarandi tákn eiga við um heildarsölupöntunina.

|Heiti táknsins|Tákn|
|---|---|
|Pöntunarnúmer|%salesid%|
|Nafn viðskiptavinar|%customername%|
|Afh.aðsetur|%deliveryaddress%|
|Póstfang greiðanda|%customeraddress%|
|Pöntunardagsetning|%shipdate%|
|Afhendingarmáti|%modeofdelivery%|
|Afsláttur|%discount%|
|Virðisaukaskattur|%tax%|
|Heildarupphæð pöntunar|%total%|

**Sölulína** - Eftirfarandi tákn eru byggð fyrir hverja vöru í röðinni.

*Athugasemd: Settu táknin **Vörulisti - byrja** og **Vörulisti - lok** í byrjun og lok HTML blokkar sem endurtekur fyrir hverja vöru.*

|Heiti táknsins|Tákn|
|---|---|
|Afurðalisti - hefja|\<!--%tablebegin.salesline% -->|
|Afurðalisti - lok|\<!--%tableend.salesline%-->|
|Afurðarnafn|%lineproductname%|
|Lýsing|%lineproductdescription%|
|Magn|%linequantity%|
|Einingaverð línu|%lineprice% (staðfesta)|
|Heildarfjöldi línuatriða|%linenetamount%|
|línuafsláttur|%linediscount%|
|Sendingardagsetning|%lineshipdate%|
|Innkaupaaðferð|%linedeliverymode%|
|afhendingaraðsetur|%linedeliveryaddress%|
|Sölueining línunnar|%lineunit%|

