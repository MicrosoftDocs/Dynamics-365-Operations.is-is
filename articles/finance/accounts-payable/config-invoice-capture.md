---
title: Stilltu lausnina fyrir innheimtu reikninga
description: Þessi grein útskýrir hvernig á að stilla reikningsfangalausnina.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690984"
---
# <a name="configure-the-invoice-capture-solution"></a>Stilltu lausnina fyrir innheimtu reikninga

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Eftir að lausn reikningsfanga hefur verið sett upp verður þú að stilla umhverfið. Ferlið samanstendur af eftirfarandi grunnskrefum.

1. **Áskilið:** Samstilla lögaðila frá Microsoft Dynamics 365 Fjármál. Þetta skref er notað til að setja upp skipulag í Microsoft Power Platform.
2. **Áskilið:** Stilltu rásir fyrir innflutning á reikningsmyndum. Lausnin styður eftirfarandi rásir:

    - Office 365 Outlook (sjálfgefið)
    - Outlook.com
    - OneDrive
    - SharePoint

3. **Valfrjálst:** Skilgreindu viðbótarstillingarhópa fyrir OCR-þjónustuna (optical character recognition).
4. **Valfrjálst:** Skilgreindu vörpunarreglur fyrir lögaðila, lánardrottinsreikning, vöru og innkaupagerð.

Þessi grein beinist að tveimur nauðsynlegum skrefum ferlisins. Fyrir frekari upplýsingar um stillingarhópa, sjá [Stillingarhópar fyrir lausnarupptöku reikninga](invoice-capture-config-group.md). Fyrir frekari upplýsingar um kortlagningarreglur, sjá [Kortlagningarreglur fyrir lausn reikningsfanga](invoice-capture-mapping-rules.md).

## <a name="manage-legal-entities"></a>Stjórna lögaðilum

Fjármál skilgreina lögaðila sem stofnanir sem eru auðkenndar með skráningu hjá lögum. Atvinnustarfsemi fer fram og skráð í aðskildum lögaðilum. Í Microsoft Power Platform, rekstrareiningar, öryggishlutverk og notendur eru tengdir saman á þann hátt sem er í samræmi við hlutverkatengda öryggislíkanið.

Rekstrareiningar eru notaðar ásamt öryggishlutverkum til að stjórna gagnaaðgangi. Notendur sjá aðeins þær upplýsingar sem þeir þurfa til að vinna störf sín. Invoice capture lausnin býður upp á stillingarrými þar sem þú getur hlaðið inn grunnupplýsingum frá núverandi lögaðilum í Finance og stjórnað þeim aðilum sem eru búnir til handvirkt. Lögaðilarnir eru notaðir á reikningum lánardrottna og í öryggiseftirliti.

Þegar lögaðili er stofnaður og sýndur í listaskjánum er sjálfkrafa stofnuð sjálfgefin rekstrareining sem ber sama nafn. Liðið er veitt **AP skrifstofumaður** öryggishlutverk. Þegar lögaðilar eru fluttir inn eru grunnaðalgögn frá Finance flutt inn. Hlutirnir sem ekki eru til verða auðkenndir af lögaðila og munu bæta þeim við reikningsfangalausnina. Sjálfgefna stillingarhópnum er úthlutað nýjum lögaðilum.

### <a name="sync-legal-entities"></a>Samstilla lögaðila

Þú getur ekki stofnað lögaðila beint. Hins vegar geturðu samstillt lögaðila frá Finance. Til að samstilla lögaðila skaltu fylgja þessum skrefum.

1. Fara til **Uppsetning \> Kerfisuppsetning \> Stjórna lögaðilum**.
2. Veldu **Samstilla lögaðila**, og veldu síðan **Allt í lagi** í staðfestingarglugganum.

Eftir að samstillingu er lokið er fjöldi nýrra lögaðila sýndur. Nýju lögaðilarnir eru sýndir á listaskjánum. Sjálfgefna stillingarhópnum er úthlutað til nýju lögaðilanna.

## <a name="configure-invoice-import-channels"></a>Stilltu innflutningsrásir reikninga

Seljendur senda reikninga frá mismunandi rásum (tölvupóstur, skráarvinnusvæði eða reikningagátt) með mismunandi sniðum (pappír eða mynd). Invoice capture lausnin getur séð um mismunandi rásir og snið. Eftirfarandi gerðir eru studdar:

- Office 365 Horfur
- Outlook.com
- SharePoint
- OneDrive

