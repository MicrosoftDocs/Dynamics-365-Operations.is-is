---
title: Auka virkni Talent með því að nota PowerApps og Microsoft Flow – dæmi um atburðarásir
description: Þetta efnisatriði lýsir sumum dæmum um atburðarás stækkunarhæfni fyrir Microsoft Dynamics 365 for Talent sem notar Microsoft PowerApps og Microsoft Flow.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 for Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c113b0f4ab2c8e44d00fcfca3f0a6ca828a854ae
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518254"
---
# <a name="extend-talent-by-using-powerapps-and-microsoft-flow---example-scenarios"></a>Auka virkni Talent með því að nota PowerApps og Microsoft Flow – dæmi um atburðarásir

Þetta efnisatriði lýsir sumum dæmum um atburðarás stækkunarhæfni fyrir Microsoft Dynamics 365 for Talent sem notar Microsoft PowerApps og Microsoft Flow. Hægt er að flytja lausnapakkann sem tengist hverju dæmi inn í PowerApps umhverfið þitt. Síðan er hægt að nota pakkana annaðhvort sem leiðarvísi eða sem upphafspunkta til að innleiða atburðarásir sem eiga við um fyrirtækið þitt.

> [!IMPORTANT]
> Ef þú vilt nota sniðmátin og forritið sem lýst er í þessu efnisatriði „eins og það er“, skaltu vera viss um að prófa þau til að ganga úr skugga um þau nái utan um allar atburðarásirnar sem tengjast innleiðingunni þinni.


## <a name="prerequisites"></a>Forkröfur

- Til að flytja inn pakka verða notendur að hafa heimildina **Umhverfishönnuður**.
- Til að flytja forrit út eða inn verða notendur að hafa PowerApps Plan 2 leyfi eða PowerApps Plan 2 prufuleyfi.

## <a name="flow--form-connect"></a>Flæði - Tengja skjámynd

Sniðmátið **Flæði - Tengja skjámynd** er hægt að nota til að lesa gögn úr Microsoft Forms og vista þau í Common Data Service einingunni.

Þetta sniðmát er hægt að framlengja þannig að hægt sé að nota það í öðrum atburðarásum. Hér eru nokkur dæmi:

- Sækja mat á umsækjanda.
- Sækja niðurstöður úr spurningalistum námskeiðs.
- Taka saman safn af viðtalsspurningum fyrir mannauðsstjóra.
- Sækja mat umsækjanda á viðtalsferlinu

Í Microsoft Dynamics 365: Attract, skjámyndir geta birst í umsækjendagátt og umsækjendur geta fyllt út upplýsingar. Einnig er hægt að fella inn skjámyndir sem verkþætti í starfssniðmáti.

Þegar umsækjandi sendir inn eyðublað, sækir Microsoft Flow innsent eyðublaðið, les gögnin og geymir þau í Common Data Service-einingunni.

