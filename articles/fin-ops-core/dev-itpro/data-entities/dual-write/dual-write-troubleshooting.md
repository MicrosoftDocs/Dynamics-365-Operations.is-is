---
title: Almenn úrræðaleit
description: Þessi grein veitir upplýsingar um almenna úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita fjármála- og reksturs og Dataverse.
author: RamaKrishnamoorthy
ms.date: 04/18/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: be3d72063ac18b9abea77d5aec6e230b0c930ae6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289361"
---
# <a name="general-troubleshooting"></a>Almenn úrræðaleit

[!include [banner](../../includes/banner.md)]



Þessi grein veitir upplýsingar um almenna úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita fjármála- og reksturs og Dataverse.

> [!IMPORTANT]
> Nokkur þeirra atriða sem þessi grein fjallar um geta krafist annað hvort kerfisstjórans eða Microsoft Azure Active Directory (Azure AD) Leyfisupplýsingar leigjanda. Hlutinn fyrir hvert vandamál útskýrir hvort krafist sé sérstaks hlutverks eða skilríkja.

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>Virkið og skoðið rakningarkladda viðbóta í Dataverse til að skoða upplýsingar um villu

Rakningarkladdar geta verið gagnlegir þegar gerð er úrræðaleit á samstillingarvandamáli varðandi keyrslu tvöfaldrar skráningar á milli fjármála- og reksturs og Dataverse. Kladdarnir geta gefið ákveðnar upplýsingar til teymisins sem veitir tæknilega og hönnunarlega aðstoð fyrir Dynamics 365. Þessi grein fjallar um hvernig á að virkja rakningarkladda og hvernig á að skoða þá. Rakningarklöddum er stjórnað á stillingasíðu Dynamics 365 og krefst réttinda á stjórnunarstigi til að breyta og skoða. 

**Nauðsynlegt hlutverk til að kveikja á rakningarkladda og skoða villur:** Kerfisstjóri

### <a name="turn-on-the-trace-log"></a>Kveikja á rakningarkladda
Fylgdu þessum skrefum til að kveikja á rakningarkladda.

1.  Skráðu þig inn í Dynamics 365 og veldu síðan **Stillingar** á efstu yfirlitsstikunni. Á síðunni Kerfi er smellt á **Stjórnun**.
2.  Á síðunni Stjórnun skal velja **Kerfisstillingar**.
3.  Veldu flipann **Sérstilling** og viðbót og síðan í rakningarhluta sérsniðinnar verkflæðisaðgerðar skal breyta fellilistanum í **Allt**. Þetta mun rekja allar aðgerðir og veitir ítarlegt gagnasafn fyrir teymin sem verða að yfirfara hugsanleg vandamál.

> [!NOTE]
> Að stilla fellilistann á **Undantekning** mun aðeins veita rakningarupplýsingar þegar undantekningar (villur) koma upp.

Þegar það hefur verið virkjað verður haldið áfram að safna rakningarklöddum viðbótar þar til slökkt verður á þeim handvirkt með því að fara aftur á þessa staðsetningu og velja **Slökkva**.

### <a name="view-the-trace-log"></a>Skoða rakningarkladdann
Fylgdu þessum skrefum til að skoða rakningarkladdann.

1. Á stillingasíðu Dynamics 365 skal velja **Stillingar** á efstu yfirlitsstikunni. 
2. Veldu **Viðbót rakningarkladda** í hlutanum **Sérstillingar** á síðunni.
3. Hægt er að finna færslur í listanum yfir rakningarkladda út frá heiti tegundar og/eða heiti skilaboða.
4. Opna viðkomandi færslu til að skoða allan kladdann. Skilaboðablokkin í keyrsluhlutanum mun bjóða upp á tiltækar upplýsingar fyrir viðbótina. Einnig verða veittar upplýsingar um undantekningar ef þær eru fyrir hendi. 

Hægt er að afrita efni rakningarkladda og líma það í annað forrit eins og Notepad eða önnur verkfæri til að skoða kladda eða textaskrár til að sjá allt efnið á auðveldari hátt. 

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>Kveiktu á kembiforriti til að leysa vandamál samstillingar í beinni í forritum fjármála- og reksturs

**Nauðsynlegt hlutverk til að skoða villurnar:** Kerfisstjóri

Villur tvöfaldrar skráningar sem koma úr Dataverse geta birst í forriti fjármála- og reksturs. Til að virkja fjölorða skráningu fyrir villurnar skal fylgja þessum skrefum:

