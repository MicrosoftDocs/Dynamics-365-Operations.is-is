---
title: Yfirlit rafrænna reikninga
description: Í þessu efnisatriði er að finna upplýsingar um rafræna reikningsfærslu í Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: c3a0cc24a77b29cedaa10ebb4d6e2ad2a4cbf629
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344759"
---
# <a name="electronic-invoicing-overview"></a>Yfirlit rafrænna reikninga

[!include [banner](../includes/banner.md)]

Rafræn reikningsfærsla fyrir Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management er yfirgripsmikil þjónusta fyrir marga leigjendur sem gerir kleift að gera stillanlegar vinnslur á skjölum rafrænna reikninga og stillanleg skjalaskipti. Vinnslan og samþættingarreglurnar eru hægt að stilla að vild og reiknireglurnar eru keyrðar utan Finance og Supply Chain Management. Þjónustan miðast aðallega við vinnslu á rafrænum reikningum í samskiptum fyrirtækja við yfirvöld en hægt er að skilgreina hana sérstaklega í öðrum tilgangi.

Rafræn reikningsfærsla getur auðveldað þér að ná eftirfarandi markmiðum:

- Fljótleg og auðveld aðlögun að lands-/svæðisbundnum kröfum
- Staðlaðar innleiðingar á lausnum rafrænnar reikningsfærslu
- Aukinn rekjanleiki skjalaferils
- Styttri innleiðingartími
- Minni heildarkostnaður á eignarhaldi (TCO)
- Auðveldar stillingar á skilgreiningum sem krefjast ekki kóðabreytinga
- Einfaldaðar grunnstillingarpakki
- Innbyggður útflutningur, innflutningur og samþætting og auðveld stækkunarhæfni við vinnslu á rafrænum reikningsskjölum
- Auðveld endurnýting á sömu skilgreiningum á útflutningi, innflutningi og samþættingu í mörgum fyrirtækjum

Til að nota rafrænna reikningsfærslu þarf að setja hana upp í verkinu þínu í Microsoft Dynamics Lifecycle Services (LCS). Næst skal fylgja uppsetningarferlinu til að kveikja á samþættingu við Finance and Supply Chain Management. Frekari upplýsingar eru í [Hafist handa með rafrænar reikningsfærslur](e-invoicing-get-started.md).

## <a name="service-availability"></a><a name="availability"></a>Framboð þjónustu

Sem stendur er rafræn reikningsfærsla tiltæk fyrir viðskiptavini í gegnum forskoðunarforritið og í næsta áfanga verður þjónustan almennt tiltæk. Vegna þess að virkni sem tengist lands-/svæðisbundnum kröfum kann að vera takmörkuð á mismunandi stigum útgáfunnar, ætti alltaf að athuga nýjustu fylgigögnin sem fjalla um umfang lausna sem eru háðar löndum/svæðum.

Rafræn reikningsfærsla er sett upp á eftirfarandi staðsetningum Azure:

- Bandaríkin
- Evrópa

> [!NOTE]
> Rafræn reikningsfærsla styður ekki uppsetningar á staðnum.

## <a name="extended-configurability"></a>Aukinn stillanleiki

Hægt er að nota rafræna reikningsfærslu í aðstæðum þar sem stofna þarf og senda rafrænt skjal til tilnefndra aðila. Hún er sérstaklega hönnuð til að keyra stillanlegt flæði í vinnsluaðgerðum, samkvæmt mótteknum gögnum. Stillingamöguleikarnir sem eru tiltækir í Finance og Supply Chain Management takmarkast við skjalabreytingar. Þjónustan eykur þessa valmöguleika með því að bæta við stillanlegri samþættingu sem er í boði í henni. Auk þess nota allar aðgerðir rafrænna reikninga sem voru áður í boði, t.d. brasilískar Nota fiscal eletrônica (NF-e), mexíkóskar Comprobante Fiscal Digital por Internet (CFDI) eða aðrar vestur-evrópskar Universal Business Language (UBL)/Pan-European Public Procurement OnLine (PEPPOL) aðgerðir, skilgreiningar fyrir útflutning og innflutning og til að virkja samþættingar við ytri vefþjónustur.

## <a name="feature-highlights"></a>Helstu atriði eiginleika

- Tilbúin samþætting við Finance og Supply Chain Management
- Samræmd notendaupplifun fyrir skilgreiningu og eftirlit á ferli rafrænna reikninga fyrir öll lönd og svæði
- Hraðari, auðveldari og ódýrari aðlögun á rafrænni reikningsfærsluviðbót í nýjum löndum og svæðum
- Skilgreining þjónustunnar í gegnum Regulatory Configuration Service (RCS) og uppsetningu altækra eiginleika
- Viðskiptagögnum breytt í margs konar snið rafrænna reikninga (XML, JavaScript Object Notation \[JSON\], TXT og gildi aðskilin með kommu \[CSV\]) með því að nota stillingar sem eru skilgreindar í RCS:

    - Snið rafrænnar skýrslugerðar sem eru í boði fyrir lönd og svæði þar sem stillanleiki fyrir breytingu á rafrænum reikningi er ekki í boði

