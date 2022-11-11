---
title: Kyngrunnur enum stækkanleiki
description: Þessi grein veitir yfirlit yfir stækkanleika kynjagrunntalningarinnar (enum).
author: twheeloc
ms.date: 05/23/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.custom:
- "51941"
- intro-internal
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 61a80c16d24d8fda264340d79ed393db3f635908
ms.sourcegitcommit: 1717ff6af1879c6f3a8360936c42ecf55f86acd0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/07/2022
ms.locfileid: "9749301"
---
# <a name="gender-base-enum-extensibility"></a>Kyngrunnur enum stækkanleiki

The **Kyn** upptalning (enum) er nú stækkanleg. Þessi grein lýsir þeim breytingum sem þú verður að gera á kóðagrunninum ef þú ætlar að framlengja **Kyn** enum.

## <a name="gender-vs-hcmpersongender"></a>Kyn vs HcmPersonKyn

Það eru tvær upptalningar fyrir kynjagildi:

- **Kyn** (Umsóknarvettvangur)
- **HcmPersonGender** (Starfsmannastjórnun)

The **Kyn** enum er notað í gegn Microsoft Dynamics 365 Fjármál, en **HcmPersonGender** er sértækt fyrir virkni mannauðsstjórnunar (HCM). Ef þú ert að nota HCM virkni og þú gerir einhverjar breytingar á **Kyn** enum, þú ættir að íhuga að gera sömu breytingar á **HcmPersonGender**. Til dæmis ef þú bætir við **Transgender** til **Kyn** enum, bæta við **Transgender** til **HcmPersonGender** enum líka.

## <a name="hcmpersongendertranformutil-class"></a>HcmPersonGenderTransformUtil (Class)

Nýtt **HcmPersonGenderTransformUtil** flokkur var búinn til til að leyfa þýðingar á milli grunntalninganna tveggja. Í þessum flokki eru tvær aðferðir: **convertGenderToHcmPersonGender** og **convertHcmPersonGenderToGender**. Þú ættir að búa til viðbót með því að nota **Goggunarröð** bekk eða **atburðastjórar**, og útvíkka báðar aðferðirnar til að kortleggja ný gildi sem bætast við annaðhvort grunntalninguna.

## <a name="payrollstatewagetaxprepdp-class"></a>PayrollStateWageTaxPrepDP (Class)

**PayrollStateWageTaxPrepDP** er gagnaveitendaflokkurinn fyrir **Undirbúningur launaskatts ríkisins** Skýrsla SQL Server Reporting Services (SSRS). Fyrir Bandaríkin eru þrjú gildi í boði: **Karlkyns**, **·**, og **Ótilgreint**. Í **populatePayrollStateWageTaxPrepTmp** aðferð, það er switch setning sem er notuð til að kortleggja gildi **HcmPersonGender** enum í einn af þremur sviðum: **IsMale**, **kvenkyns**, eða **IsUnspecifiedGender**. Sjálfgefið gildi fyrir skiptayfirlýsinguna er **IsUnspecifiedGender**. Ef þú bætir einhverjum gildum við **HcmPersonGender** enum til að kortleggja öðruvísi, verður þú að búa til viðbót með því að nota **Goggunarröð** bekk yfir **populatePayrollStateWageTaxPrepTmp** aðferð til að breyta gildinu eftir þörfum.

## <a name="smmoutlooksync_contact-class"></a>smmOutlookSync_Contact (Class)

The **smmOutlookSync_Contact** samþættingarflokkur tengir gildi til og frá **Horfur** og **Tengiliður**. **Horfur** styður þrjú gildi: **Karlkyns**, **·**, og **Ótilgreint**. Bekkurinn hefur tvær aðferðir til að hjálpa þér að kortleggja **Kyn** til **OutlookGenders**. Sjálfgefin aðferð er **Ósérgreint/Ótilgreint**. Ef þú býrð til viðbótargildi fyrir **Kyn** enum, þú ættir að búa til viðbót með því að nota **Goggunarröð** bekk yfir báðar aðferðir og kort eftir þörfum.
