---
title: Almenn úrræðaleit
description: Þessi grein veitir almennar upplýsingar um bilanaleit fyrir tvískrifa samþættingu milli fjármála- og rekstrarforrita og Dataverse.
author: RamaKrishnamoorthy
ms.date: 04/18/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2f263e331d23ce0ddf60a4abc2467513aa342445
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/02/2022
ms.locfileid: "9112365"
---
# <a name="general-troubleshooting"></a>Almenn úrræðaleit

[!include [banner](../../includes/banner.md)]



Þessi grein veitir almennar upplýsingar um bilanaleit fyrir tvískrifa samþættingu milli fjármála- og rekstrarforrita og Dataverse.

> [!IMPORTANT]
> Sum vandamálin sem þessi grein fjallar um gætu þurft annað hvort kerfisstjórahlutverkið eða Microsoft Azure Active Directory (Azure AD) leigjanda stjórnanda skilríki. Hlutinn fyrir hvert vandamál útskýrir hvort krafist sé sérstaks hlutverks eða skilríkja.

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>Virkið og skoðið rakningarkladda viðbóta í Dataverse til að skoða upplýsingar um villu

Rekjaskrár geta verið gagnlegar þegar bilanaleit eru tvískrifuð samstillingarvandamál milli Finance & Operations og Dataverse. Logarnir geta veitt sérstakar upplýsingar til teymanna sem veita tæknilega og verkfræðilega aðstoð fyrir Dynamics 365. Þessi grein fjallar um hvernig á að virkja rekja annála og hvernig á að skoða þá. Rekjaskrám er stjórnað á Dynamics 365 Stillingar síðunni og krefjast réttindi stjórnandastigs til að breyta og skoða. 

**Nauðsynlegt hlutverk til að kveikja á rakningarkladda og skoða villur:** Kerfisstjóri

### <a name="turn-on-the-trace-log"></a>Kveiktu á rekjaskránni
Fylgdu þessum skrefum til að kveikja á rakningarkladda.

1.  Skráðu þig inn á Dynamics 365 og veldu síðan **Stillingar** í efstu yfirlitsstikunni. Á Systems síðunni, smelltu **Stjórnsýsla**.
2.  Á stjórnunarsíðunni smellirðu á **Kerfisstillingar**.
3.  Veldu **Sérsniðin** flipa og viðbætur, og síðan í hlutanum fyrir sérsniðna vinnuflæðisvirkni, breyttu fellilistanum í **Allt**. Þetta mun rekja alla starfsemi og veita alhliða gagnasett fyrir teymin sem verða að fara yfir hugsanleg vandamál.

> [!NOTE]
> Stillir fellilistann á **Undantekning** mun aðeins veita rakningarupplýsingar þegar undantekningar (villur) eiga sér stað.

Þegar kveikt hefur verið á þeim verður rekjaskrám viðbótanna safnað áfram þar til slökkt er handvirkt á þeim með því að fara aftur á þennan stað og velja **Af**.

### <a name="view-the-trace-log"></a>Skoðaðu rekjaskrána
Fylgdu þessum skrefum til að skoða rakningarkladdann.

1. Á Dynamics 365 Settings síðunni velurðu **Stillingar** í efstu yfirlitsstikunni. 
2. Veldu **Viðbót sporaskrá** í **Sérstillingar** hluta síðunnar.
3. Þú getur fundið færslur í listanum yfir rekjaskrár, byggt á tegundarheiti og/eða heiti skilaboða.
4. Opnaðu viðkomandi færslu til að skoða heildarskrána. Skilaboðablokkin í framkvæmd hlutanum mun veita tiltækar upplýsingar um viðbótina. Ef þær eru tiltækar verða upplýsingar um undantekningar einnig veittar. 