- Stillanleg innsending á rafrænum reikningum til vefþjónusta, þ.m.t. meðhöndlun vottorða í gegnum stafræna undirskrift:

    - Innbyggð, auðveldlega stækkanleg og stillanleg samþætting við viðbótarefni fyrir ýmis lönd

    > [!NOTE]
    > Sem stendur er takmarkaður fjöldi beinna innsendingar studdur. Frekari upplýsingar er að finna í hlutanum [Þjónustuframboð](#availability) fyrr í þessu efnisatriði. Stuðningur verður lengdur í framtíðinni.

- Meðhöndlun svara frá vefþjónustum, þ.m.t. meðhöndlun á stillanlegum undantekningarboðum
- Stuðningur við rafrænar undirskriftir (til dæmis með því að nota reiknirit XMLDSig-undirskriftar)
- Runuvinnsla á skilaboðum rafrænna reikninga

## <a name="architecture-and-data-flow"></a>Skipulag og gagnaflæði

Þegar rafrænni reikningsfærslu hefur verið sett upp úr LCS og nauðsynlegri uppsetningu er lokið í öllum nauðsynlegum forritum, er öruggri tengingu komið á. Þjónustan er nú staðsett í gagnamiðstöðvum í Bandaríkjunum og Evrópu. Þess vegna gæti staðsetning þjónustunnar verið önnur en staðsetning tengdrar tilvika af Finance og Supply Chain Management. Þegar búið er að ljúka uppsetningu á rafrænni reikningsfærslu og kveikja á samþættingu, í hvert sinn sem rafrænn reikningur er sendur, verða aðalgögn og færslugögn sem tengjast tilteknu skjali send til rafrænnar reikningsfærslu.

> [!NOTE]
> Ef rafrænn reikningur eða annað skjal inniheldur persónuupplýsingar, skal staðfesta að þessi eiginleiki sem er notaður uppfylli skilyrði almennu persónuverndarreglugerðarinnar og annarra reglugerða sem tengjast flutningi persónuupplýsinga.

### <a name="high-level-description-of-the-data-flow"></a>Mjög ítarleg lýsing á gagnaflæði

1. Biðlarinn sendir viðurkennt viðskiptaskjal til þjónustunnar.
2. Á grundvelli samhengisupplýsinga sem eru mótteknar frá biðlaranum, velur þjónustan viðeigandi úrvinnsluflæði.
3. Þjónustan keyrir vinnsluaðgerðirnar. Þessar aðgerðir gætu falið í sér breytingu á viðskiptaskjalinu í rafrænan reikningi, nota rafræna undirskrift og senda skjalið til ytri vefþjónustu.
4. Öll móttekin og unnin skjöl eru geymd í Azure Blob geymslu viðskiptavinar.
5. Allir leynilyklar og vottorð leigjandans sem voru notuð í úrvinnslu eru geymd í Azure-lyklageymslu viðskiptavinarins.
6. Þjónustan veitir upplýsingar samkvæmt eftirspurn til biðlarans um vinnslustöðu viðskiptaskjalsins sem var sent.
7. Biðlarinn tekur við upplýsingum um lokna vinnslu og gerir allar kladdaupplýsingar tiltækar. Hún gerir einnig skjalið sem var stofnað eða móttekið í vinnsluflæðinu tiltækt.

Eftirfarandi mynd sýnir hvernig gögn streyma til og frá rafrænni reikningsfærslu.

![Gagnaflæði fyrir rafræna reikningsfærslu.](media/e-invoicing-service-data-flow-diagram-overview.png)

## <a name="privacy-notice"></a>Tilkynning um persónuvernd
Við virkjun og notkun rafrænnar reikningsfærslu þarf hugsanlega að senda takmörkuð gögn, sem fela í sér skattskráningarkenni fyrirtækisins. Þetta verður sent til stofnanir þriðja aðila sem skattyfirvöld heimila að megi senda rafræna reikninga til þessara skattyfirvalda á fyrirframskilgreindu sniði sem þarf fyrir samþættingu við vefþjónustu yfirvalda. Gögn sem eru flutt inn úr þessum ytri kerfum í þessa Dynamics 365-netþjónustu falla undir [yfirlýsingu okkar um persónuvernd](https://go.microsoft.com/fwlink/?LinkId=512132). Frekari upplýsingar er að finna í köflunum um persónuverndaryfirlýsingu í fylgiskjölum um eiginleika eftir löndum.

## <a name="additional-resources"></a>Frekari upplýsingar
- [Þjónustustjórnun](e-invoicing-service-administration.md)
- [Skilgreina rafræna reikninga í RCS](e-invoicing-configuration-rcs.md)
- [Gefa út rafræna reikninga í Finance and Supply Chain Management](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