1. Fyrir allar skilgreiningar verks í forriti fjármála- og reksturs er flagg **IsDebugMode** í töflunni **DualWriteProjectConfiguration**.
2. Opnaðu **DualWriteProjectConfiguration** með Excel-innbótinni. Til að nota innbótina skaltu virkja hönnunarsnið í Excel-innbót fjármála- og reksturs og bæta **DualWriteProjectConfiguration** við vinnublaðið. Frekari upplýsingar er að finna í [Skoða og uppfæra einingagögn með Excel](../../office-integration/use-excel-add-in.md).
3. Stilltu **IsDebugMode** á **Já** í verkinu.
4. Keyrðu atburðarásina sem er að búa til villur.
5. Fjölorða kladdar eru geymdir í töflunni **DualWriteErrorLog**.
6. Til að fletta upp gögnum á töfluvafra skal nota eftirfarandi tengil: `https://999aos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`, sem kemur í staðinn fyrir `999` eftir þörfum.
7. Uppfærðu aftur eftir [KB 4595434](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=98e5dc124ac125c57ad633d885ac612aea3ddb8f4abf9d71ab3aa354f2e06cbe) sem er í boði fyrir uppfærslur á verkvangi 37 og síðar. Ef þú ert með þessa lagfæringu uppsetta þá sækir kembistillingin fleiri kladda.  

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Athugaðu samstillingarvillur á sýndarvélinni fyrir forrit fjármála- og reksturs

**Nauðsynlegt hlutverk til að skoða villurnar:** Kerfisstjóri

1. Skráðu þig inn í Microsoft Dynamics Lifecycle Services (LCS).
2. Opnaðu LCS-verkið sem þú valdir til að gera tvískriftaprófun fyrir.
3. Veldu reitinn **Umhverfi í skýi**.
4. Notaðu Remote Desktop til að skrá þig inn á sýndarvélina (VM) fyrir forrit fjármála- og reksturs. Notaðu staðbundna reikninginn sem er sýndur í LCS.
5. Opnaðu tilvikayfirlit.
6. Veldu **Forrit og þjónustukladdar \> Microsoft \> Dynamics \> AX -DualWriteSync \> Virkt**.
7. Farðu yfir listann yfir nýlegar villur.

## <a name="dual-write-ui-landing-page-showing-blank"></a>Lendingarsíða notendaviðmóts með tvöfaldri skráningu er auð
Þegar síða tvöfaldrar skráningar er opnuð í Microsoft Edge eða Google Chrome-vafra hleðst upphafssíðan ekki og þú sérð auða síðu eða villu eins og „Eitthvað fór úrskeiðis“.
Í Devtools sérðu villu í klöddum stjórnborðsins:

>bundle.eed39124e62c58ef34d2.js:37 DOMException: Ekki tókst að lesa eiginleikann „sessionStorage“ úr „Glugga“: Aðgangur óheimill fyrir þetta skjal. at t.storeInSessionStorage (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:16:136860 ) at new t (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:69:20103 ) at ci (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:44115 ) at Eo (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:58728 ) at jo (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:65191 ) at Nr (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:84692 ) at Or (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:85076 ) at Ss (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:91750 ) at vs (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:91130 ) at hs (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:90151 )

Notendaviðmótið notar „lotugeymslu“ vafrans til að geyma nokkur eiginleikagildi til að hlaða inn upphafssíðunni. Til að þetta virki þarf að leyfa kökur frá þriðja aðila í vafranum fyrir þetta svæði. Villan bendir til þess að notendaviðmótið hafi ekki aðgang að lotugeymslunni. Tvær sviðsmyndir geta komið upp þar sem þetta vandamál kemur upp:

1.  Þú ert að opna notendaviðmótið í huliðsstillingu Edge/Chrome og lokað er á kökur frá þriðja aðila í huliðsstillingu.
2.  Þú hefur útilokað kökur frá þriðja aðila í Edge/Chrome.

### <a name="mitigation"></a>Mildun
Vefkökur þriðja aðila þurfa að vera leyfðar í stillingum vafrans.

### <a name="google-chrome-browser"></a>Google Chrome-vafri
Fyrsti valkostur:
1.  Farðu í stillingar með því að slá inn chrome://settings/ í veffangastikunni og farðu svo í Persónuvernd og öryggi -> Kökur og önnur gögn vefsvæðis.
2.  Veljið „Leyfa allar kökur“. Ef þú vilt ekki gera þetta skaltu velja seinni kostinn.

Annar valkostur:
1.  Farðu í stillingar með því að slá inn chrome://settings/ í veffangastikunni og farðu svo í Persónuvernd og öryggi -> Kökur og önnur gögn vefsvæðis.
2.  Ef „Útiloka kökur frá þriðja aðila í huliðsstillingu“ eða „Útiloka kökur frá þriðja aðila“ er valið skal fara í „Vefsvæði sem geta alltaf notað kökur“ og smelltu á **Bæta við**. 
3.  Bæta við svæðaheiti Finance & Operations-forrita – https://<your_FinOp_instance>.cloudax.dynamics.com. Gættu þess að þú veljir gátreitinn fyrir „Öll fótspor, aðeins á þessu vefsvæði“. 