Þegar rás er búin til fyrir ákveðinn reikning er sjálfvirkt flæði sem hefur fyrirfram skilgreint sniðmát smíðað til að fylgjast með komandi tölvupósti eða skrám í pósthólfinu eða rýminu. Hægt er að bera kennsl á hvaða skrá sem er með gildan reikning og senda á reikningssvæðið til að bíða afgreiðslu hjá viðskiptaskuldaskrifstofu (AP). Viðhengið ætti að vera á PDF eða myndformi. Hægt er að hlaða reikningum inn í Invoice capture lausnina í samræmi við rásaruppsetningu.

### <a name="create-a-channel"></a>Búðu til rás

Ef þú hefur flutt inn viðbótarlausnarpakkann (Dynamics 365 Invoice capture – Uppsetningarverkfæri), er sjálfgefin tenging fyrir Office 365 Outlook er tilbúið til notkunar. Ef þú vilt búa til fleiri tengingar fyrir mismunandi tölvupóstreikninga eða aðrar rásargerðir, sjáðu [Búðu til viðbótartengingar fyrir rásir](invoice-capture-advanced-settings.md#create-additional-connections-for-channels).

Fylgdu þessum skrefum til að búa til rás.

1. Fara til **Uppsetning \> Kerfisuppsetning \> Stilla rásir**.
2. Veljið **Nýtt**.
3. Stilltu eftirfarandi svæði:

    - Heiti rásar
    - Lýsing
    - Gerð
    - Tenging

Aðeins er hægt að flytja tölvupóst eða skrár sem passa við eftirfarandi skilyrði inn í lausnina.

| Gerð               | Skilgreining  | Meiri upplýsingar |
|--------------------|----------------|------------------|
| Office 365 Horfur | Mappa         | Tölvupóstmöppan verður að vera undir rótarskránni. Sjálfgefið er að Inbox mappan er notuð. Undirmappa er ekki studd. |
|                    | Efnissía | (Valfrjálst) Undirstrengur sem ætti að vera með í efninu. |
|                    | Frá           | (Valfrjálst) Netfang sendanda eða sendenda. Ef þú tilgreinir mörg heimilisföng, notaðu semíkommu (;) sem skilju. |
| SharePoint         | Heimilisfang síðunnar   | Vefslóð veffangsins. |
|                    | Mappa         | Mappan í veffanginu. |

### <a name="activate-the-channel"></a>Virkjaðu rásina

Þegar flæði er vistað sýna reitir stöðu rásarinnar og tímann þegar hún var búin til. Upphaflega var **Staða** reiturinn er stilltur á **Óvirkt**. The **Staða ástæða** reiturinn gefur til kynna að rásin hafi verið frumstillt og að hún sé tilbúin til að virkja hana.

Til að virkja rásina velurðu **Virkjaðu**. The **Staða** og **Staða ástæða** reitirnir eru uppfærðir.

Ef ekki er þörf á rás geturðu gert hana óvirka. Til að slökkva á rás velurðu **Afvirkja**. The **Staða** og **Staða ástæða** reitirnir eru uppfærðir.

### <a name="manage-flows-in-flow-management"></a>Stjórna flæði í flæðisstjórnun

Þú getur skoðað rás á **Stilla rásir** síðu eða í flæðisstjórnun.

Til að skoða frekari upplýsingar, farðu á **Stjórnunarkerfi \> Sjálfgefin lausn \> Ský flæðir**, og veldu markflæði. Upplýsingarnar sem eru sýndar innihalda tengdar tengingar, eigendur og keyrslusögu.

Til að samstilla stöðuna velurðu **Athugaðu** til að staðfesta að staða rásarinnar samsvari stöðu flæðisins.

Sum tilvik um meðhöndlun undantekninga eru sýnd í **Staða ástæða** reit:

- **Vantar Dataverse Tenging** – Núverandi notandi hefur ekki búið til að minnsta kosti einn **Microsoft Dataverse** tengingartilvísun.
- **Ekki fundið** – Flæðinu sem er tengt rásinni hefur verið eytt í flæðisstjórnun. Rásin ætti að vista aftur til að búa til nýja rás.
- **Óvirkt í flæðisstjórnun** – Rennslið hefur verið gert óvirkt í flæðisstjórnun og staða rásarinnar er frábrugðin stöðu flæðisins.
- **Virkjað í flæðisstjórnun** – Rennslið hefur verið virkjað í flæðisstjórnun og staða rásarinnar er frábrugðin stöðu flæðisins.
- **Óvænt villa kom upp** – Notandinn verður að staðfesta að vefsvæðið sé „samskiptasíða“ og að mappan sé „skjalasafn“.
