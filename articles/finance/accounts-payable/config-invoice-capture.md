---
title: Skilgreina Invoice capture-lausnina
description: Þessi grein útskýrir hvernig eigi að skilgreina Invoice capture-lausnina.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: e297dafc930368f14f2e68213ce4153ba792ef4d
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690984"
---
# <a name="configure-the-invoice-capture-solution"></a>Skilgreina Invoice capture-lausnina

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Eftir að Invoice capture-lausn hefur verið sett upp verður að skilgreina umhverfið. Ferlið samanstendur af eftirfarandi grunnskrefum.

1. **Nauðsynlegt:** Samstilla lögaðilana frá Microsoft Dynamics 365 Finance. Þetta skref er notað til að setja upp fyrirtækjaskipulagið í Microsoft Power Platform.
2. **Áskilið:** Skilgreinið rásir fyrir innflutning reikningsmynda. Lausnin styður eftirfarandi rásir:

    - Office 365 Outlook (sjálfgefið)
    - Outlook.com
    - OneDrive
    - SharePoint

3. **Valfrjálst:** Skilgreindu fleiri skilgreiningarhópa fyrir OCR-þjónustu.
4. **Valfrjálst:** Skilgreina vörpunarreglur fyrir lögaðila, lánardrottnalykil, vöru og innkaupagerð.

Í þessari grein er sjónum beint að tveimur nauðsynlegum skrefum í ferlinu. Frekari upplýsingar um skilgreiningarhópa eru í [Skilgreiningarhópar Invoice capture-lausnar](invoice-capture-config-group.md). Frekari upplýsingar um vörpunarreglur er að finna á [Vörpunarreglur Invoice Capture-lausnar](invoice-capture-mapping-rules.md).

## <a name="manage-legal-entities"></a>Stjórna lögaðila

Fjármálafyrirtæki skilgreinir lögaðila sem stofnanir sem eru auðkenndar með skráningu hjá lögbærum yfirvöldum. Fyrirtæki eru skráð og stunda starfsemi sem lögaðili. Í Microsoft Power Platform eru viðskiptaeiningar, öryggishlutverk og notendur tengd saman á þann hátt sem samræmist öryggislíkaninu sem byggir á hlutverkum.

Viðskiptaeiningar eru notaðar ásamt öryggishlutverki til að stjórna aðgangi að gögnum. Notendur sjá aðeins þær upplýsingar sem þeir þurfa til að sinna störfum sínum. Invoice capture-lausnin býður upp á skilgreiningarrými þar sem þú getur hlaðið inn grunnupplýsingum frá núverandi lögaðilum í Finance og stjórnað þeim aðilum sem eru stofnaðir handvirkt. Lögaðilarnir eru notaðir á reikningum lánardrottna og við öryggisstjórnun.

Þegar lögaðili er stofnaður og sýndur í listayfirliti er sjálfgefin viðskiptaeining sem ber sama heiti búin til sjálfkrafa. Teymið fær hlutverk **Bókari viðskiptavina**. Þegar lögaðilar eru fluttir inn eru grunnaðalgögn úr Finance flutt inn. Þær vörur sem ekki eru til verða auðkenndar af lögaðila og þeim verður bætt við Invoice capture-lausnina. Sjálfgefni skilgreiningarhópurinn er úthlutaður á nýju lögaðilana.

### <a name="sync-legal-entities"></a>Samstilla lögaðila

Ekki er hægt að stofna lögaðila beint. Þú getur hins vegar samstillt lögaðila úr Finance. Til að samstilla lögaðila skal fylgja eftirfarandi skrefum.

1. Farið í **Uppsetning \> Kerfisuppsetning \> Stjórna lögaðila**.
2. Veljið **Samstilla lögaðila** og veljið svo **Í lagi** í staðfestingarglugganum.

Eftir að samstillingu er lokið er fjöldi nýrra lögaðila sýndur. Nýju lögaðilarnir eru sýndir á listayfirlitinu. Sjálfgefni stillihópurinn er úthlutaður á nýju lögaðilana.

## <a name="configure-invoice-import-channels"></a>Skilgreina reikningsinnflutningsrásir

Lánardrottnar senda reikninga frá mismunandi rásum (tölvupósti, vinnusvæði skráa eða reikningsgátt) í gegnum mismunandi snið (pappír eða mynd). Invoice capture-lausnin ræður við mismunandi rásir og snið. Eftirfarandi gerðir eru studdar:

- Office 365 Outlook
- Outlook.com
- SharePoint
- OneDrive