Þú getur afritað innihald rakningarskránna og límt það inn í annað forrit eins og Notepad eða önnur verkfæri til að skoða annála eða textaskrár til að sjá allt innihald á auðveldan hátt. 

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>Virkjaðu villuleitarstillingu til að leysa vandamál í beinni samstillingu í fjármála- og rekstrarforritum

**Nauðsynlegt hlutverk til að skoða villurnar:** Kerfisstjóri

Tvöfalt skrif villur sem eiga uppruna sinn í Dataverse getur birst í fjármála- og rekstrarappinu. Til að virkja fjölorða skráningu fyrir villurnar skal fylgja þessum skrefum:

1. Fyrir allar verkefnastillingar í fjármála- og rekstrarappi er fáni **IsDebugMode** á **DualWriteProjectConfiguration** borð.
2. Opnaðu **DualWriteProjectConfiguration** með Excel-innbótinni. Til að nota viðbótina skaltu virkja hönnunarham í Excel-viðbótinni fyrir fjármál og rekstrar og bæta við **DualWriteProjectConfiguration** að blaðinu. Frekari upplýsingar er að finna í [Skoða og uppfæra einingagögn með Excel](../../office-integration/use-excel-add-in.md).
3. Stilltu **IsDebugMode** á **Já** í verkinu.
4. Keyrðu atburðarásina sem er að búa til villur.
5. Fjölorða kladdar eru geymdir í töflunni **DualWriteErrorLog**.
6. Til að fletta upp gögnum á töfluvafra skal nota eftirfarandi tengil: `https://999aos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`, sem kemur í staðinn fyrir `999` eftir þörfum.
7. Uppfærðu aftur eftir [KB 4595434](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=98e5dc124ac125c57ad633d885ac612aea3ddb8f4abf9d71ab3aa354f2e06cbe) sem er í boði fyrir uppfærslur á verkvangi 37 og síðar. Ef þú ert með þessa lagfæringu uppsetta þá sækir kembistillingin fleiri kladda.  

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Athugaðu samstillingarvillur á sýndarvélinni fyrir fjármála- og rekstrarappið

**Nauðsynlegt hlutverk til að skoða villurnar:** Kerfisstjóri

1. Skráðu þig inn í Microsoft Dynamics Lifecycle Services (LCS).
2. Opnaðu LCS-verkið sem þú valdir til að gera tvískriftaprófun fyrir.
3. Veldu reitinn **Umhverfi í skýi**.
4. Notaðu Remote Desktop til að skrá þig inn á sýndarvélina (VM) fyrir fjármála- og rekstrarappið. Notaðu staðbundna reikninginn sem er sýndur í LCS.
5. Opnaðu tilvikayfirlit.
6. Veldu **Forrit og þjónustukladdar \> Microsoft \> Dynamics \> AX -DualWriteSync \> Virkt**.
7. Farðu yfir listann yfir nýlegar villur.

## <a name="dual-write-ui-landing-page-showing-blank"></a>Tvöfalt skrifa UI áfangasíða sem sýnir auð
Þegar þú opnar tvískrifa síðuna í Microsoft Edge eða Google Chrome vafra, heimasíðan hleðst ekki og þú sérð auða síðu eða villu eins og „Eitthvað fór úrskeiðis“.
Í Devtools sérðu villu í stjórnborðsskránum:

>bundle.eed39124e62c58ef34d2.js:37 DOMException: Mistókst að lesa 'sessionStorage' eignina úr 'Window': Aðgangi er hafnað fyrir þetta skjal. á t.storeInSessionStorage (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:16:136860) á nýju t (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:69:20103) á ci (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:44115) hjá Eo (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:58728) hjá jo (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:65191) á Nr (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:84692) á Eða (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:85076) hjá Ss (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:91750) á vs (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:91130) á hs (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:90151)

Notendaviðmótið notar „lotugeymslu“ vafra til að geyma nokkur eignagildi til að hlaða heimasíðunni. Til að þetta virki þurfa vafrakökur frá þriðja aðila að vera leyfðar í vafra síðunnar. Villan er til marks um að notendaviðmótið hafi ekki aðgang að lotugeymslunni. Það geta verið tvær aðstæður þar sem þetta vandamál kemur upp:

1.  Þú ert að opna notendaviðmótið í huliðsstillingu Edge/Chrome og þriðju aðila kökur í huliðsstillingu eru læstar.
2.  Þú hefur algjörlega lokað á kökur þriðja aðila í Edge/Chrome.

### <a name="mitigation"></a>Mildun
Vefkökur þriðju aðila þurfa að vera leyfðar í stillingum vafra.

### <a name="google-chrome-browser"></a>Google Chrome vafri
1. valkostur:
1.  Farðu í stillingar með því að slá inn chrome://settings/ í veffangastikunni og farðu síðan í Privacy and Security -> Cookies and other site data.
2.  Veldu 'Leyfa allar vafrakökur'. Ef þú vilt ekki gera þetta skaltu fara í seinni valkostinn.

2. kostur:
1.  Farðu í stillingar með því að slá inn chrome://settings/ í veffangastikunni og farðu síðan í Privacy and Security -> Cookies and other site data.
2.  Ef 'Loka á vafrakökur frá þriðja aðila í huliðsstillingu' eða 'Loka á vafrakökur frá þriðja aðila' er valið, farðu í 'Síður sem geta alltaf notað vafrakökur' og smelltu á **Bæta við**. 
3.  Bættu við heiti vefsvæðis fyrir fjármála- og rekstrarappa -https://<your_FinOp_instance>.cloudax.dynamics.com. Gakktu úr skugga um að þú veljir gátreitinn fyrir "Allar vafrakökur, aðeins á þessari síðu". 

### <a name="microsoft-edge-browser"></a>Microsoft Edge vafra
1.  Farðu í Stillingar -> Heimildir vefsvæðis -> Vafrakökur og vefgögn.
2.  Slökktu á „Loka á kökur frá þriðja aðila“.  

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a>Aftengdu og tengdu annað Dataverse umhverfi frá fjármála- og rekstrarappi

**Áskilið hlutverk til að aftengja umhverfið:** Kerfisstjóri fyrir annað hvort fjármála- og rekstrarapp eða Dataverse.

1. Skráðu þig inn á fjármála- og rekstrarappið.
2. Farðu í **Vinnusvæði \> Gagnastjórnun** og veldu reitinn **Tvöfalt skrif**.
3. Veldu allar keyrandi kortlagningar og veldu síðan **Hætta**.
4. Veldu **Aftengja umhverfi**.
5. Veldu **Já** til að staðfesta aðgerðina.

Þú getur nú tengt nýtt umhverfi.

## <a name="unable-to-view-the-sales-order-line-information-form"></a>Ekki er hægt að skoða Upplýsingar sölupöntunarlínu 

Þegar búin er til sölupöntun í Dynamics 365 Sales og smellt er á **+ Bæta við afurðum** kanntu að fara á eyðublað Dynamics 365 Project Operations pöntunarlínu. Ekki er hægt að skoða **Upplýsingar** sölupöntunarlínu úr þeirri skjámynd. Valkosturinn fyrir **Upplýsingar** birtist ekki í fellivalmyndinni fyrir neðan **Ný pöntunarlína**. Þetta gerist vegna þess að Project Operations hefur verið sett upp í umhverfi þínu.

Fylgdu þessum skrefum til að gera virkja valkostinn **Upplýsingar** aftur:

1. Fara í töfluna **Pöntunarlína**.
2. Finndu **Upplýsingar** undir skjámyndum.
3. Veldu **Upplýsingar** og smelltu á **Virkja öryggishlutverk**.
4. Breyttu öryggisstillingunni í **Sýna öllum**.

## <a name="how-to-ensure-data-integration-is-using-the-most-current-finance-and-operations-schema"></a>Hvernig á að tryggja að gagnasamþætting sé með nýjustu fjármála- og rekstraráætlunum

