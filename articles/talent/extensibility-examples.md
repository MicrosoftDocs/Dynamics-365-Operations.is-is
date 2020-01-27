---
title: Stækka Talent með Power Apps og Power Automate
description: Þetta efnisatriði lýsir sumum dæmum um atburðarás stækkunarhæfni fyrir Microsoft Dynamics 365 Talent sem notar Microsoft Power Apps og Microsoft Power Automate.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 Talent;PowerApps;Flow;Common Data Service
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
ms.openlocfilehash: 6c8a583a93c2ceb70d8c3b0e0047e2bf2047b56d
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898318"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a>Stækka Talent með Power Apps og Power Automate

Þetta efnisatriði lýsir sumum dæmum um atburðarás stækkunarhæfni fyrir Microsoft Dynamics 365 Talent sem notar Microsoft Power Apps og Microsoft Power Automate. Hægt er að flytja lausnapakkann sem tengist hverju dæmi inn í Power Apps-umhverfið. Síðan er hægt að nota pakkana annaðhvort sem leiðarvísi eða sem upphafspunkta til að innleiða atburðarásir sem eiga við um fyrirtækið þitt.

> [!IMPORTANT]
> Ef þú vilt nota sniðmátin og forritið sem lýst er í þessu efnisatriði „eins og það er“, skaltu vera viss um að prófa þau til að ganga úr skugga um þau nái utan um allar atburðarásirnar sem tengjast innleiðingunni þinni.


## <a name="prerequisites"></a>Forkröfur

- Til að flytja inn pakka verða notendur að hafa heimildina **Umhverfishönnuður**.
- Til að flytja forrit út eða inn verða notendur að hafa Power Apps Plan 2 leyfi eða Power Apps Plan 2 prufuleyfi.

## <a name="power-automate--form-connect"></a>Power Automate - Skjámynd Connect

Sniðmátið **Power Automate - Skjámynd Connect** er hægt að nota til að lesa gögn úr Microsoft Forms og vista þau í einingunni Common Data Service.

Þetta sniðmát er hægt að framlengja þannig að hægt sé að nota það í öðrum atburðarásum. Hér eru nokkur dæmi:

- Sækja mat á umsækjanda.
- Sækja niðurstöður úr spurningalistum námskeiðs.
- Taka saman safn af viðtalsspurningum fyrir mannauðsstjóra.
- Sækja mat umsækjanda á viðtalsferlinu

Í Microsoft Dynamics 365: Attract, skjámyndir geta birst í umsækjendagátt og umsækjendur geta fyllt út upplýsingar. Einnig er hægt að fella inn skjámyndir sem verkþætti í starfssniðmáti.

Þegar umsækjandi sendir inn eyðublað, sækir Microsoft Power Automate innsent eyðublaðið, les gögnin og geymir þau í Common Data Service-einingunni.

