---
title: Þjónustuumhverfi
description: Þessi grein veitir upplýsingar um þjónustuumhverfi fyrir rafræna reikninga og útskýrir hvernig á að setja þau upp.
author: gionoder
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: ff6f50ff78676f5efed7d905fb622ad662b541d7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291600"
---
# <a name="service-environments"></a>Þjónustuumhverfi

[!include [banner](../includes/banner.md)]

Þjónustuumhverfi eru rökrétt skipting sem eru búin til til að styðja við hnattvæðingareiginleikana og samsvarandi skjöl sem eru unnin í rafrænni reikningsþjónustu. Öryggisleyndarmálin og stafræn skilríki, og aðgangsheimildir (stjórnun), verða að vera stillt á þjónustuumhverfisstigi.

Þú getur búið til eins mörg þjónustuumhverfi og þú þarft. Öll þjónustuumhverfi sem þú býrð til eru óháð hvert öðru. Sem bestu starfsvenjur mælum við með að þú búir til að minnsta kosti tvö þjónustuumhverfi:

- Eitt umhverfi fyrir helstu þróunar- og löggildingartilgang. Þetta umhverfi er venjulega notendaviðurkenningarprófun (UAT) umhverfi.
- Eitt umhverfi í framleiðslutilgangi. Þetta umhverfi er venjulega framleiðsluumhverfi.

Þessi tegund af skiptingu hjálpar til við að tryggja að rafræn reikningsferlar séu staðfestir og sérsniðnir í sandkassanum áður en þeir fara í framleiðslu.

Þjónustuumhverfi verður að búa til og viðhalda í Regulatory Configuration Service (RCS). Síðan, þegar þær eru tilbúnar, þarf að birta þær í rafræna reikningaþjónustu. Útgáfuferlið sendir færibreytur þjónustuumhverfisins frá RCS tilvikinu til rafrænnar reikningaþjónustunnar.

Ef þú lýkur ekki útgáfuferlinu eftir að þú hefur búið til nýtt þjónustuumhverfi eða breytt núverandi þjónustuumhverfi (til dæmis með því að bæta við eða fjarlægja notendur eða Microsoft Azure Key Vault leyndarmál), munu breytingarnar ekki taka gildi. Aðeins er hægt að nálgast birt umhverfi með Dynamics 365 Finance eða Dynamics 365 Supply Chain Management.

## <a name="service-environment-statuses"></a>Staða þjónustuumhverfis

Hægt er að stjórna þjónustuumhverfi með stöðu þeirra. Þú getur skoðað stöðu umhverfisins á **Þjónustuumhverfi** síðu. Eftirfarandi stöður eru í boði:

- **Ekki birt** – Umhverfið hefur verið stofnað, en hefur ekki verið birt.
- **Birt** – Umhverfið hefur verið birt rafrænum reikningum.
- **Breytt** – Eigindum útgefins umhverfis hefur verið breytt, en breytingarnar hafa ekki enn verið gefnar út.

## <a name="users"></a>Notendur

Hvert þjónustuumhverfi þarf að skrá þá notendur sem geta tengst rafrænum reikningum frá fjármála- eða framboðskeðjustjórnun.

## <a name="applications"></a>Hugbúnaður

Í sumum tilfellum gætu önnur forrit en fjármála- eða birgðakeðjustjórnun þurft að tengjast rafrænum reikningaþjónustu til að leggja fram rafræn skjöl til frekari vinnslu eða til að sækja upplýsingar eins og skilastöðu skjals. Í þessum tilfellum ætti forritið að vera skilgreint á listanum yfir forrit. Þannig mun það hafa aðgang að rafrænum reikningaþjónustu. Einnig þarf að skrá umsóknina sem umsókn í Azure Active Directory (Azure AD), og auðkenni hlutar verður að nota til að auðkenna það. 

Vegna þess að Microsoft krefst mikillar öryggisstjórnunar yfir forritum sem geta tengst rafrænu reikningsþjónustunni, verður þú að hafa samband við Microsoft á<DGXRegulatoryservicesengineering@service.microsoft.com> og gefðu upp eftirfarandi upplýsingar um umsókn þína:

- Azure AD-leigjandakenni
- Microsoft Dynamics Auðkenni líftímaþjónustu (LCS) umhverfi
- Auðkenni umsókn (auðkenni viðskiptavinar)
- Kenni hlutar
- Rökstuðningur og lýsing á umsókn á háu stigi

