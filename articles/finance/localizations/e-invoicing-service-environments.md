---
title: Þjónustuumhverfi
description: Þessi grein veitir upplýsingar um þjónustuumhverfi fyrir rafræna reikningsfærslu og útskýrir hvernig á að setja þau upp.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291600"
---
# <a name="service-environments"></a>Þjónustuumhverfi

[!include [banner](../includes/banner.md)]

Þjónustuumhverfi eru röklegar deildaskiptingar sem eru búnar til til að styðja altæka eiginleika og samsvarandi skjöl sem eru unnin í rafrænu reikningsfærsluþjónustunni. Öryggislyklar og stafræn vottorð og aðgangsheimildir (stjórnun) verða að vera skilgreind á öryggisstigi þjónustunnar.

Hægt er að stofna eins mörg þjónustuumhverfi og þarf. Öll þjónustuumhverfi sem þú býrð til eru óháð hvert öðru. Við mælum með því að þú búir til að minnsta kosti tvö þjónustuumhverfi:

- Eitt aðalumhverfi til þróunar og staðfestingar. Þetta umhverfi er yfirleitt umhverfi samþykkisprófunar notanda.
- Eitt umhverfi til framleiðslu. Þetta umhverfi er yfirleitt framleiðsluumhverfi.

Þessi gerð deildaskiptingar hjálpar til við að tryggja að rafræn reikningsfærslufærslu sé staðfest og sérsniðin í sandkassanum áður en þau fara í framleiðslu.

Þjónustuumhverfi verða að vera búin til og haldið við í Regulatory Configuration Service (RCS). Þegar þau eru tilbúin þarf að birta þau í rafrænu reikningsfærsluþjónustunni. Birtingarferlið sendir færibreytur þjónustuumhverfisins frá RCS-tilvikinu til rafrænu reikningaþjónustunnar.

Ef þú lýkur ekki birtingarferlinu eftir að þú hefur búið til nýtt þjónustuumhverfi eða aðlagað núverandi þjónustuumhverfi (til dæmis með því að bæta við eða fjarlægja notendur eða leynilykla Microsoft Azure-lyklageymslu) munu breytingarnar ekki taka gildi. Einungis birt umhverfi er hægt að nálgast hjá Dynamics 365 Finance eða Dynamics 365 Supply Chain Management.

## <a name="service-environment-statuses"></a>Staða þjónustuumhverfis

Hægt er að stjórna þjónustuumhverfum í gegnum stöðu þeirra. Það er hægt að skoða stöðu umhverfis á síðunni **Þjónustuumhverfi**. Eftirfarandi stöður eru í boði:

- **Ekki birt** – Umhverfið hefur verið stofnað, en hefur ekki verið birt.
- **Birt** – Umhverfið hefur verið birt í viðbót rafrænnar reikningsfærsluþjónustu.
- **Breytt** – Eigindum útgefins umhverfis hefur verið breytt, en breytingarnar hafa ekki enn verið gefnar út.

## <a name="users"></a>Notendur

Hvert þjónustuumhverfi verður að sýna notendurna sem geta tengst við rafræna reikningsfærslu úr Finance eða Supply Chain Management.

## <a name="applications"></a>Hugbúnaður

Í sumum tilvikum gætu önnur forrit en Finance eða Supply Chain Management þurft að tengjast rafrænu reikningsfærsluþjónustunni til að senda rafræn skjöl til frekari úrvinnslu eða til að sækja upplýsingar á borð við stöðu á framlagningu skjals. Í þessum aðstæðum ætti að skilgreina forritið í listanum yfir forrit. Á þennan hátt fær það aðgang að rafrænni reikningsfærsluþjónustu. Einnig þarf að skrá forritið sem forrit í Azure Active Directory (Azure AD), og nota þarf hlutarauðkennið til að auðkenna það. 

Þar sem Microsoft krefst mikillar öryggisstjórnunar á forritum sem geta tengst rafrænu reikningagerðarþjónustunni verður þú að hafa samband við Microsoft á <DGXRegulatoryservicesengineering@service.microsoft.com> og gefa upp eftirfarandi upplýsingar um forritið:

- Azure AD-leigjandakenni
- Microsoft Dynamics Auðkenni Lifecycle Services-umhverfis (LCS)
- Forritsauðkenni (biðlaraauðkenni)
- Kenni hlutar
- Réttlæting og nákvæm lýsing á forritinu

Microsoft mun meta beiðnina og skrá forritið í öryggisskrá til að tryggja að það geti unnið með rafrænni reikningsfærslu.

