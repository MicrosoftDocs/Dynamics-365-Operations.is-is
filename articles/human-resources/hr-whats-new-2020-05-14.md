---
title: Hvað er nýtt eða breytt í Dynamics 365 Human Resources (14. maí 2020)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d46671f73a75a9ed3a652d76153c923a3542b5f6
ms.sourcegitcommit: 7c750711e9fe1d3726c6ee650669529684933001
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386108"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-14-2020"></a>Hvað er nýtt eða breytt í Dynamics 365 Human Resources (14. maí 2020)

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Dynamics 365 Human Resources. Breytingar eiga við um byggingarnúmer 8.1.3244. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera í Lifecycle Services (LCS) vegna tilvísunar.

## <a name="platform-changes"></a>Verkvangsbreytingar

Breytingar á verkvangi eru teknar með í útgáfu þessarar viku. Frekari upplýsingar er að finna í [Verkvangsuppfærslur fyrir útgáfu 10.0.10 af Finance and Operations -forritum (maí 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34). Þessi útgáfa inniheldur villuleiðréttingar og breytingar á vistuðum yfirlitum.
 
## <a name="ensure-common-data-service-picklists-are-consistent-with-leave-enums-436343"></a>Tryggið að tínslulistar Common Data Service séu í samræmi við fasttexta leyfa (436343)

Tínslulistar Common Data Service eru nú í samræmi við fasttexta leyfa.

## <a name="allow-users-to-configure-leave-request-workflow-based-on-the-request-amount-300044"></a>Leyfa notendum að grunnstilla verkflæði leyfisbeiðna út frá umbeðnu magni (300044)

Notendur geta skilgreint verkflæði leyfisbeiðna út frá umbeðnu magni.
 
## <a name="new-worker-form-exposes-data-through-the-view-menu-when-advanced-security-is-enabled-403185"></a>Nýtt eyðublað starfskrafts birtir gögn í gegnum Skoðunarvalmynd þegar Ítarlegar öryggisstillingar eru virkar (403185)

Þessi útgáfa leiðréttir hvernig skoðun starfsmanna milli lögaðila virkar þegar ítarlegur aðgangur er virkur og starfsmenn í öðrum fyrirtækjum eru aðgengilegir.

## <a name="allow-running-leave-accruals-for-a-single-plan-or-a-single-company-318844"></a>Leyfa keyrslu uppsafnaðra leyfa fyrir eina áætlun eða eitt fyrirtæki (318844)

Með þessari breytingu er hægt að keyra uppsöfnun fyrir fyrirtæki eða áætlun.
 
## <a name="show-the-positions-full-time-equivalent-fte-in-the-enrolled-workers-form-414658"></a>Sýna jafngildi stöðunnar í fullu starfi (FTE) á skjámyndinni „skráðir starfsmenn“ (414658)

FTE-gildi fyrir stöðu starfsmanns ákvarðar uppsöfnun réttinda starfsmanns þegar valkosturinn FTE er virkur í leyfisgerðinni. Þessi reitur er nú hafður með í skjámyndinni **„Skráðir starfsmenn“** og svarglugganum **„Fjöldaskráning“**.

## <a name="add-leave-balance-expiration-batch-job-431266"></a>Bæta við lokarunuvinnslu leyfisstöðu (431266)

Ný runuvinnsla er nú tiltæk sem keyrir daglega. Það styttir eftirstandandi leyfisstöðu þegar lokadagsetningar verða gildandi.

## <a name="exporting-personal-contacts-for-an-employee-using-the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-the-parent-relationship-type-345893"></a>Við útflutning persónulegs tengiliðs fyrir starfsmann með einingunni Persónulegur tengiliður starfsmanns eru persónulegir tengiliðir af venslagerðinni Yfireining ekki fluttir út (345893)

Gagnaeiningin **Persónulegur tengiliður starfsmanns** (**HcmPersonalContactPersonEntity** í DMF og **PersonalContactPerson** í OData) gat ekki flutt út persónulega tengiliði sem er með venslagerðina **Yfireining**. Þetta atriði er fast fyrir persónulega tengiliði sem stofnaðir eru eftir þessa breytingu. Fyrirliggjandi persónulegir tengiliðir af gerðinni **Yfireining** verða fastir í nýrri útgáfu.

## <a name="reason-codes-display-across-different-scenarios-when-theyre-marked-as-leave-and-absence-and-the-streamlined-employee-form-is-enabled-434163"></a>Ástæðukóðar birtast í mismunandi aðstæðum þegar þeir eru merktir sem „leyfi og fjarvistir“ og einfölduð skjámynd starfsmanns er virk (434163)

Þessi breyting takmarkar ástæðukóðana við leyfis-og fjarvistakóða þegar einfaldaður innsláttur starfsmanns er virkur.

## <a name="the-preview-feature-assign-a-leave-plan-to-employees-in-the-future-displays-error-433555"></a>Forskoðunareiginleikinn „Úthluta leyfisáætlun til starfsmanna í framtíðinni“ sýnir villu (433555)

Þessi breyting leiðréttir villu þegar tveimur leyfisgerðum hefur verið úthlutað á leyfisáætlun og reynt er að úthluta starfsmanni.

## <a name="getting-started-banner-appears-for-all-users-441731"></a>Borðarnir „Hafist handa“ birtast fyrir alla notendur (441731)

Með þessari breytingu er borðinn „Hafist handa“ falinn fyrir notendum sem eru ekki kerfisstjórar eða stjórnendur gagnastjórnunar. 

## <a name="the-common-data-service-worker-address-entity-works-differently-in-terms-of-date-time-effective-dates-in-human-resources-425071"></a>Einingin Common Data Service póstfang starfsmanns vinnur á annan hátt að því er varðar dagsetningar gildisdagsetninga í Mannauði (425071)

Þessi breyting heldur upplýsingum um aðsetur jöfnuðum í vissum aðstæðum, með hliðsjón af dagsetningum aðseturs.

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-425407"></a>Ekki er hægt að bæta viðhengi við samþykkta beiðni um leyfi (425407)

Í útgáfu þessarar viku er hægt að bæta viðhengjum við samþykktar beiðnir um leyfi án þess að breyta leyfisbeiðninni.

## <a name="in-preview"></a>Í kynningarútgáfu

## <a name="leave-suspension"></a>Frestun leyfis

Þú getur frestað leyfi og fjarvistum í Human Resources fyrir starfsmann. Frestun leyfis stöðvar leyfisuppsöfnun fyrir valdar leyfisgerðir. Ef frestunin á sér stað eftir að uppsöfnun hefur verið unnin skapar frestun leyfis hlutfallslega leiðréttingu á leyfisstöðu starfsmanns. Frekari upplýsingar eru í [Fresta leyfi](hr-leave-and-absence-suspend-leave.md).

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>Uppfæra notendaupplifun til að sýna að uppsöfnun sé frestað (429550)

Notandaupplifunin sýnir nú að uppsöfnun hafi verið frestað fyrir áætlun.

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a>Uppsafnað leyfi í bið fyrir tilteknar leyfisgerðir (272447)

Í þessari útgáfu getur mannauður búið til reglu til að fresta uppsöfnun leyfis fyrir starfsmenn með beiðnum um leyfi sem færðar eru inn fyrir ógreitt leyfi. Ógreit leyfi getur verið gerð, en þarf ekki að vera það. Hægt er að fresta öllu leyfi út frá gerð annarrar leyfisgerðar.

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a>DMF-eining er í boði fyrir frestun uppsöfnunar (429549)

DMF-eining er ekki til staðar fyrir uppsöfnun í bið.

## <a name="add-reason-code-to-accrual-suspensions-429547"></a>Bæta ástæðukóða við frestun uppsöfnunar (429547)

Ástæðukóðum hefur verið bætt við uppsöfnun í bið.

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a>Hefja flutning úr færibreytum Human Resources í færibreytur leyfis og fjarvista

Þessi útgáfa byrjar á að sameina færibreytur mannauðsstjórnunar með færibreytum leyfis og fjarvista.

## <a name="carry-forward-rules"></a>Yfirfærslureglur

Hægt er að tilgreina yfirfærsluorlofsgerð fyrir yfirfærslustöður þar sem yfirfærsluleiðréttingar eru fluttar. Til dæmis, ef starfsmaður yfirfærir 10 daga getur þú valið aðra leyfisgerð fyrir þessa 10 daga. Fyrir frekari upplýsingar, sjá [Grunnstilla gerðir leyfis og fjarvista](hr-leave-and-absence-types.md).