Þegar rás er stofnuð fyrir tiltekinn lykil er sjálfvirkt flæði sem er með fyrirframskilgreint sniðmát stofnað til að fylgjast með tölvupóstum eða skrám sem berast í innhólfið eða rýmið. Allar skrár sem eru með gildan reikning er hægt að auðkenna og senda á reikningssvæðið til að bíða úrvinnslu hjá starfsmanni viðskiptaskulda. Viðhengið á að vera á PDF-sniði eða myndsniði. Hægt er að hlaða reikningum inn í Invoice capture-lausnina í samræmi við skilgreiningu rásarinnar.

### <a name="create-a-channel"></a>Uppsetning rása

Ef þú hefur flutt inn viðbótarlausnapakkann (Dynamics 365 Invoice capture – Installation Tools) er sjálfgefna tengingin fyrir Office 365 Outlook tilbúin til notkunar. Ef þú vilt búa til fleiri tengingar fyrir mismunandi tölvupóstreikninga eða aðrar rásartegundir skaltu skoða [Búa til fleiri tengingar fyrir rásir](invoice-capture-advanced-settings.md#create-additional-connections-for-channels).

Fylgdu þessum skrefum til að stofna rás.

1. Farið í **Uppsetning \> Kerfisuppsetning \> Skilgreiningarrásir**.
2. Veljið **Nýtt**.
3. Stilltu eftirfarandi svæði:

    - Heiti rásar
    - Lýsing
    - Gerð
    - Tenging

Aðeins er hægt að flytja inn tölvupósta eða skrár sem passa við eftirfarandi skilyrði í lausnina.

| Gerð               | Skilgreining  | Meiri upplýsingar |
|--------------------|----------------|------------------|
| Office 365 Outlook | Mappa         | Póstmappan verður að vera undir rótarmöppunni. Innhólfsmappan er sjálfgefið notuð. Undirmappa er ekki studd. |
|                    | Efnissía | (Valfrjálst) Undirstrengur sem á að fylgja í efninu. |
|                    | Frá           | (Valfrjálst) Netfang sendanda (eins eða fleiri) Ef þú tilgreinir mörg heimilisföng skaltu nota semíkommu (;) til aðgreiningar. |
| SharePoint         | Veffang svæðis   | Veffang vefsetursins. |
|                    | Mappa         | Mappan í veffanginu. |

### <a name="activate-the-channel"></a>Virkja rásina

Þegar flæði er vistað sýna reitir stöðu rásarinnar og tímann þegar hún er búin til. Reiturinn **Staða** er upphaflega stilltur á **Óvirkt**. Reiturinn **Staða** gefur til kynna að rásin hafi verið ræst og sé tilbúin til virkjunar.

Rásin er virkjuð með því að velja **Virk**. Reitirnir **Staða** og **Ástæða stöðu** eru uppfærðir.

Ef ekki er þörf á rás er hægt að óvirkja hana. Til að óvirkja rás skal velja **Óvirkja**. Reitirnir **Staða** og **Ástæða stöðu** eru uppfærðir.

### <a name="manage-flows-in-flow-management"></a>Stjórna flæði í flæðisstjórnun

Hægt er að skoða rás á síðunni **Skilgreiningarrásir** eða í flæðisstjórnun.

Til að skoða nánari upplýsingar ferðu í **Stjórnandakerfi\> Sjálfgefin lausn \> Skýjaflæði** og velur markflæðið. Upplýsingarnar sem eru sýndar innihalda tengdar tengingar, eigendur og sögu keyrslu.

Til að samstilla stöðu skal velja **Athuga** til að staðfesta að staða rásar sé í samræmi við stöðu flæðis.

Sum tilvik þar sem undantekningar eru meðhöndlaðar eru sýnd í reitnum **Staða ástæðu**:

- **Vantar Dataverse tengingu** – Núverandi notandi hefur ekki búið til að minnsta kosti eina tengitilvísun fyrir **Microsoft Dataverse**.
- **Fannst ekki** – Flæðinu sem er tengt rásinni hefur verið eytt í flæðisstjórnun. Rásin ætti að vera vistuð aftur til að stofna nýja rás.
- **Afvirkjað í flæðisstjórnun** – Flæðið hefur verið gert óvirkt í flæðisstjórnun og staða rásarinnar er frábrugðin stöðu flæðisins.
- **Virkjað í flæðisstjórnun** – Flæðið hefur verið virkjað í flæðisstjórnun og staða rásarinnar er frábrugðin stöðu flæðisins.
- **Óvænt villa kom upp** – Notandinn verður að staðfesta að vefsvæðið sé „Samskiptasvæði“ og að mappan sé „Skjalasafn“.