Microsoft mun meta beiðnina og skrá forritið í öryggisskrána til að tryggja að það geti starfað með rafrænum reikningum.

## <a name="number-sequences"></a>Númeraraðir

Ef aðstæður þínar krefjast númeraraðir (til dæmis í skráarnöfnum) geturðu notað númeraraðir sem eru skilgreindar fyrir tiltekið umhverfi, en sem hægt er að nota annaðhvort yfir hnattvæðingareiginleika eða fyrir tiltekna hnattvæðingareiginleika. Eftir að talnaröð er skilgreind er hægt að nota hana í breytum og vinnslupípum. Til að fylgjast með notkun þess, á **Númeraraðir** síðu, leitaðu að gildi á **Núverandi** fyrir **Í notkun** breytu.

### <a name="working-with-number-sequences"></a>Unnið með númeraraðir
Á **Númeraraðir** síða: 

- Veldu **Nýtt** til að búa til talnaröð. Sláðu síðan inn nafn og lýsingu. 
- Veldu **Eyða** til að eyða númeraröð ef hún er ekki lengur notuð.
- Þú þarft ekki að velja **Birta** á aðgerðarrúðunni til að birta breytingarnar á númeraröð. Uppfærslan fer fram sjálfkrafa.

## <a name="create-a-key-vault-reference"></a>Búðu til Key Vault tilvísun

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Á vinnusvæðinu **Altækur eiginleiki**, í hlutanum **Umhverfi**, skal velja reitinn **Rafræn reikningsfærsla**.
3. Á **Umhverfisuppsetning** síðu, á aðgerðarrúðunni, veldu **Þjónustuumhverfi**.
4. Á **Þjónustuumhverfi** síðu, á aðgerðarrúðunni, veldu **Helstu færibreytur Vault**.
5. Á **Helstu færibreytur Vault** síðu, veldu **Nýtt** til að búa til Key Vault tilvísun.
6. Í **Nafn** reit, sláðu inn heiti Key Vault tilvísunarinnar.
7. Í reitnum **Lýsing** skal færa inn lýsingu.
8. Í **Key Vault URI** reit, límdu Key Vault URI frá lyklahólfinu (`https://<your key vault>.vault.azure.net/`). Fyrir frekari upplýsingar, sjá [Búðu til Azure lykilhólf í Azure gáttinni](e-invoicing-create-azure-key-vault-azure-portal.md).
9. Veldu **Vista**.
    
## <a name="create-a-secret-for-the-storage-account-secret-token"></a>Búðu til leyndarmál fyrir leyndarmál geymslureikningsins

1. Á **Helstu færibreytur Vault** síðu, veldu Key Vault tilvísunina sem þú bjóst til í fyrra ferli og síðan í **Skírteini** kafla, veldu **Bæta við**.
2. Í reitinn **Heiti** skal færa inn heiti fyrir leynilykil geymslureiknings. Þetta nafn ætti að passa við nafn Key Vault-leyndarmálsins sem geymir SAS-táknið (e. storage shared access signature). Fyrir frekari upplýsingar, sjá [Búðu til Azure geymslureikning í Azure gáttinni](e-invoicing-create-azure-storage-account-azure-portal.md). 
3. Í reitnum **Lýsing** skal færa inn lýsingu.
4. Í reitnum **Gerð** skal velja **Leynilykill**.
5. Veldu **Vista**.
    
## <a name="create-a-service-environment"></a>Stofna þjónustuumhverfi

1. Á **Þjónustuumhverfi** síðu, veldu **Nýtt** að skapa þjónustuumhverfi.
2. Í **Nafn** reit skal slá inn heiti rafrænna reikningaumhverfisins.
3. Í reitnum **Lýsing** skal færa inn lýsingu.
4. Í reitnum **SAS-leynilykill geymslu** skal velja heiti leynilykils geymslureikningsins sem þarf að nota til að auðkenna aðgang að geymslureikningnum.
5. Í **Notendur** kafla, veldu **Bæta við** að bæta við notanda sem hefur heimild til að senda inn rafræna reikninga í gegnum umhverfið og tengjast geymslureikningnum.
6. Í reitinn **Notandakenni** skal færa inn samnefni notandans. 
7. Í reitinn **Tölvupóstur** skal færa inn netfang notandans.
8. Veldu **Vista**.
9. Á aðgerðarrúðunni velurðu **Birta** að birta umhverfið til rafrænna reikningaþjónustunnar. Staðfestu að verðmæti **Staða** sviði er breytt í **Birt**.
