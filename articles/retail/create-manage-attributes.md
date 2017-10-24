---
title: "Stofna og viðhalda eigind"
description: "Þessi grein lýsir eigindum í Microsoft Dynamics 365 for Retail. Eigindir leyfa þér að lýsa afurð og einkennum hennar gegnum notendaskilgreindra svæða."
author: pdp1207
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16461
ms.assetid: 2b85491c-f830-4e79-a2cb-681b7ced6988
ms.search.region: global
ms.search.industry: Retail
ms.author: prabhup
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: a1a254827051bf37f7b87d1db4ccf09ac47cbbfb
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="create-and-manage-attributes"></a>Stofna og viðhalda eigind

[!include[banner](includes/banner.md)]


Þessi grein lýsir eigindum í Microsoft Dynamics 365 for Retail. Eigindir leyfa þér að lýsa afurð og einkennum hennar gegnum notendaskilgreindra svæða.

Eigindir leyfa þér að lýsa afurð og einkennum hennar gegnum notendaskilgreindra svæða. Til dæmis er hægt að tilgreina stærð minnis fyrir vöruna og afkastagetu harða diskinum og gefa til kynna hvort afurðin er í samræmi við Energy star. Eigindir getur verið tengdur við mismunandi smásölueiningar, eins og afurðaflokka og smásölurása, og hægt er að setja sjálfgefin gildi fyrir þær. Afurðir erfa eigindir þeirra og sjálfgefin gildi fyrir þær eigindir þegar þær tengjast afurðaflokka eða smásölurása. Hægt er að hnekkja sjálfgildunum á stigi einstakra afurðar, stigi rásar eða í smásöuvörulista.

#### <a name="examples"></a>Dæmi

| Tegund   | Eigind                | Möguleg gildi eru:          | Sjálfgildi |
|------------|--------------------------|-----------------------------|---------------|
| Sjónvarp og myndbönd | Vörumerki                    | Öll gild Vörumerki gildi       | Enginn          |
| Sjónvarp         | Stærð skjás              | 20″–80″                     | Enginn          |
| Sjónvarp         | Lóðrétt upplaus      | 480i, 720p, 1080i eða 1080p | 1080p         |
| Sjónvarp         | Endurnýjunarhraða skjánum      | 60hz, 120hz eða 240hz       | 60hz          |
| Sjónvarp         | HDMI inntök              | 0–10                        | 3             |
| Sjónvarp         | DVI inntök               | 0–10                        | 1             |
| Sjónvarp         | Samsettur inntök         | 0–10                        | 2             |
| Sjónvarp         | Inntök íhluta         | 0–10                        | 1             |
| LCD        | 3D Ready                 | Já eða Nei                   | Já           |
| LCD        | 3D virkjað               | Já eða Nei                   | Ekkert            |
| Plasma     | Rekstrarhitastig frá      | 32–110 gráður              | 32            |
| Plasma     | Rekstrarhitastig til        | 32–110 gráður              | 100           |
| Projection | Ábyrgð á túbuskjá | 6, 12 eða 18 mánuðir         | 12            |
| Projection | # túbuskjáa    | 1–5                         | 3             |


## <a name="attribute-type"></a>Gerð eigindar
  [![attributes-fixed-copy](./media/attributes-fixed-copy.png)](./media/attributes-fixed-copy.png) 
  
Eigindir eru byggðar á tegundum eiginda Eigindagerðir auðkennir gagnategundina sem hægt er að slá inn fyrir tiltekna eigind. Eins og er styður Microsoft Dynamics 365 for Retail eftirfarandi gerðir eiginda:

-   **Gjaldmiðill** – Þessa eigindargerð styður gildi gjaldmiðils. Hægt er að hafa það afmarkað (þ.e. hægt styðja gildissvið), eða hún getur verið skilið eftir opna.
-   **DateTime** – Þessi eigindagerð styður gildi dagsetningar og tíma. Hægt er að hafa það afmarkað (þ.e. hægt styðja gildissvið), eða hún getur verið skilið eftir opna.
-   **Tugastafir** – Þessa eigindargerð styður númeragildi með tugasætum. Hann styður einnig mælieiningar. Hægt er að hafa það afmarkað (þ.e. hægt styðja gildissvið), eða hún getur verið skilið eftir opna.
-   **heiltala** – Þessa eigindargerð styður gildi númeragildi. Hann styður einnig mælieiningar. Hægt er að hafa það afmarkað (þ.e. hægt styðja gildissvið), eða hún getur verið skilið eftir opna.
-   **Texti** – Þessa eigindargerð styður gildi texta. Hann styður einnig fyrirfram skilgreint sett af möguleg gildi (tölusetning).
-   **Boole-** – Þessa eigindargerð styður tvíundakerfisgildi (**satt**/**rangt**).
-   **Tilvísun**.

## <a name="attribute"></a>Eigind
  [![CreateAndManageAttribute-8](./media/createandmanageattribute-8.png)](./media/createandmanageattribute-8.png) auk heitis, stutt heiti, lýsing, og hjálpartextinn, eitt eða fleiri af eftirfarandi gerðum upplýsinga getur verið tekin fyrir eigind:

-   Sjálfgildi
-   Lýsigögn eiginda, eins og lýsigögn sem gefur til kynna hvort leita má í eigind, svo sem fínpússa eða raðað

## <a name="attribute-group"></a>Eigindarflokkur
  [![CreateAndManageAttribute-10](./media/createandmanageattribute-10.png)](./media/createandmanageattribute-10.png) Eftir að eigindir hafa verið skilgreindar er hægt þær flokkaðar í eigindaflokka. Eigindaflokkar veita flokkanir einstakra eiginda, og hægt að úthluta þeim á smásölutegundir eða smásölurásir.

## <a name="assigning-attribute-groups-to-retail-categories"></a>úthluta eigindahópum á smásöluflokka.
  [![CreateAndManageAttribute-12](./media/createandmanageattribute-12.png)](./media/createandmanageattribute-12.png) Eina eða fleiri eigindaflokkum getur verið tengt tegundahnúta í flokkastigveldi smásöluafurða. Þegar vörur hafa verið flokkaðar, erfa þær eigindir sem eru innifaldar í eigindaflokkana.

## <a name="assigning-attribute-groups-to-retail-stores"></a>Úthluta eigindahópum á smásöluflokka.
  [![createandmanageattribute-13-1024x576](./media/createandmanageattribute-13-1024x576.png)](./media/createandmanageattribute-13-1024x576.png) Eina eða fleiri eigindaflokkum getur verið tengt tegundahnúta í flokkastigveldi smásöluafurða. Þegar vörur hafa verið flokkaðar fyrir tilteknar smásöluverslanir, erfa þær eigindir sem eru innifaldar í eigindaflokkana.

## <a name="overriding-attribute-values"></a>Hnekkja eigindagildum
### <a name="at-the-product-level"></a>Á Afurðastigi

  [![CreateAndManageAttribute-14](./media/createandmanageattribute-14-1024x576.png)](./media/createandmanageattribute-14-1024x576.png) sjálfgildi eiginda er hægt er að hnekkja á stigi afurðar (þ.e. fyrir einstaka vörur).

### <a name="in-a-retail-catalog"></a>í smásöluvörulista.

  [![CreateAndManageAttribute-2](./media/createandmanageattribute-2.png)](./media/createandmanageattribute-2.png) hægt er að hnekkja sjálfgefnum gildum eiginda fyrir einstaka vörur í ákveðnum vörulista sem eru ætlaðar fyrir tiltekinna smásölurása.

### <a name="at-the-retail-channel-level"></a>Á stigi smásölurásar

  [![CreateAndManageAttribute-1](./media/createandmanageattribute-1.jpg)](./media/createandmanageattribute-1.jpg) hægt er að hnekkja sjálfgefnum gildum eiginda fyrir einstaka vörur í ákveðnum vörulista sem eru ætlaðar fyrir tiltekinna smásölurása.