## <a name="number-sequences"></a>Númeraraðir

Ef aðstæður þínar krefjast númeraraða (t.d. í skráarheitum) er hægt að nota númeraraðir sem eru skilgreindar fyrir tiltekið umhverfi, en sem hægt er að nota annað hvort yfir altæka eiginleika eða fyrir tiltekinn altækan eiginleika. Eftir að númeraröð er skilgreind geturðu notað hana í breytum og pípuvinnslum. Til að fylgjast með notkun þess, á síðunni **Númeraraðir**, leitaðu að gildi **Núverandi** fyrir færibreytuna **Í notkun**.

### <a name="working-with-number-sequences"></a>Unnið með númeraraðir
Á síðunni **Númeraraðir**: 

- Veljið **Nýtt** til að búa til nýja númeraröð. Færa skal inn heiti og lýsingu. 
- Veldu **Eyða** til að eyða númeraröð ef hún er ekki lengur notuð.
- Þú þarft ekki að velja **Birta** á aðgerðasvæðinu til að birta breytingar á númeraröð. Uppfærsla á sér stað sjálfvirkt.

## <a name="create-a-key-vault-reference"></a>Stofna lyklageymslutilvísun

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Á vinnusvæðinu **Altækur eiginleiki**, í hlutanum **Umhverfi**, skal velja reitinn **Rafræn reikningsfærsla**.
3. Á síðunni **Uppsetningar umhverfis**, á aðgerðasvæðinu, skal velja **Þjónustuumhverfi**.
4. Á síðunni **Þjónustuumhverfi** á aðgerðasvæðinu skal velja **Færibreytur lyklageymslu**.
5. Á síðunni **Færibreytur lyklageymslu** veljið **Ný** til að stofna tilvísun í lyklageymslu.
6. Í reitinn **Heiti** skal slá inn heiti á tilvísun lyklageymslu.
7. Í reitnum **Lýsing** skal færa inn lýsingu.
8. Í reitinn **URI lyklageymslu** skal líma URI lyklageymslu úr lyklageymslunni (`https://<your key vault>.vault.azure.net/`). Frekari upplýsingar eru í [Stofna Azure-lyklageymslu í Azure-gáttinni](e-invoicing-create-azure-key-vault-azure-portal.md).
9. Veldu **Vista**.
    
## <a name="create-a-secret-for-the-storage-account-secret-token"></a>Búðu til leynilykil fyrir leynilegan lykil geymslureikningsins

1. Á síðunni **Færibreytur lyklageymslu** skal velja tilvísun lyklageymslu sem var stofnuð í fyrri vinnslu og síðan í hlutanum **Vottorð** skal velja **Bæta við**.
2. Í reitinn **Heiti** skal færa inn heiti fyrir leynilykil geymslureiknings. Þetta heiti ætti að samsvara heiti leynilykils lyklageymslunnar sem geymir undirskriftina fyrir sameiginlegan aðgang að geymslu (SAS). Frekari upplýsingar eru í [Stofna Azure-geymslureikning í Azure-gáttinni](e-invoicing-create-azure-storage-account-azure-portal.md). 
3. Í reitnum **Lýsing** skal færa inn lýsingu.
4. Í reitnum **Gerð** skal velja **Leynilykill**.
5. Veldu **Vista**.
    
## <a name="create-a-service-environment"></a>Stofna þjónustuumhverfi

1. Á síðunni **Þjónustuumhverfi** skal velja **Nýtt** til að búa til þjónustuumhverfi.
2. Í reitinn **Heiti** skal slá inn heiti á umhverfi rafrænnar reikningsfærslu.
3. Í reitnum **Lýsing** skal færa inn lýsingu.
4. Í reitnum **SAS-leynilykill geymslu** skal velja heiti leynilykils geymslureikningsins sem þarf að nota til að auðkenna aðgang að geymslureikningnum.
5. Í hlutanum **Notendur** skal velja **Bæta við** til að bæta við notanda sem hefur heimild til að senda inn rafræna reikninga í gegnum umhverfið og tengjast við geymslureikninginn.
6. Í reitinn **Notandakenni** skal færa inn samnefni notandans. 
7. Í reitinn **Tölvupóstur** skal færa inn netfang notandans.
8. Veldu **Vista**.
9. Á aðgerðasvæðinu skal velja **Birta** til að birta umhverfið á þjóni rafrænnar reikningsfærsluþjónustu. Staðfestið að gildi reitsins **Staða** er breytt í **Birt**.