Þú gætir lent í gagnavandamálum við samþættingu gagna ef ekki er verið að nota nýjasta skemað. Eftirfarandi skref munu hjálpa þér að endurnýja aðilalistann í fjármála- og rekstrarforritum og einingarnar í gagnasamþættingunni.

### <a name="refresh-entity-list-in-finance-and-operations-environment"></a>Uppfærðu aðilalista í fjármála- og rekstrarumhverfi
1.  Skráðu þig inn í fjármála- og rekstrarumhverfið þitt.
2.  Veldu **Gagnastjórnun**.
3.  Inni í Gagnastjórnun, veldu **Rammabreytur**.
4.  Á **Gagnainnflutningur/útflutningur rammafæribreytur** síðu, veldu **Einingastillingar** flipann og veldu **Endurnýja einingarlista**. Þetta getur tekið meira en 30 mínútur að endurnýja, allt eftir fjölda aðila sem taka þátt.
5.  Siglaðu til **Gagnastjórnun** og veldu **Gagnaeiningar** til að sannreyna að væntanlegir aðilar séu skráðir. Ef væntanlegar einingar eru ekki skráðar, staðfestu að einingarnar komi fram í fjármála- og rekstrarumhverfi þínu og endurheimtu þær einingar sem vantar, eftir þörfum.

#### <a name="if-the-refresh-fails-to-resolve-the-issue-delete-and-re-add-the-entities"></a>Ef endurnýjunin tekst ekki að leysa vandamálið skaltu eyða og bæta við einingunum aftur

> [!NOTE]
> Þú gætir þurft að stöðva vinnsluhópa sem eru virkir að nota einingarnar áður en þeim er eytt.

1.  Veldu **Gagnastjórnun** í þínu fjármála- og rekstrarumhverfi og veldu **Gagnaeiningar**.
2.  Leitaðu að aðilum sem eiga í vandræðum og skráðu markeininguna, sviðsetningartöfluna, heiti einingar og aðrar stillingar. Eyddu einingunni eða einingunum af listanum.
3.  Veldu **Nýtt** og bættu einingunni eða einingunum við aftur með því að nota gögnin frá skrefi 2. 

#### <a name="refresh-entities-in-data-integrator"></a>Endurnýjaðu einingar í Data integrator
Skráðu þig inn á Power Platform Stjórnunarmiðstöð og veldu **Samþætting gagna**. Opnaðu verkefnið þar sem vandamálin eiga sér stað og veldu **Endurnýja einingar**.

## <a name="how-to-enable-and-save-network-trace-so-that-traces-can-be-attached-to-support-tickets"></a>Hvernig á að virkja og vista netrakningu þannig að hægt verði að hengja rakningar við þjónustubeiðni

Þjónustudeildin gæti þurft að fara yfir netrakningar til að  úrræðaleita sum vandamál. Til að búa til netrakningu skal fylgja þessum skrefum:

### <a name="google-chrome-browser"></a>Google Chrome vafri

1. Í opna flipanum skal ýta á **F12** eða velja **Verkfæri þróunaraðila** til að opna verkfæri þróunaraðila.
2. Opnaðu flipann **Netkerfi** og sláðu inn **integ** í textasíureitinn.
3. Keyrðu aðstæðurnar og fylgstu með beiðnunum sem eru skráðar inn.
4. Hægrismelltu á færslurnar og veldu **Vista allt sem HAR með efni**.

### <a name="microsoft-edge-browser"></a>Microsoft Edge vafra

1. Í opna flipanum skal ýta á **F12** eða velja **Verkfæri þróunaraðila** til að opna verkfæri þróunaraðila.
2. Opnaðu flipann **Netkerfi**.
3. Keyrðu aðstæðurnar.
4. Veldu **vista** til að flytja út niðurstöður sem HAR.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