Til að niðurhala sniðmátinu **Flæði - Tengja skjámynd** og sérsniðinni skipulagseiningu skal fara í [Flæði - Tengja skjámynd](https://go.microsoft.com/fwlink/?linkid=2081988) í Microsoft Download Center.

## <a name="initiate-and-extract-parameters-passed-to-powerapps"></a>Hefja og draga út færibreytur sem sendar eru til PowerApps

Sniðmátið **Hefja og draga út færibreytur sem sendar eru til PowerApps** er hægt að nota sem upphafspunkt fyrir allar atburðarásir PowerApps sem miðast við Attract. Það inniheldur allar sjálfgefnu færibreyturnar sem sendar til Attract, t.d. **Starfsumsókn**, **Auðkenni umsækjanda** og **Auðkenni starfs**.

Hægt er að nota þetta sniðmát til að sækja skjámynd fyrir mat á umsækjanda svo að ráðningarstjóri geti skoðað matið sem umsækjandi fyllti út.

Forrit sem eru búin til með því að nota PowerApps geta verið felld inn í starfssniðmátið í Attract.

Til að hlaða niður sniðmátinu **Hefja og draga út færibreytur sem sendar eru til PowerApps** og sérsniðna skipulagseiningu skal fara í [Hefja og draga út færibreytur sem sendar eru til PowerApps](https://go.microsoft.com/fwlink/?linkid=2081991) í Microsoft Download Center.

## <a name="integration-with-office-365"></a>Samþætting með Office 365

Forritið **Samþætting við Office 365** er hægt að nota til að draga út upplýsingar um hóp fyrir innskráða notendur úr Microsoft Office 365. Það vísar í starfskrafta í Talent til að draga út upplýsingar um inn- og útstimplun og færslur undantekninga. Upplýsingar um inn- og útstimplun eru geymdar í sérsniðnum Common Data Service-einingum. Gert er ráð fyrir að þessar upplýsingar séu fylltar inn úr kerfum þriðja aðila í gegnum samþættingu.

Þetta forrit er hægt að stækka þannig að hægt sé að nota það í öðrum atburðarásum. Til dæmis er hægt að nota það til að sýna upplýsingar um frí hóps, viðburði dagatals og alla viðburði sem tengjast hópnum.

Til að hlaða niður forritinu **Samþætting við Office 365** og sérsniðnu skipulagseininguna skal fara í [Samþætting við Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) í Microsoft Download Center.

## <a name="flow--email-notification"></a>Flæði - Tilkynning í tölvupósti

Sniðmátið **Flæði - Tilkynning í tölvupósti** er hægt að nota í atburðarásum tölvupóststilkynningar. Hægt er að nota það til að ræsa tilkynningapósta til umsækjenda sem ráðningarhópurinn hafnar einhvern tímann á stigi ráðningarferlis.

Hægt er að stækka sniðmátið til að fylgjast með breytingum á stigi umsækjanda í gegnum ráðningarferlið, og til að senda tilkynningapósta á ráðningarhóp og umsækjanda.

Almennt, fyrir einingar sem eru geymdar í Common Data Service, er hægt að setja upp flæði til að senda tilkynningar á viðburðum sem eiga sér stað í Core HR, Attract eða Dynamics 365 Talent: Onboard.

Til að hlaða niður sniðmátinu **Flæði - Tilkynning í tölvupósti** skal fara í [Flæði - Tilkynning í tölvupósti](https://go.microsoft.com/fwlink/?linkid=2082103) í Microsoft Download Center.

## <a name="flow--sql-connect-and-execute"></a>Flæði - Tengja og keyra SQL

Sniðmátið **Flæði - Tengja og keyra SQL** tengist við Microsoft SQL Server og virkjar keyrslu á SQL-fyrirspurnum.

Þótt þetta sniðmát sé hannað til að lesa og uppfæra SQL-töflur, er hægt að stækka það til að nota við aðrar kringumstæður. Til dæmis er hægt að nota það til að fylla út millistigsvistunartöflu í Common Data Service með skrám úr SQL-þjóni, og til að gera reglubundna samstillingu á millistigsvistunartöflu með því að nota stigvaxandi færslu úr SQL-þjóni.

Til að hlaða niður sniðmátinu **Flæði - Tengja og keyra SQL** skal fara í [Flæði - Tengja og keyra SQL](https://go.microsoft.com/fwlink/?linkid=2081789) í Microsoft Download Center.

## <a name="flow--sharepoint-integration"></a>Flæði - SharePoint Samþætting

Hægt er að nota sniðmátið **Flæði - SharePoint samþætting** til að lesa gögn úr Microsoft SharePoint-lista, bera listann saman við reitagildi fyrir allar Common Data Service-einingar og senda niðurstöður samanburðar sem tilkynningapóst. 

Fyrirtæki gæti verið með einhverja hæfni sem þarf nauðsynlega að uppfylla. Þessa hæfni er hægt að geyma í SharePoint sem SharePoint-lista. Þegar umsækjandi sækir um eitthvað starf þar sem ákveðin hæfni er tekin fram er tilkynningapóstur sendur ef góð samsvörun er milli hæfni umsækjanda og hæfninnar sem geymd er í SharePoint. Þannig er fyllt hraðar upp í stöður sem þarf nauðsynlega að ráða í, því að tilkynningarnar hjálpa ráðningaraðilum að ná til og endurráða umsækjendur innan fyrirtækisins.

Hægt er að stækka þetta sniðmát svo nota megi það fyrir atburðarás sem hefur með SharePoint-samþættingu að gera.

Til að hlaða niður sniðmátinu **Flæði - SharePoint samþætting** skal fara í [Flæði - SharePoint samþætting](https://go.microsoft.com/fwlink/?linkid=2082109) í Microsoft Download Center.

## <a name="admin-console-to-manage-talent-pools"></a>Stjórnborð stjórnanda til að hafa umsjón með hæfileikasöfnum

Þegar kveikt er á samþættingu við LinkedIn, stofnar Attract sjálfkrafa LinkedIn-hæfileikasafn. Þegar ráðningaraðili skiptir á InMail við nýjan starfsmann í gegnum LinkedIn býr Attract til notandasíðu fyrir starfsmanninn og hann verður að meðlimi í hæfileikasafni LinkedIn. Þetta PowerApps-forrit er gagnlegt til að endurskipuleggja umsækjendur í hæfileikasöfnum á grunni hæfni.

Keyra þetta PowerApps-forrit á stjórnborði stjórnanda til að framkvæma eftirfarandi verk:

- Birta umsækjendur í hæfileikasafni
- Bæta við og fjarlægja umsækjendur úr hæfileikasafni
- Færa umsækjendur úr einu hæfileikasafni í annað
- Ákveða hvort umsækjendur séu þegar hluti af hæfileikasafni áður en þeir eru færðir
- Athuga hæfni umsækjenda áður en þeir eru færðir í önnur hæfileikasöfn

Þetta PowerApps-forrit notar margþætt samskipti svo hægt sé að nota það sem sniðmát fyrir aðrar atburðarásir þar sem er nauðsynlegt að draga út færslur sem eru með margþætt samskipti.

Til að sækja sniðmátið **Stjórnborð stjórnanda til að hafa umsjón með hæfileikasöfnum** skal opna [Stjórnborð stjórnanda til að hafa umsjón með hæfileikasöfnum](http://www.microsoft.com/downloads/details.aspx?FamilyID=780a5eee-0e2a-4159-9a83-009f9ccdc469) í Microsoft Download Center.

## <a name="additional-resources"></a>Frekari upplýsingar

[ Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[Flytja forrit á milli leigjenda og umhverfa](https://docs.microsoft.com/en-us/power-platform/admin/environment-and-tenant-migration)