Til að sækja sniðmátið **Power Automate - Skjámynd Connect** og sérsniðna skipulagseiningu skal fara í [Power Automate - Skjámynd Connect](https://go.microsoft.com/fwlink/?linkid=2081988) í Microsoft Download Center.

## <a name="initiate-and-extract-parameters-passed-to-power-apps"></a>Hefja og draga út færibreytur sem sendar eru í Power Apps

Sniðmátið **Hefja og draga út færibreytur sem sendar eru til Power Apps** er hægt að nota sem upphafspunkt fyrir allar atburðarásir Power Apps sem miðast við Attract. Það inniheldur allar sjálfgefnu færibreyturnar sem sendar til Attract, t.d. **Starfsumsókn**, **Auðkenni umsækjanda** og **Auðkenni starfs**.

Hægt er að nota þetta sniðmát til að sækja skjámynd fyrir mat á umsækjanda svo að ráðningarstjóri geti skoðað matið sem umsækjandi fyllti út.

Forrit sem eru búin til með því að nota Power Apps geta verið felld inn í starfssniðmátið í Attract.

Til að hlaða niður sniðmátinu **Hefja og draga út færibreytur sem sendar eru í Power Apps** og sérsniðna skipulagseiningu skal fara í [Hefja og draga út færibreytur sem sendar eru í Power Apps](https://go.microsoft.com/fwlink/?linkid=2081991) í Microsoft Download Center.

## <a name="integration-with-office-365"></a>Samþætting með Office 365

Forritið **Samþætting við Office 365** er hægt að nota til að draga út upplýsingar um hóp fyrir innskráða notendur úr Microsoft Office 365. Það vísar í starfskrafta í Talent til að draga út upplýsingar um inn- og útstimplun og færslur undantekninga. Upplýsingar um inn- og útstimplun eru geymdar í sérsniðnum Common Data Service-einingum. Gert er ráð fyrir að þessar upplýsingar séu fylltar inn úr kerfum þriðja aðila í gegnum samþættingu.

Þetta forrit er hægt að stækka þannig að hægt sé að nota það í öðrum atburðarásum. Til dæmis er hægt að nota það til að sýna upplýsingar um frí hóps, viðburði dagatals og alla viðburði sem tengjast hópnum.

Til að hlaða niður forritinu **Samþætting við Office 365** og sérsniðnu skipulagseininguna skal fara í [Samþætting við Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) í Microsoft Download Center.

## <a name="power-automate--email-notification"></a>Power Automate – Tölvupósttilkynning

Sniðmátið **Power Automate - Tilkynning í tölvupósti** er hægt að nota í atburðarásum tölvupóststilkynningar. Hægt er að nota það til að ræsa tilkynningapósta til umsækjenda sem ráðningarhópurinn hafnar einhvern tímann á stigi ráðningarferlis.

Hægt er að stækka sniðmátið til að fylgjast með breytingum á stigi umsækjanda í gegnum ráðningarferlið, og til að senda tilkynningapósta á ráðningarhóp og umsækjanda.

Almennt, fyrir einingar sem eru geymdar í Common Data Service, er hægt að setja upp flæði til að senda tilkynningar á viðburðum sem eiga sér stað í Core HR, Attract eða Onboard.

Til að hlaða niður sniðmátinu **Power Automate - Tilkynning í tölvupósti** skal fara í [Power Automate - Tilkynning í tölvupósti](https://go.microsoft.com/fwlink/?linkid=2082103) í Microsoft Download Center.

## <a name="power-automate--sql-connect-and-execute"></a>Power Automate - SQL Connect og framkvæmd

Sniðmátið **Power Automate - SQL Connect og framkvæmd** tengist við Microsoft SQL Server og virkjar keyrslu á SQL-fyrirspurnum.

Þótt þetta sniðmát sé hannað til að lesa og uppfæra SQL-töflur, er hægt að stækka það til að nota við aðrar kringumstæður. Til dæmis er hægt að nota það til að fylla út millistigsvistunartöflu í Common Data Service með skrám úr SQL-þjóni, og til að gera reglubundna samstillingu á millistigsvistunartöflu með því að nota stigvaxandi færslu úr SQL-þjóni.

Til að hlaða niður sniðmátinu **Power Automate - SQL Connect og framkvæmd** skal fara í [Power Automate - SQL Connect og framkvæmd](https://go.microsoft.com/fwlink/?linkid=2081789) í Microsoft Download Center.

## <a name="power-automate--sharepoint-integration"></a>Power Automate – SharePoint samþætting

Hægt er að nota sniðmátið **Power Automate – SharePoint samþætting** til að lesa gögn úr Microsoft SharePoint-lista, bera listann saman við reitagildi fyrir allar Common Data Service-einingar og senda niðurstöður samanburðar sem tilkynningapóst. 

Fyrirtæki gæti verið með einhverja hæfni sem þarf nauðsynlega að uppfylla. Þessa hæfni er hægt að geyma í SharePoint sem SharePoint-lista. Þegar umsækjandi sækir um eitthvað starf þar sem ákveðin hæfni er tekin fram er tilkynningapóstur sendur ef góð samsvörun er milli hæfni umsækjanda og hæfninnar sem geymd er í SharePoint. Þannig er fyllt hraðar upp í stöður sem þarf nauðsynlega að ráða í, því að tilkynningarnar hjálpa ráðningaraðilum að ná til og endurráða umsækjendur innan fyrirtækisins.

Hægt er að stækka þetta sniðmát svo nota megi það fyrir atburðarás sem hefur með SharePoint-samþættingu að gera.

Til að hlaða niður sniðmátinu **Power Automate - SharePoint samþætting** skal fara í [Power Automate - SharePoint samþætting](https://go.microsoft.com/fwlink/?linkid=2082109) í Microsoft Download Center.

## <a name="referral-app"></a>Tilvísunforrit
Hægt er að nota tilvísunarforritið til að bæta við umbjóðendum í sameiginlegt hæfileikasafn. Tilvísandi getur fært inn **Fornafn**, **Eftirnafn**, **Netfang** og **Slóð í LinkedIn** við framlagningu umsækjanda. Lýsigögn umsækjandans eru síðan fyllt út með upplýsingum tilvísunaraðila.

Hægt er að fella þetta forrit inn í starfsmannaþjónustuna (ESS) til að senda tilvísanir, eða nota það sem tengil á fyrirtækjagáttina og keyrt sem sjálfstætt forrit.

Til að sækja **forritið Referral** ferðu í [Dynamics 365 Talent viðbótarlausnina: Referral App](https://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) í Microsoft Download Center. Þú getur flutt þetta forrit inn og sérsniðið það til að bæta við viðbótarvirkni.

## <a name="additional-resources"></a>Frekari upplýsingar

[Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[Flytja forrit á milli leigjenda og umhverfa](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
