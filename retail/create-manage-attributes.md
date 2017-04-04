---
title: "Stofna og viðhalda eigind"
description: "Þessi skrá lýsir eigindir í Microsoft Dynamics 365 fyrir Aðgerðir. Eigindir leyfa þér að lýsa afurð og einkennum hennar gegnum notendaskilgreindra svæða."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16461
ms.assetid: 2b85491c-f830-4e79-a2cb-681b7ced6988
ms.search.region: global
ms.search.industry: Retail
ms.author: prabhup
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 26c628e10aaa5f47bc87d7510ca8f41ab3630204
ms.lasthandoff: 03/31/2017


---

# <a name="create-and-manage-attributes"></a>Stofna og viðhalda eigind

Þessi skrá lýsir eigindir í Microsoft Dynamics 365 fyrir Aðgerðir. Eigindir leyfa þér að lýsa afurð og einkennum hennar gegnum notendaskilgreindra svæða.

Eigindir leyfa þér að lýsa afurð og einkennum hennar gegnum notendaskilgreindra svæða. Til dæmis er hægt að tilgreina stærð minnis fyrir vöruna og afkastagetu harða diskinum og gefa til kynna hvort afurðin er í samræmi við Energy star. Eigindir getur verið tengdur við mismunandi smásölueiningar, eins og afurðaflokka og smásölurása, og hægt er að setja sjálfgefin gildi fyrir þær. Afurðir erfa eigindir þeirra og sjálfgefin gildi fyrir þær eigindir þegar þær tengjast afurðaflokka eða smásölurása. Hægt er að hnekkja sjálfgildunum á stigi einstakra afurðar, stigi rásar eða í smásöuvörulista.

#### <a name="examples"></a>Dæmi

Tegund

Eigind

Möguleg gildi eru:

Sjálfgildi

Sjónvarp og myndbönd

Vörumerki

Öll gild **Vörumerki** gildi

Ekkert

Sjónvarp

Stærð skjás

**20"**–**80"**

Ekkert

Lóðrétt upplaus

**480i**, **720p**, **1080i** eða **1080p**

**1080p**

Endurnýjunarhraða skjánum

**60hz**, **120hz** eða **240hz**

**60hz**

HDMI inntök

**0**–**10**

**3**

DVI inntök

**0**–**10**

**1**

Samsettur inntök

**0**–**10**

**2**

Inntök íhluta

**0**–**10**

**1**

LCD

3D Ready

**Já** eða **Nei**

**Já**

3D virkjað

**Já** eða **Nei**

**Nei**

Plasma

Rekstrarhitastig frá

**32**–**110** gráður

**32**

Rekstrarhitastig til

**32**–**110** gráður

**100**

Projection

Ábyrgð á túbuskjá

**6**, **12** eða **18** mánuðir

**12**

\#af Projection Tubes

**1**–**5**

**3**

## <a name="attribute-type"></a>Gerð eigindar
  [![eigindir-fast-afrit](./media/attributes-fixed-copy.png)](./media/attributes-fixed-copy.png) Eigindir eru byggð á gerðir eiginda. Eigindagerðir auðkennir gagnategundina sem hægt er að slá inn fyrir tiltekna eigind. Núna, Microsoft Dynamics 365 aðgerða styður eftirfarandi gerðir eiginda:

-   **Gjaldmiðill** – Þessa eigindargerð styður gildi gjaldmiðils. Hægt er að hafa það afmarkað (þ.e. hægt styðja gildissvið), eða hún getur verið skilið eftir opna.
-   **DateTime** – Þessi eigindagerð styður gildi dagsetningar og tíma. Hægt er að hafa það afmarkað (þ.e. hægt styðja gildissvið), eða hún getur verið skilið eftir opna.
-   **Tugastafir** – Þessa eigindargerð styður númeragildi með tugasætum. Hann styður einnig mælieiningar. Hægt er að hafa það afmarkað (þ.e. hægt styðja gildissvið), eða hún getur verið skilið eftir opna.
-   **heiltala** – Þessa eigindargerð styður gildi númeragildi. Hann styður einnig mælieiningar. Hægt er að hafa það afmarkað (þ.e. hægt styðja gildissvið), eða hún getur verið skilið eftir opna.
-   **Texti** – Þessa eigindargerð styður gildi texta. Hann styður einnig fyrirfram skilgreint sett af möguleg gildi (tölusetning).
-   **Boole-** – Þessa eigindargerð styður tvíundakerfis gildi (**satt**/**false**).
-   **Tilvísun**.

## <a name="attribute"></a>Eigind
  [![createandmanageattribute 8](./media/createandmanageattribute-8.png)](./media/createandmanageattribute-8.png) auk þess heiti, stutt heiti, lýsing, og textinn, eitt eða fleiri af eftirfarandi gerðum upplýsinga getur verið tekin fyrir eigind:

-   Sjálfgildi
-   Lýsigögn eiginda, eins og lýsigögn sem gefur til kynna hvort leita má í eigind, svo sem fínpússa eða raðað

## <a name="attribute-group"></a>Eigindarflokkur
  [![createandmanageattribute 10](./media/createandmanageattribute-10.png)](./media/createandmanageattribute-10.png) Eftir eigindir hafa verið skilgreindar er hægt þær flokkaðar í eigindaflokka. Eigindaflokkar veita flokkanir einstakra eiginda, og hægt að úthluta þeim á smásölutegundir eða smásölurásir.

## <a name="assigning-attribute-groups-to-retail-categories"></a>úthluta eigindahópum á smásöluflokka.
  [![createandmanageattribute 12](./media/createandmanageattribute-12.png)](./media/createandmanageattribute-12.png) Eina eða fleiri eigindaflokkum getur verið tengt tegundahnúta í flokkastigveldi smásöluafurða. Þegar vörur hafa verið flokkaðar, erfa þær eigindir sem eru innifaldar í eigindaflokkana.

## <a name="assigning-attribute-groups-to-retail-stores"></a>Úthluta eigindahópum á smásöluflokka.
  [![createandmanageattribute-13-1024 x 576](./media/createandmanageattribute-13-1024x576.png)](./media/createandmanageattribute-13-1024x576.png) Eina eða fleiri eigindaflokkum er hægt að tengja við einn eða fleiri smásöluverslanir stigveldis verslanir. Þegar vörur hafa verið flokkaðar fyrir tilteknar smásöluverslanir, erfa þær eigindir sem eru innifaldar í eigindaflokkana.

## <a name="overriding-attribute-values"></a>Hnekkja eigindagildum
### <a name="at-the-product-level"></a>Á Afurðastigi

  [![createandmanageattribute-14-1024 x 576](./media/createandmanageattribute-14-1024x576.png)](./media/createandmanageattribute-14-1024x576.png) sjálfgildi eigindir sem hægt er að hnekkja stigi afurð (sem er fyrir einstaka vörur).

### <a name="in-a-retail-catalog"></a>í smásöluvörulista.

  [![createandmanageattribute 2](./media/createandmanageattribute-2.png)](./media/createandmanageattribute-2.png) hægt er að hnekkja sjálfgefnum gildum í eigindir fyrir einstaka vörur í ákveðnum vörulista sem eru ætlaðar fyrir tiltekinna smásölurása.

### <a name="at-the-retail-channel-level"></a>Á stigi smásölurásar

  [![createandmanageattribute 1](./media/createandmanageattribute-1.jpg)](./media/createandmanageattribute-1.jpg) hægt er að hnekkja sjálfgefnum gildum í eigindir fyrir einstaka vörur í ákveðnum vörulista sem eru ætlaðar fyrir tiltekinna smásölurása.