### <a name="microsoft-edge-browser"></a>Microsoft Edge vafri
1.  Fara í Stillingar -> Heimildir vefsvæða -> Kökur og gögn vefsvæða.
2.  Slökkva á „Útiloka allar kökur frá þriðju aðilum“.  

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a>Taktu af og tengdu annað Dataverse-umhverfi úr forriti fjármála- og reksturs

**Nauðsynlegt hlutverk til að aftengja umhverfið:** Kerfisstjóri fyrir forrit fjármála- og reksturs eða Dataverse.

1. Skráið inn á forrit fjármála- og reksturs.
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

## <a name="how-to-ensure-data-integration-is-using-the-most-current-finance-and-operations-schema"></a>Hvernig á að tryggja samþættingu gagna er að nota nýjasta skema fjármála- og reksturs

Þú gætir lent í vandræðum með gögn í gagnasamþættingunni ef nýjasta skemað er ekki notað. Eftirfarandi skref hjálpa þér að endurhlaða einingalistann í forritum fjármála- og reksturs og einingum í gagnasamþættara.

### <a name="refresh-entity-list-in-finance-and-operations-environment"></a>Uppfæra einingalista í umhverfi fjármála- og reksturs
1.  Skráðu þig inn í umhverfi fjármála- og reksturs.
2.  Veljið **Gagnastjórnun**.
3.  Inni í Gagnastjórnun, veldu **Færibreytur ramma**.
4.  Á síðunni **Færibreytur ramma fyrir inn- og útflutning gagna** skal velja flipann **Einingastillingar** og síðan velja **Uppfæra einingalista**. Það getur tekið yfir 30 mínútur að uppfærast, fer eftir fjölda eininga.
5.  Farðu í **Gagnastjórnun** og veldu **Gagnaeiningar** til að staðfesta að væntanlegar einingar séu gefnar upp. Ef væntanlegir einingar eru ekki taldar upp skal staðfesta að einingarnar birtist í umhverfi fjármála- og reksturs og endurheimta einingarnar sem vantar, eftir þörfum.

#### <a name="if-the-refresh-fails-to-resolve-the-issue-delete-and-re-add-the-entities"></a>Ef uppfærslan leysir ekki úr vandamálinu skaltu eyða og bæta við einingunum við aftur

> [!NOTE]
> Þú gætir þurft að stöðva alla vinnsluhópa sem eru að nota einingarnar áður en eyðing er gerð.

1.  Veldu **Gagnastjórnun** í umhverfi fjármála- og reksturs og veldu **Gagnaeiningar**.
2.  Leitaðu að einingum með vandamálum og skrifaðu hjá þér markeininguna, millistigstöfluna, einingarheitið og aðrar stillingar. Eyðið einingunni eða einingunum af listanum.
3.  Veldu **Nýtt** og settu aftur inn eininguna eða einingarnar sem nota gögnin úr skrefi 2. 

#### <a name="refresh-entities-in-data-integrator"></a>Endurnýja einingar í gagnasamþættara
Skráðu þig inn Power Platform-stjórnendamiðstöð og veldu **Samþætting gagna**. Opnið verkið þar sem vandamálin eru og veldu **Uppfæra einingar**.

## <a name="how-to-enable-and-save-network-trace-so-that-traces-can-be-attached-to-support-tickets"></a>Hvernig á að virkja og vista netrakningu þannig að hægt verði að hengja rakningar við þjónustubeiðni

Þjónustudeildin gæti þurft að fara yfir netrakningar til að  úrræðaleita sum vandamál. Til að búa til netrakningu skal fylgja þessum skrefum:

### <a name="google-chrome-browser"></a>Google Chrome-vafri

1. Í opna flipanum skal ýta á **F12** eða velja **Verkfæri þróunaraðila** til að opna verkfæri þróunaraðila.
2. Opnaðu flipann **Netkerfi** og sláðu inn **integ** í textasíureitinn.
3. Keyrðu aðstæðurnar og fylgstu með beiðnunum sem eru skráðar inn.
4. Hægrismelltu á færslurnar og veldu **Vista allt sem HAR með efni**.

### <a name="microsoft-edge-browser"></a>Microsoft Edge vafri

1. Í opna flipanum skal ýta á **F12** eða velja **Verkfæri þróunaraðila** til að opna verkfæri þróunaraðila.
2. Opnaðu flipann **Netkerfi**.
3. Keyrðu aðstæðurnar.
4. Veldu **vista** til að flytja út niðurstöður sem HAR.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

