---
title: Stækka Talent með Power Apps og Power Automate
description: Þessi grein lýsir sumum dæmum um atburðarás stækkunarhæfni fyrir Microsoft Dynamics 365 Talent - Attract sem notar Microsoft Power Apps og Microsoft Power Automate.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: cfdf36e9486aa4853d3bf674afa73ec3a4d1c161
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529635"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a>Stækka Talent með Power Apps og Power Automate

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Þessi grein lýsir sumum dæmum um atburðarás stækkunarhæfni fyrir Microsoft Dynamics 365 Talent: Attract sem notar Microsoft Power Apps og Microsoft Power Automate. Hægt er að flytja lausnapakkann sem tengist hverju dæmi inn í Power Apps-umhverfið. Síðan er hægt að nota pakkana annaðhvort sem leiðarvísi eða sem upphafspunkta til að innleiða atburðarásir sem eiga við um fyrirtækið þitt.

> [!IMPORTANT]
> Ef þú vilt nota sniðmátin og forritið sem lýst er í þessari grein „eins og það er“, skaltu vera viss um að prófa þau til að ganga úr skugga um þau nái utan um allar atburðarásirnar sem tengjast innleiðingunni þinni.


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

Í Microsoft Dynamics 365: Attract er hægt að nota skjámyndir í umsækjendagátt, þar sem umsækjendur fylla út upplýsingar. Einnig er hægt að fella inn skjámyndir sem verkþætti í starfssniðmáti.

Þegar umsækjandi sendir inn eyðublað, sækir Microsoft Power Automate innsent eyðublaðið, les gögnin og geymir þau í Common Data Service-einingunni.

Til að sækja sniðmátið **Power Automate - Skjámynd Connect** og sérsniðna skipulagseiningu skal fara í [Power Automate - Skjámynd Connect](https://go.microsoft.com/fwlink/?linkid=2081988) í Microsoft Download Center.

## <a name="power-automate--sharepoint-integration"></a>Power Automate – SharePoint samþætting

Hægt er að nota sniðmátið **Power Automate – SharePoint samþætting** til að lesa gögn úr Microsoft SharePoint-lista, bera listann saman við reitagildi fyrir allar Common Data Service-einingar og senda niðurstöður samanburðar sem tilkynningapóst. 

Fyrirtæki gæti verið með einhverja hæfni sem þarf nauðsynlega að uppfylla. Þessa hæfni er hægt að geyma í SharePoint sem SharePoint-lista. Þegar umsækjandi sækir um eitthvað starf þar sem ákveðin hæfni er tekin fram er tilkynningapóstur sendur ef góð samsvörun er milli hæfni umsækjanda og hæfninnar sem geymd er í SharePoint. Þannig er fyllt hraðar upp í stöður sem þarf nauðsynlega að ráða í, því að tilkynningarnar hjálpa ráðningaraðilum að endurráða umsækjendur innan fyrirtækisins.

Hægt er að stækka þetta sniðmát svo nota megi það fyrir atburðarás sem hefur með SharePoint-samþættingu að gera.

Til að hlaða niður sniðmátinu **Power Automate - SharePoint samþætting** skal fara í [Power Automate - SharePoint samþætting](https://go.microsoft.com/fwlink/?linkid=2082109) í Microsoft Download Center.

## <a name="referral-app"></a>Tilvísunforrit

Hægt er að nota tilvísunarforritið til að bæta við umbjóðendum í sameiginlegt hæfileikasafn. Tilvísandi getur fært inn **Fornafn**, **Eftirnafn**, **Netfang** og **Slóð í LinkedIn** við framlagningu umsækjanda. Lýsigögn umsækjandans eru síðan fyllt út með upplýsingum tilvísunaraðila.

Hægt er að fella þetta forrit inn í starfsmannaþjónustuna til að senda tilvísanir, eða nota það sem tengil á fyrirtækjagáttina og keyra það sem sjálfstætt forrit.

Til að sækja **forritið Referral** ferðu í [Dynamics 365 Talent viðbótarlausnina: Referral App](https://www.microsoft.com/download/details.aspx?id=58497) í Microsoft Download Center. Þú getur flutt þetta forrit inn og sérsniðið það til að bæta við viðbótarvirkni.

## <a name="additional-resources"></a>Frekari upplýsingar

[Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[Flytja forrit á milli leigjenda og umhverfa](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)


[!INCLUDE[footer-include](../includes/footer-banner.md)]